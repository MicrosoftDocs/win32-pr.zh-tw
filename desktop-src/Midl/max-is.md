---
title: max_is 屬性
description: '\ Max \_ 是 \ 屬性，會指定有效陣列索引的最大值。'
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is 屬性 MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dfa7e8cdc5b1df752a3a6eb442524157228d354079f262a27a5514860e335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642964"
---
# <a name="max_is-attribute"></a>max \_ 為 attribute

**\[ Max \_ 為 attribute \] 會** 指定有效陣列索引的最大值。

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a>參數

<dl> <dt>

*有限運算式清單* 
</dt> <dd>

指定一或多個 C 語言運算式。 每個運算式都會評估為表示最高有效陣列索引的整數。 MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。 MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。 以逗號分隔多個運算式。

</dd> </dl>

## <a name="remarks"></a>備註

Max of 屬性不一定會對應到陣列中的元素數目。 **\[ \_ \]** 若為 C 中大小為 *n* 的陣列，其中第一個陣列元素為元素編號零，則有效陣列索引的最大值為 *n*–1。

當 **\[ \_ \]** **\[** [**size \_ 為**](size-is.md)attribute 時，max as 屬性不能同時當做 field 屬性使用 **\]** 。

雖然使用 **\[ max \_ 是 \]** 具有常數運算式的屬性是合法的，但這麼做並不具效率。 例如，使用固定大小陣列：

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

而非：

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a>範例

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[欄位屬性](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**最小值 \_ 為**](min-is.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
</dt> </dl>

 

 