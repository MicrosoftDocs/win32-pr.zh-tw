---
title: ptr 屬性
description: '\ Ptr \ 屬性會將指標指定為完整指標。'
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- ptr 屬性 MIDL
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314800"
---
# <a name="ptr-attribute"></a>ptr 屬性

**\[ Ptr \]** 屬性會將指標指定為完整指標。

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至類型的一或多個屬性。 有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md)或 **\[ \] ptr**; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[** [**字串**](string.md) **\]** 和 **\[** [**略**](ignore.md)過 **\]** 。 以逗號分隔多個屬性。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底類型](midl-base-types.md)、 [**結構**](struct.md)、 [**等**](union.md)位或 [**列舉**](enum.md) 類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*標準-宣告子* 
</dt> <dd>

指定標準 C 宣告子，例如識別碼、指標宣告子或陣列宣告子。 如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。

</dd> <dt>

*宣告子清單* 
</dt> <dd>

指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。 宣告子 *清單* 包含一或多個以逗號分隔的宣告子。 函式宣告子中的參數名稱識別碼是選擇性的。

</dd> <dt>

*欄位屬性清單* 
</dt> <dd>

指定套用至結構或等位成員或函數參數的零或多個欄位屬性。 有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length \_**](length-is.md) **\]** 、max、 **\[** [**max \_**](max-is.md) **\]** 、 **\[** [**size、 \_**](size-is.md) **\]** usage 屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**ignore**](ignore.md) **\]** 和 **\[** [**coNtext \_ 控制碼**](context-handle.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[ ptr \]**; 以及 union 屬性 **\[** [**參數 \_ 類型**](switch-type.md) **\]** 。 以逗號分隔多個欄位屬性。

</dd> <dt>

*函數-屬性清單* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local**](local.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[ ptr \]**; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**忽略**](ignore.md) **\]** 和 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 。

</dd> <dt>

*ptr-decl* 
</dt> <dd>

指定至少一個要套用 **\[ ptr \]** 屬性的指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*參數屬性清單* 
</dt> <dd>

包含零或多個適用于指定之參數類型的屬性。 參數 [**屬性可以採用和**](in.md)[**輸出**](out-idl.md)方向屬性;欄位屬性 [**first \_ 是**](first-is.md)、 [**last \_**](last-is.md)、length、 [**max \_**](length-is.md)、 [**max、 \_**](max-is.md)size、and [**switch \_ type**](switch-type.md)、指標屬性 [**ref**](ref.md)、 [**unique**](unique.md)或 **\[ ptr \]**; 以及 usage 屬性 [**內容 \_ 控制碼**](context-handle.md)和 [**字串**](string.md)。 [**\_**](size-is.md) Usage 屬性 [**ignore**](ignore.md) 不能用來做為參數屬性。 以逗號分隔多個屬性。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Ptr \]** 屬性指定的完整指標會使用 C 語言指標的完整功能。 完整指標的值可以是 **null** ，而且可以在呼叫期間從 **null** 變更為非 **Null**。 具有完整指標的儲存區可由應用程式中的其他名稱所指向，以支援別名和迴圈。 這項功能在遠端程序呼叫中需要更多的額外負荷來識別指標所參考的資料、判斷值是否為 **Null**，以及探索兩個指標是否指向相同的資料。

使用的完整指標：

-   遠端傳回值。
-   當輸出參數的大小未知時，即為雙指標。
-   **Null** 指標。

完整 (和唯一的) 指標不能用來描述陣列或等位的大小，因為這些指標可以有 **Null** 值。 MIDL 的這項限制可防止在將 **Null** 值當做大小使用時可能產生的錯誤。

參考和唯一指標會假設為沒有資料的別名。 從唯一或參考指標開始，而且只在下列情況下，只包含唯一或參考指標的導向圖形都不會包含 reconvergence 和迴圈。

為了避免別名，所有指標值都應該從相同指標類別的輸入指標取得。 如果有一個以上的指標指向相同的記憶體位置，則所有這類指標都必須是完整的指標。

在某些情況下，可以混合完整和唯一的指標。 只要指派不違反變更唯一指標值的限制，就可以將唯一指標的值指派給完整指標。 但是，當您將唯一指標指派為完整指標的值時，可能會導致別名。

混合完整和唯一指標可能會導致別名，如下列範例所示：

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

雖然 "t >left" 和 "t->right" 指向唯一的記憶體位置，但 "t->左 >.pdata" 和 "t >右 >.pdata" 都有別名。 基於這個理由，別名支援演算法必須遵循所有指標 (包括唯一和參考指標，) 最後可能會到達完整指標。

## <a name="examples"></a>範例

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**回撥**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[**第一個 \_ 是**](first-is.md)
</dt> <dt>

[**處理**](handle.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**忽略**](ignore.md)
</dt> <dt>

[**last \_**](last-is.md)
</dt> <dt>

[**長度 \_ 為**](length-is.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**最大值 \_ 為**](max-is.md)
</dt> <dt>

[**指標 \_ 預設值**](pointer-default.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[**結構**](struct.md)
</dt> <dt>

[**切換 \_ 類型**](switch-type.md)
</dt> <dt>

[**傳輸 \_ 為**](transmit-as.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 