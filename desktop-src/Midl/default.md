---
title: default 屬性
description: '\ Default \ 屬性工作表示在 coclass 內定義的介面或介面介面，代表預設的可程式性介面。 這個屬性是供宏語言使用。'
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- 預設屬性 MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463009"
---
# <a name="default-attribute"></a>default 屬性

**\[ 預設 \]** 屬性會指出在 [**coclass**](coclass.md)內定義的 [**介面**](interface.md)[**或介面介面，**](dispinterface.md)代表預設的可程式性介面。 這個屬性是供宏語言使用。

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*uuid-數位* 
</dt> <dd>

指定 [**coclass**](coclass.md)的通用唯一識別碼。

</dd> <dt>

*屬性清單* 
</dt> <dd>

指定其他 [**coclass**](coclass.md) 屬性。 以逗號分隔多個屬性。

</dd> <dt>

*coclass-名稱* 
</dt> <dd>

指定其他軟體元件可以參考此 [**coclass**](coclass.md)的名稱。

</dd> <dt>

*選用-interface 屬性* 
</dt> <dd>

**\[** [**Source**](source.md) **\]** 屬性（指定介面或分配介面為傳出）是唯一可在此處使用的其他屬性。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

[**Coclass**](coclass.md)最多隻能有兩個 **\[ 預設 \]** 成員。 其中一個代表外寄 (來源) 介面或分配介面，另一個則代表傳入的 (接收) 介面或多介面。 如果未針對 **coclass** 或 **cotype** 的任何成員指定 **\[ \] 預設** 屬性，則會將未受限制屬性的第一個傳出和傳入成員 **\[** [](restricted.md) **\]** 視為預設值。

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FDEFAULT

## <a name="examples"></a>範例

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**限制**](restricted.md)
</dt> <dt>

[**源**](source.md)
</dt> </dl>

 

 