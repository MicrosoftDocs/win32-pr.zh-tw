---
title: OnChangeViewOnlineListError 事件
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |OnChangeViewOnlineListError 事件
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- External. OnChangeViewOnlineListError 事件 Windows Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ed6191de129bffea0e11abb24f1e271fc0b2873d2b306430a4e7eafe39b214d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648798"
---
# <a name="externalonchangeviewonlinelisterror-event"></a>OnChangeViewOnlineListError 事件

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

當 [changeViewOnlineList](external-changeviewonlinelist.md)方法的呼叫產生錯誤時，就會發生 **OnChangeViewOnlineListError** 事件。

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a>可能的值

這是唯讀屬性，它會指定腳本中的函式名稱，此函式會在事件發生時 Windows Media Player 呼叫。

## <a name="parameters"></a>參數

處理此錯誤的函式具有下列參數。

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*人力資源*
</dt> <dd>

**HRESULT** 失敗代碼，指出失敗的原因。

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

在 **changeViewOnlineList** 的 **LibraryLocationType** 參數中傳遞的相同字串。

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

在 **changeViewOnlineList** 的 **LibraryLocationID** 參數中傳遞的相同字串。

</dd> <dt>

<span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*
</dt> <dd>

在 **changeViewOnlineList** 的 **Params** 參數中傳遞的相同字串。

</dd> <dt>

<span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*友好*
</dt> <dd>

在 **changeViewOnlineList** 的 **FriendlyName** 參數中傳遞的相同字串。

</dd> <dt>

<span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*
</dt> <dd>

在 **changeViewOnlineList** 的 **ListType** 參數中傳遞的相同字串。

</dd> <dt>

<span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*
</dt> <dd>

在 **changeViewOnlineList** 的 **ViewMode** 參數中傳遞的相同字串。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





