---
description: Windows Shell 提供一組強大的自動化物件，可讓您以 Microsoft Visual Basic 和指令碼語言（例如 Microsoft JScript）來設計 Shell， (與 ECMA 262 語言規格相容) 和 Microsoft Visual Basic Scripting Edition (VBScript) 。 您可以使用這些物件來存取許多 Shell 的功能和對話方塊。 例如，您可以存取檔案系統、啟動程式，以及變更系統設定。
title: 可編寫腳本的 Shell 物件
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c39e7e58a9715598056fb74aa154ed8a850f523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973605"
---
# <a name="scriptable-shell-objects"></a><span data-ttu-id="cbea8-105">可編寫腳本的 Shell 物件</span><span class="sxs-lookup"><span data-stu-id="cbea8-105">Scriptable Shell Objects</span></span>

<span data-ttu-id="cbea8-106">Windows Shell 提供一組強大的自動化物件，可讓您以 Microsoft Visual Basic 和指令碼語言（例如 Microsoft JScript）來設計 Shell， (與 ECMA 262 語言規格相容) 和 Microsoft Visual Basic Scripting Edition (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="cbea8-106">The Windows Shell provides a powerful set of automation objects that enable you to program the Shell with Microsoft Visual Basic and scripting languages such as Microsoft JScript (compatible with ECMA 262 language specification) and Microsoft Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="cbea8-107">您可以使用這些物件來存取許多 Shell 的功能和對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cbea8-107">You can use these objects to access many of the Shell's features and dialog boxes.</span></span> <span data-ttu-id="cbea8-108">例如，您可以存取檔案系統、啟動程式，以及變更系統設定。</span><span class="sxs-lookup"><span data-stu-id="cbea8-108">For example, you can access the file system, launch programs, and change system settings.</span></span>

<span data-ttu-id="cbea8-109">本節介紹可編寫腳本的 Shell 物件。</span><span class="sxs-lookup"><span data-stu-id="cbea8-109">This section introduces the scriptable Shell objects.</span></span>

-   [<span data-ttu-id="cbea8-110">Shell 版本</span><span class="sxs-lookup"><span data-stu-id="cbea8-110">Shell Versions</span></span>](#shell-versions)
-   [<span data-ttu-id="cbea8-111">具現化 Shell 物件</span><span class="sxs-lookup"><span data-stu-id="cbea8-111">Instantiating Shell Objects</span></span>](#instantiating-shell-objects)
    -   [<span data-ttu-id="cbea8-112">晚期繫結</span><span class="sxs-lookup"><span data-stu-id="cbea8-112">Late Binding</span></span>](#late-binding)
    -   [<span data-ttu-id="cbea8-113">HTML 物件元素</span><span class="sxs-lookup"><span data-stu-id="cbea8-113">HTML OBJECT Element</span></span>](#html-object-element)
-   [<span data-ttu-id="cbea8-114">Shell 物件</span><span class="sxs-lookup"><span data-stu-id="cbea8-114">Shell Object</span></span>](#shell-object)
    -   [<span data-ttu-id="cbea8-115">安全性</span><span class="sxs-lookup"><span data-stu-id="cbea8-115">Security</span></span>](#security)
-   [<span data-ttu-id="cbea8-116">資料夾物件</span><span class="sxs-lookup"><span data-stu-id="cbea8-116">Folder Objects</span></span>](#folder-objects)

## <a name="shell-versions"></a><span data-ttu-id="cbea8-117">Shell 版本</span><span class="sxs-lookup"><span data-stu-id="cbea8-117">Shell Versions</span></span>

<span data-ttu-id="cbea8-118">許多 Shell 物件在 Shell 的 [4.71 版](versions.md) 中都有提供。</span><span class="sxs-lookup"><span data-stu-id="cbea8-118">Many of the Shell objects became available in [version 4.71](versions.md) of the Shell.</span></span> <span data-ttu-id="cbea8-119">其他則可在5.00 版和更新版本中使用。</span><span class="sxs-lookup"><span data-stu-id="cbea8-119">Others are available in version 5.00 and later.</span></span> <span data-ttu-id="cbea8-120">Windows 2000 已可使用5.00 版。</span><span class="sxs-lookup"><span data-stu-id="cbea8-120">Version 5.00 became available with Windows 2000.</span></span> <span data-ttu-id="cbea8-121">下表列出物件變成可用之 Shell 版本底下的每個 Shell 物件。</span><span class="sxs-lookup"><span data-stu-id="cbea8-121">The following table lists each Shell object under the version of the Shell in which the object became available.</span></span>



| <span data-ttu-id="cbea8-122">版本4.71</span><span class="sxs-lookup"><span data-stu-id="cbea8-122">Version 4.71</span></span>                                            | <span data-ttu-id="cbea8-123">版本5.00</span><span class="sxs-lookup"><span data-stu-id="cbea8-123">Version 5.00</span></span>                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="cbea8-124">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="cbea8-124">**Folder**</span></span>](folder.md)                                | [<span data-ttu-id="cbea8-125">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="cbea8-125">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)     |
| [<span data-ttu-id="cbea8-126">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="cbea8-126">**FolderItemVerb**</span></span>](folderitemverb.md)                | [<span data-ttu-id="cbea8-127">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="cbea8-127">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)   |
| [<span data-ttu-id="cbea8-128">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="cbea8-128">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | [<span data-ttu-id="cbea8-129">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-129">**Folder2**</span></span>](folder2-object.md)                     |
| [<span data-ttu-id="cbea8-130">**殼層**</span><span class="sxs-lookup"><span data-stu-id="cbea8-130">**Shell**</span></span>](shell.md)                                  | [<span data-ttu-id="cbea8-131">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="cbea8-131">**FolderItem**</span></span>](folderitem.md)                      |
| [<span data-ttu-id="cbea8-132">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="cbea8-132">**ShellFolderView**</span></span>](shellfolderview.md)              | [<span data-ttu-id="cbea8-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="cbea8-133">**FolderItems**</span></span>](folderitems.md)                    |
| [<span data-ttu-id="cbea8-134">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="cbea8-134">**ShellUIHelper**</span></span>](shelluihelper.md)                  | [<span data-ttu-id="cbea8-135">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-135">**FolderItems2**</span></span>](folderitems2-object.md)           |
| [<span data-ttu-id="cbea8-136">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="cbea8-136">**ShellWindows**</span></span>](shellwindows.md)                    | [<span data-ttu-id="cbea8-137">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-137">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)     |
| [<span data-ttu-id="cbea8-138">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="cbea8-138">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | [<span data-ttu-id="cbea8-139">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-139">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)     |
|                                                         | [<span data-ttu-id="cbea8-140">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="cbea8-140">**ShellFolderItem**</span></span>](shellfolderitem-object.md)     |
|                                                         | [<span data-ttu-id="cbea8-141">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="cbea8-141">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md) |
|                                                         | [<span data-ttu-id="cbea8-142">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="cbea8-142">**ShellLinkObject**</span></span>](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a><span data-ttu-id="cbea8-143">具現化 Shell 物件</span><span class="sxs-lookup"><span data-stu-id="cbea8-143">Instantiating Shell Objects</span></span>

<span data-ttu-id="cbea8-144">若要在使用早期繫結的 Visual Basic 應用程式中具現化 Shell 物件，請在您的專案中新增下列程式庫的參考：</span><span class="sxs-lookup"><span data-stu-id="cbea8-144">To instantiate the Shell objects in Visual Basic applications with early binding, add references to the following libraries in your project:</span></span>

-   <span data-ttu-id="cbea8-145">Microsoft Internet Controls (Shdocvw.dll) </span><span class="sxs-lookup"><span data-stu-id="cbea8-145">Microsoft Internet Controls (SHDocVw)</span></span>
-   <span data-ttu-id="cbea8-146">Microsoft Shell 控制項和自動化 (Shell32) </span><span class="sxs-lookup"><span data-stu-id="cbea8-146">Microsoft Shell Controls and Automation (Shell32)</span></span>

### <a name="late-binding"></a><span data-ttu-id="cbea8-147">晚期繫結</span><span class="sxs-lookup"><span data-stu-id="cbea8-147">Late Binding</span></span>

<span data-ttu-id="cbea8-148">您也可以使用晚期繫結將許多 Shell 物件具現化。</span><span class="sxs-lookup"><span data-stu-id="cbea8-148">You can also instantiate many of the Shell objects with late binding.</span></span> <span data-ttu-id="cbea8-149">這種方法適用于 Visual Basic 應用程式和腳本。</span><span class="sxs-lookup"><span data-stu-id="cbea8-149">This approach works in Visual Basic applications and in script.</span></span> <span data-ttu-id="cbea8-150">下列範例顯示如何在 JScript 中具現化 [**Shell**](shell.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="cbea8-150">The following example shows how to instantiate the [**Shell**](shell.md) object in JScript.</span></span>


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



<span data-ttu-id="cbea8-151">下列範例顯示如何在 VBScript 中具現化 [**資料夾**](folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="cbea8-151">The following example shows how to instantiate the [**Folder**](folder.md) object in VBScript.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



<span data-ttu-id="cbea8-152">在上述範例中， *sDir* 是 [**資料夾**](folder.md) 物件的路徑。</span><span class="sxs-lookup"><span data-stu-id="cbea8-152">In the preceding example, *sDir* is the path to the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="cbea8-153">請注意，腳本中無法使用 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 列舉值。</span><span class="sxs-lookup"><span data-stu-id="cbea8-153">Note that the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span>

<span data-ttu-id="cbea8-154">下表顯示每個 Shell 物件的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="cbea8-154">The ProgID for each of the Shell objects is shown in the following table.</span></span>



| <span data-ttu-id="cbea8-155">Object</span><span class="sxs-lookup"><span data-stu-id="cbea8-155">Object</span></span>                                                  | <span data-ttu-id="cbea8-156">ProgID</span><span class="sxs-lookup"><span data-stu-id="cbea8-156">ProgID</span></span>                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbea8-157">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="cbea8-157">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="cbea8-158">DiskQuota. 1</span><span class="sxs-lookup"><span data-stu-id="cbea8-158">Microsoft.DiskQuota.1</span></span>                                                                   |
| [<span data-ttu-id="cbea8-159">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="cbea8-159">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="cbea8-160">無法晚期繫結</span><span class="sxs-lookup"><span data-stu-id="cbea8-160">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="cbea8-161">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="cbea8-161">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="cbea8-162">殼。Shell \_ 應用程式。命名空間 ( "..." ) </span><span class="sxs-lookup"><span data-stu-id="cbea8-162">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="cbea8-163">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-163">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="cbea8-164">殼。Shell \_ 應用程式。命名空間 ( "..." ) </span><span class="sxs-lookup"><span data-stu-id="cbea8-164">shell.Shell\_Application.NameSpace("...")</span></span>                                               |
| [<span data-ttu-id="cbea8-165">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="cbea8-165">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="cbea8-166">殼。Shell \_ 應用程式。命名空間 ( "..." ) 。Self 或 Folder. 專案或資料夾. ParseName</span><span class="sxs-lookup"><span data-stu-id="cbea8-166">shell.Shell\_Application.NameSpace("...").Self or Folder.Items.Item or Folder.ParseName</span></span> |
| [<span data-ttu-id="cbea8-167">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="cbea8-167">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="cbea8-168">資料夾。專案</span><span class="sxs-lookup"><span data-stu-id="cbea8-168">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="cbea8-169">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-169">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="cbea8-170">資料夾。專案</span><span class="sxs-lookup"><span data-stu-id="cbea8-170">Folder.Items</span></span>                                                                            |
| [<span data-ttu-id="cbea8-171">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="cbea8-171">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="cbea8-172">Shell. NameSpace ( "..." ) 。Self. () 的專案</span><span class="sxs-lookup"><span data-stu-id="cbea8-172">Shell.NameSpace("...").Self.Verbs.Item()</span></span>                                                |
| [<span data-ttu-id="cbea8-173">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="cbea8-173">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="cbea8-174">FolderItem，或 Shell. NameSpace ( "..." ) 。自我動詞</span><span class="sxs-lookup"><span data-stu-id="cbea8-174">FolderItem.Verbs or Shell.NameSpace("...").Self.Verbs</span></span>                                   |
| [<span data-ttu-id="cbea8-175">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-175">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="cbea8-176">殼。Shell \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="cbea8-176">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="cbea8-177">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-177">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="cbea8-178">Shell. NameSpace ( "..." ) 。GetLink 或 Shell. NameSpace ( "..." ) 。 () 專案。GetLink</span><span class="sxs-lookup"><span data-stu-id="cbea8-178">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="cbea8-179">**殼層**</span><span class="sxs-lookup"><span data-stu-id="cbea8-179">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="cbea8-180">殼。Shell \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="cbea8-180">shell.Shell\_Application</span></span>                                                                |
| [<span data-ttu-id="cbea8-181">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="cbea8-181">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="cbea8-182">Shell. NameSpace ( "..." ) 。Self 或 Shell. NameSpace ( "..." ) 。專案 () </span><span class="sxs-lookup"><span data-stu-id="cbea8-182">Shell.NameSpace("...").Self or Shell.NameSpace("...").Items()</span></span>                           |
| [<span data-ttu-id="cbea8-183">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="cbea8-183">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="cbea8-184">無法晚期繫結</span><span class="sxs-lookup"><span data-stu-id="cbea8-184">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="cbea8-185">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="cbea8-185">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="cbea8-186">無法晚期繫結</span><span class="sxs-lookup"><span data-stu-id="cbea8-186">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="cbea8-187">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="cbea8-187">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="cbea8-188">Shell. NameSpace ( "..." ) 。GetLink 或 Shell. NameSpace ( "..." ) 。 () 專案。GetLink</span><span class="sxs-lookup"><span data-stu-id="cbea8-188">Shell.NameSpace("...").Self.GetLink or Shell.NameSpace("...").Items().GetLink</span></span>           |
| [<span data-ttu-id="cbea8-189">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="cbea8-189">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="cbea8-190">無法晚期繫結</span><span class="sxs-lookup"><span data-stu-id="cbea8-190">Cannot late bind</span></span>                                                                        |
| [<span data-ttu-id="cbea8-191">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="cbea8-191">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="cbea8-192">殼。Shell \_ 視窗或 ShellWindows。 \_NewEnum</span><span class="sxs-lookup"><span data-stu-id="cbea8-192">shell.Shell\_Windows or ShellWindows.\_NewEnum</span></span>                                          |
| [<span data-ttu-id="cbea8-193">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="cbea8-193">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="cbea8-194">無法晚期繫結</span><span class="sxs-lookup"><span data-stu-id="cbea8-194">Cannot late bind</span></span>                                                                        |



 

### <a name="html-object-element"></a><span data-ttu-id="cbea8-195">HTML 物件元素</span><span class="sxs-lookup"><span data-stu-id="cbea8-195">HTML OBJECT Element</span></span>

<span data-ttu-id="cbea8-196">您也可以使用 [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) 元素，在 HTML 網頁上具現化 Shell 物件。</span><span class="sxs-lookup"><span data-stu-id="cbea8-196">You can also use the [**OBJECT**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) element to instantiate Shell objects on an HTML page.</span></span> <span data-ttu-id="cbea8-197">若要這樣做，請將 **物件** 專案的 **ID** 屬性設定為您將在腳本中使用的變數名稱，並使用其註冊的數位 (CLASSID) 來識別物件。</span><span class="sxs-lookup"><span data-stu-id="cbea8-197">To do this, set the **OBJECT** element's **ID** attribute to the variable name you will use in your scripts, and identify the object using its registered number (CLASSID).</span></span> <span data-ttu-id="cbea8-198">下列 HTML 會使用 **object** 元素來建立 [**ShellFolderItem**](shellfolderitem-object.md)物件的實例。</span><span class="sxs-lookup"><span data-stu-id="cbea8-198">The following HTML creates an instance of the [**ShellFolderItem**](shellfolderitem-object.md) object using the **OBJECT** element.</span></span>


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



<span data-ttu-id="cbea8-199">下表列出每個 Shell 物件及其各自的 CLASSID。</span><span class="sxs-lookup"><span data-stu-id="cbea8-199">The following table lists each Shell object and its respective CLASSID.</span></span>



|                                                         |                                      |
|---------------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="cbea8-200">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="cbea8-200">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)       | <span data-ttu-id="cbea8-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="cbea8-201">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="cbea8-202">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="cbea8-202">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)     | <span data-ttu-id="cbea8-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span><span class="sxs-lookup"><span data-stu-id="cbea8-203">7988B571-EC89-11cf-9C00-00AA00A14F56</span></span> |
| [<span data-ttu-id="cbea8-204">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="cbea8-204">**Folder**</span></span>](folder.md)                                | <span data-ttu-id="cbea8-205">BBCBDE60-C3FF-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="cbea8-205">BBCBDE60-C3FF-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="cbea8-206">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-206">**Folder2**</span></span>](folder2-object.md)                       | <span data-ttu-id="cbea8-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span><span class="sxs-lookup"><span data-stu-id="cbea8-207">f0d2d8ef-3890-11d2-bf8b-00c04fb93661</span></span> |
| [<span data-ttu-id="cbea8-208">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="cbea8-208">**FolderItem**</span></span>](folderitem.md)                        | <span data-ttu-id="cbea8-209">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="cbea8-209">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="cbea8-210">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="cbea8-210">**FolderItems**</span></span>](folderitems.md)                      | <span data-ttu-id="cbea8-211">744129E0-CBE5-11CE-8350-444553540000</span><span class="sxs-lookup"><span data-stu-id="cbea8-211">744129E0-CBE5-11CE-8350-444553540000</span></span> |
| [<span data-ttu-id="cbea8-212">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-212">**FolderItems2**</span></span>](folderitems2-object.md)             | <span data-ttu-id="cbea8-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span><span class="sxs-lookup"><span data-stu-id="cbea8-213">C94F0AD0-F363-11d2-A327-00C04F8EEC7F</span></span> |
| [<span data-ttu-id="cbea8-214">**FolderItemVerb**</span><span class="sxs-lookup"><span data-stu-id="cbea8-214">**FolderItemVerb**</span></span>](folderitemverb.md)                | <span data-ttu-id="cbea8-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="cbea8-215">08EC3E00-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="cbea8-216">**FolderItemVerbs**</span><span class="sxs-lookup"><span data-stu-id="cbea8-216">**FolderItemVerbs**</span></span>](folderitemverbs.md)              | <span data-ttu-id="cbea8-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span><span class="sxs-lookup"><span data-stu-id="cbea8-217">1F8352C0-50B0-11CF-960C-0080C7F4EE85</span></span> |
| [<span data-ttu-id="cbea8-218">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-218">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)       | <span data-ttu-id="cbea8-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span><span class="sxs-lookup"><span data-stu-id="cbea8-219">A4C6892C-3BA9-11d2-9DEA-00C04FB16162</span></span> |
| [<span data-ttu-id="cbea8-220">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="cbea8-220">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)       | <span data-ttu-id="cbea8-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span><span class="sxs-lookup"><span data-stu-id="cbea8-221">317EE249-F12E-11d2-B1E4-00C04F8EEB3E</span></span> |
| [<span data-ttu-id="cbea8-222">**殼層**</span><span class="sxs-lookup"><span data-stu-id="cbea8-222">**Shell**</span></span>](shell.md)                                  | <span data-ttu-id="cbea8-223">13709620-C279-11CE-A49E-444553540000</span><span class="sxs-lookup"><span data-stu-id="cbea8-223">13709620-C279-11CE-A49E-444553540000</span></span> |
| [<span data-ttu-id="cbea8-224">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="cbea8-224">**ShellFolderItem**</span></span>](shellfolderitem-object.md)       | <span data-ttu-id="cbea8-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span><span class="sxs-lookup"><span data-stu-id="cbea8-225">2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e</span></span> |
| [<span data-ttu-id="cbea8-226">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="cbea8-226">**ShellFolderView**</span></span>](shellfolderview.md)              | <span data-ttu-id="cbea8-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span><span class="sxs-lookup"><span data-stu-id="cbea8-227">62112AA1-EBE4-11cf-A5FB-0020AFE7292D</span></span> |
| [<span data-ttu-id="cbea8-228">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="cbea8-228">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)   | <span data-ttu-id="cbea8-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span><span class="sxs-lookup"><span data-stu-id="cbea8-229">4a3df050-23bd-11d2-939f-00a0c91eedba</span></span> |
| [<span data-ttu-id="cbea8-230">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="cbea8-230">**ShellLinkObject**</span></span>](shelllinkobject-object.md)       | <span data-ttu-id="cbea8-231">11219420-1768-11d1-95BE-00609797EA4F</span><span class="sxs-lookup"><span data-stu-id="cbea8-231">11219420-1768-11d1-95BE-00609797EA4F</span></span> |
| [<span data-ttu-id="cbea8-232">**ShellUIHelper**</span><span class="sxs-lookup"><span data-stu-id="cbea8-232">**ShellUIHelper**</span></span>](shelluihelper.md)                  | <span data-ttu-id="cbea8-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span><span class="sxs-lookup"><span data-stu-id="cbea8-233">64AB4BB7-111E-11D1-8F79-00C04FC2FBE1</span></span> |
| [<span data-ttu-id="cbea8-234">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="cbea8-234">**ShellWindows**</span></span>](shellwindows.md)                    | <span data-ttu-id="cbea8-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span><span class="sxs-lookup"><span data-stu-id="cbea8-235">9BA05972-F6A8-11CF-A442-00A0C90A8F39</span></span> |
| [<span data-ttu-id="cbea8-236">**WebViewFolderContents**</span><span class="sxs-lookup"><span data-stu-id="cbea8-236">**WebViewFolderContents**</span></span>](../lwef/webviewfoldercontents.md) | <span data-ttu-id="cbea8-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span><span class="sxs-lookup"><span data-stu-id="cbea8-237">1820FED0-473E-11D0-A96C-00C04FD705A2</span></span> |



 

## <a name="shell-object"></a><span data-ttu-id="cbea8-238">Shell 物件</span><span class="sxs-lookup"><span data-stu-id="cbea8-238">Shell Object</span></span>

<span data-ttu-id="cbea8-239">[**Shell**](shell.md)物件代表 shell 中的物件。</span><span class="sxs-lookup"><span data-stu-id="cbea8-239">The [**Shell**](shell.md) object represents the objects in the Shell.</span></span> <span data-ttu-id="cbea8-240">您可以使用 Shell 物件所公開的方法來：</span><span class="sxs-lookup"><span data-stu-id="cbea8-240">You can use the methods exposed by the Shell object to:</span></span>

-   <span data-ttu-id="cbea8-241">開啟、流覽和流覽資料夾。</span><span class="sxs-lookup"><span data-stu-id="cbea8-241">Open, explore, and browse for folders.</span></span>
-   <span data-ttu-id="cbea8-242">將開啟的視窗最小化、還原、重迭顯示或並排顯示。</span><span class="sxs-lookup"><span data-stu-id="cbea8-242">Minimize, restore, cascade, or tile open windows.</span></span>
-   <span data-ttu-id="cbea8-243">啟動主控台的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cbea8-243">Launch Control Panel applications.</span></span>
-   <span data-ttu-id="cbea8-244">顯示系統對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cbea8-244">Display system dialog boxes.</span></span>

<span data-ttu-id="cbea8-245">使用者可能最熟悉從 [ **開始** ] 功能表和工作列的快捷方式功能表存取的命令。</span><span class="sxs-lookup"><span data-stu-id="cbea8-245">Users are perhaps most familiar with the commands they access from the **Start** menu and the taskbar's shortcut menu.</span></span> <span data-ttu-id="cbea8-246">當使用者以滑鼠右鍵按一下工作列時，會出現工作列的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="cbea8-246">The taskbar's shortcut menu appears when users right-click the taskbar.</span></span> <span data-ttu-id="cbea8-247">下列 HTML 應用程式 (HTA) 會產生具有可執行許多 [**Shell**](shell.md) 物件方法之按鈕的起始頁。</span><span class="sxs-lookup"><span data-stu-id="cbea8-247">The following HTML Application (HTA) produces a start page with buttons that implement many of the [**Shell**](shell.md) object's methods.</span></span> <span data-ttu-id="cbea8-248">其中一些方法會在 [ **開始** ] 功能表和工作列的快捷方式功能表上執行功能。</span><span class="sxs-lookup"><span data-stu-id="cbea8-248">Some of these methods implement features on the **Start** menu and the taskbar's shortcut menu.</span></span>


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a><span data-ttu-id="cbea8-249">安全性</span><span class="sxs-lookup"><span data-stu-id="cbea8-249">Security</span></span>

<span data-ttu-id="cbea8-250">以應用程式來說，HTA 會在與網頁不同的安全性模型下執行。</span><span class="sxs-lookup"><span data-stu-id="cbea8-250">As an application, an HTA runs under a different security model than a webpage.</span></span> <span data-ttu-id="cbea8-251">若要與執行 Shell 物件功能的網頁互動，使用者必須啟用 [ **初始化] 和 [編寫 ActiveX 控制項未標示為安全的 ActiveX 控制項** ] 選項，以供他們在其中查看頁面的安全性區域使用。</span><span class="sxs-lookup"><span data-stu-id="cbea8-251">To interact with a webpage that implements the functionality of the Shell objects, users must enable the **Initialize and script ActiveX Controls not marked as safe** option for the security zone in which they are viewing the page.</span></span>

## <a name="folder-objects"></a><span data-ttu-id="cbea8-252">資料夾物件</span><span class="sxs-lookup"><span data-stu-id="cbea8-252">Folder Objects</span></span>

<span data-ttu-id="cbea8-253">[**Folder**](folder.md)物件代表 Shell 資料夾。</span><span class="sxs-lookup"><span data-stu-id="cbea8-253">The [**Folder**](folder.md) object represents a Shell folder.</span></span> <span data-ttu-id="cbea8-254">您可以使用資料夾物件所公開的方法來：</span><span class="sxs-lookup"><span data-stu-id="cbea8-254">You can use the methods exposed by the Folder object to:</span></span>

-   <span data-ttu-id="cbea8-255">取得資料夾的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cbea8-255">Get information about a folder.</span></span>
-   <span data-ttu-id="cbea8-256">建立子資料夾。</span><span class="sxs-lookup"><span data-stu-id="cbea8-256">Create subfolders.</span></span>
-   <span data-ttu-id="cbea8-257">將檔案物件複製並移至資料夾。</span><span class="sxs-lookup"><span data-stu-id="cbea8-257">Copy and move file objects into the folder.</span></span>

<span data-ttu-id="cbea8-258">[**FolderItem**](folderitem.md)物件代表 Shell 資料夾中的專案。</span><span class="sxs-lookup"><span data-stu-id="cbea8-258">The [**FolderItem**](folderitem.md) object represents an item in a Shell folder.</span></span> <span data-ttu-id="cbea8-259">它的屬性可讓您取得專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cbea8-259">Its properties enable you to retrieve information about the item.</span></span> <span data-ttu-id="cbea8-260">您可以使用此物件所公開的方法來執行專案的動詞，或取得專案之 [**FolderItemVerbs**](folderitemverbs.md) 物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cbea8-260">You can use the methods exposed by this object to run an item's verbs, or to retrieve information about an item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

<span data-ttu-id="cbea8-261">[**FolderItems**](folderitems.md)物件代表 Shell 資料夾中的專案集合。</span><span class="sxs-lookup"><span data-stu-id="cbea8-261">The [**FolderItems**](folderitems.md) object represents a collection of items in a Shell folder.</span></span> <span data-ttu-id="cbea8-262">它的方法和屬性可讓您取得集合的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cbea8-262">Its methods and properties enable you to retrieve information about the collection.</span></span>

<span data-ttu-id="cbea8-263">下列 Visual Basic 範例會顯示數個資料夾物件之間的關聯性，以及如何搭配使用它們。</span><span class="sxs-lookup"><span data-stu-id="cbea8-263">The following Visual Basic example shows the relationship between several of the folder objects and how they can be used together.</span></span> <span data-ttu-id="cbea8-264">當使用者按一下名為 **cmdGetPath** 的命令按鈕時，程式會顯示一個對話方塊，讓使用者從 **我的電腦** 選取資料夾，其中 SsfDRIVES 是 **我的電腦** 的 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)列舉值。</span><span class="sxs-lookup"><span data-stu-id="cbea8-264">When the user clicks the command button called **cmdGetPath**, the program displays a dialog box that enables the user to select a folder from **My Computer**, where ssfDRIVES is the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration value for **My Computer**.</span></span> <span data-ttu-id="cbea8-265">當使用者選擇資料夾時，該資料夾的路徑會顯示在名為 **txtPath** 的文字方塊中。</span><span class="sxs-lookup"><span data-stu-id="cbea8-265">When the user chooses a folder, the folder's path is displayed in the text box called **txtPath**.</span></span>


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



<span data-ttu-id="cbea8-266">在 VBScript 中，此函式會稍有不同，因為腳本中無法使用 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 的列舉值。</span><span class="sxs-lookup"><span data-stu-id="cbea8-266">In VBScript, this function is slightly different because the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) enumeration values are not available in script.</span></span> <span data-ttu-id="cbea8-267">下列範例顯示前一個範例的 VBScript 對等專案。</span><span class="sxs-lookup"><span data-stu-id="cbea8-267">The following example shows the VBScript equivalent of the previous example.</span></span>


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



<span data-ttu-id="cbea8-268">在下列 JScript 範例中（這是先前 VBScript 範例的直接轉譯），請注意如何使用空括弧 ' () ' 來叫用 [**專案**](folder-items.md) 和 [**專案**](folderitems-item.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="cbea8-268">In the following JScript example, which is a direct translation of the preceding VBScript example, note how the empty parentheses '()' are used to invoke the [**Items**](folder-items.md) and [**Item**](folderitems-item.md) methods.</span></span>


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
