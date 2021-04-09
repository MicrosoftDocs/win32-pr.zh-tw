---
description: COM + 應用程式的調試技術取決於您選擇用來撰寫元件的語言。
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: 偵錯工具 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db096ceb525cd988afa55e49cc88fda0ddf52549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689111"
---
# <a name="debugging-com-applications"></a><span data-ttu-id="dfa9e-103">偵錯工具 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="dfa9e-103">Debugging COM+ Applications</span></span>

<span data-ttu-id="dfa9e-104">COM + 應用程式的調試技術取決於您選擇用來撰寫元件的語言。</span><span class="sxs-lookup"><span data-stu-id="dfa9e-104">Debugging techniques for COM+ applications depend on the language in which you choose to write your component.</span></span>

<span data-ttu-id="dfa9e-105">如果您在 Microsoft Visual C++ 中撰寫程式碼，您可以在 c + + 中啟動偵錯工具，或使用遠端用戶端，透過使用 OLE remote procedure control (RPC) 和即時 (JIT) 偵錯工具來進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="dfa9e-105">If you code in Microsoft Visual C++, you can launch the debugger in C++ or, with a remote client, you can debug by using OLE remote procedure control (RPC) and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="dfa9e-106">您一律可以使用 [元件服務] 系統管理工具，透過 [COM + 應用程式 **屬性**] 對話方塊之 [ **Advanced** ] 索引標籤上的 [com +**啟動于偵錯工具**] 設定來對元件進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="dfa9e-106">You can always use the Component Services administrative tool to debug your component with the COM+ **Launch in debugger** setting on the **Advanced** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="dfa9e-107">如需有關以 c + + 撰寫程式碼之元件的詳細資訊，請參閱 [以 Visual C++ 撰寫的偵錯工具元件](debugging-components-written-in-visual-c--.md)。</span><span class="sxs-lookup"><span data-stu-id="dfa9e-107">For more information on debugging components coded in C++, see [Debugging Components Written in Visual C++](debugging-components-written-in-visual-c--.md).</span></span>

<span data-ttu-id="dfa9e-108">除非您目前正在進行多執行緒處理、元件追蹤、遠端呼叫或進程隔離，否則您可以使用 Microsoft Visual Basic 環境進行調試。</span><span class="sxs-lookup"><span data-stu-id="dfa9e-108">Unless you are currently debugging multithreading, component tracking, remote calls, or process isolation, you can use the Microsoft Visual Basic environment for debugging purposes.</span></span> <span data-ttu-id="dfa9e-109">[以 Visual Basic 撰寫的調試](debugging-components-written-in-visual-basic.md) 程式描述 Visual Basic 環境內的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="dfa9e-109">[Debugging Components Written in Visual Basic](debugging-components-written-in-visual-basic.md) describes the debugging process within a Visual Basic environment.</span></span>

<span data-ttu-id="dfa9e-110">[VISUAL BASIC ide 中](debugging-in-the-visual-basic-ide.md)的主題偵錯工具，提供有關在整合式開發環境 (IDE) 中進行偵錯工具的指導方針、秘訣和程式的一般總覽。</span><span class="sxs-lookup"><span data-stu-id="dfa9e-110">The topic [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md) provides a general overview with guidelines, tips and a procedure on debugging in the integrated development environment (IDE).</span></span>

<span data-ttu-id="dfa9e-111">若要查看有關偵錯工具高階進程的詳細資訊，請參閱 [Visual Basic 元件的調試](debugging-compiled-visual-basic-components.md)程式。</span><span class="sxs-lookup"><span data-stu-id="dfa9e-111">To view more information about debugging advanced processes, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

> [!Note]  
> <span data-ttu-id="dfa9e-112">針對 COM +，使用 Visual Basic 環境來對具有 MTS 的元件進行偵錯工具的幾項限制已解決。</span><span class="sxs-lookup"><span data-stu-id="dfa9e-112">Several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="dfa9e-113">如需詳細資訊，請參閱 [Com + Visual Basic 與 MTS 對比的支援](com--visual-basic-debugging-support-contrasted-with-mts.md)。</span><span class="sxs-lookup"><span data-stu-id="dfa9e-113">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dfa9e-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="dfa9e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfa9e-115">在 COM + 中處理錯誤</span><span class="sxs-lookup"><span data-stu-id="dfa9e-115">Handling Errors in COM+</span></span>](handling-errors-in-com-.md)
</dt> </dl>

 

 



