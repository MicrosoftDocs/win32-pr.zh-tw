---
title: first_is 屬性
description: '\ First \_ 是 \ 屬性，它會指定要傳送之第一個陣列元素的索引。'
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is 屬性 MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842291"
---
# <a name="first_is-attribute"></a>first \_ 是屬性

\[**第一個 \_ 是屬性，它會** \] 指定要傳送之第一個陣列元素的索引。

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a>參數

<dl> <dt>

*有限運算式清單* 
</dt> <dd>

指定一或多個 C 語言運算式。 每個運算式都會評估為整數，表示要傳送之第一個陣列元素的陣列索引。 MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。 MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。 以逗號分隔多個運算式。

</dd> </dl>

## <a name="remarks"></a>備註

如果 **\[ 第一個 \_ 是 \]** 屬性不存在，或指定的索引為負數，則陣列元素零會是第一個傳送的元素。

**\[ 第 \_ 一個 \]** 屬性也可以協助判斷對應到最後一個的陣列索引值， **\[** [**\_**](last-is.md) **\]** 或 **\[** 當未指定這些屬性時，[**它的長度 \_ 是**](length-is.md) **\]** 屬性。 這些陣列索引之間的關聯性為：

``` syntax
length = last - first + 1
```

下列關聯性也必須保留：

``` syntax
0 <= first_is <= max_is
```

當 **\[** [**max \_ 為**](max-is.md)**\] <= 0** 時，下列關聯性必須保持：

``` syntax
first_is == 0
```

**\[ 第一個 \_ 是 \]** 屬性，不能與 **\[** [**字串**](string.md) **\]** 屬性同時使用。

使用具有 **\[ 第一個 \_ \]** 的常數運算式是屬性，就不適合使用屬性。 它是合法的，但效率不佳，而且會導致較慢的封送處理常式代碼。

## <a name="examples"></a>範例

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[欄位 \_ 屬性](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**last \_**](last-is.md)
</dt> <dt>

[**長度 \_ 為**](length-is.md)
</dt> <dt>

[**最大值 \_ 為**](max-is.md)
</dt> <dt>

[**最小值 \_ 為**](min-is.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
</dt> <dt>

[**字串**](string.md)
</dt> </dl>

 

 