---
title: size_is 屬性
description: 使用 \ size \_ 為 \ 屬性來指定記憶體的大小、元素中配置給大小指標的指標、調整大小指標大小的指標，以及單一或多維度陣列。
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is 屬性 MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681769"
---
# <a name="size_is-attribute"></a>大小 \_ 為屬性

使用 \[ **size \_ 為** \] attribute 來指定記憶體大小、元素中配置給調整大小指標的指標、調整大小指標大小的指標，以及單一或多維度陣列。

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a>參數

<dl> <dt>

*有限運算式清單* 
</dt> <dd>

指定一或多個 C 語言運算式。 每個運算式都會評估為非負整數，代表配置給大小指標或陣列的記憶體數量。 如果是陣列，則會指定單一運算式，代表該陣列第一個維度的配置大小（以元素為單位）。 MIDL 編譯器支援條件運算式、邏輯運算式、關聯式運算式和算術運算式。 MIDL 不允許運算式中的函式呼叫，也不允許遞增和遞減運算子。 使用逗號作為隱含參數的預留位置，或分隔多個運算式。

</dd> </dl>

## <a name="remarks"></a>備註

如果您使用 [ \[ **大小 \_ 為**] \] 屬性來配置多維度陣列的記憶體，而且您正在使用陣列 \[ \] 標記法，請記住，只有多維陣列的第一個維度可在執行時間以動態方式判斷。 其他維度必須以靜態方式指定。 如需使用 \[ **大小 \_ 為** \] 具有多個指標層級之屬性的詳細資訊，讓伺服器能夠將動態大小的資料陣列傳回給用戶端（如範例 Proc7 所示），請參閱 [多層級的指標](/windows/desktop/Rpc/multiple-levels-of-pointers)。

您可以使用 [ \[ **大小 \_** ] \] 或 [**[ \_ 最大值**](max-is.md)] (，但不能同時使用相同的屬性清單) 來指定在執行時間決定其上限的陣列大小。 但是請注意， \[ **size \_ 是** \] attribute 無法用於固定的陣列維度。 \[ **Max \_ 是** \] 屬性指定最大有效陣列索引。 因此，指定 \[ size \_ 是 (n) \] 相當於指定 \[ max \_ (n-1) \] 。

\[ [**In**](in.md) \] 或 \[ in、 [**out**](out-idl.md) \] 符合標準的陣列參數（包含 \[ [**字串**](string.md) \] 屬性）不需要 \[ **大小 \_ 為** \] attribute 或 \[ [**max \_**](max-is.md) \] 。 在此情況下，配置的大小取決於輸入字串的 Null 結束字元。 具有字串屬性的所有其他符合標準的陣列都 \[ \] 必須是屬性的 \[ **大小 \_** \] 或 \[ **最大 \_** 值 \] 。

雖然使用 \[ **size \_ 是** 具有常數的屬性是合法的 \] ，但這麼做並不具效率。 例如，使用固定大小陣列：

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

而非：

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

您可以使用 [ \[ **大小 \_** ] \] 和 [長度] \[ [**\_ 都是**](length-is.md) \] 屬性。 當您這樣做時，[ \[ **大小] 屬性 \_ 會** 控制配置給 \] 資料的記憶體數量。 [ \[ **長度] \_ 是**[ \] 屬性] 指定要傳輸的元素數目。 大小所指定的記憶體數量 \[ **\_ 是** \] ，而且 \[ **長度 \_ 是** \] 屬性不需要相同的。 比方說，您的用戶端可能會將 \[ in、out \] 參數傳遞至伺服器，並指定大小為的大型記憶體配置 \[ **\_** \] ，即使它指定要以長度傳遞的少量資料元素 \[ **\_ 也是** 一樣 \] 。 這可讓伺服器在陣列中填入超過其所接收的資料，然後再傳回給用戶端。

一般情況下，同時指定 \[ **size \_** \] 和 \[ [**length \_**](length-is.md)在 \] \[ in \] 或 \[ out \] 參數中並不實用。 在這兩種情況下， \[ **大小 \_ 都會** \] 控制記憶體配置。 您的應用程式可以使用 \[ **大小 \_ ，** \] 因為配置的陣列元素比 (的 \[) **長度 \_ 所** 指定的更多 \] 。 不過，這樣做會沒有效率。 為大小指定相同的值 \[ **\_** \] ，且 \[ **長度 \_ 為**，也會沒有效率 \] 。 它會在參數封送處理期間產生額外的負荷。 如果 size 的值 \[ **\_ 為** \] 且 \[ **length \_** \] 永遠相同，請省略 \[ **length \_ 為** \] attribute。

## <a name="examples"></a>範例

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[欄位屬性](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**第一個 \_ 是**](first-is.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**在**](in.md)
</dt> <dt>

[**last \_**](last-is.md)
</dt> <dt>

[**長度 \_ 為**](length-is.md)
</dt> <dt>

[**最大值 \_ 為**](max-is.md)
</dt> <dt>

[**最小值 \_ 為**](min-is.md)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**字串**](string.md)
</dt> </dl>

 

 