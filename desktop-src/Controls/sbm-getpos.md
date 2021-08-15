---
title: 'SBM_GETPOS 訊息 (Winuser .h) '
description: 傳送 SBM \_ GETPOS 訊息，以抓取捲軸控制項捲動方塊的目前位置。
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- SBM_GETPOS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0105b2c015614c9f064b2c97f60100c2240bd6588612d34b25546c7ced832bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408891"
---
# <a name="sbm_getpos-message"></a>SBM \_ GETPOS 訊息

傳送 **SBM \_ GETPOS** 訊息，以抓取捲軸控制項捲動方塊的目前位置。 目前的位置是相依于目前滾動範圍的相對值。 例如，如果滾動的範圍是0到100，而且捲動方塊位於橫條的中間，則目前的位置是50。

應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **GetScrollPos** 函數才能正常運作。

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

傳回值是捲軸中捲動方塊的目前位置。

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

[**SBM \_ GETRANGE**](sbm-getrange.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SETRANGE**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

