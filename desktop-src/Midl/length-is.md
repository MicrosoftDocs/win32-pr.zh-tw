---
title: length_is 屬性
description: '\ Length \_ 是 \ 屬性，可指定要傳送的陣列元素數目。 您必須指定非負數值。'
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is 屬性 MIDL
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463108"
---
# <a name="length_is-attribute"></a>長度 \_ 為屬性

[ **\[ 長度 \_ ] \] 是**[屬性] 指定要傳送的陣列元素數目。 您必須指定非負數值。

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a>參數

<dl> <dt>

*有限運算式清單* 
</dt> <dd>

指定一或多個 C 語言運算式。 每個運算式都會評估為整數，表示要傳送的陣列元素數目。 MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。 MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。 以逗號分隔多個運算式。

</dd> </dl>

## <a name="remarks"></a>備註

[ **\[ 長度 \_ ] \] 是**[屬性]，會決定 **\[** [**\_**](last-is.md) **\]** 當未指定 **\[ \_ \] last** 時，對應到 last 的陣列索引值是屬性。 這些陣列索引之間的關聯性如下： length = last-first + 1。

**\[ Length \_ 是 \]** attribute 無法與 **\[** [**最後一個 \_ 是**](last-is.md) **\]** 屬性或 **\[** [**字串**](string.md) **\]** 屬性同時使用。

若要定義 **\[ 長度 \_ 為 \]** 或 last 的計數位符串為 **\[** [**\_**](last-is.md) **\]** 屬性，請使用不含 **\[** [**字串**](string.md)屬性的字元陣列或指標 **\]** 。

使用 **\[ 長度 \_ 為 \]** attribute 的常數運算式是不適當的屬性使用方式。 它是合法的，但效率不佳，而且會導致較慢的封送處理常式代碼。

您可以使用 [ **\[** [**大小 \_**](size-is.md) ] **\]** 和 [長度] **\[ \_ 都 \] 是** 屬性。 當您這樣做時，[大小] 屬性 **\[ \_ 會 \]** 控制配置給資料的記憶體數量。 [ **\[ 長度 \_ ] \] 是**[屬性] 指定要傳輸的元素數目。 大小所指定的記憶體數量 **\[ \_ 是 \]** ，而且 **\[ 長度 \_ 是 \]** 屬性不需要相同的。 比方說，您的用戶端可能會將 **\[ in**、 **out \]** 參數傳遞至伺服器，並指定 **\[ 大小 \_ 為 \]** 的大型記憶體配置，即使它指定要以長度傳遞的少量資料元素 **\[ \_ 也是 \]** 一樣。 這可讓伺服器在陣列中填入超過其所接收的資料，然後再傳回給用戶端。

一般情況下，同時指定 **\[** [**size \_**](size-is.md) **\]** 和 **\[ length \_ \]** 在 **\[** [**in**](in.md) **\]** 或 **\[** [**out**](out-idl.md) **\]** 參數中並不實用。 在這兩種情況下， **\[ 大小 \_ 都會 \]** 控制記憶體配置。 您的應用程式可以使用 **\[ 大小 \_ ， \]** 因為配置的陣列元素比 (的) **\[ 長度 \_ 所 \]** 指定的更多。 不過，這樣做會沒有效率。 為 **\[ \_ 大小 \]** 指定相同的值，且 **\[ 長度 \_ 為 \]**，也會沒有效率。 因為它會在參數封送處理期間產生額外的負擔。 當 **\[ \_ size \]** 的值和 **\[ \_ length \]** 永遠相同時，請省略 **\[ length \_ \] 為** attribute。

## <a name="examples"></a>範例

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[欄位屬性](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**第一個 \_ 是**](first-is.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**last \_**](last-is.md)
</dt> <dt>

[**最大值 \_ 為**](max-is.md)
</dt> <dt>

[**最小值 \_ 為**](min-is.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
</dt> <dt>

[**字串**](string.md)
</dt> </dl>

 

 