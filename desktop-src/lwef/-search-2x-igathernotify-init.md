---
title: IGatherNotify Init (已淘汰的) 方法
description: 此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search ISearchPersistentItemsChangedSink API 取代。 |IGatherNotify Init (已淘汰的) 方法
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Init (淘汰的) 方法舊版 Windows 環境功能
- Init (淘汰的) 方法舊版 Windows 環境功能，IGatherNotify 介面
- IGatherNotify 介面舊版 Windows 環境功能、Init (已淘汰) 方法
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db5666197524afb454927036cdd68375dfb2937197ed211646b63d80a09e5b12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359298"
---
# <a name="igathernotifyinit-deprecated-method"></a>IGatherNotify：： Init (已淘汰的) 方法

\[**Init** 可能會在作業系統或產品的後續版本中變更或無法使用。\]

此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API 取代。

初始化收集介面。 也會指定要通知的索引，以及要監視的應用程式存放區。

## <a name="syntax"></a>語法


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrApplication* \[在\]
</dt> <dd>

類型： **BSTR**

指定目標應用程式的字串。

</dd> <dt>

*bstrProject* \[在\]
</dt> <dd>

類型： **BSTR**

字串，指定要傳遞收集程式資訊的索引子名稱。

</dd> <dt>

*varScopesBstrArray* \[在\]
</dt> <dd>

類型： **variant**

選擇性參數，可讓您傳遞要初始化的範圍陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

使用 application = "RSApp"，Project = "MyIndex" 初始化。

 

 
