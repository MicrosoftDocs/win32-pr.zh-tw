---
description: 訂閱者的名字。
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: IEventSubscription2SubscriberMoniker 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: cdd783a4e3f8d29d3ffc4ae279602db71c3ee16247ad58c6f23aa10bb3ba5350
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070668"
---
# <a name="ieventsubscription2subscribermoniker-property"></a>IEventSubscription2：： SubscriberMoniker 屬性

訂閱者的名字。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a>屬性值

指定訂閱者的標記字串。

## <a name="error-codes"></a>錯誤碼

這個方法可以傳回標準傳回值 E \_ INVALIDARG、e \_ OUTOFMEMORY、e 非 \_ 預期、e \_ 失敗和 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




