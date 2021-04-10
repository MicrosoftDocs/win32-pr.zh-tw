---
title: 處理 IDL 檔案中的定義
description: 此頁面描述為何以 \ 定義定義的符號會從 MIDL 編譯器產生的 H 檔案消失，以及可以完成的工作。 這項說明適用于 MIDL 所處理的任何檔案，例如 \ .idl、acf、.h 檔案。
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL 編譯器 MIDL，處理定義
- 定義 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af77979824c2e76352d6f28bef72161249845d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021404"
---
# <a name="dealing-with-defines-in-idl-files"></a><span data-ttu-id="cb454-106">處理 \# IDL 檔案中的定義</span><span class="sxs-lookup"><span data-stu-id="cb454-106">Dealing with \#defines in IDL Files</span></span>

<span data-ttu-id="cb454-107">此頁面描述使用 **\# 定義** 定義的符號為何會從 MIDL 編譯器產生的 H 檔案消失，以及可以完成的工作。</span><span class="sxs-lookup"><span data-stu-id="cb454-107">This page describes why symbols defined with a **\#define** disappear from the MIDL compiler generated H files, and what can be done about it.</span></span> <span data-ttu-id="cb454-108">這項說明適用于 MIDL 所處理的任何檔案，例如 \* .idl、 \* . acf、 \* .h 檔案。</span><span class="sxs-lookup"><span data-stu-id="cb454-108">This explanation applies to any files processed by MIDL, such as \*.idl, \*.acf, \*.h files.</span></span>

<span data-ttu-id="cb454-109">**\# 定義** 符號的消失是 MIDL 將預先處理的輸入檔委派給預處理器的結果。</span><span class="sxs-lookup"><span data-stu-id="cb454-109">The disappearance of **\#define** symbols is a result of MIDL delegating the preprocessing of input files to a preprocessor.</span></span> <span data-ttu-id="cb454-110">根據預設，預處理器是組建環境中的 C/c + + 預處理器。</span><span class="sxs-lookup"><span data-stu-id="cb454-110">By default, the preprocessor is a C/C++ preprocessor from the build environment.</span></span> <span data-ttu-id="cb454-111">在前置處理之後，MIDL 接收的輸入資料流程只會有 \# 行預處理器指示詞。</span><span class="sxs-lookup"><span data-stu-id="cb454-111">After preprocessing, the input stream MIDL receives has only \#line preprocessor directives.</span></span> <span data-ttu-id="cb454-112">尤其是，預處理器會展開輸入檔中的所有巨集定義，因此 MIDL 無法偵測到它們的存在。</span><span class="sxs-lookup"><span data-stu-id="cb454-112">In particular, the preprocessor unrolls all macro definitions in input files, and therefore, MIDL cannot detect their presence.</span></span> <span data-ttu-id="cb454-113">因此，當 MIDL 將輸入檔中的型別定義複寫到產生的 H 檔案時， \# 就不會複寫定義。</span><span class="sxs-lookup"><span data-stu-id="cb454-113">Consequently, when MIDL replicates type definitions from an input file to the generated H file, the \#defines are not replicated.</span></span> <span data-ttu-id="cb454-114">因此， \# 如果稍後從產生的 H 檔案使用，請勿直接在 IDL 檔案中使用定義。</span><span class="sxs-lookup"><span data-stu-id="cb454-114">Therefore, do not use \#defines directly in IDL files if they are to be used later from the generated H file.</span></span>

<span data-ttu-id="cb454-115">建議您採用下列四種解決方法：</span><span class="sxs-lookup"><span data-stu-id="cb454-115">The following four workarounds are recommended:</span></span>

-   <span data-ttu-id="cb454-116">使用 [**const**](const.md) 宣告規格。</span><span class="sxs-lookup"><span data-stu-id="cb454-116">Use the [**const**](const.md) declaration specification.</span></span>
-   <span data-ttu-id="cb454-117">使用匯入或包含在 IDL 檔案中的個別標頭檔，稍後包含在 C 原始程式碼中。</span><span class="sxs-lookup"><span data-stu-id="cb454-117">Use separate header files that are imported or included in the IDL file, and later included in the C-source code.</span></span>
-   <span data-ttu-id="cb454-118">使用 IDL 檔案中的列舉常數。</span><span class="sxs-lookup"><span data-stu-id="cb454-118">Use enumeration constants in the IDL file.</span></span>
-   <span data-ttu-id="cb454-119">使用 [**cpp \_ 引號**](cpp-quote.md)在產生的標頭檔中重現 **\# 定義**。</span><span class="sxs-lookup"><span data-stu-id="cb454-119">Use [**cpp\_quote**](cpp-quote.md) to reproduce **\#define** in the generated header file.</span></span>

<span data-ttu-id="cb454-120">您可以使用 **IDL 常數宣告語法** 來重現資訊清單常數。</span><span class="sxs-lookup"><span data-stu-id="cb454-120">You can reproduce manifest constants using the **IDL constant-declaration syntax**.</span></span> <span data-ttu-id="cb454-121">請注意，IDL 常數宣告中的 [**常數**](const.md) 與 c/c + + **const** 語義不同，只是導入 idl 編譯的命名常數。</span><span class="sxs-lookup"><span data-stu-id="cb454-121">Note that the [**const**](const.md) in the IDL constant-declaration is different from C/C++ **const** semantics, and simply introduces a named constant for an IDL compilation.</span></span> <span data-ttu-id="cb454-122">例如：</span><span class="sxs-lookup"><span data-stu-id="cb454-122">For example:</span></span>

``` syntax
const short ARRSIZE = 10
```

<span data-ttu-id="cb454-123">這個範例會指定 **ARRSIZE** 是值為10的常數。</span><span class="sxs-lookup"><span data-stu-id="cb454-123">This example specifies that **ARRSIZE** is a constant with a value of 10.</span></span> <span data-ttu-id="cb454-124">您可以在 IDL 陣列宣告子中使用已命名的常數，以及 C 程式設計人員會使用資訊清單定義的其他位置。</span><span class="sxs-lookup"><span data-stu-id="cb454-124">Named constants can be used in IDL array declarators and other places where a C programmer would use a manifest defines.</span></span> <span data-ttu-id="cb454-125">此外，此語法會導致在標頭檔中產生下行：</span><span class="sxs-lookup"><span data-stu-id="cb454-125">In addition, this syntax results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

<span data-ttu-id="cb454-126">處理 define 語句的另一種方式 **\#** ，是將它們封裝在個別的標頭檔中，放在專門用來定義語句的檔案， **\#** 或只包含型別定義的檔案中。</span><span class="sxs-lookup"><span data-stu-id="cb454-126">Another way to handle **\#** define statements is to package them in a separate header file, either into a file devoted to **\#** define statements or into a file that contains only type definitions.</span></span> <span data-ttu-id="cb454-127">IDL 檔案和 C 原始程式檔都可以安全地同時包含預處理器指示詞的檔案。</span><span class="sxs-lookup"><span data-stu-id="cb454-127">A file that contains only preprocessor directives may be safely included both by the IDL file and the C-source files.</span></span> <span data-ttu-id="cb454-128">雖然 MIDL 編譯器所產生的標頭檔中將無法使用指示詞，但 C 來來源程式可包含個別的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="cb454-128">Although the directives will not be available in the header file generated by the MIDL compiler, the C-source program can include the separate header file.</span></span> <span data-ttu-id="cb454-129">以類似的方式， **\#** 可以從 IDL 檔案匯入具有定義語句和一般類型定義的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="cb454-129">In a similar fashion, a header file with **\#** define statements and regular type definitions can be imported from your IDL file.</span></span> <span data-ttu-id="cb454-130">這種方法 **\#** 會在 H 檔案中使用定義和 typedef 語句，讓 **\#** 定義符號不會直接在匯入 IDL 檔案中使用。</span><span class="sxs-lookup"><span data-stu-id="cb454-130">This approach encapsulates the **\#** define and typedef statements by using them in an H file such that the **\#** define symbols are not used in the importing IDL file directly.</span></span> <span data-ttu-id="cb454-131">將標頭或 IDL 檔案匯入至另一個 IDL 檔案，可防止 typedef 語句複寫到 MIDL 所產生的 H 檔案 (這與 **\#** include 語句) 相反。</span><span class="sxs-lookup"><span data-stu-id="cb454-131">Importing a header or IDL file to another IDL file prevents the typedef statements from being replicated to the H file generated by MIDL (which is in contrast to **\#** include statements).</span></span> <span data-ttu-id="cb454-132">這種方法可讓原始的標頭檔在產生的 H 檔中安全地從 C 程式碼參考，而不會有重複定義的問題。</span><span class="sxs-lookup"><span data-stu-id="cb454-132">This approach allows the original header file to be safely referenced from the C code along the generated H file without having a problem with duplicated definitions.</span></span>

<span data-ttu-id="cb454-133">在 IDL 檔案中使用列舉常數也是有效的。</span><span class="sxs-lookup"><span data-stu-id="cb454-133">Use of enumeration constants in the IDL file is also effective.</span></span> <span data-ttu-id="cb454-134">這些常數可以在 IDL 的常數運算式中使用，例如，在陣列宣告子中。</span><span class="sxs-lookup"><span data-stu-id="cb454-134">These constants can be used in constant expressions in IDL, for example, in array declarators.</span></span> <span data-ttu-id="cb454-135">C 編譯器預處理器不會在 MIDL 編譯的早期階段中移除列舉常數，因此可在 MIDL 編譯器所產生的標頭檔中使用列舉常數。</span><span class="sxs-lookup"><span data-stu-id="cb454-135">Enumeration constants are not removed during the early phases of MIDL compilation by the C-compiler preprocessor, so enumeration constants are available in the header file generated by the MIDL compiler.</span></span> <span data-ttu-id="cb454-136">以下列陳述式為例：</span><span class="sxs-lookup"><span data-stu-id="cb454-136">Consider the following statement:</span></span>

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

<span data-ttu-id="cb454-137">C 預處理器不會在 MIDL 編譯期間移除此語句，而且 typedef 將會複寫至產生的 H 檔案。</span><span class="sxs-lookup"><span data-stu-id="cb454-137">This statement will not be removed during MIDL compilation by the C preprocessor and the typedef will be replicated to the generated H file.</span></span> <span data-ttu-id="cb454-138">常數 MAXSTRINGCOUNT 適用于 C 來來源程式，其中包括 MIDL 編譯器所產生的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="cb454-138">The constant MAXSTRINGCOUNT is available to C-source programs that include the header file generated by the MIDL compiler.</span></span>

<span data-ttu-id="cb454-139">最後，MIDL 的 [**cpp \_ 引號**](cpp-quote.md) 指示詞可以用來將任一字元串直接寫到產生的 H 檔案中。</span><span class="sxs-lookup"><span data-stu-id="cb454-139">Finally, the [**cpp\_quote**](cpp-quote.md) directive of MIDL can be used to write out an arbitrary string directly into the generated H file.</span></span> <span data-ttu-id="cb454-140">例如，若要取得先前在此頁面上使用 **cpp \_ 引號** 的資訊清單常數，可以使用下列語句：</span><span class="sxs-lookup"><span data-stu-id="cb454-140">For example, to get the manifest constant used previously on this page with **cpp\_quote**, the following statement can be used:</span></span>

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

<span data-ttu-id="cb454-141">此語句會導致在標頭檔中產生下行：</span><span class="sxs-lookup"><span data-stu-id="cb454-141">This statement results in the following line being generated in the header file:</span></span>

``` syntax
#define ARRSIZE 10
```

 

 




