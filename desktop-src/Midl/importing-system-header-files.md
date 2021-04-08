---
title: 匯入系統標頭檔
description: 雖然通常可以使用-include 指示詞在 IDL 檔案中包含標頭檔，但並不建議這麼做。
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- 匯入 MIDL、系統標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696342"
---
# <a name="importing-system-header-files"></a><span data-ttu-id="c8c17-104">匯入系統標頭檔</span><span class="sxs-lookup"><span data-stu-id="c8c17-104">Importing System Header Files</span></span>

<span data-ttu-id="c8c17-105">雖然通常可以使用 **\# include** 指示詞將標頭檔包含在 IDL 檔案中，但不建議您這樣做。</span><span class="sxs-lookup"><span data-stu-id="c8c17-105">While it is often possible to use the **\#include** directive to include header files in your IDL file, it is not recommended.</span></span> <span data-ttu-id="c8c17-106">MIDL 編譯器會針對正在編譯的 IDL 檔案中定義的所有函式產生存根。</span><span class="sxs-lookup"><span data-stu-id="c8c17-106">The MIDL compiler will generate stubs for all functions defined in the IDL file being compiled.</span></span> <span data-ttu-id="c8c17-107">通常，標頭檔會包含您不需要或不想要包含在存根檔案中的一些原型，而且會將所有這些定義有效地放入 **\# 您的主要** IDL 檔案中。</span><span class="sxs-lookup"><span data-stu-id="c8c17-107">Usually a header file contains a number of prototypes that you neither need nor want to include in your stub files, and a **\#include** effectively puts all those definitions into your main IDL file.</span></span> <span data-ttu-id="c8c17-108">此外，如果標頭檔中有定義不可遠端處理類型，IDL 檔案可能不會編譯。</span><span class="sxs-lookup"><span data-stu-id="c8c17-108">Furthermore, if there are nonremotable types defined in the header file, the IDL file may not compile.</span></span>

<span data-ttu-id="c8c17-109">有兩種方式可將標頭檔中的類型定義包含在 IDL 檔案中：</span><span class="sxs-lookup"><span data-stu-id="c8c17-109">There are two ways to include type definitions from header files in an IDL file:</span></span>

-   <span data-ttu-id="c8c17-110">使用匯 [**入**](import.md) 指示詞來包含標頭檔中定義的資料類型。</span><span class="sxs-lookup"><span data-stu-id="c8c17-110">Use the [**import**](import.md) directive to include data types defined in a header file.</span></span> <span data-ttu-id="c8c17-111">與 C 語言 **\# include** 指示詞不同，匯 **入** 指示詞只會挑選型別和常數定義，並忽略程式原型。</span><span class="sxs-lookup"><span data-stu-id="c8c17-111">Unlike the C-language **\#include** directive, the **import** directive only picks up type and constant definitions and ignores procedure prototypes.</span></span> <span data-ttu-id="c8c17-112">只要您的主要 IDL 檔案未參考標頭檔中定義的任何不可遠端處理類型，這個方法就會運作。</span><span class="sxs-lookup"><span data-stu-id="c8c17-112">This approach will work as long as your main IDL file does not reference any nonremotable types defined in the header file.</span></span>
-   <span data-ttu-id="c8c17-113">使用包含標頭檔的虛擬介面建立 helper IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="c8c17-113">Create a helper IDL file with a dummy interface that includes the header files.</span></span> <span data-ttu-id="c8c17-114">然後，使用匯 [**入**](import.md) 指示詞來包含 helper 檔案。</span><span class="sxs-lookup"><span data-stu-id="c8c17-114">Then, use the [**import**](import.md) directive to include the helper file.</span></span> <span data-ttu-id="c8c17-115">如此一來，只有 [**typedef**](typedef.md)才會出現在已編譯的存根中。</span><span class="sxs-lookup"><span data-stu-id="c8c17-115">In this way, only the [**typedef**](typedef.md)s will appear in the compiled stubs.</span></span> <span data-ttu-id="c8c17-116">例如：</span><span class="sxs-lookup"><span data-stu-id="c8c17-116">For example:</span></span>

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
