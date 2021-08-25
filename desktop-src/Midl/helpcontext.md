---
title: helpcontext 屬性
description: '\ HelpcoNtext \ 屬性會指定內容識別碼，讓使用者可在說明檔中查看這個元素的相關資訊。'
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- helpcoNtext 屬性 MIDL
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3caa5dd32257fb5d75bbf77cde4ae5e71c6e97574cd1c263ead47aacedccadc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895248"
---
# <a name="helpcontext-attribute"></a>helpcontext 屬性

\[ **HelpcoNtext** \] 屬性會指定內容識別碼，讓使用者可在說明檔中查看此元素的相關資訊。

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*uuid-數位* 
</dt> <dd>

指定連結 [**庫**](library.md)、 \[ [**importlib**](importlib.md) \] 、[**介面**](interface.md)、介面 [**介面**](dispinterface.md)、[**模組**](module.md)、 [**typedef**](typedef.md)、**方法**、 **\[ \] 屬性** 或 [**coclass**](coclass.md)的通用唯一識別碼。

</dd> <dt>

*helpcoNtext-值* 
</dt> <dd>

唯一的整數，識別與目前 MIDL 元素相關聯的解說文字。

</dd> <dt>

*屬性清單* 
</dt> <dd>

指定一或多個套用至 MIDL 元素整體的屬性清單。

</dd> <dt>

*元素* 
</dt> <dd>

下列其中一個指示詞： [**library**](library.md)、 \[ [**importlib**](importlib.md) \] 、 [**interface**](interface.md)、 [****](dispinterface.md)、 [**module、module**](module.md)、 [**typedef**](typedef.md)、 **method**、 **property** 或 [**coclass**](coclass.md)。

</dd> <dt>

*元素名稱* 
</dt> <dd>

其他軟體元件可用來描繪目前元素的名稱。

</dd> <dt>

*定義* 
</dt> <dd>

指定組成元素定義的語句。

</dd> </dl>

## <a name="remarks"></a>備註

\[ **HelpcoNtext** \] 屬性可以套用至下列元素： [**library**](library.md)、 \[ [**importlib**](importlib.md) \] 、 [**interface、interface**](interface.md) [**、**](dispinterface.md) [**module**](module.md)、 [**typedef**](typedef.md)、 **method**、 **property** 或 [**coclass**](coclass.md)。

*HelpcoNtext-值* 是說明檔內的32位內容識別碼，可使用 [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib)和 [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo)介面中的 [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation)函式進行抓取。

## <a name="examples"></a>範例

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[**圖書館**](library.md)
</dt> <dt>

[**模組**](module.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 