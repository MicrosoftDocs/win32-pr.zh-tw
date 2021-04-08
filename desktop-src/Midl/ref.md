---
title: ref 屬性
description: '\ Ref \ 屬性會識別參考指標。 它只會用來表示間接取值層級。'
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- ref 屬性 MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842155"
---
# <a name="ref-attribute"></a>ref 屬性

**\[ Ref \]** 屬性會識別參考指標。 它只會用來表示間接取值層級。

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至類型的一或多個屬性。 有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[ \] ref**、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[** [**字串**](string.md)和 **\]** **\[** [**忽略**](ignore.md) **\]** 。 以逗號分隔多個屬性。

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

指定套用至結構、聯集成員或函數參數的零或多個欄位屬性。 有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length \_**](length-is.md) **\]** 、max、 **\[** [**max \_**](max-is.md) **\]** 、 **\[** [**size、 \_**](size-is.md) **\]** usage 屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**ignore**](ignore.md) **\]** 和 **\[** [**coNtext \_ 控制碼**](context-handle.md) **\]** ; 指標屬性 **\[ ref \]**、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及 union 屬性 **\[** [**參數 \_ 類型**](switch-type.md) **\]** 。 以逗號分隔多個欄位屬性。

</dd> <dt>

*函數-屬性清單* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local**](local.md)、 **\]** 指標屬性 **\[ ref \]**、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**忽略**](ignore.md) **\]** 和 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 。

</dd> <dt>

*ptr-decl* 
</dt> <dd>

指定至少一個要套用 **\[ ref \]** 屬性的指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*參數屬性清單* 
</dt> <dd>

包含零或多個適用于指定之參數類型的屬性。 參數屬性可將方向性屬性 **\[** 移 [**入**](in.md) **\]** 和 **\[** [**移出**](out-idl.md) **\]** ; 欄位屬性 **\[** [**first \_ 是**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**length \_**](length-is.md)、 **\]** **\[** [**max、 \_**](max-is.md) **\]** size、 **\[** [**size \_**](size-is.md) **\]** 、以及 **\[** [**switch \_ type**](switch-type.md)、 **\]** 指標屬性 **\[ ref \]**、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及 usage 屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 和 **\[** [**字串**](string.md) **\]** 。 Usage 屬性 **\[** [**ignore**](ignore.md) **\]** 不能用來做為參數屬性。 以逗號分隔多個屬性。

</dd> </dl>

## <a name="remarks"></a>備註

指標屬性可以套用為型別屬性（attribute），做為套用至結構成員、等位成員或參數的欄位屬性。或作為套用至函式傳回型別的函式屬性。 指標屬性也可以與 **\[** [**指標 \_ default**](pointer-default.md)關鍵字一起出現 **\]** 。

參考指標具有下列特性：

-   一律指向有效的儲存體;絕不會有 **Null** 值。 參考指標一律可以取值。
-   在呼叫期間永遠不會變更。 參考指標一律會指向用戶端上和呼叫之後的相同儲存體。
-   不會在用戶端上配置新的記憶體。 從伺服器傳回的資料會寫入至呼叫之前，由參考指標的值所指定的現有儲存體。
-   不會造成別名。 參考指標所指向的儲存體無法從函式中的任何其他名稱到達。

參考指標不能當做函式所傳回指標的類型使用。

如果未指定最上層指標參數的屬性，則會將它視為參考指標。

## <a name="examples"></a>範例

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
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

[**擴展**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
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

 

 