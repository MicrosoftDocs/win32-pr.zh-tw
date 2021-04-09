---
title: helpstring 屬性
description: '\ Helpstring \ 屬性會指定用來描述所套用之元素的字元字串。'
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- helpstring 屬性 MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933128"
---
# <a name="helpstring-attribute"></a>helpstring 屬性

**\[ Helpstring \]** 屬性會指定用來描述所套用之元素的字元字串。 您可以將 **\[ helpstring \]** 屬性套用至程式庫、importlib、介面、介面介面、模組或 coclass 語句、typedef、屬性和方法。

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a>參數

<dl> <dt>

*說明-文字字串* 
</dt> <dd>

以零結束的字元字串，其中包含解說文字。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

零或多個 MIDL 屬性語句。

</dd> <dt>

*元素* 
</dt> <dd>

下列其中一個指示詞： [**library**](library.md)、 **\[** [**importlib**](importlib.md) **\]** 、 [**interface**](interface.md)、 [****](dispinterface.md)、 [**module、module**](module.md)、 [**typedef**](typedef.md)、 **method**、 **property** 或 [**coclass**](coclass.md)。

</dd> <dt>

*元素名稱* 
</dt> <dd>

其他軟體元件可用來描繪目前元素的名稱

</dd> <dt>

*definition* 
</dt> <dd>

指定組成元素定義的語句。

</dd> <dt>

*idl 語句* 
</dt> <dd>

MIDL 介面定義語句，例如 [**propget**](propget.md) 或 [**propput**](propput.md)。

</dd> </dl>

## <a name="remarks"></a>備註

使用 [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib)和 [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo)介面中的 [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation)函式來取出說明字串。

## <a name="examples"></a>範例

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**圖書館**](library.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**模組**](module.md)
</dt> <dt>

[**coclass**](coclass.md)
</dt> <dt>

[**著**](typedef.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 