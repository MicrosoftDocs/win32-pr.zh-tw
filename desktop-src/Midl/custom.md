---
title: Custom Attribute - 自訂屬性
description: '\ Custom \ 屬性會建立使用者定義的屬性。'
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- 自訂屬性 MIDL
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968691"
---
# <a name="custom-attribute"></a>Custom Attribute - 自訂屬性

**\[ 自訂 \]** 屬性會建立使用者定義的屬性。

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a>參數

<dl> <dt>

*屬性識別碼* 
</dt> <dd>

自訂屬性的 GUID。

</dd> <dt>

*屬性-值* 
</dt> <dd>

屬性保存的值。 值必須是可以放入 VARIANT 型別的一個值。

</dd> <dt>

*屬性清單* 
</dt> <dd>

適用于此元素的其他屬性，例如 **\[** [**uuid**](uuid.md) **\]** 和 **\[** [**helpstring**](helpstring.md) **\]** 。

</dd> <dt>

*元素類型* 
</dt> <dd>

要套用自訂屬性的元素類型。 這可以是程式庫語句、類型資訊、變數、函數或參數。 您無法在 coclass 的成員上使用自訂屬性。

</dd> <dt>

*元素名稱* 
</dt> <dd>

元素的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

使用 **\[ 自訂 \]** 屬性來定義您自己的屬性。 例如，您可以建立字串值屬性，以提供類別的 ProgID。

若要取出自訂屬性值，請呼叫下列其中一項：

-   ITypeLib2：： GetCustData (rguid，pvarVal) 
-   ITypeInfo2：： GetCustData (rguid，pvarVal) 
-   ITypeInfo2：： GetFuncCustData (index、rguid、pvarVal) 
-   ITypeInfo2：： GetVarCustData (index、rguid、pvarval) 
-   ITypeInfo2：： GetParamCustData (indexFunc、indexParam、rguid、pvarVal) 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**圖書館**](library.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 