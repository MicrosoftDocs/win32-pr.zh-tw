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
# <a name="const-attribute"></a><span data-ttu-id="f5482-104">const 屬性</span><span class="sxs-lookup"><span data-stu-id="f5482-104">const attribute</span></span>

<span data-ttu-id="f5482-105">**Const** 關鍵字會修改型別宣告的型別或函式參數的型別，以防止值改變。</span><span class="sxs-lookup"><span data-stu-id="f5482-105">The **const** keyword modifies the type of a type declaration or the type of a function parameter, preventing the value from varying.</span></span>

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a><span data-ttu-id="f5482-106">參數</span><span class="sxs-lookup"><span data-stu-id="f5482-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5482-107">*const 類型*</span><span class="sxs-lookup"><span data-stu-id="f5482-107">*const-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-108">指定有效的 MIDL 整數、字元、字串或布林值類型。</span><span class="sxs-lookup"><span data-stu-id="f5482-108">Specifies a valid MIDL integer, character, string, or Boolean type.</span></span> <span data-ttu-id="f5482-109">有效的 MIDL 類型 [**包括 small**](small.md)、 [**short**](short.md)、 [**long**](long.md)、 [**char**](char-idl.md)、 **\* charÂ**、 [**wchar \_ t**](wchar-t.md)、 **wchar \_ tÂ \***、 [**byte**](byte.md)、 **byteÂ \*** 和 [**voidÂ \***](void.md)。</span><span class="sxs-lookup"><span data-stu-id="f5482-109">Valid MIDL types include [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), **charÂ \***, [**wchar\_t**](wchar-t.md), **wchar\_tÂ \***, [**byte**](byte.md), **byteÂ \***, and [**voidÂ \***](void.md).</span></span> <span data-ttu-id="f5482-110">可以 [**簽署**](signed.md) 或不帶 [**正負**](unsigned.md)號的整數和字元類型。</span><span class="sxs-lookup"><span data-stu-id="f5482-110">The integer and character types can be [**signed**](signed.md) or [**unsigned**](unsigned.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5482-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="f5482-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-112">指定有效的 MIDL 識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5482-112">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="f5482-113">有效的 MIDL 識別碼最多包含31個英數位元和/或底線字元，而且開頭必須是字母或底線字元。</span><span class="sxs-lookup"><span data-stu-id="f5482-113">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="f5482-114">*const 運算式*</span><span class="sxs-lookup"><span data-stu-id="f5482-114">*const-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-115">指定適用于指定類型的運算式、識別碼或數值或字元常數：整數常數的常數整數常值或常數整數運算式;可以在編譯時計算 [**布林值**](boolean.md)類型的布林運算式;[**char**](char-idl.md)類型的單一字元常數;**\[**[**字串**](string.md)類型的字串常數 **\]** 。</span><span class="sxs-lookup"><span data-stu-id="f5482-115">Specifies an expression, identifier, or numeric or character constant appropriate for the specified type: constant integer literals or constant integer expressions for integer constants; Boolean expressions that can be computed at compilation for [**Boolean**](boolean.md) types; single-character constants for [**char**](char-idl.md) types; and string constants for **\[**[**string**](string.md)**\]** types.</span></span> <span data-ttu-id="f5482-116">[**VoidÂ \***](void.md)類型只能初始化為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f5482-116">The [**voidÂ \***](void.md) type can be initialized only to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f5482-117">*type-attribute-list*</span><span class="sxs-lookup"><span data-stu-id="f5482-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-118">指定套用至類型的一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="f5482-118">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="f5482-119">*指標類型*</span><span class="sxs-lookup"><span data-stu-id="f5482-119">*pointer-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-120">指定有效的 MIDL 指標類型。</span><span class="sxs-lookup"><span data-stu-id="f5482-120">Specifies a valid MIDL pointer type.</span></span>

</dd> <dt>

<span data-ttu-id="f5482-121">*宣告子和宣告子清單*</span><span class="sxs-lookup"><span data-stu-id="f5482-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-122">指定標準的 C 宣告子，例如識別碼、指標宣告子，以及陣列宣告子。</span><span class="sxs-lookup"><span data-stu-id="f5482-122">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="f5482-123">如需詳細資訊，請參閱 [陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md) [**、陣列、陣列和**](arrays-1.md)[指標](/windows/desktop/Rpc/arrays-and-pointers)。</span><span class="sxs-lookup"><span data-stu-id="f5482-123">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="f5482-124">宣告子清單包含一或多個宣告子， *並* 以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="f5482-124">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="f5482-125">函式宣告子中的參數名稱識別碼是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f5482-125">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="f5482-126">*函數-attr-list*</span><span class="sxs-lookup"><span data-stu-id="f5482-126">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-127">指定套用至函數的零或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="f5482-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="f5482-128">有效的函式屬性為 **\[** [**回呼**](callback.md) **\]** 、 **\[** [**local**](local.md)、 **\]** 指標屬性 **\[** [**ref**](ref.md) **\]** 、 **\[** [**unique**](unique.md) **\]** 或 **\[** [**ptr**](ptr.md) **\]** ; 以及使用方式屬性 **\[** [**字串**](string.md) **\]** 、 **\[** [**忽略**](ignore.md) **\]** 和 **\[** [**內容 \_ 控制碼**](context-handle.md) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="f5482-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="f5482-129">*類型規範*</span><span class="sxs-lookup"><span data-stu-id="f5482-129">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-130">指定 [基底 \_ 類型](midl-base-types.md)、[**結構**](struct.md)、[**等位、**](union.md)[**列舉**](enum.md)類型或類型識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5482-130">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="f5482-131">選擇性的儲存規格可以在 *類型* 規範之前。</span><span class="sxs-lookup"><span data-stu-id="f5482-131">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="f5482-132">*ptr-decl*</span><span class="sxs-lookup"><span data-stu-id="f5482-132">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-133">指定零個或多個指標宣告子。</span><span class="sxs-lookup"><span data-stu-id="f5482-133">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="f5482-134">指標宣告子與 C 中使用的指標宣告子相同。它是由指示項 **\*** 、最 **遠** 的修飾詞和限定詞 **const** 所構成。</span><span class="sxs-lookup"><span data-stu-id="f5482-134">A pointer declarator is the same as the pointer declarator used in C. It is constructed from the **\*** designator, modifiers such as **far**, and the qualifier **const**.</span></span>

</dd> <dt>

<span data-ttu-id="f5482-135">*函數名稱*</span><span class="sxs-lookup"><span data-stu-id="f5482-135">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-136">指定遠端程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5482-136">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f5482-137">*參數屬性清單*</span><span class="sxs-lookup"><span data-stu-id="f5482-137">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f5482-138">指定適用于指定之參數類型的零或多個方向屬性、欄位屬性、使用方式屬性和指標屬性。</span><span class="sxs-lookup"><span data-stu-id="f5482-138">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="f5482-139">以逗號分隔多個屬性。</span><span class="sxs-lookup"><span data-stu-id="f5482-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5482-140">備註</span><span class="sxs-lookup"><span data-stu-id="f5482-140">Remarks</span></span>

<span data-ttu-id="f5482-141">MIDL 可讓您在 IDL 檔案的介面主體中宣告常數整數、字元、字串和布林類型。</span><span class="sxs-lookup"><span data-stu-id="f5482-141">MIDL allows you to declare constant integer, character, string, and Boolean types in the interface body of the IDL file.</span></span> <span data-ttu-id="f5482-142">**常數** 類型宣告會在產生的標頭檔中重現為 **\# 定義** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="f5482-142">**Const** type declarations are reproduced in the generated header file as **\#define** directives.</span></span>

<span data-ttu-id="f5482-143">DCE IDL 編譯器不支援常數運算式。</span><span class="sxs-lookup"><span data-stu-id="f5482-143">DCE IDL compilers do not support constant expressions.</span></span> <span data-ttu-id="f5482-144">因此，當您使用 MIDL 編譯器 [**/osf**](-osf.md) 參數時，就無法使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="f5482-144">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="f5482-145">先前定義的常數可以當做後續常數的指派值使用。</span><span class="sxs-lookup"><span data-stu-id="f5482-145">A previously defined constant can be used as the assigned value of a subsequent constant.</span></span> <span data-ttu-id="f5482-146">常數整數運算式的值會根據 C 轉換規則自動轉換成個別的整數類型。</span><span class="sxs-lookup"><span data-stu-id="f5482-146">The value of a constant integral expression is automatically converted to the respective integer type in accordance with C conversion rules.</span></span>

<span data-ttu-id="f5482-147">字元常數的值必須是以單引號括住的 ASCII 字元。</span><span class="sxs-lookup"><span data-stu-id="f5482-147">The value of a character constant must be a single-quoted ASCII character.</span></span> <span data-ttu-id="f5482-148">當字元常數是單引號字元本身 ( ' ) 時，反斜線字元 (\) 必須在單引號字元之前，如 \\ '。</span><span class="sxs-lookup"><span data-stu-id="f5482-148">When the character constant is the single-quote character itself ('), the backslash character (\) must precede the single-quote character, as in \\'.</span></span>

<span data-ttu-id="f5482-149">字元字串常數的值必須是以雙引號括住的字串。</span><span class="sxs-lookup"><span data-stu-id="f5482-149">The value of a character-string constant must be a double-quoted string.</span></span> <span data-ttu-id="f5482-150">在字串中，反斜線 (**\\**) 字元前面必須加上常值雙引號字元 ( **"** ) ，如下所 **\\ 示**。</span><span class="sxs-lookup"><span data-stu-id="f5482-150">Within a string, the backslash (**\\**) character must precede a literal double-quote character ( **"** ), as in **\\"**.</span></span> <span data-ttu-id="f5482-151">在字串中，反斜線字元 (**\\**) 代表一個 escape 字元。</span><span class="sxs-lookup"><span data-stu-id="f5482-151">Within a string, the backslash character (**\\**) represents an escape character.</span></span> <span data-ttu-id="f5482-152">字串常數最多可包含255個字元。</span><span class="sxs-lookup"><span data-stu-id="f5482-152">String constants can consist of up to 255 characters.</span></span>

<span data-ttu-id="f5482-153">**Null** 值是 [**voidÂ \***](void.md)類型常數的唯一有效值。</span><span class="sxs-lookup"><span data-stu-id="f5482-153">The value **NULL** is the only valid value for constants of type [**voidÂ \***](void.md).</span></span> <span data-ttu-id="f5482-154">任何與 **const** 宣告相關聯的屬性都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f5482-154">Any attributes associated with the **const** declaration are ignored.</span></span>

<span data-ttu-id="f5482-155">MIDL 編譯器不會檢查 **常數** 初始化中的範圍錯誤。</span><span class="sxs-lookup"><span data-stu-id="f5482-155">The MIDL compiler does not check for range errors in **const** initialization.</span></span> <span data-ttu-id="f5482-156">例如，當您指定 "const short x = 0xFFFFFFFF;" 時，MIDL 編譯器不會報告錯誤，而且會在產生的標頭檔中重現初始化運算式。</span><span class="sxs-lookup"><span data-stu-id="f5482-156">For example, when you specify "const short x = 0xFFFFFFFF;" the MIDL compiler does not report an error and the initializer is reproduced in the generated header file.</span></span>

## <a name="examples"></a><span data-ttu-id="f5482-157">範例</span><span class="sxs-lookup"><span data-stu-id="f5482-157">Examples</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f5482-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5482-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5482-159">**陣 列**</span><span class="sxs-lookup"><span data-stu-id="f5482-159">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="f5482-160">MIDL 基底類型</span><span class="sxs-lookup"><span data-stu-id="f5482-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="f5482-161">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f5482-161">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="f5482-162">**位元組**</span><span class="sxs-lookup"><span data-stu-id="f5482-162">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="f5482-163">**回撥**</span><span class="sxs-lookup"><span data-stu-id="f5482-163">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="f5482-164">**字元**</span><span class="sxs-lookup"><span data-stu-id="f5482-164">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="f5482-165">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="f5482-165">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="f5482-166">**枚舉**</span><span class="sxs-lookup"><span data-stu-id="f5482-166">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="f5482-167"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="f5482-167">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="f5482-168">**忽略**</span><span class="sxs-lookup"><span data-stu-id="f5482-168">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="f5482-169">**當地**</span><span class="sxs-lookup"><span data-stu-id="f5482-169">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="f5482-170">**long**</span><span class="sxs-lookup"><span data-stu-id="f5482-170">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="f5482-171">**/osf**</span><span class="sxs-lookup"><span data-stu-id="f5482-171">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="f5482-172">**ptr**</span><span class="sxs-lookup"><span data-stu-id="f5482-172">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="f5482-173">**ref**</span><span class="sxs-lookup"><span data-stu-id="f5482-173">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="f5482-174">**short**</span><span class="sxs-lookup"><span data-stu-id="f5482-174">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="f5482-175">**signed**</span><span class="sxs-lookup"><span data-stu-id="f5482-175">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="f5482-176">**小**</span><span class="sxs-lookup"><span data-stu-id="f5482-176">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="f5482-177">**字串**</span><span class="sxs-lookup"><span data-stu-id="f5482-177">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="f5482-178">**結構**</span><span class="sxs-lookup"><span data-stu-id="f5482-178">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="f5482-179">**聯盟**</span><span class="sxs-lookup"><span data-stu-id="f5482-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="f5482-180">**獨特**</span><span class="sxs-lookup"><span data-stu-id="f5482-180">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="f5482-181">**符號**</span><span class="sxs-lookup"><span data-stu-id="f5482-181">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="f5482-182">**void**</span><span class="sxs-lookup"><span data-stu-id="f5482-182">**void**</span></span>](void.md)
</dt> <dt>

[<span data-ttu-id="f5482-183">**wchar \_ t**</span><span class="sxs-lookup"><span data-stu-id="f5482-183">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 