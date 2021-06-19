---
description: 當您在 Windows Shell 中執行自訂檔案格式時，請選擇靜態或動態快捷方式功能表方法。
title: 選擇靜態或動態快捷方式功能表方法
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: dfd73ee052594e1136fe2885ce92b682f229096b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394773"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a><span data-ttu-id="225b1-103">選擇靜態或動態快捷方式功能表方法</span><span class="sxs-lookup"><span data-stu-id="225b1-103">Choosing a Static or Dynamic Shortcut Menu Method</span></span>

<span data-ttu-id="225b1-104">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="225b1-104">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="225b1-105">選擇動詞方法</span><span class="sxs-lookup"><span data-stu-id="225b1-105">Choose a Verb Method</span></span>](#choose-a-verb-method)
    -   [<span data-ttu-id="225b1-106">靜態動詞方法</span><span class="sxs-lookup"><span data-stu-id="225b1-106">Static Verb Methods</span></span>](#static-verb-methods)
    -   [<span data-ttu-id="225b1-107">慣用動態動詞方法</span><span class="sxs-lookup"><span data-stu-id="225b1-107">Preferred Dynamic Verb Methods</span></span>](#preferred-dynamic-verb-methods)
    -   [<span data-ttu-id="225b1-108">不建議的動態動詞方法</span><span class="sxs-lookup"><span data-stu-id="225b1-108">Discouraged Dynamic Verb Methods</span></span>](#discouraged-dynamic-verb-methods)
-   [<span data-ttu-id="225b1-109">擴充快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="225b1-109">Extend a Shortcut Menu</span></span>](#extend-a-shortcut-menu)
-   [<span data-ttu-id="225b1-110">依作業系統支援動詞方法</span><span class="sxs-lookup"><span data-stu-id="225b1-110">Support for Verb Methods by Operating System</span></span>](#support-for-verb-methods-by-operating-system)
-   [<span data-ttu-id="225b1-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="225b1-111">Related topics</span></span>](#related-topics)

## <a name="choose-a-verb-method"></a><span data-ttu-id="225b1-112">選擇動詞方法</span><span class="sxs-lookup"><span data-stu-id="225b1-112">Choose a Verb Method</span></span>

<span data-ttu-id="225b1-113">強烈建議您使用其中一個靜態動詞方法來執行快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="225b1-113">It is strongly encouraged that you implement a shortcut menu using one of the static verb methods.</span></span>

### <a name="static-verb-methods"></a><span data-ttu-id="225b1-114">靜態動詞方法</span><span class="sxs-lookup"><span data-stu-id="225b1-114">Static Verb Methods</span></span>

<span data-ttu-id="225b1-115">靜態動詞是最簡單的動詞命令，但是它們仍提供豐富的功能。</span><span class="sxs-lookup"><span data-stu-id="225b1-115">Static verbs are the simplest verbs to implement, but they still provide rich functionality.</span></span> <span data-ttu-id="225b1-116">請一律選擇符合您需求的最簡單快捷方式功能表方法。</span><span class="sxs-lookup"><span data-stu-id="225b1-116">Always chose the simplest shortcut menu method that meets your needs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="225b1-117">靜態動詞</span><span class="sxs-lookup"><span data-stu-id="225b1-117">Static Verb</span></span></th>
<th><span data-ttu-id="225b1-118">描述</span><span class="sxs-lookup"><span data-stu-id="225b1-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="225b1-119">使用命令列參數的<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a></span><span class="sxs-lookup"><span data-stu-id="225b1-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> with command line parameters</span></span></td>
<td><span data-ttu-id="225b1-120">這是實作為靜態動詞命令的最簡單且最常見的方法。</span><span class="sxs-lookup"><span data-stu-id="225b1-120">This is the simplest and most familiar means of implementing a static verb.</span></span> <span data-ttu-id="225b1-121">處理常式是透過對 <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> 函式的呼叫來叫用，並以選取的檔案和任何選擇性參數傳遞做為命令列。</span><span class="sxs-lookup"><span data-stu-id="225b1-121">A process is invoked through a call to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> function with the selected files and any optional parameters passed as the command line.</span></span> <span data-ttu-id="225b1-122">這會開啟檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="225b1-122">This opens the file or folder.</span></span><br/> <span data-ttu-id="225b1-123">此方法具有下列限制：</span><span class="sxs-lookup"><span data-stu-id="225b1-123">This method has the following limitations:</span></span>
<ul>
<li><span data-ttu-id="225b1-124">命令列長度限制為2000個字元，這會限制動詞可以處理的專案數。</span><span class="sxs-lookup"><span data-stu-id="225b1-124">The command-line length is limited to 2000 characters, which limits the number of items that the verb can handle.</span></span></li>
<li><span data-ttu-id="225b1-125">只能搭配檔案系統專案使用。</span><span class="sxs-lookup"><span data-stu-id="225b1-125">Can only be used with file system items.</span></span></li>
<li><span data-ttu-id="225b1-126">不允許重複使用已在執行中的進程。</span><span class="sxs-lookup"><span data-stu-id="225b1-126">Does not enable re-use of an already running process.</span></span></li>
<li><span data-ttu-id="225b1-127">需要安裝可執行檔才能處理動詞。</span><span class="sxs-lookup"><span data-stu-id="225b1-127">Requires that an executable be installed to handle the verb.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="225b1-128"><strong>DropTarget</strong> /<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></span><span class="sxs-lookup"><span data-stu-id="225b1-128"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a></span></span></td>
<td><span data-ttu-id="225b1-129">以 COM 為基礎的動詞啟用表示支援進程內或跨進程啟用。</span><span class="sxs-lookup"><span data-stu-id="225b1-129">A COM-based verb activation means that supports in-proc or out-of-proc activation.</span></span> <span data-ttu-id="225b1-130"><strong>DropTarget</strong> /當本機伺服器執行<strong>IDropTarget</strong>介面時， <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>也支援重複使用已在執行中的處理常式。</span><span class="sxs-lookup"><span data-stu-id="225b1-130"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> also supports re-use of an already running handler when the <strong>IDropTarget</strong> interface is implemented by a local server.</span></span> <span data-ttu-id="225b1-131">它也會透過封送處理的資料物件完全表示專案，並提供叫用網站鏈的參考，讓您可以透過 <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>與啟動程式互動。</span><span class="sxs-lookup"><span data-stu-id="225b1-131">It also perfectly expresses the items via the marshaled data object and provides a reference to the invoking site chain so that you can interact with the invoker through the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="225b1-132">Windows 7 和更新版本： <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="225b1-132">Windows 7 and later: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a></span></span></td>
<td><span data-ttu-id="225b1-133">最直接的實作為方法。</span><span class="sxs-lookup"><span data-stu-id="225b1-133">The most direct implementation method.</span></span> <span data-ttu-id="225b1-134">因為這是以 COM 為基礎的叫用方法 (像是 DropTarget) 這個介面支援進程內部和跨進程啟用。</span><span class="sxs-lookup"><span data-stu-id="225b1-134">Because this is a COM-based invoke method (like DropTarget) this interface supports in-proc and out-of-proc activation.</span></span> <span data-ttu-id="225b1-135">此動詞命令會執行 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>，並選擇性地 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="225b1-135">The verb implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>, and optionally <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span></span> <span data-ttu-id="225b1-136">這些專案會直接傳遞為 Shell 專案陣列，而來自啟動程式的更多參數則可用於動詞執行，包括叫用點、鍵盤狀態等等。</span><span class="sxs-lookup"><span data-stu-id="225b1-136">The items are passed directly as a Shell item array and more of the parameters from the invoker are available to the verb implementation, including the invoke point, keyboard state, and so forth.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="225b1-137">Windows 7 和更新版本：<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="225b1-137">Windows 7 and later:<strong>ExplorerCommand</strong>/ <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span></span></td>
<td><span data-ttu-id="225b1-138">啟用透過 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> 提供命令模組命令的資料來源，以使用這些命令做為快捷方式功能表上的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="225b1-138">Enables data sources that provide their command module commands through <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="225b1-139">因為這個介面僅支援同進程啟用，所以建議您在命令和快捷方式功能表之間必須共用執行的 Shell 資料來源使用。</span><span class="sxs-lookup"><span data-stu-id="225b1-139">Because this interface supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="225b1-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 是靜態和動態動詞之間的混合式。</span><span class="sxs-lookup"><span data-stu-id="225b1-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) is a hybrid between a static and dynamic verb.</span></span> <span data-ttu-id="225b1-141">**IExplorerCommand** 是在 windows Vista 中宣告，但它在快捷方式功能表中執行動詞的能力是 windows 7 的新功能。</span><span class="sxs-lookup"><span data-stu-id="225b1-141">**IExplorerCommand** was declared in Windows Vista, but its ability to implement a verb in a shortcut menu is new to Windows 7.</span></span>

 

<span data-ttu-id="225b1-142">如需檔案關聯屬性之 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 和 Shell 查詢的詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="225b1-142">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="preferred-dynamic-verb-methods"></a><span data-ttu-id="225b1-143">慣用動態動詞方法</span><span class="sxs-lookup"><span data-stu-id="225b1-143">Preferred Dynamic Verb Methods</span></span>

<span data-ttu-id="225b1-144">慣用的動態動詞方法如下：</span><span class="sxs-lookup"><span data-stu-id="225b1-144">The following dynamic verb methods are preferred:</span></span>



| <span data-ttu-id="225b1-145">動詞類型</span><span class="sxs-lookup"><span data-stu-id="225b1-145">Verb Type</span></span>                                                                                 | <span data-ttu-id="225b1-146">描述</span><span class="sxs-lookup"><span data-stu-id="225b1-146">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="225b1-147">上表中所列的靜態動詞命令 () + Advanced 查詢語法 (AQS) </span><span class="sxs-lookup"><span data-stu-id="225b1-147">Static verb (listed in the previous table) + Advanced Query Syntax (AQS)</span></span>                  | <span data-ttu-id="225b1-148">此選項會取得動態動詞可視性。</span><span class="sxs-lookup"><span data-stu-id="225b1-148">This choice gets dynamic verb visibility.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="225b1-149">Windows 7 和更新版本： [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span><span class="sxs-lookup"><span data-stu-id="225b1-149">Windows 7 and later: [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span></span>                         | <span data-ttu-id="225b1-150">此選項可讓您在 Windows 檔案總管的命令模組中顯示動詞和 explorer 命令的一般執行。</span><span class="sxs-lookup"><span data-stu-id="225b1-150">This choice enables a common implementation of verbs and explorer commands that are displayed in the command module in Windows Explorer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="225b1-151">Windows 7 和更新版本： [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + 靜態動詞</span><span class="sxs-lookup"><span data-stu-id="225b1-151">Windows 7 and later: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + static verb</span></span> | <span data-ttu-id="225b1-152">這種選擇也會取得動態動詞的可見度。</span><span class="sxs-lookup"><span data-stu-id="225b1-152">This choice also gets dynamic verb visibility.</span></span> <span data-ttu-id="225b1-153">它是一種混合式模型，其中會使用簡單的同進程處理常式來計算是否應該 displyed 指定的靜態動詞。</span><span class="sxs-lookup"><span data-stu-id="225b1-153">It is a hybrid model where a simple in-process handler is used to compute if a given static verb should be displyed.</span></span> <span data-ttu-id="225b1-154">這可套用至所有的靜態動詞命令實方法，以達成動態行為，並將同進程邏輯的曝光降至最低。</span><span class="sxs-lookup"><span data-stu-id="225b1-154">This can be applied to all of the static verb implementation methods to achieve dynamic behavior and minimize the exposure of the in-process logic.</span></span> <span data-ttu-id="225b1-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) 具有在背景執行緒上執行的優點，因此可避免 UI 停止回應。</span><span class="sxs-lookup"><span data-stu-id="225b1-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) has the advantage of running on a background thread, and thereby avoids UI hangs.</span></span> <span data-ttu-id="225b1-156">它比 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)簡單得多。</span><span class="sxs-lookup"><span data-stu-id="225b1-156">It is considerably simpler than [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> |



 

### <a name="discouraged-dynamic-verb-methods"></a><span data-ttu-id="225b1-157">不建議的動態動詞方法</span><span class="sxs-lookup"><span data-stu-id="225b1-157">Discouraged Dynamic Verb Methods</span></span>

<span data-ttu-id="225b1-158">[**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 是最強大的功能，但也是最複雜的方法來執行。</span><span class="sxs-lookup"><span data-stu-id="225b1-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="225b1-159">它是以在呼叫端執行緒上執行的同進程 COM 物件為基礎，這通常會 Windows 檔案總管，但可以是裝載專案的任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="225b1-159">It is based on in-process COM objects that run on the thread of the caller, which usually Windows Explorer but can be any application hosting the items.</span></span> <span data-ttu-id="225b1-160">**ICoNtextMenu** 支援動詞可見度、排序和自訂繪圖。</span><span class="sxs-lookup"><span data-stu-id="225b1-160">**IContextMenu** supports verb visibility, ordering, and custom drawing.</span></span> <span data-ttu-id="225b1-161">其中有些功能已新增至靜態動詞功能，例如與命令相關聯的圖示，以及 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 來處理可見度。</span><span class="sxs-lookup"><span data-stu-id="225b1-161">Some of these features have been added to the static verb features, such as an icon to be associated with a command, and [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) to deal with visibility.</span></span>

<span data-ttu-id="225b1-162">如果您必須註冊檔案類型的動態動詞命令以擴充檔案類型的快捷方式功能表，請依照 [使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)中提供的指示進行。</span><span class="sxs-lookup"><span data-stu-id="225b1-162">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided in [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

## <a name="extend-a-shortcut-menu"></a><span data-ttu-id="225b1-163">擴充快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="225b1-163">Extend a Shortcut Menu</span></span>

<span data-ttu-id="225b1-164">選擇動詞方法之後，您可以註冊檔案類型的靜態動詞命令，以擴充檔案類型的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="225b1-164">After you choose a verb method you can extend a shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="225b1-165">如需詳細資訊，請參閱 [建立快顯功能表處理常式](context-menu-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="225b1-165">For more information, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="support-for-verb-methods-by-operating-system"></a><span data-ttu-id="225b1-166">依作業系統支援動詞方法</span><span class="sxs-lookup"><span data-stu-id="225b1-166">Support for Verb Methods by Operating System</span></span>

<span data-ttu-id="225b1-167">下表列出對動詞調用方法的支援（依作業系統）。</span><span class="sxs-lookup"><span data-stu-id="225b1-167">Support for verb invocation methods by operating system are listed in the following table.</span></span>



| <span data-ttu-id="225b1-168">Verb 方法</span><span class="sxs-lookup"><span data-stu-id="225b1-168">Verb Method</span></span>          | <span data-ttu-id="225b1-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="225b1-169">Windows XP</span></span> | <span data-ttu-id="225b1-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="225b1-170">Windows Vista</span></span> | <span data-ttu-id="225b1-171">Windows 7 和以上</span><span class="sxs-lookup"><span data-stu-id="225b1-171">Windows 7 and beyond</span></span> |
|----------------------|------------|---------------|----------------------|
| <span data-ttu-id="225b1-172">CreateProcess</span><span class="sxs-lookup"><span data-stu-id="225b1-172">CreateProcess</span></span>        | <span data-ttu-id="225b1-173">X</span><span class="sxs-lookup"><span data-stu-id="225b1-173">X</span></span>          | <span data-ttu-id="225b1-174">X</span><span class="sxs-lookup"><span data-stu-id="225b1-174">X</span></span>             | <span data-ttu-id="225b1-175">X</span><span class="sxs-lookup"><span data-stu-id="225b1-175">X</span></span>                    |
| <span data-ttu-id="225b1-176">DDE</span><span class="sxs-lookup"><span data-stu-id="225b1-176">DDE</span></span>                  | <span data-ttu-id="225b1-177">X</span><span class="sxs-lookup"><span data-stu-id="225b1-177">X</span></span>          | <span data-ttu-id="225b1-178">X</span><span class="sxs-lookup"><span data-stu-id="225b1-178">X</span></span>             | <span data-ttu-id="225b1-179">X</span><span class="sxs-lookup"><span data-stu-id="225b1-179">X</span></span>                    |
| <span data-ttu-id="225b1-180">DropTarget</span><span class="sxs-lookup"><span data-stu-id="225b1-180">DropTarget</span></span>           | <span data-ttu-id="225b1-181">X</span><span class="sxs-lookup"><span data-stu-id="225b1-181">X</span></span>          | <span data-ttu-id="225b1-182">X</span><span class="sxs-lookup"><span data-stu-id="225b1-182">X</span></span>             | <span data-ttu-id="225b1-183">X</span><span class="sxs-lookup"><span data-stu-id="225b1-183">X</span></span>                    |
| <span data-ttu-id="225b1-184">ExecuteCommand</span><span class="sxs-lookup"><span data-stu-id="225b1-184">ExecuteCommand</span></span>       |            | <span data-ttu-id="225b1-185">X</span><span class="sxs-lookup"><span data-stu-id="225b1-185">X</span></span>             | <span data-ttu-id="225b1-186">X</span><span class="sxs-lookup"><span data-stu-id="225b1-186">X</span></span>                    |
| <span data-ttu-id="225b1-187">ExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="225b1-187">ExplorerCommand</span></span>      |            |               | <span data-ttu-id="225b1-188">X</span><span class="sxs-lookup"><span data-stu-id="225b1-188">X</span></span>                    |
| <span data-ttu-id="225b1-189">ExplorerCommandState</span><span class="sxs-lookup"><span data-stu-id="225b1-189">ExplorerCommandState</span></span> |            |               | <span data-ttu-id="225b1-190">X</span><span class="sxs-lookup"><span data-stu-id="225b1-190">X</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="225b1-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="225b1-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="225b1-192">快速鍵功能表處理常式和多重選取動詞的最佳作法</span><span class="sxs-lookup"><span data-stu-id="225b1-192">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="225b1-193">建立快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="225b1-193">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="225b1-194">使用動態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="225b1-194">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="225b1-195">快捷方式 (內容) 功能表和快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="225b1-195">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="225b1-196">快速鍵功能表參考</span><span class="sxs-lookup"><span data-stu-id="225b1-196">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> <dt>

[<span data-ttu-id="225b1-197">動詞和檔案關聯</span><span class="sxs-lookup"><span data-stu-id="225b1-197">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> </dl>

 

 
