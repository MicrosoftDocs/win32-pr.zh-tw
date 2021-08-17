---
title: 'Up-Down 控制項樣式 (CommCtrl .h) '
description: 本節列出建立上下控制項時所使用的樣式。
ms.assetid: d35198cb-6a5b-485e-a914-1b2ede53462f
topic_type:
- apiref
api_name:
- UDS_ALIGNLEFT
- UDS_ALIGNRIGHT
- UDS_ARROWKEYS
- UDS_AUTOBUDDY
- UDS_HORZ
- UDS_HOTTRACK
- UDS_NOTHOUSANDS
- UDS_SETBUDDYINT
- UDS_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809ab4ce2c4d8670363dc7f0751ae4a3756ee7b4e5dc9b75c79986c3a56d359d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957697"
---
# <a name="up-down-control-styles"></a>Up-Down 控制項樣式

本節列出建立上下控制項時所使用的樣式。



| 常數                                                                                                                                                            | 描述                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UDS_ALIGNLEFT"></span><span id="uds_alignleft"></span><dl> <dt>**UD \_ ALIGNLEFT**</dt> </dl>       | 將上下控制項放在好友視窗左邊緣的旁邊。 好友視窗會移至右邊，並減少其寬度以容納上下按鈕控制項的寬度。<br/>                                                                                                                                                                                                   |
| <span id="UDS_ALIGNRIGHT"></span><span id="uds_alignright"></span><dl> <dt>**UD \_ ALIGNRIGHT**</dt> </dl>    | 在好友視窗的右邊緣旁邊放置上下控制項。 好友視窗的寬度會減少以容納上下按鈕控制項的寬度。<br/>                                                                                                                                                                                                                          |
| <span id="UDS_ARROWKEYS"></span><span id="uds_arrowkeys"></span><dl> <dt>**UD \_ ARROWKEYS**</dt> </dl>       | 當按下向上鍵和向下鍵時，會讓下一個控制項遞增和遞減位置。<br/>                                                                                                                                                                                                                                                                          |
| <span id="UDS_AUTOBUDDY"></span><span id="uds_autobuddy"></span><dl> <dt>**UD \_ AUTOBUDDY**</dt> </dl>       | 以迭置順序自動選取前一個視窗，做為上下按鈕控制項的合作者視窗。<br/>                                                                                                                                                                                                                                                                                                |
| <span id="UDS_HORZ"></span><span id="uds_horz"></span><dl> <dt>**UD \_ HORZ**</dt> </dl>                      | 讓上下按鈕控制項的箭號向左和向右指向，而不是向上和向下。<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="UDS_HOTTRACK"></span><span id="uds_hottrack"></span><dl> <dt>**UD \_ HOTTRACK**</dt> </dl>          | 使控制項呈現「熱追蹤」行為。 也就是說，它會在指標通過時，反白顯示控制項上的向上箭號和向下箭號。 此樣式需要 Windows 98 或 Windows 2000。 如果系統正在執行 Windows 95 或 Windows NT 4.0，則會忽略旗標。 若要檢查是否已啟用熱追蹤，請呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)。 <br/> |
| <span id="UDS_NOTHOUSANDS"></span><span id="uds_nothousands"></span><dl> <dt>**UD \_ NOTHOUSANDS**</dt> </dl> | 不會在每三個小數位數之間插入千位分隔符號。 <br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="UDS_SETBUDDYINT"></span><span id="uds_setbuddyint"></span><dl> <dt>**UD \_ SETBUDDYINT**</dt> </dl> | 當位置變更時，會讓下一個控制項使用 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息) 來設定合作者視窗的文字 (。 此文字包含格式化為十進位或十六進位字串的位置。<br/>                                                                                                                                                             |
| <span id="UDS_WRAP"></span><span id="uds_wrap"></span><dl> <dt>**UD \_ 換行**</dt> </dl>                      | 如果遞增或減少超出範圍的結束或開頭，則會使位置「換行」。<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

