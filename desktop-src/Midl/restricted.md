---
title: restricted 屬性
description: '\ 限制 \ 屬性指定無法任意呼叫模組、介面或分配介面的程式庫或成員。'
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- 受限制的屬性 MIDL
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375181"
---
# <a name="restricted-attribute"></a>restricted 屬性

**\[ 受限制 \]** 的屬性會指定無法任意呼叫程式庫或模組、介面或分配介面的成員。

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*其他屬性* 
</dt> <dd>

零或多個 MIDL 屬性。

</dd> <dt>

*語句類型* 
</dt> <dd>

下列其中一項：連結 [**庫**](library.md)、[**模組**](module.md)、[**介面、介面**](interface.md)介面。 [](dispinterface.md)

</dd> <dt>

*語句-名稱* 
</dt> <dd>

軟體用來參考這個語句的識別碼。

</dd> <dt>

*定義* 
</dt> <dd>

用來定義這個語句內容的 MIDL 語言元素。

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性可讓您控制對介面、程式庫、模組和分配介面之元素的存取。 例如，它可以防止宏程式設計人員使用資料項目。 您可以將此屬性套用至 [**coclass**](coclass.md)的成員，與成員是否為分配介面或介面無關，而不論成員是否為接收 (傳入) 或來源 (傳出) 。 **Coclass** 的成員不能同時有 **\[ 受 \] 限制** 的和 **\[ 預設 \]** 屬性。

### <a name="flags"></a>Flags

IMPLTYPEFLAG \_ FRESTRICTED、FUNCFLAG \_ FRESTRICTED

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**圖書館**](library.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**模組**](module.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 