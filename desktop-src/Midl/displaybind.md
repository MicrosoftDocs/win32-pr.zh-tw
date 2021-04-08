---
title: displaybind 屬性
description: '\ Displaybind \ 屬性工作表示應該向使用者顯示為可系結的屬性。'
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- displaybind 屬性 MIDL
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681891"
---
# <a name="displaybind-attribute"></a>displaybind 屬性

**\[ Displaybind \]** 屬性工作表示應該向使用者顯示為可系結的屬性。

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

指定介面屬性的選擇性清單。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

介面的名稱。

</dd> <dt>

*屬性清單* 
</dt> <dd>

指定套用至函式傳回型別的一或多個屬性清單（以逗號分隔）。

</dd> <dt>

*returntype* 
</dt> <dd>

指定函式的傳回型別。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定將套用 **\[ displaybind \]** 屬性的函數名稱。

</dd> <dt>

*params* 
</dt> <dd>

函數參數清單。

</dd> </dl>

## <a name="remarks"></a>備註

具有 **\[ displaybind \]** 屬性的屬性也必須具有可系結 **\[** [](bindable.md) **\]** 屬性。 物件可以支援資料系結，但不能有這個屬性。

### <a name="flags"></a>Flags

FUNCFLAG \_ FDISPLAYBIND、VARFLAG \_ FDISPLAYBIND

## <a name="examples"></a>範例

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 