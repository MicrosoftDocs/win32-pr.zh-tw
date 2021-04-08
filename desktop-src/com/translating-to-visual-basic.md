---
title: 翻譯為 Visual Basic
description: 翻譯為 Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840284"
---
# <a name="translating-to-visual-basic"></a><span data-ttu-id="c3192-103">翻譯為 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c3192-103">Translating to Visual Basic</span></span>

<span data-ttu-id="c3192-104">您可以將 COM 物件新增至 Visual Basic 專案中，做為參考或元件。</span><span class="sxs-lookup"><span data-stu-id="c3192-104">You can add a COM object to your Visual Basic project either as a reference or a component.</span></span> <span data-ttu-id="c3192-105">將物件加入至專案之後，您的應用程式就可以存取其類別和介面。</span><span class="sxs-lookup"><span data-stu-id="c3192-105">Once the object is added to your project, your application can access its classes and interfaces.</span></span> <span data-ttu-id="c3192-106">然後，您可以使用 Visual Basic 的物件瀏覽器，以 Visual Basic 語法來查看物件的型別程式庫資訊。</span><span class="sxs-lookup"><span data-stu-id="c3192-106">You can then use the Visual Basic Object Browser to view the object's type library information in Visual Basic syntax.</span></span>

<span data-ttu-id="c3192-107">通常會將控制項新增至專案做為元件，並將 noncontrols 新增為參考。</span><span class="sxs-lookup"><span data-stu-id="c3192-107">Typically, controls are added to a project as a components and noncontrols are added as references.</span></span> <span data-ttu-id="c3192-108">當 COM 物件加入為元件時，它會出現在 Visual Basic 的 [工具箱] 中。</span><span class="sxs-lookup"><span data-stu-id="c3192-108">When a COM object is added as a component, it appears in the Visual Basic toolbox.</span></span> <span data-ttu-id="c3192-109">將物件圖示從 [工具箱] 拖曳至 Visual Basic 表單或其他類型的容器，即可建立該物件的新實例。</span><span class="sxs-lookup"><span data-stu-id="c3192-109">New instances of that object are created by dragging the object icon from the toolbox onto a Visual Basic form or other type of container.</span></span> <span data-ttu-id="c3192-110">加入做為參考的 COM 物件的新實例會使用 **new** 關鍵字來建立。</span><span class="sxs-lookup"><span data-stu-id="c3192-110">New instances of COM objects added as references are created using the **new** keyword.</span></span>

<span data-ttu-id="c3192-111">使用類別做為參考與元件的差異很微妙，但很重要。</span><span class="sxs-lookup"><span data-stu-id="c3192-111">The distinction between using a class as a reference versus a component is subtle but important.</span></span> <span data-ttu-id="c3192-112">當您加入物件做為參考時，您只能使用控制項所提供的類型程式庫，或使用「原始」類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="c3192-112">When you add an object as a reference, you can use only the type library that the control provides, or the "raw" type library.</span></span>

<span data-ttu-id="c3192-113">如果您將控制項加入為元件，Visual Basic 會合並以控制項類型程式庫內嵌控制項的表單的擴充項屬性和方法，藉此提供類型程式庫的包裝擴充版本。</span><span class="sxs-lookup"><span data-stu-id="c3192-113">If you add a control as a component, Visual Basic merges the extender properties and methods of the form in which the control is embedded with the control's type library, thus providing a wrapped, extended version of the type library.</span></span> <span data-ttu-id="c3192-114">使用這個版本的類型程式庫時，您可以使用擴充項屬性（例如 Top 和 Left），如同它們是控制項的一部分，而不是控制項的容器。</span><span class="sxs-lookup"><span data-stu-id="c3192-114">With this version of the type library, you can use extender properties such as Top and Left as if they were part of the control, instead of the control's container.</span></span>

<span data-ttu-id="c3192-115">Visual Basic 目前不支援單一 .dll 檔案內建的多個類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="c3192-115">Visual Basic does not currently support multiple type libraries built into a single .dll file.</span></span> <span data-ttu-id="c3192-116">如果您遇到合併多個類型程式庫的 DLL，您應該從提供物件的來源取得類型程式庫的獨立複本，以便搭配 Visual Basic 使用物件。</span><span class="sxs-lookup"><span data-stu-id="c3192-116">If you run into a DLL that incorporates multiple type libraries, you should get stand-alone copies of the type libraries from the source that supplied the object in order to use the object with Visual Basic.</span></span>

<span data-ttu-id="c3192-117">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="c3192-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="c3192-118">從 c + + 翻譯為 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c3192-118">Translating to Visual Basic from C++</span></span>](translating-to-visual-basic-from-c--.md)
-   [<span data-ttu-id="c3192-119">從 JAVA 轉譯為 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c3192-119">Translating to Visual Basic from Java</span></span>](translating-to-visual-basic-from-java.md)
-   [<span data-ttu-id="c3192-120">將元件新增至 Visual Basic 專案</span><span class="sxs-lookup"><span data-stu-id="c3192-120">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
-   [<span data-ttu-id="c3192-121">加入 Visual Basic 專案的參考</span><span class="sxs-lookup"><span data-stu-id="c3192-121">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
-   [<span data-ttu-id="c3192-122">Visual Basic 物件瀏覽器</span><span class="sxs-lookup"><span data-stu-id="c3192-122">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="related-topics"></a><span data-ttu-id="c3192-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3192-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3192-124">轉換成 c + +</span><span class="sxs-lookup"><span data-stu-id="c3192-124">Translating to C++</span></span>](translating-to-c--.md)
</dt> <dt>

[<span data-ttu-id="c3192-125">轉換成 JAVA</span><span class="sxs-lookup"><span data-stu-id="c3192-125">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




