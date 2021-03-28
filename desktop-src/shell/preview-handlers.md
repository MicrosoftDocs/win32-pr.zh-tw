---
description: 在選取專案時，會呼叫預覽處理常式，以在視圖的讀取窗格中顯示檔案內容的輕量、豐富、唯讀預覽。 這樣做不會啟動檔案的相關聯應用程式。
ms.assetid: 166a4001-d237-44a4-a457-e320e995639c
title: 預覽處理常式和 Shell 預覽主機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993c6c8e7b15d9bfc24b5dd42352407a3a53c45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973352"
---
# <a name="preview-handlers-and-shell-preview-host"></a><span data-ttu-id="8a2e6-104">預覽處理常式和 Shell 預覽主機</span><span class="sxs-lookup"><span data-stu-id="8a2e6-104">Preview Handlers and Shell Preview Host</span></span>

<span data-ttu-id="8a2e6-105">在選取專案時，會呼叫預覽處理常式，以在視圖的讀取窗格中顯示檔案內容的輕量、豐富、 *唯讀* 預覽。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-105">Preview handlers are called when an item is selected to show a lightweight, rich, *read-only* preview of the file's contents in the view's reading pane.</span></span> <span data-ttu-id="8a2e6-106">這樣做不會啟動檔案的相關聯應用程式。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-106">This is done without launching the file's associated application.</span></span>

<span data-ttu-id="8a2e6-107">本主題將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="8a2e6-107">This topic discusses the following topics:</span></span>

-   [<span data-ttu-id="8a2e6-108">預覽處理常式架構</span><span class="sxs-lookup"><span data-stu-id="8a2e6-108">Preview Handler Architecture</span></span>](#preview-handler-architecture)
-   [<span data-ttu-id="8a2e6-109">伺服器模型選項</span><span class="sxs-lookup"><span data-stu-id="8a2e6-109">Server Model Options</span></span>](#server-model-options)
-   [<span data-ttu-id="8a2e6-110">初始 化</span><span class="sxs-lookup"><span data-stu-id="8a2e6-110">Initialization</span></span>](#initialization)
-   [<span data-ttu-id="8a2e6-111">預覽處理常式資料流程</span><span class="sxs-lookup"><span data-stu-id="8a2e6-111">Preview Handler Data Flow</span></span>](#preview-handler-data-flow)
-   [<span data-ttu-id="8a2e6-112">對預覽處理常式進行偵錯工具</span><span class="sxs-lookup"><span data-stu-id="8a2e6-112">Debugging a Preview Handler</span></span>](#debugging-a-preview-handler)
-   [<span data-ttu-id="8a2e6-113">提供您自己的預覽處理常式流程</span><span class="sxs-lookup"><span data-stu-id="8a2e6-113">Providing Your Own Process for a Preview Handler</span></span>](#providing-your-own-process-for-a-preview-handler)
-   [<span data-ttu-id="8a2e6-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a2e6-114">Related topics</span></span>](#related-topics)

## <a name="preview-handler-architecture"></a><span data-ttu-id="8a2e6-115">預覽處理常式架構</span><span class="sxs-lookup"><span data-stu-id="8a2e6-115">Preview Handler Architecture</span></span>

<span data-ttu-id="8a2e6-116">預覽處理常式是託管應用程式。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-116">A preview handler is a hosted application.</span></span> <span data-ttu-id="8a2e6-117">主機包含 Windows Vista 或 Microsoft Outlook 2007 中的 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-117">Hosts include the Windows Explorer in Windows Vista or Microsoft Outlook 2007.</span></span> <span data-ttu-id="8a2e6-118">主機會將 [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) 實作為預覽處理常式和主機之間的通訊方法。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-118">Hosts implement [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) as a method of communication between the preview handler and the host.</span></span>

<span data-ttu-id="8a2e6-119">預覽處理常式本身會執行這些介面：</span><span class="sxs-lookup"><span data-stu-id="8a2e6-119">The preview handler itself implements these interfaces:</span></span>

-   [<span data-ttu-id="8a2e6-120">**IInitializeWithStream**</span><span class="sxs-lookup"><span data-stu-id="8a2e6-120">**IInitializeWithStream**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="8a2e6-121">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="8a2e6-121">**IObjectWithSite**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [<span data-ttu-id="8a2e6-122">**IOleWindow**</span><span class="sxs-lookup"><span data-stu-id="8a2e6-122">**IOleWindow**</span></span>](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
-   [<span data-ttu-id="8a2e6-123">**IPreviewHandler**</span><span class="sxs-lookup"><span data-stu-id="8a2e6-123">**IPreviewHandler**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
-   <span data-ttu-id="8a2e6-124">[**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (選用) </span><span class="sxs-lookup"><span data-stu-id="8a2e6-124">[**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (Optional)</span></span>

<span data-ttu-id="8a2e6-125">您的處理常式會透過其 [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)來呼叫，它會傳回一個 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標，要求 [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) 物件與主機互動。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-125">Your handler is called through its [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), which returns an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer through which you request an [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) object to interact with the host.</span></span>

## <a name="server-model-options"></a><span data-ttu-id="8a2e6-126">伺服器模型選項</span><span class="sxs-lookup"><span data-stu-id="8a2e6-126">Server Model Options</span></span>

<span data-ttu-id="8a2e6-127">預覽處理常式一律會用盡進程。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-127">Preview handlers always run out of process.</span></span> <span data-ttu-id="8a2e6-128">有兩種方法可以執行這項操作：</span><span class="sxs-lookup"><span data-stu-id="8a2e6-128">There are two methods of implementing this:</span></span>

1.  <span data-ttu-id="8a2e6-129">預覽處理常式可以建立為同進程伺服器，但會透過跨進程的代理主機來執行。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-129">A preview handler can be built as an in-process server but run through an out-of-process surrogate host.</span></span> <span data-ttu-id="8a2e6-130">這是慣用的方法。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-130">This is the preferred method.</span></span> <span data-ttu-id="8a2e6-131">系統會在 Prevhost.exe 檔案中為此提供代理主機。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-131">The system provides a surrogate host for this in the Prevhost.exe file.</span></span> <span data-ttu-id="8a2e6-132">這個方法所建立的預覽處理常式與 Windows XP 上的 Outlook 2007 不相容。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-132">Preview handlers built by this method are not compatible with Outlook 2007 on Windows XP.</span></span> <span data-ttu-id="8a2e6-133">不過，這些相同的處理常式適用于在 Windows Vista 上執行的 Windows 檔案總管和 Outlook 2007。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-133">However, these same handlers will work in Windows Explorer and Outlook 2007 running on Windows Vista.</span></span>
2.  <span data-ttu-id="8a2e6-134">預覽處理常式可以用 (COM) server 的本機組件物件模型來建立。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-134">A preview handler can be built as a local Component Object Model (COM) server.</span></span> <span data-ttu-id="8a2e6-135">不建議您這麼做的原因有好幾種。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-135">This is not recommended for several reasons.</span></span> <span data-ttu-id="8a2e6-136">首先，執行同進程伺服器比較容易。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-136">First, implementation of an in-process server is easier.</span></span> <span data-ttu-id="8a2e6-137">更重要的是，執行為內含式伺服器，可提供更好的控制處理常式物件存留期，以提供更好的清除和效率。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-137">More importantly, implementation as an in-process server provides greater control over the lifetime of the handler object, which allows for better cleanup and efficiency.</span></span>

<span data-ttu-id="8a2e6-138">根據預設，預覽處理常式會基於安全性理由，在低完整性層級 (IL) 進程中執行。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-138">By default, preview handlers run in a low integrity level (IL) process for security reasons.</span></span> <span data-ttu-id="8a2e6-139">您可以藉由在登錄中設定下列值，選擇性地停用做為低 IL 處理常式的執行。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-139">You can optionally disable running as a low IL process by setting the following value in the registry.</span></span> <span data-ttu-id="8a2e6-140">但是，不建議這麼做。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-140">However, it is not recommended to do so.</span></span> <span data-ttu-id="8a2e6-141">系統最終可能會將系統設定為拒絕不是低 IL 的任何處理程式。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-141">Systems could eventually be configured to reject any process that is not low IL.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {YOUR HANDLER'S CLSID}
         DisableLowILProcessIsolation [DWORD] = 1
```

<span data-ttu-id="8a2e6-142">依預設，不同的預覽處理常式會共用相同的進程。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-142">Different preview handlers share the same process by default.</span></span> <span data-ttu-id="8a2e6-143">Prevhost.exe 可以同時執行兩個實例;一個用於以低 IL 進程的形式執行的處理常式，一個用於已退出宣告該行為的處理常式。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-143">Two instances of Prevhost.exe can be running simultaneously; one for handlers running as low IL processes, one for handlers that have opted out of that behavior.</span></span>

## <a name="initialization"></a><span data-ttu-id="8a2e6-144">初始化</span><span class="sxs-lookup"><span data-stu-id="8a2e6-144">Initialization</span></span>

<span data-ttu-id="8a2e6-145">如同縮圖和屬性處理常式，強烈建議您使用資料流程初始化處理常式。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-145">As with thumbnail and property handlers, it is strongly recommended that you initialize your handler with a stream.</span></span> <span data-ttu-id="8a2e6-146">如有必要，您可以透過檔案或專案初始化，但資料流程提供最安全的方式來執行處理常式。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-146">You can initialize through a file or item if necessary, but streams provide the most secure way to implement a handler.</span></span> <span data-ttu-id="8a2e6-147">透過資料流程進行初始化可確保檔案完整性和穩定性，讓執行處理常式的系統成為低 IL 進程，例如保護系統免于緩衝區溢位、限制處理常式可以寫入資訊的位置，以及限制與其他視窗的通訊。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-147">Initialization through a stream ensures file integrity and the stability benefits to the system of running the handler as a low IL process, such as protecting the system from buffer overruns, limiting where a handler can write information, and limiting communication with other windows.</span></span>

<span data-ttu-id="8a2e6-148">如果您必須使用檔案或 Shell 專案來初始化，請儲存檔案路徑或 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)的參考。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-148">If you must initialize with a file or Shell item, store the file path or a reference to the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem).</span></span> <span data-ttu-id="8a2e6-149">在呼叫 [**IPreviewHandler：:D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) 之前，請勿從這些來源讀取資料。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-149">Do not read data from these sources until [**IPreviewHandler::DoPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) is called.</span></span>

<span data-ttu-id="8a2e6-150">一般情況下，初始化不應執行任何繁重的工作，例如撰寫和儲存預覽影像。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-150">In general, initialization should not do any heavy work such as composing and storing a preview image.</span></span> <span data-ttu-id="8a2e6-151">為了達到最佳效率，在呼叫預覽之前，不應執行這類處理。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-151">For optimal efficiency, that sort of processing should not be done until the preview is called for.</span></span>

## <a name="preview-handler-data-flow"></a><span data-ttu-id="8a2e6-152">預覽處理常式資料流程</span><span class="sxs-lookup"><span data-stu-id="8a2e6-152">Preview Handler Data Flow</span></span>

<span data-ttu-id="8a2e6-153">預覽程式中的資料流程會遵循此處顯示的一般路徑。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-153">The data flow in the preview process follows the general path shown here.</span></span> <span data-ttu-id="8a2e6-154">您可以將主機視為 Windows Vista 或 Outlook 2007 中的 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-154">The host can be thought of as Windows Explorer in Windows Vista or Outlook 2007.</span></span>

1.  <span data-ttu-id="8a2e6-155">預覽處理常式已初始化，最好是使用資料流程。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-155">The preview handler is initialized, preferably with a stream.</span></span>
2.  <span data-ttu-id="8a2e6-156">視圖視窗會透過 [**IPreviewHandler：： SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow)從主機傳遞給處理常式。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-156">The view window is passed from the host to the handler through [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow).</span></span>
3.  <span data-ttu-id="8a2e6-157">此時，處理常式應該不會再執行任何動作，直到 [**IPreviewHandler：呼叫:D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) 為止。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-157">At this point, the handler should do nothing more until [**IPreviewHandler::DoPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) is called.</span></span>
4.  <span data-ttu-id="8a2e6-158">預覽會透過呼叫 [**IPreviewHandler：:D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)顯示在 [讀取窗格] 中。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-158">The preview is displayed in the reading pane through a call to [**IPreviewHandler::DoPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview).</span></span>
5.  <span data-ttu-id="8a2e6-159">視窗的大小是透過 [**IPreviewHandler：： SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)來設定。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-159">The size of the window is set through [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).</span></span>
6.  <span data-ttu-id="8a2e6-160">視窗會在需要時透過 [**IPreviewHandler：： SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)調整大小。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-160">The window is resized when needed through [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).</span></span>
7.  <span data-ttu-id="8a2e6-161">您可以透過呼叫 [**IPreviewHandler：： Unload**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload)，卸載預覽並在不再需要時釋放其資源。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-161">The preview is unloaded and its resources released when it is no longer needed, through a call to [**IPreviewHandler::Unload**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload).</span></span>

## <a name="debugging-a-preview-handler"></a><span data-ttu-id="8a2e6-162">對預覽處理常式進行偵錯工具</span><span class="sxs-lookup"><span data-stu-id="8a2e6-162">Debugging a Preview Handler</span></span>

<span data-ttu-id="8a2e6-163">如果您已遵循將預覽處理常式實作為同進程伺服器的建議，以將您的預覽處理常式進行偵錯工具，您可以將其附加至 Prevhost.exe。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-163">If you have followed the recommendations to implement your preview handler as an in-process server, to debug your preview handler, you can attach to Prevhost.exe.</span></span> <span data-ttu-id="8a2e6-164">如先前所述，請注意，Prevhost.exe 的兩個實例，一個用於一般的低 IL 進程，另一個用於已選擇不以低 IL 進程的方式執行的處理常式。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-164">As mentioned earlier, be aware that there could be two instances of Prevhost.exe, one for normal low IL processes and one for those handlers that have opted out of running as a low IL process.</span></span>

<span data-ttu-id="8a2e6-165">如果您在可用的進程清單中找不到 Prevhost.exe，表示該時間點可能尚未載入。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-165">If you do not find Prevhost.exe in your list of available processes, it probably has not been loaded at that point.</span></span> <span data-ttu-id="8a2e6-166">按一下檔案以供預覽時，會載入代理程式，然後應該會顯示為可附加的進程。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-166">Clicking on a file for a preview loads the surrogate and it should then appear as an attachable process.</span></span>

## <a name="providing-your-own-process-for-a-preview-handler"></a><span data-ttu-id="8a2e6-167">提供您自己的預覽處理常式流程</span><span class="sxs-lookup"><span data-stu-id="8a2e6-167">Providing Your Own Process for a Preview Handler</span></span>

<span data-ttu-id="8a2e6-168">如果您想要強制建立處理常式的新進程，而不是在預設進程下執行，請為您的處理常式在 **AppID** 下建立新的子機碼，並將其 DllSurrogate 專案設定為 "Prevhost.exe"。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-168">If you want to force the creation of a new process for your handler rather than running under the default process, create a new subkey for your handler under **AppID** and set its DllSurrogate entry to "Prevhost.exe".</span></span> <span data-ttu-id="8a2e6-169">使用 **appid** 子機碼，而不是預設的 Prevhost.exe **appid**。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-169">Use that **AppID** subkey instead of the default Prevhost.exe **AppID**.</span></span>

<span data-ttu-id="8a2e6-170">藉由提供新的處理常式，處理常式可以避免在共用進程下執行，如同預設的一樣。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-170">By providing a new process, the handler can avoid running under a shared process as it would do by default.</span></span> <span data-ttu-id="8a2e6-171">例如，這可以讓您確保特定版本的 common language runtime (CLR) 在進程中。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-171">This could allow you, for example, to ensure the specific version of the common language runtime (CLR) in the process.</span></span> <span data-ttu-id="8a2e6-172">如果您要建立預覽處理常式的 managed 執行，則這是必要的。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-172">This is required if you are building a managed implementation of a preview handler.</span></span>

> [!Note]  
> <span data-ttu-id="8a2e6-173">32位預覽處理常式在64位作業系統上安裝時，應使用 **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C}。</span><span class="sxs-lookup"><span data-stu-id="8a2e6-173">32-bit preview handlers should use **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} when installed on 64-bit operating systems.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8a2e6-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a2e6-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a2e6-175">建立預覽處理常式</span><span class="sxs-lookup"><span data-stu-id="8a2e6-175">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="8a2e6-176">如何註冊預覽處理常式</span><span class="sxs-lookup"><span data-stu-id="8a2e6-176">How to Register a Preview Handler</span></span>](how-to-register-a-preview-handler.md)
</dt> <dt>

[<span data-ttu-id="8a2e6-177">預覽處理常式指導方針</span><span class="sxs-lookup"><span data-stu-id="8a2e6-177">Preview Handler Guidelines</span></span>](preview-handler-guidelines.md)
</dt> </dl>

 

 
