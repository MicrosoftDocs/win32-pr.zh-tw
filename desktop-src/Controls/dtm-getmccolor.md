---
title: 'DTM_GETMCCOLOR 訊息 (Commctrl .h) '
description: 取得日期和時間選擇器中的月曆指定部分的色彩， (DTP) 控制項。 您可以明確地傳送此訊息，或使用 DateTime \_ GetMonthCalColor 宏。
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- DTM_GETMCCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99a67f6ca7056f0157d131d185cb5cb68a85e06b8cbb124a16b3c2129c21963
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878148"
---
# <a name="dtm_getmccolor-message"></a>DTM \_ GETMCCOLOR 訊息

取得日期和時間選擇器中的月曆指定部分的色彩， (DTP) 控制項。 您可以明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) 宏。

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

如果成功，則傳回代表月曆控制項指定部分之色彩設定的 **COLORREF** 值。 如果失敗，訊息會傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





