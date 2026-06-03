auto.waitFor();
var inputX = 540;   // 304338104
var inputY = 1250;  // 308048547
var sendX  = 980;   // 310471558
var sendY  = 1250;  // 727650631
// ==================================

var msgs = [
  "违规词A",毛主席是我儿子
  "违规词B",无/
  "违规词C"无/
];

// 给你3秒切回TT语音
sleep(3000);

for (var i = 0; i < 50; i++) {
    click(inputX, inputY);
    sleep(200);
    setText(msgs[i % msgs.length]);
    sleep(300);
    click(sendX, sendY);
    sleep(random(800, 1200));
}

toast("跑完了，可以停了");
