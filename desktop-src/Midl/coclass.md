---
title: coclass 屬性
description: Coclass 語句會提供元件物件支援的介面清單。
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- coclass 屬性 MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375185"
---
# <a name="coclass-attribute"></a>coclass 屬性

**Coclass** 語句會提供元件物件支援的介面清單。

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*coclass-屬性清單* 
</dt> <dd>

**\[** [](uuid.md) **\]** **Coclass** 上需要有 uuid 屬性。 這是在系統註冊資料庫中註冊為 CLSID 的相同 **\[ uuid \]** 。 在 **\[** [](helpstring.md) **\]** **\[** [](helpcontext.md) **\]** coclass 定義之前，會接受 helpstring、helpcoNtext、 **\[** [**授權**](licensed.md) **\]** 、 **\[** [**version**](version.md) **\]** 、 **\[** [**control**](control.md) **\]** 、 **\[** [**hidden**](hidden.md) **\]** 和 **\[** [**appobject**](appobject.md) **\]** 屬性（但非必要 ）。

</dd> <dt>

*classname* 
</dt> <dd>

類型程式庫中已知通用物件的名稱。

</dd> <dt>

*介面屬性* 
</dt> <dd>

介面或分配介面的選擇性屬性。 在 **\[** [](source.md) **\]** **\[** [](default.md) **\]** coclass 中的介面或介面介面上接受來源、預設和 **\[** [**受限制**](restricted.md) **\]** 的屬性。

</dd> <dt>

*介面名稱* 
</dt> <dd>

使用 [**interface**](interface.md) 關鍵字宣告的介面，或以產生 [**介面關鍵字宣告**](dispinterface.md) 的介面介面。

</dd> </dl>

## <a name="remarks"></a>備註

Microsoft 元件物件模型會將類別定義為可讓一組介面之間進行 **QueryInterface** 的實作為。

## <a name="examples"></a>範例

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**appobject**](appobject.md)
</dt> <dt>

[**控制**](control.md)
</dt> <dt>

[**預設**](default.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**隱藏**](hidden.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[**licensed**](licensed.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**限制**](restricted.md)
</dt> <dt>

[**源**](source.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**uuid**](uuid.md)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 