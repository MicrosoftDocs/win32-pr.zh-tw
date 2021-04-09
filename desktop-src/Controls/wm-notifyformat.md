---
title: 'WM_NOTIFYFORMAT 訊息 (Winuser .h) '
description: 判斷視窗是否接受 WM 通知通知訊息中的 ANSI 或 Unicode 結構 \_ 。 \_從通用控制項將 WM NOTIFYFORMAT 訊息傳送至其父視窗，以及從父視窗傳送至通用控制項。
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- WM_NOTIFYFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934618"
---
# <a name="wm_notifyformat-message"></a>WM \_ NOTIFYFORMAT 訊息

判斷視窗是否接受 [**WM \_ 通知**](wm-notify.md) 通知訊息中的 ANSI 或 Unicode 結構。 **WM \_NOTIFYFORMAT** 訊息會從通用控制項傳送至其父視窗，以及從父視窗傳送至通用控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

傳送 **WM \_ NOTIFYFORMAT** 訊息的視窗控制碼。 如果 *lParam* 為「nf-e \_ 查詢」，這個參數就是控制項的控制碼。 如果 *lParam* 為 nf-e \_ REQUERY，此參數就是控制項父視窗的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

命令值，指定 **WM \_ NOTIFYFORMAT** 訊息的本質。 這會是下列其中一個值：



| 值                                                                                                                                                | 意義                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <dt>**NF-E \_ 查詢**</dt> </dl>       | 此訊息是用來判斷是否應在 [**WM \_ 通知**](wm-notify.md) 訊息中使用 ANSI 或 Unicode 結構的查詢。 此命令會在建立控制項期間從控制項傳送至其父視窗，並回應 NF-E \_ REQUERY 命令。<br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <dt>**NF-E \_ 查詢**</dt> </dl> | 此訊息是控制項的要求，可將 \_ 此訊息的「Nf-e 查詢」表單傳送至其父視窗。 此命令會從父視窗傳送。 父視窗會要求控制項對要在 [**WM \_ 通知**](wm-notify.md) 訊息中使用的結構類型進行重新查詢。 如果 *lParam* 為 nf-e \_ 查詢，則傳回值是重新查詢作業的結果。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                                 | Description                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NFR \_ ANSI**</dt> </dl>    | ANSI 結構應使用於控制項所傳送的 [**WM \_ 通知**](wm-notify.md) 訊息中。<br/>     |
| <dl> <dt>**NFR \_ UNICODE**</dt> </dl> | Unicode 結構應使用於控制項所傳送的 [**WM \_ 通知**](wm-notify.md) 訊息中。 <br/> |
| <dl> <dt>**0**</dt> </dl>            | 發生錯誤。<br/>                                                                                  |



 

## <a name="remarks"></a>備註

建立通用控制項時，控制項會將 **wm \_ NOTIFYFORMAT** 訊息傳送至其父視窗，以判斷要在 [**WM \_ 通知**](wm-notify.md) 訊息中使用的結構類型。 如果父視窗未處理此訊息，則 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會根據父視窗的型別進行回應。 也就是說，如果父視窗是 Unicode 視窗， **DefWindowProc** 會傳回 NFR \_ unicode，如果父視窗是 ANSI 視窗， **DefWindowProc** 會傳回 NFR \_ ANSI。 如果父視窗是對話方塊，而且不處理此訊息，則 [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) 函式會根據 (UNICODE 或 ANSI) 的對話方塊類型來做出類似的回應。

父視窗可以變更通用控制項在 [**WM \_ 通知**](wm-notify.md) 訊息中使用的結構類型，方法是將 *lParam* 設定為 Nf-e \_ REQUERY，然後將 **WM \_ NOTIFYFORMAT** 訊息傳送至控制項。 這會導致控制項將 \_ **WM \_ NOTIFYFORMAT** 訊息的 nf-e 查詢形式傳送至父視窗。

所有的通用控制項都會傳送 **WM \_ NOTIFYFORMAT** 訊息。 但是，標準的 Windows 控制項 (編輯控制項、下拉式方塊、清單方塊、按鈕、捲軸和靜態控制項) 不能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



 

