---
title: last_is 屬性
description: Field 屬性 \ last \_ 是 \ 指定要傳送之最後一個陣列元素的索引。 當指定的索引為零或負數時，不會傳送任何陣列元素。
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- last_is 屬性 MIDL
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507907"
---
# <a name="last_is-attribute"></a>last \_ 是屬性

Field 屬性 **\[ last \_ 是 \]** 指定要傳送之最後一個陣列元素的索引。 當指定的索引為零或負數時，不會傳送任何陣列元素。

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a>參數

<dl> <dt>

*有限運算式清單* 
</dt> <dd>

指定一或多個 C 語言運算式。 每個運算式都會評估為整數，表示要傳送之最後一個陣列元素的陣列索引。 MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。 MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。 以逗號分隔多個運算式。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 最後一個 \_ 屬性 \] 會** 決定 **\[** [**\_**](length-is.md) **\]** 當未指定 **\[ 長度 \_ \]** 時，對應至長度的陣列索引值為屬性。 這些陣列索引之間的關聯性如下： length = last-first + 1。

如果第一個指定的陣列索引值大於 **\[** [**\_**](first-is.md) **\]** **\[ \_ \] last** 所指定的值，則會傳送零個元素。

**\[ 最後一個 \_ 是 \]** 屬性，因為 **\[** [**長度 \_ 是**](length-is.md) **\]** 屬性或 **\[** [**字串**](string.md)屬性，所以不能同時做為欄位屬性使用 **\]** 。

使用具有 last 的常數運算式 **\[ \_ 是 \]** 屬性，就不適合使用屬性。 它是合法的，但效率不佳，而且會導致較慢的封送處理常式代碼。

當 max 指定的值 **\[** [**\_**](max-is.md) **\]** 等於或大於零時，下列關聯性必須成立： 0 <= last \_ <= max \_ 是。

## <a name="examples"></a>範例

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[欄位屬性](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**第一個 \_ 是**](first-is.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**長度 \_ 為**](length-is.md)
</dt> <dt>

[**最大值 \_ 為**](max-is.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
</dt> </dl>

 

 