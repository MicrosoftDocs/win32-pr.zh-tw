---
title: IGatherNotify AddScope (已淘汰的) 方法
description: 此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search ISearchPersistentItemsChangedSink API 取代。 |IGatherNotify AddScope (已淘汰的) 方法
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- AddScope (淘汰的) 方法舊版 Windows 環境功能
- AddScope (淘汰的) 方法舊版 Windows 環境功能，IGatherNotify 介面
- IGatherNotify 介面舊版 Windows 環境功能，AddScope (已淘汰) 方法
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a49c0cf652b0cfde59167fa98498a978d3c2c41d3a886ee092b8f4a28d35f61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755589"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>IGatherNotify：： AddScope (已淘汰的) 方法

\[**AddScope** 可能會在作業系統或產品的後續版本中變更或無法使用。\]

此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API 取代。

新增您要監視的起始頁或 URL。 這會在您連接時起始增量編目，然後假設所有進一步的 URL 變更都是由通知所變更。

## <a name="syntax"></a>語法


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrScope* \[在\]
</dt> <dd>

類型： **BSTR**

字串，指定您要監視的起始頁或 URLthat。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當連接到存放區時，呼叫這個方法會啟動增量編目。 之後，假設所有的 URL 變更都是在初始更新之後的通知。

 

 
