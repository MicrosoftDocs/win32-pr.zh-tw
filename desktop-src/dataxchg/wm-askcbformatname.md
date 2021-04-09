---
title: 'WM_ASKCBFORMATNAME 訊息 (Winuser .h) '
description: 由剪貼簿檢視器視窗傳送給剪貼簿擁有者，以要求 CF \_ OWNERDISPLAY 剪貼簿格式的名稱。
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME 訊息資料交換
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094200"
---
# <a name="wm_askcbformatname-message"></a>WM \_ ASKCBFORMATNAME 訊息

由剪貼簿檢視器視窗傳送給剪貼簿擁有者，以要求 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 剪貼簿格式的名稱。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*LParam* 參數所指向之緩衝區的大小（以字元為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>

要接收剪貼簿格式名稱之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

為了回應這則訊息，剪貼簿擁有者應該將擁有者顯示格式的名稱複製到指定的緩衝區，而不超過 *wParam* 參數所指定的緩衝區大小。

[剪貼簿檢視器] 視窗會將此訊息傳送給剪貼簿擁有者，以判斷 [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) 格式的名稱，例如，用來初始化功能表清單的可用格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[剪貼簿總覽](clipboard.md)
</dt> </dl>

 

