---
title: string 屬性
description: '\ 字串 \ 屬性工作表示一維 char、wchar \_ t、byte (或對等的) 陣列，或對這類陣列的指標必須視為字串。'
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- 字串屬性 MIDL
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1537fe258315f379bbc7bee3284f5dcb06cdd140f2b85ac34f00e9ee4f77ec5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119382978"
---
# <a name="string-attribute"></a>string 屬性

**\[ 字串 \]** 屬性工作表示一維 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**byte**](byte.md) (或對等的) 陣列，或是這類陣列的指標必須視為字串。 字串也可以是陣列 (或陣列的指標) ，其欄位全都是 **byte** 類型的結構。

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至類型的一或多個屬性。 有效的型別屬性包括 **\[** [**控制碼**](handle.md) **\]** 、 **\[** [**切換 \_ 類型**](switch-type.md) **\]** 、 **\[** [**傳輸 \_ 為**](transmit-as.md) **\]** ; 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 、 **\[ 字串 \]** 和 **\[** [**略**](ignore.md)過 **\]** 。 以逗號分隔多個屬性。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底類型](midl-base-types.md)、 [**結構**](struct.md) 類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*標準-宣告子* 
</dt> <dd>

指定標準 C 宣告子，例如識別碼、指標宣告子或陣列宣告子。 如需詳細 [**資訊，請**](arrays-1.md)參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)、陣列和 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。

</dd> <dt>

*宣告子清單* 
</dt> <dd>

指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 如需詳細 [**資訊，請**](arrays-1.md)參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)、陣列和 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。 宣告子 *清單* 包含一或多個以逗號分隔的宣告子。 函式宣告子中的參數名稱識別碼是選擇性的。

</dd> <dt>

*欄位屬性清單* 
</dt> <dd>

指定套用至結構、聯集成員或函數參數的零或多個欄位屬性。 這兩個有效的欄位屬性是 **\[** [**最大 \_**](max-is.md)值， **\]** 且 **\[** [**大小 \_ 為**](size-is.md) **\]** ; 使用方式屬性 **\[ 字串 \]**、 **\[ 忽略 \]** 和 **\[ 內容 \_ 控制碼 \]**、指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[ unique \]** 或 **\[** [**ptr**](ptr.md) **\]** ，以及 union 屬性 **\[ 參數 \_ 類型 \]**。 以逗號分隔多個欄位屬性。

</dd> <dt>

*函數-屬性清單* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local、**](local.md) **\]** 指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**; 以及使用方式屬性 **\[ 字串 \]**、 **\[ 忽略 \]** 和 **\[ 內容 \_ 控制碼 \]**。

</dd> <dt>

*ptr-decl* 
</dt> <dd>

指定套用 **\[ 字串 \]** 屬性的選擇性指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同：它是由指示項 \* 、最 **遠** 的修飾詞和限定詞 [**const**](const.md)所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*參數屬性清單* 
</dt> <dd>

包含零或多個適用于指定之參數類型的屬性。 參數屬性可以取得和 **\[ 輸出 \]** 方向 **\[ 性 \] 屬性;** 欄位屬性 **\[** [**最大值 \_**](max-is.md)為 **\]** ，而 **\[** [**大小 \_ 為**](size-is.md) **\]** ; 指標屬性 **\[ ref \]**、 **\[ unique \]** 或 **\[ ptr \]**; 以及使用屬性 **\[ 內容 \_ 句 \] 柄** 和 **\[ 字串 \]**。 Usage 屬性 **\[ ignore \]** 不能用來做為參數屬性。 以逗號分隔多個屬性。

</dd> </dl>

## <a name="remarks"></a>備註

如果 **\[ \] 字串** 屬性搭配在執行時間決定界限的陣列使用，則您也必須指定 [ **\[ \_ \]** **\[ \_ \]** 大小] 或 [最大值] 屬性，如下列範例所示：

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

**\[ 字串 \]** 屬性不能與指定傳輸專案範圍的屬性搭配使用，例如 **\[ \_ \]** **\[ first \_ 是 \]**、last 和 **\[ length \_ \]**。

在多維陣列上使用時， **\[ 字串 \]** 屬性會套用至最右邊的陣列。

若要定義計數位符串，請勿使用 **\[ 字串 \]** 屬性。 使用字元陣列或以字元為基礎的指標，如下所示：

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

**\[ 字串 \]** 屬性會指定存根應使用語言提供的方法來判斷字串的長度。

在 C 中宣告字串時，您必須配置空間給標記字串結尾的額外字元。

## <a name="examples"></a>範例

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**回撥**](callback.md)
</dt> <dt>

[**char**](char-idl.md)
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

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**大小 \_ 為**](size-is.md)
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
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 