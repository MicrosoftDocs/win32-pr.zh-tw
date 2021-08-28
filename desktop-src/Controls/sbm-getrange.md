---
title: 'SBM_GETRANGE 訊息 (Winuser .h) '
description: 傳送 SBM \_ GETRANGE 訊息，以抓取捲軸控制項的最小和最大位置值。
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- SBM_GETRANGE 訊息 Windows 控制項
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
ms.openlocfilehash: 8e66c6e7bf79c270d66fdeac0ece1a1ce82ed813d1638be3587be7237ecd30e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770038"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



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

 

