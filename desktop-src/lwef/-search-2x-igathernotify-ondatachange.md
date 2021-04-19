---
title: IGatherNotify OnDataChange (已淘汰的) 方法
description: 此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search ISearchPersistentItemsChangedSink API 取代。 |IGatherNotify OnDataChange (已淘汰的) 方法
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- OnDataChange (淘汰的) 方法舊版 Windows 環境功能
- OnDataChange (淘汰的) 方法舊版 Windows 環境功能，IGatherNotify 介面
- IGatherNotify 介面舊版 Windows 環境功能，OnDataChange (已淘汰的) 方法
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988557"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>IGatherNotify：： OnDataChange (已淘汰的) 方法

\[**OnDataChange** 可能會在作業系統或產品的後續版本中變更或無法使用。\]

此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API 取代。

這個方法會通知索引子已變更的資料。 當它將通知傳送至索引子時，它會包含變更類型、實體位址和邏輯位址。

## <a name="syntax"></a>語法


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*eChangeAdvise* \[在\]
</dt> <dd>

類型： **long**

指定變更類型的列舉值。

</dd> <dt>

*bstrPhysicalAddress* \[在\]
</dt> <dd>

類型： **BSTR**

變更之專案的實體位址。

</dd> <dt>

*bstrLogicalAddress* \[在\]
</dt> <dd>

類型： **BSTR**

變更之專案的邏輯位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

 

 
