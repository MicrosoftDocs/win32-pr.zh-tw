---
title: " (CommCtrl 的 [隱藏] 控制項樣式) "
description: 本章節包含與 [資料] 控制項搭配使用之樣式的相關資訊。
ms.assetid: ac2f59c6-85a2-4f41-aace-4132971d3559
topic_type:
- apiref
api_name:
- TBS_AUTOTICKS
- TBS_VERT
- TBS_HORZ
- TBS_TOP
- TBS_BOTTOM
- TBS_LEFT
- TBS_RIGHT
- TBS_BOTH
- TBS_NOTICKS
- TBS_ENABLESELRANGE
- TBS_FIXEDLENGTH
- TBS_NOTHUMB
- TBS_TOOLTIPS
- TBS_REVERSED
- TBS_DOWNISLEFT
- TBS_NOTIFYBEFOREMOVE
- TBS_TRANSPARENTBKGND
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42966f98db18257c9a6a9ca463d5bd88028a02f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981280"
---
# <a name="trackbar-control-styles"></a>[控制項] 控制項樣式

本章節包含與 [資料] 控制項搭配使用之樣式的相關資訊。



| 常數                                                                                                                                                                           | 描述                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_AUTOTICKS"></span><span id="tbs_autoticks"></span><dl> <dt>**TB \_ AUTOTICKS**</dt> </dl>                      | [資料格] 控制項的值範圍內的每個遞增都有一個刻度標記。 <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_VERT"></span><span id="tbs_vert"></span><dl> <dt>**以 TB 為 \_ 垂直**</dt> </dl>                                     | [對齊程式] 控制項是垂直方向。<br/>                                                                                                                                                                                                                                                                                                               |
| <span id="TBS_HORZ"></span><span id="tbs_horz"></span><dl> <dt>**TB \_ HORZ**</dt> </dl>                                     | [並排] 控制項是水準方向的。 這是預設方向。 <br/>                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOP"></span><span id="tbs_top"></span><dl> <dt>**\_最高 TB**</dt> </dl>                                        | [顯示] 控制項會在控制項上方顯示刻度標記。 這個樣式只適用于 [TB] \_ HORZ。 <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_BOTTOM"></span><span id="tbs_bottom"></span><dl> <dt>**最 \_ 小 TB**</dt> </dl>                               | [顯示] 控制項會在控制項下方顯示刻度標記。 這個樣式只適用于 [TB] \_ HORZ。 <br/>                                                                                                                                                                                                                                                      |
| <span id="TBS_LEFT"></span><span id="tbs_left"></span><dl> <dt>**剩餘的 TB \_**</dt> </dl>                                     | [顯示] 控制項會顯示控制項左邊的刻度。 此樣式只有在使用 TB 垂直時才有效 \_ 。 <br/>                                                                                                                                                                                                                                             |
| <span id="TBS_RIGHT"></span><span id="tbs_right"></span><dl> <dt>**最 TB 的 \_ 許可權**</dt> </dl>                                  | [顯示] 控制項會顯示控制項右邊的刻度。 此樣式只有在使用 TB 垂直時才有效 \_ 。 <br/>                                                                                                                                                                                                                                            |
| <span id="TBS_BOTH"></span><span id="tbs_both"></span><dl> <dt>**TB \_**</dt> </dl>                                     | [顯示] 控制項會在控制項的兩側顯示刻度標記。 當搭配使用 [TB] HORZ 時，這會是頂端和底部，如果搭配 [TB] 使用，則為 \_ 左右 \_ 。 <br/>                                                                                                                                                                           |
| <span id="TBS_NOTICKS"></span><span id="tbs_noticks"></span><dl> <dt>**TB \_ NOTICKS**</dt> </dl>                            | [顯示] 控制項不會顯示任何刻度標記。 <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TBS_ENABLESELRANGE"></span><span id="tbs_enableselrange"></span><dl> <dt>**TB \_ ENABLESELRANGE**</dt> </dl>       | [選取範圍] 控制項只會顯示選取範圍。 選取範圍的開始和結束位置上的刻度會顯示為三角形 (而不是垂直虛線) ，而且會反白顯示選取範圍。 <br/>                                                                                                                           |
| <span id="TBS_FIXEDLENGTH"></span><span id="tbs_fixedlength"></span><dl> <dt>**TB \_ FIXEDLENGTH**</dt> </dl>                | [顯示] 控制項可讓滑杆的大小以 [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md) 訊息進行變更。 <br/>                                                                                                                                                                                                                      |
| <span id="TBS_NOTHUMB"></span><span id="tbs_nothumb"></span><dl> <dt>**TB \_ NOTHUMB**</dt> </dl>                            | [顯示] 控制項不會顯示滑杆。 <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="TBS_TOOLTIPS"></span><span id="tbs_tooltips"></span><dl> <dt>**TB \_ 工具提示**</dt> </dl>                         | [版本 4.70](common-control-versions.md)。 [提示] 控制項支援工具提示。 當使用此樣式建立的 [顯示] 控制項時，它會自動建立預設的工具提示控制項，以顯示滑杆的目前位置。 您可以使用 [**TBM \_ SETTIPSIDE**](tbm-settipside.md) 訊息來變更顯示工具提示的位置。 <br/> |
| <span id="TBS_REVERSED"></span><span id="tbs_reversed"></span><dl> <dt>**已 \_ 反轉 TB**</dt> </dl>                         | [版本5.80。](common-control-versions.md)此樣式位會用於「反轉」 trackbars，其中較小的數位表示「較高」，而較大的數位表示「較低」。 它對控制項沒有任何作用;這只是可以檢查的標籤，以判斷是否為正常或反向的標題。<br/>                                             |
| <span id="TBS_DOWNISLEFT"></span><span id="tbs_downisleft"></span><dl> <dt>**TB \_ DOWNISLEFT**</dt> </dl>                   | 依預設，[追蹤器] 控制項使用向右和向上等於左。 您可以使用 [TB] \_ DOWNISLEFT 樣式來反轉預設值，使其向左和向右對齊。 <br/>                                                                                                                                                                          |
| <span id="TBS_NOTIFYBEFOREMOVE"></span><span id="tbs_notifybeforemove"></span><dl> <dt>**TB \_ NOTIFYBEFOREMOVE**</dt> </dl> | [版本 6.00](common-control-versions.md) 和 **Windows Vista。** 由於使用者動作 (啟用貼齊) ，因此在定位滑杆之前，應該會通知父代。 <br/>                                                                                                                                                                                   |
| <span id="TBS_TRANSPARENTBKGND"></span><span id="tbs_transparentbkgnd"></span><dl> <dt>**TB \_ TRANSPARENTBKGND**</dt> </dl> | [版本 6.00](common-control-versions.md) 和 **Windows Vista。** 背景由父系透過 WM \_ PRINTCLIENT 訊息繪製。 <br/>                                                                                                                                                                                                                   |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





