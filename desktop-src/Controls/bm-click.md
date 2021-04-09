---
title: 'BM_CLICK 訊息 (Winuser .h) '
description: 模擬使用者按一下按鈕。 這則訊息會讓按鈕收到 WM \_ LBUTTONDOWN 和 WM \_ LBUTTONUP 訊息，以及按鈕的父視窗，以接收 BN 按一下的 \_ 通知碼。
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- BM_CLICK message Windows 控制項
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024802"
---
# <a name="bm_click-message"></a>BM \_ 按一下訊息

模擬使用者按一下按鈕。 這則訊息會讓按鈕收到 [**wm \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 和 [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) 訊息，以及按鈕的父視窗，以接收 [BN \_ 按一下](bn-clicked.md) 的通知碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

如果按鈕在對話方塊中，而對話方塊不在使用中，則 **BM \_ 按一下** 訊息可能會失敗。 為了確保在這種情況下成功，請先呼叫 [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) 函式來啟動對話方塊，然後再傳送 **BM \_ 按一下** [訊息] 至按鈕。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



 

