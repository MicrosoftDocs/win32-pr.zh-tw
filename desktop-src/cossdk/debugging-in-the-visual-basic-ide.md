---
description: 使用 Microsoft Visual Basic 整合式開發環境 (IDE) 進行偵錯工具，可讓 Visual Basic 開發人員存取熟悉的工具和易用的工具。
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Visual Basic IDE 中的調試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385896"
---
# <a name="debugging-in-the-visual-basic-ide"></a><span data-ttu-id="ba2d2-103">Visual Basic IDE 中的調試</span><span class="sxs-lookup"><span data-stu-id="ba2d2-103">Debugging in the Visual Basic IDE</span></span>

<span data-ttu-id="ba2d2-104">使用 Microsoft Visual Basic 整合式開發環境 (IDE) 進行偵錯工具，可讓 Visual Basic 開發人員存取熟悉的工具和易用的工具。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-104">Using the Microsoft Visual Basic integrated development environment (IDE) for debugging gives Visual Basic developers access to familiar tools and ease-of-use.</span></span> <span data-ttu-id="ba2d2-105">雖然許多元件最終需要使用 Microsoft Visual C++ 環境進行更完整的調試，但是有一項策略可能會先使用 Visual Basic 盡可能地進行最多的功能偵測。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-105">While many components will eventually need to be more fully debugged using the Microsoft Visual C++ environment, one strategy might be to first debug as much functionality as possible with Visual Basic.</span></span> <span data-ttu-id="ba2d2-106">例如，您可能會想要使用 Visual Basic IDE，以在您尚未進行多執行緒處理、元件追蹤、遠端呼叫或進程隔離時，于 COM + 內進行的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-106">For example, you might want to use the Visual Basic IDE for debugging within COM+ when you aren't yet debugging multithreading, component tracking, remote calls, or process isolation.</span></span>

<span data-ttu-id="ba2d2-107">一般來說，當您使用 Visual Basic 環境進行偵錯工具時，您必須先編譯專案，並將 DLL 加入至 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-107">In general, when using the Visual Basic environment for debugging, you first compile the project and add the DLL to a COM+ application.</span></span> <span data-ttu-id="ba2d2-108">然後，您可以設定專案的二進位相容性、參考您所建立的 DLL，然後啟動專案開始進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-108">Then you set binary compatibility for the project, referencing the DLL you made, and start the project to begin debugging.</span></span>

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a><span data-ttu-id="ba2d2-109">在 Visual Basic 環境中進行偵錯工具的一般指導方針</span><span class="sxs-lookup"><span data-stu-id="ba2d2-109">General Guidelines for Debugging in the Visual Basic Environment</span></span>

-   <span data-ttu-id="ba2d2-110">當您使用 Visual Basic 進行偵錯工具時，COM + 會將 Visual Basic 元件視為屬於程式庫應用程式，即使元件已註冊為屬於伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-110">While you are debugging using Visual Basic, COM+ treats the Visual Basic components as if they belong to a library application, even if the components are registered as belonging to a server application.</span></span> <span data-ttu-id="ba2d2-111">因為它是以程式庫應用程式的形式執行，所以 [元件服務] 系統管理工具中的元件圖示不會在元件進行調試時旋轉。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-111">Because it runs as a library application, the component icons in the Component Services administrative tool do not spin as the components are debugged.</span></span>
-   <span data-ttu-id="ba2d2-112">如果您在偵錯工具期間變更元件的交易屬性，或變更需要 Visual Basic 產生新 CLSID 或 ProgID 的原始程式碼，請務必刪除並重新安裝包含該元件的 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-112">If you change transaction attributes on a component during debugging or make a source code change that requires Visual Basic to generate a new CLSID or ProgID, be sure to delete and reinstall the COM+ application containing the component.</span></span> <span data-ttu-id="ba2d2-113">如果您已設定元件的二進位相容性，系統會警告您已發生變更。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-113">If you have set binary compatibility for the component, you will be warned that changes have occurred.</span></span>

## <a name="notes-on-debugging-within-a-com-application"></a><span data-ttu-id="ba2d2-114">COM + 應用程式內的偵錯工具注意事項</span><span class="sxs-lookup"><span data-stu-id="ba2d2-114">Notes on Debugging Within a COM+ Application</span></span>

-   <span data-ttu-id="ba2d2-115">如果您在元件介面、類別名稱、專案名稱、交易式支援或其他設定的 Visual Basic IDE 中進行變更，[元件服務] explorer 中的設定資料與在 Visual Basic 偵錯工具中執行的實際設定之間可能不相符。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-115">If you make changes in the Visual Basic IDE in your component's interfaces, class names, project names, transactional support or other settings, there may be mismatches between the configuration data in the Component Services explorer and the actual configuration running in the Visual Basic debugger.</span></span>
-   <span data-ttu-id="ba2d2-116">當您在應用程式中對元件進行偵錯工具時，請勿匯出 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-116">Do not export a COM+ application while you are debugging a component in the application.</span></span> <span data-ttu-id="ba2d2-117">COM + 會將 Visual Basic 開發環境視為元件。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-117">COM+ will treat the Visual Basic development environment as the component.</span></span>
-   <span data-ttu-id="ba2d2-118">如果您在偵錯工具外部執行元件，然後決定開始進行偵錯工具，則當您在偵錯工具中啟動元件的實例時，該元件的實例可能仍在 COM + 中執行。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-118">If you are running a component outside the debugger and then decide to begin debugging, an instance of the component may still be running in COM+ when you start it in the debugger.</span></span> <span data-ttu-id="ba2d2-119">COM + 會偵測到此狀況，並嘗試以無訊息方式關閉它所控制的實例。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-119">COM+ will detect this condition and attempt to silently shut down the instance it controls.</span></span> <span data-ttu-id="ba2d2-120">若要避免這個問題，請先從 [元件服務] 系統管理工具移除元件，再開始進行調試。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-120">To avoid this problem, remove the component from the Component Services administrative tool before you begin debugging.</span></span>

<span data-ttu-id="ba2d2-121">**使用 Visual Basic 環境進行調試**</span><span class="sxs-lookup"><span data-stu-id="ba2d2-121">**To debug using the Visual Basic environment**</span></span>

1.  <span data-ttu-id="ba2d2-122">在 Visual Basic 中開啟元件專案。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-122">Open the component project in Visual Basic.</span></span>

2.  <span data-ttu-id="ba2d2-123">編譯您的元件，然後將專案中的二進位相容性設定為已編譯的元件。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-123">Compile your component, and then set binary compatibility in your project to the compiled component.</span></span>

3.  <span data-ttu-id="ba2d2-124">將 MTSTransactionMode 屬性設定為 0-NotAnMTSObject 以外的值。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-124">Set the MTSTransactionMode property to a value other than 0 - NotAnMTSObject.</span></span> <span data-ttu-id="ba2d2-125">當您啟動專案時，此設定會提示 Visual Basic 在 COM + 內啟動您的元件。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-125">When you start the project, this setting prompts Visual Basic to activate your component within COM+.</span></span>

4.  <span data-ttu-id="ba2d2-126">從 [ **專案** ] 功能表按一下 [ **屬性**]，然後在 [ **調試** 程式] 索引標籤上輸入啟動程式。啟動程式是呼叫此元件的用戶端可執行檔。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-126">From the **Project** menu, click **Properties**, and then enter the start program on the **Debugging** tab. The start program is the client executable that calls this component.</span></span>

    > [!Note]  
    > <span data-ttu-id="ba2d2-127">啟動程式必須在您要進行調試的元件的本機上。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-127">The start program must be local to the component you are debugging.</span></span>

     

5.  <span data-ttu-id="ba2d2-128">按 F5 鍵開始對元件進行調試。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-128">Press the F5 key to begin debugging the component.</span></span>

<span data-ttu-id="ba2d2-129">按下 F5 之後，Visual Basic 會啟動用戶端應用程式，並在 [偵測] 模式中執行該元件。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-129">After you press F5, Visual Basic launches the client application and runs the component in debug mode.</span></span> <span data-ttu-id="ba2d2-130">您可以將中斷點放置在元件的程式碼中，並在變數上設定監看式。</span><span class="sxs-lookup"><span data-stu-id="ba2d2-130">You can place breakpoints in the component's code and set watches on variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba2d2-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba2d2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba2d2-132">COM + Visual Basic 支援與 MTS 對比</span><span class="sxs-lookup"><span data-stu-id="ba2d2-132">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="ba2d2-133">已編譯的 Visual Basic 元件的調試</span><span class="sxs-lookup"><span data-stu-id="ba2d2-133">Debugging Compiled Visual Basic Components</span></span>](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



