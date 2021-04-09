---
title: const 屬性
description: Const 關鍵字會修改型別宣告的型別或函式參數的型別，以防止值改變。
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- const 屬性 MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2980f0f484c838e4f972bbf12fb72173edb3e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681774"
---
# <a name="const-attribute"></a>const 屬性

**Const** 關鍵字會修改型別宣告的型別或函式參數的型別，以防止值改變。

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a>參數

<dl> <dt>

*const 類型* 
</dt> <dd>

指定有效的 MIDL 整數、字元、字串或布林值類型。 有效的 MIDL 類型 [**包括 small**](small.md)、 [**short**](short.md)、 [**long**](long.md)、 [**char**](char-idl.md)、 **\* charÂ**、 [**wchar \_ t**](wchar-t.md)、 **wchar \_ tÂ \***、 [**byte**](byte.md)、 **byteÂ \*** 和 [**voidÂ \***](void.md)。 可以 [**簽署**](signed.md) 或不帶 [**正負**](unsigned.md)號的整數和字元類型。

</dd> <dt>

*identifier* 
</dt> <dd>

指定有效的 MIDL 識別碼。 有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。

</dd> <dt>

*const 運算式* 
</dt> <dd>

指定適用于指定類型的運算式、識別碼或數值或字元常數：整數常數的常數整數常值或常數整數運算式;可以在編譯時計算 [**布林值**](boolean.md)類型的布林運算式;[**char**](char-idl.md)類型的單一字元常數;**\[**[**字串**](string.md)類型的字串常數 **\]** 。 [**VoidÂ \***](void.md)類型只能初始化為 **Null**。

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至類型的一或多個屬性。

</dd> <dt>

*指標類型* 
</dt> <dd>

指定有效的 MIDL 指標類型。

</dd> <dt>

*宣告子和宣告子清單* 
</dt> <dd>

指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。 如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。 宣告子清單包含一或多個宣告子， *並* 以逗號分隔。 函式宣告子中的參數名稱識別碼是選擇性的。

</dd> <dt>

*函數-attr-list* 
</dt> <dd>

指定套用至函數的零或多個屬性。 有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local**](local.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**忽略**](ignore.md) **\]** 和 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 。

</dd> <dt>

*類型規範* 
</dt> <dd>

指定 [基底 \_ 類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。 選擇性的儲存規格可以在 *類型* 規範之前。

</dd> <dt>

*ptr-decl* 
</dt> <dd>

指定零個或多個指標宣告子。 指標宣告子與 C 中使用的指標宣告子相同。它是由指示項 **\*** 、最 **遠** 的修飾詞和限定詞 **const** 所構成。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定遠端程式的名稱。

</dd> <dt>

*參數屬性清單* 
</dt> <dd>

指定適用于指定之參數類型的零或多個方向屬性、欄位屬性、使用方式屬性和指標屬性。 以逗號分隔多個屬性。

</dd> </dl>

## <a name="remarks"></a>備註

MIDL 可讓您在 IDL 檔案的介面主體中宣告常數整數、字元、字串和布林類型。 **常數** 類型宣告會在產生的標頭檔中重現為 **\# 定義** 指示詞。

DCE IDL 編譯器不支援常數運算式。 因此，當您使用 MIDL 編譯器 [**/osf**](-osf.md) 參數時，就無法使用這項功能。

先前定義的常數可以當做後續常數的指派值使用。 常數整數運算式的值會根據 C 轉換規則自動轉換成個別的整數類型。

字元常數的值必須是以單引號括住的 ASCII 字元。 當字元常數是單引號字元本身 ( ' ) 時，反斜線字元 (\) 必須在單引號字元之前，如 \\ '。

字元字串常數的值必須是以雙引號括住的字串。 在字串中，反斜線 (**\\**) 字元前面必須加上常值雙引號字元 ( **"** ) ，如下所 **\\ 示**。 在字串中，反斜線字元 (**\\**) 代表一個 escape 字元。 字串常數最多可包含255個字元。

**Null** 值是 [**voidÂ \***](void.md)類型常數的唯一有效值。 任何與 **const** 宣告相關聯的屬性都會被忽略。

MIDL 編譯器不會檢查 **常數** 初始化中的範圍錯誤。 例如，當您指定 "const short x = 0xFFFFFFFF;" 時，MIDL 編譯器不會報告錯誤，而且會在產生的標頭檔中重現初始化運算式。

## <a name="examples"></a>範例

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**位元組**](byte.md)
</dt> <dt>

[**回撥**](callback.md)
</dt> <dt>

[**字元**](char-idl.md)
</dt> <dt>

[**內容 \_ 控制碼**](context-handle.md)
</dt> <dt>

[**枚舉**](enum.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**忽略**](ignore.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**signed**](signed.md)
</dt> <dt>

[**小**](small.md)
</dt> <dt>

[**字串**](string.md)
</dt> <dt>

[**結構**](struct.md)
</dt> <dt>

[**聯盟**](union.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> <dt>

[**void**](void.md)
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 