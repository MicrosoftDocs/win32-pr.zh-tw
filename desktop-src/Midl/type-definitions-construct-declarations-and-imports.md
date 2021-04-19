---
title: 型別定義、結構宣告和匯入
description: 型別定義、結構宣告和匯入可以出現在介面主體之外。
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- 介面 MIDL、類型定義
- 介面 MIDL、結構聲明
- 介面 MIDL、imports
- 類型定義 MIDL
- 結構聲明 MIDL
- 匯入 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645781f033566ba43dc6e355935ed112d0e8f5f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106999776"
---
# <a name="type-definitions-construct-declarations-and-imports"></a><span data-ttu-id="ee8c5-109">型別定義、結構宣告和匯入</span><span class="sxs-lookup"><span data-stu-id="ee8c5-109">Type Definitions, Construct Declarations, and Imports</span></span>

<span data-ttu-id="ee8c5-110">型別定義、結構宣告和匯入可以出現在介面主體之外。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-110">Type definitions, construct declarations, and imports can occur outside of the interface body.</span></span> <span data-ttu-id="ee8c5-111">所有來自主要 IDL 檔案的定義都會出現在產生的標頭檔中，而主要 IDL 檔案中所有介面的所有程式都會產生存根常式。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-111">All definitions from the main IDL file will appear in the generated header file, and all the procedures from all the interfaces in the main IDL file will generate stub routines.</span></span> <span data-ttu-id="ee8c5-112">這可讓支援多個介面的應用程式將 IDL 檔案合併成單一合併的 IDL 檔。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-112">This enables applications that support multiple interfaces to merge IDL files into a single, combined IDL file.</span></span>

<span data-ttu-id="ee8c5-113">因此，編譯檔案需要較少的時間，而且也允許 MIDL 減少產生的存根中的冗余。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-113">As a result, it requires less time to compile the files and also allows MIDL to reduce redundancies in the generated stubs.</span></span> <span data-ttu-id="ee8c5-114">這可以透過共用基底介面和衍生介面的通用程式碼的能力，大幅改善 [**物件**](object.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-114">This can significantly improve [**object**](object.md) interfaces through the ability to share common code for base interfaces and derived interfaces.</span></span> <span data-ttu-id="ee8c5-115">若是非 **物件** 介面，程式名稱在所有介面中都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-115">For non- **object** interfaces, the procedure names must be unique across all the interfaces.</span></span> <span data-ttu-id="ee8c5-116">針對 **物件** 介面，程式名稱只需要在介面內是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-116">For **object** interfaces, the procedure names need to be unique only within an interface.</span></span> <span data-ttu-id="ee8c5-117">請注意，當您使用 [**/osf**](-osf.md) 參數時，不允許使用多個介面。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-117">Note that multiple interfaces are not permitted when you use the [**/osf**](-osf.md) switch.</span></span>

## <a name="declarative-constructs"></a><span data-ttu-id="ee8c5-118">宣告式結構</span><span class="sxs-lookup"><span data-stu-id="ee8c5-118">Declarative Constructs</span></span>

<span data-ttu-id="ee8c5-119">IDL 檔案中宣告式結構的語法類似于 C 的語法。 MIDL 支援所有的 Microsoft C/c + + 宣告式結構，但以下除外：</span><span class="sxs-lookup"><span data-stu-id="ee8c5-119">The syntax for declarative constructs in the IDL file is similar to that for C. MIDL supports all Microsoft C/C++ declarative constructs except the following:</span></span>

-   <span data-ttu-id="ee8c5-120">較舊的樣式宣告子，允許在沒有類型規範的情況下指定宣告子，例如：</span><span class="sxs-lookup"><span data-stu-id="ee8c5-120">Older style declarators that allow a declarator to be specified without a type specifier, such as:</span></span>

    ``` syntax
    x (y) 
    short x (y)
    ```

-   <span data-ttu-id="ee8c5-121">具有初始化運算式 (MIDL 的宣告只接受符合 MIDL [**const**](const.md) 語法) 的宣告。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-121">Declarations with initializers (MIDL only accepts declarations that conform to the MIDL [**const**](const.md) syntax).</span></span>

<span data-ttu-id="ee8c5-122">[**Import**](import.md)關鍵字會指定要匯入的一或多個 IDL 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-122">The [**import**](import.md) keyword specifies the names of one or more IDL files to import.</span></span> <span data-ttu-id="ee8c5-123">匯入指示詞類似 C [**include**](include.md) 指示詞，但只有資料類型會 assimilated 到匯入的 IDL 檔案中。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-123">The import directive is similar to the C [**include**](include.md) directive, except that only data types are assimilated into the importing IDL file.</span></span>

## <a name="constant-declaration"></a><span data-ttu-id="ee8c5-124">常數宣告</span><span class="sxs-lookup"><span data-stu-id="ee8c5-124">Constant Declaration</span></span>

<span data-ttu-id="ee8c5-125">常數宣告會指定 [**布林值**](boolean.md)、整數、字元、寬字元、字串和 **void \*** 常數。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-125">The constant declaration specifies [**Boolean**](boolean.md), integer, character, wide-character, string, and **void \*** constants.</span></span> <span data-ttu-id="ee8c5-126">如需詳細資訊，請參閱 [**const**](const.md)。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-126">For more information, see [**const**](const.md).</span></span>

## <a name="general-declaration"></a><span data-ttu-id="ee8c5-127">一般宣告</span><span class="sxs-lookup"><span data-stu-id="ee8c5-127">General Declaration</span></span>

<span data-ttu-id="ee8c5-128">一般宣告類似于 C [**typedef**](typedef.md) 語句加上 IDL 型別屬性。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-128">A general declaration is similar to the C [**typedef**](typedef.md) statement with the addition of IDL type attributes.</span></span> <span data-ttu-id="ee8c5-129">除了在 [**/osf**](-osf.md) 模式中，MIDL 編譯器也會允許變數定義形式的隱含宣告。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-129">Except in [**/osf**](-osf.md) mode, the MIDL compiler also allows an implicit declaration in the form of a variable definition.</span></span>

## <a name="function-declaration"></a><span data-ttu-id="ee8c5-130">函式宣告</span><span class="sxs-lookup"><span data-stu-id="ee8c5-130">Function Declaration</span></span>

<span data-ttu-id="ee8c5-131">函式宣告子是一般宣告的特殊案例。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-131">The function declarator is a special case of the general declaration.</span></span> <span data-ttu-id="ee8c5-132">您可以使用 IDL 屬性來指定函式傳回類型和每個參數的行為。</span><span class="sxs-lookup"><span data-stu-id="ee8c5-132">You can use IDL attributes to specify the behavior of the function return type and each of the parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="ee8c5-133">範例</span><span class="sxs-lookup"><span data-stu-id="ee8c5-133">Examples</span></span>

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 




