---
title: id 屬性
description: '\ Id \ 屬性會指定成員函式的 DISPID (屬性或方法，在介面或) 的介面中。'
ms.assetid: 6f1be049-81b4-4aa2-a893-5dd79bb4d63c
keywords:
- id 屬性 MIDL
topic_type:
- apiref
api_name:
- id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4d783265ebfcf9dca454c80c39031dc0c37dfb63a8749b4d0e6299a510d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643064"
---
# <a name="id-attribute"></a>id 屬性

**\[ Id \]** 屬性會指定成員函式的 DISPID (屬性或方法，在介面或) 的介面中。

``` syntax
[id(id-num) [,optional-attribute-list]] return-type function-name(optional-parameter-list)
```

## <a name="parameters"></a>參數

<dl> <dt>

*識別碼-num* 
</dt> <dd>

函數的 DISPID。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

指定零個或更多 MIDL 介面屬性的清單。

</dd> <dt>

*傳回類型* 
</dt> <dd>

指定函式的傳回型別。

</dd> <dt>

*函數名稱* 
</dt> <dd>

在 IDL 檔案中指定函數的名稱。

</dd> <dt>

*選擇性-參數-清單* 
</dt> <dd>

零或多個函數參數。

</dd> </dl>

## <a name="remarks"></a>備註

當您想要指派標準 DISPID (例如 dispid **\[ \]** \_ 值、dispid \_ NEWENUM 等 ) 至方法或屬性，或當您執行您自己的 **IDispatch：： invoke** 而不是委派給 **DispInvoke** / **ITypeInfo：： invoke** 時，請使用 id 屬性。

如果您未在介面上使用 **\[ id \]** 屬性，MIDL 編譯器將為您指派 DISPID。 但是，當您使用屬性和方法來指定分配介面時，您必須針對每個屬性和方法指定 DISPID。

*識別碼-num* 是32位的正整數值。 負的識別碼是保留供 Automation 使用。

## <a name="examples"></a>範例

``` syntax
interface IKnown : IUnknown
{
    properties:
        [id(90), propget, 
         helpstring("A meaningful comment."] long Func1(void);

    /* Other interface statements */
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 