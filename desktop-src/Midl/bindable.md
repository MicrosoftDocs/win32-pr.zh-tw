---
title: bindable 屬性
description: '\ 可系結 \ 屬性工作表示屬性支援資料系結。'
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- 可系結屬性 MIDL
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106995150"
---
# <a name="bindable-attribute"></a>bindable 屬性

可系結屬性工作表示屬性支援資料系結。 **\[ \]**

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

指定套用至整個介面的零或多個 IDL 屬性清單。 當有兩個或多個介面屬性存在時，它們必須以逗號分隔。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> <dt>

*屬性清單* 
</dt> <dd>

指定套用至屬性之函式原型的零或多個屬性，或是 [**介面**](interface.md) 或 [**介面介面中**](dispinterface.md)方法的屬性。 以下是有效的屬性： [**\[ helpstring \]**](helpstring.md)、 [**\[ helpcoNtext \]**](helpcontext.md)、 [**\[ string \]**](string.md)、 [**\[ defaultbind \]**](defaultbind.md)、 [**\[ displaybind \]**](displaybind.md)、 [**\[ immediatebind \]**](immediatebind.md)、 [**\[ propget \]**](propget.md)、 [**\[ propput \]**](propput.md)、 [**\[ propputref \]**](propputref.md)和 [**\[ vararg \]**](vararg.md)。 如果指定了 **vararg** ，則最後一個參數必須是 VARIANT 類型的安全陣列。 以逗號分隔多個屬性。

</dd> <dt>

*returntype* 
</dt> <dd>

指定函式的傳回型別。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定將套用可系結 **\[ \] 屬性之** 函式的名稱。

</dd> <dt>

*params* 
</dt> <dd>

函數參數清單。

</dd> </dl>

## <a name="remarks"></a>備註

藉由支援資料系結 **\[ \]** ，可系結屬性可讓用戶端在屬性變更值時收到通知。  (如果您希望用戶端收到屬性即將變更的通知，請使用 [**\[ requestedit \]**](requestedit.md)屬性。 ) 

因為可系結屬性會將屬性（property）視為整個屬性（property），所以必須在定義屬性的位置指定該屬性（property）。 **\[ \]** 因此，您必須同時在屬性存取函式和屬性設定函數上指定屬性。

### <a name="flags"></a>Flags

FUNCFLAG \_ FBINDABLE、VARFLAG \_ FBINDABLE

## <a name="examples"></a>範例

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**immediatebind**](immediatebind.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**requestedit**](requestedit.md)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**vararg**](vararg.md)
</dt> </dl>

 

 