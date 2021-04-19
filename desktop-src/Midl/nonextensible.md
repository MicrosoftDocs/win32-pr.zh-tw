---
title: nonextensible 屬性
description: '\ Nonextensible \ 屬性指定 IDispatch 的實作為只包含介面描述中所列的屬性和方法，而且無法在執行時間以其他成員擴充。'
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- nonextensible 屬性 MIDL
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965837"
---
# <a name="nonextensible-attribute"></a>nonextensible 屬性

**\[ Nonextensible \]** 屬性會指定 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)執行只包含介面描述中所列出的屬性和方法，而且在執行時間無法以其他成員擴充。  (根據預設，自動化會假設介面可能會在執行時間加入成員;也就是說，它會假設它們是可擴充的。 ) 

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*uuid-數位* 
</dt> <dd>

指定 [**介面**](interface.md)的通用唯一識別碼。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

指定零個或更多 MIDL 介面屬性的清單。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定 [**介面**](interface.md)[**或分配介面的**](dispinterface.md)名稱。

</dd> <dt>

*介面定義* 
</dt> <dd>

指定組成介面 [**或分配**](dispinterface.md)[**介面**](interface.md)定義的 IDL 語句。

</dd> </dl>

## <a name="remarks"></a>備註

您可以將 **\[ nonextensible \]** 屬性套用至介面或介面介面。 不過，介面也必須有 **\[** [**雙重**](dual.md) **\]** 屬性和 **\[** [**oleautomation**](oleautomation.md) **\]** 屬性。

### <a name="flags"></a>Flags

TYPEFLAG \_ FNONEXTENSIBLE

## <a name="examples"></a>範例

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[型別程式庫的內容](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[**雙**](dual.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 