---
description: COM + Visual Basic 支援與 MTS 對比
ms.assetid: aa012f88-1f88-4c7f-b774-82b9e29da5e9
title: COM + Visual Basic 支援與 MTS 對比
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038b29bbc6fbe5c8375f91f0006b85940f00b944
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971139"
---
# <a name="com-visual-basic-debugging-support-contrasted-with-mts"></a><span data-ttu-id="d31a1-103">COM + Visual Basic 支援與 MTS 對比</span><span class="sxs-lookup"><span data-stu-id="d31a1-103">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>

<span data-ttu-id="d31a1-104">COM + 移除或減少使用 Microsoft Visual Basic 6.0 和 MTS 進行偵錯工具的幾項限制。</span><span class="sxs-lookup"><span data-stu-id="d31a1-104">COM+ removes or reduces several limitations of debugging with Microsoft Visual Basic 6.0 and MTS.</span></span> <span data-ttu-id="d31a1-105">下列清單摘要說明 COM + 所能預期的變更：</span><span class="sxs-lookup"><span data-stu-id="d31a1-105">The following list summarizes changes you can expect with COM+:</span></span>

-   <span data-ttu-id="d31a1-106">多個元件的偵錯工具：在 COM + 中，您可以在其中一個 IDE 實例中執行的用戶端呼叫任何數目的 Dll，以做為專案群組。</span><span class="sxs-lookup"><span data-stu-id="d31a1-106">Debugging multiple components—In COM+, you can debug scenarios in which a client running in one instance of the IDE makes calls to any number of DLLs running in another as a project group.</span></span> <span data-ttu-id="d31a1-107">群組 DLL 專案中的物件可以任意地呼叫彼此，並視需要將內容流動。</span><span class="sxs-lookup"><span data-stu-id="d31a1-107">The objects in the grouped DLL projects can call each other arbitrarily, flowing context as needed.</span></span> <span data-ttu-id="d31a1-108">當然，這也適用于當 Dll 和用戶端位於相同的 IDE 實例中的相同專案群組時。</span><span class="sxs-lookup"><span data-stu-id="d31a1-108">Of course, this also works when the DLLs and the client are in the same project group in the same instance of the IDE.</span></span>

-   <span data-ttu-id="d31a1-109">\_使用 com + 來偵測類別 initialize 和 class \_ terminate 事件的限制：您可以使用 com + 將程式碼放在 \_ \_ com + 應用程式元件的類別 initialize 和 class terminate 事件中，即使該程式碼嘗試存取物件或其對應的內容物件。</span><span class="sxs-lookup"><span data-stu-id="d31a1-109">Debugging Limitations on Class\_Initialize and Class\_Terminate Events—With COM+, you can put code in the Class\_Initialize and Class\_Terminate events of a COM+ application component even if that code attempts to access the object or its corresponding context object.</span></span> <span data-ttu-id="d31a1-110">您可以在該處設定中斷點，並使用監看式。</span><span class="sxs-lookup"><span data-stu-id="d31a1-110">You can set breakpoints there and use watches.</span></span> <span data-ttu-id="d31a1-111">您也可以在類別終止事件中設定中斷點 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d31a1-111">You can also set breakpoints in the Class\_Terminate event.</span></span>

    <span data-ttu-id="d31a1-112">雖然不再需要作為因應措施，但如果您需要在啟動和關閉元件期間執行程式碼，您仍然可以執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) 介面並 [**使用其啟動**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) 和 [**停用**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) 方法。</span><span class="sxs-lookup"><span data-stu-id="d31a1-112">Although it is no longer needed as a workaround, you can still implement the [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) interface and use its [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) and [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) methods if you need to execute code during startup and shutdown of your component.</span></span> <span data-ttu-id="d31a1-113">您現在也可以在程式碼中，將中斷點放在 **停用** 或 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) 方法的程式碼中。</span><span class="sxs-lookup"><span data-stu-id="d31a1-113">You can also now put breakpoints in code for the **Deactivate** or [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) methods.</span></span>

-   <span data-ttu-id="d31a1-114">監看 MTS 物件：使用 COM +，您可以為 COM + 所傳回的物件變數加入監看式，包括 [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)、 [**GetObjectCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)和 [**IObjectCoNtext：： CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) 方法的傳回值。</span><span class="sxs-lookup"><span data-stu-id="d31a1-114">Watching MTS Objects—With COM+, you can add watches for object variables returned by COM+, including return values from the [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef), [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext), and [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) methods.</span></span>

-   <span data-ttu-id="d31a1-115">當元件失敗時，系統會增加穩定性-在 COM + 中，元件失敗不會再停止 Visual Basic (，這會在與所) 的調試元件相同的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="d31a1-115">Increased stability when components fail—In COM+, a component failure will no longer always stop Visual Basic (which runs in the same process as the debugged component).</span></span> <span data-ttu-id="d31a1-116">例如，支援即時 (JIT) 重新開機失敗現在可讓您在進行偵錯工具時查看物件內容。</span><span class="sxs-lookup"><span data-stu-id="d31a1-116">For example, support for just-in-time (JIT) reactivation failures now allows you to look at the object context while debugging.</span></span>

-   <span data-ttu-id="d31a1-117">偵錯工具可能會重新啟用 COM + 所發行的物件—如同使用 MTS 一樣，Visual Basic 6.0 可能會在您透過用戶端進行單一步驟的偵錯工具時，重新啟用 COM + 物件。</span><span class="sxs-lookup"><span data-stu-id="d31a1-117">Debugger may reactivate objects released by COM+—As with MTS, Visual Basic 6.0 may reactivate COM+ objects while you are debugging single-step through a client.</span></span> <span data-ttu-id="d31a1-118">基於 Visual Basic 6.0 探索物件相關資訊的方式，這是預期的行為。</span><span class="sxs-lookup"><span data-stu-id="d31a1-118">Because of the way that Visual Basic 6.0 discovers information about objects, this is expected behavior.</span></span> <span data-ttu-id="d31a1-119">例如，請參考下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="d31a1-119">For example, consider the following code:</span></span>

    ``` syntax
    Dim obj As Object
    Set obj = CreateObject("MyApp.MyClass")
    obj.Test  'Call the user-defined subroutine named Test.
    Set obj = Nothing
    ```

    <span data-ttu-id="d31a1-120">如果為 obj。測試方法呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)，com + 立即釋出記憶體中的 obj，但是 obj 尚未設定為 Nothing。</span><span class="sxs-lookup"><span data-stu-id="d31a1-120">If the obj.Test method calls [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), COM+ immediately frees obj from memory, but obj has not yet been set to Nothing.</span></span> <span data-ttu-id="d31a1-121">當是 obj 時。測試會傳回，Visual Basic 偵錯工具會針對 [**IProvideClassInfo**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo)介面呼叫 obj 上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="d31a1-121">When obj.Test returns, the Visual Basic debugger calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on obj for the [**IProvideClassInfo**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo) interface.</span></span> <span data-ttu-id="d31a1-122">與 obj 相關聯的內容包裝函式會建立新的 MyApp 實例，以服務 **QueryInterface** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="d31a1-122">The context wrapper associated with obj creates a new instance of MyApp.MyClass to service the **QueryInterface** call.</span></span> <span data-ttu-id="d31a1-123">如此一來，您就會在偵錯工具中的 obj 之後看到未初始化的物件。已傳回測試。</span><span class="sxs-lookup"><span data-stu-id="d31a1-123">As a result, you will see this uninitialized object in the debugger after obj.Test has returned.</span></span> <span data-ttu-id="d31a1-124">此物件只會出現在偵錯工具中，並由後續指令移除，以將 obj 設為 Nothing。</span><span class="sxs-lookup"><span data-stu-id="d31a1-124">This object appears only in the debugger and is removed by the subsequent instruction to set obj to Nothing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d31a1-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="d31a1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d31a1-126">已編譯的 Visual Basic 元件的調試</span><span class="sxs-lookup"><span data-stu-id="d31a1-126">Debugging Compiled Visual Basic Components</span></span>](debugging-compiled-visual-basic-components.md)
</dt> <dt>

[<span data-ttu-id="d31a1-127">Visual Basic IDE 中的調試</span><span class="sxs-lookup"><span data-stu-id="d31a1-127">Debugging in the Visual Basic IDE</span></span>](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 
