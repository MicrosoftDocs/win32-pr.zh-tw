---
description: 為了確保您的資料已編制索引，並在搜尋期間正確呈現給使用者，您需要執行 Shell 資料存放區 (也稱為 Shell 命名空間延伸模組) ，以及檔案類型處理常式 (也稱為 Shell 擴充、延伸模組處理常式或 Shell 延伸模組處理常式) 。
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: 新增圖示、預覽和快捷方式功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511106"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a><span data-ttu-id="3ed1e-103">新增圖示、預覽和快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="3ed1e-103">Adding Icons, Previews and Shortcut Menus</span></span>

<span data-ttu-id="3ed1e-104">為了確保您的資料已編制索引，並在搜尋期間正確呈現給使用者，您需要執行 Shell 資料存放區 (也稱為 [Shell 命名空間延伸](../shell/nse-works.md) 模組) ，以及檔案類型處理常式 (也稱為 shell 擴充、 [延伸模組處理](../shell/handlers.md)程式或 shell 延伸模組處理常式) 。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-104">To ensure that your data is indexed and presented correctly to the user during searches, you need to implement Shell data stores (also known as [Shell Namespace Extensions](../shell/nse-works.md)), and file type handlers (also known as Shell extensions, [extension handlers](../shell/handlers.md), or Shell extension handlers).</span></span>

<span data-ttu-id="3ed1e-105">本主題說明下列介面：</span><span class="sxs-lookup"><span data-stu-id="3ed1e-105">This topic describes the following interfaces:</span></span>

-   [<span data-ttu-id="3ed1e-106">執行檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="3ed1e-106">Implementing File Type Handlers</span></span>](#implementing-file-type-handlers)
    -   [<span data-ttu-id="3ed1e-107">IPersist</span><span class="sxs-lookup"><span data-stu-id="3ed1e-107">IPersist</span></span>](#ipersist)
    -   [<span data-ttu-id="3ed1e-108">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="3ed1e-108">IPersistFolder</span></span>](#ipersistfolder)
    -   [<span data-ttu-id="3ed1e-109">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="3ed1e-109">IShellFolder</span></span>](#ishellfolder)
    -   [<span data-ttu-id="3ed1e-110">ICoNtextMenu</span><span class="sxs-lookup"><span data-stu-id="3ed1e-110">IContextMenu</span></span>](#icontextmenu)
    -   [<span data-ttu-id="3ed1e-111">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="3ed1e-111">IExtractIcon</span></span>](#iextracticon)
    -   [<span data-ttu-id="3ed1e-112">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="3ed1e-112">IPreviewHandler</span></span>](#ipreviewhandler)
-   [<span data-ttu-id="3ed1e-113">其他資源</span><span class="sxs-lookup"><span data-stu-id="3ed1e-113">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="3ed1e-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ed1e-114">Related topics</span></span>](#related-topics)

## <a name="implementing-file-type-handlers"></a><span data-ttu-id="3ed1e-115">執行檔案類型處理常式</span><span class="sxs-lookup"><span data-stu-id="3ed1e-115">Implementing File Type Handlers</span></span>

<span data-ttu-id="3ed1e-116">這些 Shell 擴充或檔案類型處理常式可為您的使用者提供下列 Shell 體驗：</span><span class="sxs-lookup"><span data-stu-id="3ed1e-116">These Shell extensions or file type handlers provide your users with the following Shell experiences:</span></span>

-   <span data-ttu-id="3ed1e-117">結果檢視會顯示您專案類型的特定圖示。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-117">The results view displays a specific icon for your item type.</span></span>
-   <span data-ttu-id="3ed1e-118">當使用者選取專案時，結果檢視會顯示專案的預覽。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-118">The results view displays a preview of the item when the user selects the item.</span></span>
-   <span data-ttu-id="3ed1e-119">使用者可以按兩下專案來起始事件，例如開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-119">Users can double-click items to initiate events such as opening the file.</span></span>
-   <span data-ttu-id="3ed1e-120">使用者可以滑鼠右鍵按一下專案，以存取快捷方式 (內容) 功能表。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-120">Users can right-click items to access a shortcut (context) menu.</span></span>
-   <span data-ttu-id="3ed1e-121">使用者可以拖放專案。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-121">Users can drag-and-drop items.</span></span>

<span data-ttu-id="3ed1e-122">如同所有元件物件模型 (COM) 物件，檔案類型處理常式必須執行 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面和 class factory。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-122">Like all Component Object Model (COM) objects, file type handlers must implement an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface and a class factory.</span></span>

<span data-ttu-id="3ed1e-123">在 Windows XP 或更早版本中，處理常式也應該執行：</span><span class="sxs-lookup"><span data-stu-id="3ed1e-123">In Windows XP or earlier, handlers should also implement:</span></span>

-   <span data-ttu-id="3ed1e-124">任一個 [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span><span class="sxs-lookup"><span data-stu-id="3ed1e-124">Either [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile)</span></span>
-   <span data-ttu-id="3ed1e-125">或 [IShellExtInit 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span><span class="sxs-lookup"><span data-stu-id="3ed1e-125">Or [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)</span></span>

<span data-ttu-id="3ed1e-126">在 Windows Vista 中， [IPersistFile 介面](/windows/win32/api/objidl/nn-objidl-ipersistfile) 和 [IShellExtInit 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 已取代為 Shell 用來初始化處理常式的下列三個介面：</span><span class="sxs-lookup"><span data-stu-id="3ed1e-126">In Windows Vista, [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [IShellExtInit Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) were replaced by the following three interfaces for Shell to initialize the handler:</span></span>

-   [<span data-ttu-id="3ed1e-127">IInitializeWithStream 介面</span><span class="sxs-lookup"><span data-stu-id="3ed1e-127">IInitializeWithStream Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="3ed1e-128">IInitializeWithItem 介面</span><span class="sxs-lookup"><span data-stu-id="3ed1e-128">IInitializeWithItem Interface</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="3ed1e-129">IInitializeWithFile 介面</span><span class="sxs-lookup"><span data-stu-id="3ed1e-129">IInitializeWithFile Interface</span></span>](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="3ed1e-130">若要提供合理的使用者體驗，您必須使用您的通訊協定處理常式來提供 Shell 資料存放區。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-130">To provide a reasonable user experience you must provide a Shell data store with your protocol handler.</span></span> <span data-ttu-id="3ed1e-131">然後該資料存放區會作為圖示處理常式、快捷方式功能表處理常式、預覽處理常式等的「factory」。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-131">That data store then serves as the "factory" for icon handlers, shortcut menu handlers, preview handlers, and so forth.</span></span> <span data-ttu-id="3ed1e-132">[IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)需要最基本的[IPersist 介面](/windows/desktop/api/objidl/nn-objidl-ipersist)和[IPersistFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)，而且[ICoNtextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)和[IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)需要最基本的 IShellFolder 介面實作為。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-132">Minimal implementations of [IPersist Interface](/windows/desktop/api/objidl/nn-objidl-ipersist) and [IPersistFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) are required by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), and a minimal implementation of IShellFolder Interface is required for the [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) and [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).</span></span>

> [!Note]  
> <span data-ttu-id="3ed1e-133">應針對 **IPersist**、 **IPersistFolder** 和 **IShellFolder** 執行相同的類別識別碼 (CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-133">The same class identifier (CLSID) should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="3ed1e-134">如需建立 Shell 資料存放區以支援通訊協定處理常式的詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-134">For more information about creating a Shell data store to support a protocol handler, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

### <a name="ipersist"></a><span data-ttu-id="3ed1e-135">IPersist</span><span class="sxs-lookup"><span data-stu-id="3ed1e-135">IPersist</span></span>

<span data-ttu-id="3ed1e-136">**IPersist** 介面會定義單一方法 **GetClassID**，其設計目的是要提供可持續儲存在系統中之物件的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-136">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="3ed1e-137">方法</span><span class="sxs-lookup"><span data-stu-id="3ed1e-137">Method</span></span>     | <span data-ttu-id="3ed1e-138">描述</span><span class="sxs-lookup"><span data-stu-id="3ed1e-138">Description</span></span>                                      |
|------------|--------------------------------------------------|
| <span data-ttu-id="3ed1e-139">GetClassID</span><span class="sxs-lookup"><span data-stu-id="3ed1e-139">GetClassID</span></span> | <span data-ttu-id="3ed1e-140">傳回 Shell 資料存放區物件的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-140">Returns the CLSID of the Shell data store object</span></span> |



 

### <a name="ipersistfolder"></a><span data-ttu-id="3ed1e-141">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="3ed1e-141">IPersistFolder</span></span>

<span data-ttu-id="3ed1e-142">**IPersistFolder** 介面是用來初始化 Shell 資料夾物件。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-142">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="3ed1e-143">此介面的實作為衍生自 **IPersist** 的介面，是資料夾在 Shell 命名空間中的通知位置。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-143">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span> <span data-ttu-id="3ed1e-144">您不會直接使用此介面。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-144">You do not use this interface directly.</span></span> <span data-ttu-id="3ed1e-145">它是由 [IShellFolder：： BindToObject 方法](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) 的檔案系統實作為初始化 Shell 資料夾物件時使用。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-145">It is used by the file system implementation of [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) when it initializes a Shell folder object.</span></span>



| <span data-ttu-id="3ed1e-146">方法</span><span class="sxs-lookup"><span data-stu-id="3ed1e-146">Method</span></span>     | <span data-ttu-id="3ed1e-147">描述</span><span class="sxs-lookup"><span data-stu-id="3ed1e-147">Description</span></span>                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed1e-148">初始化</span><span class="sxs-lookup"><span data-stu-id="3ed1e-148">Initialize</span></span> | <span data-ttu-id="3ed1e-149">指示 Shell 資料夾物件根據傳遞的資訊進行初始化，並傳回 S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="3ed1e-149">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

### <a name="ishellfolder"></a><span data-ttu-id="3ed1e-150">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="3ed1e-150">IShellFolder</span></span>

<span data-ttu-id="3ed1e-151">[IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面是用來管理資料夾，而且需要部分執行，如此一來，針對通訊協定處理常式所執行的圖示和內容介面在 Windows Search 結果使用者介面中的運作方式會正確。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-151">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Search results user interface.</span></span> <span data-ttu-id="3ed1e-152">需要的大部分功能都是透過 **GetUIObjectOf** 方法來公開。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-152">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="3ed1e-153">這個方法可讓增益集查詢 **IExtractIcon** 和 **ICoNtextMenu** 介面。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-153">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="3ed1e-154">[IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面會使用 pidl 而非 url。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-154">The [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="3ed1e-155">相對於完整 Shell 資料存放區的需求，增益集可以使用只包含 URL 的簡單 IDL 結構。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-155">In contrast to the requirements of a complete Shell data store, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="3ed1e-156">您必須執行下列 [IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 的方法。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-156">The following methods of [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) must be implemented.</span></span> <span data-ttu-id="3ed1e-157">其中五種方法需要進行基本的執行。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-157">Five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="3ed1e-158">方法</span><span class="sxs-lookup"><span data-stu-id="3ed1e-158">Method</span></span>           | <span data-ttu-id="3ed1e-159">描述</span><span class="sxs-lookup"><span data-stu-id="3ed1e-159">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed1e-160">BindToObject</span><span class="sxs-lookup"><span data-stu-id="3ed1e-160">BindToObject</span></span>     | <span data-ttu-id="3ed1e-161">傳回 E \_ >notimpl</span><span class="sxs-lookup"><span data-stu-id="3ed1e-161">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ed1e-162">BindToStorage</span><span class="sxs-lookup"><span data-stu-id="3ed1e-162">BindToStorage</span></span>    | <span data-ttu-id="3ed1e-163">傳回 E \_ >notimpl</span><span class="sxs-lookup"><span data-stu-id="3ed1e-163">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ed1e-164">CreateViewObject</span><span class="sxs-lookup"><span data-stu-id="3ed1e-164">CreateViewObject</span></span> | <span data-ttu-id="3ed1e-165">傳回 E \_ >notimpl</span><span class="sxs-lookup"><span data-stu-id="3ed1e-165">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ed1e-166">SetNameOf</span><span class="sxs-lookup"><span data-stu-id="3ed1e-166">SetNameOf</span></span>        | <span data-ttu-id="3ed1e-167">傳回 E \_ >notimpl</span><span class="sxs-lookup"><span data-stu-id="3ed1e-167">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3ed1e-168">ParseDisplayName</span><span class="sxs-lookup"><span data-stu-id="3ed1e-168">ParseDisplayName</span></span> | <span data-ttu-id="3ed1e-169">將 URL 轉換成 PIDL 結構</span><span class="sxs-lookup"><span data-stu-id="3ed1e-169">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="3ed1e-170">CompareIDs</span><span class="sxs-lookup"><span data-stu-id="3ed1e-170">CompareIDs</span></span>       | <span data-ttu-id="3ed1e-171">比較兩個 PIDL 值</span><span class="sxs-lookup"><span data-stu-id="3ed1e-171">Compares two PIDL values</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3ed1e-172">GetDisplayNameOf</span><span class="sxs-lookup"><span data-stu-id="3ed1e-172">GetDisplayNameOf</span></span> | <span data-ttu-id="3ed1e-173">傳回 PIDL 的 URL。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-173">Returns the URL for a PIDL</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3ed1e-174">GetUIObjectOf</span><span class="sxs-lookup"><span data-stu-id="3ed1e-174">GetUIObjectOf</span></span>    | <span data-ttu-id="3ed1e-175">這個方法類似 [IUnknown：： QueryInterface 方法](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-175">This method is similar to the [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="3ed1e-176">如果要求圖示，呼叫端會要求 IID \_ IExtractIcon; 如果要求快捷方式功能表，則呼叫端會要求 iid \_ ICoNtextMenu</span><span class="sxs-lookup"><span data-stu-id="3ed1e-176">If an icon is requested, the caller requests the IID\_IExtractIcon; if a shortcut menu is requested, the caller requests the IID\_IContextMenu</span></span> |



 

<span data-ttu-id="3ed1e-177">**IShellFolder** 不會用來列舉資料夾。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-177">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="3ed1e-178">這表示資料夾的顯示名稱將會是實體 URL。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-178">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="3ed1e-179">未來可能會變更。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-179">This may change in the future.</span></span>

### <a name="icontextmenu"></a><span data-ttu-id="3ed1e-180">ICoNtextMenu</span><span class="sxs-lookup"><span data-stu-id="3ed1e-180">IContextMenu</span></span>

<span data-ttu-id="3ed1e-181">當 Windows Search 向使用者顯示結果時，使用者可以在專案上按一下滑鼠右鍵，並查看 **ICoNtextMenu** 介面所定義的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-181">When Windows Search displays results to the user, the user can right-click an item and see a shortcut menu defined by your **IContextMenu** interface.</span></span> <span data-ttu-id="3ed1e-182">快速鍵功能表也稱為內容功能表。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-182">Shortcut menus are also known as context menus.</span></span>

<span data-ttu-id="3ed1e-183">操作功能表上的預設動作，與按兩下專案時所採取的動作相同。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-183">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="3ed1e-184">如果專案沒有對應的 **IShellFolder** 或 **ICoNtextMenu** 介面，則按兩下事件的預設行為是將 URL 當作引數傳遞至 [ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) 函式函數。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-184">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the [ShellExecute Function](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function.</span></span>

<span data-ttu-id="3ed1e-185">如需有關建立快捷方式功能表處理常式的詳細資訊，以及範例程式碼之[通訊協定處理常式的範例： Shell 擴充](-search-3x-wds-ph-ui-samplecode.md)功能，請參閱[建立內容功能表處理常式](../shell/context-menu-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-185">Refer to [Creating Context Menu Handlers](../shell/context-menu-handlers.md) for more information on creating shortcut menu handlers, and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="iextracticon"></a><span data-ttu-id="3ed1e-186">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="3ed1e-186">IExtractIcon</span></span>

<span data-ttu-id="3ed1e-187">**IExtractIcon** 會根據您的通訊協定處理常式所提供的 PIDL 中的 URL，來抓取 Windows Search 使用者介面的圖示。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-187">**IExtractIcon** retrieves an icon for the Windows Search user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

<span data-ttu-id="3ed1e-188">如需有關如何建立圖示處理常式和範例：適用于程式碼範例的[通訊協定處理常式的 Shell 擴充](-search-3x-wds-ph-ui-samplecode.md)功能，請參閱[建立圖示處理常式](../shell/how-to-create-icon-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-188">Refer to [Creating Icon Handlers](../shell/how-to-create-icon-handlers.md) for more information on creating icon handlers and [Sample: Shell Extensions for Protocol Handlers](-search-3x-wds-ph-ui-samplecode.md) for sample code.</span></span>

### <a name="ipreviewhandler"></a><span data-ttu-id="3ed1e-189">IPreviewHandler</span><span class="sxs-lookup"><span data-stu-id="3ed1e-189">IPreviewHandler</span></span>

<span data-ttu-id="3ed1e-190">[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)會呈現 Windows 檔案總管中所選取專案的豐富預覽。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-190">The [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) renders a rich preview of a selected item in Windows Explorer.</span></span> <span data-ttu-id="3ed1e-191">預覽適用于 Windows Search 4.0，或在 Windows Vista 中，使用 Windows Desktop Search 3.x。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-191">Previews are available in Windows Search 4.0, or in Windows Vista with Windows Desktop Search 3.x.</span></span>

<span data-ttu-id="3ed1e-192">若要建立自訂預覽處理常式：</span><span class="sxs-lookup"><span data-stu-id="3ed1e-192">To create a custom preview handler:</span></span>

1.  <span data-ttu-id="3ed1e-193">遵循[預覽處理常式](../shell/preview-handlers.md)中提供的指導方針，來執行採用[IStream](/windows/win32/api/objidl/nn-objidl-istream)的[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) 。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-193">Implement an [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) that takes an [IStream](/windows/win32/api/objidl/nn-objidl-istream), following the guidelines provided in [Preview Handlers](../shell/preview-handlers.md).</span></span>
2.  <span data-ttu-id="3ed1e-194">註冊您的預覽處理常式：</span><span class="sxs-lookup"><span data-stu-id="3ed1e-194">Register your preview handler:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  <span data-ttu-id="3ed1e-195">完成下列兩個步驟，以針對您的 URL 執行 Shell 資料夾：</span><span class="sxs-lookup"><span data-stu-id="3ed1e-195">Complete the following two steps to implement a Shell folder for your URL:</span></span>
    1.  <span data-ttu-id="3ed1e-196">在 [IShellFolder：： GetUIObjectOf 方法](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof)中，處理 [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) 並傳回 Shell 專案的關聯，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-196">In [IShellFolder::GetUIObjectOf Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), handle [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) and return your association for your Shell items, as shown in the following code sample.</span></span>

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  <span data-ttu-id="3ed1e-197">在 Shell 查詢您的 Shell 資料夾以便讓資料流程初始化預覽處理常式之後，請移至您的 [IShellFolder：： BindToObject 方法](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) 方法、處理 IID \_ istream，然後將 [ISTREAM](/windows/win32/api/objidl/nn-objidl-istream) 傳回您的 URL。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-197">After the Shell queries your Shell folder for the data stream to initialize the preview handler, go to your [IShellFolder::BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) method, handle IID\_IStream and return an [IStream](/windows/win32/api/objidl/nn-objidl-istream) to your URL.</span></span>

<span data-ttu-id="3ed1e-198">若要針對您的檔案類型重複使用現有的預覽處理常式，請執行下列兩個步驟：</span><span class="sxs-lookup"><span data-stu-id="3ed1e-198">To reuse an existing preview handler for your file type, follow these two steps:</span></span>

1.  <span data-ttu-id="3ed1e-199">使用現有預覽處理常式的 CLSID 來為您的檔案類型註冊該預覽處理常式，以取代您的 \_ PreviewHandler \_ GUID> <。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-199">Register that preview handler for your file type using the CLSID of the existing preview handler in place of <Your\_PreviewHandler\_GUID>.</span></span>
2.  <span data-ttu-id="3ed1e-200">執行 Shell 資料夾。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-200">Implement a Shell folder.</span></span>

<span data-ttu-id="3ed1e-201">如需有關建立預覽處理常式的詳細資訊，請參閱 [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) 和 [預覽處理常式](../shell/preview-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-201">For more information on creating preview handlers, see [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ed1e-202">其他資源</span><span class="sxs-lookup"><span data-stu-id="3ed1e-202">Additional Resources</span></span>

-   <span data-ttu-id="3ed1e-203">如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-203">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="3ed1e-204">如需建立處理常式的詳細資訊，請參閱 [註冊 Shell 擴充](../shell/reg-shell-exts.md)功能、 [建立 Shell 延伸模組處理常式](../shell/handlers.md)、 [內容功能表](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))、 [Shell 命名空間延伸](../shell/nse-works.md) 和 [預覽處理常式](../shell/preview-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="3ed1e-204">For information about creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md), [Creating Shell Extension Handlers](../shell/handlers.md), [Context Menu](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [Shell Namespace Extensions](../shell/nse-works.md) and [Preview Handlers](../shell/preview-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ed1e-205">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ed1e-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3ed1e-206">**概念**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3ed1e-207">開發通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="3ed1e-207">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-208">瞭解通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="3ed1e-208">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-209">通知索引變更</span><span class="sxs-lookup"><span data-stu-id="3ed1e-209">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-210">程式碼範例：通訊協定處理常式的 Shell 擴充功能</span><span class="sxs-lookup"><span data-stu-id="3ed1e-210">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-211">安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="3ed1e-211">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-212">建立通訊協定處理常式的搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="3ed1e-212">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-213">偵錯工具通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="3ed1e-213">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
