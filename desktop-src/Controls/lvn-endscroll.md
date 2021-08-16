---
title: 'LVN_ENDSCROLL 訊息 (Commctrl .h) '
description: 當滾動操作結束時，通知清單視圖控制項的父視窗。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- LVN_ENDSCROLL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d0abc3c12170dbc14f5e8a67329ed226610baa7b00fd042a24ed67193e6df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915138"
---
# <a name="lvn_endscroll-message"></a>LVN \_ ENDSCROLL 訊息

當滾動操作結束時，通知清單視圖控制項的父視窗。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll)結構的指標，其中包含捲軸操作結束位置的水準或垂直位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





