---
title: 使用 Shell 擴充功能新增圖示和內容功能表
description: 您可以藉由執行 Shell 擴充功能，來改善使用者使用 Microsoft Windows 桌面搜尋 (WDS) 和通訊協定處理常式的體驗。
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "104185493"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a><span data-ttu-id="8d4d7-103">使用 Shell 擴充功能新增圖示和內容功能表</span><span class="sxs-lookup"><span data-stu-id="8d4d7-103">Adding Icons and Context Menus with Shell Extensions</span></span>

> [!NOTE]
> <span data-ttu-id="8d4d7-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8d4d7-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="8d4d7-106">您可以藉由執行 Shell 擴充功能，來改善使用者使用 Microsoft Windows 桌面搜尋 (WDS) 和通訊協定處理常式的體驗。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-106">You can improve your users' experience with Microsoft Windows Desktop Search (WDS) and your protocol handler by implementing Shell extensions.</span></span> <span data-ttu-id="8d4d7-107">如果沒有進一步的擴充功能，您所建立的通訊協定處理常式將不會包含下列使用者體驗：</span><span class="sxs-lookup"><span data-stu-id="8d4d7-107">Without further extension, the protocol handler you create will not include the following user experiences:</span></span>

-   <span data-ttu-id="8d4d7-108">WDS 不會顯示結果的特定圖示。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-108">WDS will not display specific icons for your results.</span></span>
-   <span data-ttu-id="8d4d7-109">當使用者按兩下專案時，使用者介面將不會回應事件。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-109">When users double-click an item, the user interface will not respond to the event.</span></span>
-   <span data-ttu-id="8d4d7-110">當使用者以滑鼠右鍵按一下專案時，內容功能表將不支援此專案的任何作業。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-110">When users right-click an item, the context menu will not support any operations for the item.</span></span>

<span data-ttu-id="8d4d7-111">**IShellFolder** 需要最基本的 **IPersist** 和 **IPersistFolder** ，而且 **ICoNtextMenu** 和 **IExtractIcon** 需要最基本的 **IShellFolder** 執行，這兩個介面可提供更順暢的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-111">Minimal implementations of **IPersist** and **IPersistFolder** are required by **IShellFolder**, and a minimal implementation of **IShellFolder** is required for **IContextMenu** and **IExtractIcon**, the two interfaces that provide a more seamless user experience.</span></span>

 

## <a name="ipersist"></a><span data-ttu-id="8d4d7-112">IPersist</span><span class="sxs-lookup"><span data-stu-id="8d4d7-112">IPersist</span></span>

<span data-ttu-id="8d4d7-113">**IPersist** 介面會定義單一方法 **GetClassID**，其設計目的是要提供可持續儲存在系統中之物件的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-113">The **IPersist** interface defines the single method **GetClassID**, which is designed to supply the CLSID of an object that can be stored persistently in the system.</span></span>



| <span data-ttu-id="8d4d7-114">方法</span><span class="sxs-lookup"><span data-stu-id="8d4d7-114">Method</span></span>       | <span data-ttu-id="8d4d7-115">描述</span><span class="sxs-lookup"><span data-stu-id="8d4d7-115">Description</span></span>                                 |
|--------------|---------------------------------------------|
| <span data-ttu-id="8d4d7-116">GetClassID () </span><span class="sxs-lookup"><span data-stu-id="8d4d7-116">GetClassID()</span></span> | <span data-ttu-id="8d4d7-117">傳回通訊協定處理常式的 ClassID</span><span class="sxs-lookup"><span data-stu-id="8d4d7-117">Returns the ClassID of the protocol handler</span></span> |



 

> [!Note]
>
> <span data-ttu-id="8d4d7-118">應針對 **IPersist**、 **IPersistFolder** 和 **IShellFolder** 執行相同的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-118">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

 

## <a name="ipersistfolder"></a><span data-ttu-id="8d4d7-119">IPersistFolder</span><span class="sxs-lookup"><span data-stu-id="8d4d7-119">IPersistFolder</span></span>

<span data-ttu-id="8d4d7-120">**IPersistFolder** 介面是用來初始化 Shell 資料夾物件。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-120">The **IPersistFolder** interface is used to initialize Shell folder objects.</span></span> <span data-ttu-id="8d4d7-121">此介面的實作為衍生自 **IPersist** 的介面，是資料夾在 Shell 命名空間中的通知位置。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-121">Implementation of this interface, which is derived from **IPersist**, is how the folder is told where it is in the Shell namespace.</span></span>



| <span data-ttu-id="8d4d7-122">方法</span><span class="sxs-lookup"><span data-stu-id="8d4d7-122">Method</span></span>       | <span data-ttu-id="8d4d7-123">描述</span><span class="sxs-lookup"><span data-stu-id="8d4d7-123">Description</span></span>                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d4d7-124">初始化 () </span><span class="sxs-lookup"><span data-stu-id="8d4d7-124">Initialize()</span></span> | <span data-ttu-id="8d4d7-125">指示 Shell 資料夾物件根據傳遞的資訊進行初始化，並傳回 S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="8d4d7-125">Instructs a Shell folder object to initialize itself based on the information passed and returns S\_OK</span></span> |



 

> [!Note]
>
> <span data-ttu-id="8d4d7-126">應針對 **IPersist**、 **IPersistFolder** 和 **IShellFolder** 執行相同的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-126">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="8d4d7-127">您不會直接使用此介面。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-127">You do not use this interface directly.</span></span> <span data-ttu-id="8d4d7-128">它會在初始化 Shell 資料夾物件時，由 IShellFolder：： BindToObject 介面的檔案系統實作為使用。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-128">It is used by the file system implementation of the IShellFolder::BindToObject interface when it initializes a Shell folder object.</span></span>

 

## <a name="ishellfolder"></a><span data-ttu-id="8d4d7-129">IShellFolder</span><span class="sxs-lookup"><span data-stu-id="8d4d7-129">IShellFolder</span></span>

<span data-ttu-id="8d4d7-130">**IShellFolder** 介面是用來管理資料夾，而且需要部分執行，如此一來，為通訊協定處理常式所執行的圖示和內容介面，在 Windows 桌面搜尋結果使用者介面中的行為就會正確。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-130">The **IShellFolder** interface is used to manage folders, and a partial implementation is required so that the icon and context interfaces implemented for a protocol handler will behave correctly in the Windows Desktop Search results user interface.</span></span> <span data-ttu-id="8d4d7-131">需要的大部分功能都是透過 **GetUIObjectOf** 方法來公開。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-131">Most of the functionality required is exposed through the **GetUIObjectOf** method.</span></span> <span data-ttu-id="8d4d7-132">這個方法可讓增益集查詢 **IExtractIcon** 和 **ICoNtextMenu** 介面。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-132">This method enables an add-in to query for the **IExtractIcon** and **IContextMenu** interfaces.</span></span>

<span data-ttu-id="8d4d7-133">**IShellFolder** 介面會使用 pidl 而非 url。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-133">The **IShellFolder** interface uses PIDLs instead of URLs.</span></span> <span data-ttu-id="8d4d7-134">相較于完整命名空間延伸模組的需求，增益集可以使用僅包含 URL 的簡單 IDL 結構。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-134">In contrast to the requirements of a complete Namespace extension, add-ins can use a simple IDL structure that contains only the URL.</span></span>

<span data-ttu-id="8d4d7-135">您必須執行下列 **IShellFolder** 方法。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-135">The following methods of **IShellFolder** must be implemented.</span></span> <span data-ttu-id="8d4d7-136">請注意，其中五種方法需要進行基本的執行。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-136">Note that five of these methods require minimal implementation.</span></span>



| <span data-ttu-id="8d4d7-137">方法</span><span class="sxs-lookup"><span data-stu-id="8d4d7-137">Method</span></span>             | <span data-ttu-id="8d4d7-138">描述</span><span class="sxs-lookup"><span data-stu-id="8d4d7-138">Description</span></span>                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d4d7-139">BindToObject () </span><span class="sxs-lookup"><span data-stu-id="8d4d7-139">BindToObject()</span></span>     | <span data-ttu-id="8d4d7-140">傳回 E \_ >notimpl</span><span class="sxs-lookup"><span data-stu-id="8d4d7-140">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="8d4d7-141">BindToStorage () </span><span class="sxs-lookup"><span data-stu-id="8d4d7-141">BindToStorage()</span></span>    | <span data-ttu-id="8d4d7-142">傳回 E \_ >notimpl</span><span class="sxs-lookup"><span data-stu-id="8d4d7-142">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="8d4d7-143">CreateViewObject () </span><span class="sxs-lookup"><span data-stu-id="8d4d7-143">CreateViewObject()</span></span> | <span data-ttu-id="8d4d7-144">傳回 E \_ >notimpl</span><span class="sxs-lookup"><span data-stu-id="8d4d7-144">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="8d4d7-145">SetNameOf () </span><span class="sxs-lookup"><span data-stu-id="8d4d7-145">SetNameOf()</span></span>        | <span data-ttu-id="8d4d7-146">傳回 E \_ >notimpl</span><span class="sxs-lookup"><span data-stu-id="8d4d7-146">Returns E\_NOTIMPL</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="8d4d7-147">ParseDisplayName () </span><span class="sxs-lookup"><span data-stu-id="8d4d7-147">ParseDisplayName()</span></span> | <span data-ttu-id="8d4d7-148">將 URL 轉換成 PIDL 結構</span><span class="sxs-lookup"><span data-stu-id="8d4d7-148">Converts a URL to the PIDL structure</span></span>                                                                                                                                                                        |
| <span data-ttu-id="8d4d7-149">CompareIDs () </span><span class="sxs-lookup"><span data-stu-id="8d4d7-149">CompareIDs()</span></span>       | <span data-ttu-id="8d4d7-150">比較兩個 PIDL 值</span><span class="sxs-lookup"><span data-stu-id="8d4d7-150">Compares two PIDL values</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="8d4d7-151">GetDisplayNameOf () </span><span class="sxs-lookup"><span data-stu-id="8d4d7-151">GetDisplayNameOf()</span></span> | <span data-ttu-id="8d4d7-152">傳回 PIDL 的 URL。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-152">Returns the URL for a PIDL</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="8d4d7-153">GetUIObjectOf () </span><span class="sxs-lookup"><span data-stu-id="8d4d7-153">GetUIObjectOf()</span></span>    | <span data-ttu-id="8d4d7-154">這個方法類似于 OLE COM QueryInterface 方法。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-154">This method is similar to the OLE COM QueryInterface method.</span></span> <span data-ttu-id="8d4d7-155">如果要求的是圖示，呼叫端會要求 IID \_ IExtractIcon; 如果要求內容功能表，呼叫端會要求 iid \_ ICoNtextMenu。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-155">If an icon is requested, the caller requests the IID\_IExtractIcon; if a context menu is requested, the caller requests the IID\_IContextMenu.</span></span> |



 

> [!Note]
>
> <span data-ttu-id="8d4d7-156">應針對 **IPersist**、 **IPersistFolder** 和 **IShellFolder** 執行相同的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-156">The same CLSID should be implemented for **IPersist**, **IPersistFolder** and **IShellFolder**.</span></span>

 

<span data-ttu-id="8d4d7-157">**IShellFolder** 不會用來列舉資料夾。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-157">**IShellFolder** is not used to enumerate folders.</span></span> <span data-ttu-id="8d4d7-158">這表示資料夾的顯示名稱將會是實體 URL。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-158">This means that the display name of a folder will be the physical URL.</span></span> <span data-ttu-id="8d4d7-159">未來可能會變更。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-159">This may change in the future.</span></span>

 

## <a name="icontextmenu"></a><span data-ttu-id="8d4d7-160">ICoNtextMenu</span><span class="sxs-lookup"><span data-stu-id="8d4d7-160">IContextMenu</span></span>

<span data-ttu-id="8d4d7-161">當 WDS 向使用者顯示結果時，使用者可以在專案上按一下滑鼠右鍵，並查看 **ICoNtextMenu** 介面所定義的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-161">When WDS displays results to the user, the user can right-click an item and see a context menu defined by your **IContextMenu** interface.</span></span>

<span data-ttu-id="8d4d7-162">操作功能表上的預設動作，與按兩下專案時所採取的動作相同。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-162">The default action on the context menu is the same action taken when the item is double-clicked.</span></span> <span data-ttu-id="8d4d7-163">如果專案沒有對應的 **IShellFolder** 或 **ICoNtextMenu** 介面，則按兩下事件的預設行為是將 URL 當作引數傳遞至 ShellExecute 函式。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-163">Without the corresponding **IShellFolder** or **IContextMenu** interfaces for the item, the default behavior for a double-click event is to pass the URL as an argument to the ShellExecute function.</span></span>

 

## <a name="iextracticon"></a><span data-ttu-id="8d4d7-164">IExtractIcon</span><span class="sxs-lookup"><span data-stu-id="8d4d7-164">IExtractIcon</span></span>

<span data-ttu-id="8d4d7-165">**IExtractIcon** 會根據您的通訊協定處理常式所提供的 PIDL URL，抓取 WDS 使用者介面的圖示。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-165">**IExtractIcon** retrieves an icon for the WDS user interface based on the URL in the PIDL provided by your protocol handler.</span></span>

 

## <a name="code-sample"></a><span data-ttu-id="8d4d7-166">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="8d4d7-166">Code Sample</span></span>

<span data-ttu-id="8d4d7-167">[自訂通訊協定處理常式消費者介面範例程式碼](-search-2x-wds-ph-ui-samplecode.md)示範 **IShellFolder** 和支援介面的執行，並包含操作 pidl 的支援。</span><span class="sxs-lookup"><span data-stu-id="8d4d7-167">The [Custom Protocol Handler User Interface Sample Code](-search-2x-wds-ph-ui-samplecode.md) demonstrates an implementation of **IShellFolder** and supporting interfaces and includes support for manipulating the PIDLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d4d7-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d4d7-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8d4d7-169">**參考**</span><span class="sxs-lookup"><span data-stu-id="8d4d7-169">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8d4d7-170">自訂通訊協定處理常式消費者介面範例程式碼</span><span class="sxs-lookup"><span data-stu-id="8d4d7-170">Custom Protocol Handler User Interface Sample Code</span></span>](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="8d4d7-171">安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="8d4d7-171">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




