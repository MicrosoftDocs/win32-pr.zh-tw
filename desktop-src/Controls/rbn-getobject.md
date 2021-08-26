---
title: 'RBN_GETOBJECT (Commctrl 的通知碼) '
description: '\_當物件拖曳至控制項中的範圍時，以 RBS REGISTERDROP 樣式建立的 Rebar 控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。'
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- RBN_GETOBJECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9709313a16d068e44b847f5e0862adf1e133b9f0ea92136a12e9aae24ffb14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985038"
---
# <a name="rbn_getobject-notification-code"></a>RBN \_ GETOBJECT 通知碼

當物件拖曳至控制項中的範圍時，以 [**RBS \_ REGISTERDROP**](rebar-control-styles.md) 樣式建立的 Rebar 控制項所傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的指標，其中包含將物件拖曳到其中的頻外相關資訊，同時也會接收接收應用程式提供的資料，以回應此通知碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

此通知碼的傳回值必須為零。

## <a name="remarks"></a>備註

若要接收 RBN 的 \_ GETOBJECT 通知碼，請呼叫 [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) 或 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize)來初始化 OLE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

