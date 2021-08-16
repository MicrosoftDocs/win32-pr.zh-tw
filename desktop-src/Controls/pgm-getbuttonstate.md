---
title: 'PGM_GETBUTTONSTATE 訊息 (Commctrl .h) '
description: 抓取頁面導航控制項中指定之按鈕的狀態。 您可以明確地傳送此訊息，或使用呼叫器 \_ GetButtonState 宏。
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- PGM_GETBUTTONSTATE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2014b6e36a0ab883155d786760ef54f02c89ee0d17192d6082d40ad19eec95a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830189"
---
# <a name="pgm_getbuttonstate-message"></a>PGM \_ GETBUTTONSTATE 訊息

抓取頁面導航控制項中指定之按鈕的狀態。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

指出要取得狀態的按鈕。 這個值可以是下列其中一個值：



| 值                                                                                                                                                                     | 意義                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <dt>**PGB \_ TOPORLEFT**</dt> </dl>             | 指出 [**pg \_ 垂直**](pager-control-styles.md) 呼機控制項中的頂端按鈕，或 [**pg \_ HORZ**](pager-control-styles.md) 頁面控制項中的左按鈕。 <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <dt>**PGB \_ BOTTOMORRIGHT**</dt> </dl> | 表示 [**pg \_ 垂直**](pager-control-styles.md) 呼機控制項中的底部按鈕，或 [**pg \_ HORZ**](pager-control-styles.md) 頁面控制項中的右方按鈕。 <br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 *lParam* 中指定之按鈕的狀態。 這會是下列其中一個或多個值 (如果傳回一個以上的值，則會使用位 OR) 來合併它們：



| 傳回碼                                                                                   | 描述                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**PGF \_ 不可見**</dt> </dl> | 看不到此按鈕。 <br/>      |
| <dl> <dt>**PGF \_ 正常**</dt> </dl>    | 按鈕處於正常狀態。 <br/>  |
| <dl> <dt>**PGF \_ 灰色**</dt> </dl>    | 按鈕處於灰色狀態。 <br/>  |
| <dl> <dt>**PGF \_ 按下**</dt> </dl> | 按鈕處於按下狀態。 <br/> |
| <dl> <dt>**PGF \_ 熱**</dt> </dl>       | 按鈕處於作用中狀態。 <br/>     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





