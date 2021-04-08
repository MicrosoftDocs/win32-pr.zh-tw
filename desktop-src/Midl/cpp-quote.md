---
title: cpp_quote 屬性
description: Cpp \_ 引號關鍵字會指示 MIDL 將指定的字串（不含引號字元）發出至產生的標頭檔。
ms.assetid: 0e5a929e-b564-43f7-9270-e79486279834
keywords:
- cpp_quote 屬性 MIDL
topic_type:
- apiref
api_name:
- cpp_quote
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b85f9a909e82395a0a75cf66fb2957c4b03d9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022596"
---
# <a name="cpp_quote-attribute"></a><span data-ttu-id="9260c-104">cpp \_ quote 屬性</span><span class="sxs-lookup"><span data-stu-id="9260c-104">cpp\_quote attribute</span></span>

<span data-ttu-id="9260c-105">**Cpp \_ 引號** 關鍵字會指示 MIDL 將指定的字串（不含引號字元）發出至產生的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="9260c-105">The **cpp\_quote** keyword instructs MIDL to emit the specified string, without the quote characters, into the generated header file.</span></span>

``` syntax
cpp_quote("string")
```

## <a name="parameters"></a><span data-ttu-id="9260c-106">參數</span><span class="sxs-lookup"><span data-stu-id="9260c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9260c-107">*string*</span><span class="sxs-lookup"><span data-stu-id="9260c-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="9260c-108">指定在產生的標頭檔中發出的加上引號的字串。</span><span class="sxs-lookup"><span data-stu-id="9260c-108">Specifies a quoted string that is emitted in the generated header file.</span></span> <span data-ttu-id="9260c-109">字串必須以引號括住，以防止 C 預處理器進行擴充。</span><span class="sxs-lookup"><span data-stu-id="9260c-109">The string must be quoted to prevent expansion by the C preprocessor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9260c-110">備註</span><span class="sxs-lookup"><span data-stu-id="9260c-110">Remarks</span></span>

<span data-ttu-id="9260c-111">出現在 IDL 檔案中的 c 語言前置處理指示詞是由 C 編譯器的預處理器所處理。</span><span class="sxs-lookup"><span data-stu-id="9260c-111">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="9260c-112">IDL 編譯期間會提供 IDL 檔案中的 **\# 定義** 指示詞，但 C 編譯器無法使用這些指示詞。</span><span class="sxs-lookup"><span data-stu-id="9260c-112">The **\#define** directives in the IDL file are available during MIDL compilation but are not available to the C compiler.</span></span>

<span data-ttu-id="9260c-113">例如，當預處理器遇到「定義 WINDOWS 4」指示詞時 \# ，預處理器會將 IDL 檔案中所有出現的 "WINDOWS" 取代為 "4"。</span><span class="sxs-lookup"><span data-stu-id="9260c-113">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="9260c-114">C 語言編譯期間無法使用符號 "WINDOWS"。</span><span class="sxs-lookup"><span data-stu-id="9260c-114">The symbol "WINDOWS" is not available during C-language compilation.</span></span>

<span data-ttu-id="9260c-115">若要允許 C 預處理器巨集定義傳遞 MIDL 編譯器至 C 編譯器，請使用 **\# pragma MIDL \_ echo** 或 **cpp \_ 引號** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="9260c-115">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or **cpp\_quote** directive.</span></span> <span data-ttu-id="9260c-116">這些指示詞會指示 MIDL 編譯器產生包含參數字串的標頭檔，並移除引號。</span><span class="sxs-lookup"><span data-stu-id="9260c-116">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="9260c-117">**\# Pragma midl \_ echo** 和 **cpp \_ 引號** 指示詞是相等的。</span><span class="sxs-lookup"><span data-stu-id="9260c-117">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="9260c-118">MIDL 編譯器會將 **cpp \_ 引號** 和 [**pragma**](pragma.md) 指示詞中所指定的字串，以 idl 檔案中指定的順序，以及 idl 檔案中其他介面元件的相對順序，放在標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="9260c-118">The MIDL compiler places the strings specified in the **cpp\_quote** and [**pragma**](pragma.md) directives into the header file in the sequence in which they are specified in the IDL file, and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="9260c-119">在所有匯 [**入**](import.md) 作業之後，字串通常應該會出現在 IDL 檔案介面主體區段中。</span><span class="sxs-lookup"><span data-stu-id="9260c-119">The strings should usually appear in the IDL file interface body section after all [**import**](import.md) operations.</span></span>

## <a name="examples"></a><span data-ttu-id="9260c-120">範例</span><span class="sxs-lookup"><span data-stu-id="9260c-120">Examples</span></span>

``` syntax
cpp_quote("#include \"myfile.h\" ")  
cpp_quote("#define UNICODE")
```

## <a name="see-also"></a><span data-ttu-id="9260c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9260c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9260c-122"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="9260c-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="9260c-123">**進口**</span><span class="sxs-lookup"><span data-stu-id="9260c-123">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="9260c-124">**pragma**</span><span class="sxs-lookup"><span data-stu-id="9260c-124">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




