---
title: defaultbind 屬性
description: '\ Defaultbind \ 屬性工作表示最能代表物件的單一、可系結屬性。'
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- defaultbind 屬性 MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a981d0469219a32b5931507f5df6d742e84fa67e6676e44c24edfb823f521a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807294"
---
# <a name="defaultbind-attribute"></a>defaultbind 屬性

**\[ Defaultbind \]** 屬性工作表示最能代表物件的單一、可系結屬性。

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

指定套用至整個介面的一或多個屬性清單。 當有兩個或多個介面屬性存在時，它們必須以逗號分隔。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。

</dd> <dt>

*屬性清單* 
</dt> <dd>

指定套用至函數的一或多個屬性清單。 當有兩個或多個介面屬性存在時，它們必須以逗號分隔。

</dd> <dt>

*returntype* 
</dt> <dd>

指定函式的傳回型別。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定將套用 **\[ defaultbind \]** 屬性的函數名稱。

</dd> <dt>

*params* 
</dt> <dd>

函數參數清單。

</dd> </dl>

## <a name="remarks"></a>備註

具有 **\[ defaultbind \]** 屬性的屬性也必須具有可系結 **\[** [](bindable.md) **\]** 屬性。 介面或分配介面中只有一個屬性可以有 **\[ defaultbind \]** 屬性。

如果容器具有與物件系結的使用者模型，而不是系結至物件的屬性，則會使用這個屬性。 物件可以支援資料系結，但不能有這個屬性。

### <a name="flags"></a>Flags

FUNCFLAG \_ FDEFAULTBIND、VARFLAG \_ FDEFAULTBIND

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 