---
title: pragma 屬性
description: '\ Pragma midl \_ echo 指示詞會指示 midl 將指定的字串（不含引號）發出至產生的標頭檔。'
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- pragma 屬性 MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932623"
---
# <a name="pragma-attribute"></a><span data-ttu-id="8330e-104">pragma 屬性</span><span class="sxs-lookup"><span data-stu-id="8330e-104">pragma attribute</span></span>

<span data-ttu-id="8330e-105">\# **Pragma midl \_ echo** 指示詞會指示 midl 將指定的字串（不含引號字元）發出至產生的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="8330e-105">The \#**pragma midl\_echo** directive instructs MIDL to emit the specified string, without the quotation characters, into the generated header file.</span></span>

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a><span data-ttu-id="8330e-106">參數</span><span class="sxs-lookup"><span data-stu-id="8330e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8330e-107">*string*</span><span class="sxs-lookup"><span data-stu-id="8330e-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="8330e-108">指定插入產生的標頭檔中的字串。</span><span class="sxs-lookup"><span data-stu-id="8330e-108">Specifies a string that is inserted into the generated header file.</span></span> <span data-ttu-id="8330e-109">插入過程中會移除引號。</span><span class="sxs-lookup"><span data-stu-id="8330e-109">The quotation marks are removed during the insertion process.</span></span>

</dd> <dt>

<span data-ttu-id="8330e-110">*權杖順序*</span><span class="sxs-lookup"><span data-stu-id="8330e-110">*token-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="8330e-111">指定在產生的標頭檔中插入為 **\# pragma** 指示詞一部分的權杖順序，而不是由 MIDL 編譯器處理。</span><span class="sxs-lookup"><span data-stu-id="8330e-111">Specifies a sequence of tokens that are inserted into the generated header file as part of a **\#pragma** directive without processing by the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="8330e-112">*n*</span><span class="sxs-lookup"><span data-stu-id="8330e-112">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="8330e-113">指定目前的套件大小。</span><span class="sxs-lookup"><span data-stu-id="8330e-113">Specifies the current pack size.</span></span> <span data-ttu-id="8330e-114">有效值為 1、2、4、8 和 16。</span><span class="sxs-lookup"><span data-stu-id="8330e-114">Valid values are 1, 2, 4, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="8330e-115">*id*</span><span class="sxs-lookup"><span data-stu-id="8330e-115">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="8330e-116">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="8330e-116">Specifies the user identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8330e-117">備註</span><span class="sxs-lookup"><span data-stu-id="8330e-117">Remarks</span></span>

<span data-ttu-id="8330e-118">出現在 IDL 檔案中的 c 語言前置處理指示詞是由 C 編譯器的預處理器所處理。</span><span class="sxs-lookup"><span data-stu-id="8330e-118">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="8330e-119">在 MIDL 編譯期間，可以使用 IDL 檔案中的 **\# 定義** 指示詞，但不能使用 C 編譯器。</span><span class="sxs-lookup"><span data-stu-id="8330e-119">The **\#define** directives in the IDL file are available during MIDL compilation, although not to the C compiler.</span></span>

<span data-ttu-id="8330e-120">例如，當預處理器遇到「定義 WINDOWS 4」指示詞時 \# ，預處理器會將 IDL 檔案中所有出現的 "WINDOWS" 取代為 "4"。</span><span class="sxs-lookup"><span data-stu-id="8330e-120">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="8330e-121">C 編譯時間不提供符號 "WINDOWS"。</span><span class="sxs-lookup"><span data-stu-id="8330e-121">The symbol "WINDOWS" is not available at C-compile time.</span></span>

<span data-ttu-id="8330e-122">若要允許 C 預處理器巨集定義傳遞 MIDL 編譯器至 C 編譯器，請使用 **\# pragma MIDL \_ echo** 或 [**cpp \_ 引號**](cpp-quote.md)指示詞。</span><span class="sxs-lookup"><span data-stu-id="8330e-122">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or [**cpp\_quote**](cpp-quote.md) directive.</span></span> <span data-ttu-id="8330e-123">這些指示詞會指示 MIDL 編譯器產生包含參數字串的標頭檔，並移除引號。</span><span class="sxs-lookup"><span data-stu-id="8330e-123">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="8330e-124">**\# Pragma midl \_ echo** 和 **cpp \_ 引號** 指示詞是相等的。</span><span class="sxs-lookup"><span data-stu-id="8330e-124">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="8330e-125">MIDL 編譯器會使用 **\# pragma pack** 指示詞來控制結構的封裝。</span><span class="sxs-lookup"><span data-stu-id="8330e-125">The **\#pragma pack** directive is used by the MIDL compiler to control the packing of structures.</span></span> <span data-ttu-id="8330e-126">它會覆寫 [**/Zp**](-zp.md) 命令列參數。</span><span class="sxs-lookup"><span data-stu-id="8330e-126">It overrides the [**/Zp**](-zp.md) command-line switch.</span></span> <span data-ttu-id="8330e-127">Pack (*n*) 選項會將目前的套件大小設定為特定的值：1、2、4、8或16。</span><span class="sxs-lookup"><span data-stu-id="8330e-127">The pack (*n*) option sets the current pack size to a specific value: 1, 2, 4, 8, or 16.</span></span> <span data-ttu-id="8330e-128">套件 (推送) 和套件 (pop) 選項具有下列特性：</span><span class="sxs-lookup"><span data-stu-id="8330e-128">The pack (push) and pack (pop) options have the following characteristics:</span></span>

-   <span data-ttu-id="8330e-129">編譯器會維護封裝堆疊。</span><span class="sxs-lookup"><span data-stu-id="8330e-129">The compiler maintains a packing stack.</span></span> <span data-ttu-id="8330e-130">封裝堆疊的元素包含套件大小和選擇性 *識別碼*。堆疊僅受限於堆疊頂端有目前套件大小的可用記憶體。</span><span class="sxs-lookup"><span data-stu-id="8330e-130">The elements of the packing stack include a pack size and an optional *id*. The stack is limited only by available memory with the current pack size at the top of the stack.</span></span>
-   <span data-ttu-id="8330e-131">封裝 (推送) 會導致目前的套件大小推送至封裝堆疊。</span><span class="sxs-lookup"><span data-stu-id="8330e-131">Pack (push) results in the current pack size pushed onto the packing stack.</span></span> <span data-ttu-id="8330e-132">堆疊受到可用記憶體的限制。</span><span class="sxs-lookup"><span data-stu-id="8330e-132">The stack is limited by available memory.</span></span>
-   <span data-ttu-id="8330e-133">套件 (推入，*n*) 與套件 (推入) ，接著套件 (*n*) 相同。</span><span class="sxs-lookup"><span data-stu-id="8330e-133">Pack (push,*n*) is the same as pack (push) followed by pack (*n*).</span></span>
-   <span data-ttu-id="8330e-134">套件 (推送， *識別碼*) 也會將 *識別碼* 和套件大小一起推送至封裝堆疊。</span><span class="sxs-lookup"><span data-stu-id="8330e-134">Pack (push, *id*) also pushes *id* onto the packing stack along with the pack size.</span></span>
-   <span data-ttu-id="8330e-135">套件 (推送、 *識別碼*、 *n*) 與套件 (推送、 *識別碼*) ，然後再加上套件 (*n*) 相同。</span><span class="sxs-lookup"><span data-stu-id="8330e-135">Pack (push, *id*, *n*) is the same as pack (push, *id*) followed by pack (*n*).</span></span>
-   <span data-ttu-id="8330e-136">Pack (pop) 會導致推出封裝堆疊。</span><span class="sxs-lookup"><span data-stu-id="8330e-136">Pack (pop) results in popping the packing stack.</span></span> <span data-ttu-id="8330e-137">不對稱的 pop 會導致警告，並將目前的套件大小設定為命令列值。</span><span class="sxs-lookup"><span data-stu-id="8330e-137">Unbalanced pops cause warnings and set the current pack size to the command-line value.</span></span>
-   <span data-ttu-id="8330e-138">如果指定了 pack (pop、 *id*、 *n*) ，則會忽略 *n* 。</span><span class="sxs-lookup"><span data-stu-id="8330e-138">If pack (pop, *id*, *n*) is specified, then *n* is ignored.</span></span>

<span data-ttu-id="8330e-139">MIDL 編譯器會將 [**\\ cpp \_ 引號**](cpp-quote.md)和 **pragma** 指示詞中所指定的字串，以 idl 檔案中指定的順序，以及 idl 檔案中其他介面元件的相對順序，放在標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="8330e-139">The MIDL compiler places the strings specified in the [**\\cpp\_quote**](cpp-quote.md) and **pragma** directives in the header file in the sequence in which they are specified in the IDL file and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="8330e-140">在所有匯 [**入**](import.md) 作業之後，字串通常應該會出現在 IDL 檔案的介面主體區段中。</span><span class="sxs-lookup"><span data-stu-id="8330e-140">The strings should usually appear in the interface-body section of the IDL file after all [**import**](import.md) operations.</span></span>

<span data-ttu-id="8330e-141">MIDL 編譯器不會嘗試處理開頭不是前置詞 "MIDL" 的 **\# pragma** 指示詞 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8330e-141">The MIDL compiler does not attempt to process **\#pragma** directives that do not start with the prefix "midl\_."</span></span> <span data-ttu-id="8330e-142">IDL 檔案中的其他 **\# pragma** 指示詞會傳遞至產生的標頭檔，而不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="8330e-142">Other **\#pragma** directives in the IDL file are passed into the generated header file without changes.</span></span>

## <a name="examples"></a><span data-ttu-id="8330e-143">範例</span><span class="sxs-lookup"><span data-stu-id="8330e-143">Examples</span></span>

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a><span data-ttu-id="8330e-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8330e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8330e-145">**cpp \_ 引號**</span><span class="sxs-lookup"><span data-stu-id="8330e-145">**cpp\_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="8330e-146"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="8330e-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="8330e-147">**進口**</span><span class="sxs-lookup"><span data-stu-id="8330e-147">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="8330e-148">**/Zp**</span><span class="sxs-lookup"><span data-stu-id="8330e-148">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




