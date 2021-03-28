---
description: 從 Windows Vista 開始，當用來開啟或儲存檔案時，[一般專案] 對話方塊會取代舊的 [一般檔案] 對話方塊。
title: 一般專案對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 896514779b2ba3d11d3db0551f82e21f1d4120b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318115"
---
# <a name="common-item-dialog"></a><span data-ttu-id="34ff6-103">一般專案對話方塊</span><span class="sxs-lookup"><span data-stu-id="34ff6-103">Common Item Dialog</span></span>

<span data-ttu-id="34ff6-104">從 Windows Vista 開始，當用來開啟或儲存檔案時，[一般專案] 對話方塊會取代舊的 [一般檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-104">Starting with Windows Vista, the Common Item Dialog supersedes the older Common File Dialog when used to open or save a file.</span></span> <span data-ttu-id="34ff6-105">[一般專案] 對話方塊用於兩種變化： [ **開啟** ] 對話方塊和 [ **儲存** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-105">The Common Item Dialog is used in two variations: the **Open** dialog and the **Save** dialog.</span></span> <span data-ttu-id="34ff6-106">這兩個對話方塊共用大部分的功能，但每個都有自己的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="34ff6-106">These two dialogs share most of their functionality, but each has its own unique methods.</span></span>

<span data-ttu-id="34ff6-107">雖然這個較新的版本命名為 [一般專案] 對話方塊，但在大部分的檔中，它仍會繼續稱為 [一般檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-107">While this newer version is named the Common Item Dialog, it continues to be called the Common File Dialog in most documentation.</span></span> <span data-ttu-id="34ff6-108">除非您處理的是舊版 Windows，否則您應該假設任何提及的 [一般檔案] 對話方塊都會參考這個 [一般專案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-108">Unless you are dealing specifically with an older version of Windows, you should assume that any mention of the Common File Dialog refers to this Common Item Dialog.</span></span>

<span data-ttu-id="34ff6-109">以下將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="34ff6-109">The following topics are discussed here:</span></span>

-   [<span data-ttu-id="34ff6-110">IFileDialog、IFileOpenDialog 和 IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="34ff6-110">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [<span data-ttu-id="34ff6-111">範例使用方式</span><span class="sxs-lookup"><span data-stu-id="34ff6-111">Sample Usage</span></span>](#sample-usage)
-   [<span data-ttu-id="34ff6-112">從對話方塊接聽事件</span><span class="sxs-lookup"><span data-stu-id="34ff6-112">Listening to Events from the Dialog</span></span>](#listening-to-events-from-the-dialog)
    -   [<span data-ttu-id="34ff6-113">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="34ff6-113">OnFileOk</span></span>](#onfileok)
    -   [<span data-ttu-id="34ff6-114">OnShareViolation 和 OnOverwrite</span><span class="sxs-lookup"><span data-stu-id="34ff6-114">OnShareViolation and OnOverwrite</span></span>](#onshareviolation-and-onoverwrite)
-   [<span data-ttu-id="34ff6-115">自訂對話方塊</span><span class="sxs-lookup"><span data-stu-id="34ff6-115">Customizing the Dialog</span></span>](#customizing-the-dialog)
    -   <span data-ttu-id="34ff6-116">[將選項新增至 [確定] 按鈕](#adding-options-to-the-ok-button)</span><span class="sxs-lookup"><span data-stu-id="34ff6-116">[Adding Options to the OK Button](#adding-options-to-the-ok-button)</span></span>
    -   [<span data-ttu-id="34ff6-117">回應新增控制項中的事件</span><span class="sxs-lookup"><span data-stu-id="34ff6-117">Responding to Events in Added Controls</span></span>](#responding-to-events-in-added-controls)
-   [<span data-ttu-id="34ff6-118">完整範例</span><span class="sxs-lookup"><span data-stu-id="34ff6-118">Full Samples</span></span>](#full-samples)
-   [<span data-ttu-id="34ff6-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="34ff6-119">Related topics</span></span>](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a><span data-ttu-id="34ff6-120">IFileDialog、IFileOpenDialog 和 IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="34ff6-120">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>

<span data-ttu-id="34ff6-121">Windows Vista 提供 [ **開啟** ] 和 [ **儲存** ] 對話方塊的實作為： clsid \_ FileOpenDialog 和 clsid \_ FileSaveDialog。</span><span class="sxs-lookup"><span data-stu-id="34ff6-121">Windows Vista provides implementations of the **Open** and **Save** dialogs: CLSID\_FileOpenDialog and CLSID\_FileSaveDialog.</span></span> <span data-ttu-id="34ff6-122">這些對話方塊如下所示。</span><span class="sxs-lookup"><span data-stu-id="34ff6-122">Those dialog boxes are shown here.</span></span>

![[開啟] 對話方塊的螢幕擷取畫面](images/cid/openfiledialog.png)

![[另存新檔] 對話方塊的螢幕擷取畫面](images/cid/savefiledialog.png)

<span data-ttu-id="34ff6-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) 和 [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) 繼承自 [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) ，並共用許多功能。</span><span class="sxs-lookup"><span data-stu-id="34ff6-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) and [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) inherit from [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and share much of their functionality.</span></span> <span data-ttu-id="34ff6-126">此外，[ **開啟** ] 對話方塊支援 **IFileOpenDialog**，而 [ **儲存** ] 對話方塊支援 **IFileSaveDialog**。</span><span class="sxs-lookup"><span data-stu-id="34ff6-126">In addition, the **Open** dialog supports **IFileOpenDialog**, and the **Save** dialog supports **IFileSaveDialog**.</span></span>

<span data-ttu-id="34ff6-127">在 Windows Vista 中找到的通用專案對話方塊可提供比舊版中提供的數個優點：</span><span class="sxs-lookup"><span data-stu-id="34ff6-127">The Common Item Dialog implementation found in Windows Vista provides several advantages over the implementation provided in earlier versions:</span></span>

-   <span data-ttu-id="34ff6-128">支援透過 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 直接使用 Shell 命名空間，而不是使用檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="34ff6-128">Supports direct use of the Shell namespace through [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) instead of using file system paths.</span></span>
-   <span data-ttu-id="34ff6-129">啟用對話方塊的簡單自訂，例如在 [ **確定]** 按鈕上設定標籤，而不需要進行勾點程式。</span><span class="sxs-lookup"><span data-stu-id="34ff6-129">Enables simple customization of the dialog, such as setting the label on the **OK** button, without requiring a hook procedure.</span></span>
-   <span data-ttu-id="34ff6-130">藉由新增一組在不使用 Win32 對話方塊範本運作的資料驅動控制項，支援更廣泛的對話自訂。</span><span class="sxs-lookup"><span data-stu-id="34ff6-130">Supports more extensive customization of the dialog by the addition of a set of data-driven controls that operate without a Win32 dialog template.</span></span> <span data-ttu-id="34ff6-131">這個自訂配置會釋出 UI 配置的呼叫進程。</span><span class="sxs-lookup"><span data-stu-id="34ff6-131">This customization scheme frees the calling process from UI layout.</span></span> <span data-ttu-id="34ff6-132">由於對話方塊設計的任何變更會繼續使用此資料模型，因此對話的執行不會系結至特定的目前版本對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-132">Since any changes to the dialog design continue to use this data model, the dialog implementation is not tied to the specific current version of the dialog.</span></span>
-   <span data-ttu-id="34ff6-133">支援對話方塊內事件的呼叫端通知，例如選取範圍變更或檔案類型變更。</span><span class="sxs-lookup"><span data-stu-id="34ff6-133">Supports caller notification of events within the dialog, such as selection change or file type change.</span></span> <span data-ttu-id="34ff6-134">也可讓呼叫進程攔截對話方塊中的特定事件，例如剖析。</span><span class="sxs-lookup"><span data-stu-id="34ff6-134">Also enables the calling process to hook certain events in the dialog, such as the parsing.</span></span>
-   <span data-ttu-id="34ff6-135">引進新的對話方塊功能，例如將呼叫者指定的位置新增至 **位置** 列。</span><span class="sxs-lookup"><span data-stu-id="34ff6-135">Introduces new dialog features such as adding caller-specified places to the **Places** bar.</span></span>
-   <span data-ttu-id="34ff6-136">在 [ **儲存** ] 對話方塊中，開發人員可以利用 Windows Vista Shell 的新中繼資料功能。</span><span class="sxs-lookup"><span data-stu-id="34ff6-136">In the **Save** dialog, developers can take advantage of new metadata features of the Windows Vista Shell.</span></span>

<span data-ttu-id="34ff6-137">此外，開發人員也可以選擇執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="34ff6-137">Additionally, developers can choose to implement the following interfaces:</span></span>

-   <span data-ttu-id="34ff6-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) ，以接收對話方塊內的事件通知。</span><span class="sxs-lookup"><span data-stu-id="34ff6-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) to receive notifications of events within the dialog.</span></span>
-   <span data-ttu-id="34ff6-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ，將控制項加入對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="34ff6-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) to add controls to the dialog.</span></span>
-   <span data-ttu-id="34ff6-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) ，以在這些新增的控制項中收到事件的通知。</span><span class="sxs-lookup"><span data-stu-id="34ff6-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) to be notified of events in those added controls.</span></span>

<span data-ttu-id="34ff6-141">[ **開啟** ] 或 [ **儲存** ] 對話方塊會將 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 或 [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) 物件傳回給呼叫進程。</span><span class="sxs-lookup"><span data-stu-id="34ff6-141">The **Open** or **Save** dialog returns an [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) or [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) object to the calling process.</span></span> <span data-ttu-id="34ff6-142">接著，呼叫者可以使用個別的 **IShellItem** 物件取得檔案系統路徑，或開啟專案上的資料流程來讀取或寫入資訊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-142">The caller can then use an individual **IShellItem** object to get a file system path or to open a stream on the item to read or write information.</span></span>

<span data-ttu-id="34ff6-143">新對話方法可用的旗標和選項非常類似于 [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)結構中找到的舊版 **OFN** 旗標，並用於 [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)和 [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)。</span><span class="sxs-lookup"><span data-stu-id="34ff6-143">Flags and options available to the new dialog methods are very similar to the older **OFN** flags found in the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure and used in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="34ff6-144">其中有許多都是一樣的，不同之處在于它們是以 FOS 前置詞開頭。</span><span class="sxs-lookup"><span data-stu-id="34ff6-144">Many of them are exactly the same, except that they begin with an FOS prefix.</span></span> <span data-ttu-id="34ff6-145">您可以在 [**IFileDialog：： GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) 和 [**IFileDialog：： >setoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) 主題中找到完整的清單。</span><span class="sxs-lookup"><span data-stu-id="34ff6-145">The complete list can be found in the [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) and [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) topics.</span></span> <span data-ttu-id="34ff6-146">[**開啟**] 和 [**儲存**] 對話方塊預設會以最常見的旗標建立。</span><span class="sxs-lookup"><span data-stu-id="34ff6-146">**Open** and **Save** dialogs are created by default with the most common flags.</span></span> <span data-ttu-id="34ff6-147">針對 [ **開啟** ] 對話方塊，這是 (fos \_ PATHMUSTEXIST \| fos \_ FILEMUSTEXIST \| fos \_ NOCHANGEDIR) ，而針對 [ **儲存** ] 對話方塊，這是 (fos \_ OVERWRITEPROMPT \| fos \_ NOREADONLYRETURN \| fos \_ PATHMUSTEXIST \| fos \_ NOCHANGEDIR) 。</span><span class="sxs-lookup"><span data-stu-id="34ff6-147">For the **Open** dialog, this is (FOS\_PATHMUSTEXIST \| FOS\_FILEMUSTEXIST \| FOS\_NOCHANGEDIR) and for the **Save** dialog this is (FOS\_OVERWRITEPROMPT \| FOS\_NOREADONLYRETURN \| FOS\_PATHMUSTEXIST \| FOS\_NOCHANGEDIR).</span></span>

<span data-ttu-id="34ff6-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) 和其子系介面繼承自並擴充 [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow)。</span><span class="sxs-lookup"><span data-stu-id="34ff6-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and its descendant interfaces inherit from and extend [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span></span> <span data-ttu-id="34ff6-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) 會以它唯一的參數做為父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="34ff6-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) takes as its only parameter the handle of the parent window.</span></span> <span data-ttu-id="34ff6-150">如果 **Show** 傳回成功，則會有有效的結果。</span><span class="sxs-lookup"><span data-stu-id="34ff6-150">If **Show** returns successfully, there is a valid result.</span></span> <span data-ttu-id="34ff6-151">如果傳回 `HRESULT_FROM_WIN32(ERROR_CANCELLED)` ，則表示使用者已取消對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-151">If it returns `HRESULT_FROM_WIN32(ERROR_CANCELLED)`, it means the user canceled the dialog.</span></span> <span data-ttu-id="34ff6-152">它也可能會合法傳回另一個錯誤碼，例如 **E \_ OUTOFMEMORY**。</span><span class="sxs-lookup"><span data-stu-id="34ff6-152">It might also legitimately return another error code such as **E\_OUTOFMEMORY**.</span></span>

### <a name="sample-usage"></a><span data-ttu-id="34ff6-153">範例用法</span><span class="sxs-lookup"><span data-stu-id="34ff6-153">Sample Usage</span></span>

<span data-ttu-id="34ff6-154">下列各節顯示各種對話工作的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="34ff6-154">The following sections show example code for a variety of dialog tasks.</span></span>

-   [<span data-ttu-id="34ff6-155">基本使用方式</span><span class="sxs-lookup"><span data-stu-id="34ff6-155">Basic Usage</span></span>](#basic-usage)
-   [<span data-ttu-id="34ff6-156">將結果限制為檔案系統專案</span><span class="sxs-lookup"><span data-stu-id="34ff6-156">Limiting Results to File System Items</span></span>](#limiting-results-to-file-system-items)
-   [<span data-ttu-id="34ff6-157">指定對話方塊的檔案類型</span><span class="sxs-lookup"><span data-stu-id="34ff6-157">Specifying File Types for a Dialog</span></span>](#specifying-file-types-for-a-dialog)
-   [<span data-ttu-id="34ff6-158">控制預設資料夾</span><span class="sxs-lookup"><span data-stu-id="34ff6-158">Controlling the Default Folder</span></span>](#controlling-the-default-folder)
-   [<span data-ttu-id="34ff6-159">將專案加入至位置列</span><span class="sxs-lookup"><span data-stu-id="34ff6-159">Adding Items to the Places Bar</span></span>](#adding-items-to-the-places-bar)
-   [<span data-ttu-id="34ff6-160">狀態持續性</span><span class="sxs-lookup"><span data-stu-id="34ff6-160">State Persistence</span></span>](#state-persistence)
-   [<span data-ttu-id="34ff6-161">多重複選功能</span><span class="sxs-lookup"><span data-stu-id="34ff6-161">Multiselect Capabilities</span></span>](#multiselect-capabilities)

<span data-ttu-id="34ff6-162">大部分的範例程式碼都可以在 Windows SDK 一般檔案 [對話方塊範例](samples-commonfiledialog.md)中找到。</span><span class="sxs-lookup"><span data-stu-id="34ff6-162">Most of the sample code can be found in the Windows SDK [Common File Dialog Sample](samples-commonfiledialog.md).</span></span>

### <a name="basic-usage"></a><span data-ttu-id="34ff6-163">基本使用方式</span><span class="sxs-lookup"><span data-stu-id="34ff6-163">Basic Usage</span></span>

<span data-ttu-id="34ff6-164">下列範例說明如何啟動 **開啟** 的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-164">The following example illustrates how to launch an **Open** dialog.</span></span> <span data-ttu-id="34ff6-165">在此範例中，它會限制為 Microsoft Word 檔。</span><span class="sxs-lookup"><span data-stu-id="34ff6-165">In this example, it is restricted to Microsoft Word documents.</span></span>

> [!Note]  
> <span data-ttu-id="34ff6-166">本主題中的數個範例會使用 `CDialogEventHandler_CreateInstance` helper 函式來建立 [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) 執行的實例。</span><span class="sxs-lookup"><span data-stu-id="34ff6-166">Several examples in this topic use the `CDialogEventHandler_CreateInstance` helper function to create an instance of the [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) implementation.</span></span> <span data-ttu-id="34ff6-167">若要在您自己的程式碼中使用此函式，請 `CDialogEventHandler_CreateInstance` 從 [ [一般檔案] 對話方塊範例](samples-commonfiledialog.md)複製函式的原始程式碼，此範例取自本主題中的所有範例。</span><span class="sxs-lookup"><span data-stu-id="34ff6-167">To use this function in your own code, copy the source code for the `CDialogEventHandler_CreateInstance` function from the [Common File Dialog Sample](samples-commonfiledialog.md), from which all of the examples in this topic are taken.</span></span>

 


```C++
HRESULT BasicFileOpen()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
                    if (SUCCEEDED(hr))
                    {
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
                                if (SUCCEEDED(hr))
                                {
                                    // Show the dialog
                                    hr = pfd->Show(NULL);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Obtain the result once the user clicks 
                                        // the 'Open' button.
                                        // The result is an IShellItem object.
                                        IShellItem *psiResult;
                                        hr = pfd->GetResult(&psiResult);
                                        if (SUCCEEDED(hr))
                                        {
                                            // We are just going to print out the 
                                            // name of the file for sample sake.
                                            PWSTR pszFilePath = NULL;
                                            hr = psiResult->GetDisplayName(SIGDN_FILESYSPATH, 
                                                               &pszFilePath);
                                            if (SUCCEEDED(hr))
                                            {
                                                TaskDialog(NULL,
                                                           NULL,
                                                           L"CommonFileDialogApp",
                                                           pszFilePath,
                                                           NULL,
                                                           TDCBF_OK_BUTTON,
                                                           TD_INFORMATION_ICON,
                                                           NULL);
                                                CoTaskMemFree(pszFilePath);
                                            }
                                            psiResult->Release();
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="limiting-results-to-file-system-items"></a><span data-ttu-id="34ff6-168">將結果限制為檔案系統專案</span><span class="sxs-lookup"><span data-stu-id="34ff6-168">Limiting Results to File System Items</span></span>

<span data-ttu-id="34ff6-169">下列範例取自上述範例，示範如何將結果限制為檔案系統專案。</span><span class="sxs-lookup"><span data-stu-id="34ff6-169">The following example, taken from above, demonstrates how to restrict results to file system items.</span></span> <span data-ttu-id="34ff6-170">請注意， [**IFileDialog：： >setoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) 會將新的旗標加入至透過 [**IFileDialog：： GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions)取得的值。</span><span class="sxs-lookup"><span data-stu-id="34ff6-170">Note that [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) adds the new flag to a value obtained through [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span></span> <span data-ttu-id="34ff6-171">這是建議的方法。</span><span class="sxs-lookup"><span data-stu-id="34ff6-171">This is the recommended method.</span></span>


```C++
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
```



### <a name="specifying-file-types-for-a-dialog"></a><span data-ttu-id="34ff6-172">指定對話方塊的檔案類型</span><span class="sxs-lookup"><span data-stu-id="34ff6-172">Specifying File Types for a Dialog</span></span>

<span data-ttu-id="34ff6-173">若要設定對話方塊可以處理的特定檔案類型，請使用 [**IFileDialog：： SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) 方法。</span><span class="sxs-lookup"><span data-stu-id="34ff6-173">To set specific file types that the dialog can handle, use the [**IFileDialog::SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) method.</span></span> <span data-ttu-id="34ff6-174">該方法會接受 [**COMDLG \_ FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) 結構的陣列，其中每個結構都代表一種檔案類型。</span><span class="sxs-lookup"><span data-stu-id="34ff6-174">That method accepts an array of [**COMDLG\_FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) structures, each of which represents a file type.</span></span>

<span data-ttu-id="34ff6-175">對話方塊中的預設擴充機制與 [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) 和 [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)不一樣。</span><span class="sxs-lookup"><span data-stu-id="34ff6-175">The default extension mechanism in a dialog is unchanged from [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="34ff6-176">當對話方塊開啟時，會初始化附加至 [檔案名] 編輯方塊中使用者所輸入之文字的副檔名。</span><span class="sxs-lookup"><span data-stu-id="34ff6-176">The file name extension that is appended to the text the user types in the file name edit box is initialized when the dialog opens.</span></span> <span data-ttu-id="34ff6-177">它應該符合 (在對話方塊開啟) 時選取的預設檔案類型。</span><span class="sxs-lookup"><span data-stu-id="34ff6-177">It should match the default file type (that selected as the dialog opens).</span></span> <span data-ttu-id="34ff6-178">如果預設檔案類型為 " \* . \* " () 的所有檔案，則檔案可以是您選擇的副檔名。</span><span class="sxs-lookup"><span data-stu-id="34ff6-178">If the default file type is "\*.\*" (all files), the file can be an extension of your choice.</span></span> <span data-ttu-id="34ff6-179">如果使用者選擇不同的檔案類型，擴充功能會自動更新為與該檔案類型相關聯的第一個副檔名。</span><span class="sxs-lookup"><span data-stu-id="34ff6-179">If the user chooses a different file type, the extension automatically updates to the first file name extension associated with that file type.</span></span> <span data-ttu-id="34ff6-180">如果使用者選擇 " \* . \* " () 的所有檔案，則延伸模組會還原為其原始值。</span><span class="sxs-lookup"><span data-stu-id="34ff6-180">If the user chooses "\*.\*" (all files), then the extension reverts to its original value.</span></span>

<span data-ttu-id="34ff6-181">下列範例說明如何完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="34ff6-181">The following example illustrates how this was done above.</span></span>


```C++
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
```



### <a name="controlling-the-default-folder"></a><span data-ttu-id="34ff6-182">控制預設資料夾</span><span class="sxs-lookup"><span data-stu-id="34ff6-182">Controlling the Default Folder</span></span>

<span data-ttu-id="34ff6-183">Shell 命名空間中的任何資料夾都可以作為對話方塊的預設資料夾， (當使用者選擇開啟或儲存檔案) 時所顯示的資料夾。</span><span class="sxs-lookup"><span data-stu-id="34ff6-183">Almost any folder in the Shell namespace can be used as the default folder for the dialog (the folder presented when the user chooses to open or save a file).</span></span> <span data-ttu-id="34ff6-184">呼叫 [**IFileDialog：： SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) ，然後再呼叫 [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) 來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="34ff6-184">Call [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) to do so.</span></span>

<span data-ttu-id="34ff6-185">預設資料夾是在使用者第一次從您的應用程式開啟對話方塊時，對話方塊啟動的資料夾。</span><span class="sxs-lookup"><span data-stu-id="34ff6-185">The default folder is the folder in which the dialog starts the first time a user opens it from your application.</span></span> <span data-ttu-id="34ff6-186">之後，對話方塊會在使用者開啟的最後一個資料夾或用來儲存專案的最後一個資料夾中開啟。</span><span class="sxs-lookup"><span data-stu-id="34ff6-186">After that, the dialog will open in the last folder a user opened or the last folder they used to save an item.</span></span> <span data-ttu-id="34ff6-187">如需詳細資訊，請參閱 [狀態持續](#state-persistence) 性。</span><span class="sxs-lookup"><span data-stu-id="34ff6-187">See [State Persistence](#state-persistence) for more details.</span></span>

<span data-ttu-id="34ff6-188">您可以藉由呼叫 [**IFileDialog：： SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder)，強制對話方塊在開啟時一律顯示相同的資料夾（不論先前的使用者動作為何）。</span><span class="sxs-lookup"><span data-stu-id="34ff6-188">You can force the dialog to always show the same folder when it opens, regardless of previous user action, by calling [**IFileDialog::SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span></span> <span data-ttu-id="34ff6-189">不過，我們不建議這麼做。</span><span class="sxs-lookup"><span data-stu-id="34ff6-189">However, we do not recommended doing this.</span></span> <span data-ttu-id="34ff6-190">如果您在顯示對話方塊之前呼叫 **SetFolder** ，則不會顯示使用者所儲存或開啟的最新位置。</span><span class="sxs-lookup"><span data-stu-id="34ff6-190">If you call **SetFolder** before you display the dialog box, the most recent location that the user saved to or opened from is not shown.</span></span> <span data-ttu-id="34ff6-191">除非此行為有很明確的原因，否則它不是良好或預期的使用者經驗，應予以避免。</span><span class="sxs-lookup"><span data-stu-id="34ff6-191">Unless there is a very specific reason for this behavior, it is not a good or expected user experience and should be avoided.</span></span> <span data-ttu-id="34ff6-192">在幾乎所有的情況下， [**IFileDialog：： SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) 是較佳的方法。</span><span class="sxs-lookup"><span data-stu-id="34ff6-192">In almost all instances, [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) is the better method.</span></span>

<span data-ttu-id="34ff6-193">當您第一次在 [ **儲存** ] 對話方塊中儲存檔時，您應該遵循相同的指導方針來決定初始資料夾，就像在 [ **開啟** ] 對話方塊中所做的一樣。</span><span class="sxs-lookup"><span data-stu-id="34ff6-193">When saving a document for the first time in the **Save** dialog, you should follow the same guidelines in determining the initial folder as you did in the **Open** dialog.</span></span> <span data-ttu-id="34ff6-194">如果使用者正在編輯先前現有的檔，請在儲存該檔的資料夾中開啟對話方塊，然後在編輯方塊中填入該檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="34ff6-194">If the user is editing a previously existing document, open the dialog in the folder where that document is stored, and populate the edit box with that document's name.</span></span> <span data-ttu-id="34ff6-195">呼叫 [**IFileSaveDialog：： SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) 與目前的專案，然後再呼叫 [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show)。</span><span class="sxs-lookup"><span data-stu-id="34ff6-195">Call [**IFileSaveDialog::SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) with the current item prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span></span>

### <a name="adding-items-to-the-places-bar"></a><span data-ttu-id="34ff6-196">將專案加入至位置列</span><span class="sxs-lookup"><span data-stu-id="34ff6-196">Adding Items to the Places Bar</span></span>

<span data-ttu-id="34ff6-197">下列範例示範如何將專案加入至 **位置** 列：</span><span class="sxs-lookup"><span data-stu-id="34ff6-197">The following example demonstrates the addition of items to the **Places** bar:</span></span>


```C++
HRESULT AddItemsToCommonPlaces()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Always use known folders instead of hard-coding physical file paths.
        // In this case we are using Public Music KnownFolder.
        IKnownFolderManager *pkfm = NULL;
        hr = CoCreateInstance(CLSID_KnownFolderManager, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pkfm));
        if (SUCCEEDED(hr))
        {
            // Get the known folder.
            IKnownFolder *pKnownFolder = NULL;
            hr = pkfm->GetFolder(FOLDERID_PublicMusic, &pKnownFolder);
            if (SUCCEEDED(hr))
            {
                // File Dialog APIs need an IShellItem that represents the location.
                IShellItem *psi = NULL;
                hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                if (SUCCEEDED(hr))
                {
                    // Add the place to the bottom of default list in Common File Dialog.
                    hr = pfd->AddPlace(psi, FDAP_BOTTOM);
                    if (SUCCEEDED(hr))
                    {
                        // Show the File Dialog.
                        hr = pfd->Show(NULL);
                        if (SUCCEEDED(hr))
                        {
                            //
                            // You can add your own code here to handle the results.
                            //
                        }
                    }
                    psi->Release();
                }
                pKnownFolder->Release();
            }
            pkfm->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="state-persistence"></a><span data-ttu-id="34ff6-198">狀態持續性</span><span class="sxs-lookup"><span data-stu-id="34ff6-198">State Persistence</span></span>

<span data-ttu-id="34ff6-199">在 Windows Vista 之前，狀態（例如 [上次流覽的] 資料夾）是以每個進程為基礎進行儲存。</span><span class="sxs-lookup"><span data-stu-id="34ff6-199">Prior to Windows Vista, a state, such as the last visited folder, was saved on a per-process basis.</span></span> <span data-ttu-id="34ff6-200">不過，無論特定動作為何，都會使用該資訊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-200">However, that information was used regardless of the particular action.</span></span> <span data-ttu-id="34ff6-201">例如，影片編輯應用程式會在 [轉譯 **為** ] 對話方塊中顯示相同的資料夾，就像在 [匯 **入媒體** ] 對話方塊中一樣。</span><span class="sxs-lookup"><span data-stu-id="34ff6-201">For example, a video editing application would present the same folder in the **Render As** dialog as is would in the **Import Media** dialog.</span></span> <span data-ttu-id="34ff6-202">在 Windows Vista 中，您可以透過使用 Guid 來更加明確。</span><span class="sxs-lookup"><span data-stu-id="34ff6-202">In Windows Vista you can be more specific through the use of GUIDs.</span></span> <span data-ttu-id="34ff6-203">若要將 **GUID** 指派給對話，請呼叫 [**IFileDialog：： SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid)。</span><span class="sxs-lookup"><span data-stu-id="34ff6-203">To assign a **GUID** to the dialog, call [**iFileDialog::SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span></span>

### <a name="multiselect-capabilities"></a><span data-ttu-id="34ff6-204">多重複選功能</span><span class="sxs-lookup"><span data-stu-id="34ff6-204">Multiselect Capabilities</span></span>

<span data-ttu-id="34ff6-205">您可以使用 [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults)方法，在 [**開啟**] 對話方塊中找到多重複選功能，如下所示。</span><span class="sxs-lookup"><span data-stu-id="34ff6-205">Multiselect functionality is available in the **Open** dialog using the [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) method as shown here.</span></span>


```C++
HRESULT MultiselectInvoke()
{
    IFileOpenDialog *pfd;
    
    // CoCreate the dialog object.
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));

    if (SUCCEEDED(hr))
    {
        DWORD dwOptions;
        // Specify multiselect.
        hr = pfd->GetOptions(&dwOptions);
        
        if (SUCCEEDED(hr))
        {
            hr = pfd->SetOptions(dwOptions | FOS_ALLOWMULTISELECT);
        }

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog.
            hr = pfd->Show(NULL);

            if (SUCCEEDED(hr))
            {
                // Obtain the result of the user interaction.
                IShellItemArray *psiaResults;
                hr = pfd->GetResults(&psiaResults);
                
                if (SUCCEEDED(hr))
                {
                    //
                    // You can add your own code here to handle the results.
                    //
                    psiaResults->Release();
                }
            }
        }
        pfd->Release();
    }
    return hr;
}
```



## <a name="listening-to-events-from-the-dialog"></a><span data-ttu-id="34ff6-206">從對話方塊接聽事件</span><span class="sxs-lookup"><span data-stu-id="34ff6-206">Listening to Events from the Dialog</span></span>

<span data-ttu-id="34ff6-207">呼叫進程可以使用 [**IFileDialog：： Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise)和 [**IFileDialog：： Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise)方法，以對話方塊註冊 [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)介面，如下所示。</span><span class="sxs-lookup"><span data-stu-id="34ff6-207">A calling process can register an [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) interface with the dialog by using the [**IFileDialog::Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) and [**IFileDialog::Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) methods as shown here.</span></span>

<span data-ttu-id="34ff6-208">這是取自 [基本使用](#basic-usage) 範例。</span><span class="sxs-lookup"><span data-stu-id="34ff6-208">This is taken from the [Basic Usage](#basic-usage) sample.</span></span>


```C++
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
```



<span data-ttu-id="34ff6-209">大部分的對話處理都是放在這裡。</span><span class="sxs-lookup"><span data-stu-id="34ff6-209">The bulk of the dialog processing would be placed here.</span></span>


```C++
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



<span data-ttu-id="34ff6-210">當使用者變更資料夾、檔案類型或選取專案時，呼叫進程可以使用事件來進行通知。</span><span class="sxs-lookup"><span data-stu-id="34ff6-210">The calling process can use events for notification when the user changes the folder, file type, or selection.</span></span> <span data-ttu-id="34ff6-211">當呼叫進程已將控制項新增至對話方塊時，這些事件特別有用 (請參閱 [自訂對話方塊](#customizing-the-dialog)) ，而且必須變更這些控制項的狀態，以回應這些事件。</span><span class="sxs-lookup"><span data-stu-id="34ff6-211">These events are particularly useful when the calling process has added controls to the dialog (see [Customizing the Dialog](#customizing-the-dialog)) and must change the state of those controls in reaction to these events.</span></span> <span data-ttu-id="34ff6-212">在所有情況下都很有用，那就是呼叫進程提供自訂程式碼來處理狀況的功能，例如共用違規、覆寫檔案，或在對話方塊關閉之前判斷檔案是否有效。</span><span class="sxs-lookup"><span data-stu-id="34ff6-212">Useful in all cases is the ability of the calling process to provide custom code to deal with situations such as sharing violations, overwriting files, or determining if a file is valid before the dialog closes.</span></span> <span data-ttu-id="34ff6-213">本節將說明其中一些案例。</span><span class="sxs-lookup"><span data-stu-id="34ff6-213">Some of those cases are described in this section.</span></span>

### <a name="onfileok"></a><span data-ttu-id="34ff6-214">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="34ff6-214">OnFileOk</span></span>

<span data-ttu-id="34ff6-215">當使用者選擇專案之後，就會呼叫這個方法，就在對話方塊關閉之前。</span><span class="sxs-lookup"><span data-stu-id="34ff6-215">This method is called after the user chooses an item, just before the dialog closes.</span></span> <span data-ttu-id="34ff6-216">然後，應用程式可以呼叫 [**IFileDialog：： GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) 或 [**IFileOpenDialog：： GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) ，就像在對話方塊關閉後才會完成。</span><span class="sxs-lookup"><span data-stu-id="34ff6-216">The application can then call [**IFileDialog::GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) or [**IFileOpenDialog::GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) as would be done once the dialog had closed.</span></span> <span data-ttu-id="34ff6-217">如果選擇的專案是可接受的，則可以傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="34ff6-217">If the item chosen is acceptable, they can return S\_OK.</span></span> <span data-ttu-id="34ff6-218">否則，它們會傳回 \_ FALSE 和顯示 UI，告訴使用者為何選擇的專案無效。</span><span class="sxs-lookup"><span data-stu-id="34ff6-218">Otherwise, they return S\_FALSE and display UI that tells the user why the chosen item is not valid.</span></span> <span data-ttu-id="34ff6-219">如果 \_ 傳回 FALSE，則不會關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-219">If S\_FALSE is returned, the dialog does not close.</span></span>

<span data-ttu-id="34ff6-220">呼叫進程可以使用對話方塊本身的視窗控制碼作為 UI 的父系。</span><span class="sxs-lookup"><span data-stu-id="34ff6-220">The calling process can use the window handle of the dialog itself as the parent of the UI.</span></span> <span data-ttu-id="34ff6-221">您可以先呼叫 [**IOleWindow：： QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) 來取得該控制碼，然後使用此範例所示的控制碼來呼叫 [**IOleWindow：： GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) 。</span><span class="sxs-lookup"><span data-stu-id="34ff6-221">That handle can be obtained by first calling [**IOleWindow::QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) and then calling [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) with the handle as shown in this example.</span></span>


```C++
HRESULT CDialogEventHandler::OnFileOk(IFileDialog *pfd) 
{ 
    IShellItem *psiResult;
    HRESULT hr = pfd->GetResult(&psiResult);
    
    if (SUCCEEDED(hr))
    {
        SFGAOF attributes;
        hr = psiResult->GetAttributes(SFGAO_COMPRESSED, &attributes);
    
        if (SUCCEEDED(hr))
        {
            if (attributes & SFGAO_COMPRESSED)
            {
                // Accept the file.
                hr = S_OK;
            }
            else
            {
                // Refuse the file.
                hr = S_FALSE;
                
                _DisplayMessage(pfd, L"Not a compressed file.");
            }
        }
        psiResult->Release();
    }
    return hr;
};

HRESULT CDialogEventHandler::_DisplayMessage(IFileDialog *pfd, PCWSTR pszMessage)
{
    IOleWindow *pWindow;
    HRESULT hr = pfd->QueryInterface(IID_PPV_ARGS(&pWindow));
    
    if (SUCCEEDED(hr))
    {
        HWND hwndDialog;
        hr = pWindow->GetWindow(&hwndDialog);
    
        if (SUCCEEDED(hr))
        {
            MessageBox(hwndDialog, pszMessage, L"An error has occurred", MB_OK);
        }
        pWindow->Release();
    }
    return hr;
}
```



### <a name="onshareviolation-and-onoverwrite"></a><span data-ttu-id="34ff6-222">OnShareViolation 和 OnOverwrite</span><span class="sxs-lookup"><span data-stu-id="34ff6-222">OnShareViolation and OnOverwrite</span></span>

<span data-ttu-id="34ff6-223">如果使用者選擇要在 [ **儲存** ] 對話方塊中覆寫檔案，或正在儲存或取代的檔案正在使用中，而且無法寫入 (共用違規) ，則應用程式可以提供自訂功能來覆寫對話方塊的預設行為。</span><span class="sxs-lookup"><span data-stu-id="34ff6-223">If the user chooses to overwrite a file in the **Save** dialog, or if a file being saved or replaced is in use and cannot be written to (a sharing violation), the application can provide custom functionality to override the default behavior of the dialog.</span></span> <span data-ttu-id="34ff6-224">根據預設，覆寫檔案時，對話方塊會顯示提示，讓使用者驗證此動作。</span><span class="sxs-lookup"><span data-stu-id="34ff6-224">By default, when overwriting a file, the dialog displays a prompt allowing the user to verify this action.</span></span> <span data-ttu-id="34ff6-225">對於共用違規，對話方塊預設會顯示錯誤訊息，而不會關閉，而且使用者必須進行其他選擇。</span><span class="sxs-lookup"><span data-stu-id="34ff6-225">For sharing violations, by default the dialog displays an error message, it does not close, and the user is required to make another choice.</span></span> <span data-ttu-id="34ff6-226">呼叫進程可以覆寫這些預設值，並視需要顯示自己的 UI。</span><span class="sxs-lookup"><span data-stu-id="34ff6-226">The calling process can override these defaults and display its own UI if desired.</span></span> <span data-ttu-id="34ff6-227">您可以指示對話方塊拒絕檔案，並保持開啟或接受檔案並成功關閉。</span><span class="sxs-lookup"><span data-stu-id="34ff6-227">The dialog can be instructed to refuse the file and remain open or accept the file and close successfully.</span></span>

## <a name="customizing-the-dialog"></a><span data-ttu-id="34ff6-228">自訂對話方塊</span><span class="sxs-lookup"><span data-stu-id="34ff6-228">Customizing the Dialog</span></span>

<span data-ttu-id="34ff6-229">您可以將各種控制項新增至對話方塊，而不需要提供 Win32 對話方塊範本。</span><span class="sxs-lookup"><span data-stu-id="34ff6-229">A variety of controls can be added to the dialog without supplying a Win32 dialog template.</span></span> <span data-ttu-id="34ff6-230">這些控制項包括按鈕、ComboBox、編輯方塊、CheckButton、選項按鈕清單、群組、分隔符號和靜態文字控制項。</span><span class="sxs-lookup"><span data-stu-id="34ff6-230">These controls include PushButton, ComboBox, EditBox, CheckButton, RadioButton lists, Groups, Separators, and Static Text controls.</span></span> <span data-ttu-id="34ff6-231">呼叫 ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog)、 [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)或 [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) 的對話方塊物件上的 **QueryInterface** ，以取得 [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)指標。</span><span class="sxs-lookup"><span data-stu-id="34ff6-231">Call **QueryInterface** on the dialog object ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), or [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) to obtain an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer.</span></span> <span data-ttu-id="34ff6-232">使用該介面來新增控制項。</span><span class="sxs-lookup"><span data-stu-id="34ff6-232">Use that interface to add controls.</span></span> <span data-ttu-id="34ff6-233">每個控制項都有相關聯的呼叫端提供的識別碼，以及可由呼叫進程設定的 *可見* 和 *已啟用* 狀態。</span><span class="sxs-lookup"><span data-stu-id="34ff6-233">Each control has an associated caller-supplied ID as well as a *visible* and *enabled* state that can be set by the calling process.</span></span> <span data-ttu-id="34ff6-234">某些控制項（例如按鈕）也有相關聯的文字。</span><span class="sxs-lookup"><span data-stu-id="34ff6-234">Some controls, such as PushButton, also have text associated with them.</span></span>

<span data-ttu-id="34ff6-235">您可以將多個控制項加入至「視覺效果群組」中，以在對話方塊的版面配置中以單一單位移動。</span><span class="sxs-lookup"><span data-stu-id="34ff6-235">Multiple controls can be added into a "visual group" that moves as a single unit in the layout of the dialog.</span></span> <span data-ttu-id="34ff6-236">群組可以有與其相關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="34ff6-236">Groups can have a label associated with them.</span></span>

<span data-ttu-id="34ff6-237">只有在顯示對話方塊之前，才可以加入控制項。</span><span class="sxs-lookup"><span data-stu-id="34ff6-237">Controls can be added only before the dialog is shown.</span></span> <span data-ttu-id="34ff6-238">不過，一旦出現對話方塊，就可以視需要隱藏或顯示控制項，以回應使用者動作。</span><span class="sxs-lookup"><span data-stu-id="34ff6-238">However, once the dialog is displayed, controls can be hidden or shown as desired, perhaps in response to user action.</span></span> <span data-ttu-id="34ff6-239">下列範例示範如何將選項按鈕清單新增至對話方塊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-239">The following examples show how to add a radio button list to the dialog.</span></span>


```C++
// Controls
#define CONTROL_GROUP           2000
#define CONTROL_RADIOBUTTONLIST 2
#define CONTROL_RADIOBUTTON1    1
#define CONTROL_RADIOBUTTON2    2       // It is OK for this to have the same ID
                    // as CONTROL_RADIOBUTTONLIST, because it 
                    // is a child control under CONTROL_RADIOBUTTONLIST


// This code snippet demonstrates how to add custom controls in the Common File Dialog.
HRESULT AddCustomControls()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    // Create a Visual Group.
                    hr = pfdc->StartVisualGroup(CONTROL_GROUP, L&quot;Sample Group&quot;);
                    if (SUCCEEDED(hr))
                    {
                        // Add a radio-button list.
                        hr = pfdc->AddRadioButtonList(CONTROL_RADIOBUTTONLIST);
                        if (SUCCEEDED(hr))
                        {
                            // Set the state of the added radio-button list.
                            hr = pfdc->SetControlState(CONTROL_RADIOBUTTONLIST, 
                                               CDCS_VISIBLE | CDCS_ENABLED);
                            if (SUCCEEDED(hr))
                            {
                                // Add individual buttons to the radio-button list.
                                hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                          CONTROL_RADIOBUTTON1,
                                                          L&quot;Change Title to ABC&quot;);
                                if (SUCCEEDED(hr))
                                {
                                    hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                              CONTROL_RADIOBUTTON2,
                                                              L&quot;Change Title to XYZ&quot;);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Set the default selection to option 1.
                                        hr = pfdc->SetSelectedControlItem(CONTROL_RADIOBUTTONLIST,
                                                                          CONTROL_RADIOBUTTON1);
                                    }
                                }
                            }
                        }
                        // End the visual group.
                        pfdc->EndVisualGroup();
                    }
                    pfdc->Release();
                }

                if (FAILED(hr))
                {
                    // Unadvise here in case we encounter failures 
                    // before we get a chance to show the dialog.
                    pfd->Unadvise(dwCookie);
                }
            }
            pfde->Release();
        }

        if (SUCCEEDED(hr))
        {
            // Now show the dialog.
            hr = pfd->Show(NULL);
            if (SUCCEEDED(hr))
            {
                //
                // You can add your own code here to handle the results.
                //
            }
            // Unhook the event handler.
            pfd->Unadvise(dwCookie);
        }
        pfd->Release();
    }
    return hr;
}
```





### <a name="adding-options-to-the-ok-button"></a><span data-ttu-id="34ff6-240">將選項新增至 [確定] 按鈕</span><span class="sxs-lookup"><span data-stu-id="34ff6-240">Adding Options to the OK Button</span></span>

<span data-ttu-id="34ff6-241">同樣地，您也可以將選擇新增至 [ **開啟** ] 或 [ **儲存** ] 按鈕，這是其各自對話方塊類型的 **[確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="34ff6-241">Similarly, choices can be added to the **Open** or **Save** buttons, which are the **OK** button for their respective dialog types.</span></span> <span data-ttu-id="34ff6-242">您可以透過附加至按鈕的下拉式清單方塊來存取這些選項。</span><span class="sxs-lookup"><span data-stu-id="34ff6-242">The options are accessible through a drop-down list box attached to the button.</span></span> <span data-ttu-id="34ff6-243">清單中的第一個專案會變成按鈕的文字。</span><span class="sxs-lookup"><span data-stu-id="34ff6-243">The first item in the list becomes the text for the button.</span></span> <span data-ttu-id="34ff6-244">下列範例示範如何提供有兩種可能性的 **開啟** 按鈕：「開啟」和「以唯讀方式開啟」。</span><span class="sxs-lookup"><span data-stu-id="34ff6-244">The following example shows how to provide an **Open** button with two possibilities: "Open" and "Open as read-only".</span></span>


```C++
// OpenChoices options
#define OPENCHOICES 0
#define OPEN 0
#define OPEN_AS_READONLY 1


HRESULT AddOpenChoices()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    hr = pfdc->EnableOpenDropDown(OPENCHOICES);
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, OPEN, L&quot;&Open&quot;);
                    }                    
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, 
                                                OPEN_AS_READONLY, 
                                                L&quot;Open as &read-only&quot;);
                    }
                    if (SUCCEEDED(hr))
                    {
                        pfd->Show(NULL);
                    }
                }
                pfdc->Release();
            }
            pfd->Unadvise(dwCookie);
        }
        pfde->Release();
    }
    pfd->Release();
    return hr;
}
```





<span data-ttu-id="34ff6-245">使用者的選擇可以在對話方塊從 Show 方法傳回後，如同您針對 ComboBox 所做的一樣驗證，也可以 [**透過**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) [**IFileDialogEvents：： OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok)確認為處理的一部分。</span><span class="sxs-lookup"><span data-stu-id="34ff6-245">The user's choice can be verified after the dialog returns from the [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) method as you would for a ComboBox, or it can verified as part of the handling by [**IFileDialogEvents::OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span></span>

### <a name="responding-to-events-in-added-controls"></a><span data-ttu-id="34ff6-246">回應新增控制項中的事件</span><span class="sxs-lookup"><span data-stu-id="34ff6-246">Responding to Events in Added Controls</span></span>

<span data-ttu-id="34ff6-247">除了 [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents)以外，呼叫進程所提供的事件處理常式還可以執行 [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) 。</span><span class="sxs-lookup"><span data-stu-id="34ff6-247">The events handler provided by the calling process can implement [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) in addition to [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span></span> <span data-ttu-id="34ff6-248">**IFileDialogControlEvents** 可讓呼叫進程回應這些事件：</span><span class="sxs-lookup"><span data-stu-id="34ff6-248">**IFileDialogControlEvents** enables the calling process to react to these events:</span></span>

-   <span data-ttu-id="34ff6-249">按一下按鈕</span><span class="sxs-lookup"><span data-stu-id="34ff6-249">PushButton clicked</span></span>
-   <span data-ttu-id="34ff6-250">CheckButton 狀態已變更</span><span class="sxs-lookup"><span data-stu-id="34ff6-250">CheckButton state changed</span></span>
-   <span data-ttu-id="34ff6-251">從功能表、ComboBox 或選項按鈕清單中選取的專案</span><span class="sxs-lookup"><span data-stu-id="34ff6-251">Item selected from a menu, ComboBox, or RadioButton list</span></span>
-   <span data-ttu-id="34ff6-252">控制啟用。</span><span class="sxs-lookup"><span data-stu-id="34ff6-252">Control activating.</span></span> <span data-ttu-id="34ff6-253">當呼叫進程想要變更清單中的專案時，當功能表即將顯示下拉式清單時，就會傳送這項資訊。</span><span class="sxs-lookup"><span data-stu-id="34ff6-253">This is sent when a menu is about to display a drop-down list, in case the calling process wants to change the items in the list.</span></span>

## <a name="full-samples"></a><span data-ttu-id="34ff6-254">完整範例</span><span class="sxs-lookup"><span data-stu-id="34ff6-254">Full Samples</span></span>

<span data-ttu-id="34ff6-255">以下是 Windows 軟體開發套件 () SDK 的完整可下載 c + + 範例，其示範如何使用和與 [一般專案] 對話方塊的互動。</span><span class="sxs-lookup"><span data-stu-id="34ff6-255">The following are complete, downloadable C++ samples from the Windows Software Development Kit (SDK) which demonstrate the use of and interaction with the Common Item Dialog.</span></span>

-   [<span data-ttu-id="34ff6-256">一般檔案對話方塊範例</span><span class="sxs-lookup"><span data-stu-id="34ff6-256">Common File Dialog Sample</span></span>](samples-commonfiledialog.md)
-   [<span data-ttu-id="34ff6-257">一般檔案對話方塊模式範例</span><span class="sxs-lookup"><span data-stu-id="34ff6-257">Common File Dialog Modes Sample</span></span>](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a><span data-ttu-id="34ff6-258">相關主題</span><span class="sxs-lookup"><span data-stu-id="34ff6-258">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34ff6-259">**IID \_ PPV 引數 \_**</span><span class="sxs-lookup"><span data-stu-id="34ff6-259">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
