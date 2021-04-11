---
title: 'SBM_GETRANGE 訊息 (Winuser .h) '
description: 傳送 SBM \_ GETRANGE 訊息，以抓取捲軸控制項的最小和最大位置值。
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- SBM_GETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934788"
---
# <a name="sbm_getrange-message"></a>SBM \_ GETRANGE 訊息

傳送 **SBM \_ GETRANGE** 訊息，以抓取捲軸控制項的最小和最大位置值。

應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **GetScrollRange** 函數才能正常運作。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

接收最小滾動位置之變數的指標。

</dd> <dt>

*lParam* 
</dt> <dd>

接收最大滾動位置之變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SETRANGE**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

