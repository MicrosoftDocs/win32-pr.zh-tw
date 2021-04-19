---
title: '捲軸控制項樣式 (Winuser .h) '
description: 若要使用 CreateWindow 或 CreateWindowEx 函式來建立捲軸控制項，請指定捲軸類別、適當的視窗樣式常數，以及下列捲軸控制項樣式的組合。
ms.assetid: 07195a95-eff8-4a47-926a-9d503fa7b299
topic_type:
- apiref
api_name:
- SBS_BOTTOMALIGN
- SBS_HORZ
- SBS_LEFTALIGN
- SBS_RIGHTALIGN
- SBS_SIZEBOX
- SBS_SIZEBOXBOTTOMRIGHTALIGN
- SBS_SIZEBOXTOPLEFTALIGN
- SBS_SIZEGRIP
- SBS_TOPALIGN
- SBS_VERT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5de721fd4cc44867fca0dbe1b35dcaf58c6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992579"
---
# <a name="scroll-bar-control-styles"></a>捲軸控制項樣式

若要使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立捲軸控制項，請指定捲軸類別、適當的視窗樣式常數，以及下列捲軸控制項樣式的組合。 某些樣式會建立使用預設寬度或高度的捲軸控制項。 但是，當您呼叫 **CreateWindow** 或 **CreateWindowEx** 時，一定要指定捲軸的 x 和 y 座標和其他維度。



| 常數                                                                                                                                                                                                | 描述                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SBS_BOTTOMALIGN"></span><span id="sbs_bottomalign"></span><dl> <dt>**SBS \_ BOTTOMALIGN**</dt> </dl>                                     | 將捲軸的下邊緣與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)函式的 *x*、 *y*、 *nWidth* 和 *nHeight* 參數所定義之矩形的下邊緣對齊。 捲軸具有系統捲軸的預設高度。 使用此樣式搭配 SBS \_ HORZ 樣式。<br/>                      |
| <span id="SBS_HORZ"></span><span id="sbs_horz"></span><dl> <dt>**SBS \_ HORZ**</dt> </dl>                                                          | 指定水準捲軸。 如果 \_ 未指定 sbs BOTTOMALIGN 或 sbs \_ TOPALIGN 樣式，則捲軸具有 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的 *x*、 *y*、 *nWidth* 和 *nHeight* 參數所指定的高度、寬度和位置。<br/>                                                      |
| <span id="SBS_LEFTALIGN"></span><span id="sbs_leftalign"></span><dl> <dt>**SBS \_ LEFTALIGN**</dt> </dl>                                           | 將捲軸的左邊緣與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的 *x*、 *y*、 *nWidth* 和 *nHeight* 參數所定義之矩形的左邊緣對齊。 捲軸具有系統捲軸的預設寬度。 使用此樣式搭配 SBS \_ 垂直樣式。<br/>                                    |
| <span id="SBS_RIGHTALIGN"></span><span id="sbs_rightalign"></span><dl> <dt>**SBS \_ RIGHTALIGN**</dt> </dl>                                        | 將捲軸的右邊緣與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的 *x*、 *y*、 *nWidth* 和 *nHeight* 參數所定義之矩形的右邊緣對齊。 捲軸具有系統捲軸的預設寬度。 使用此樣式搭配 SBS \_ 垂直樣式。<br/>                                  |
| <span id="SBS_SIZEBOX"></span><span id="sbs_sizebox"></span><dl> <dt>**SBS \_ SIZEBOX**</dt> </dl>                                                 | 指定大小方塊。 如果您未指定 SBS \_ SIZEBOXBOTTOMRIGHTALIGN 或 sbs \_ SIZEBOXTOPLEFTALIGN 樣式，則 [大小] 方塊具有 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的 *x*、 *y*、 *nWidth* 和 *nHeight* 參數所指定的高度、寬度和位置。 <br/>                                          |
| <span id="SBS_SIZEBOXBOTTOMRIGHTALIGN"></span><span id="sbs_sizeboxbottomrightalign"></span><dl> <dt>**SBS \_ SIZEBOXBOTTOMRIGHTALIGN**</dt> </dl> | 將 [大小] 方塊右下角與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)之 *x*、 *y*、 *nWidth* 和 *nHeight* 參數所指定矩形的右下角對齊。 [大小] 方塊具有 [系統大小] 方塊的預設大小。 使用此樣式搭配 SBS \_ SIZEBOX 或 sbs \_ SIZEGRIP 樣式。<br/> |
| <span id="SBS_SIZEBOXTOPLEFTALIGN"></span><span id="sbs_sizeboxtopleftalign"></span><dl> <dt>**SBS \_ SIZEBOXTOPLEFTALIGN**</dt> </dl>             | 將 [大小] 方塊的左上角與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的 *x*、 *y*、 *nWidth* 和 *nHeight* 參數所指定的矩形左上角對齊。 [大小] 方塊具有 [系統大小] 方塊的預設大小。 使用此樣式搭配 SBS \_ SIZEBOX 或 sbs \_ SIZEGRIP 樣式。<br/>   |
| <span id="SBS_SIZEGRIP"></span><span id="sbs_sizegrip"></span><dl> <dt>**SBS \_ SIZEGRIP**</dt> </dl>                                              | 與 SBS \_ SIZEBOX 相同，但具有引發的 edge。 <br/>                                                                                                                                                                                                                                                                                  |
| <span id="SBS_TOPALIGN"></span><span id="sbs_topalign"></span><dl> <dt>**SBS \_ TOPALIGN**</dt> </dl>                                              | 將捲軸的上邊緣與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的 *x*、 *y*、 *nWidth* 和 *nHeight* 參數所定義之矩形的上邊緣對齊。 捲軸具有系統捲軸的預設高度。 使用此樣式搭配 SBS \_ HORZ 樣式。<br/>                                     |
| <span id="SBS_VERT"></span><span id="sbs_vert"></span><dl> <dt>**SBS \_ 垂直**</dt> </dl>                                                          | 指定垂直捲動條。 如果您未指定 SBS \_ RIGHTALIGN 或 sbs \_ LEFTALIGN 樣式，則捲軸具有 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的 *x*、 *y*、 *nWidth* 和 *nHeight* 參數所指定的高度、寬度和位置。<br/>                                                     |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winuser。h</dt> </dl> |



 

