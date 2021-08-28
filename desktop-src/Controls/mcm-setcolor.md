---
title: 'MCM_SETCOLOR 訊息 (Commctrl .h) '
description: 設定月曆控制項指定部分的色彩。 您可以使用 MonthCal SetColor 宏明確地傳送此訊息 \_ 。
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- MCM_SETCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0915f78ad2dc666d6476cebb51be4f8b8c6102cb1433da59af7b9a1342deedc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697148"
---
# <a name="mcm_setcolor-message"></a>MCM \_ SETCOLOR 訊息

設定月曆控制項指定部分的色彩。 您可以使用 [**MonthCal \_ SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**Int** 類型的值，指定要設定的月曆色彩。 這個值可以是下列其中一個值：



| 值                                                                                                                                                                     | 意義                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**MCSC \_ 背景**</dt> </dl>       | 設定在月份之間顯示的背景色彩。<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | 設定在月份內顯示的背景色彩。<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**MCSC \_ 文字**</dt> </dl>                         | 設定用來顯示一個月內文字的色彩。<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | 設定日曆標題中顯示的背景色彩。<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | 設定用來顯示行事曆標題內文字的色彩。<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | 設定用來顯示頁首日和尾端日文字的色彩。 [頁首] 和 [結束日期] 是出現在當月日曆上的上個月和之後幾天。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) 值，表示將針對月曆的指定區域所設定的色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**COLORREF**](/windows/desktop/gdi/colorref) 值，表示如果成功，則表示月曆控制項指定部分的先前色彩設定。 否則，傳回-1。

## <a name="remarks"></a>備註

如果視覺化樣式為使用中，則除了 *wParam* 為 MCSC 背景時，此訊息沒有任何作用 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

