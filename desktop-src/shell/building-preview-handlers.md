---
description: 本主題討論建立預覽處理常式所需的特定介面和方法。
ms.assetid: 6c240a63-c184-4b65-9483-794f5de4d695
title: 建立預覽處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a309873cf082071d5f426ce0ba6d039107c59665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318116"
---
# <a name="building-preview-handlers"></a><span data-ttu-id="706e0-103">建立預覽處理常式</span><span class="sxs-lookup"><span data-stu-id="706e0-103">Building Preview Handlers</span></span>

<span data-ttu-id="706e0-104">本主題討論建立預覽處理常式所需的特定介面和方法。</span><span class="sxs-lookup"><span data-stu-id="706e0-104">This topic discusses the specific interfaces and methods required to create a preview handler.</span></span>

<span data-ttu-id="706e0-105">預覽處理常式必須執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="706e0-105">A preview handler must implement the following interfaces:</span></span>

-   <span data-ttu-id="706e0-106">[IInitializeWithStream：： Initialize](#iinitializewithstreaminitialize) (強慣用) 、 [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)或 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)</span><span class="sxs-lookup"><span data-stu-id="706e0-106">[IInitializeWithStream::Initialize](#iinitializewithstreaminitialize) (strongly preferred), [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile), or [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)</span></span>
-   [<span data-ttu-id="706e0-107">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="706e0-107">IObjectWithSite</span></span>](#iobjectwithsite)
-   [<span data-ttu-id="706e0-108">IOleWindow</span><span class="sxs-lookup"><span data-stu-id="706e0-108">IOleWindow</span></span>](#iolewindow)
-   [<span data-ttu-id="706e0-109">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="706e0-109">IPreviewHandler</span></span>](#ipreviewhandler)

<span data-ttu-id="706e0-110">如果您的預覽處理常式支援主控制項（例如背景色彩和字型）所提供的視覺效果設定，它也必須執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="706e0-110">If your preview handler supports visual settings provided by the host such as background color and font, it must also implement the following interface:</span></span>

-   [<span data-ttu-id="706e0-111">IPreviewHandlerVisuals</span><span class="sxs-lookup"><span data-stu-id="706e0-111">IPreviewHandlerVisuals</span></span>](#ipreviewhandlervisuals)

<span data-ttu-id="706e0-112">本主題假設預覽處理常式是以資料流程初始化，並且已註冊特定的副檔名。</span><span class="sxs-lookup"><span data-stu-id="706e0-112">This topic assumes that the preview handler is initialized with a stream and is registered for a particular file name extension.</span></span>

## <a name="iinitializewithstreaminitialize"></a><span data-ttu-id="706e0-113">IInitializeWithStream：： Initialize</span><span class="sxs-lookup"><span data-stu-id="706e0-113">IInitializeWithStream::Initialize</span></span>

<span data-ttu-id="706e0-114">儲存 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 和 mode 參數，讓您可以在準備好預覽專案時讀取專案的資料。</span><span class="sxs-lookup"><span data-stu-id="706e0-114">Store the [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) and mode parameters so that you can read the item's data when you are ready to preview the item.</span></span> <span data-ttu-id="706e0-115">請勿在 [**Initialize**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize)中載入資料。</span><span class="sxs-lookup"><span data-stu-id="706e0-115">Do not load the data in [**Initialize**](/windows/desktop/api/Propsys/nf-propsys-iinitializewithstream-initialize).</span></span> <span data-ttu-id="706e0-116">載入 IPreviewHandler 中的資料 [**：:D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) 。</span><span class="sxs-lookup"><span data-stu-id="706e0-116">Load the data in [**IPreviewHandler::DoPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) just before you render.</span></span>

## <a name="iobjectwithsite"></a><span data-ttu-id="706e0-117">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="706e0-117">IObjectWithSite</span></span>

-   [<span data-ttu-id="706e0-118">IObjectWithSite：： SetSite</span><span class="sxs-lookup"><span data-stu-id="706e0-118">IObjectWithSite::SetSite</span></span>](#iobjectwithsitesetsite)
-   [<span data-ttu-id="706e0-119">IObjectWithSite：： GetSite</span><span class="sxs-lookup"><span data-stu-id="706e0-119">IObjectWithSite::GetSite</span></span>](#iobjectwithsitegetsite)

### <a name="iobjectwithsitesetsite"></a><span data-ttu-id="706e0-120">IObjectWithSite：： SetSite</span><span class="sxs-lookup"><span data-stu-id="706e0-120">IObjectWithSite::SetSite</span></span>

<span data-ttu-id="706e0-121">儲存 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標以供稍後存取。</span><span class="sxs-lookup"><span data-stu-id="706e0-121">Store the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer for later access.</span></span>

<span data-ttu-id="706e0-122">如果您目前有 [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) 物件的參考，請加以釋放。</span><span class="sxs-lookup"><span data-stu-id="706e0-122">If you currently have a reference to an [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) object, release it.</span></span> <span data-ttu-id="706e0-123">使用儲存的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標來呼叫網站上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，以取得新的 **IPreviewHandlerFrame** 參考。</span><span class="sxs-lookup"><span data-stu-id="706e0-123">Use the stored [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer to call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for a new **IPreviewHandlerFrame** reference.</span></span>

<span data-ttu-id="706e0-124">如果您目前有快速鍵對應表，請將它終結。</span><span class="sxs-lookup"><span data-stu-id="706e0-124">If you currently have an accelerator table, destroy it.</span></span> <span data-ttu-id="706e0-125">呼叫 [**IPreviewHandlerFrame：： GetWindowCoNtext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) 以取得新的快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="706e0-125">Call [**IPreviewHandlerFrame::GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext) to get a new accelerator table.</span></span> <span data-ttu-id="706e0-126">儲存此資料表。</span><span class="sxs-lookup"><span data-stu-id="706e0-126">Store this table.</span></span> <span data-ttu-id="706e0-127">請注意，它只會用來做為框架所支援的快速鍵清單。</span><span class="sxs-lookup"><span data-stu-id="706e0-127">Note that it is used only as a list of accelerator keys that the frame supports.</span></span> <span data-ttu-id="706e0-128">加速器專案中的命令會被忽略。</span><span class="sxs-lookup"><span data-stu-id="706e0-128">Commands in the accelerator entries are ignored.</span></span>

### <a name="iobjectwithsitegetsite"></a><span data-ttu-id="706e0-129">IObjectWithSite：： GetSite</span><span class="sxs-lookup"><span data-stu-id="706e0-129">IObjectWithSite::GetSite</span></span>

<span data-ttu-id="706e0-130">傳回網站指標，不管是什麼。</span><span class="sxs-lookup"><span data-stu-id="706e0-130">Return the site pointer, whatever it is.</span></span>

## <a name="iolewindow"></a><span data-ttu-id="706e0-131">IOleWindow</span><span class="sxs-lookup"><span data-stu-id="706e0-131">IOleWindow</span></span>

-   [<span data-ttu-id="706e0-132">IOleWindow：： CoNtextSensitiveHelp</span><span class="sxs-lookup"><span data-stu-id="706e0-132">IOleWindow::ContextSensitiveHelp</span></span>](#iolewindowcontextsensitivehelp)
-   [<span data-ttu-id="706e0-133">IOleWindow：： GetWindow</span><span class="sxs-lookup"><span data-stu-id="706e0-133">IOleWindow::GetWindow</span></span>](#iolewindowgetwindow)

### <a name="iolewindowcontextsensitivehelp"></a><span data-ttu-id="706e0-134">IOleWindow：： CoNtextSensitiveHelp</span><span class="sxs-lookup"><span data-stu-id="706e0-134">IOleWindow::ContextSensitiveHelp</span></span>

<span data-ttu-id="706e0-135">傳回 \_ 這個方法的 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="706e0-135">Return E\_NOTIMPL for this method.</span></span>

### <a name="iolewindowgetwindow"></a><span data-ttu-id="706e0-136">IOleWindow：： GetWindow</span><span class="sxs-lookup"><span data-stu-id="706e0-136">IOleWindow::GetWindow</span></span>

<span data-ttu-id="706e0-137">如果預覽處理常式的視窗目前存在，則傳回該視窗的 **HWND** 和 s \_ 確定。</span><span class="sxs-lookup"><span data-stu-id="706e0-137">If the preview handler's window currently exists, return the **HWND** of that window and S\_OK.</span></span> <span data-ttu-id="706e0-138">如果視窗不存在，則傳回 E \_ 會失敗。</span><span class="sxs-lookup"><span data-stu-id="706e0-138">If the window does not exist, return E\_FAIL.</span></span>

## <a name="ipreviewhandler"></a><span data-ttu-id="706e0-139">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="706e0-139">IPreviewHandler</span></span>

-   [<span data-ttu-id="706e0-140">IPreviewHandler：： SetWindow</span><span class="sxs-lookup"><span data-stu-id="706e0-140">IPreviewHandler::SetWindow</span></span>](#ipreviewhandlersetwindow)
-   [<span data-ttu-id="706e0-141">IPreviewHandler：： SetRect</span><span class="sxs-lookup"><span data-stu-id="706e0-141">IPreviewHandler::SetRect</span></span>](#ipreviewhandlersetrect)
-   [<span data-ttu-id="706e0-142">IPreviewHandler：:D oPreview</span><span class="sxs-lookup"><span data-stu-id="706e0-142">IPreviewHandler::DoPreview</span></span>](#ipreviewhandlerdopreview)
-   [<span data-ttu-id="706e0-143">IPreviewHandler：： SetFocus</span><span class="sxs-lookup"><span data-stu-id="706e0-143">IPreviewHandler::SetFocus</span></span>](#ipreviewhandlersetfocus)
-   [<span data-ttu-id="706e0-144">IPreviewHandler：： QueryFocus</span><span class="sxs-lookup"><span data-stu-id="706e0-144">IPreviewHandler::QueryFocus</span></span>](#ipreviewhandlerqueryfocus)
-   [<span data-ttu-id="706e0-145">IPreviewHandler：： TranslateAccelerator</span><span class="sxs-lookup"><span data-stu-id="706e0-145">IPreviewHandler::TranslateAccelerator</span></span>](#ipreviewhandlertranslateaccelerator)
-   [<span data-ttu-id="706e0-146">IPreviewHandler：： Unload</span><span class="sxs-lookup"><span data-stu-id="706e0-146">IPreviewHandler::Unload</span></span>](#ipreviewhandlerunload)

### <a name="ipreviewhandlersetwindow"></a><span data-ttu-id="706e0-147">IPreviewHandler：： SetWindow</span><span class="sxs-lookup"><span data-stu-id="706e0-147">IPreviewHandler::SetWindow</span></span>

<span data-ttu-id="706e0-148">將這個方法的 *hwnd* 參數設定為預覽處理常式 **hwnd** 的父系。</span><span class="sxs-lookup"><span data-stu-id="706e0-148">Set the *hwnd* parameter of this method to the parent of your preview handler's **HWND**.</span></span> <span data-ttu-id="706e0-149">您可以多次呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="706e0-149">This method can be called multiple times.</span></span> <span data-ttu-id="706e0-150">調整您的預覽大小，使其只在 *prc* 參數所描述的區域中轉譯。</span><span class="sxs-lookup"><span data-stu-id="706e0-150">Resize your preview so that it renders only in the area described by the *prc* parameter.</span></span>

<span data-ttu-id="706e0-151">如果預覽程式正在轉譯中，請使用 [**IPreviewHandler：： SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) 方法來變更預覽程式的父系。</span><span class="sxs-lookup"><span data-stu-id="706e0-151">If the previewer is in the process of rendering, use the [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) method to change the parent of the previewer.</span></span> <span data-ttu-id="706e0-152">也請變更預覽程式的呈現區域。</span><span class="sxs-lookup"><span data-stu-id="706e0-152">Also change the area in which the previewer is rendering.</span></span>

### <a name="ipreviewhandlersetrect"></a><span data-ttu-id="706e0-153">IPreviewHandler：： SetRect</span><span class="sxs-lookup"><span data-stu-id="706e0-153">IPreviewHandler::SetRect</span></span>

<span data-ttu-id="706e0-154">調整您的預覽大小，使其只在此方法的 *中國* 所描述的區域內轉譯。</span><span class="sxs-lookup"><span data-stu-id="706e0-154">Resize your preview so that it only renders in the area described by this method's *prc*.</span></span>

<span data-ttu-id="706e0-155">如果預覽程式正在轉譯中，請變更您的預覽器呈現區域。</span><span class="sxs-lookup"><span data-stu-id="706e0-155">If the previewer is in the process of rendering, change the area in which your previewer renders.</span></span>

### <a name="ipreviewhandlerdopreview"></a><span data-ttu-id="706e0-156">IPreviewHandler：:D oPreview</span><span class="sxs-lookup"><span data-stu-id="706e0-156">IPreviewHandler::DoPreview</span></span>

<span data-ttu-id="706e0-157">這是實際工作的完成位置。</span><span class="sxs-lookup"><span data-stu-id="706e0-157">This is where the real work is done.</span></span> <span data-ttu-id="706e0-158">因為預覽版是動態的，所以只有在需要時才會載入預覽內容。</span><span class="sxs-lookup"><span data-stu-id="706e0-158">Since a preview is dynamic, the preview content should only be loaded when it is needed.</span></span> <span data-ttu-id="706e0-159">請勿在初始化中載入內容。</span><span class="sxs-lookup"><span data-stu-id="706e0-159">Do not load content in the initialization.</span></span>

<span data-ttu-id="706e0-160">如果預覽處理常式視窗不存在，請加以建立。</span><span class="sxs-lookup"><span data-stu-id="706e0-160">If the preview handler window does not exist, create it.</span></span> <span data-ttu-id="706e0-161">預覽處理常式的視窗應該是 [**IPreviewHandler：： SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow)所提供視窗的子系。</span><span class="sxs-lookup"><span data-stu-id="706e0-161">Your preview handler's windows should be children of the window provided by [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow).</span></span> <span data-ttu-id="706e0-162">它們應該是 **IPreviewHandler：： SetWindow** 和 [**IPreviewHandler：： SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) 所提供的大小， (最近呼叫過的) 。</span><span class="sxs-lookup"><span data-stu-id="706e0-162">They should be the size provided by **IPreviewHandler::SetWindow** and [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect) (whichever was called most recently).</span></span>

<span data-ttu-id="706e0-163">當您擁有視窗之後，請從已初始化預覽處理常式的 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 載入資料，並將該資料轉譯為您的預覽處理常式視窗。</span><span class="sxs-lookup"><span data-stu-id="706e0-163">Once you have a window, load the data from the [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) that the preview handler was initialized with, and render that data to your preview handler's window.</span></span>

### <a name="ipreviewhandlersetfocus"></a><span data-ttu-id="706e0-164">IPreviewHandler：： SetFocus</span><span class="sxs-lookup"><span data-stu-id="706e0-164">IPreviewHandler::SetFocus</span></span>

<span data-ttu-id="706e0-165">當焦點透過索引標籤動作進入讀取窗格時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="706e0-165">This method is called when the focus enters the reading pane through a tab action.</span></span> <span data-ttu-id="706e0-166">因為它可以輸入為 [轉寄] 索引標籤或 [反向] 索引標籤，所以請使用 SHIFT 鍵的目前狀態，來決定讀取窗格中的第一個或最後一個索引標籤是否應該接收焦點。</span><span class="sxs-lookup"><span data-stu-id="706e0-166">Since it can be entered as a forward tab or reverse tab, use the current state of the SHIFT key to decide whether the first or last tab stop in the reading pane should receive the focus.</span></span>

### <a name="ipreviewhandlerqueryfocus"></a><span data-ttu-id="706e0-167">IPreviewHandler：： QueryFocus</span><span class="sxs-lookup"><span data-stu-id="706e0-167">IPreviewHandler::QueryFocus</span></span>

<span data-ttu-id="706e0-168">這個方法應該呼叫 [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) 函式，並在 *phwnd* 參數中傳回該呼叫的結果。</span><span class="sxs-lookup"><span data-stu-id="706e0-168">This method should call the [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) function and return the result of that call in the *phwnd* parameter.</span></span>

### <a name="ipreviewhandlertranslateaccelerator"></a><span data-ttu-id="706e0-169">IPreviewHandler：： TranslateAccelerator</span><span class="sxs-lookup"><span data-stu-id="706e0-169">IPreviewHandler::TranslateAccelerator</span></span>

<span data-ttu-id="706e0-170">預覽處理常式的進程會呼叫這個方法， (是否 prevhost.exe 或自訂本機伺服器) 來回應使用者擊鍵。</span><span class="sxs-lookup"><span data-stu-id="706e0-170">This method is called by the message pump of the preview handler's process (whether prevhost.exe or a custom local server) in response to user keystrokes.</span></span> <span data-ttu-id="706e0-171">預覽處理常式應該根據下面詳述的演算法來處理這些按鍵，或將它們轉送到其主機。</span><span class="sxs-lookup"><span data-stu-id="706e0-171">Preview handlers should handle these keystrokes or forward them to their host according to the algorithm detailed below.</span></span>

<span data-ttu-id="706e0-172">不過，因為預覽是唯讀的，所以鍵盤輸入應該是最小和優化，例如在許多情況下都不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="706e0-172">However, because previews are read-only, keyboard input should be minimal and optimizations such as this are not needed in many cases.</span></span>

<span data-ttu-id="706e0-173">如果透過訊息提取傳遞給這個方法的鍵盤快速鍵是預覽處理常式接受的加速器，則處理它，並傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="706e0-173">If the keyboard accelerator passed to this method through the message pump is an accelerator that your preview handler accepts, then process it and return S\_OK.</span></span> <span data-ttu-id="706e0-174">如果您的處理常式不接受該加速器，則可以將快速鍵訊息傳回給要處理的畫面格。</span><span class="sxs-lookup"><span data-stu-id="706e0-174">If your handler does not accept that accelerator, the accelerator message can be sent back as far as the frame to be handled.</span></span>

<span data-ttu-id="706e0-175">有兩個選項可將鍵盤快速鍵轉送回框架：</span><span class="sxs-lookup"><span data-stu-id="706e0-175">There are two options for forwarding keyboard accelerators back to the frame:</span></span>

<span data-ttu-id="706e0-176">最簡單的模型是使用 [**IPreviewHandlerFrame：： TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator)將所有擊鍵轉送至主機。</span><span class="sxs-lookup"><span data-stu-id="706e0-176">The simplest model is to forward all keystrokes to the host using [**IPreviewHandlerFrame::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator).</span></span> <span data-ttu-id="706e0-177">這是在 Windows 軟體開發套件 (SDK) 提供的預覽處理常式範例中完成。</span><span class="sxs-lookup"><span data-stu-id="706e0-177">This is done in the preview handler sample provided with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="706e0-178">所有低完整性預覽處理常式都必須使用此模型。</span><span class="sxs-lookup"><span data-stu-id="706e0-178">All low-integrity preview handlers must use this model.</span></span> <span data-ttu-id="706e0-179">如果您的預覽處理常式未處理此加速器，請呼叫 **IPreviewHandlerFrame：： TranslateAccelerator** 並傳回其結果。</span><span class="sxs-lookup"><span data-stu-id="706e0-179">If the accelerator is not handled by your preview handler, call **IPreviewHandlerFrame::TranslateAccelerator** and return its result.</span></span>

<span data-ttu-id="706e0-180">另一個模型是使用快速鍵對應表作為優化，以避免跨進程界限傳送太多按鍵：</span><span class="sxs-lookup"><span data-stu-id="706e0-180">The other model is to use an accelerator table as an optimization to avoid sending too many keystrokes across process boundaries:</span></span>

1.  <span data-ttu-id="706e0-181">在預覽處理常式上呼叫 [**IObjectWithSite：： SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 時，透過 [**IPreviewHandlerFrame：： GetWindowCoNtext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext)取得快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="706e0-181">When [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is called on your preview handler, acquire the accelerator table through [**IPreviewHandlerFrame::GetWindowContext**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext).</span></span> <span data-ttu-id="706e0-182"> (在您的預覽程式終結時，請務必釋放快速鍵對應表的控制碼。 ) </span><span class="sxs-lookup"><span data-stu-id="706e0-182">(Be sure to free the handle to the accelerator table when your previewer is destroyed.)</span></span>
2.  <span data-ttu-id="706e0-183">如果您的預覽處理常式處理此加速器，請進行處理，並傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="706e0-183">If the accelerator is handled by your preview handler, handle it and return S\_OK.</span></span>
3.  <span data-ttu-id="706e0-184">如果您的預覽處理常式未處理此加速器，請針對取得的快速鍵對應表，使用 [**IsAccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) 來比較訊息。</span><span class="sxs-lookup"><span data-stu-id="706e0-184">If the accelerator is not handled by your preview handler, compare the message using [**IsAccelerator**](/windows/win32/api/ole2/nf-ole2-isaccelerator) against the accelerator table acquired.</span></span>
4.  <span data-ttu-id="706e0-185">如果快速鍵符合該快速鍵對應表中的專案，請呼叫 [**IPreviewHandlerFrame：： TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) 並傳回其結果。</span><span class="sxs-lookup"><span data-stu-id="706e0-185">If the accelerator matches an entry in that accelerator table, call [**IPreviewHandlerFrame::TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-translateaccelerator) and return its result.</span></span>
5.  <span data-ttu-id="706e0-186">如果快速鍵不符合快速鍵對應表中的任何專案，則傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="706e0-186">If the accelerator does not match any entry in the accelerator table, return S\_FALSE.</span></span>

### <a name="ipreviewhandlerunload"></a><span data-ttu-id="706e0-187">IPreviewHandler：： Unload</span><span class="sxs-lookup"><span data-stu-id="706e0-187">IPreviewHandler::Unload</span></span>

<span data-ttu-id="706e0-188">當呼叫這個方法時，請停止任何轉譯、釋放從資料流程讀取資料所配置的任何資源，然後釋放 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 本身。</span><span class="sxs-lookup"><span data-stu-id="706e0-188">When this method is called, stop any rendering, release any resources allocated by reading data from the stream, and release the [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) itself.</span></span>

<span data-ttu-id="706e0-189">一旦呼叫這個方法，就必須重新初始化處理常式，然後再嘗試呼叫 [**IPreviewHandler：:D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) 。</span><span class="sxs-lookup"><span data-stu-id="706e0-189">Once this method is called, the handler must be reinitialized before any attempt to call [**IPreviewHandler::DoPreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) again.</span></span>

## <a name="ipreviewhandlervisuals"></a><span data-ttu-id="706e0-190">IPreviewHandlerVisuals</span><span class="sxs-lookup"><span data-stu-id="706e0-190">IPreviewHandlerVisuals</span></span>

-   [<span data-ttu-id="706e0-191">IPreviewHandlerVisuals::SetBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="706e0-191">IPreviewHandlerVisuals::SetBackgroundColor</span></span>](#ipreviewhandlervisualssetbackgroundcolor)
-   [<span data-ttu-id="706e0-192">IPreviewHandlerVisuals::SetFont</span><span class="sxs-lookup"><span data-stu-id="706e0-192">IPreviewHandlerVisuals::SetFont</span></span>](#ipreviewhandlervisualssetfont)
-   [<span data-ttu-id="706e0-193">IPreviewHandlerVisuals::SetTextColor</span><span class="sxs-lookup"><span data-stu-id="706e0-193">IPreviewHandlerVisuals::SetTextColor</span></span>](#ipreviewhandlervisualssettextcolor)

<span data-ttu-id="706e0-194">當您導向預覽處理常式來回應主機的色彩和字型配置時，應該執行這些方法。</span><span class="sxs-lookup"><span data-stu-id="706e0-194">These methods should be implemented when directing the preview handler to respond to the host's color and font schemes.</span></span> <span data-ttu-id="706e0-195">主機會查詢 [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals)的處理常式。</span><span class="sxs-lookup"><span data-stu-id="706e0-195">The host queries the handler for [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals).</span></span> <span data-ttu-id="706e0-196">如果發現支援，主機會提供色彩、字型和文字色彩。</span><span class="sxs-lookup"><span data-stu-id="706e0-196">If found to be supported, the host provides it with color, font, and text color.</span></span>

### <a name="ipreviewhandlervisualssetbackgroundcolor"></a><span data-ttu-id="706e0-197">IPreviewHandlerVisuals::SetBackgroundColor</span><span class="sxs-lookup"><span data-stu-id="706e0-197">IPreviewHandlerVisuals::SetBackgroundColor</span></span>

<span data-ttu-id="706e0-198">當您想要提供背景色彩時，請儲存此色彩，並在轉譯期間使用它。</span><span class="sxs-lookup"><span data-stu-id="706e0-198">Store this color and use it during rendering when you want to provide a background color.</span></span> <span data-ttu-id="706e0-199">例如，當處理常式轉譯至小於 [**IPreviewHandler：： SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) 和 [**IPreviewHandler：： SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)提供之區域的區域時，就會填滿視窗。</span><span class="sxs-lookup"><span data-stu-id="706e0-199">For instance, to fill the window when the handler renders to an area smaller than the area provided by [**IPreviewHandler::SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow) and [**IPreviewHandler::SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).</span></span> <span data-ttu-id="706e0-200">不過請注意，您不應該在這些方法所提供的區域之外繪製。</span><span class="sxs-lookup"><span data-stu-id="706e0-200">Note, however, that you should not draw outside the area provided by those methods.</span></span>

<span data-ttu-id="706e0-201">如果在呈現預覽版時呼叫這個方法，則應該使用此背景色彩重新開機轉譯。</span><span class="sxs-lookup"><span data-stu-id="706e0-201">If this method is called while the preview is already being rendered, the rendering should be restarted using this background color.</span></span>

### <a name="ipreviewhandlervisualssetfont"></a><span data-ttu-id="706e0-202">IPreviewHandlerVisuals::SetFont</span><span class="sxs-lookup"><span data-stu-id="706e0-202">IPreviewHandlerVisuals::SetFont</span></span>

<span data-ttu-id="706e0-203">當您想要顯示與目前 Windows Vista 設定一致的文字時，請儲存此字型資訊，並在轉譯期間使用它。</span><span class="sxs-lookup"><span data-stu-id="706e0-203">Store this font information and use it during rendering when you want to display text consistent with the current Windows Vista settings.</span></span>

### <a name="ipreviewhandlervisualssettextcolor"></a><span data-ttu-id="706e0-204">IPreviewHandlerVisuals::SetTextColor</span><span class="sxs-lookup"><span data-stu-id="706e0-204">IPreviewHandlerVisuals::SetTextColor</span></span>

<span data-ttu-id="706e0-205">當您想要顯示與目前 Windows Vista 設定一致的文字時，請儲存此文字色彩資訊，並在轉譯期間使用它。</span><span class="sxs-lookup"><span data-stu-id="706e0-205">Store this text color information and use it during rendering when you want to display text consistent with the current Windows Vista settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="706e0-206">相關主題</span><span class="sxs-lookup"><span data-stu-id="706e0-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="706e0-207">預覽處理常式和 Shell 預覽主機</span><span class="sxs-lookup"><span data-stu-id="706e0-207">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="706e0-208">如何註冊預覽處理常式</span><span class="sxs-lookup"><span data-stu-id="706e0-208">How to Register a Preview Handler</span></span>](how-to-register-a-preview-handler.md)
</dt> <dt>

[<span data-ttu-id="706e0-209">預覽處理常式指導方針</span><span class="sxs-lookup"><span data-stu-id="706e0-209">Preview Handler Guidelines</span></span>](preview-handler-guidelines.md)
</dt> </dl>

 

 
