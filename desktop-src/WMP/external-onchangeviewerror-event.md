---
title: OnChangeViewError 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |OnChangeViewError 事件
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- External. OnChangeViewError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa1152c753501b2e2385de8c56af614d62cfb367fcca8468aaa032e9536e8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648828"
---
# <a name="externalonchangeviewerror-event"></a>OnChangeViewError 事件

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

當 [changeView](external-changeview.md)方法的呼叫產生錯誤時，就會發生 **OnChangeViewError** 事件。

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a>可能的值

這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。

## <a name="parameters"></a>參數

處理此事件的函式具有下列參數。

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*人力資源*
</dt> <dd>

**HRESULT** 失敗代碼，指出失敗的原因。

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

在 **changeView** 的 **LibraryLocationType** 參數中傳遞的相同字串。

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

在 **changeView** 的 **LibraryLocationID** 參數中傳遞的相同字串 thatwas。

</dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*濾波器*
</dt> <dd>

在 **changeView** 的 **篩選** 參數中傳遞的相同字串。

</dd> <dt>

<span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*
</dt> <dd>

在 **changeView** 的 **ViewParams** 參數中傳遞的相同字串。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的 ExternalObject**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





