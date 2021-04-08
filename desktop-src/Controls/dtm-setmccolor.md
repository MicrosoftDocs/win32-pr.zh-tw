---
title: 'DTM_SETMCCOLOR 訊息 (Commctrl .h) '
description: 在日期和時間選擇器中，設定日曆指定部分的色彩， (DTP) 控制項。 您可以明確地傳送此訊息，或使用 DateTime \_ SetMonthCalColor 宏。
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- DTM_SETMCCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686173"
---
# <a name="dtm_setmccolor-message"></a>DTM \_ SETMCCOLOR 訊息

在日期和時間選擇器中，設定日曆指定部分的色彩， (DTP) 控制項。 您可以明確地傳送此訊息，或使用 [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) 宏。

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

**COLORREF** 值，表示將針對月曆的指定區域設定的色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **COLORREF** 值，表示如果成功，則表示月曆控制項指定部分的先前色彩設定。 否則，訊息會傳回-1。

## <a name="remarks"></a>備註

啟用視覺化樣式時，除了 *wParam* 為 MCSC 背景時，此訊息不會有任何作用 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





