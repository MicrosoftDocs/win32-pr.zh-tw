---
title: 'LVN_ODCACHEHINT (Commctrl 的通知碼) '
description: 由虛擬清單-view 控制項在其顯示區域的內容變更時傳送。
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- LVN_ODCACHEHINT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3693291eeaef0879bdf861f392b89a1d0f2d5ec52f8a9c0d092b5495eb4565a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170175"
---
# <a name="lvn_odcachehint-notification-code"></a>LVN \_ ODCACHEHINT 通知碼

由虛擬清單-view 控制項在其顯示區域的內容變更時傳送。 例如，當使用者滾動控制項的顯示時，清單視圖控制項會傳送此通知碼。 LVN \_ ODCACHEHINT 通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint)結構的指標，其中包含要快取之專案範圍的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

接收此通知碼的應用程式必須傳回零。

## <a name="remarks"></a>備註

處理此訊息可讓應用程式更新保留在快取中的專案資訊，以便在傳送 [LVN \_ GETDISPINFO](lvn-getdispinfo.md) 通知碼時立即可供使用。

請注意，此通知碼不一定是 [LVN \_ GETDISPINFO](lvn-getdispinfo.md)所要求之專案的確切表示。 因此，如果在處理 LVN GETDISPINFO 時未快取要求的專案 \_ ，應用程式必須準備好從快取外部的來源提供要求的資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





