---
description: 您必須先註冊 Shell 擴充處理常式物件，Shell 才能使用它。 本主題是如何註冊 Shell 擴充處理常式的一般討論。
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: 註冊 Shell 延伸模組處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973473"
---
# <a name="registering-shell-extension-handlers"></a><span data-ttu-id="08c3d-104">註冊 Shell 延伸模組處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-104">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="08c3d-105">您必須先註冊 Shell 擴充處理常式物件，Shell 才能使用它。</span><span class="sxs-lookup"><span data-stu-id="08c3d-105">A Shell extension handler object must be registered before the Shell can use it.</span></span> <span data-ttu-id="08c3d-106">本主題是如何註冊 Shell 擴充處理常式的一般討論。</span><span class="sxs-lookup"><span data-stu-id="08c3d-106">This topic is a general discussion of how to register a Shell extension handler.</span></span>

<span data-ttu-id="08c3d-107">每當您建立或變更 Shell 延伸模組處理常式時，請務必通知系統您已進行變更。</span><span class="sxs-lookup"><span data-stu-id="08c3d-107">Any time you create or change a Shell extension handler, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="08c3d-108">若要這麼做，請呼叫 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)，並指定 **SHCNE \_ ASSOCCHANGED** 事件。</span><span class="sxs-lookup"><span data-stu-id="08c3d-108">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="08c3d-109">如果您未呼叫 **SHChangeNotify**，在系統重新開機之前，可能無法辨識變更。</span><span class="sxs-lookup"><span data-stu-id="08c3d-109">If you do not call **SHChangeNotify**, the change might not be recognized until the system is rebooted.</span></span>

<span data-ttu-id="08c3d-110">還有一些適用于 Windows 2000 系統的其他因素。</span><span class="sxs-lookup"><span data-stu-id="08c3d-110">There are some additional factors that apply to Windows 2000 systems.</span></span> <span data-ttu-id="08c3d-111">如需詳細資訊，請參閱在 [Windows 2000 系統上註冊 Shell 擴充處理常式](#registering-shell-extension-handlers) 一節。</span><span class="sxs-lookup"><span data-stu-id="08c3d-111">For details, see the [Registering Shell Extension Handlers on Windows 2000 Systems](#registering-shell-extension-handlers) section.</span></span>

<span data-ttu-id="08c3d-112">如同所有元件物件模型 (COM) 物件，您必須使用 Windows 軟體開發套件 (SDK) 提供的工具（例如 Guidgen.exe）來建立處理常式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="08c3d-112">As with all Component Object Model (COM) objects, you must create a GUID for the handler using a tool such as Guidgen.exe, which is provided with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="08c3d-113">在 **HKEY \_ 類別 \_ 根目錄** CLSID 下建立子機碼， \\ 其名稱是該 GUID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="08c3d-113">Create a subkey under **HKEY\_CLASSES\_ROOT**\\**CLSID** whose name is the string form of that GUID.</span></span> <span data-ttu-id="08c3d-114">由於 Shell 擴充處理常式是同進程伺服器，因此您也必須在該 GUID 子機碼底下建立 **InprocServer32** 子機碼，並將 (預設) 值設定為處理常式 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="08c3d-114">Because Shell extension handlers are in-process servers, you also must create an **InprocServer32** subkey under that GUID subkey with the (Default) value set to the path of the handler's DLL.</span></span> <span data-ttu-id="08c3d-115">使用單元執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="08c3d-115">Use the apartment threading model.</span></span> <span data-ttu-id="08c3d-116">以下顯示一個範例：</span><span class="sxs-lookup"><span data-stu-id="08c3d-116">An example is shown here:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

<span data-ttu-id="08c3d-117">每當 Shell 採取的動作都可能牽涉到 Shell 擴充處理常式時，就會檢查適當的登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="08c3d-117">Any time the Shell takes an action that can involve a Shell extension handler, it checks the appropriate registry subkey.</span></span> <span data-ttu-id="08c3d-118">擴充功能處理常式在呼叫時，所使用的子機碼控制項。</span><span class="sxs-lookup"><span data-stu-id="08c3d-118">The subkey under which an extension handler is registered controls when it will be called.</span></span> <span data-ttu-id="08c3d-119">比方說，當 Shell 針對 [檔案類型](fa-file-types.md)的成員顯示快捷方式功能表時，會呼叫快捷方式功能表處理常式，是常見的作法。</span><span class="sxs-lookup"><span data-stu-id="08c3d-119">For instance, it is a common practice to have a shortcut menu handler called when the Shell displays a shortcut menu for a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="08c3d-120">在此情況下，處理常式必須在檔案類型的 **ProgID** 子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="08c3d-120">In this case, the handler must be registered under the file type's **ProgID** subkey.</span></span>

<span data-ttu-id="08c3d-121">本主題將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="08c3d-121">This topic discusses the following subjects:</span></span>

-   [<span data-ttu-id="08c3d-122">處理常式名稱</span><span class="sxs-lookup"><span data-stu-id="08c3d-122">Handler Names</span></span>](#handler-names)
-   [<span data-ttu-id="08c3d-123">預先定義的 Shell 物件</span><span class="sxs-lookup"><span data-stu-id="08c3d-123">Predefined Shell Objects</span></span>](#predefined-shell-objects)
-   [<span data-ttu-id="08c3d-124">擴充處理常式註冊的範例</span><span class="sxs-lookup"><span data-stu-id="08c3d-124">Example of an Extension Handler Registration</span></span>](#example-of-an-extension-handler-registration)
    -   [<span data-ttu-id="08c3d-125">註冊 Shell 延伸模組處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-125">Registering Shell Extension Handlers</span></span>](#registering-shell-extension-handlers)
-   [<span data-ttu-id="08c3d-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="08c3d-126">Related topics</span></span>](#related-topics)

## <a name="handler-names"></a><span data-ttu-id="08c3d-127">處理常式名稱</span><span class="sxs-lookup"><span data-stu-id="08c3d-127">Handler Names</span></span>

<span data-ttu-id="08c3d-128">若要啟用 Shell 延伸模組處理常式，請使用處理程式子機碼名稱來建立子機碼 (在 [檔) 類型] 的 **ProgID** (的 [ **ShellEx** ] 子機碼下) ，或 ([預先定義之 \_ shell \_ 物件](handlers.md)的 [shell 物件類型名稱) ]。</span><span class="sxs-lookup"><span data-stu-id="08c3d-128">To enable a Shell extension handler, create a subkey with the handler subkey name (see below) under the **ShellEx** subkey of either the **ProgID** (for file types) or the Shell object type name (for [predefined\_shell\_objects](handlers.md)).</span></span>

<span data-ttu-id="08c3d-129">例如，如果您想要註冊 Myprogram.exe 的快捷方式功能表延伸模組處理常式，請先建立下列子機碼：</span><span class="sxs-lookup"><span data-stu-id="08c3d-129">For example, if you wanted to register a shortcut menu extension handler for MyProgram.1, you begin by creating the following subkey:</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

<span data-ttu-id="08c3d-130">針對下列處理常式，請在名為的「處理常式子機碼名稱」子機碼底下建立子機碼，並將其命名為 Shell 延伸模組 (CLSID) 的字串版本。</span><span class="sxs-lookup"><span data-stu-id="08c3d-130">For the following handlers, create a subkey underneath the "Handler Subkey name" subkey named as the string version of the class identifier (CLSID) of the Shell extension.</span></span> <span data-ttu-id="08c3d-131">藉由建立多個子機碼，可以在處理常式子機碼名稱下註冊多個擴充功能。</span><span class="sxs-lookup"><span data-stu-id="08c3d-131">Multiple extensions can be registered under the handler subkey name by creating multiple subkeys.</span></span>



| <span data-ttu-id="08c3d-132">處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-132">Handler</span></span>                 | <span data-ttu-id="08c3d-133">介面</span><span class="sxs-lookup"><span data-stu-id="08c3d-133">Interface</span></span>          | <span data-ttu-id="08c3d-134">處理常式子機碼名稱</span><span class="sxs-lookup"><span data-stu-id="08c3d-134">Handler Subkey Name</span></span>       |
|-------------------------|--------------------|---------------------------|
| <span data-ttu-id="08c3d-135">資料行提供者處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-135">Column provider handler</span></span> | <span data-ttu-id="08c3d-136">IColumnProvider</span><span class="sxs-lookup"><span data-stu-id="08c3d-136">IColumnProvider</span></span>    | <span data-ttu-id="08c3d-137">**ColumnHandlers**</span><span class="sxs-lookup"><span data-stu-id="08c3d-137">**ColumnHandlers**</span></span>        |
| <span data-ttu-id="08c3d-138">快速鍵功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-138">Shortcut menu handler</span></span>   | <span data-ttu-id="08c3d-139">ICoNtextMenu</span><span class="sxs-lookup"><span data-stu-id="08c3d-139">IContextMenu</span></span>       | <span data-ttu-id="08c3d-140">**CoNtextMenuHandlers**</span><span class="sxs-lookup"><span data-stu-id="08c3d-140">**ContextMenuHandlers**</span></span>   |
| <span data-ttu-id="08c3d-141">Copyhook 處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-141">Copyhook handler</span></span>        | <span data-ttu-id="08c3d-142">ICopyHook</span><span class="sxs-lookup"><span data-stu-id="08c3d-142">ICopyHook</span></span>          | <span data-ttu-id="08c3d-143">**CopyHookHandlers**</span><span class="sxs-lookup"><span data-stu-id="08c3d-143">**CopyHookHandlers**</span></span>      |
| <span data-ttu-id="08c3d-144">拖放功能處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-144">Drag-and-drop handler</span></span>   | <span data-ttu-id="08c3d-145">ICoNtextMenu</span><span class="sxs-lookup"><span data-stu-id="08c3d-145">IContextMenu</span></span>       | <span data-ttu-id="08c3d-146">**DragDropHandlers**</span><span class="sxs-lookup"><span data-stu-id="08c3d-146">**DragDropHandlers**</span></span>      |
| <span data-ttu-id="08c3d-147">屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-147">Property sheet handler</span></span>  | <span data-ttu-id="08c3d-148">IShellPropSheetExt</span><span class="sxs-lookup"><span data-stu-id="08c3d-148">IShellPropSheetExt</span></span> | <span data-ttu-id="08c3d-149">**PropertySheetHandlers**</span><span class="sxs-lookup"><span data-stu-id="08c3d-149">**PropertySheetHandlers**</span></span> |



 

<span data-ttu-id="08c3d-150">針對下列處理常式，「處理常式子機碼名稱」索引鍵的預設值是 Shell 延伸模組之 CLSID 的字串版本。</span><span class="sxs-lookup"><span data-stu-id="08c3d-150">For the following handlers, the default value of the "Handler Subkey Name" key is the string version of the CLSID of the Shell extension.</span></span> <span data-ttu-id="08c3d-151">您只能為這些處理常式註冊一個擴充功能。</span><span class="sxs-lookup"><span data-stu-id="08c3d-151">Only one extension can be registered for these handlers.</span></span>



| <span data-ttu-id="08c3d-152">處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-152">Handler</span></span>                 | <span data-ttu-id="08c3d-153">介面</span><span class="sxs-lookup"><span data-stu-id="08c3d-153">Interface</span></span>            | <span data-ttu-id="08c3d-154">處理常式子機碼名稱</span><span class="sxs-lookup"><span data-stu-id="08c3d-154">Handler Subkey Name</span></span>                        |
|-------------------------|----------------------|--------------------------------------------|
| <span data-ttu-id="08c3d-155">資料處理程式</span><span class="sxs-lookup"><span data-stu-id="08c3d-155">Data handler</span></span>            | <span data-ttu-id="08c3d-156">IDataObject</span><span class="sxs-lookup"><span data-stu-id="08c3d-156">IDataObject</span></span>          | <span data-ttu-id="08c3d-157">**DataHandler**</span><span class="sxs-lookup"><span data-stu-id="08c3d-157">**DataHandler**</span></span>                            |
| <span data-ttu-id="08c3d-158">捨棄處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-158">Drop handler</span></span>            | <span data-ttu-id="08c3d-159">IDropTarget</span><span class="sxs-lookup"><span data-stu-id="08c3d-159">IDropTarget</span></span>          | <span data-ttu-id="08c3d-160">**DropHandler**</span><span class="sxs-lookup"><span data-stu-id="08c3d-160">**DropHandler**</span></span>                            |
| <span data-ttu-id="08c3d-161">圖示處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-161">Icon handler</span></span>            | <span data-ttu-id="08c3d-162">IExtractIconA/W</span><span class="sxs-lookup"><span data-stu-id="08c3d-162">IExtractIconA/W</span></span>      | <span data-ttu-id="08c3d-163">**IconHandler**</span><span class="sxs-lookup"><span data-stu-id="08c3d-163">**IconHandler**</span></span>                            |
| <span data-ttu-id="08c3d-164">縮圖影像處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-164">Thumbnail image handler</span></span> | <span data-ttu-id="08c3d-165">IThumbnailProvider</span><span class="sxs-lookup"><span data-stu-id="08c3d-165">IThumbnailProvider</span></span>   | <span data-ttu-id="08c3d-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span><span class="sxs-lookup"><span data-stu-id="08c3d-166">**{E357FCCD-A995-4576-B01F-234630154E96}**</span></span> |
| <span data-ttu-id="08c3d-167">資訊提示處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-167">Infotip handler</span></span>         | <span data-ttu-id="08c3d-168">IQueryInfo</span><span class="sxs-lookup"><span data-stu-id="08c3d-168">IQueryInfo</span></span>           | <span data-ttu-id="08c3d-169">**{00021500-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="08c3d-169">**{00021500-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="08c3d-170"> (ANSI) 的 Shell 連結</span><span class="sxs-lookup"><span data-stu-id="08c3d-170">Shell link (ANSI)</span></span>       | <span data-ttu-id="08c3d-171">IShellLinkA</span><span class="sxs-lookup"><span data-stu-id="08c3d-171">IShellLinkA</span></span>          | <span data-ttu-id="08c3d-172">**{000214EE-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="08c3d-172">**{000214EE-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="08c3d-173">Shell 連結 (UNICODE) </span><span class="sxs-lookup"><span data-stu-id="08c3d-173">Shell link (UNICODE)</span></span>    | <span data-ttu-id="08c3d-174">IShellLinkW</span><span class="sxs-lookup"><span data-stu-id="08c3d-174">IShellLinkW</span></span>          | <span data-ttu-id="08c3d-175">**{000214F9-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="08c3d-175">**{000214F9-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="08c3d-176">結構化儲存體</span><span class="sxs-lookup"><span data-stu-id="08c3d-176">Structured storage</span></span>      | <span data-ttu-id="08c3d-177">IStorage</span><span class="sxs-lookup"><span data-stu-id="08c3d-177">IStorage</span></span>             | <span data-ttu-id="08c3d-178">**{0000000B-0000-0000-C000-000000000046}**</span><span class="sxs-lookup"><span data-stu-id="08c3d-178">**{0000000B-0000-0000-C000-000000000046}**</span></span> |
| <span data-ttu-id="08c3d-179">中繼資料</span><span class="sxs-lookup"><span data-stu-id="08c3d-179">Metadata</span></span>                | <span data-ttu-id="08c3d-180">IPropertySetStorage</span><span class="sxs-lookup"><span data-stu-id="08c3d-180">IPropertySetStorage</span></span>  | <span data-ttu-id="08c3d-181">**PropertyHandler**</span><span class="sxs-lookup"><span data-stu-id="08c3d-181">**PropertyHandler**</span></span>                        |
| <span data-ttu-id="08c3d-182">釘選到開始功能表</span><span class="sxs-lookup"><span data-stu-id="08c3d-182">Pin to Start Menu</span></span>       | <span data-ttu-id="08c3d-183">IStartMenuPinnedList</span><span class="sxs-lookup"><span data-stu-id="08c3d-183">IStartMenuPinnedList</span></span> | <span data-ttu-id="08c3d-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span><span class="sxs-lookup"><span data-stu-id="08c3d-184">**{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}**</span></span> |
| <span data-ttu-id="08c3d-185">釘選到工作列</span><span class="sxs-lookup"><span data-stu-id="08c3d-185">Pin to Taskbar</span></span>          |                      | <span data-ttu-id="08c3d-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span><span class="sxs-lookup"><span data-stu-id="08c3d-186">**{90AA3A4E-1CBA-4233-B8BB-535773D48449}**</span></span> |



 

<span data-ttu-id="08c3d-187">只有包含 [IsShortCut](./links.md)專案的檔案類型才需要指定的子機碼，以將 [釘選到 **開始] 功能表** 和 [**釘選到工作列**] 新增至專案的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="08c3d-187">The subkeys specified to add **Pin to Start Menu** and **Pin to Taskbar** to an item's shortcut menu are only required for file types that include the [IsShortCut](./links.md) entry.</span></span>

## <a name="predefined-shell-objects"></a><span data-ttu-id="08c3d-188">預先定義的 Shell 物件</span><span class="sxs-lookup"><span data-stu-id="08c3d-188">Predefined Shell Objects</span></span>

<span data-ttu-id="08c3d-189">Shell 會在 **HKEY \_ 類別 \_ 根目錄** 下定義其他物件，其可透過與檔案類型相同的方式來擴充。</span><span class="sxs-lookup"><span data-stu-id="08c3d-189">The Shell defines additional objects under **HKEY\_CLASSES\_ROOT** which can be extended in the same way as file types.</span></span> <span data-ttu-id="08c3d-190">例如，若要新增所有檔案的屬性工作表處理常式，您可以在 **PropertySheetHandlers** 子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="08c3d-190">For example, to add a property sheet handler for all files, you can register under the **PropertySheetHandlers** subkey.</span></span>

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

<span data-ttu-id="08c3d-191">下表提供 **HKEY \_ 類別 \_ 根目錄** 的各種子機碼，您可以在這些子機碼下註冊擴充處理常式。</span><span class="sxs-lookup"><span data-stu-id="08c3d-191">The following table gives the various subkeys of **HKEY\_CLASSES\_ROOT** under which extension handlers can be registered.</span></span> <span data-ttu-id="08c3d-192">請注意，許多擴充程式處理常式無法在所有列出的子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="08c3d-192">Note that many extension handlers cannot be registered under all of the listed subkeys.</span></span> <span data-ttu-id="08c3d-193">如需進一步的詳細資料，請參閱特定處理常式的檔。</span><span class="sxs-lookup"><span data-stu-id="08c3d-193">For further details, see the specific handler's documentation.</span></span>



| <span data-ttu-id="08c3d-194">子機碼</span><span class="sxs-lookup"><span data-stu-id="08c3d-194">Subkey</span></span>                    | <span data-ttu-id="08c3d-195">Description</span><span class="sxs-lookup"><span data-stu-id="08c3d-195">Description</span></span>                                                          | <span data-ttu-id="08c3d-196">可能的處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-196">Possible Handlers</span></span>                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="08c3d-197">\**\** _</span><span class="sxs-lookup"><span data-stu-id="08c3d-197">\**\** _</span></span>                    | <span data-ttu-id="08c3d-198">所有檔案</span><span class="sxs-lookup"><span data-stu-id="08c3d-198">All files</span></span>                                                            | <span data-ttu-id="08c3d-199">快速鍵功能表、屬性工作表、動詞 (請參閱以下) </span><span class="sxs-lookup"><span data-stu-id="08c3d-199">Shortcut Menu, Property Sheet, Verbs (see below)</span></span> |
| <span data-ttu-id="08c3d-200">_ *AllFileSystemObjects*\*</span><span class="sxs-lookup"><span data-stu-id="08c3d-200">_ *AllFileSystemObjects*\*</span></span>  | <span data-ttu-id="08c3d-201">所有檔案和檔案資料夾</span><span class="sxs-lookup"><span data-stu-id="08c3d-201">All files and file folders</span></span>                                           | <span data-ttu-id="08c3d-202">快速鍵功能表、屬性工作表、動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-202">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="08c3d-203">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="08c3d-203">**Folder**</span></span>                | <span data-ttu-id="08c3d-204">全部資料夾</span><span class="sxs-lookup"><span data-stu-id="08c3d-204">All folders</span></span>                                                          | <span data-ttu-id="08c3d-205">快速鍵功能表、屬性工作表、動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-205">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="08c3d-206">**目錄**</span><span class="sxs-lookup"><span data-stu-id="08c3d-206">**Directory**</span></span>             | <span data-ttu-id="08c3d-207">資料夾</span><span class="sxs-lookup"><span data-stu-id="08c3d-207">File folders</span></span>                                                         | <span data-ttu-id="08c3d-208">快速鍵功能表、屬性工作表、動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-208">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="08c3d-209">**目錄 \\ 背景**</span><span class="sxs-lookup"><span data-stu-id="08c3d-209">**Directory\\Background**</span></span> | <span data-ttu-id="08c3d-210">檔案資料夾背景</span><span class="sxs-lookup"><span data-stu-id="08c3d-210">File folder background</span></span>                                               | <span data-ttu-id="08c3d-211">僅快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="08c3d-211">Shortcut Menu only</span></span>                               |
| <span data-ttu-id="08c3d-212">**DesktopBackground**</span><span class="sxs-lookup"><span data-stu-id="08c3d-212">**DesktopBackground**</span></span>     | <span data-ttu-id="08c3d-213">桌面背景 (Windows 7 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="08c3d-213">Desktop background (Windows 7 and higher)</span></span>                            | <span data-ttu-id="08c3d-214">快捷方式功能表，動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-214">Shortcut Menu, Verbs</span></span>                             |
| <span data-ttu-id="08c3d-215">**磁碟機**</span><span class="sxs-lookup"><span data-stu-id="08c3d-215">**Drive**</span></span>                 | <span data-ttu-id="08c3d-216">MyComputer 中的所有磁片磁碟機，例如 "C： \\ "</span><span class="sxs-lookup"><span data-stu-id="08c3d-216">All drives in MyComputer, such as "C:\\"</span></span>                             | <span data-ttu-id="08c3d-217">快速鍵功能表、屬性工作表、動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-217">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="08c3d-218">**Network**</span><span class="sxs-lookup"><span data-stu-id="08c3d-218">**Network**</span></span>               | <span data-ttu-id="08c3d-219">網路下的整個網路 () </span><span class="sxs-lookup"><span data-stu-id="08c3d-219">Entire network (under My Network Places)</span></span>                             | <span data-ttu-id="08c3d-220">快速鍵功能表、屬性工作表、動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-220">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="08c3d-221">**網路 \\ 類型\\\#**</span><span class="sxs-lookup"><span data-stu-id="08c3d-221">**Network\\Type\\\#**</span></span>     | <span data-ttu-id="08c3d-222"> (類型的所有物件 \# 如下所示) </span><span class="sxs-lookup"><span data-stu-id="08c3d-222">All objects of type \# (see below)</span></span>                                   | <span data-ttu-id="08c3d-223">快速鍵功能表、屬性工作表、動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-223">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="08c3d-224">**NetShare**</span><span class="sxs-lookup"><span data-stu-id="08c3d-224">**NetShare**</span></span>              | <span data-ttu-id="08c3d-225">所有網路共用</span><span class="sxs-lookup"><span data-stu-id="08c3d-225">All network shares</span></span>                                                   | <span data-ttu-id="08c3d-226">快速鍵功能表、屬性工作表、動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-226">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="08c3d-227">**NetServer**</span><span class="sxs-lookup"><span data-stu-id="08c3d-227">**NetServer**</span></span>             | <span data-ttu-id="08c3d-228">所有網路伺服器</span><span class="sxs-lookup"><span data-stu-id="08c3d-228">All network servers</span></span>                                                  | <span data-ttu-id="08c3d-229">快速鍵功能表、屬性工作表、動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-229">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="08c3d-230">*網路 \_ 提供者 \_ 名稱*</span><span class="sxs-lookup"><span data-stu-id="08c3d-230">*network\_provider\_name*</span></span> | <span data-ttu-id="08c3d-231">網路提供者「*網路 \_ 提供者 \_ 名稱*」提供的所有物件</span><span class="sxs-lookup"><span data-stu-id="08c3d-231">All objects provided by network provider "*network\_provider\_name*"</span></span> | <span data-ttu-id="08c3d-232">快速鍵功能表、屬性工作表、動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-232">Shortcut Menu, Property Sheet, Verbs</span></span>             |
| <span data-ttu-id="08c3d-233">**印表機**</span><span class="sxs-lookup"><span data-stu-id="08c3d-233">**Printers**</span></span>              | <span data-ttu-id="08c3d-234">所有印表機</span><span class="sxs-lookup"><span data-stu-id="08c3d-234">All printers</span></span>                                                         | <span data-ttu-id="08c3d-235">快速鍵功能表，屬性工作表</span><span class="sxs-lookup"><span data-stu-id="08c3d-235">Shortcut Menu, Property Sheet</span></span>                    |
| <span data-ttu-id="08c3d-236">**AudioCD**</span><span class="sxs-lookup"><span data-stu-id="08c3d-236">**AudioCD**</span></span>               | <span data-ttu-id="08c3d-237">CD 光碟機中的音訊 CD</span><span class="sxs-lookup"><span data-stu-id="08c3d-237">Audio CD in CD drive</span></span>                                                 | <span data-ttu-id="08c3d-238">僅限動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-238">Verbs only</span></span>                                       |
| <span data-ttu-id="08c3d-239">**Dvd**</span><span class="sxs-lookup"><span data-stu-id="08c3d-239">**DVD**</span></span>                   | <span data-ttu-id="08c3d-240">DVD 光碟機 (Windows 2000) </span><span class="sxs-lookup"><span data-stu-id="08c3d-240">DVD drive (Windows 2000)</span></span>                                             | <span data-ttu-id="08c3d-241">快速鍵功能表、屬性工作表、動詞</span><span class="sxs-lookup"><span data-stu-id="08c3d-241">Shortcut Menu, Property Sheet, Verbs</span></span>             |



 

### <a name="notes"></a><span data-ttu-id="08c3d-242">備註</span><span class="sxs-lookup"><span data-stu-id="08c3d-242">Notes</span></span>

-   <span data-ttu-id="08c3d-243">您可以用滑鼠右鍵按一下檔案資料夾，而不是在資料夾的任何內容中，來存取檔案資料夾背景快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="08c3d-243">The file folder background shortcut menu is accessed by right-clicking within a file folder, but not over any of the folder's contents.</span></span>
-   <span data-ttu-id="08c3d-244">「動詞」是在 **HKEY \_ 類別 \_ 根** 子機碼 \\  \\ **Shell** \\ **動詞** 命令下註冊的特殊命令。</span><span class="sxs-lookup"><span data-stu-id="08c3d-244">"Verbs" are special commands registered under **HKEY\_CLASSES\_ROOT**\\*Subkey*\\**Shell**\\**Verb**.</span></span>
-   <span data-ttu-id="08c3d-245">針對 **網路** \\ **類型** \\ **\#** ，" \# " 是十進位中的網路提供者類型代碼。</span><span class="sxs-lookup"><span data-stu-id="08c3d-245">For **Network**\\**Type**\\**\#**, "\#" is a network provider type code in decimal.</span></span> <span data-ttu-id="08c3d-246">網路提供者類型代碼是網路類型的最高文字。</span><span class="sxs-lookup"><span data-stu-id="08c3d-246">The network provider type code is the high word of a network type.</span></span> <span data-ttu-id="08c3d-247">網路類型清單是在 Winnetwk 中提供的， (WNNC \_ NET \_ \* values) 。</span><span class="sxs-lookup"><span data-stu-id="08c3d-247">The list of network types is given in the Winnetwk.h header file (WNNC\_NET\_\* values).</span></span> <span data-ttu-id="08c3d-248">例如，WNNC \_ NET \_ SHIVA 是0x00330000，因此對應的型別子機碼會是 **HKEY 類別的 \_ \_ ROOT** \\ **Network** \\ **type** \\ **51**。</span><span class="sxs-lookup"><span data-stu-id="08c3d-248">For example, WNNC\_NET\_SHIVA is 0x00330000, so the corresponding type subkey would be **HKEY\_CLASSES\_ROOT**\\**Network**\\**Type**\\**51**.</span></span>
-   <span data-ttu-id="08c3d-249">「*網路 \_ 提供者 \_ 名稱*」是 [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)所指定的網路提供者名稱，並已將空格轉換成底線。</span><span class="sxs-lookup"><span data-stu-id="08c3d-249">"*network\_provider\_name*" is a network provider name as specified by [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), with the spaces converted into underscores.</span></span> <span data-ttu-id="08c3d-250">例如，如果已安裝 Microsoft 網路網路提供者，其提供者名稱為「Microsoft Windows 網路」，而對應的 *網路 \_ 提供者 \_ 名稱* 為 **Microsoft \_ windows \_ network**。</span><span class="sxs-lookup"><span data-stu-id="08c3d-250">For example, if the Microsoft Networking network provider is installed, its provider name is "Microsoft Windows Network", and the corresponding *network\_provider\_name* is **Microsoft\_Windows\_Network**.</span></span>

## <a name="example-of-an-extension-handler-registration"></a><span data-ttu-id="08c3d-251">擴充處理常式註冊的範例</span><span class="sxs-lookup"><span data-stu-id="08c3d-251">Example of an Extension Handler Registration</span></span>

<span data-ttu-id="08c3d-252">若要啟用特定處理常式，請使用處理程式的名稱，在擴充處理常式類型子機碼底下建立子機碼。</span><span class="sxs-lookup"><span data-stu-id="08c3d-252">To enable a particular handler, create a subkey under the extension handler type subkey with the name of the handler.</span></span> <span data-ttu-id="08c3d-253">Shell 不會使用處理程式的名稱，但它必須與該類型子機碼下的所有其他名稱不同。</span><span class="sxs-lookup"><span data-stu-id="08c3d-253">The Shell does not use the handler's name, but it must be different from all other names under that type subkey.</span></span> <span data-ttu-id="08c3d-254">將名稱子機碼的預設值設定為處理常式 GUID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="08c3d-254">Set the default value of the name subkey to the string form of the handler's GUID.</span></span>

<span data-ttu-id="08c3d-255">下列範例說明使用 myp 檔案類型啟用快捷方式功能表和屬性工作表延伸模組處理常式的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="08c3d-255">The following example illustrates registry entries that enable shortcut menu and property sheet extension handlers, using an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a><span data-ttu-id="08c3d-256">註冊 Shell 延伸模組處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-256">Registering Shell Extension Handlers</span></span>

<span data-ttu-id="08c3d-257">本章節中討論的註冊程式必須遵循所有的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="08c3d-257">The registration procedure discussed in this section must be followed for all Windows systems.</span></span> <span data-ttu-id="08c3d-258">不過，在稍後的系統中，可能需要額外的步驟。</span><span class="sxs-lookup"><span data-stu-id="08c3d-258">However, with later systems, an additional step might be necessary.</span></span> <span data-ttu-id="08c3d-259">因為這些較新的 Windows 版本是設計用來在受控環境中使用，所以登錄的存取權可能會受到系統管理員限制，需要的安裝方式與上一節所述的安裝方式稍有不同。</span><span class="sxs-lookup"><span data-stu-id="08c3d-259">Because these later versions of Windows are designed to be used in a managed environment, access to the registry could be administratively restricted, requiring a somewhat different approach to installation than described in the previous section.</span></span>

> [!Note]  
> <span data-ttu-id="08c3d-260">安裝程式通常不應該直接寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="08c3d-260">Setup programs should generally not write directly to the registry.</span></span> <span data-ttu-id="08c3d-261">相反地，您應該使用 Windows Installer 套件來完成安裝程式。</span><span class="sxs-lookup"><span data-stu-id="08c3d-261">Instead, setup should be accomplished with Windows Installer packages.</span></span> <span data-ttu-id="08c3d-262">這些工具可確保軟體正常執行，並提供對每個使用者類別註冊等功能的存取。</span><span class="sxs-lookup"><span data-stu-id="08c3d-262">These tools ensure that software runs well and provides access to capabilities such as per-user class registration.</span></span>

 

<span data-ttu-id="08c3d-263">Shell 擴充處理常式會在 Shell 進程中執行。</span><span class="sxs-lookup"><span data-stu-id="08c3d-263">Shell extension handlers run in the Shell process.</span></span> <span data-ttu-id="08c3d-264">由於它是系統進程，因此系統管理員可以藉由將 **Explorer** 索引鍵的 EnforceShellExtensionSecurity 值設定為1，將 Shell 擴充處理常式限制在已核准清單上的處理常式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="08c3d-264">Because it is a system process, the administrator of a system can limit Shell extension handlers to those on an approved list by setting the EnforceShellExtensionSecurity value of the **Explorer** key to 1 as shown here:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

<span data-ttu-id="08c3d-265">若要將 Shell 擴充處理常式放在核准的清單上，請建立 **REG \_ SZ** 值，其名稱是在 **已核准** 子機碼下的處理常式 GUID 字串形式。</span><span class="sxs-lookup"><span data-stu-id="08c3d-265">To place a Shell extension handler on the approved list, create a **REG\_SZ** value whose name is the string form of the handler's GUID under the **Approved** subkey.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

<span data-ttu-id="08c3d-266">例如，下列範例會將 *MyCommand* 和 *MyPropSheet* 處理常式新增至核准的清單。</span><span class="sxs-lookup"><span data-stu-id="08c3d-266">For example, the following example adds the *MyCommand* and *MyPropSheet* handlers to the approved list.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

<span data-ttu-id="08c3d-267">Shell 不會使用指派給 GUID 的值，但應該設定為讓檢查登錄變得更容易。</span><span class="sxs-lookup"><span data-stu-id="08c3d-267">The Shell does not use the value that is assigned to the GUID, but it should be set to make inspecting the registry easier.</span></span>

<span data-ttu-id="08c3d-268">如果安裝應用程式的人員具有足夠的許可權，則您的安裝程式應用程式可以將值新增至 **核准** 的子機碼。</span><span class="sxs-lookup"><span data-stu-id="08c3d-268">Your setup application can add values to the **Approved** subkey only if the person installing the application has sufficient privileges.</span></span> <span data-ttu-id="08c3d-269">如果嘗試新增延伸模組處理常式失敗，您應該通知使用者需要系統管理許可權才能完整安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="08c3d-269">If the attempt to add an extension handler fails, you should inform the user that administrative privileges are required to fully install the application.</span></span> <span data-ttu-id="08c3d-270">如果處理常式對應用程式而言是必要的，您應該會使設定失敗，並通知使用者與系統管理員聯絡。</span><span class="sxs-lookup"><span data-stu-id="08c3d-270">If the handler is essential to the application, you should fail the setup and notify the user to contact an administrator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08c3d-271">相關主題</span><span class="sxs-lookup"><span data-stu-id="08c3d-271">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08c3d-272">初始化 Shell 擴充處理常式</span><span class="sxs-lookup"><span data-stu-id="08c3d-272">Initializing Shell Extension Handlers</span></span>](int-shell-exts.md)
</dt> </dl>

 

 
