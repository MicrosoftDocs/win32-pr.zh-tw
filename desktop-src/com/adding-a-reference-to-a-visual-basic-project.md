---
title: 加入 Visual Basic 專案的參考
description: 加入 Visual Basic 專案的參考
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300571"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a><span data-ttu-id="1918c-103">加入 Visual Basic 專案的參考</span><span class="sxs-lookup"><span data-stu-id="1918c-103">Adding a Reference to a Visual Basic Project</span></span>

<span data-ttu-id="1918c-104">下列程式描述如何將 COM 物件的參考加入至 Visual Basic 專案。</span><span class="sxs-lookup"><span data-stu-id="1918c-104">The following procedure describes how to add a reference to a COM object to a Visual Basic project.</span></span> <span data-ttu-id="1918c-105">然後，您的應用程式可以使用該物件的類別。</span><span class="sxs-lookup"><span data-stu-id="1918c-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="1918c-106">當您加入物件做為參考時，您只能使用控制項所提供的類型程式庫，或使用「原始」類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="1918c-106">When you add an object as a reference, you can only use the type library provided by the control, or the "raw" type library.</span></span> <span data-ttu-id="1918c-107">相反地，將控制項加入為元件也會公開 Visual Basic 的擴充項屬性和方法，如同它們是控制項的一部分一樣。</span><span class="sxs-lookup"><span data-stu-id="1918c-107">In contrast, adding a control as a component also exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span>

<span data-ttu-id="1918c-108">**若要建立元件的 Visual Basic 參考**</span><span class="sxs-lookup"><span data-stu-id="1918c-108">**To make a Visual Basic reference to a component**</span></span>

1.  <span data-ttu-id="1918c-109">從 [專案] 功能表中，按一下 [參考]。</span><span class="sxs-lookup"><span data-stu-id="1918c-109">On the **Project** menu, click **References**.</span></span>
2.  <span data-ttu-id="1918c-110">按一下以選取您要新增之元件旁的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="1918c-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="1918c-111">如果未列出元件，請使用 **[流覽]** 找出 .dll 或 .ocx 檔。</span><span class="sxs-lookup"><span data-stu-id="1918c-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="1918c-112">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="1918c-112">Click **OK**.</span></span>

<span data-ttu-id="1918c-113">元件現在是專案的一部分。</span><span class="sxs-lookup"><span data-stu-id="1918c-113">The component is now part of the project.</span></span> <span data-ttu-id="1918c-114">您的應用程式可以使用 **New** 關鍵字來建立類別實例。</span><span class="sxs-lookup"><span data-stu-id="1918c-114">Your application can create class instances using the **New** keyword.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1918c-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="1918c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1918c-116">將元件新增至 Visual Basic 專案</span><span class="sxs-lookup"><span data-stu-id="1918c-116">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="1918c-117">翻譯為 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1918c-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




