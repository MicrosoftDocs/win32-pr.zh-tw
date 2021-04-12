---
title: 建立搜尋處理常式
description: Shell 支援數個搜尋公用程式，可讓使用者找出命名空間物件，例如檔案或印表機。 您可以建立自訂搜尋引擎，並藉由執行和註冊搜尋處理常式，讓使用者可以使用它。
ms.assetid: ffd023bb-16ab-43ce-b00b-5e32656c8013
keywords:
- 搜尋處理常式
- 註冊，搜尋處理常式
- 靜態搜尋處理常式
- 註冊、靜態搜尋處理常式
- 動態搜尋處理常式
- 註冊、動態搜尋處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6476109302a176822137747353b2762b0caea8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315034"
---
# <a name="creating-search-handlers"></a><span data-ttu-id="95402-110">建立搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-110">Creating Search Handlers</span></span>

<span data-ttu-id="95402-111">\[只有在 Windows XP 或更早版本才支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="95402-111">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="95402-112">請改用 Windows Search。\]</span><span class="sxs-lookup"><span data-stu-id="95402-112">Use Windows Search instead.\]</span></span>

<span data-ttu-id="95402-113">Shell 支援數個搜尋公用程式，可讓使用者找出命名空間物件，例如檔案或印表機。</span><span class="sxs-lookup"><span data-stu-id="95402-113">The Shell supports several search utilities that allow users to locate namespace objects such as files or printers.</span></span> <span data-ttu-id="95402-114">您可以建立自訂搜尋引擎，並藉由執行和註冊 *搜尋處理常式*，讓使用者可以使用它。</span><span class="sxs-lookup"><span data-stu-id="95402-114">You can create a custom search engine and make it available to users by implementing and registering a *search handler*.</span></span>

<span data-ttu-id="95402-115">[建立 shell](/windows/desktop/shell/handlers)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。</span><span class="sxs-lookup"><span data-stu-id="95402-115">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](/windows/desktop/shell/handlers).</span></span> <span data-ttu-id="95402-116">本檔著重于搜尋處理常式特定的執行層面。</span><span class="sxs-lookup"><span data-stu-id="95402-116">This document focuses on those aspects of implementation that are specific to search handlers.</span></span>

-   [<span data-ttu-id="95402-117">搜尋處理常式的運作方式</span><span class="sxs-lookup"><span data-stu-id="95402-117">How Search Handlers Work</span></span>](#how-search-handlers-work)
-   [<span data-ttu-id="95402-118">註冊搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-118">Registering Search Handlers</span></span>](#registering-search-handlers)
    -   [<span data-ttu-id="95402-119">註冊靜態搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-119">Registering a Static Search Handler</span></span>](#registering-a-static-search-handler)
    -   [<span data-ttu-id="95402-120">註冊動態搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-120">Registering a Dynamic Search Handler</span></span>](#registering-a-dynamic-search-handler)
-   [<span data-ttu-id="95402-121">執行搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-121">Implementing Search Handlers</span></span>](#implementing-search-handlers)

## <a name="how-search-handlers-work"></a><span data-ttu-id="95402-122">搜尋處理常式的運作方式</span><span class="sxs-lookup"><span data-stu-id="95402-122">How Search Handlers Work</span></span>

<span data-ttu-id="95402-123">使用者有兩種方式可以選取搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="95402-123">Users have two ways to select a search engine.</span></span> <span data-ttu-id="95402-124">第一種方式是從 [開始] 功能表。</span><span class="sxs-lookup"><span data-stu-id="95402-124">The first way is from the Start menu.</span></span> <span data-ttu-id="95402-125">在 Windows 2000 之前的系統上，選取 [**開始**] 功能表上的 [**尋找**] 命令會顯示可用搜尋引擎的子功能表。</span><span class="sxs-lookup"><span data-stu-id="95402-125">With systems earlier than Windows 2000, selecting the **Find** command on the **Start** menu displays a submenu of the available search engines.</span></span> <span data-ttu-id="95402-126">在 Windows 2000 和更新版本中， **St** 的功能表的 [ **尋找** ] 命令會重新命名為 [搜尋]。</span><span class="sxs-lookup"><span data-stu-id="95402-126">With Windows 2000 and later, the **St** art menu's **Find** command is renamed Search.</span></span> <span data-ttu-id="95402-127">下圖顯示 Windows XP 系統上的 [ **搜尋** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="95402-127">The following illustration shows the **Search** button on a Windows XP system.</span></span>

![[開始] 功能表的 [搜尋] 子功能表](images/searchhandler1.jpg)

<span data-ttu-id="95402-129">使用者也可以從 Windows 檔案總管啟動搜尋。</span><span class="sxs-lookup"><span data-stu-id="95402-129">Users can also launch a search from Windows Explorer.</span></span> <span data-ttu-id="95402-130">在 Windows 2000 之前的系統上，他們會按一下 [**工具**] 功能表上的 [**尋找**] 命令，顯示與 [**開始**] 功能表相關聯的功能表基本上是相同的功能表。</span><span class="sxs-lookup"><span data-stu-id="95402-130">On systems earlier than Windows 2000, they click the **Find** command on the **Tools** menu to display essentially the same menu as the one associated with the **Start** menu.</span></span> <span data-ttu-id="95402-131">不過，Windows 2000 的 Windows 檔案總管會以非常不同的方式處理搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="95402-131">However, Windows Explorer for Windows 2000 handles search engines in a very different way.</span></span> <span data-ttu-id="95402-132">工具列上現在有一個 [**搜尋**] 按鈕，而不是以 **工具** 功能表的子功能表來處理搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="95402-132">Instead of handling search engines as a submenu of the **Tools** menu, there is now a **Search** button on the toolbar.</span></span> <span data-ttu-id="95402-133">按一下這個按鈕會開啟 Explorer 列的 [ **搜尋** ] 窗格。</span><span class="sxs-lookup"><span data-stu-id="95402-133">Clicking this button opens the Explorer bar's **Search** pane.</span></span> <span data-ttu-id="95402-134">下圖顯示 [ **搜尋檔案和資料夾** ] 搜尋窗格。</span><span class="sxs-lookup"><span data-stu-id="95402-134">The following illustration shows the **Search For Files And Folders** search pane.</span></span>

![windows explorer bar 的 [搜尋] 窗格](images/searchhandler2.jpg)

<span data-ttu-id="95402-136">Windows 2000 和舊版系統如何管理影響執行和註冊的搜尋處理常式有一些差異。</span><span class="sxs-lookup"><span data-stu-id="95402-136">There are a number of differences in how Windows 2000 and earlier systems manage search handlers that affect both implementation and registration.</span></span>



| <span data-ttu-id="95402-137">Windows 之前的2000</span><span class="sxs-lookup"><span data-stu-id="95402-137">Pre-Windows 2000</span></span>                                                                                                                                                                                                       | <span data-ttu-id="95402-138">Windows 2000 和更新版本</span><span class="sxs-lookup"><span data-stu-id="95402-138">Windows 2000 and later</span></span>                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95402-139">搜尋處理常式會實作為 [快捷方式功能表處理常式](/windows/desktop/shell/context-menu-handlers)的類型。</span><span class="sxs-lookup"><span data-stu-id="95402-139">Search handlers are implemented as a type of [shortcut menu handler](/windows/desktop/shell/context-menu-handlers).</span></span>                                                                                                                     | <span data-ttu-id="95402-140">搜尋處理常式可以實作為快捷方式功能表處理常式，或是動態 HTML (DHTML) 檔。</span><span class="sxs-lookup"><span data-stu-id="95402-140">Search handlers can be implemented as shortcut menu handlers, or as Dynamic HTML (DHTML) documents.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="95402-141">搜尋處理常式可以是靜態或動態。</span><span class="sxs-lookup"><span data-stu-id="95402-141">Search handlers can be either static or dynamic.</span></span> <span data-ttu-id="95402-142">只有當使用者選取靜態處理常式時，才會載入靜態處理常式。</span><span class="sxs-lookup"><span data-stu-id="95402-142">Static handlers are loaded only when they are selected by the user.</span></span> <span data-ttu-id="95402-143">動態處理常式是由 Shell 在啟動時載入，而且在 Shell 結束之前不會終止。</span><span class="sxs-lookup"><span data-stu-id="95402-143">Dynamic handlers are loaded by the Shell at startup and are not terminated until the Shell exits.</span></span> | <span data-ttu-id="95402-144">實作為快捷方式功能表處理常式的處理常式可以是靜態或動態。</span><span class="sxs-lookup"><span data-stu-id="95402-144">Handlers implemented as shortcut menu handlers can be either static or dynamic.</span></span> <span data-ttu-id="95402-145">實作為 DHTML 檔案的處理常式必須是靜態的。</span><span class="sxs-lookup"><span data-stu-id="95402-145">Handlers implemented as DHTML documents must be static.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="95402-146">搜尋處理常式會顯示在 [**開始**] 功能表的 [**尋找**] 子功能表和 [Windows 檔案總管  **工具**] 功能表的 [**尋找**] 子功能表中。</span><span class="sxs-lookup"><span data-stu-id="95402-146">Search handlers appear on the **Find** submenu of the **Start** menu and the **Find** submenu of the Windows Explorer **Tools** menu.</span></span>                                                                                  | <span data-ttu-id="95402-147">搜尋處理常式只會出現在 [**開始**] 功能表的 [**搜尋**] 子功能表上。</span><span class="sxs-lookup"><span data-stu-id="95402-147">Search handlers appear only on the **Search** submenu of the **Start** menu.</span></span> <span data-ttu-id="95402-148">若要透過 Windows 檔案總管的功能表列提供自訂的搜尋窗格，您必須將它實作為 [帶區物件](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="95402-148">To make a custom search pane available through the Windows Explorer menu bar, you must implement it as a [band object](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)).</span></span> <span data-ttu-id="95402-149">然後，它會列在 [Windows 檔案總管  **View** ] 功能表的 [ **Explorer Bar** ] 子功能表上。</span><span class="sxs-lookup"><span data-stu-id="95402-149">It is then listed on the **Explorer Bar** submenu of the Windows Explorer **View** menu.</span></span> |



 

## <a name="registering-search-handlers"></a><span data-ttu-id="95402-150">註冊搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-150">Registering Search Handlers</span></span>

<span data-ttu-id="95402-151">搜尋處理常式會在檔案類型的 **FindExtensions** 子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="95402-151">Search handlers are registered under the file types's **FindExtensions** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

<span data-ttu-id="95402-152">從此時開始，註冊程式取決於處理常式是靜態或動態。</span><span class="sxs-lookup"><span data-stu-id="95402-152">From this point, the registration procedure depends on whether the handler is to be static or dynamic.</span></span> <span data-ttu-id="95402-153">如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](/windows/desktop/shell/handlers)程式。</span><span class="sxs-lookup"><span data-stu-id="95402-153">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](/windows/desktop/shell/handlers).</span></span>

### <a name="registering-a-static-search-handler"></a><span data-ttu-id="95402-154">註冊靜態搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-154">Registering a Static Search Handler</span></span>

<span data-ttu-id="95402-155">靜態搜尋處理常式只有在使用者啟動時才會載入。</span><span class="sxs-lookup"><span data-stu-id="95402-155">Static search handlers are loaded only when they are launched by the user.</span></span> <span data-ttu-id="95402-156">這種方法最適合適用于較小且可快速載入的 Dll。</span><span class="sxs-lookup"><span data-stu-id="95402-156">This approach works best for DLLs that are small and can be loaded quickly.</span></span> <span data-ttu-id="95402-157">如果您使用 DHTML 來執行處理常式，它必須是靜態的。</span><span class="sxs-lookup"><span data-stu-id="95402-157">If you are using DHTML to implement your handler, it must be static.</span></span> <span data-ttu-id="95402-158">若要註冊靜態延伸模組處理常式，請在 **FindExtensions** 子機碼的 **靜態** 子機碼下，建立名為的處理常式的子機碼。</span><span class="sxs-lookup"><span data-stu-id="95402-158">To register a static extension handler, create a subkey named for the handler under the **Static** subkey of the **FindExtensions** subkey.</span></span> <span data-ttu-id="95402-159">系統不會使用該名稱，但它不能與 **FindExtensions** 子機碼下的其他搜尋處理常式名稱相同。</span><span class="sxs-lookup"><span data-stu-id="95402-159">The name is not used by the system, but it must not be identical to other search handler names under the **FindExtensions** subkey.</span></span>

### <a name="shortcut-menu-based-search-handlers"></a><span data-ttu-id="95402-160">以快捷方式功能表為基礎的搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-160">Shortcut menu-based search handlers</span></span>

<span data-ttu-id="95402-161">如果您的處理常式是實作為 [快捷方式功能表處理常式](/windows/desktop/shell/context-menu-handlers)，請將處理常式名稱子機碼的預設值設定為物件的類別識別碼， (CLSID) GUID。</span><span class="sxs-lookup"><span data-stu-id="95402-161">If your handler is implemented as a [shortcut menu handler](/windows/desktop/shell/context-menu-handlers), set the default value of the handler's name subkey to the object's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="95402-162">在處理常式的名稱子機碼下，建立名為 **0** (零) 的子機碼，   並將其預設值設定為要顯示在 [**搜尋**] 或 [**尋找**] 子功能表中的字串。</span><span class="sxs-lookup"><span data-stu-id="95402-162">Under the handler's name subkey, create a subkey named **0** (zero) and set its default value to the string that will be displayed in the **Search** or **Find** submenu.</span></span> <span data-ttu-id="95402-163">您可以用一般方式啟用鍵盤快速鍵，方法是在快速鍵字元前面加上連字號 (&) 。</span><span class="sxs-lookup"><span data-stu-id="95402-163">You can enable keyboard shortcuts in the usual way, by preceding the shortcut character with an ampersand (&).</span></span> <span data-ttu-id="95402-164">您可以在 [ **0** ] 子機碼底下建立 **DefaultIcon** 子機碼，以在功能表文字右邊顯示選擇性的小圖示。</span><span class="sxs-lookup"><span data-stu-id="95402-164">You can have an optional small icon displayed to the right of the menu text by creating a **DefaultIcon** subkey under the **0** subkey.</span></span> <span data-ttu-id="95402-165">將其預設值設定為字串，其中包含包含圖示之檔案的路徑，後面接著逗號，再接著圖示的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="95402-165">Set its default value to a string containing the path of the file containing the icon, followed by a comma, followed by the icon's zero-based index.</span></span>

<span data-ttu-id="95402-166">下列範例會註冊 **MySearchEngine** 搜尋處理常式。</span><span class="sxs-lookup"><span data-stu-id="95402-166">The following example registers the **MySearchEngine** search handler.</span></span> <span data-ttu-id="95402-167">功能表文字是「我的搜尋引擎」，其中 M 指定為快速鍵。</span><span class="sxs-lookup"><span data-stu-id="95402-167">The menu text is "My Search Engine", with M specified as the shortcut key.</span></span> <span data-ttu-id="95402-168">此圖示為 C： \\ MyDir \\MySearch.dll，索引為2。</span><span class="sxs-lookup"><span data-stu-id="95402-168">The icon is in C:\\MyDir\\MySearch.dll, with an index of 2.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {MySearchEngine CLSID GUID}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
```

### <a name="dhtml-based-search-handlers"></a><span data-ttu-id="95402-169">以 DHTML 為基礎的搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-169">DHTML-based search handlers</span></span>

<span data-ttu-id="95402-170">使用 Windows 2000，您也可以將搜尋處理常式實作為 DHTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="95402-170">With Windows 2000, you can also implement a search handler as a DHTML document.</span></span> <span data-ttu-id="95402-171">其名稱會列在 [**開始**] 功能表的 [**搜尋**] 子功能表中。</span><span class="sxs-lookup"><span data-stu-id="95402-171">Its name is listed in the **Search** submenu of the **Start** menu.</span></span> <span data-ttu-id="95402-172">當使用者選取該檔案時，它會啟動 Windows 檔案總管，並開啟搜尋檔的瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="95402-172">When the user selects it, it launches Windows Explorer with the Explorer bar opened to the search document.</span></span> <span data-ttu-id="95402-173">您也可以指定要顯示在 Explorer 列右邊的 DHTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="95402-173">You can also specify a DHTML document to be displayed to the right of the Explorer bar.</span></span> <span data-ttu-id="95402-174">沒有任何方法可以從預設的 [搜尋] 窗格啟動不同的處理常式。</span><span class="sxs-lookup"><span data-stu-id="95402-174">There is no way to launch a different handler from the default Search pane.</span></span> <span data-ttu-id="95402-175">您可以直接從 Windows 檔案總管啟動搜尋引擎，但必須將它們實作為 [頻外物件](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="95402-175">Search engines can be launched directly from Windows Explorer, but only if they are implemented as as [band objects](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)).</span></span>

<span data-ttu-id="95402-176">若要註冊以 DHTML 為基礎的搜尋處理常式，請將處理常式的名稱子機碼設定為 CLSID \_ ShellSearchExt (目前為 {169A0691-8DF9-11d1-A1C4-00C04FD75D13} ) 的字串格式，然後建立下列子機碼。</span><span class="sxs-lookup"><span data-stu-id="95402-176">To register a DHTML-based search handler, set the handler's name subkey to the string form of CLSID\_ShellSearchExt (currently {169A0691-8DF9-11d1-A1C4-00C04FD75D13}) and create the following subkeys.</span></span>

1.  <span data-ttu-id="95402-177">在處理常式名稱子機碼底下建立 **0** (零) 子機碼，並將其預設值設定為功能表文字。</span><span class="sxs-lookup"><span data-stu-id="95402-177">Create a **0**(zero) subkey under the handler name subkey and set its default value to the menu text.</span></span>
2.  <span data-ttu-id="95402-178">若要在功能表文字旁邊顯示圖示，請在 **0** 底下建立 **DefaultIcon** 子機碼，並將其預設值設定為圖示的路徑和索引。</span><span class="sxs-lookup"><span data-stu-id="95402-178">To have an icon displayed next to the menu text, create a **DefaultIcon** subkey under **0** and set its default value to the icon's path and index.</span></span>
3.  <span data-ttu-id="95402-179">在 **0** 底下建立 **SearchGUID** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="95402-179">Create a **SearchGUID** subkey under **0**.</span></span> <span data-ttu-id="95402-180">將 GUID 指派給 DHTML 檔案，並將 **SearchGUID** 的預設值設定為其字串格式。</span><span class="sxs-lookup"><span data-stu-id="95402-180">Assign a GUID to the DHTML document and set the default value of **SearchGUID** to its string form.</span></span> <span data-ttu-id="95402-181">此 GUID 不需要在 **HKEY \_ 類別的 \_ 根目錄 \\ CLSID** 下註冊。</span><span class="sxs-lookup"><span data-stu-id="95402-181">This GUID does not need to be registered under **HKEY\_CLASSES\_ROOT\\CLSID**.</span></span>
4.  <span data-ttu-id="95402-182">在 **SearchGUID** 下建立 **Url** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="95402-182">Create a **Url** subkey under **SearchGUID**.</span></span> <span data-ttu-id="95402-183">將其預設值設定為將會出現在 Explorer 列中的 HTML 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="95402-183">Set its default value to the path of the HTML document that will appear in the Explorer bar.</span></span>
5.  <span data-ttu-id="95402-184">在 **SearchGUID** 下建立 **UrlNavNew** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="95402-184">Create a **UrlNavNew** subkey under **SearchGUID**.</span></span> <span data-ttu-id="95402-185">將其預設值設定為顯示在 Explorer 列右邊的 HTML 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="95402-185">Set its default value to the path of the HTML document that will appear to the right of the Explorer bar.</span></span>

<span data-ttu-id="95402-186">下列範例會註冊實作為 DHTML 檔案的 **MySearchEngine** 搜尋處理常式。</span><span class="sxs-lookup"><span data-stu-id="95402-186">The following example registers the **MySearchEngine** search handler implemented as a DHTML document.</span></span> <span data-ttu-id="95402-187">功能表文字是「我的搜尋引擎」，其中 M 指定為快速鍵。</span><span class="sxs-lookup"><span data-stu-id="95402-187">The menu text is "My Search Engine", with M specified as the shortcut key.</span></span> <span data-ttu-id="95402-188">此圖示為 C： \\ MyDir \\MySearch.dll，索引為2。</span><span class="sxs-lookup"><span data-stu-id="95402-188">The icon is in C:\\MyDir\\MySearch.dll, with an index of 2.</span></span> <span data-ttu-id="95402-189">Explorer 列的 DHTML 檔案是 C： \\ MyDir \\MySearch.htm，而顯示在 Explorer 列右邊的檔是 c： \\ MyDir \\MySearchPage.htm。</span><span class="sxs-lookup"><span data-stu-id="95402-189">The Explorer bar's DHTML document is C:\\MyDir\\MySearch.htm, and the document that will be displayed to the right of the Explorer bar is C:\\MyDir\\MySearchPage.htm.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {169A0691-8DF9-11d1-A1C4-00C04FD75D13}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
                                 SearchGUID
                                    (Default) = {My Search GUID}
                                    Url
                                       (Default) = C:\MyDir\MySearch.htm
                                    UrlNavNew
                                       (Default) = C:\MyDir\MySearchPage.htm
```

### <a name="registering-a-dynamic-search-handler"></a><span data-ttu-id="95402-190">註冊動態搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-190">Registering a Dynamic Search Handler</span></span>

<span data-ttu-id="95402-191">如果您的處理常式實作為 [快捷方式功能表處理常式](/windows/desktop/shell/context-menu-handlers)，您也可以將它註冊為動態處理常式。</span><span class="sxs-lookup"><span data-stu-id="95402-191">If your handler is implemented as a [shortcut menu handler](/windows/desktop/shell/context-menu-handlers), you can also register it as a dynamic handler.</span></span> <span data-ttu-id="95402-192">在這種情況下，它會使用 Shell 載入，而且只會在 Shell 結束時終止。</span><span class="sxs-lookup"><span data-stu-id="95402-192">In that case, it will be loaded with the Shell and will terminate only when the Shell exits.</span></span> <span data-ttu-id="95402-193">當使用者啟動動態搜尋處理常式時，動態搜尋處理常式的回應速度會比靜態處理常式更快。</span><span class="sxs-lookup"><span data-stu-id="95402-193">Dynamic search handlers respond much more quickly than static handlers when they are launched by the user.</span></span> <span data-ttu-id="95402-194">如果處理常式的 DLL 可能需要很長的時間載入，或可能經常呼叫，這個方法的效果最好。</span><span class="sxs-lookup"><span data-stu-id="95402-194">This approach works best if your handler's DLL might take a long time to load, or if it is likely to be called frequently.</span></span>

<span data-ttu-id="95402-195">動態搜尋處理常式會在 **FindExtensions** 子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="95402-195">Dynamic search handlers are registered under the **FindExtensions** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

<span data-ttu-id="95402-196">針對處理常式建立名為 **FindExtensions** 的子機碼，並將其預設值設定為處理常式的 CLSID GUID。</span><span class="sxs-lookup"><span data-stu-id="95402-196">Create a subkey of **FindExtensions** named for the handler, and set its default value to the handler's CLSID GUID.</span></span> <span data-ttu-id="95402-197">動態搜尋處理常式不支援功能表圖示。</span><span class="sxs-lookup"><span data-stu-id="95402-197">Menu icons are not supported for dynamic search handlers.</span></span> <span data-ttu-id="95402-198">下列範例會將 MySearchEngine 註冊為動態搜尋處理常式。</span><span class="sxs-lookup"><span data-stu-id="95402-198">The following example registers MySearchEngine as a dynamic search handler.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     MySearchEngine
                        (Default) = {MySearchEngine CLSID GUID}
                        0
                           (Default) = &My Search Engine
```

<span data-ttu-id="95402-199">與靜態搜尋處理常式不同的是，您不會在登錄中指定功能表文字。</span><span class="sxs-lookup"><span data-stu-id="95402-199">Unlike static search handlers, you do not specify the menu text in the registry.</span></span> <span data-ttu-id="95402-200">載入處理常式時，Shell 會呼叫處理常式的 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 方法，將專案加入至 [ **尋找** ] 或 [ **搜尋** ] 子功能表。</span><span class="sxs-lookup"><span data-stu-id="95402-200">When the handler is loaded, the Shell will call the handler's [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) method to add items to the **Find** or **Search** submenu.</span></span>

## <a name="implementing-search-handlers"></a><span data-ttu-id="95402-201">執行搜尋處理常式</span><span class="sxs-lookup"><span data-stu-id="95402-201">Implementing Search Handlers</span></span>

<span data-ttu-id="95402-202">搜尋處理常式可以實作為所有 Windows 版本的快捷方式功能表處理常式。</span><span class="sxs-lookup"><span data-stu-id="95402-202">Search handlers can be implemented as shortcut menu handlers for all versions of Windows.</span></span> <span data-ttu-id="95402-203">針對 Windows 2000，也可以將它們實作為 DHTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="95402-203">For Windows 2000, they can also be implemented as DHTML documents.</span></span>

<span data-ttu-id="95402-204">如需如何執行快捷方式功能表處理常式的一般討論，請參閱 [建立內容功能表處理常式](/windows/desktop/shell/context-menu-handlers)。</span><span class="sxs-lookup"><span data-stu-id="95402-204">For a general discussion of how to implement shortcut menu handlers, see [Creating Context Menu Handlers](/windows/desktop/shell/context-menu-handlers).</span></span> <span data-ttu-id="95402-205">搜尋處理常式不同于標準快捷方式功能表處理常式，只是幾種方式。</span><span class="sxs-lookup"><span data-stu-id="95402-205">Search handlers differ from standard shortcut menu handlers in only a few ways.</span></span>

<span data-ttu-id="95402-206">若為靜態功能表處理常式，則會從登錄中的資訊建立 [ **尋找** ] 或 [ **搜尋** ] 子功能表。</span><span class="sxs-lookup"><span data-stu-id="95402-206">For static menu handlers, the **Find** or **Search** submenu is created from the information in the registry.</span></span> <span data-ttu-id="95402-207">您不需要讓處理常式加入功能表項目，因為一般的快捷方式功能表處理常式會這樣做。</span><span class="sxs-lookup"><span data-stu-id="95402-207">There is no need to have the handler add a menu item, as a normal shortcut menu handler would.</span></span> <span data-ttu-id="95402-208">Shell 會以下列方式管理靜態功能表處理常式。</span><span class="sxs-lookup"><span data-stu-id="95402-208">The Shell manages static menu handlers in the following way.</span></span>

-   <span data-ttu-id="95402-209">當使用者啟動處理常式的功能表項目時，Shell 會載入處理常式的 DLL，並呼叫 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 來通知處理常式啟動搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="95402-209">When the user launches the handler's menu item, the Shell loads the handler's DLL and calls [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) to notify the handler to launch the search engine.</span></span> <span data-ttu-id="95402-210">不會呼叫 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) 和 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 方法。</span><span class="sxs-lookup"><span data-stu-id="95402-210">The [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) and [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) methods are not called.</span></span>
-   <span data-ttu-id="95402-211">呼叫 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)時，傳入的 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)結構的 **lpVerb** 成員會識別命令。</span><span class="sxs-lookup"><span data-stu-id="95402-211">When [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called, the **lpVerb** member of the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure that is passed in identifies the command.</span></span> <span data-ttu-id="95402-212">**LpVerb** 的低序位字組會設定為與命令子機碼名稱相等的數位。</span><span class="sxs-lookup"><span data-stu-id="95402-212">The low-order word of **lpVerb** is set to the numerical equivalent of the command's subkey name.</span></span> <span data-ttu-id="95402-213">因為這個子機碼通常會命名為 **0**，所以 **lpVerb** 通常會設定為零。</span><span class="sxs-lookup"><span data-stu-id="95402-213">Since this subkey is normally named **0**, **lpVerb** is usually set to zero.</span></span> <span data-ttu-id="95402-214">然後，處理常式應該啟動搜尋引擎。</span><span class="sxs-lookup"><span data-stu-id="95402-214">The handler should then launch the search engine.</span></span>

<span data-ttu-id="95402-215">動態搜尋處理常式的執行方式與一般快捷方式功能表處理常式的方式大致相同。</span><span class="sxs-lookup"><span data-stu-id="95402-215">Dynamic search handlers are implemented in much the same way as normal shortcut menu handlers.</span></span> <span data-ttu-id="95402-216">主要的例外狀況是在呼叫 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) 時， *pidlFolder* 和 *lpdobj* 引數都會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="95402-216">The primary exception is that when [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) is called, the *pidlFolder* and *lpdobj* arguments are set to **NULL**.</span></span>

<span data-ttu-id="95402-217">DHTML 搜尋處理常式會實作為一般 DHTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="95402-217">DHTML-based search handlers are implemented as a normal DHTML document.</span></span> <span data-ttu-id="95402-218">它們可以包含 Windows Internet Explorer 所支援的任何 HTML、DHTML 或腳本技術。</span><span class="sxs-lookup"><span data-stu-id="95402-218">They can include any HTML, DHTML, or scripting technology that is supported by Windows Internet Explorer.</span></span>

 

 