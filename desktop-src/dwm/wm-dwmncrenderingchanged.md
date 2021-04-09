---
title: 'WM_DWMNCRENDERINGCHANGED 訊息 (Winuser .h) '
description: 當非工作區轉譯原則變更時傳送。
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- WM_DWMNCRENDERINGCHANGED 訊息桌面視窗管理員
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934458"
---
# <a name="wm_dwmncrenderingchanged-message"></a>WM \_ DWMNCRENDERINGCHANGED 訊息

當非工作區轉譯原則變更時傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定是否針對視窗的非工作區啟用 DWM 轉譯。 如果已啟用，則 **為 TRUE** ;否則 **為 FALSE**。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

[**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute)和 [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute)函數可用來取得或設定非用戶端轉譯原則。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



 

