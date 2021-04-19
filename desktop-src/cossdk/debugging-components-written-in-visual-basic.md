---
description: 調試 Visual Basic 中撰寫的元件
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: 調試 Visual Basic 中撰寫的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980929"
---
# <a name="debugging-components-written-in-visual-basic"></a><span data-ttu-id="9c643-103">調試 Visual Basic 中撰寫的元件</span><span class="sxs-lookup"><span data-stu-id="9c643-103">Debugging Components Written in Visual Basic</span></span>

<span data-ttu-id="9c643-104">您可以使用 Microsoft Visual Basic 6.0 開發環境，在某些情況下進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="9c643-104">You can use the Microsoft Visual Basic 6.0 development environment for debugging within certain scenarios.</span></span> <span data-ttu-id="9c643-105">使用 Visual Basic 進行偵錯工具，可讓您存取 Visual Basic 程式設計人員熟悉的工具。</span><span class="sxs-lookup"><span data-stu-id="9c643-105">Using Visual Basic for debugging allows access to tools familiar to Visual Basic programmers.</span></span> <span data-ttu-id="9c643-106">另一方面，因為在 Visual Basic 環境的程式中執行 Visual Basic 元件的偵錯工具時，您可能需要在使用 Microsoft Visual C++ 開發環境來編譯元件之後，對元件進行 debug。</span><span class="sxs-lookup"><span data-stu-id="9c643-106">On the other hand, because during debugging Visual Basic components run within the Visual Basic environment's process, it may be necessary to debug your component after it has been compiled by using the Microsoft Visual C++ development environment.</span></span>

<span data-ttu-id="9c643-107">如需在 Visual Basic 整合式開發環境內進行偵錯工具 (IDE) 的詳細資訊，請參閱 [VISUAL BASIC ide 中的調試](debugging-in-the-visual-basic-ide.md)程式。</span><span class="sxs-lookup"><span data-stu-id="9c643-107">For more information about debugging within the Visual Basic integrated development environment (IDE), see [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md).</span></span> <span data-ttu-id="9c643-108">如需使用 Visual C++ 開發環境來編譯 Visual Basic 元件的詳細資訊，請參閱 [Visual Basic 元件的調試](debugging-compiled-visual-basic-components.md)程式。</span><span class="sxs-lookup"><span data-stu-id="9c643-108">For more on debugging Visual Basic components after they're compiled using the Visual C++ development environment, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

<span data-ttu-id="9c643-109">此外，使用 Visual Basic 環境來對具有 MTS 的元件進行偵錯工具的幾項限制，已針對 COM + 進行解析。</span><span class="sxs-lookup"><span data-stu-id="9c643-109">Also, several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="9c643-110">如需詳細資訊，請參閱 [Com + Visual Basic 與 MTS 對比的支援](com--visual-basic-debugging-support-contrasted-with-mts.md)。</span><span class="sxs-lookup"><span data-stu-id="9c643-110">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

> [!Note]  
> <span data-ttu-id="9c643-111">如果您已在與 COM + 相同的電腦上使用 Visual Basic，您可能已注意到 Visual Basic 環境中可用的元件服務增益集。</span><span class="sxs-lookup"><span data-stu-id="9c643-111">If you have already used Visual Basic on the same computer as COM+, you may have noticed the Component Services add-in available in the Visual Basic environment.</span></span> <span data-ttu-id="9c643-112">這項功能原本是在 MTS 中，每次您重新編譯 COM + 應用程式中的元件時，都必須更新登錄。</span><span class="sxs-lookup"><span data-stu-id="9c643-112">Originally in MTS, this feature was designed to update the registry each time you recompiled a component in a COM+ application.</span></span> <span data-ttu-id="9c643-113">不過，由於 Microsoft Windows 登錄和 COM + 註冊資料庫的互動本質，某些設定可能不會完全更新。</span><span class="sxs-lookup"><span data-stu-id="9c643-113">However, given the nature of the interaction of the Microsoft Windows Registry and the COM+ registration database, some settings may not be completely updated.</span></span> <span data-ttu-id="9c643-114">因此，您應該在重新編譯之後移除並重新安裝元件，以更新設定，而不是使用此增益集提供的命令。</span><span class="sxs-lookup"><span data-stu-id="9c643-114">Therefore, instead of using the commands available with this add-in, you should remove and reinstall your components to update settings after recompiling.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9c643-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c643-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c643-116">調試 Visual C++ 中撰寫的元件</span><span class="sxs-lookup"><span data-stu-id="9c643-116">Debugging Components Written in Visual C++</span></span>](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



