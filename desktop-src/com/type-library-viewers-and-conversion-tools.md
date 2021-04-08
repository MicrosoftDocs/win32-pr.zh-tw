---
title: 類型程式庫檢視器和轉換工具
description: 類型程式庫檢視器和轉換工具
ms.assetid: 35c29e2c-3ee3-4e73-b925-6aa0ccb50a00
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bf4ac71b3c2c2ff9cc63b196485b9e0aaa4e13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671551"
---
# <a name="type-library-viewers-and-conversion-tools"></a><span data-ttu-id="6b30b-103">類型程式庫檢視器和轉換工具</span><span class="sxs-lookup"><span data-stu-id="6b30b-103">Type Library Viewers and Conversion Tools</span></span>

<span data-ttu-id="6b30b-104">類型程式庫包含一或多個 COM 元素的規格，包括類別、介面、列舉等等。</span><span class="sxs-lookup"><span data-stu-id="6b30b-104">Type libraries contain the specification for one or more COM elements, including classes, interfaces, enumerations, and more.</span></span> <span data-ttu-id="6b30b-105">這些檔案會以標準二進位格式儲存。</span><span class="sxs-lookup"><span data-stu-id="6b30b-105">These files are stored in a standard binary format.</span></span> <span data-ttu-id="6b30b-106">類型程式庫可以是副檔名為 .tlb 的獨立檔案，也可以將它儲存為可執行檔中的資源，該檔案的副檔名可以是 .ocx、.dll 或 .exe。</span><span class="sxs-lookup"><span data-stu-id="6b30b-106">A type library can be a stand-alone file with the .tlb file name extension, or it can be stored as a resource in an executable file, which can have an .ocx, .dll, or .exe file name extension.</span></span> <span data-ttu-id="6b30b-107">下列所述的類型程式庫檢視器和轉換工具會讀取此格式，以瞭解程式庫中 COM 元素的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6b30b-107">The type library viewers and conversion tools described following read this format to gain information about the COM elements in the library.</span></span>

<span data-ttu-id="6b30b-108">在您可以使用特定程式設計語言來設計物件之前，您必須能夠以該語言來查看其型別程式庫。</span><span class="sxs-lookup"><span data-stu-id="6b30b-108">Before you can program an object in a particular programming language, you must be able to view its type library in that language.</span></span> <span data-ttu-id="6b30b-109">這樣做可為您提供 COM 物件的類別、介面、方法、屬性和事件的正確語法。</span><span class="sxs-lookup"><span data-stu-id="6b30b-109">Doing this provides you with the proper syntax for the classes, interfaces, methods, properties, and events of the COM object.</span></span>

<span data-ttu-id="6b30b-110">Microsoft 開發產品提供下列工具，可讓您用來產生、解壓縮和查看型別程式庫資訊。</span><span class="sxs-lookup"><span data-stu-id="6b30b-110">Microsoft development products provide the following tools that you can use to generate, extract, and view type library information.</span></span>

## <a name="c"></a><span data-ttu-id="6b30b-111">C++</span><span class="sxs-lookup"><span data-stu-id="6b30b-111">C++</span></span>

-   [<span data-ttu-id="6b30b-112">OLE COM 物件檢視器</span><span class="sxs-lookup"><span data-stu-id="6b30b-112">OLE-COM Object Viewer</span></span>](ole-com-object-viewer.md)
-   [<span data-ttu-id="6b30b-113">MIDL 編譯器</span><span class="sxs-lookup"><span data-stu-id="6b30b-113">MIDL compiler</span></span>](midl-compiler.md)
-   [<span data-ttu-id="6b30b-114">Mktyplib.exe</span><span class="sxs-lookup"><span data-stu-id="6b30b-114">MkTypLib</span></span>](mktyplib-command-line-tool.md)

## <a name="visual-basic"></a><span data-ttu-id="6b30b-115">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6b30b-115">Visual Basic</span></span>

-   [<span data-ttu-id="6b30b-116">Visual Basic 物件瀏覽器</span><span class="sxs-lookup"><span data-stu-id="6b30b-116">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="java"></a><span data-ttu-id="6b30b-117">Java</span><span class="sxs-lookup"><span data-stu-id="6b30b-117">Java</span></span>

-   [<span data-ttu-id="6b30b-118">JActiveX</span><span class="sxs-lookup"><span data-stu-id="6b30b-118">JActiveX</span></span>](jactivex-command-line-tool.md)
-   [<span data-ttu-id="6b30b-119">JAVA 類型程式庫嚮導</span><span class="sxs-lookup"><span data-stu-id="6b30b-119">Java Type Library Wizard</span></span>](java-type-library-wizard.md)
-   [<span data-ttu-id="6b30b-120">JAVATLB</span><span class="sxs-lookup"><span data-stu-id="6b30b-120">JavaTLB</span></span>](javatlb-command-line-tool.md)

<span data-ttu-id="6b30b-121">如需這些工具如何與型別程式庫互動的總覽，請參閱 [開發人員工具如何使用類型庫](how-developer-tools-use-type-libraries.md)。</span><span class="sxs-lookup"><span data-stu-id="6b30b-121">For an overview of how these tools interact with type libraries, see [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

 

 




