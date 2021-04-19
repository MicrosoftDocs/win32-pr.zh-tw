---
title: helpstringcoNtext 屬性
description: '\ HelpstringcoNtext \ 屬性指定說明檔中的32位說明內容識別碼。 您可以將 \ helpstringcoNtext \ 屬性套用至程式庫、介面、介面介面、模組、coclass、typedef 語句、屬性、參數和方法。'
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- helpstringcoNtext 屬性 MIDL
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966425"
---
# <a name="helpstringcontext-attribute"></a>helpstringcoNtext 屬性

**\[ HelpstringcoNtext \]** 屬性會指定說明檔中的32位說明內容識別碼。 您可以將 **\[ \] helpstringcoNtext** 屬性套用至連結 [**庫**](library.md)、[**介面**](interface.md)、介面 [**介面**](dispinterface.md)、[**模組**](module.md)、 [**coclass**](coclass.md)、 [**typedef**](typedef.md)語句、屬性、參數和方法。

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a>參數

<dl> <dt>

*coNtextid* 
</dt> <dd>

唯一的整數，識別與目前 MIDL 語句相關聯的解說文字。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

零或多個 MIDL 屬性。

</dd> <dt>

*idl 語句* 
</dt> <dd>

將套用 **\[ helpstringcoNtext \]** 屬性的 MIDL 語句。

</dd> </dl>

## <a name="remarks"></a>備註

使用 **ITypeLib2** 和 **ITypeInfo2** 介面中的 **GetDocumentation2** 函式來取出說明字串。

## <a name="examples"></a>範例

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




