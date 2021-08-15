---
title: iid_is 屬性
description: '\ Iid \_ 是 \ 指標屬性，可指定介面指標所指向之 COM 介面的 iid。'
ms.assetid: 7fb5eb87-15d8-4717-b79a-e8a81f2f7293
keywords:
- iid_is 屬性 MIDL
topic_type:
- apiref
api_name:
- iid_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74553fdb1e3020d49eca7dfdd219354a4690056c45126b3af208395117ade991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383865"
---
# <a name="iid_is-attribute"></a>iid \_ 為屬性

**\[ Iid \_ 是 \]** 指標屬性，可指定介面指標所指向之 COM 介面的 iid。

``` syntax
[ iid_is(limited-expression) ]
```

## <a name="parameters"></a>參數

<dl> <dt>

*有限運算式* 
</dt> <dd>

指定 C 語言運算式。 MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。 MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。

</dd> </dl>

## <a name="remarks"></a>備註

您可以在函數參數和結構或等位成員的屬性清單中使用 **\[ iid \_ \]** 。 存根使用 IID 來判斷如何封送處理介面指標。 這適用于類型為基類參數的介面指標。

使用 iid 的檔案 **\[ \_ 是 \]** 在預設模式下，使用 MIDL 編譯器來編譯的屬性，不是使用 [**/osf**](-osf.md)參數。

## <a name="examples"></a>範例

``` syntax
HRESULT    CreateInstance( 
    [in] REFIID riid, 
    [out, iid_is(riid)] IUnknown ** ppvObject);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**物件**](object.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 




