---
title: source 屬性
description: '\ Source \ 屬性工作表示 coclass、屬性或方法的成員是事件來源。 對於 coclass 的成員而言，這個屬性工作表示會呼叫該成員，而不是實作為成員。'
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- source 屬性 MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933114"
---
# <a name="source-attribute"></a>source 屬性

**\[ Source \]** 屬性工作表示 [**coclass**](coclass.md)、屬性或方法的成員是事件來源。 對於 **coclass** 的成員而言，這個屬性工作表示會呼叫該成員，而不是實作為成員。

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>參數

<dl> <dt>

*coclass-屬性* 
</dt> <dd>

將套用至 [**coclass**](coclass.md)的零或多個屬性。

</dd> <dt>

*coclass-名稱* 
</dt> <dd>

[**Coclass**](coclass.md)的名稱識別碼。

</dd> <dt>

*選用-屬性* 
</dt> <dd>

零或多個 MIDL 屬性。

</dd> <dt>

*語句類型* 
</dt> <dd>

可以是 [**介面或介面介面**](interface.md)。 [](dispinterface.md)

</dd> <dt>

*語句-名稱* 
</dt> <dd>

介面 [**或分配**](dispinterface.md)[**介面**](interface.md)的名稱。

</dd> <dt>

*物件類型* 
</dt> <dd>

方法傳回的物件類型。 此物件是事件的來源。

</dd> <dt>

*函數名稱* 
</dt> <dd>

[**介面**](interface.md)[**或分配介面中**](dispinterface.md)方法的名稱。

</dd> <dt>

*選擇性-參數-清單* 
</dt> <dd>

零或多個方法參數。

</dd> </dl>

## <a name="remarks"></a>備註

在屬性或方法上， **\[ source \]** 屬性會指出成員會傳回屬於事件來源的物件或變異數。 物件會執行 **IConnectionPointContainer**。

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FSOURCE、VARFLAG \_ 來源、FUNCFLAG \_ 來源

## <a name="examples"></a>範例

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 