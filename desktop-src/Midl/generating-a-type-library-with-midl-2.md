---
title: 使用 MIDL 產生類型程式庫
description: ODL 語法的最上層元素是程式庫語句 (程式庫區塊) 。
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Microsoft 介面定義語言 MIDL、工作、產生類型程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85f6e8f7ea6f65bc503c08872c9199ff3d5fd828
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967893"
---
# <a name="generating-a-type-library-with-midl"></a><span data-ttu-id="c7adb-104">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c7adb-104">Generating a Type Library with MIDL</span></span>

<span data-ttu-id="c7adb-105">ODL 語法的最上層元素是程式庫語句 (程式庫區塊) 。</span><span class="sxs-lookup"><span data-stu-id="c7adb-105">The top-level element of the ODL syntax is the library statement (library block).</span></span> <span data-ttu-id="c7adb-106">除了套用至程式庫語句的屬性之外，每個其他 ODL 語句都必須定義于程式庫區塊內。</span><span class="sxs-lookup"><span data-stu-id="c7adb-106">Every other ODL statement, with the exception of the attributes that are applied to the library statement, must be defined within the library block.</span></span> <span data-ttu-id="c7adb-107">當 MIDL 編譯器看到程式庫區塊時，它會產生類型程式庫，與 Mktyplib.exe 的方式大致相同。</span><span class="sxs-lookup"><span data-stu-id="c7adb-107">When the MIDL compiler sees a library block, it generates a type library in much the same way that MkTypLib does.</span></span> <span data-ttu-id="c7adb-108">除了 [MIDL 和 Mktyplib.exe 之間的差異](differences-between-midl-and-mktyplib.md)中所述的一些例外狀況，程式庫區塊內的語句應遵循與 ODL 語言和 mktyplib.exe 中相同的語法。</span><span class="sxs-lookup"><span data-stu-id="c7adb-108">With a few exceptions, described in [Differences Between MIDL and MKTYPLIB](differences-between-midl-and-mktyplib.md), the statements within the library block should follow the same syntax as in the ODL language and MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="c7adb-109">Mktyplib.exe 工具已淘汰。</span><span class="sxs-lookup"><span data-stu-id="c7adb-109">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="c7adb-110">請改用 MIDL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="c7adb-110">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="c7adb-111">您可以將 ODL 屬性套用至在程式庫區塊內部或外部定義的元素。</span><span class="sxs-lookup"><span data-stu-id="c7adb-111">You can apply ODL attributes to elements that are defined either inside or outside the library block.</span></span> <span data-ttu-id="c7adb-112">除非從程式庫區塊內參考所套用的元素，否則這些屬性不會在程式庫區塊之外生效。</span><span class="sxs-lookup"><span data-stu-id="c7adb-112">These attributes have no effect outside the library block unless the element they are applied to is referenced from within the library block.</span></span> <span data-ttu-id="c7adb-113">程式庫區塊內的語句可以參考外部專案，方法是使用它作為基底類型、繼承自它，或在行上參考它，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c7adb-113">Statements inside the library block can reference an outside element either by using it as a base type, inheriting from it, or by referencing it on a line as shown:</span></span>

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

<span data-ttu-id="c7adb-114">如果程式庫區塊內所定義的元素是在程式庫區塊內參考，則其定義會放入產生的類型程式庫中。</span><span class="sxs-lookup"><span data-stu-id="c7adb-114">If an element defined outside the library block is referenced within the library block, then its definition will be put into the generated type library.</span></span> <span data-ttu-id="c7adb-115">MIDL 編譯器會將程式庫區塊以外的語句視為一般的 IDL 檔案，並剖析這些語句，因為它一律已完成。</span><span class="sxs-lookup"><span data-stu-id="c7adb-115">The MIDL compiler treats the statements outside of a library block as a typical IDL file and parses those statements as it has always done.</span></span> <span data-ttu-id="c7adb-116">一般來說，這表示會為 RPC 應用程式產生 C 語言的存根。</span><span class="sxs-lookup"><span data-stu-id="c7adb-116">Normally, this means generating C-language stubs for an RPC application.</span></span>

<span data-ttu-id="c7adb-117">如需 ODL 檔之一般語法的詳細資訊，請參閱 [ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)。</span><span class="sxs-lookup"><span data-stu-id="c7adb-117">For more information about the general syntax for an ODL file see [ODL File Syntax](/previous-versions/windows/desktop/automat/odl-file-syntax).</span></span>

 

 