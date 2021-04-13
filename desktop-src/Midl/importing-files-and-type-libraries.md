---
title: 匯入檔案和型別程式庫
description: MIDL 關鍵字包括、匯入和 importlib，可讓您藉由參考現有的標頭、IDL 和物件定義語言 (ODL) 檔和編譯的類型程式庫來重複使用程式碼。
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Microsoft 介面定義語言 MIDL、工作、匯入檔案和型別程式庫
- 匯入 MIDL
- 類型程式庫 MIDL，匯入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104322572"
---
# <a name="importing-files-and-type-libraries"></a><span data-ttu-id="86e53-106">匯入檔案和型別程式庫</span><span class="sxs-lookup"><span data-stu-id="86e53-106">Importing Files and Type Libraries</span></span>

<span data-ttu-id="86e53-107">MIDL 關鍵字 [**包括**](include.md)、匯 [**入**](import.md)和 [**importlib**](importlib.md) ，可讓您藉由參考現有的標頭、IDL 和物件定義語言 (ODL) 檔和編譯的類型程式庫來重複使用程式碼。</span><span class="sxs-lookup"><span data-stu-id="86e53-107">The MIDL keywords [**include**](include.md), [**import**](import.md), and [**importlib**](importlib.md) let you reuse code by referencing existing header, IDL, and object definition language (ODL) files, and compiled type libraries.</span></span>

<span data-ttu-id="86e53-108">ACF [**include**](include.md) 指示詞可讓您在 ACF 檔中指定要包含在 MIDL 產生的存根程式碼中的一或多個 C 語言標頭檔。</span><span class="sxs-lookup"><span data-stu-id="86e53-108">The ACF [**include**](include.md) directive lets you specify in an ACF file one or more C-language header files to be included in the MIDL-generated stub code.</span></span> <span data-ttu-id="86e53-109">產生的檔案會有一行包含 C 預處理器指示詞，其中 **\# 包含** 指定的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="86e53-109">The generated file will have a line with a **\#include** C-preprocessor directive with the indicated header file.</span></span> <span data-ttu-id="86e53-110">使用這個 **include** 指示詞來帶入特定作業環境專屬的標頭檔，而不包含用戶端與伺服器之間的介面所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="86e53-110">Use this **include** directive to bring in header files that are specific to a particular operating environment and that do not contain information necessary for the interface between client and server.</span></span> <span data-ttu-id="86e53-111">針對包含您要提供給 IDL 檔案之資料類型的標頭檔，請勿使用 **include** ：請改用 [**import**](import.md) 指示詞。</span><span class="sxs-lookup"><span data-stu-id="86e53-111">Do not use **include** for header files containing data types that you want available to the IDL file; instead, use the [**import**](import.md) directive.</span></span>

## <a name="example-1"></a><span data-ttu-id="86e53-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="86e53-112">Example 1</span></span>

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

<span data-ttu-id="86e53-113">IDL 匯 [**入**](import.md) 指示詞是一種標準方法，可將其他 IDL (或 ODL) 檔案和標頭檔中的型別和介面定義帶入 IDL 檔案中。</span><span class="sxs-lookup"><span data-stu-id="86e53-113">The IDL [**import**](import.md) directive is the standard method for bringing type and interface definitions from other IDL (or ODL) files and header files into your IDL file.</span></span> <span data-ttu-id="86e53-114">匯入的檔案中的所有 IDL 語句，例如 typedef、 [**const**](const.md) 宣告和介面定義，都會變成可供匯入的 IDL 檔案使用。</span><span class="sxs-lookup"><span data-stu-id="86e53-114">All IDL statements in the imported file, such as typedefs, [**const**](const.md) declarations, and interface definitions become available to the importing IDL file.</span></span>

<span data-ttu-id="86e53-115">如同 C 語言預處理器指示詞， [**import-module**](import.md)會告知編譯器 **\# 要包含匯** 入的 IDL 檔案中所定義的資料類型。</span><span class="sxs-lookup"><span data-stu-id="86e53-115">Like the C-language preprocessor directive **\#include**, the [**import**](import.md) directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="86e53-116">和 **\# include** 指示詞不同，匯 **入** 指示詞會忽略程式原型，因為匯入檔案中的任何作業都不會產生任何 stub。</span><span class="sxs-lookup"><span data-stu-id="86e53-116">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span> <span data-ttu-id="86e53-117">因為會針對匯入的檔案個別叫用預處理器，所以預處理器指示詞 (例如 \* \* ) 不會延續至匯入的 IDL 檔。</span><span class="sxs-lookup"><span data-stu-id="86e53-117">Because the preprocessor is invoked separately for the imported file, preprocessor directives (such as \*\*) do not carry over to the importing IDL file.</span></span>

<span data-ttu-id="86e53-118">如需使用匯 [**入**](import.md) 在 IDL 檔案中包含系統標頭檔的詳細資訊，請參閱匯 [入系統標頭檔](importing-system-header-files.md)。</span><span class="sxs-lookup"><span data-stu-id="86e53-118">For additional information on using [**import**](import.md) to include system header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

## <a name="example-2"></a><span data-ttu-id="86e53-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="86e53-119">Example 2</span></span>

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

<span data-ttu-id="86e53-120">ODL [**importlib**](importlib.md) 指示詞可讓您參考 IDL 或 ODL 檔案中已編譯的類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="86e53-120">The ODL [**importlib**](importlib.md) directive lets you reference a compiled type library in your IDL or ODL file.</span></span> <span data-ttu-id="86e53-121">**Importlib** 指示詞必須在程式庫 [**語句內**](library.md)，而且必須在程式庫中的其他類型描述之前。</span><span class="sxs-lookup"><span data-stu-id="86e53-121">The **importlib** directive must be inside a [**library**](library.md) statement, and must precede other type descriptions in the library.</span></span> <span data-ttu-id="86e53-122">匯入的程式庫以及產生的程式庫，都必須可供應用程式在執行時間使用。</span><span class="sxs-lookup"><span data-stu-id="86e53-122">The imported library, as well as the generated library, must be available to the application at runtime.</span></span>

## <a name="example-3"></a><span data-ttu-id="86e53-123">範例 3</span><span class="sxs-lookup"><span data-stu-id="86e53-123">Example 3</span></span>

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

<span data-ttu-id="86e53-124">您也可以使用 C 預處理器 **\# include** 指示詞，在 IDL 或 ODL 檔案中包含標頭和其他檔案。</span><span class="sxs-lookup"><span data-stu-id="86e53-124">You can also use the C-preprocessor **\#include** directive to include headers and other files in your IDL or ODL file.</span></span> <span data-ttu-id="86e53-125">不過請注意，這個指示詞實際上會包含指定檔案的整個內容。</span><span class="sxs-lookup"><span data-stu-id="86e53-125">Be aware, however, that this directive will literally include the entire contents of the specified file.</span></span> <span data-ttu-id="86e53-126">如果標頭檔包含在 MIDL 產生的存根檔案中不需要或不想要的原型，或包含不可遠端處理類型定義，則您應該使用 MIDL 匯 [**入**](import.md)指示詞，而不是 **\# include** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="86e53-126">If a header file contains prototypes that you do not need or want in the MIDL-generated stub files, or if it contains nonremotable type definitions, you should use the MIDL [**import**](import.md) directive instead of the **\#include** directive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86e53-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="86e53-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86e53-128">**進口**</span><span class="sxs-lookup"><span data-stu-id="86e53-128">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="86e53-129">**importlib**</span><span class="sxs-lookup"><span data-stu-id="86e53-129">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="86e53-130">**包括**</span><span class="sxs-lookup"><span data-stu-id="86e53-130">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="86e53-131">匯入系統標頭檔</span><span class="sxs-lookup"><span data-stu-id="86e53-131">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




