---
description: 管理訂用帳戶的篩選準則。
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: IEventSubscription2：： >filtercriteria 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3d973066ef637882d3477cb9992d01afad72ae3bd314b1a413d628e5c561c007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070658"
---
# <a name="ieventsubscription2filtercriteria-property"></a>IEventSubscription2：： >filtercriteria 屬性

管理訂用帳戶的篩選準則。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a>屬性值

執行 [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter)之類別的篩選準則或 CLSID。

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

 

 




