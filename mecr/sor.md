Gui, add, button, x20 y40 w110 h40, 시작
Gui, add, button, x220 y40 w110 h40, 종료
gui, show
CoordMode, Pixel, Screen
CoordMode, Mouse, Screen

return

Button시작:
{

Loop
{
;화면 위로
;WinSet, AlwaysOnTop, on, SM-N976N

Sleep, 600

;목록보기 클릭
  click,1200,880
Sleep, 1100
;대기중 이미지 찾기
ImageSearch, X1,Y1,1315,317,1391,373,*30 1.png
if(ErrorLevel = 0) {
  click,1313,1026
  Sleep, 200
} else {
;MsgBox %ErrorLevel%
  ;첫번째 병원 클릭
  click,1208,365
  Sleep, 200
  ;예약 클릭
  click,1331,972
  Sleep, 200
  ;종류 선택 클릭
  click,1052,860
  ;예약 클릭
  click,1331,972
  Sleep, 200
  ;확인 클릭
  click,1318,663
  Sleep, 200
}


}
}
return

Button종료:
{
;WinSet, AlwaysOnTop, off, SM-N976N
ExitApp
}


F3::
{
;WinSet, AlwaysOnTop, off, SM-N976N
ExitApp
}
