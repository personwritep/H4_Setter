// ==UserScript==
// @name        H4 Setter ⭐
// @namespace        http://tampermonkey.net/
// @version        0.1
// @description        ブログ編集画面で任意のdiv要素を「h4」に変更する
// @author        Ameba Blog User
// @match        https://blog.ameba.jp/ucs/entry/srventry*
// @exclude        https://blog.ameba.jp/ucs/entry/srventrylist*
// @icon        https://www.google.com/s2/favicons?sz=64&domain=ameba.jp
// @grant        none
// @updateURL        https://github.com/personwritep/H4_Setter/raw/main/H4_Setter.user.js
// @downloadURL        https://github.com/personwritep/H4_Setter/raw/main/H4_Setter.user.js
// ==/UserScript==


let retry=0;
let interval=setInterval(wait_target, 20);
function wait_target(){
    retry++;
    if(retry>100){ // リトライ制限 100回 2sec
        clearInterval(interval); }
    let target=document.getElementById('cke_1_contents'); // 監視 target
    if(target){
        clearInterval(interval);
        main(target); }}


function main(target){

    let monitor=new MutationObserver(set_elem);
    monitor.observe(target, {childList: true});

    set_elem();

    function set_elem(){
        let editor_iframe=document.querySelector('.cke_wysiwyg_frame');
        if(editor_iframe){ // iframe読込みが実行条件
            let iframe_doc=editor_iframe.contentWindow.document;
            if(iframe_doc){
                let hset=
                    '<style class="hset">'+
                    'h4::before { content: "▶"; position: absolute; left: -20px; color:red; '+
                    'font: normal 16px Meiryo; }'+
                    '</style>';

                if(!iframe_doc.querySelector('.hset')){
                    iframe_doc.documentElement.insertAdjacentHTML('beforeend', hset); }


                iframe_doc.addEventListener('click', function(event){
                    if(event.ctrlKey){
                        let elem=iframe_doc.elementFromPoint(event.clientX, event.clientY);
                        let div_elem=elem.closest('div');
                        if(div_elem.parentElement==iframe_doc.body){
                            if(!div_elem.querySelector('a')){ // リンクカードを除外
                                let outer=div_elem.outerHTML;
                                let regexp_s=/<div/;
                                let regexp_e=/<\/div>$/;
                                let new_s=outer.replace(regexp_s, '<h4');
                                let new_e=new_s.replace(regexp_e, '</h4>');
                                div_elem.outerHTML=new_e; }
                        }}});

            }}} // set_elem()

} // main()
