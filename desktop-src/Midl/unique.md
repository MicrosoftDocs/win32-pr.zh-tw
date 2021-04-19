---
title: unique 屬性
description: '\ Unique \ 屬性指定唯一指標。'
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- unique 屬性 MIDL
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106994961"
---
# <a name="unique-attribute"></a>unique 屬性

**\[ Unique \]** 屬性指定唯一指標。

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至類型的一或多個屬性。 有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[ unique \]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[** [**字串**](string.md) **\]** 和 **\[** [**略**](ignore.md)過 **\]** 。 以逗號分隔多個屬性。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*宣告子和宣告子清單* 
</dt> <dd>

指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 如需詳細 [**資訊，請**](arrays-1.md)參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)、陣列和 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。 宣告子 *清單* 包含一或多個以逗號分隔的宣告子。 函式宣告子中的參數名稱識別碼是選擇性的。

</dd> <dt>

*struct 或 union-宣告子* 
</dt> <dd>

指定 MIDL [**結構**](struct.md)[**或等**](union.md)位宣告子。

</dd> <dt>

*欄位屬性清單* 
</dt> <dd>

指定套用至結構成員、聯集成員或函數參數的零或多個欄位屬性。 有效的欄位屬性包括 **\[** [**first \_**](first-is.md) **\]** 、 **\[** [**last \_**](last-is.md) **\]** 、 **\[** [**\_ length**](length-is.md) **\]** 、max、 **\[** [**max \_**](max-is.md) **\]** 、 **\[** [**size、 \_**](size-is.md) **\]** usage 屬性 **\[ 字串 \]**、 **\[ ignore \]** 和 **\[ coNtext \_ 控制碼 \]**; 指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**; 以及 union 屬性 **\[ 參數 \_ 類型 \]**。 以逗號分隔多個欄位屬性。

</dd> <dt>

*函數-屬性清單* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local、**](local.md) **\]** 指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**; 以及使用方式屬性 **\[ 字串 \]**、 **\[ 忽略 \]** 和 **\[ 內容 \_ 控制碼 \]**。

</dd> <dt>

*ptr-decl* 
</dt> <dd>

指定至少一個要套用 **\[ 唯一 \]** 屬性的指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*參數屬性清單* 
</dt> <dd>

包含零或多個適用于指定之參數類型的屬性。 參數屬性可將方向性屬性移 **\[ 入 \]** 和 **\[ 移 \] 出**; [](ptr.md) **\[ \]** **\[ \] 欄位屬性**  **\[ first \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ 是 \] 、** last、length、 **\[ max、 \_ size、size、以及 switch type、指標屬性 ref、unique 或 ptr; 以及 usage 屬性內容控制碼和字串。 \]** **\[ \_ \]** **\[ \_ \]** Usage 屬性 **\[ ignore \]** 不能用來做為參數屬性。 以逗號分隔多個屬性。

</dd> </dl>

## <a name="remarks"></a>備註

指標屬性可以套用為類型屬性;作為套用至結構成員、等位成員或參數的欄位屬性;或作為套用至函式傳回型別的函式屬性。 指標屬性也可以與 **\[** [**指標 \_ default**](pointer-default.md)關鍵字一起出現 **\]** 。

唯一指標具有下列特性：

-   的值可以是 **Null**。
-   從 **Null** 呼叫到非 **null**、從非 null 到 **null**，或從一個非 **null** **值到另** 一個非 null 值時，可能會變更。
-   可以在用戶端上配置新的記憶體。 當唯一指標從 **Null** 變更為非 **Null** 時，從伺服器傳回的資料會寫入至新的儲存體。
-   可以在用戶端上使用現有的記憶體，而不需要配置新的記憶體。 當唯一指標在從一個非 **Null** 值呼叫期間變更為另一個時，會假設指標指向相同型別的資料物件。 從伺服器傳回的資料會寫入至在呼叫之前，由 unique 指標的值所指定的現有儲存體。
-   可以是用戶端上的孤立記憶體。 如果唯一指標在呼叫期間變更為 **Null** ，而且用戶端沒有其他方法可取值儲存體，則不會釋放非 **Null** 唯一指標所參考的記憶體。
-   不會造成別名。 就像參考指標所指向的儲存體一樣，無法從函式中的任何其他名稱連接到由唯一指標所指向的儲存體。

存根會呼叫使用者提供的記憶體管理函式 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Rpc/the-midl-user-allocate-function) 和 [**midl 使用者可 \_ \_ 自由**](/windows/desktop/Rpc/the-midl-user-free-function) 配置和解除配置唯一指標與其參考的所需記憶體。

下列限制適用于唯一的指標：

-   **\[ Unique \]** 屬性無法套用至系結控制碼參數， ([**處理 \_ t**](handle-t.md)) 和內容控制碼參數。
-   **\[ 唯一 \]** 的屬性無法套用至僅 **\[** [](out-idl.md) **\]** 有 **\[ out \]** 方向屬性)  (參數的最上層指標參數。
-   依預設，參數清單中的最上層指標是 **\[** [**ref**](ref.md) **\]** 指標。 即使介面指定 **指標 \_ 預設 (唯一)**，也是如此。 參數清單中的 **\[ \]** 最上層參數必須指定為唯一的屬性，才能成為唯一的指標。
-   唯一指標不能用來描述陣列或聯集 arm 的大小，因為唯一指標的值可以是 **Null**。 這項限制可防止產生 **Null** 值做為陣列大小或聯集 arm 大小的錯誤。

## <a name="examples"></a>範例

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
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

[**處理 \_ t**](handle-t.md)
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

[midl \_ 使用者 \_ 配置](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[midl \_ 使用者 \_ 免費](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**擴展**](out-idl.md)
</dt> <dt>

[**指標 \_ 預設值**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
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
</dt> </dl>

 

 