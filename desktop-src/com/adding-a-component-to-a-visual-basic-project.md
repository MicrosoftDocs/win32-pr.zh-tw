---
title: 將元件新增至 Visual Basic 專案
description: 將元件新增至 Visual Basic 專案
ms.assetid: 7e78853a-b134-46d7-a230-3ee8d80d05c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd64b8367b33590b972adc2439af3a2479ee920e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300572"
---
# <a name="adding-a-component-to-a-visual-basic-project"></a><span data-ttu-id="8bee9-103">將元件新增至 Visual Basic 專案</span><span class="sxs-lookup"><span data-stu-id="8bee9-103">Adding a Component to a Visual Basic Project</span></span>

<span data-ttu-id="8bee9-104">下列程式描述如何將 COM 物件做為元件加入至 Visual Basic 專案。</span><span class="sxs-lookup"><span data-stu-id="8bee9-104">The following procedure describes how to add a COM object as a component to a Visual Basic project.</span></span> <span data-ttu-id="8bee9-105">然後，您的應用程式可以使用該物件的類別。</span><span class="sxs-lookup"><span data-stu-id="8bee9-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="8bee9-106">將控制項加入為元件會公開 Visual Basic 的擴充項屬性和方法，如同它們是控制項的一部分一樣。</span><span class="sxs-lookup"><span data-stu-id="8bee9-106">Adding a control as a component exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span> <span data-ttu-id="8bee9-107">相反地，當您將物件加入為參考時，您只能使用控制項所提供的類型程式庫，或「原始」類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="8bee9-107">In contrast, when you add an object as a reference you can only use the type library provided by the control, or the "raw" type library.</span></span>

<span data-ttu-id="8bee9-108">**將控制項插入 Visual Basic 專案中**</span><span class="sxs-lookup"><span data-stu-id="8bee9-108">**To insert a control into a Visual Basic project**</span></span>

1.  <span data-ttu-id="8bee9-109">從 [專案] 功能表中，按一下 [元件]。</span><span class="sxs-lookup"><span data-stu-id="8bee9-109">On the **Project** menu, click **Components**.</span></span>
2.  <span data-ttu-id="8bee9-110">按一下以選取您要新增之元件旁的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="8bee9-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="8bee9-111">如果未列出元件，請使用 **[流覽]** 找出 .dll 或 .ocx 檔。</span><span class="sxs-lookup"><span data-stu-id="8bee9-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="8bee9-112">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="8bee9-112">Click **OK**.</span></span>

<span data-ttu-id="8bee9-113">元件現在是專案的一部分，而且會出現在 [物件] 工具列中。</span><span class="sxs-lookup"><span data-stu-id="8bee9-113">The component is now part of the project and appears in the object toolbar.</span></span> <span data-ttu-id="8bee9-114">您的應用程式可以從工具列拖曳控制項，然後將它放到表單或對話方塊中，以建立控制項的實例。</span><span class="sxs-lookup"><span data-stu-id="8bee9-114">Your application can create instances of the control by dragging the control from the toolbar and dropping it onto a form or dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bee9-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="8bee9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bee9-116">加入 Visual Basic 專案的參考</span><span class="sxs-lookup"><span data-stu-id="8bee9-116">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="8bee9-117">翻譯為 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8bee9-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




