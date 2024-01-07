<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <meta
            name="viewport"
            content="width=device-width, initial-scale=1"
        />
        <style>
            /* This is needed because the page cover bleed (100vw) will cause horizontal scrolling */
            /* FIXME: use :has once it is ready for Firefox and lift these back to PageSheetView.module.css */
            html,
            body{
                overflow-x: clip;
            }

            body.theme-overlay {
                position: fixed;
                width: 0;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background-color: var(--theme-overlay-background);
                z-index: 10000;
            }

            .gitbook-splashscreen {
                view-transition-name: splashscreen;
                position: fixed;
                top: 0;
                right: 0;
                bottom: 0;
                left: 0;
                display: flex;
                width: 100%;
                height: 100%;
                z-index: 10000;
            }
            .slate-spacer {
                height: 0;
                color: transparent;
                outline: none;
                position: absolute;
            }

            ::view-transition-old(splashscreen), ::view-transition-new(splashscreen) {
                animation-duration: 300ms;
            }
        </style>
        <title>카카오비즈니스 가이드 - kakao business 비즈니스 가이드</title><link rel="preload" as="font" type="font/woff2" href="https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Bold.woff2?v=3.21" crossorigin="anonymous"/><link rel="preload" as="font" type="font/woff2" href="https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-BoldItalic.woff2?v=3.21" crossorigin="anonymous"/><link rel="preload" as="font" type="font/woff2" href="https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Black.woff2?v=3.21" crossorigin="anonymous"/><link rel="preload" as="font" type="font/woff2" href="https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-BlackItalic.woff2?v=3.21" crossorigin="anonymous"/><link rel="preload" as="font" type="font/woff2" href="https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-SemiBold.woff2?v=3.21" crossorigin="anonymous"/><link rel="preload" as="font" type="font/woff2" href="https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-SemiBoldItalic.woff2?v=3.21" crossorigin="anonymous"/><link rel="preload" as="font" type="font/woff2" href="https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Regular.woff2?v=3.21" crossorigin="anonymous"/><link rel="preload" as="font" type="font/woff2" href="https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Italic.woff2?v=3.21" crossorigin="anonymous"/><style id="__font-SourceSansPro-gitbook-content-font">@font-face {
            font-family: 'gitbook-content-font';
            font-style:  normal;
            font-weight: 700;
            font-display: swap;
            src: local("Source Sans Pro Bold"), local("SourceSansPro-Bold"), url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Bold.woff2?v=3.21") format("woff2"),
                    url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Bold.woff?v=3.21") format("woff");
        }
@font-face {
            font-family: 'gitbook-content-font';
            font-style:  italic;
            font-weight: 700;
            font-display: swap;
            src: local("Source Sans Pro BoldItalic"), local("SourceSansPro-BoldItalic"), url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-BoldItalic.woff2?v=3.21") format("woff2"),
                    url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-BoldItalic.woff?v=3.21") format("woff");
        }
@font-face {
            font-family: 'gitbook-content-font';
            font-style:  normal;
            font-weight: 800;
            font-display: swap;
            src: local("Source Sans Pro Black"), local("SourceSansPro-Black"), url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Black.woff2?v=3.21") format("woff2"),
                    url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Black.woff?v=3.21") format("woff");
        }
@font-face {
            font-family: 'gitbook-content-font';
            font-style:  italic;
            font-weight: 800;
            font-display: swap;
            src: local("Source Sans Pro BlackItalic"), local("SourceSansPro-BlackItalic"), url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-BlackItalic.woff2?v=3.21") format("woff2"),
                    url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-BlackItalic.woff?v=3.21") format("woff");
        }
@font-face {
            font-family: 'gitbook-content-font';
            font-style:  normal;
            font-weight: 500;
            font-display: swap;
            src: local("Source Sans Pro SemiBold"), local("SourceSansPro-SemiBold"), url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-SemiBold.woff2?v=3.21") format("woff2"),
                    url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-SemiBold.woff?v=3.21") format("woff");
        }
@font-face {
            font-family: 'gitbook-content-font';
            font-style:  italic;
            font-weight: 500;
            font-display: swap;
            src: local("Source Sans Pro SemiBoldItalic"), local("SourceSansPro-SemiBoldItalic"), url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-SemiBoldItalic.woff2?v=3.21") format("woff2"),
                    url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-SemiBoldItalic.woff?v=3.21") format("woff");
        }
@font-face {
            font-family: 'gitbook-content-font';
            font-style:  normal;
            font-weight: 400;
            font-display: swap;
            src: local("Source Sans Pro Regular"), local("SourceSansPro-Regular"), url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Regular.woff2?v=3.21") format("woff2"),
                    url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Regular.woff?v=3.21") format("woff");
        }
@font-face {
            font-family: 'gitbook-content-font';
            font-style:  italic;
            font-weight: 400;
            font-display: swap;
            src: local("Source Sans Pro Italic"), local("SourceSansPro-Italic"), url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Italic.woff2?v=3.21") format("woff2"),
                    url("https://app.gitbook.com/public/fonts/SourceSansPro/SourceSansPro-Italic.woff?v=3.21") format("woff");
        }</style><style id="__style-root-primary-color" type="text/css">:root {
                        --custom-theme-color-primary-xxlight: #d5def6;
--custom-theme-color-primary-xlight: #b3c4ee;
--custom-theme-color-primary-light: #7192df;
--custom-theme-color-primary-base: #426DD5;
--custom-theme-color-primary-dark: #425a93;
--custom-theme-color-primary-xdark: #2d3e67;
--custom-theme-color-primary-xxdark: #1f242e;
                  }
            </style><meta name="description" content="당신의 비즈니스에 도움이 되는 다양한 자료를 만나보세요." id="__meta-description"/><meta name="og:description" content="당신의 비즈니스에 도움이 되는 다양한 자료를 만나보세요." id="__meta-og:description"/><meta name="og:image" content="https://app.gitbook.com/share/space/thumbnail/-MVZVmVOd-5LtENUPqdq.png?color=%23426DD5&amp;logo=https%3A%2F%2F3168043928-files.gitbook.io%2F~%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MVZVmVOd-5LtENUPqdq%252Flogo%252FQyhOPTRHle6GksEVFzf3%252F%25E1%2584%2587%25E1%2585%25B5%25E1%2584%258C%25E1%2585%25B3%25E1%2584%2582%25E1%2585%25B5%25E1%2584%2589%25E1%2585%25B3%25E1%2584%2580%25E1%2585%25A1%25E1%2584%258B%25E1%2585%25B5%25E1%2584%2583%25E1%2585%25B3_%25E1%2584%2592%25E1%2585%25A9%25E1%2586%25B7%25E1%2584%2587%25E1%2585%25A5%25E1%2584%2590%25E1%2585%25B3%25E1%2586%25AB.png%3Falt%3Dmedia%26token%3D96877152-3a26-4f42-afa0-f8664a165681&amp;theme=default" id="__meta-og:image"/><meta name="twitter:card" content="summary_large_image" id="__meta-twitter:card"/><meta name="og:title" content="카카오비즈니스 가이드" id="__meta-og:title"/><meta name="twitter:site" content="kakao business 비즈니스 가이드" id="__meta-twitter:site"/><meta name="robots" content="index" id="__meta-robots"/><link rel="icon" href="https://3168043928-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MVZVmVOd-5LtENUPqdq%2Ficon%2FwSKDZq14uNEuXqusdCmN%2Fkakao.png?alt=media&amp;token=30f13b1b-991d-4d5c-97d0-02e1b426d968" id="__link-icon"/><link rel="apple-touch-icon" href="https://3168043928-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MVZVmVOd-5LtENUPqdq%2Ficon%2FwSKDZq14uNEuXqusdCmN%2Fkakao.png?alt=media&amp;token=30f13b1b-991d-4d5c-97d0-02e1b426d968"/><link rel="preload" as="image" href="https://www.gitbook.com/cdn-cgi/image/width=256,dpr=2,height=40,fit=contain,format=auto/https%3A%2F%2F3168043928-files.gitbook.io%2F~%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MVZVmVOd-5LtENUPqdq%252Flogo%252FQyhOPTRHle6GksEVFzf3%252F%25E1%2584%2587%25E1%2585%25B5%25E1%2584%258C%25E1%2585%25B3%25E1%2584%2582%25E1%2585%25B5%25E1%2584%2589%25E1%2585%25B3%25E1%2584%2580%25E1%2585%25A1%25E1%2584%258B%25E1%2585%25B5%25E1%2584%2583%25E1%2585%25B3_%25E1%2584%2592%25E1%2585%25A9%25E1%2586%25B7%25E1%2584%2587%25E1%2585%25A5%25E1%2584%2590%25E1%2585%25B3%25E1%2586%25AB.png%3Falt%3Dmedia%26token%3D96877152-3a26-4f42-afa0-f8664a165681"/><link rel="stylesheet" href="https://app.gitbook.com/public/emojis/emoji-assets-sprite.css?v=6.0.0" type="text/css" media="all"/><link rel="preload" as="image" href="https://3168043928-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-MVZVmVOd-5LtENUPqdq%2F-Ma8cviUkWI2ayhujcav%2F-Ma8d5rJTWO6Iq9Qr6K8%2Finitial_top.png?alt=media&amp;token=38e22c88-ee09-463f-b466-8e34643d1c32"/>
                
                <script type="module" defer src="https://app.gitbook.com/public/app/public-3WJUP54D.min.js?v=10.9.543-362a3f189e923e51f0febd5b45950e2f8ed79baf-7425258621"></script>
                <link as="style" rel="preload" href="https://app.gitbook.com/public/app/public-MHTYWMYW.css?v=10.9.543-362a3f189e923e51f0febd5b45950e2f8ed79baf-7425258621">
                <link rel="stylesheet" href="https://app.gitbook.com/public/app/public-MHTYWMYW.css?v=10.9.543-362a3f189e923e51f0febd5b45950e2f8ed79baf-7425258621">
                <style id="react-native-stylesheet">[stylesheet-group="0"]{}
body{margin:0;}
button::-moz-focus-inner,input::-moz-focus-inner{border:0;padding:0;}
html{-ms-text-size-adjust:100%;-webkit-text-size-adjust:100%;-webkit-tap-highlight-color:rgba(0,0,0,0);}
input::-webkit-search-cancel-button,input::-webkit-search-decoration,input::-webkit-search-results-button,input::-webkit-search-results-decoration{display:none;}
[stylesheet-group="1"]{}
.css-11aywtz{-moz-appearance:textfield;-webkit-appearance:none;background-color:rgba(0,0,0,0.00);border-bottom-left-radius:0px;border-bottom-right-radius:0px;border-top-left-radius:0px;border-top-right-radius:0px;border:0 solid black;box-sizing:border-box;font:14px -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;margin:0px;padding:0px;resize:none;}
.css-175oi2r{align-items:stretch;background-color:rgba(0,0,0,0.00);border:0 solid black;box-sizing:border-box;display:flex;flex-basis:auto;flex-direction:column;flex-shrink:0;list-style:none;margin:0px;min-height:0px;min-width:0px;padding:0px;position:relative;text-decoration:none;z-index:0;}
.css-1qaijid{background-color:rgba(0,0,0,0.00);border:0 solid black;box-sizing:border-box;color:inherit;display:inline;font:inherit;list-style:none;margin:0px;padding:0px;text-align:inherit;text-decoration:none;white-space:inherit;word-wrap:break-word;}
.css-1rynq56{background-color:rgba(0,0,0,0.00);border:0 solid black;box-sizing:border-box;color:rgba(0,0,0,1.00);display:inline;font:14px -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;list-style:none;margin:0px;padding:0px;text-align:inherit;text-decoration:none;white-space:pre-wrap;word-wrap:break-word;}
.css-9pa8cd{bottom:0px;height:100%;left:0px;opacity:0;position:absolute;right:0px;top:0px;width:100%;z-index:-1;}
[stylesheet-group="2"]{}
.r-1064s9p{margin:4px;}
.r-117ykcp{border-bottom-color:var(--sp-color-border-base);border-left-color:var(--sp-color-border-base);border-right-color:var(--sp-color-border-base);border-top-color:var(--sp-color-border-base);}
.r-11mg6pl{border-bottom-color:rgba(255,255,255,1.00);border-left-color:rgba(255,255,255,1.00);border-right-color:rgba(255,255,255,1.00);border-top-color:rgba(255,255,255,1.00);}
.r-13awgt0{flex:1;}
.r-13fxbef{border-bottom-color:rgba(211,61,61,1.00);border-left-color:rgba(211,61,61,1.00);border-right-color:rgba(211,61,61,1.00);border-top-color:rgba(211,61,61,1.00);}
.r-1471scf{display:inline;}
.r-156hn8l{border-bottom-color:rgba(211,220,228,1.00);border-left-color:rgba(211,220,228,1.00);border-right-color:rgba(211,220,228,1.00);border-top-color:rgba(211,220,228,1.00);}
.r-17gur6a{border-bottom-left-radius:0px;border-bottom-right-radius:0px;border-top-left-radius:0px;border-top-right-radius:0px;}
.r-18c69zk{border-bottom-left-radius:100px;border-bottom-right-radius:100px;border-top-left-radius:100px;border-top-right-radius:100px;}
.r-190qawg{border-bottom-color:rgba(227,232,237,1.00);border-left-color:rgba(227,232,237,1.00);border-right-color:rgba(227,232,237,1.00);border-top-color:rgba(227,232,237,1.00);}
.r-19dn8jc{border-bottom-color:rgba(104,60,17,1.00);border-left-color:rgba(104,60,17,1.00);border-right-color:rgba(104,60,17,1.00);border-top-color:rgba(104,60,17,1.00);}
.r-1awa8pu{border-bottom-color:rgba(101,119,134,1.00);border-left-color:rgba(101,119,134,1.00);border-right-color:rgba(101,119,134,1.00);border-top-color:rgba(101,119,134,1.00);}
.r-1c57tb8{border-bottom-left-radius:34px;border-bottom-right-radius:34px;border-top-left-radius:34px;border-top-right-radius:34px;}
.r-1d4xg89{border-bottom-color:rgba(170,184,194,1.00);border-left-color:rgba(170,184,194,1.00);border-right-color:rgba(170,184,194,1.00);border-top-color:rgba(170,184,194,1.00);}
.r-1dqxon3{overflow-x:auto;overflow-y:auto;}
.r-1e1rmqb{border-bottom-color:rgba(213,222,246,1.00);border-left-color:rgba(213,222,246,1.00);border-right-color:rgba(213,222,246,1.00);border-top-color:rgba(213,222,246,1.00);}
.r-1edjr5w{padding:80px;}
.r-1fdo3w0{margin:16px;}
.r-1fuqb1j{border-bottom-left-radius:24px;border-bottom-right-radius:24px;border-top-left-radius:24px;border-top-right-radius:24px;}
.r-1j16mh1{border-bottom-left-radius:100%;border-bottom-right-radius:100%;border-top-left-radius:100%;border-top-right-radius:100%;}
.r-1jkafct{border-bottom-left-radius:2px;border-bottom-right-radius:2px;border-top-left-radius:2px;border-top-right-radius:2px;}
.r-1jyn79y{border-bottom-color:rgba(0,150,136,1.00);border-left-color:rgba(0,150,136,1.00);border-right-color:rgba(0,150,136,1.00);border-top-color:rgba(0,150,136,1.00);}
.r-1p0fg95{border-bottom-color:rgba(245,247,249,1.00);border-left-color:rgba(245,247,249,1.00);border-right-color:rgba(245,247,249,1.00);border-top-color:rgba(245,247,249,1.00);}
.r-1phboty{border-bottom-style:solid;border-left-style:solid;border-right-style:solid;border-top-style:solid;}
.r-1rwzld0{border-bottom-color:rgba(11,79,47,1.00);border-left-color:rgba(11,79,47,1.00);border-right-color:rgba(11,79,47,1.00);border-top-color:rgba(11,79,47,1.00);}
.r-1udh08x{overflow-x:hidden;overflow-y:hidden;}
.r-1ufqoot{border-bottom-color:rgba(20,23,28,1.00);border-left-color:rgba(20,23,28,1.00);border-right-color:rgba(20,23,28,1.00);border-top-color:rgba(20,23,28,1.00);}
.r-1w1o3af{border-bottom-color:rgba(251,232,240,1.00);border-left-color:rgba(251,232,240,1.00);border-right-color:rgba(251,232,240,1.00);border-top-color:rgba(251,232,240,1.00);}
.r-1wgstfn{border-bottom-style:none;border-left-style:none;border-right-style:none;border-top-style:none;}
.r-1x0lp8v{border-bottom-color:rgba(220,238,244,1.00);border-left-color:rgba(220,238,244,1.00);border-right-color:rgba(220,238,244,1.00);border-top-color:rgba(220,238,244,1.00);}
.r-1xc7w19{border-bottom-color:rgba(0,0,0,1.00);border-left-color:rgba(0,0,0,1.00);border-right-color:rgba(0,0,0,1.00);border-top-color:rgba(0,0,0,1.00);}
.r-1xfd6ze{border-bottom-left-radius:8px;border-bottom-right-radius:8px;border-top-left-radius:8px;border-top-right-radius:8px;}
.r-1xutcf9{padding:40px;}
.r-1yadl64{border-bottom-width:0px;border-left-width:0px;border-right-width:0px;border-top-width:0px;}
.r-42olwf{border-bottom-color:rgba(0,0,0,0.00);border-left-color:rgba(0,0,0,0.00);border-right-color:rgba(0,0,0,0.00);border-top-color:rgba(0,0,0,0.00);}
.r-4a18lf{border-bottom-color:rgba(255,0,0,1.00);border-left-color:rgba(255,0,0,1.00);border-right-color:rgba(255,0,0,1.00);border-top-color:rgba(255,0,0,1.00);}
.r-4qtqp9{display:inline-block;}
.r-60ke3l{border-bottom-color:rgba(0,128,0,1.00);border-left-color:rgba(0,128,0,1.00);border-right-color:rgba(0,128,0,1.00);border-top-color:rgba(0,128,0,1.00);}
.r-6578ry{margin:40px;}
.r-6koalj{display:flex;}
.r-6ncur5{border-bottom-left-radius:18px;border-bottom-right-radius:18px;border-top-left-radius:18px;border-top-right-radius:18px;}
.r-6t2glc{border-bottom-left-radius:40px;border-bottom-right-radius:40px;border-top-left-radius:40px;border-top-right-radius:40px;}
.r-81s47e{border-bottom-color:rgba(66,109,213,1.00);border-left-color:rgba(66,109,213,1.00);border-right-color:rgba(66,109,213,1.00);border-top-color:rgba(66,109,213,1.00);}
.r-9x6qib{border-bottom-color:rgba(204,214,221,1.00);border-left-color:rgba(204,214,221,1.00);border-right-color:rgba(204,214,221,1.00);border-top-color:rgba(204,214,221,1.00);}
.r-ancj0c{border-bottom-color:rgba(218,212,255,1.00);border-left-color:rgba(218,212,255,1.00);border-right-color:rgba(218,212,255,1.00);border-top-color:rgba(218,212,255,1.00);}
.r-by8dw1{margin:24px;}
.r-bztko3{overflow-x:visible;overflow-y:visible;}
.r-cdmcib{border-bottom-left-radius:3px;border-bottom-right-radius:3px;border-top-left-radius:3px;border-top-right-radius:3px;}
.r-cpet4d{border-bottom-left-radius:999px;border-bottom-right-radius:999px;border-top-left-radius:999px;border-top-right-radius:999px;}
.r-crgep1{margin:0px;}
.r-d045u9{border-bottom-width:2px;border-left-width:2px;border-right-width:2px;border-top-width:2px;}
.r-d23pfw{padding:24px;}
.r-dta0w2{flex:2;}
.r-edyy15{padding:8px;}
.r-eg6o18{border-bottom-style:dashed;border-left-style:dashed;border-right-style:dashed;border-top-style:dashed;}
.r-egco7n{border-bottom-color:rgba(253,195,137,1.00);border-left-color:rgba(253,195,137,1.00);border-right-color:rgba(253,195,137,1.00);border-top-color:rgba(253,195,137,1.00);}
.r-fx7oqy{border-bottom-color:rgba(0,0,255,1.00);border-left-color:rgba(0,0,255,1.00);border-right-color:rgba(0,0,255,1.00);border-top-color:rgba(0,0,255,1.00);}
.r-hvic4v{display:none;}
.r-hwh8t1{margin:8px;}
.r-jqra5g{border-bottom-color:rgba(55,65,81,1.00);border-left-color:rgba(55,65,81,1.00);border-right-color:rgba(55,65,81,1.00);border-top-color:rgba(55,65,81,1.00);}
.r-jxo161{border-bottom-color:rgba(255,204,203,1.00);border-left-color:rgba(255,204,203,1.00);border-right-color:rgba(255,204,203,1.00);border-top-color:rgba(255,204,203,1.00);}
.r-kdyh1x{border-bottom-left-radius:6px;border-bottom-right-radius:6px;border-top-left-radius:6px;border-top-right-radius:6px;}
.r-krxsd3{display:-webkit-box;}
.r-m2nopt{border-bottom-color:rgba(43,46,57,1.00);border-left-color:rgba(43,46,57,1.00);border-right-color:rgba(43,46,57,1.00);border-top-color:rgba(43,46,57,1.00);}
.r-m7id7e{flex:unset;}
.r-m9k8lk{border-bottom-color:rgba(223,255,240,1.00);border-left-color:rgba(223,255,240,1.00);border-right-color:rgba(223,255,240,1.00);border-top-color:rgba(223,255,240,1.00);}
.r-nsbfu8{padding:16px;}
.r-p4pd8u{border-bottom-color:rgba(36,42,49,1.00);border-left-color:rgba(36,42,49,1.00);border-right-color:rgba(36,42,49,1.00);border-top-color:rgba(36,42,49,1.00);}
.r-qwd59z{border-bottom-left-radius:1px;border-bottom-right-radius:1px;border-top-left-radius:1px;border-top-right-radius:1px;}
.r-rs99b7{border-bottom-width:1px;border-left-width:1px;border-right-width:1px;border-top-width:1px;}
.r-t60dpp{padding:0px;}
.r-texgdz{margin:80px;}
.r-tuq35u{padding:4px;}
.r-tyhe3k{border-bottom-left-radius:64px;border-bottom-right-radius:64px;border-top-left-radius:64px;border-top-right-radius:64px;}
.r-xoduu5{display:inline-flex;}
.r-xyw6el{padding:12px;}
.r-ywje51{margin:auto;}
.r-z2wwpe{border-bottom-left-radius:4px;border-bottom-right-radius:4px;border-top-left-radius:4px;border-top-right-radius:4px;}
.r-zhp00w{padding:2px;}
[stylesheet-group="2.1"]{}
.r-10x3wzx{padding-bottom:40px;padding-top:40px;}
.r-11yq8vr{margin-left:40px;margin-right:40px;}
.r-1e081e0{padding-left:12px;padding-right:12px;}
.r-1guathk{padding-left:24px;padding-right:24px;}
.r-1h4fu65{padding-bottom:24px;padding-top:24px;}
.r-1hy1u7s{margin-left:24px;margin-right:24px;}
.r-1isdzm1{padding-left:80px;padding-right:80px;}
.r-1jgb5lz{margin-left:auto;margin-right:auto;}
.r-1p02zvt{padding-left:48px;padding-right:48px;}
.r-1p4rafz{padding-left:2px;padding-right:2px;}
.r-1p6iasa{margin-bottom:4px;margin-top:4px;}
.r-1pn2ns4{padding-left:8px;padding-right:8px;}
.r-1r5su4o{margin-bottom:16px;margin-top:16px;}
.r-1unineu{margin-bottom:40px;margin-top:40px;}
.r-1w3m5we{padding-bottom:80px;padding-top:80px;}
.r-1ybube5{margin-left:8px;margin-right:8px;}
.r-1ydw1k6{margin-left:16px;margin-right:16px;}
.r-1yzf0co{padding-bottom:16px;padding-top:16px;}
.r-4amgru{margin-left:4px;margin-right:4px;}
.r-5njf8e{padding-bottom:8px;padding-top:8px;}
.r-5wp0in{padding-left:40px;padding-right:40px;}
.r-c8eef1{margin-bottom:8px;margin-top:8px;}
.r-g4w12b{padding-left:94px;padding-right:94px;}
.r-g8va3u{margin-left:80px;margin-right:80px;}
.r-mk0yit{padding-left:0px;padding-right:0px;}
.r-mvpalk{margin-left:0px;margin-right:0px;}
.r-oyd9sg{padding-bottom:4px;padding-top:4px;}
.r-pw2am6{margin-bottom:24px;margin-top:24px;}
.r-r0h9e2{margin-bottom:0px;margin-top:0px;}
.r-r26ds4{margin-bottom:80px;margin-top:80px;}
.r-rjfia{padding-bottom:0px;padding-top:0px;}
.r-s1qlax{padding-left:4px;padding-right:4px;}
.r-ymttw5{padding-left:16px;padding-right:16px;}
[stylesheet-group="2.2"]{}
.r-100vyta{margin-top:7px;}
.r-1029d6i{top:-24px;}
.r-105ug2t{pointer-events:auto!important;}
.r-109y4c4{height:1px;}
.r-10kz8ia{color:rgba(228,79,137,1.00);}
.r-10ptun7{height:16px;}
.r-10pyoum{color:rgba(5,5,5,1.00);}
.r-10x49cs{font-size:10px;}
.r-10xqauy{padding-top:env(safe-area-inset-top);}
.r-111w7nw{box-shadow:0px 1px 2px rgba(0,0,0,0.69);}
.r-113qch9{cursor:auto;}
.r-116b19x{padding-left:40px;}
.r-119vxgs{border-top-style:dashed;}
.r-11c0sde{margin-top:24px;}
.r-11f42r{height:314px;}
.r-11g3r6m{padding-right:24px;}
.r-11j9u27{visibility:hidden;}
.r-11mo1y0{margin-bottom:7px;}
.r-11mpjr4{background-color:rgba(223,223,223,1.00);}
.r-11udlyb{background-color:rgba(0,150,136,1.00);}
.r-11vxtcu{background-color:rgba(211,220,228,1.00);}
.r-11wrixw{margin-left:0px;}
.r-11xdecz{max-width:233px;}
.r-11yh6sk{overflow-x:hidden;}
.r-11ys0m{-webkit-break-before:auto;break-before:auto;}
.r-123mryc{color:rgba(185,94,4,1.00);}
.r-127358a{animation-name:r-9p3sdl;}
.r-127gp16{max-width:150px;}
.r-12dqhl9{height:calc(100vh - 80px);}
.r-12mrs02{object-fit:contain;}
.r-12vffkv>*{pointer-events:auto;}
.r-12vffkv{pointer-events:none!important;}
.r-12ym1je{width:18px;}
.r-12zb1j4{margin-right:7px;}
.r-135wba7{line-height:24px;}
.r-13gfk22{animation-delay:250ms;}
.r-13hce6t{margin-left:4px;}
.r-13i40vn{box-shadow:0px 12px 13px rgba(0,0,0,0.02);}
.r-13l2t4g{border-right-width:1px;}
.r-13ll0g2{color:rgba(10,48,105,1.00);}
.r-13lvk87{margin-left:110px;}
.r-13qz1uu{width:100%;}
.r-13tjlyg{transition-duration:0.1s;}
.r-13yce4e{border-top-width:0px;}
.r-142tt33{-webkit-text-decoration-line:line-through;text-decoration-line:line-through;}
.r-144uupt{left:2px;}
.r-146iojx{max-width:300px;}
.r-146vlhe{color:rgba(66,109,213,1.00);}
.r-1472mwg{height:24px;}
.r-14bkmb3{bottom:-3px;}
.r-14eup4l{top:3px;}
.r-14gqq1x{margin-top:4px;}
.r-14lw9ot{background-color:rgba(255,255,255,1.00);}
.r-14sbq61{background-color:rgba(33,150,243,1.00);}
.r-14utu6a{line-height:8px;}
.r-14vq63g{background-color:rgba(3,58,22,1.00);}
.r-14yzgew{line-height:18px;}
.r-150rngu{-webkit-overflow-scrolling:touch;}
.r-157h22z{background-color:rgba(45,50,58,1.00);}
.r-15g7tld{margin-bottom:80px;}
.r-15m1z73{margin-left:40px;}
.r-15m68ww{color:rgba(137,198,218,1.00);}
.r-15o5oer{bottom:auto;}
.r-15ysp7h{min-height:32px;}
.r-15zivkp{margin-bottom:4px;}
.r-16dba41{font-weight:400;}
.r-16et402{color:var(--sp-color-text-light);}
.r-16l9doz{height:auto;}
.r-16y2uox{flex-grow:1;}
.r-173mn98{align-self:flex-end;}
.r-1777fci{justify-content:center;}
.r-17bb2tj{animation-duration:0.75s;}
.r-17giqoz{box-shadow:0px 0px 7px rgba(0,0,0,0.52);}
.r-17grq5a{margin-right:-8px;}
.r-17leim2{background-repeat:repeat;}
.r-17mnkfo{background-color:var(--sp-color-button-upgrade-bg-default);}
.r-17rnw9f{line-height:30px;}
.r-17s6mgv{justify-content:flex-end;}
.r-17tb59b{opacity:0.7;}
.r-17tloay{opacity:0.6;}
.r-17wrw06{color:rgba(180,26,26,1.00);}
.r-184en5c{z-index:1;}
.r-18ayb63{border-right-color:rgba(227,232,237,1.00);}
.r-18kxxzh{flex-grow:0;}
.r-18nhz7w{top:-3px;}
.r-18p6if4{border-right-width:2px;}
.r-18u37iz{flex-direction:row;}
.r-18y5qoh{color:rgba(165,214,255,1.00);}
.r-190thrv{color:rgba(145,75,5,1.00);}
.r-19554kt{width:90px;}
.r-19akecc{color:rgba(175,245,180,1.00);}
.r-19byhck{flex-basis:32%;}
.r-19lq7b1{top:16px;}
.r-19r33im{letter-spacing:1.2px;}
.r-19tq15n{margin-top:80px;}
.r-19wmn03{width:20px;}
.r-19z077z{touch-action:none;}
.r-1a3cspq{background-color:rgba(40,49,67,1.00);}
.r-1abnn5w{animation-play-state:paused;}
.r-1acpoxo{width:36px;}
.r-1adewhw{padding-bottom:76px;}
.r-1aerykh{border-top-color:rgba(211,220,228,1.00);}
.r-1ais5m6{transform:rotate(90deg);}
.r-1aockid{width:40px;}
.r-1armvtb{font-size:8px;}
.r-1awozwy{align-items:center;}
.r-1axcl7z{border:1px solid #d3dce4;}
.r-1ay1djp{animation-duration:1s;}
.r-1b00too{background-color:rgba(236,239,241,1.00);}
.r-1b096ap{border-bottom-color:rgba(36,42,49,1.00);}
.r-1b1g84l{bottom:-8px;}
.r-1b43r93{font-size:14px;}
.r-1bcbbo8{color:rgba(17,99,41,1.00);}
.r-1bnj018{color:rgba(92,105,117,1.00);}
.r-1c681wc{color:rgba(77,222,152,1.00);}
.r-1c6unfx{forced-color-adjust:none;}
.r-1ce3o0f{max-height:80vh;}
.r-1ceczpf{min-height:24px;}
.r-1clhhh9{-moz-transition-property:all;-webkit-transition-property:all;transition-property:all;}
.r-1cmwbt1{gap:8px;}
.r-1d09ksm{align-items:baseline;}
.r-1d2f490{left:0px;}
.r-1d4mawv{margin-right:4px;}
.r-1d5kdc7{flex-direction:column-reverse;}
.r-1d7fvdj{justify-content:space-evenly;}
.r-1d9grui{border-bottom-color:rgba(211,220,228,1.00);}
.r-1ddef8g{-webkit-text-decoration-line:underline;text-decoration-line:underline;}
.r-1dernwh{height:70%;}
.r-1dlgt49{max-height:30px;}
.r-1dmvmgl{background-color:rgba(36,42,49,1.00);}
.r-1dn12g7{line-height:48px;}
.r-1dpl46z{border-bottom-right-radius:4px;}
.r-1dqbpge{cursor:text;}
.r-1dumtqg{background-color:rgba(253,195,137,1.00);}
.r-1efo1hp{border-bottom-color:rgba(43,46,57,1.00);}
.r-1ei5mc7{cursor:inherit;}
.r-1eic64l{color:rgba(198,44,104,1.00);}
.r-1enofrn{font-size:12px;}
.r-1etwnyc{color:rgba(113,146,223,1.00);}
.r-1euycsn{flex-direction:row-reverse;}
.r-1ewcgjf{box-shadow:0px 1px 3px rgba(0,0,0,0.5);}
.r-1f2v84d{color:rgba(204,207,212,1.00);}
.r-1f529hi{line-height:14px;}
.r-1f77ubx{padding-bottom:var(--sp-spacing-300);}
.r-1fd96xs{padding-left:50px;}
.r-1fe0xdi{left:0%;}
.r-1ff274t{text-align:right;}
.r-1fi01yr{background-color:rgba(55,65,81,1.00);}
.r-1fiaf3z{opacity:0.05;}
.r-1fo40xd{top:80px;}
.r-1fq43b1{flex-basis:100%;}
.r-1g7fiml{height:30px;}
.r-1g80fh1{margin-right:80px;}
.r-1gigy5k{border-bottom-color:rgba(45,50,58,1.00);}
.r-1glc72y{border-bottom-color:rgba(245,247,249,1.00);}
.r-1glkqn6{width:80px;}
.r-1h0z5md{justify-content:flex-start;}
.r-1h2t8mc{width:0px;}
.r-1h815vi{right:92%;}
.r-1h8ys4a{padding-top:4px;}
.r-1habvwh{align-items:flex-start;}
.r-1hjwoze{height:18px;}
.r-1hlnpa{height:3px;}
.r-1hpgsb4{;}
.r-1hqdnve{box-shadow:0px 0px 4px inset rgba(0,0,0, 0.08);}
.r-1hrvmjx{border-top-color:rgba(55,65,81,1.00);}
.r-1hvjb8t{padding-right:4px;}
.r-1hy97zq{padding-top:80px;}
.r-1i6wzkk{-moz-transition-property:opacity;-webkit-transition-property:opacity;transition-property:opacity;}
.r-1i7sdiz{box-shadow:0px 4px 10px rgba(0,0,0,0.05);}
.r-1i93rbr{right:0%;}
.r-1iadl42{background-color:var(--sp-color-bg-standout-base);}
.r-1ielgck{animation-duration:300ms;}
.r-1ifxtd0{margin-bottom:16px;}
.r-1ill06b{color:rgba(179,196,238,1.00);}
.r-1iln25a{word-wrap:normal;}
.r-1ioqa4e{border-top-right-radius:7px;}
.r-1ipicw7{width:300px;}
.r-1j7aebl{width:880px;}
.r-1janqcz{width:16px;}
.r-1jg9483{width:8px;}
.r-1jj8364{margin-left:auto;}
.r-1jkjb{margin-left:8px;}
.r-1jnzvcq{padding-bottom:80px;}
.r-1jocfgc{width:290px;}
.r-1jpmnxg{word-wrap:anywhere;}
.r-1jxfwug{border-top-width:2px;}
.r-1k25im9{height:26px;}
.r-1kb76zh{margin-right:8px;}
.r-1kf75xu{color:rgba(12,105,61,1.00);}
.r-1kfrs79{font-weight:600;}
.r-1kihuf0{align-self:center;}
.r-1kjq87h{width:376px;}
.r-1knl56f{animation-name:r-1hunrpy;}
.r-1kvn7zp{max-height:150px;}
.r-1l0m7dr{background-image:radial-gradient(rgba(0, 0, 0, 0.1), #ffffff);}
.r-1l7z4oj{padding-bottom:16px;}
.r-1l94q7l{box-shadow:inset 0px 0px 1px rgb(0 0 0 / 30%);}
.r-1ld3bg{top:-4px;}
.r-1ldzwu0{animation-timing-function:linear;}
.r-1ljd8xs{border-left-width:1px;}
.r-1lky6n1{background-color:rgba(227,232,237,1.00);}
.r-1lnfjr6{-webkit-background-clip:text;}
.r-1lnt56z{color:rgba(211,220,228,1.00);}
.r-1loqt21{cursor:pointer;}
.r-1m04atk{padding-left:8px;}
.r-1m4drjs{top:-6px;}
.r-1maqer6{max-width:860px;}
.r-1mdbw0j{padding-bottom:0px;}
.r-1mdsxwj{color:rgba(237,159,81,1.00);}
.r-1mgmw1x{background-image:linear-gradient(90deg, #5f45ff, #442fc8);}
.r-1mhb1uw{width:42px;}
.r-1mhtwjo{left:-3px;}
.r-1mlwlqe{flex-basis:auto;}
.r-1mnahxq{margin-top:0px;}
.r-1moh23t{bottom:16px;}
.r-1mrlafo{background-position:0;}
.r-1ms9ukt{bottom:-5px;}
.r-1mtwht8{color:rgba(210,168,255,1.00);}
.r-1muvv40{animation-iteration-count:infinite;}
.r-1n20pny{width:140px;}
.r-1n6k3lk{color:rgba(36,42,49,1.00);}
.r-1na1l7e{animation-play-state:running;}
.r-1nf4jbm{color:rgba(59,69,78,1.00);}
.r-1niwhzg{background-color:rgba(0,0,0,0.00);}
.r-1nj16ve{left:-10px;}
.r-1nlw0im{bottom:8px;}
.r-1nnq5pb{background-color:var(--sp-color-bg-base);}
.r-1ny4l3l{outline-style:none;}
.r-1o2nx2a{font-weight:360;}
.r-1ocf4r9{scroll-snap-type:y mandatory;}
.r-1odw9d6{background-color:rgba(20,23,28,1.00);}
.r-1oec5bt{opacity:0.2;}
.r-1oep0n4{left:-12px;}
.r-1ois7e2{color:rgba(55,65,81,1.00);}
.r-1or9b2r{height:10px;}
.r-1osy6ei{color:rgba(255,220,215,1.00);}
.r-1oszu61{align-items:stretch;}
.r-1otgn73{touch-action:manipulation;}
.r-1ow6zhx{margin-left:16px;}
.r-1p0dtai{bottom:0px;}
.r-1p5i0ed{bottom:-24px;}
.r-1p69tiw{border-top-color:rgba(43,46,57,1.00);}
.r-1pa6394{color:var(--sp-color-text-muted);}
.r-1peese0{margin-bottom:24px;}
.r-1ph75f1{height:80px;}
.r-1pi2tsx{height:100%;}
.r-1pl7oy7{min-height:48px;}
.r-1ptriwd{right:2px;}
.r-1pyaxff{padding-right:8px;}
.r-1q142lx{flex-shrink:0;}
.r-1q6rxnj{padding-right:110px;}
.r-1q77oe7{background-color:rgba(171,183,202,1.00);}
.r-1q9ho9q{color:rgba(48,127,152,1.00);}
.r-1q9jyb7{-webkit-filter:blur(16px) contrast(110%) hue-rotate(10deg) brightness(1.2) saturate(1.2);filter:blur(16px) contrast(110%) hue-rotate(10deg) brightness(1.2) saturate(1.2);}
.r-1qc3rpd{transform:scaleY(-1);}
.r-1qd0xha{font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;}
.r-1qdbj55{animation-name:r-ndfo3d;}
.r-1qefu2b{right:-3px;}
.r-1qhn6m8{padding-left:16px;}
.r-1qipmxq{color:var(--sp-color-button-upgrade-text);}
.r-1quu1zo{;}
.r-1r0uwd5{color:rgba(255,166,87,1.00);}
.r-1r3mtb5{border-bottom-color:rgba(20,23,28,1.00);}
.r-1r74h94{left:8px;}
.r-1r8g8re{height:36px;}
.r-1rasi3h{color:rgba(136,153,168,1.00);}
.r-1rbj2e8{outline-color:#f5f7f9;}
.r-1rdth4h{border-left-color:rgba(55,65,81,1.00);}
.r-1rho1gz{box-shadow:0px 12px 13px rgba(0,0,0,0.12);}
.r-1rkdych{max-width:1040px;}
.r-1rla0r3{background-image:linear-gradient(90deg, #d33d3d, #b41a1a);}
.r-1rnoaur{overflow-y:auto;}
.r-1ro0kt6{flex-basis:0%;}
.r-1ro7rbe{right:100%;}
.r-1rttkqs{width:400px;}
.r-1s3egr7{z-index:100;}
.r-1s8p94s{max-width:832px;}
.r-1sncvnh{transform:translateZ(0px);}
.r-1sxrcry{background-size:auto;}
.r-1t2qqvi{flex-basis:50%;}
.r-1t7uo4s{object-fit:cover;}
.r-1t8m4kl{text-shadow:0px 0px 3px rgba(36,42,49,1.00);}
.r-1tazni7{cursor:not-allowed;}
.r-1ts5s6y{aspect-ratio:1.7777777777777777;}
.r-1ttybm1{border-top-color:rgba(45,50,58,1.00);}
.r-1tymxbh{box-shadow:5px 0px 7px rgba(36,42,49,0.60);}
.r-1u9v6se{color:rgba(39,85,100,1.00);}
.r-1ua3vzd{background-color:rgba(223,255,240,1.00);}
.r-1ub1aon{transform:translateY(100%);}
.r-1udbk01{text-overflow:ellipsis;}
.r-1ufdtu9{background-image:linear-gradient(270deg, #e3e8ed 10%, #f5f7f9, #e3e8ed 90%);}
.r-1ufr4wv{z-index:9;}
.r-1ui5ee8{font-size:32px;}
.r-1ul06mb{margin-left:32px;}
.r-1ulgld5{color:rgba(255,123,114,1.00);}
.r-1um4q9x{-moz-transition:opacity 800ms ease;-webkit-transition:opacity 800ms ease;transition:opacity 800ms ease;}
.r-1uql0sn{top:-1.2em;}
.r-1ur9v65{padding-top:40px;}
.r-1ut4w64{margin-bottom:-1px;}
.r-1uwte3a{padding-bottom:40px;}
.r-1uybibz{border-bottom-color:rgba(66,109,213,1.00);}
.r-1uypc71{animation-timing-function:ease-in;}
.r-1v2oles{top:50%;}
.r-1v7sw2p{background-size:50% 80px;}
.r-1vamr63{max-width:720px;}
.r-1vckr1u{background-color:rgba(245,247,249,1.00);}
.r-1vex5ub{color:rgba(68,47,200,1.00);}
.r-1vutw0s{background-color:rgba(103,6,12,1.00);}
.r-1vzi8xi{vertical-align:middle;}
.r-1w2pmg{height:0px;}
.r-1w5p360{border-top-color:rgba(66,109,213,1.00);}
.r-1w6e6rj{flex-wrap:wrap;}
.r-1wbh5a2{flex-shrink:1;}
.r-1wezhl{margin-left:80px;}
.r-1wfhzrg{height:120px;}
.r-1wghi3f{top:-8px;}
.r-1wtj0ep{justify-content:space-between;}
.r-1wv73ep{align-self:baseline;}
.r-1ww30s9{max-width:30px;}
.r-1wyyakw{z-index:-1;}
.r-1wzrnnt{margin-top:16px;}
.r-1x35g6{font-size:24px;}
.r-1xbve24{height:6px;}
.r-1xcajam{position:fixed;}
.r-1xnzce8{-moz-user-select:text;-webkit-user-select:text;user-select:text;}
.r-1xoqk23{background-color:rgba(68,47,200,1.00);}
.r-1xsj5db{background-color:var(--sp-color-sidesheet-list-item-bg-hover);}
.r-1y0r55a{background-image:radial-gradient(rgba(255, 255, 255, 0.1), #14171c);}
.r-1y14msn{border-bottom-color:rgba(55,65,81,1.00);}
.r-1y9xkqr{left:8%;}
.r-1yb8zos{background-color:rgba(162,169,185,1.00);}
.r-1ybp48z{background-image:linear-gradient(90deg, #cc3131, #b41a1a);}
.r-1ye8kvj{max-width:600px;}
.r-1ygmrgt{padding-top:24px;}
.r-1yv4afn{border-top-color:rgba(227,232,237,1.00);}
.r-1yvhtrz{width:32px;}
.r-1yxedwg{top:8px;}
.r-1yyzdbt{border-left-color:rgba(227,232,237,1.00);}
.r-257lmc{width:1180px;}
.r-2atnlg{background-color:rgba(78,170,200,1.00);}
.r-2awvau{min-width:-webkit-max-content;min-width:-moz-max-content;min-width:max-content;}
.r-2eszeu::-webkit-scrollbar{display:none}
.r-2eszeu{scrollbar-width:none;}
.r-2fm7cc{color:rgba(139,148,158,1.00);}
.r-2fw26j{outline-offset:0px;}
.r-2jelyo{background-color:rgba(24,28,31,1.00);}
.r-2jxp4q{background-color:rgba(34,39,46,1.00);}
.r-2kxcpj{inset:0px;}
.r-2llsf{min-height:100%;}
.r-2o02ov{margin-top:40px;}
.r-2tavb8{background-color:rgba(0,0,0,0.60);}
.r-2yi16{min-height:36px;}
.r-2zpn8w{-webkit-break-inside:avoid;break-inside:avoid;}
.r-30o5oe{-moz-appearance:none;-ms-appearance:none;-webkit-appearance:none;appearance:none;}
.r-30qeir{bottom:-4px;}
.r-36ujnk{font-style:italic;}
.r-37p410{color:var(--sp-color-text-base);}
.r-37tt59{line-height:32px;}
.r-3da1kt{height:8px;}
.r-3dgjpp{border-top-color:rgba(36,42,49,1.00);}
.r-3hw5f6{color:rgba(149,56,0,1.00);}
.r-3kxdz0{outline-color:#286A7F;}
.r-3mc0re{right:8px;}
.r-3mtglp{row-gap:16px;}
.r-3o833n{background-color:rgba(251,232,240,1.00);}
.r-3pxcvb{border-bottom-color:rgba(255,255,255,1.00);}
.r-3s2u2q{white-space:nowrap;}
.r-417010{z-index:0;}
.r-432wen{width:3px;}
.r-44c749{border-bottom-left-radius:7px;}
.r-469pgu{border-right-color:rgba(66,109,213,1.00);}
.r-47i0zk{background-image:radial-gradient(rgba(0, 0, 0, 0.1), #14171c);}
.r-493a2x{width:680px;}
.r-4dj0k7{box-shadow:0px 1px 2px rgba(0,0,0,0.12);}
.r-4gszlv{background-size:cover;}
.r-4v7adb{height:5px;}
.r-5cpxsl{stroke-width:3;}
.r-5is6sd{max-width:460px;}
.r-5kkj8d{border-top-width:1px;}
.r-5ks0hp{right:3.5px;}
.r-5kx3fr{page-break-inside:avoid;}
.r-5oul0u{margin-bottom:8px;}
.r-5soawk{width:10px;}
.r-5vf7qs{width:188px;}
.r-5xr8s6{outline-width:2px;}
.r-60emj1{background-color:rgba(255,204,203,1.00);}
.r-61z16t{margin-right:0px;}
.r-633pao{pointer-events:none!important;}
.r-6d802l{border-left-color:rgba(66,109,213,1.00);}
.r-6dt33c{opacity:1;}
.r-6k4xqk{margin-top:-40px;}
.r-6t5ypu{border-bottom-left-radius:4px;}
.r-6taxm2:-ms-input-placeholder{color:var(--placeholderTextColor);opacity:1;}
.r-6taxm2::-moz-placeholder{color:var(--placeholderTextColor);opacity:1;}
.r-6taxm2::-webkit-input-placeholder{color:var(--placeholderTextColor);opacity:1;}
.r-6taxm2::placeholder{color:var(--placeholderTextColor);opacity:1;}
.r-6uxfom{margin-left:24px;}
.r-6wscbn{max-width:252px;}
.r-73dpzl{border-top-color:rgba(245,247,249,1.00);}
.r-7b7h2f{left:100%;}
.r-7cikom{font-size:inherit;}
.r-7l9xyp{background-color:rgba(255,255,255,0.20);}
.r-7q8q6z{cursor:default;}
.r-7xmw5f{width:-webkit-fit-content;width:-moz-fit-content;width:fit-content;}
.r-81rbui{animation-name:r-1ak6360;}
.r-855088{border-left-color:rgba(0,0,0,0.00);}
.r-88pszg{margin-right:16px;}
.r-8akbws{-webkit-box-orient:vertical;}
.r-8d26hk{margin-bottom:40px;}
.r-8dmbjx{color:rgba(66,90,147,1.00);}
.r-8hc5te{width:6px;}
.r-8jwyv6{-moz-transition:opacity 0.2s ease-in-out;-webkit-transition:opacity 0.2s ease-in-out;transition:opacity 0.2s ease-in-out;}
.r-8upyzv{width:260px;}
.r-8v5hsd{color:rgba(126,231,135,1.00);}
.r-9030i9{box-shadow:0px 4px 10px rgba(0,0,0,0.99);}
.r-9111t9{padding-right:410px;}
.r-92ng3h{width:1px;}
.r-934yyj{padding-left:34px;}
.r-95jzfe{padding-top:16px;}
.r-97e31f{padding-bottom:env(safe-area-inset-bottom);}
.r-97prym{flex-basis:16px;}
.r-99m41f{color:rgba(110,119,129,1.00);}
.r-9aemit{padding-right:0px;}
.r-9ji8r7{transform:translateY(0%);}
.r-9jpwak{min-width:auto;}
.r-a2tzq0{justify-content:space-around;}
.r-a5pmau{margin-right:2px;}
.r-a9hzal{height:660px;}
.r-a9ztke{color:rgba(45,62,103,1.00);}
.r-adacv{min-height:64px;}
.r-adyw6z{font-size:20px;}
.r-agyig6{background-color:var(--sp-color-button-upgrade-bg-hover);}
.r-ah5dr5>*{pointer-events:none;}
.r-ah5dr5{pointer-events:auto!important;}
.r-ak0haq{color:rgba(121,192,255,1.00);}
.r-aqxs90{-moz-transition:opacity 500ms ease-in, z-index 1000ms ease-in;-webkit-transition:opacity 500ms ease-in, z-index 1000ms ease-in;transition:opacity 500ms ease-in, z-index 1000ms ease-in;}
.r-b4cb4{max-height:440px;}
.r-b88u0q{font-weight:700;}
.r-bcqeeo{min-width:0px;}
.r-bgnin{min-width:150px;}
.r-bnwqim{position:relative;}
.r-bsjocg{@media print:[object Object];}
.r-buy8e9{overflow-y:hidden;}
.r-bv2aro{padding-left:env(safe-area-inset-left);}
.r-bxaprw{border-top-left-radius:7px;}
.r-c68hjy{color:rgba(161,161,161,1.00);}
.r-cdhzog{padding-right:80px;}
.r-cpa5s6{scroll-snap-align:start;}
.r-cqilzk{height:400px;}
.r-d822y2{color:rgba(5,80,174,1.00);}
.r-deolkf{box-sizing:border-box;}
.r-dflpy8{height:1.2em;}
.r-dkge59{background-color:rgba(170,184,194,1.00);}
.r-dnmrzs{max-width:100%;}
.r-dse9kg{outline-style:auto;}
.r-dvzd6p{right:-1px;}
.r-dvzwsg{border-left-color:rgba(211,220,228,1.00);}
.r-dwliz8{border-left-width:2px;}
.r-e1k2in{right:16px;}
.r-e9uq0i{animation-duration:1200ms;}
.r-ea455c{border:none;}
.r-eafdt9{transition-duration:0.15s;}
.r-ecifi{max-width:970px;}
.r-ehq7j7{background-size:contain;}
.r-epq5cr{height:2px;}
.r-eqz5dr{flex-direction:column;}
.r-eu3ka{height:40px;}
.r-fdjqy7{text-align:left;}
.r-flmpir{border-bottom-color:rgba(40,49,67,1.00);}
.r-fnigne{border-right-width:0px;}
.r-fpub7{color:rgba(0,0,0,0.00);}
.r-fvlm2j{color:rgba(40,106,127,1.00);}
.r-g3mlsw{animation-name:r-t2lo5v;}
.r-gg6oyi{font-family:gitbook-content-font,-apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif;}
.r-ggadg3{left:-2px;}
.r-givd4m{left:-5px;}
.r-gl891g{min-width:420px;}
.r-gpkeig{border-right-color:var(--sp-color-border-base);}
.r-gtdqiz{position:-webkit-sticky;position:sticky;}
.r-gu0qjt{padding-left:32px;}
.r-gxnn5r{border-left-width:0px;}
.r-gxopl6{left:316px;}
.r-gy4na3{padding-left:0px;}
.r-gys0vz{color:rgba(0,136,71,1.00);}
.r-h2mvr{min-width:8px;}
.r-h2q2x{transform:scaleX(-1);}
.r-h3s6tt{height:48px;}
.r-h7ga17{background-color:rgba(43,46,57,1.00);}
.r-h7gdob{color:currentColor;}
.r-ha54is{icon-color:#a2a9b9;}
.r-hauab{-moz-transition:width 50ms ease-in-out;-webkit-transition:width 50ms ease-in-out;transition:width 50ms ease-in-out;}
.r-hbpseb{line-height:22px;}
.r-hd655f{color:rgba(162,169,185,1.00);}
.r-homxoj{color:inherit;}
.r-hq6u89{left:92%;}
.r-htfu76{margin-left:-8px;}
.r-hxflta{padding-right:env(safe-area-inset-right);}
.r-i023vh{padding-right:16px;}
.r-i7h7g2{-webkit-backdrop-filter:blur(5px);backdrop-filter:blur(5px);}
.r-i8xx8x{color:rgba(207,34,46,1.00);}
.r-ia06lx{background-color:rgba(115,92,255,1.00);}
.r-ibjss6{background-color:rgba(136,153,168,1.00);}
.r-icoktb{opacity:0.5;}
.r-ifefl9{min-height:0px;}
.r-ihd41t{border:1px solid #374151;}
.r-iphfwy{padding-bottom:4px;}
.r-ipm5af{top:0px;}
.r-iqs06e{background-image:radial-gradient(rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 1));}
.r-ir6n1k{border-top-right-radius:6px;}
.r-ixzivm{@media print:[object Object];}
.r-iyfy8q{width:auto;}
.r-j300sb{animation-name:r-1rx4pb;}
.r-jfrpv2{color:rgba(130,80,223,1.00);}
.r-jn0m22{top:54px;}
.r-jn5ml{right:-5px;}
.r-jvuzdy{top:-5px;}
.r-jwli3a{color:rgba(255,255,255,1.00);}
.r-jxjwwx{left:24px;}
.r-k200y{align-self:flex-start;}
.r-k923pl{background-color:rgba(218,212,255,1.00);}
.r-kcufgn{cursor:ew-resize;}
.r-key0ze{height:240px;}
.r-kicko2{border-top-left-radius:4px;}
.r-kls4rr{padding-right:40px;}
.r-knv0ih{margin-top:8px;}
.r-kquydp{right:-4px;}
.r-ky29hr{bottom:2px;}
.r-l0gwng{width:200px;}
.r-l13dpy{z-index:200;}
.r-l27s25{background-color:rgba(204,207,212,1.00);}
.r-l9hqf4{box-shadow:0px 1px 1px rgba(0,0,0,0.69);}
.r-labphf{height:-webkit-fit-content;height:-moz-fit-content;height:fit-content;}
.r-lchren{margin-right:auto;}
.r-ld67tl{left:-72px;}
.r-lk1fr1{icon-color:#8899a8;}
.r-lltvgl{overflow-x:auto;}
.r-lqms97{margin-left:-1px;}
.r-lrsllp{width:24px;}
.r-lrvibr{-moz-user-select:none;-webkit-user-select:none;user-select:none;}
.r-lv5dtd{padding-left:110px;}
.r-lx1l9k{background-image:radial-gradient(rgba(255, 255, 255, 0.1), #ffffff);}
.r-m0vln2{border-left-color:rgba(43,46,57,1.00);}
.r-m2pi6t{padding-left:4px;}
.r-m5arl1{width:2px;}
.r-m5n4jz{background-color:rgba(220,238,244,1.00);}
.r-mabqd8{height:32px;}
.r-majxgm{font-weight:500;}
.r-mbgqwd{margin-right:24px;}
.r-mfh4gg{scroll-snap-type:x mandatory;}
.r-mhe3cw{z-index:10;}
.r-ms8t9i{border-left-width:3px;}
.r-na6qhi{;}
.r-ng8e2f{cursor:-webkit-grab;cursor:-moz-grab;cursor:grab;}
.r-njhh6i{color:rgba(78,170,200,1.00);}
.r-nkouq2{box-shadow:-5px 0px 7px rgba(36,42,49,0.60);}
.r-notknq{border-top-right-radius:4px;}
.r-nvplwv{animation-timing-function:ease-out;}
.r-nvvorq{top:3.5px;}
.r-nwxazl{line-height:40px;}
.r-nzcix3{border-bottom-color:rgba(227,232,237,1.00);}
.r-o8yidv{border-top-left-radius:6px;}
.r-o9xkwf{top:2px;}
.r-obd0qt{align-items:flex-end;}
.r-onxxid{background-color:rgba(27,30,33,0.77);}
.r-op3p1c{width:520px;}
.r-orgf3d{opacity:0;}
.r-ou6ah9{border-top-left-radius:0px;}
.r-oucylx{border-bottom-color:rgba(0,0,0,0.00);}
.r-oz83uh{box-shadow:0px 1px 1px rgba(0,0,0,0.12);}
.r-p1pxzi{margin-bottom:0px;}
.r-pex7a0{color:rgba(130,7,30,1.00);}
.r-pi8zqv{box-shadow:0px 0px 7px rgba(0,0,0,0.04);}
.r-pm9dpa{max-height:100%;}
.r-puj83k{padding-left:24px;}
.r-py1axk{border-bottom-right-radius:7px;}
.r-q4m81j{text-align:center;}
.r-qklmqi{border-bottom-width:1px;}
.r-qn3fzs{padding-bottom:24px;}
.r-r1s0sa{background-color:rgba(255,235,233,1.00);}
.r-r9hte5{-webkit-backdrop-filter:blur(10px);backdrop-filter:blur(10px);}
.r-rb415n{background-color:rgba(66,109,213,1.00);}
.r-redadu{margin-left:var(--sp-spacing-200);}
.r-rs94m5{background-image:url("data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vIj8+CjxzdmcKICAgeG1sbnM6ZGM9Imh0dHA6Ly9wdXJsLm9yZy9kYy9lbGVtZW50cy8xLjEvIgogICB4bWxuczpjYz0iaHR0cDovL2NyZWF0aXZlY29tbW9ucy5vcmcvbnMjIgogICB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiCiAgIHhtbG5zOnN2Zz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiAgIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICAgdmVyc2lvbj0iMS4xIgogICB2aWV3Qm94PSIwIDAgMSAxIgogICBwcmVzZXJ2ZUFzcGVjdFJhdGlvPSJ4TWluWU1pbiBtZWV0Ij4KICA8cGF0aAogICAgIGQ9Ik0gMC4wNDAzODA1OSwwLjYyNjc3NjcgMC4xNDY0NDY2MSwwLjUyMDcxMDY4IDAuNDI5Mjg5MzIsMC44MDM1NTMzOSAwLjMyMzIyMzMsMC45MDk2MTk0MSB6IE0gMC4yMTcxNTcyOSwwLjgwMzU1MzM5IDAuODUzNTUzMzksMC4xNjcxNTcyOSAwLjk1OTYxOTQxLDAuMjczMjIzMyAwLjMyMzIyMzMsMC45MDk2MTk0MSB6IgogICAgIGlkPSJyZWN0Mzc4MCIKICAgICBzdHlsZT0iZmlsbDojZmZmZmZmO2ZpbGwtb3BhY2l0eToxO3N0cm9rZTpub25lIiAvPgo8L3N2Zz4K");}
.r-rwqe4o{width:48px;}
.r-s09aw7{background-image:linear-gradient(to left, #735cff, rgb(109 28 169), rgb(96 104 191), #008847, #FFD139, #b95e04, #d33d3d);}
.r-s0e3za{padding-left:80px;}
.r-s8bhmr{min-width:56px;}
.r-sfbmgh{z-index:9999;}
.r-sga3zk{height:64px;}
.r-sgscqh{width:250px;}
.r-t12b5v{border-top-right-radius:0px;}
.r-t1hnsm{-moz-transition:150ms transform;-webkit-transition:150ms transform;transition:150ms transform;}
.r-t9hbny{background-color:rgba(211,61,61,1.00);}
.r-tceitz{left:16px;}
.r-td7lzs{background-color:var(--sp-color-bg-standout-side);}
.r-tni569{background-color:rgba(11,79,47,1.00);}
.r-tskmnb{padding-top:8px;}
.r-tsynxw{text-transform:uppercase;}
.r-u529wo{transform:translateY(-2px);}
.r-u6sd8q{background-repeat:no-repeat;}
.r-u8s1d{position:absolute;}
.r-u92y06{background-color:rgba(255,165,0,1.00);}
.r-u9bbvc{;}
.r-u9z937{bottom:80px;}
.r-ubezar{font-size:16px;}
.r-ud0q2t{letter-spacing:1px;}
.r-udcg8d{color:rgba(20,23,28,1.00);}
.r-ufs8t{background-clip:text;}
.r-uibjmv{font-family:gitbook-code-font, Menlo, monospace;}
.r-upfvwg{box-shadow:0px 0px 1px rgb(255 255 255 / 30%);}
.r-uweo6c{bottom:136px;}
.r-ux9zog{background-color:rgba(51,61,85,1.00);}
.r-v2u3o6{right:4px;}
.r-vq47rg{color:rgba(211,61,61,1.00);}
.r-vvn4in{background-position:center;}
.r-w0va4e{margin-right:40px;}
.r-w9n8ly{transition-delay:200ms;}
.r-wc24c3{z-index:20;}
.r-wech8c{max-width:1280px;}
.r-wgabs5{border-bottom-width:2px;}
.r-wjlvf2{outline-color:#425a93;}
.r-wk8lta{padding-top:0px;}
.r-ws9h79{left:4px;}
.r-wwqw7s{left:-1px;}
.r-wy61xf{height:72px;}
.r-x1dlf0{max-width:200px;}
.r-x3cy2q{background-size:100% 100%;}
.r-xb2eav{font-size:40px;}
.r-xd6kpl{padding-bottom:8px;}
.r-xifl00{left:-4px;}
.r-xky0vn{background-color:rgba(104,60,17,1.00);}
.r-xnn892{background-color:rgba(218,251,225,1.00);}
.r-xx3c9p{animation-name:r-imtty0;}
.r-xzortm{margin-right:-16px;}
.r-y0itry{background-color:rgba(213,222,246,1.00);}
.r-y3rmyz{width:120px;}
.r-ye2ihm{background-image:none;}
.r-yh6aho{background-image:linear-gradient(270deg, #2b2e39 10%, #22272e, #2b2e39 90%);}
.r-ymefdi{padding-top:var(--sp-spacing-300);}
.r-yrgyi6{white-space:pre;}
.r-ywxogp{color:rgba(115,92,255,1.00);}
.r-z2g584{width:76px;}
.r-z3s97b{border-right-color:rgba(43,46,57,1.00);}
.r-z80fyv{height:20px;}
.r-z9jf92{color:rgba(234,242,247,1.00);}
.r-zchlnj{right:0px;}
.r-zh076v{height:100vh;}
.r-zits6j{right:8%;}
.r-zo7nv5{-webkit-column-gap:16px;column-gap:16px;}
.r-ztyd71{background-color:rgba(0,0,0,0.20);}
@-webkit-keyframes r-1ak6360{0%{background-position-x:0%;}100%{background-position-x:100%;}}
@-webkit-keyframes r-1hunrpy{0%{transform:translateY(100%);}100%{transform:translateY(0%);}}
@-webkit-keyframes r-1rx4pb{0%{transform:translateX(-100%);}100%{transform:translateX(400%);}}
@-webkit-keyframes r-9p3sdl{0%{transform:rotate(0deg);}100%{transform:rotate(360deg);}}
@-webkit-keyframes r-imtty0{0%{opacity:0;}100%{opacity:1;}}
@-webkit-keyframes r-ndfo3d{0%{transform:translateY(0%);}100%{transform:translateY(100%);}}
@-webkit-keyframes r-t2lo5v{0%{opacity:1;}100%{opacity:0;}}
@keyframes r-1ak6360{0%{background-position-x:0%;}100%{background-position-x:100%;}}
@keyframes r-1hunrpy{0%{transform:translateY(100%);}100%{transform:translateY(0%);}}
@keyframes r-1rx4pb{0%{transform:translateX(-100%);}100%{transform:translateX(400%);}}
@keyframes r-9p3sdl{0%{transform:rotate(0deg);}100%{transform:rotate(360deg);}}
@keyframes r-imtty0{0%{opacity:0;}100%{opacity:1;}}
@keyframes r-ndfo3d{0%{transform:translateY(0%);}100%{transform:translateY(100%);}}
@keyframes r-t2lo5v{0%{opacity:1;}100%{opacity:0;}}
[stylesheet-group="10"]{}
[data-rnwrdesktop-166pt5r]{width:max(220px, calc(100vw - max(300px, calc((100vw - 970px) / 2 - 0px)) - 750px - 110px - 300px - 0px));}
[data-rnwrdesktop-18u37iz]{flex-direction:row;}
[data-rnwrdesktop-1hy97zq-1q6rxnj-lv5dtd-9111t9]{padding-left:110px;padding-right:410px;padding-top:80px;}
[data-rnwrdesktop-1ph75f1]{height:80px;}
[data-rnwrdesktop-1uwte3a]{padding-bottom:40px;}
[data-rnwrdesktop-eu3ka]{height:40px;}
[data-rnwrdesktop-fnigne]{border-right-width:0px;}
[data-rnwrdesktop-gg6oyi-1x35g6-37tt59-b88u0q]{font-family:gitbook-content-font,-apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif;font-size:24px;font-weight:700;line-height:32px;}
[data-rnwrdesktop-gg6oyi-xb2eav-1dn12g7-b88u0q]{font-family:gitbook-content-font,-apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif;font-size:40px;font-weight:700;line-height:48px;}
[data-rnwrdesktop-h3s6tt]{height:48px;}
[data-rnwrdesktop-hidden]{display: none;}
[data-rnwrdesktop-iyfy8q-1qhn6m8-11g3r6m-1h0z5md]{justify-content:flex-start;padding-left:16px;padding-right:24px;width:auto;}
[data-rnwrdesktop-visible]{display: flex;}
[stylesheet-group="11"]{}
@media (max-width: 1024px) and (max-width: 9999999.494850524510111312253100114px) { [data-rnwr1024-eqz5dr] {flex-direction:column;} }
@media (max-width: 1024px) and (max-width: 9999999.494850524511810511510598108101px) { [data-rnwr1024-visible] {display: flex;} }
@media (max-width: 1024px) and (max-width: 9999999.49485052454910510212011610048px) { [data-rnwr1024-1ifxtd0] {margin-bottom:16px;} }
@media (max-width: 1280px) and (max-width: 9999999.4950564845104105100100101110px) { [data-rnwr1280-hidden] {display: none;} }
@media (max-width: 1280px) and (max-width: 9999999.49505648454955555510299105px) { [data-rnwr1280-1777fci] {justify-content:center;} }
@media (max-width: 1430px) and (max-width: 9999999.495251484511810511510598108101px) { [data-rnwr1430-visible] {display: flex;} }
@media (max-width: 1490px) and (max-width: 9999999.49525748454955555510299105px) { [data-rnwr1490-1777fci] {justify-content:center;} }
[stylesheet-group="12"]{}
@media (max-width: 700px) and (max-width: 9999999.5548484510111312253100114px) { [data-rnwr700-eqz5dr] {flex-direction:column;} }
@media (max-width: 700px) and (max-width: 9999999.55484845103103541111211054549117105531011015645110119120971221084598565611748113px) { [data-rnwr700-gg6oyi-1ui5ee8-nwxazl-b88u0q] {font-family:gitbook-content-font,-apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif;font-size:32px;font-weight:700;line-height:40px;} }
@media (max-width: 700px) and (max-width: 9999999.5548484510310354111121105459710012111954122454951531199897554598565611748113px) { [data-rnwr700-gg6oyi-adyw6z-135wba7-b88u0q] {font-family:gitbook-content-font,-apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif;font-size:20px;font-weight:700;line-height:24px;} }
@media (max-width: 700px) and (max-width: 9999999.55484845104105100100101110px) { [data-rnwr700-hidden] {display: none;} }
@media (max-width: 700px) and (max-width: 9999999.5548484510512110212156113451011175110797px) { [data-rnwr700-iyfy8q-eu3ka] {height:40px;width:auto;} }
@media (max-width: 700px) and (max-width: 9999999.554848451051211021215611345103121521109751451054850511181044549119981045397504549104481225310910045px) { [data-rnwr700-iyfy8q-gy4na3-i023vh-1wbh5a2-1h0z5md-] {flex-shrink:1;justify-content:flex-start;padding-left:0px;padding-right:16px;width:auto;} }
@media (max-width: 700px) and (max-width: 9999999.554848451151039751122107px) { [data-rnwr700-sga3zk] {height:64px;} }
@media (max-width: 700px) and (max-width: 9999999.5548484511810511510598108101px) { [data-rnwr700-visible] {display: flex;} }
@media (max-width: 700px) and (max-width: 9999999.554848454910355102105109108px) { [data-rnwr700-1g7fiml] {height:30px;} }
@media (max-width: 700px) and (max-width: 9999999.55484845491195410154114106454955555510299105px) { [data-rnwr700-1w6e6rj-1777fci] {flex-wrap:wrap;justify-content:center;} }
@media (max-width: 700px) and (max-width: 9999999.5548484549511085011652103px) { [data-rnwr700-13l2t4g] {border-right-width:1px;} }
@media (max-width: 700px) and (max-width: 9999999.5548484557531061221021014549113104110541095645105485051118104px) { [data-rnwr700-95jzfe-1qhn6m8-i023vh] {padding-left:16px;padding-right:16px;padding-top:16px;} }
@media (max-width: 970px) and (max-width: 9999999.5755484510111312253100114px) { [data-rnwr970-eqz5dr] {flex-direction:column;} }
[stylesheet-group="13"]{}
@media (max-width: 700px) and (max-width: 9999999.554848454955555510299105px) { [data-rnwr700-1777fci] {justify-content:center;} }
[stylesheet-group="20"]{}
[data-rnwi-1pa6394-]{color:var(--sp-color-text-muted);}
[data-rnwi-handle="link"] [data-rnwilink--146vlhe-]{color:rgba(66,109,213,1.00);}
body:not(.dragging) [data-rnwi--146vlhe-hover-focus]:hover, body:not(.dragging) [data-rnwi--146vlhe-hover-focus]:focus{color:rgba(66,109,213,1.00);}
body:not(.dragging) [data-rnwi--1q9ho9q-hover-focus]:hover, body:not(.dragging) [data-rnwi--1q9ho9q-hover-focus]:focus{color:rgba(48,127,152,1.00);}
body:not(.dragging) [data-rnwi--81s47e--focus]:focus{border-bottom-color:rgba(66,109,213,1.00);border-left-color:rgba(66,109,213,1.00);border-right-color:rgba(66,109,213,1.00);border-top-color:rgba(66,109,213,1.00);}
body:not(.dragging) [data-rnwi--a9ztke-hover-focus]:hover, body:not(.dragging) [data-rnwi--a9ztke-hover-focus]:focus{color:rgba(45,62,103,1.00);}
body:not(.dragging) [data-rnwi-190qawg-hover-focus]:hover, body:not(.dragging) [data-rnwi-190qawg-hover-focus]:focus{border-bottom-color:rgba(227,232,237,1.00);border-left-color:rgba(227,232,237,1.00);border-right-color:rgba(227,232,237,1.00);border-top-color:rgba(227,232,237,1.00);}
body:not(.dragging) [data-rnwi-1b00too-hover]:hover{background-color:rgba(236,239,241,1.00);}
body:not(.dragging) [data-rnwi-1iadl42-hover-focus]:hover, body:not(.dragging) [data-rnwi-1iadl42-hover-focus]:focus{background-color:var(--sp-color-bg-standout-base);}
body:not(.dragging) [data-rnwi-5xr8s6-dse9kg-2fw26j-3kxdz0-focus-visible]:focus-visible{outline-color:#286A7F;outline-offset:0px;outline-style:auto;outline-width:2px;}
body:not(.dragging) [data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible]:focus-visible{outline-color:#425a93;outline-offset:0px;outline-style:auto;outline-width:2px;}
body:not(.dragging) [data-rnwi-handle="BaseCard"]:hover [data-rnwibasecard--146vlhe-hover-focus], body:not(.dragging) [data-rnwi-handle="BaseCard"]:focus [data-rnwibasecard--146vlhe-hover-focus]{color:rgba(66,109,213,1.00);}
body:not(.dragging) [data-rnwi-handle="BaseCard"]:hover [data-rnwibasecard--146vlhe-hover]{color:rgba(66,109,213,1.00);}
body:not(.dragging) [data-rnwi-handle="button"]:hover [data-rnwibutton--146vlhe-hover-focus], body:not(.dragging) [data-rnwi-handle="button"]:focus [data-rnwibutton--146vlhe-hover-focus]{color:rgba(66,109,213,1.00);}
body:not(.dragging) [data-rnwi-handle="button"]:hover [data-rnwibutton-37p410-hover-focus], body:not(.dragging) [data-rnwi-handle="button"]:focus [data-rnwibutton-37p410-hover-focus]{color:var(--sp-color-text-base);}
body:not(.dragging) [data-rnwi-handle="link"]:hover [data-rnwilink--a9ztke-1ddef8g-hover]{-webkit-text-decoration-line:underline;color:rgba(45,62,103,1.00);text-decoration-line:underline;}
body:not(.dragging) [data-rnwi-handle="nearest"]:hover [data-rnwinearest--146vlhe-hover]{color:rgba(66,109,213,1.00);}
body:not(.dragging) [data-rnwi-handle="nearest"]:hover [data-rnwinearest--1q9ho9q-hover-focus], body:not(.dragging) [data-rnwi-handle="nearest"]:focus [data-rnwinearest--1q9ho9q-hover-focus]{color:rgba(48,127,152,1.00);}
body:not(.dragging) [data-rnwi-handle="nearest"]:hover [data-rnwinearest-37p410-hover-focus], body:not(.dragging) [data-rnwi-handle="nearest"]:focus [data-rnwinearest-37p410-hover-focus]{color:var(--sp-color-text-base);}
body:not(.dragging) [data-rnwi-u529wo-aq1qub-c1zw6o-1khlhp8-1cut0bx-na6qhi--hover]:hover{box-shadow:0px 12px 13px rgba(0,0,0,0.02);transform:translateY(-2px);}</style>
                <style>
                    html,
                    body {
                        -webkit-font-smoothing: antialiased;
                        text-rendering: optimizelegibility;
                        width: 100%;
                        min-height: 100vh;
                        user-select: none;
                        outline: none;
                        position: relative;
                    }
                    /* Avoid Chrome to see Safari hack */
                    @supports (-webkit-touch-callout: none) {
                        html,
                        body,
                        .gitbook-root {
                            /* The hack for Safari */
                            min-height: -webkit-fill-available;
                        }
                    }
                    .gitbook-root {
                        display: flex;
                        min-height: 100vh;
                    }
                </style>
            
        <script type="text/javascript" defer src="https://cdn.iframe.ly/embed.js" async></script>
        <script
            type="text/javascript"
            defer
            src="https://cdn.polyfill.io/v2/polyfill.js?features=Intl.~locale.en"
            crossorigin="anonymous"
        ></script>

    </head>
    <body class="theme-color-light theme-radius-rounded">
        <script>
                    (function () {
                        var theme = null;

                        try {
                          var rawValue = localStorage.getItem("@gitbook/themeMode");
                          if (rawValue !== null) {
                            theme = JSON.parse(rawValue);
                          }
                        } catch (err) {
                          // Make an attempt in case it's not a JSON value
                          if (theme !== "light" && theme !== "dark") {
                            theme = null;
                          }
                        }
                        if (undefined && theme && theme !== "light") {
                          document.body.classList.add("theme-overlay");
                          document.body.classList.remove("theme-color-light");
                          document.body.classList.add("theme-color-" + theme);
                        }
                      })();
                </script>
                   <div class="gitbook-root"><div class="css-175oi2r r-13awgt0 r-12vffkv"><div class="css-175oi2r r-13awgt0 r-12vffkv"><!--$--><header data-rnwrdesktop-1ph75f1="true" data-rnwr700-sga3zk="true" class="r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-nzcix3 r-qklmqi r-gtdqiz r-ipm5af r-184en5c r-18u37iz r-1awozwy" style="background-color:rgba(255,255,255,1.00)"><div class="view_manYY publicContainer_11UZS horizontal200_M-XNg alignItemsCenter_Si4Gd withStickyHeader_HQiM-"><div aria-label="Show Table of Content" role="button" data-rnwrdesktop-hidden="true" data-rnwr700-visible="true" data-rnwi-1iadl42-hover-focus="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="button" tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-rs99b7 r-18u37iz r-18kxxzh r-1cmwbt1 r-1777fci r-1ny4l3l r-1r8g8re r-1pa6394 r-1kb76zh r-18c69zk r-mk0yit r-1acpoxo" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" preserveAspectRatio="xMidYMid meet" data-rnwibutton-37p410-hover-focus="true" data-rnwi-handle="nearest" class="r-h7gdob" style="vertical-align:middle;width:18px;height:18px"><path d="M3 12h18M3 6h18M3 18h18"></path></svg></div><a href="/main/" aria-label="kakao business 비즈니스 가이드" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" data-rnwrdesktop-iyfy8q-1qhn6m8-11g3r6m-1h0z5md="true" data-rnwr700-iyfy8q-gy4na3-i023vh-1wbh5a2-1h0z5md-="true" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s" data-testid="public.headerHomeLink"><div data-rnwrdesktop-eu3ka="true" data-rnwr700-1g7fiml="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz r-1awozwy r-6wscbn"><div data-rnwrdesktop-visible="true" data-rnwr700-hidden="true" class="css-175oi2r"><img alt="" src="https://www.gitbook.com/cdn-cgi/image/width=256,dpr=2,height=40,fit=contain,format=auto/https%3A%2F%2F3168043928-files.gitbook.io%2F~%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MVZVmVOd-5LtENUPqdq%252Flogo%252FQyhOPTRHle6GksEVFzf3%252F%25E1%2584%2587%25E1%2585%25B5%25E1%2584%258C%25E1%2585%25B3%25E1%2584%2582%25E1%2585%25B5%25E1%2584%2589%25E1%2585%25B3%25E1%2584%2580%25E1%2585%25A1%25E1%2584%258B%25E1%2585%25B5%25E1%2584%2583%25E1%2585%25B3_%25E1%2584%2592%25E1%2585%25A9%25E1%2586%25B7%25E1%2584%2587%25E1%2585%25A5%25E1%2584%2590%25E1%2585%25B3%25E1%2586%25AB.png%3Falt%3Dmedia%26token%3D96877152-3a26-4f42-afa0-f8664a165681" width="100%" height="auto" decoding="async" style="max-height:40px;max-width:252px;width:auto;height:auto"/></div><div data-rnwrdesktop-hidden="true" data-rnwr700-visible="true" class="css-175oi2r"><img alt="" src="https://www.gitbook.com/cdn-cgi/image/width=256,dpr=2,height=30,fit=contain,format=auto/https%3A%2F%2F3168043928-files.gitbook.io%2F~%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F-MVZVmVOd-5LtENUPqdq%252Flogo%252FQyhOPTRHle6GksEVFzf3%252F%25E1%2584%2587%25E1%2585%25B5%25E1%2584%258C%25E1%2585%25B3%25E1%2584%2582%25E1%2585%25B5%25E1%2584%2589%25E1%2585%25B3%25E1%2584%2580%25E1%2585%25A1%25E1%2584%258B%25E1%2585%25B5%25E1%2584%2583%25E1%2585%25B3_%25E1%2584%2592%25E1%2585%25A9%25E1%2586%25B7%25E1%2584%2587%25E1%2585%25A5%25E1%2584%2590%25E1%2585%25B3%25E1%2586%25AB.png%3Falt%3Dmedia%26token%3D96877152-3a26-4f42-afa0-f8664a165681" width="100%" height="auto" decoding="async" style="max-height:30px;max-width:252px;width:auto;height:auto"/></div></div></a><div data-rnwr700-hidden="true" class="css-175oi2r r-18u37iz r-17s6mgv r-1awozwy r-1ro0kt6 r-16y2uox r-1wbh5a2 r-1qhn6m8"><a href="https://business.kakao.com/" dir="auto" aria-label="카카오비즈니스" data-rnwi--a9ztke-hover-focus="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-1rynq56 r-8akbws r-krxsd3 r-dnmrzs r-1udh08x r-1udbk01 r-gg6oyi r-ubezar r-135wba7 r-1kfrs79 r-ymttw5 r-1loqt21" style="-webkit-line-clamp:2;color:rgba(66,109,213,1.00)">카카오비즈니스</a><a href="https://accounts.kakao.com/login/kakaobusiness?continue=https%3A%2F%2Fbusiness.kakao.com%2Fdashboard%2F" dir="auto" aria-label="비즈니스관리자" data-rnwi--a9ztke-hover-focus="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-1rynq56 r-8akbws r-krxsd3 r-dnmrzs r-1udh08x r-1udbk01 r-gg6oyi r-ubezar r-135wba7 r-1kfrs79 r-ymttw5 r-1loqt21" style="-webkit-line-clamp:2;color:rgba(66,109,213,1.00)">비즈니스관리자</a></div><div data-rnwrdesktop-visible="true" data-rnwr700-hidden="true" class="css-175oi2r r-1jj8364 r-puj83k r-1pyaxff r-11xdecz r-1ro0kt6 r-16y2uox r-1wbh5a2"><div aria-label="Search" data-rnwi-190qawg-hover-focus="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-42olwf r-kdyh1x r-rs99b7 r-1r8g8re r-13qz1uu r-18u37iz r-1wtj0ep r-1awozwy r-1qhn6m8 r-1pyaxff" style="background-color:rgba(59,69,78,0.10);transition-duration:0.15s"><div class="css-175oi2r r-18u37iz r-1awozwy"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" preserveAspectRatio="xMidYMid meet" class="r-1kb76zh" style="vertical-align:middle;width:16px;height:16px;color:rgba(59,69,78,1.00)"><path fill="currentColor" fill-rule="evenodd" d="M10.5 4a6.5 6.5 0 1 0 0 13 6.5 6.5 0 0 0 0-13ZM2 10.5a8.5 8.5 0 1 1 17 0 8.5 8.5 0 0 1-17 0Z" clip-rule="evenodd"></path><path fill="currentColor" fill-rule="evenodd" d="M15.093 15.093a1 1 0 0 1 1.414 0l5.2 5.2a1 1 0 0 1-1.414 1.414l-5.2-5.2a1 1 0 0 1 0-1.414Z" clip-rule="evenodd"></path></svg><div dir="auto" data-rnwinearest-37p410-hover-focus="true" data-rnwi-handle="nearest" class="css-1rynq56 r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb" style="color:rgba(59,69,78,1.00)">Search</div></div><div class="css-175oi2r"><div class="view_manYY gap_PR1GX"><span class="base_qcuoW shortcut_8i--D uiSmall_BjkNA">⌃</span><span class="base_qcuoW shortcut_8i--D uiSmall_BjkNA">K</span></div></div></div></div><div data-rnwrdesktop-hidden="true" data-rnwr700-visible="true" class="css-175oi2r r-1jj8364 r-puj83k r-1pyaxff"><div aria-label="Search" role="button" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="button" tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-rs99b7 r-18u37iz r-18kxxzh r-1cmwbt1 r-1777fci r-1ny4l3l r-z2wwpe r-mabqd8 r-1bnj018 r-mk0yit r-1yvhtrz" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" preserveAspectRatio="xMidYMid meet" data-rnwibutton--146vlhe-hover-focus="true" data-rnwi-handle="nearest" style="vertical-align:middle;width:16px;height:16px;color:rgba(59,69,78,1.00)"><path fill="currentColor" fill-rule="evenodd" d="M10.5 4a6.5 6.5 0 1 0 0 13 6.5 6.5 0 0 0 0-13ZM2 10.5a8.5 8.5 0 1 1 17 0 8.5 8.5 0 0 1-17 0Z" clip-rule="evenodd"></path><path fill="currentColor" fill-rule="evenodd" d="M15.093 15.093a1 1 0 0 1 1.414 0l5.2 5.2a1 1 0 0 1-1.414 1.414l-5.2-5.2a1 1 0 0 1 0-1.414Z" clip-rule="evenodd"></path></svg></div></div></div></header><div data-rnwrdesktop-hidden="true" data-rnwr700-visible="true" class="css-175oi2r"><div class="css-175oi2r r-1pl7oy7 r-14lw9ot r-1d9grui r-qklmqi r-1777fci r-nsbfu8"><div class="css-175oi2r r-lchren"><div role="button" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="button" tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-rs99b7 r-18u37iz r-18kxxzh r-1cmwbt1 r-1777fci r-1ny4l3l r-z2wwpe r-1r8g8re r-1bnj018 r-mk0yit" style="transition-duration:0.15s"><div class="css-175oi2r r-1wbh5a2 r-16y2uox"><div dir="auto" data-rnwibutton--146vlhe-hover-focus="true" data-rnwi-handle="nearest" class="css-1rynq56 r-dnmrzs r-1udh08x r-1udbk01 r-3s2u2q r-1iln25a r-gg6oyi r-ubezar r-1o2nx2a r-135wba7 r-h7gdob">Links</div></div><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" data-rnwibutton--146vlhe-hover-focus="true" data-rnwi-handle="nearest" class="r-h7gdob" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></div></div></div><div data-rnwrdesktop-18u37iz="true" data-rnwr700-eqz5dr="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-14lw9ot"><div class="view_manYY publicContainer_11UZS"><div data-rnwrdesktop-visible="true" data-rnwr1430-visible="true" data-rnwr700-hidden="true" class="css-175oi2r r-k200y r-14lw9ot r-18ayb63 r-13l2t4g r-12dqhl9 r-1rnoaur r-gtdqiz r-1fo40xd r-18u37iz r-17s6mgv" data-testid="page.desktopTableOfContents"><nav aria-label="Table of contents" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ipicw7 r-eqz5dr"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-puj83k"><div class="css-175oi2r r-150rngu r-eqz5dr r-11yh6sk r-1rnoaur r-1sncvnh r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r r-1yzf0co r-1adewhw"><!--$--><div class="css-175oi2r"><a href="/main/" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="background-color:rgba(133,160,224,0.10);transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-hbpseb r-146vlhe r-b88u0q">카카오비즈니스 가이드</div></a></div><!--/$--><!--$--><div class="css-175oi2r"><a href="https://business.kakao.com/" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오비즈니스 바로가기</div><div class="css-175oi2r r-1jkjb r-12zb1j4"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1pa6394" style="vertical-align:middle;width:18px;height:18px"><g fill="currentColor" clip-path="url(#ExternalLink_svg__a)"><path d="M7 .9a.6.6 0 1 1 0 1.2H3.5a1.4 1.4 0 0 0-1.4 1.4v9a1.4 1.4 0 0 0 1.4 1.4h9a1.4 1.4 0 0 0 1.4-1.4V9a.6.6 0 1 1 1.2 0v3.5a2.6 2.6 0 0 1-2.6 2.6h-9a2.6 2.6 0 0 1-2.6-2.6v-9A2.6 2.6 0 0 1 3.5.9H7Z"></path><path d="M9.9 1.5a.6.6 0 0 0 .6.6h2.552L9.076 6.076a.6.6 0 0 0 .848.848L13.9 2.95V5.5a.6.6 0 1 0 1.2 0v-4a.6.6 0 0 0-.6-.6h-4a.6.6 0 0 0-.6.6Z"></path></g><defs><clipPath id="ExternalLink_svg__a"><path fill="#fff" d="M0 0h16v16H0z"></path></clipPath></defs></svg></div></a></div><!--/$--><!--$--><div class="css-175oi2r"><a href="https://bizseminar.kakao.com/" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">비즈니스 세미나 바로가기</div><div class="css-175oi2r r-1jkjb r-12zb1j4"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1pa6394" style="vertical-align:middle;width:18px;height:18px"><g fill="currentColor" clip-path="url(#ExternalLink_svg__a)"><path d="M7 .9a.6.6 0 1 1 0 1.2H3.5a1.4 1.4 0 0 0-1.4 1.4v9a1.4 1.4 0 0 0 1.4 1.4h9a1.4 1.4 0 0 0 1.4-1.4V9a.6.6 0 1 1 1.2 0v3.5a2.6 2.6 0 0 1-2.6 2.6h-9a2.6 2.6 0 0 1-2.6-2.6v-9A2.6 2.6 0 0 1 3.5.9H7Z"></path><path d="M9.9 1.5a.6.6 0 0 0 .6.6h2.552L9.076 6.076a.6.6 0 0 0 .848.848L13.9 2.95V5.5a.6.6 0 1 0 1.2 0v-4a.6.6 0 0 0-.6-.6h-4a.6.6 0 0 0-.6.6Z"></path></g><defs><clipPath id="ExternalLink_svg__a"><path fill="#fff" d="M0 0h16v16H0z"></path></clipPath></defs></svg></div></a></div><!--/$--><!--$--><div class="css-175oi2r r-1r5su4o"><div data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" class="css-175oi2r r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1enofrn r-1kfrs79 r-19r33im r-14yzgew r-tsynxw r-1pa6394">비즈니스 시작하기</div></div><div class="css-175oi2r r-bnwqim r-11wrixw"><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/undefined/untitled" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오비즈니스 통합 가입</div></a></div><!--/$--></div></div></div><!--/$--><!--$--><div class="css-175oi2r r-1r5su4o"><div data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" class="css-175oi2r r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1enofrn r-1kfrs79 r-19r33im r-14yzgew r-tsynxw r-1pa6394">채널</div></div><div class="css-175oi2r r-bnwqim r-11wrixw"><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/channel/info" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">소개</div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/channel/start" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">채널 만들기</div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/channel/run" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">운영하기</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/channel/faq" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">FAQ</div></a></div><!--/$--></div></div></div><!--/$--><!--$--><div class="css-175oi2r r-1r5su4o"><div data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" class="css-175oi2r r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1enofrn r-1kfrs79 r-19r33im r-14yzgew r-tsynxw r-1pa6394">광고</div></div><div class="css-175oi2r r-bnwqim r-11wrixw"><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/ad/info" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">소개</div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/ad/moment" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오모먼트</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/ad/searchad" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">검색 광고</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/ad/bizmessage" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">알림톡/친구톡/상담톡</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/ad/shopping-ad" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오쇼핑 광고센터</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/ad/other-ad" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">기타 광고 서비스</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/ad/adspolicy" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">광고피해신고</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div></div></div><!--/$--><!--$--><div class="css-175oi2r r-1r5su4o"><div data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" class="css-175oi2r r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1enofrn r-1kfrs79 r-19r33im r-14yzgew r-tsynxw r-1pa6394">서비스/도구</div></div><div class="css-175oi2r r-bnwqim r-11wrixw"><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/kakaosync" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오싱크</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/checkout" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">톡체크아웃</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/booking" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오톡 예약하기</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/order" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오톡 주문하기</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/mystore" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오맵 매장관리</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/bizform" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">비즈니스폼</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/bizplugin" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">비즈플러그인</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/pixel-sdk" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">픽셀 &amp; SDK</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/image_editor" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">이미지 에디터</div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/chatbot" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">챗봇 관리자센터</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/knowledge" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">지식</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/for-biz" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">선물하기 for Biz</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/talkstore" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오톡 스토어</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/tool/bizwallet" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">비즈월렛</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div></div></div><!--/$--><!--$--><div class="css-175oi2r r-1r5su4o"><div data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" class="css-175oi2r r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1enofrn r-1kfrs79 r-19r33im r-14yzgew r-tsynxw r-1pa6394">비즈니스계정</div></div><div class="css-175oi2r r-bnwqim r-11wrixw"><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/bizaccount/info" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">비즈니스계정 소개</div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/bizaccount/start" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">비즈니스계정 만들기</div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/bizaccount/run" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">운영하기</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div></div></div><!--/$--><!--$--><div class="css-175oi2r r-1r5su4o"><div data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" class="css-175oi2r r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1enofrn r-1kfrs79 r-19r33im r-14yzgew r-tsynxw r-1pa6394">파트너 지원 프로그램</div></div><div class="css-175oi2r r-bnwqim r-11wrixw"><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/partner/crossmedia" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">크로스미디어</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/partner/list" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">공식 대행사 리스트</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/partner/smb" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">소상공인 지원 혜택</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="/main/partner/license" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오비즈니스 자격증</div><div tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1bnj018" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" fill-rule="evenodd" d="M5.576 3.576a.6.6 0 0 1 .848 0l4 4a.6.6 0 0 1 0 .848l-4 4a.6.6 0 0 1-.848-.848L9.15 8 5.576 4.424a.6.6 0 0 1 0-.848Z" clip-rule="evenodd"></path></svg></div></a></div><!--/$--></div></div></div><!--/$--><!--$--><div class="css-175oi2r r-1r5su4o"><div data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" class="css-175oi2r r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1enofrn r-1kfrs79 r-19r33im r-14yzgew r-tsynxw r-1pa6394">개발자 지원 가이드</div></div><div class="css-175oi2r r-bnwqim r-11wrixw"><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="https://developers.kakao.com/" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh r-15zivkp" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">카카오디벨로퍼스</div><div class="css-175oi2r r-1jkjb r-12zb1j4"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1pa6394" style="vertical-align:middle;width:18px;height:18px"><g fill="currentColor" clip-path="url(#ExternalLink_svg__a)"><path d="M7 .9a.6.6 0 1 1 0 1.2H3.5a1.4 1.4 0 0 0-1.4 1.4v9a1.4 1.4 0 0 0 1.4 1.4h9a1.4 1.4 0 0 0 1.4-1.4V9a.6.6 0 1 1 1.2 0v3.5a2.6 2.6 0 0 1-2.6 2.6h-9a2.6 2.6 0 0 1-2.6-2.6v-9A2.6 2.6 0 0 1 3.5.9H7Z"></path><path d="M9.9 1.5a.6.6 0 0 0 .6.6h2.552L9.076 6.076a.6.6 0 0 0 .848.848L13.9 2.95V5.5a.6.6 0 1 0 1.2 0v-4a.6.6 0 0 0-.6-.6h-4a.6.6 0 0 0-.6.6Z"></path></g><defs><clipPath id="ExternalLink_svg__a"><path fill="#fff" d="M0 0h16v16H0z"></path></clipPath></defs></svg></div></a></div><!--/$--></div><div class="css-175oi2r"><!--$--><div class="css-175oi2r"><a href="https://i.kakao.com/" data-rnwrdesktop-fnigne="true" data-rnwr700-13l2t4g="true" data-rnwi-1b00too-hover="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-z2wwpe r-rs99b7 r-18u37iz r-1ceczpf r-1pn2ns4 r-1kb76zh" style="transition-duration:0.15s"><div dir="auto" class="css-1rynq56 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-oyd9sg r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1bnj018">챗봇 관리자센터</div><div class="css-175oi2r r-1jkjb r-12zb1j4"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" class="r-1pa6394" style="vertical-align:middle;width:18px;height:18px"><g fill="currentColor" clip-path="url(#ExternalLink_svg__a)"><path d="M7 .9a.6.6 0 1 1 0 1.2H3.5a1.4 1.4 0 0 0-1.4 1.4v9a1.4 1.4 0 0 0 1.4 1.4h9a1.4 1.4 0 0 0 1.4-1.4V9a.6.6 0 1 1 1.2 0v3.5a2.6 2.6 0 0 1-2.6 2.6h-9a2.6 2.6 0 0 1-2.6-2.6v-9A2.6 2.6 0 0 1 3.5.9H7Z"></path><path d="M9.9 1.5a.6.6 0 0 0 .6.6h2.552L9.076 6.076a.6.6 0 0 0 .848.848L13.9 2.95V5.5a.6.6 0 1 0 1.2 0v-4a.6.6 0 0 0-.6-.6h-4a.6.6 0 0 0-.6.6Z"></path></g><defs><clipPath id="ExternalLink_svg__a"><path fill="#fff" d="M0 0h16v16H0z"></path></clipPath></defs></svg></div></a></div><!--/$--></div></div></div><!--/$--></div></div></div><div class="css-175oi2r r-1p0dtai r-u8s1d r-13qz1uu r-184en5c"><div class="css-175oi2r r-10ptun7" style="background-image:linear-gradient(3.141592653589793rad,#ffffff00,#ffffff)"></div><div class="css-175oi2r r-ymttw5 r-1l7z4oj r-14lw9ot"><a href="https://www.gitbook.com/?utm_source=content&amp;utm_medium=trademark&amp;utm_campaign=-MVZVmVOd-5LtENUPqdq" data-rnwi--1q9ho9q-hover-focus="true" data-rnwi-5xr8s6-dse9kg-2fw26j-3kxdz0-focus-visible="true" data-rnwi-handle="nearest" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-18u37iz r-1awozwy r-1b00too r-1xfd6ze r-1yzf0co r-ymttw5" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 32 30" preserveAspectRatio="xMidYMid meet" data-rnwi--1q9ho9q-hover-focus="true" data-rnwi-5xr8s6-dse9kg-2fw26j-3kxdz0-focus-visible="true" data-rnwi-handle="nearest" class="r-1pa6394" style="vertical-align:middle;width:28px;height:28px"><path fill="currentColor" d="M13.478 15.34c1.564.904 2.347 1.355 3.206 1.356.859 0 1.642-.45 3.208-1.35l9.983-5.738a1.452 1.452 0 0 0 0-2.519l-9.987-5.74C18.324.449 17.542-.001 16.683 0c-.858 0-1.64.45-3.204 1.351L4.894 6.295l-.125.072A9.638 9.638 0 0 0 0 14.617v.289a9.639 9.639 0 0 0 4.885 8.316l5.377 3.105c3.134 1.809 4.7 2.714 6.422 2.714 1.72 0 3.288-.903 6.422-2.71l5.677-3.273c1.57-.904 2.355-1.357 2.786-2.103.431-.746.431-1.652.431-3.463v-3.5a1.385 1.385 0 0 0-2.076-1.202l-11.64 6.692c-.782.449-1.172.673-1.6.673-.43 0-.82-.224-1.601-.672l-7.88-4.523c-.394-.226-.591-.34-.75-.36a.803.803 0 0 0-.846.493c-.06.148-.06.376-.057.83.002.336.003.503.034.657.07.345.252.658.517.89.118.103.263.187.553.354l8.424 4.862c.784.452 1.175.678 1.605.678.43 0 .822-.226 1.606-.677l10.325-5.952c.267-.154.401-.231.502-.173.1.058.1.212.1.521v1.588c0 .453 0 .68-.108.866-.108.186-.304.3-.696.525l-8.516 4.91c-1.568.903-2.352 1.355-3.213 1.355-.86 0-1.643-.453-3.21-1.359l-7.968-4.602-.05-.029a5.472 5.472 0 0 1-2.71-4.697v-1.515c0-1.068.568-2.055 1.492-2.59a2.638 2.638 0 0 1 2.641-.003l6.6 3.809Z"></path></svg><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-1qhn6m8"><div dir="auto" data-rnwinearest--1q9ho9q-hover-focus="true" data-rnwi-handle="nearest" class="css-1rynq56 r-gg6oyi r-1b43r93 r-16dba41 r-hbpseb r-1pa6394">Powered By <span class="css-1qaijid r-b88u0q">GitBook</span></div></div></a></div></div></nav></div><div class="css-175oi2r r-13awgt0" style="background-color:rgba(255,255,255,1.00)"><!--$--><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz"><div class="view_manYY pageWrapper_BkhZI vertical0_jPhI0 horizontalAuto_xck7M flex1_qv0N2 column_Pzect"><main class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ro0kt6 r-16y2uox r-1wbh5a2 r-eqz5dr"><div class="view_manYY blockWrapper_8BIg7 vertical0_jPhI0 horizontalAuto_xck7M"><div data-rnwr1280-1777fci="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="view_manYY relative_kNGzo column_Pzect top700_934HS bottom600_DtxRs"><div class="view_manYY pageControls_65PGe revealOnHover_QTUA- top200_Mzy9L row_apb2Z columnGap100_WpE2b"><div role="button" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="button" tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-rs99b7 r-18u37iz r-18kxxzh r-1cmwbt1 r-1777fci r-1ny4l3l r-z2wwpe r-z80fyv r-1pn2ns4 r-1bnj018 r-gy4na3" style="transition-duration:0.15s"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" data-rnwibutton--146vlhe-hover-focus="true" data-rnwi-handle="nearest" class="r-h7gdob" style="vertical-align:middle;width:16px;height:16px"><path fill="currentColor" fill-rule="evenodd" d="M15.6 4A2.6 2.6 0 0 0 13 1.4H3A2.6 2.6 0 0 0 .4 4v6A2.6 2.6 0 0 0 3 12.6h.092v2.117a.6.6 0 0 0 .987.46l2.672-2.248a1.4 1.4 0 0 1 .901-.329H13a2.6 2.6 0 0 0 2.6-2.6V4ZM13 2.6A1.4 1.4 0 0 1 14.4 4v6a1.4 1.4 0 0 1-1.4 1.4H7.652a2.6 2.6 0 0 0-1.673.61L4.292 13.43V12a.6.6 0 0 0-.6-.6H3A1.4 1.4 0 0 1 1.6 10V4A1.4 1.4 0 0 1 3 2.6h10Z" clip-rule="evenodd"></path></svg><div class="css-175oi2r r-1wbh5a2"><div dir="auto" data-rnwibutton--146vlhe-hover-focus="true" data-rnwi-handle="nearest" class="css-1rynq56 r-dnmrzs r-1udh08x r-1udbk01 r-3s2u2q r-1iln25a r-gg6oyi r-1enofrn r-16dba41 r-14yzgew r-h7gdob">Comment on page</div></div></div></div><div class="view_manYY row_apb2Z justifySpaceBetween_WG1-N alignItemsCenter_Si4Gd"><div class="css-175oi2r r-18u37iz r-1ro0kt6 r-16y2uox r-1wbh5a2"><div data-rnwrdesktop-h3s6tt="true" data-rnwr700-iyfy8q-eu3ka="true" class="css-175oi2r r-18u37iz r-17s6mgv r-1awozwy"></div><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><h1 data-rnwrdesktop-gg6oyi-xb2eav-1dn12g7-b88u0q="true" data-rnwr700-gg6oyi-1ui5ee8-nwxazl-b88u0q="true" class="r-1xnzce8 r-crgep1 r-37p410" data-testid="page.title">카카오비즈니스 가이드</h1></div></div><div aria-label="Page actions" role="button" data-rnwi-1iadl42-hover-focus="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="button" tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy r-42olwf r-rs99b7 r-18u37iz r-18kxxzh r-1cmwbt1 r-1777fci r-1ny4l3l r-1r8g8re r-1pa6394 r-18c69zk r-mk0yit r-1acpoxo" style="transition-duration:0.15s" data-testid="pageToolbar.paletteButton"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" data-rnwibutton-37p410-hover-focus="true" data-rnwi-handle="nearest" class="r-h7gdob" style="vertical-align:middle;width:18px;height:18px"><path fill="currentColor" d="M8 2.4a1.1 1.1 0 1 0 0 2.2 1.1 1.1 0 0 0 0-2.2ZM8 6.9a1.1 1.1 0 1 0 0 2.2 1.1 1.1 0 0 0 0-2.2ZM8 11.4a1.1 1.1 0 1 0 0 2.2 1.1 1.1 0 0 0 0-2.2Z"></path></svg></div></div><div class="view_manYY row_apb2Z justifySpaceBetween_WG1-N alignItemsCenter_Si4Gd"><div class="css-175oi2r r-1wzrnnt r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><span class="base_qcuoW contentParagraph_-qmPj colorMuted_Nk-dv selectable_gP-v9">당신의 비즈니스에 도움이 되는 다양한 자료를 만나보세요.</span></div></div></div></div></div></div></div><div data-rnwrdesktop-1uwte3a="true" class="css-175oi2r"><div class="css-175oi2r r-bnwqim"><div data-testid="page.contentEditor" data-slate-editor="true" data-document-key="2bfb3c3ad4eb4b62ba968baaf215288b" data-key="2bfb3c3ad4eb4b62ba968baaf215288b" autoCorrect="on" spellcheck="true" style="outline:none;white-space:pre-wrap;word-wrap:break-word"><div><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="view_manYY blockWrapper_8BIg7 vertical0_jPhI0 horizontalAuto_xck7M"><div data-rnwr1490-1777fci="true" data-rnwr700-1777fci="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz r-1777fci"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><div class="css-175oi2r"><div data-key="f6da7bb3caea45bfbc77addf6ed46167" class="view_manYY relative_kNGzo column_Pzect vertical400_IGNdU top400_n25lP bottom400_6eeBF"><div data-block-content="f6da7bb3caea45bfbc77addf6ed46167" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-eqz5dr r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ro0kt6 r-16y2uox r-1wbh5a2"><div data-rnwr700-1w6e6rj-1777fci="true" class="css-175oi2r r-18u37iz r-1777fci r-zo7nv5 r-3mtglp"><div data-slate-void="true" data-key="ffa6ca2783c24b4fad5752cf273b50dc"><div><div class="css-175oi2r r-1awozwy r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r r-z2wwpe r-bnwqim" style="max-width:100%;max-height:100%"><div data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy" style="transition-duration:0.15s"><img alt="" src="https://3168043928-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-MVZVmVOd-5LtENUPqdq%2F-Ma8cviUkWI2ayhujcav%2F-Ma8d5rJTWO6Iq9Qr6K8%2Finitial_top.png?alt=media&amp;token=38e22c88-ee09-463f-b466-8e34643d1c32" width="100%" height="auto" decoding="async" class="r-z2wwpe r-dnmrzs"/></div></div></div></div></div></div></div></div></div></div></div></div></div></div></div><div><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="view_manYY blockWrapper_8BIg7 vertical0_jPhI0 horizontalAuto_xck7M"><div data-rnwr1490-1777fci="true" data-rnwr700-1777fci="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz r-1777fci"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><div class="css-175oi2r"><div data-key="1f7edeb7481d46b0a81fe79f9daa6780" class="view_manYY relative_kNGzo column_Pzect vertical400_IGNdU top200_FwkHm bottom200_HuRwz"><div data-block-content="1f7edeb7481d46b0a81fe79f9daa6780" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-eqz5dr r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ro0kt6 r-16y2uox r-1wbh5a2"><div dir="auto" class="css-1rynq56 r-gg6oyi r-ubezar r-1o2nx2a r-135wba7 r-37p410 r-fdjqy7 r-1xnzce8"><span data-key="f8ab901ac9ed4ea8bb98b25b7137616d"><span data-offset-key="f8ab901ac9ed4ea8bb98b25b7137616d:0">카카오에서 처음 비즈니스를 시작하더라도 쉽게 따라할 수 있고, 궁금한 점이 있을 때는 빠르게 해결할 수 있도록 유용한 가이드와 자주 묻는 질문을 모아두었습니다!</span></span></div></div></div></div></div></div></div></div></div></div><div><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="view_manYY blockWrapper_8BIg7 vertical0_jPhI0 horizontalAuto_xck7M"><div data-rnwr1490-1777fci="true" data-rnwr700-1777fci="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz r-1777fci"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><div class="css-175oi2r"><div data-key="73d305d217fd4b7fa357dd9355fe9260" class="view_manYY relative_kNGzo column_Pzect vertical400_IGNdU top200_FwkHm bottom200_HuRwz"><div data-block-content="73d305d217fd4b7fa357dd9355fe9260" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-eqz5dr r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ro0kt6 r-16y2uox r-1wbh5a2"><div dir="auto" class="css-1rynq56 r-gg6oyi r-ubezar r-1o2nx2a r-135wba7 r-37p410 r-fdjqy7 r-1xnzce8"><span data-key="cdc1a4e3185f4d5086632857c3f6bac7"><span data-offset-key="cdc1a4e3185f4d5086632857c3f6bac7:0"><span data-slate-zero-width="n">​</span></span></span></div></div></div></div></div></div></div></div></div></div><div><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="view_manYY blockWrapper_8BIg7 vertical0_jPhI0 horizontalAuto_xck7M"><div data-rnwr1490-1777fci="true" data-rnwr700-1777fci="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz r-1777fci"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><div class="css-175oi2r"><div data-key="2d17861fabf249db88fcd5217ca251e9" class="view_manYY relative_kNGzo column_Pzect vertical400_IGNdU top600_sT-91 bottom200_HuRwz"><div data-block-content="2d17861fabf249db88fcd5217ca251e9" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-eqz5dr r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ro0kt6 r-16y2uox r-1wbh5a2"><h2 class="r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-18u37iz r-obd0qt" id="undefined"><div dir="auto" data-rnwrdesktop-gg6oyi-1x35g6-37tt59-b88u0q="true" data-rnwr700-gg6oyi-adyw6z-135wba7-b88u0q="true" class="css-1rynq56 r-37p410 r-fdjqy7 r-1xnzce8" id="text-undefined"><span data-key="9e131e44c56f4246a4f663d4ebf1e4da"><span data-offset-key="9e131e44c56f4246a4f663d4ebf1e4da:0">비즈니스 성공의 첫 단계 </span></span><a href="#undefined" aria-label="Direct link to heading" data-rnwi-1pa6394-="true" data-rnwi--146vlhe-hover-focus="true" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" class="css-1qaijid r-1awozwy r-xoduu5 r-1jkjb r-orgf3d r-1loqt21"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 16 16" preserveAspectRatio="xMidYMid meet" role="presentation" style="vertical-align:middle;width:20px;height:20px"><path fill="currentColor" fill-rule="evenodd" d="M7.42 1.925a.6.6 0 0 1 .405.745L7.167 4.9h3.998l.76-2.57a.6.6 0 1 1 1.15.34l-.659 2.23H14a.6.6 0 0 1 0 1.2h-1.938l-1.123 3.8H13a.6.6 0 0 1 0 1.2h-2.415l-.76 2.57a.6.6 0 0 1-1.15-.34l.658-2.23H5.335l-.76 2.57a.6.6 0 1 1-1.15-.34l.658-2.23H2a.6.6 0 1 1 0-1.2h2.438l1.123-3.8H3a.6.6 0 0 1 0-1.2h2.915l.76-2.57a.6.6 0 0 1 .745-.405ZM6.812 6.1 5.689 9.9h3.999l1.123-3.8H6.812Z" clip-rule="evenodd"></path></svg></a></div></h2></div></div></div></div></div></div></div></div></div><div><div data-slate-void="true" data-key="d6c2fef83b0d487b87e5fda22b0ab002"><div><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="view_manYY blockWrapper_8BIg7 vertical0_jPhI0 horizontalAuto_xck7M"><div data-rnwr1490-1777fci="true" data-rnwr700-1777fci="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz r-1777fci"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><div class="css-175oi2r"><div data-key="d6c2fef83b0d487b87e5fda22b0ab002" class="view_manYY relative_kNGzo column_Pzect vertical400_IGNdU top400_n25lP bottom400_6eeBF"><div data-block-content="d6c2fef83b0d487b87e5fda22b0ab002" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-eqz5dr r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><div class="css-175oi2r r-150rngu r-18u37iz r-16y2uox r-1wbh5a2 r-lltvgl r-buy8e9 r-1sncvnh r-1yadl64"><div class="css-175oi2r r-eqz5dr r-1udh08x r-bnwqim"><table class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-eqz5dr r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010"><tbody class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-eqz5dr r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010"><tr data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="table-row" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-18u37iz"><td class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-fdjqy7 r-18u37iz r-1777fci"><div class="css-175oi2r" style="position:relative;padding-top:8px;padding-bottom:8px;padding-right:16px;padding-left:16px;border-left-width:0px;border-top-width:0px;border-top-color:rgba(227,232,237,1.00);border-right-color:rgba(227,232,237,1.00);border-bottom-color:rgba(227,232,237,1.00);border-left-color:rgba(227,232,237,1.00);flex-direction:row;align-items:center;font-weight:700;width:748px"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div data-key="1b2cf0d3e07a4319be2530cb6b805cf7" data-fragment="true" data-slate-editor="true" data-document-key="2bfb3c3ad4eb4b62ba968baaf215288b"><div data-key="4d61e121bfdf40abac454ec2cff84ba0" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-eqz5dr r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010"><div dir="auto" class="css-1rynq56 r-gg6oyi r-ubezar r-1o2nx2a r-135wba7 r-37p410 r-fdjqy7 r-1xnzce8"><span data-key="571844fee3744743b0187959e032a770"><span data-offset-key="571844fee3744743b0187959e032a770:0"><span data-slate-zero-width="z">​</span></span></span><span data-slate-void="true" data-key="e926a91368e5461ab1e2d063172a7ec5"><span><span class="base_qcuoW verticalAlignMiddle_PBEii"><div class="view_manYY container_4xc2q"><div class="css-175oi2r r-4qtqp9 r-bnwqim" style="width:16px;height:16px"><span class="emj-objects _1f50d" role="img" title="magnifying glass tilted left" aria-label="magnifying glass tilted left" style="transform:translate(-50%, -50%) scale(0.25)">🔍</span></div></div></span></span></span><span data-key="e8cf1db18f3d463e82ea502ba770f90e"><span data-offset-key="e8cf1db18f3d463e82ea502ba770f90e:0">카카오비즈니스 시작하기</span></span></div></div></div></div></div></td></tr><tr data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="table-row" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-18u37iz"><td class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-fdjqy7 r-18u37iz r-1777fci"><div class="css-175oi2r" style="position:relative;padding-top:8px;padding-bottom:8px;padding-right:16px;padding-left:16px;border-left-width:0px;border-top-width:1px;border-top-color:rgba(227,232,237,1.00);border-right-color:rgba(227,232,237,1.00);border-bottom-color:rgba(227,232,237,1.00);border-left-color:rgba(227,232,237,1.00);flex-direction:row;align-items:center;width:748px"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div data-key="b56948c701c4454daf3651e69dd9894d" data-fragment="true" data-slate-editor="true" data-document-key="2bfb3c3ad4eb4b62ba968baaf215288b"><div data-key="1467f16a8c4e46a3aac88d74226a5363" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-eqz5dr r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010"><div dir="auto" class="css-1rynq56 r-gg6oyi r-ubezar r-1o2nx2a r-135wba7 r-37p410 r-fdjqy7 r-1xnzce8"><span data-key="db0fca08f7ec40bd975ca337f26cd706"><strong data-slate-leaf="true" data-offset-key="db0fca08f7ec40bd975ca337f26cd706:0" class="r-crgep1 r-b88u0q">STEP 1   카카오 계정을 만드는 방법을 알아보세요   </strong></span><!--$--><a href="/main/undefined/untitled" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="link" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1471scf" style="transition-duration:0.15s"><span data-key="c705895fac9e4de1ba873c1454c9716b" data-rnwilink--146vlhe-="true" data-rnwilink--a9ztke-1ddef8g-hover="true" data-rnwi-handle="nearest" class="r-crgep1"><span data-key="33b66d90d26145c8a6288c2c71866ff7"><span data-offset-key="33b66d90d26145c8a6288c2c71866ff7:0">자세히보기 ＞</span></span></span></a><!--/$--><span data-key="760efd2bfa4f4bc89bf6b7d698eb8658"><strong data-slate-leaf="true" data-offset-key="760efd2bfa4f4bc89bf6b7d698eb8658:0" class="r-crgep1 r-b88u0q">                                                                                                       </strong><span data-offset-key="760efd2bfa4f4bc89bf6b7d698eb8658:1"> </span></span></div></div></div></div></div></td></tr><tr data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="table-row" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-18u37iz"><td class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-fdjqy7 r-18u37iz r-1777fci"><div class="css-175oi2r" style="position:relative;padding-top:8px;padding-bottom:8px;padding-right:16px;padding-left:16px;border-left-width:0px;border-top-width:1px;border-top-color:rgba(227,232,237,1.00);border-right-color:rgba(227,232,237,1.00);border-bottom-color:rgba(227,232,237,1.00);border-left-color:rgba(227,232,237,1.00);flex-direction:row;align-items:center;width:748px"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div data-key="d8dbde980abe45248cb5a00d285adc9f" data-fragment="true" data-slate-editor="true" data-document-key="2bfb3c3ad4eb4b62ba968baaf215288b"><div data-key="e293c48e615947f4b22b51107b5499a3" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-eqz5dr r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010"><div dir="auto" class="css-1rynq56 r-gg6oyi r-ubezar r-1o2nx2a r-135wba7 r-37p410 r-fdjqy7 r-1xnzce8"><span data-key="94a761a7c8c541c1b296e9098ba4ef94"><strong data-slate-leaf="true" data-offset-key="94a761a7c8c541c1b296e9098ba4ef94:0" class="r-crgep1 r-b88u0q">STEP 2   카카오톡 비즈니스 채널을 만들어보세요   </strong></span><!--$--><a href="/main/channel/start" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="link" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1471scf" style="transition-duration:0.15s"><span data-key="d92e446dd7234ecc9f3f6d6a0a14301f" data-rnwilink--146vlhe-="true" data-rnwilink--a9ztke-1ddef8g-hover="true" data-rnwi-handle="nearest" class="r-crgep1"><span data-key="35ce5109bc9f46a693928d3945a668eb"><span data-offset-key="35ce5109bc9f46a693928d3945a668eb:0">자세히보기 ＞</span></span></span></a><!--/$--><span data-key="400b2eb7f26548ad96769518b81ff85b"><strong data-slate-leaf="true" data-offset-key="400b2eb7f26548ad96769518b81ff85b:0" class="r-crgep1 r-b88u0q">                                                                                                       </strong><span data-offset-key="400b2eb7f26548ad96769518b81ff85b:1"> </span></span></div></div></div></div></div></td></tr><tr data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="table-row" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-18u37iz"><td class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-fdjqy7 r-18u37iz r-1777fci"><div class="css-175oi2r" style="position:relative;padding-top:8px;padding-bottom:8px;padding-right:16px;padding-left:16px;border-left-width:0px;border-top-width:1px;border-top-color:rgba(227,232,237,1.00);border-right-color:rgba(227,232,237,1.00);border-bottom-color:rgba(227,232,237,1.00);border-left-color:rgba(227,232,237,1.00);flex-direction:row;align-items:center;border-bottom-width:1px;width:748px"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div data-key="39543cd97f9442f49d60732b1909c1b7" data-fragment="true" data-slate-editor="true" data-document-key="2bfb3c3ad4eb4b62ba968baaf215288b"><div data-key="33cf6dc32ddc412cbe42e5f942d08408" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-1mlwlqe r-eqz5dr r-1q142lx r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010"><div dir="auto" class="css-1rynq56 r-gg6oyi r-ubezar r-1o2nx2a r-135wba7 r-37p410 r-fdjqy7 r-1xnzce8"><span data-key="97b97b4935ec431ba999efb5b18b24df"><strong data-slate-leaf="true" data-offset-key="97b97b4935ec431ba999efb5b18b24df:0" class="r-crgep1 r-b88u0q">STEP 3   광고를 연결하여 더 많은 사용자에게 도달해보세요   </strong></span><!--$--><a href="/main/ad/moment/start" data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="link" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1471scf" style="transition-duration:0.15s"><span data-key="1af3c65a17d5456a9382d5f4913be888" data-rnwilink--146vlhe-="true" data-rnwilink--a9ztke-1ddef8g-hover="true" data-rnwi-handle="nearest" class="r-crgep1"><span data-key="10c05b70fc964a008e3c4b638272da9f"><span data-offset-key="10c05b70fc964a008e3c4b638272da9f:0">자세히보기 ＞</span></span></span></a><!--/$--><span data-key="7d682ecdcb974a9b8cd81c1f0fa002e2"><strong data-slate-leaf="true" data-offset-key="7d682ecdcb974a9b8cd81c1f0fa002e2:0" class="r-crgep1 r-b88u0q">                                                                        </strong><span data-offset-key="7d682ecdcb974a9b8cd81c1f0fa002e2:1">        </span></span></div></div></div></div></div></td></tr></tbody></table></div></div></div></div></div></div></div></div></div></div></div></div></div></div><div><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="view_manYY blockWrapper_8BIg7 vertical0_jPhI0 horizontalAuto_xck7M"><div data-rnwr1490-1777fci="true" data-rnwr700-1777fci="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz r-1777fci"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><div class="css-175oi2r"><div data-key="f20fb6bfa9e64aa4bedbbfa5dff56fe0" class="view_manYY relative_kNGzo column_Pzect vertical400_IGNdU top200_FwkHm bottom200_HuRwz"><div data-block-content="f20fb6bfa9e64aa4bedbbfa5dff56fe0" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-eqz5dr r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ro0kt6 r-16y2uox r-1wbh5a2"><div dir="auto" class="css-1rynq56 r-gg6oyi r-ubezar r-1o2nx2a r-135wba7 r-37p410 r-fdjqy7 r-1xnzce8"><span data-key="6bae44b72b354f6b81a61268203d65ab"><span data-offset-key="6bae44b72b354f6b81a61268203d65ab:0"><span data-slate-zero-width="n">​</span></span></span></div></div></div></div></div></div></div></div></div></div><div><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="view_manYY blockWrapper_8BIg7 vertical0_jPhI0 horizontalAuto_xck7M"><div data-rnwr1490-1777fci="true" data-rnwr700-1777fci="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz r-1777fci"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><div class="css-175oi2r"><div data-key="6c44d250e50643baa169453106c65580" class="view_manYY relative_kNGzo column_Pzect vertical400_IGNdU top200_FwkHm bottom200_HuRwz"><div data-block-content="6c44d250e50643baa169453106c65580" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-eqz5dr r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ro0kt6 r-16y2uox r-1wbh5a2"><div dir="auto" class="css-1rynq56 r-gg6oyi r-ubezar r-1o2nx2a r-135wba7 r-37p410 r-fdjqy7 r-1xnzce8"><span data-key="10d8fdcb3d164e8db76962c140bd73c8"><span data-offset-key="10d8fdcb3d164e8db76962c140bd73c8:0"><span data-slate-zero-width="n">​</span></span></span></div></div></div></div></div></div></div></div></div></div><div><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="view_manYY blockWrapper_8BIg7 vertical0_jPhI0 horizontalAuto_xck7M"><div data-rnwr1490-1777fci="true" data-rnwr700-1777fci="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz r-1777fci"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><div class="css-175oi2r"><div data-key="760fc426494f46e38bc873d9fc9aabea" class="view_manYY relative_kNGzo column_Pzect vertical400_IGNdU top400_n25lP bottom400_6eeBF"><div data-block-content="760fc426494f46e38bc873d9fc9aabea" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-eqz5dr r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ro0kt6 r-16y2uox r-1wbh5a2"><div data-rnwr700-1w6e6rj-1777fci="true" class="css-175oi2r r-18u37iz r-1777fci r-zo7nv5 r-3mtglp"><div data-slate-void="true" data-key="d123c6af9bfa4d88b6918a7e8bc2296b"><div><div class="css-175oi2r r-1awozwy r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r r-z2wwpe r-bnwqim" style="max-width:100%;max-height:100%"><div data-rnwi-5xr8s6-dse9kg-2fw26j-wjlvf2-focus-visible="true" data-rnwi-handle="nearest" tabindex="0" class="css-175oi2r r-1i6wzkk r-lrvibr r-1loqt21 r-1otgn73 r-1awozwy" style="transition-duration:0.15s"><img alt="" loading="lazy" src="https://3168043928-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-MVZVmVOd-5LtENUPqdq%2F-Ma8cviUkWI2ayhujcav%2F-Ma8d9kBolhuYtPzlY5X%2Finitial_ch.png?alt=media&amp;token=ba82ee8f-9c77-4fce-b998-7d41ed540dc5" width="100%" height="auto" decoding="async" class="r-z2wwpe r-dnmrzs"/></div></div></div></div></div></div></div></div></div></div></div></div></div></div></div><div><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="view_manYY blockWrapper_8BIg7 vertical0_jPhI0 horizontalAuto_xck7M"><div data-rnwr1490-1777fci="true" data-rnwr700-1777fci="true" class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2 r-18u37iz r-1777fci"><div class="css-175oi2r r-1ro0kt6 r-16y2uox r-1wbh5a2"><div class="css-175oi2r"><div class="css-175oi2r"><div data-key="3d960ca3351547fb81e97b90804b1929" class="view_manYY relative_kNGzo column_Pzect vertical400_IGNdU top200_FwkHm bottom200_HuRwz"><div data-block-content="3d960ca3351547fb81e97b90804b1929" class="r-1oszu61 r-1xc7w19 r-1phboty r-1yadl64 r-deolkf r-6koalj r-eqz5dr r-crgep1 r-ifefl9 r-bcqeeo r-t60dpp r-bnwqim r-417010 r-1ro0kt6 r-16y2uox r-1wbh5a2"><div dir="auto" class="css-1rynq56 r-gg6oyi r-ubezar r-1o2nx2a r-135wba7 r-37p410 r-fdjqy7 r-1xnzce8"><span data-key="b3b3bb383efc4d0696c81ecbd2cf1e2d"><span data-offset-key="b3b3bb383efc4d0696c81ecbd2cf1e2d:0">카카오톡 채널은 고객
