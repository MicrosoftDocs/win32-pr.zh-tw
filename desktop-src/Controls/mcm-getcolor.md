---
title: 'MCM_GETCOLOR 訊息 (Commctrl .h) '
description: 抓取月曆控制項指定部分的色彩。 您可以使用 MonthCal GetColor 宏明確地傳送此訊息 \_ 。
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- MCM_GETCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254b140e801f4d4440c9b292999e5c8f91175a30750b08bfd30abd6afd84f73d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062088"
---
# <a name="mcm_getcolor-message"></a>MCM \_ GETCOLOR 訊息

抓取月曆控制項指定部分的色彩。 您可以使用 [**MonthCal \_ GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**Int** 類型的值，指定要取出的月曆色彩。 這個值可以是下列其中一個值：



| 值                                                                                                                                                                     | 意義                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**MCSC \_ 背景**</dt> </dl>       | 取得顯示在月份之間的背景色彩。<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | 取得在月份內顯示的背景色彩。<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**MCSC \_ 文字**</dt> </dl>                         | 取得用來在一個月內顯示文字的色彩。<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | 取出日曆標題中顯示的背景色彩。<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | 抓取用來顯示行事曆標題內文字的色彩。<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | 抓取用來顯示頁首日和尾端日文字的色彩。 [頁首] 和 [結束日期] 是出現在當月日曆上的上個月和之後幾天。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回代表月曆控制項指定部分之色彩設定的 **COLORREF** 值。 否則，此訊息會傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





