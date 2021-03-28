---
description: 本節說明 Windows Shell 結構。
title: Shell 結構
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 814ae153-39b3-49ee-9da1-efe7e649c73e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5bbda4cd81c3db2dff664b9d16d2db60aa8f12f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973773"
---
# <a name="shell-structures"></a><span data-ttu-id="d732f-103">Shell 結構</span><span class="sxs-lookup"><span data-stu-id="d732f-103">Shell Structures</span></span>

<span data-ttu-id="d732f-104">本節說明 Windows Shell 結構。</span><span class="sxs-lookup"><span data-stu-id="d732f-104">This section describes the Windows Shell Structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d732f-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="d732f-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d732f-106">主題</span><span class="sxs-lookup"><span data-stu-id="d732f-106">Topic</span></span></th>
<th><span data-ttu-id="d732f-107">描述</span><span class="sxs-lookup"><span data-stu-id="d732f-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d732f-108"><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenufilename"><strong>AASHELLMENUFILENAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-108"><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenufilename"><strong>AASHELLMENUFILENAME</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-109">變數大小的結構，包含功能表檔名稱的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-109">A variable-size structure that contains information about a menu file name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-110"><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>AASHELLMENUITEM</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-110"><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>AASHELLMENUITEM</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-111">包含功能表項目的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-111">Contains information about a menu item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-112"><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>APPBARDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-112"><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>APPBARDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-113">包含系統 appbar 訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-113">Contains information about a system appbar message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-114"><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>APPCATEGORYINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-114"><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>APPCATEGORYINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-115">提供在主控台中新增/移除程式的應用程式類別目錄資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-115">Provides application category information to Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="d732f-116"><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a>結構是用來建立應用程式發行者的完整類別清單。</span><span class="sxs-lookup"><span data-stu-id="d732f-116">The <a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a> structure is used create a complete list of categories for an application publisher.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-117"><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-117"><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-118">提供應用程式發行者提供的支援應用程式類別清單，以在主控台中新增/移除程式。</span><span class="sxs-lookup"><span data-stu-id="d732f-118">Provides a list of supported application categories from an application publisher to Add/Remove Programs in Control Panel.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-119"><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>APPINFODATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-119"><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>APPINFODATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-120">提供已發佈應用程式至 [新增/移除程式] 主控台公用程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-120">Provides information about a published application to the Add/Remove Programs Control Panel utility.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-121"><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>ASSOCIATIONELEMENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-121"><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>ASSOCIATIONELEMENT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-122">定義 <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a> 用來取得指定檔案關聯之 <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> 介面的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-122">Defines information used by <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a> to retrieve an <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> interface for a given file association.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-123"><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>BANDINFOSFB</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-123"><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>BANDINFOSFB</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-124">包含有關資料夾帶的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-124">Contains information about a folder band.</span></span> <span data-ttu-id="d732f-125">此結構會與 <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>IShellFolderBand：： GetBandInfoSFB</strong></a> 和 <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>IShellFolderBand：： SetBandInfoSFB</strong></a> 方法搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-125">This structure is used with the <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>IShellFolderBand::GetBandInfoSFB</strong></a> and <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>IShellFolderBand::SetBandInfoSFB</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-126"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>BANDSITEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-126"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>BANDSITEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-127">包含有關寬線網站的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-127">Contains information about a band site.</span></span> <span data-ttu-id="d732f-128">此結構會與 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>IBandSite：： GetBandSiteInfo</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>IBandSite：： SetBandSiteInfo</strong></a> 方法搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-128">This structure is used with the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>IBandSite::GetBandSiteInfo</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>IBandSite::SetBandSiteInfo</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-129"><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-129"><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-130">包含基類的受保護成員。</span><span class="sxs-lookup"><span data-stu-id="d732f-130">Contains protected members of the base class.</span></span> <span data-ttu-id="d732f-131"><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> 會定義瀏覽器狀態，並搭配 <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2：： GetBaseBrowserData</strong></a> 和 <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2：:P utbasebrowserdata</strong></a>使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-131"><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> defines the browser state and is used with <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2::GetBaseBrowserData</strong></a> and <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2::PutBaseBrowserData</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-132"><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>BORDERWIDTHS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-132"><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>BORDERWIDTHS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-133">定義框線矩形左上角和右下角的座標。</span><span class="sxs-lookup"><span data-stu-id="d732f-133">Defines the coordinates of the upper-left and lower-right corners of a border rectangle.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-134"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>BROWSEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-134"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>BROWSEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-135">包含 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a> 函式的參數，並接收使用者所選取之資料夾的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-135">Contains parameters for the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a> function and receives information about the folder selected by the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-136"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-136"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-137">包含類別目錄資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-137">Contains category information.</span></span> <span data-ttu-id="d732f-138">元件類別是邏輯相關元件物件模型的群組， (COM) 類別，可 (CATID) 共用通用分類識別碼。</span><span class="sxs-lookup"><span data-stu-id="d732f-138">A component category is a group of logically-related Component Object Model (COM) classes that share a common category identifier (CATID).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-139"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>CIDA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-139"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>CIDA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-140">搭配 <a href="clipboard.md">CFSTR_SHELLIDLIST</a> 剪貼簿格式使用，可將指標傳送至一個或多個 Shell 命名空間物件 (PIDL) 的專案識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="d732f-140">Used with the <a href="clipboard.md">CFSTR_SHELLIDLIST</a> clipboard format to transfer the pointer to an item identifier list (PIDL) of one or more Shell namespace objects.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-141"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-141"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-142">定義資料行資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-142">Defines column information.</span></span> <span data-ttu-id="d732f-143">供 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> 介面的成員使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-143">Used by members of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-144"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-144"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-145">包含 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>ICoNtextMenu：： InvokeCommand</strong></a> 用來叫用快捷方式功能表命令所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-145">Contains information needed by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu::InvokeCommand</strong></a> to invoke a shortcut menu command.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-146"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>CMINVOKECOMMANDINFOEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-146"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>CMINVOKECOMMANDINFOEX</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-147">包含快捷方式功能表命令的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-147">Contains extended information about a shortcut menu command.</span></span> <span data-ttu-id="d732f-148">此結構是 <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> 的延伸版本，可允許使用 Unicode 值。</span><span class="sxs-lookup"><span data-stu-id="d732f-148">This structure is an extended version of <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> that allows the use of Unicode values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-149"><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-149"><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-150">一般用來篩選元素。</span><span class="sxs-lookup"><span data-stu-id="d732f-150">Used generically to filter elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-151"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>元件</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-151"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>COMPONENT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-152">由 Windows 2000 用來保存元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-152">Used by Windows 2000 to hold information about a component.</span></span> <span data-ttu-id="d732f-153">此結構會取代 <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="d732f-153">This structure replaces the <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-154"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>COMPONENTSOPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-154"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>COMPONENTSOPT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-155">包含桌面專案選項。</span><span class="sxs-lookup"><span data-stu-id="d732f-155">Contains the desktop item options.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-156"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>COMPPOS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-156"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>COMPPOS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-157">保存元件的位置和大小的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-157">Holds information about a component's position and size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-158"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>COMPSTATEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-158"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>COMPSTATEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-159">由 Windows 2000 用來保存元件狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-159">Used by Windows 2000 to hold information about a component's state.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-160"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-160"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-161">定義衝突專案結構。</span><span class="sxs-lookup"><span data-stu-id="d732f-161">Defines conflict item structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-162"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-162"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-163">定義衝突結果資訊結構。</span><span class="sxs-lookup"><span data-stu-id="d732f-163">Defines conflict result information structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-164"><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>CPLINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-164"><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>CPLINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-165">包含主控台應用程式所支援之對話方塊的資源資訊和應用程式定義的值。</span><span class="sxs-lookup"><span data-stu-id="d732f-165">Contains resource information and an application-defined value for a dialog box supported by a Control Panel application.</span></span> <span data-ttu-id="d732f-166">主控台應用程式的 <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>CPlApplet</strong></a> 函式會將這項資訊傳回主控台，以回應 <a href="cpl-inquire.md"><strong>CPL_INQUIRE</strong></a> 訊息。</span><span class="sxs-lookup"><span data-stu-id="d732f-166">The <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>CPlApplet</strong></a> function of the Control Panel application returns this information to the Control Panel in response to a <a href="cpl-inquire.md"><strong>CPL_INQUIRE</strong></a> message.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-167"><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_credential_serialization"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-167"><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_credential_serialization"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-168">包含認證的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d732f-168">Contains details about a credential.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-169"><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-169"><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-170">描述認證中的單一欄位。</span><span class="sxs-lookup"><span data-stu-id="d732f-170">Describes a single field in a credential.</span></span> <span data-ttu-id="d732f-171">例如，字串或使用者映射。</span><span class="sxs-lookup"><span data-stu-id="d732f-171">For example, a string or a user image.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-172"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>CSFV</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-172"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>CSFV</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-173">搭配 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a> 函式使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-173">Used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-174"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-174"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-175">作為 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用之部分額外資料結構的標頭。</span><span class="sxs-lookup"><span data-stu-id="d732f-175">Serves as the header for some of the extra data structures used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-176"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-176"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-177">包含 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultCoNtextMenu</strong></a>所使用的內容功能表資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-177">Contains context menu information used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-178"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>DELEGATEITEMID</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-178"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>DELEGATEITEMID</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-179">由委派資料夾用來取代標準 <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="d732f-179">Used by delegate folders in place of a standard <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-180"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>DETAILSINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-180"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>DETAILSINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-181">包含 Shell 資料夾專案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-181">Contains detail information for a Shell folder item.</span></span> <span data-ttu-id="d732f-182">搭配 <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a> 通知使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-182">Used with the <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-183"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>DFMICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-183"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>DFMICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-184">包含 <a href="dfm-invokecommandex.md"><strong>DFM_INVOKECOMMANDEX</strong></a>所使用的其他引數。</span><span class="sxs-lookup"><span data-stu-id="d732f-184">Contains additional arguments used by <a href="dfm-invokecommandex.md"><strong>DFM_INVOKECOMMANDEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-185"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>DLLVERSIONINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-185"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>DLLVERSIONINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-186">接收 DLL 特定版本資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-186">Receives DLL-specific version information.</span></span> <span data-ttu-id="d732f-187">它會與 <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> 函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-187">It is used with the <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> function.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d732f-188">您可以使用 <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a> 結構來取代此結構。</span><span class="sxs-lookup"><span data-stu-id="d732f-188">In place of this structure, you can use the <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a> structure.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-189"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-189"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-190">接收 DLL 特定版本資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-190">Receives DLL-specific version information.</span></span> <span data-ttu-id="d732f-191">它會與 <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> 函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-191">It is used with the <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-192"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-192"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-193">描述放置物件的影像和伴隨的文字。</span><span class="sxs-lookup"><span data-stu-id="d732f-193">Describes the image and accompanying text for a drop object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-194"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>DROPFILES</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-194"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>DROPFILES</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-195">定義 <a href="clipboard.md">CF_HDROP</a> 剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="d732f-195">Defines the <a href="clipboard.md">CF_HDROP</a> clipboard format.</span></span> <span data-ttu-id="d732f-196">接下來的資料是以雙精度 null 結束的檔案名清單。</span><span class="sxs-lookup"><span data-stu-id="d732f-196">The data that follows is a double null-terminated list of file names.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-197"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-197"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-198">保存 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用的額外資料區塊。</span><span class="sxs-lookup"><span data-stu-id="d732f-198">Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span> <span data-ttu-id="d732f-199">它會保存連結的 Windows Installer 識別碼。</span><span class="sxs-lookup"><span data-stu-id="d732f-199">It holds the link's Windows Installer ID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-200"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-200"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-201">儲存 Shell 連結狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-201">Stores information about the Shell link state.</span></span> <span data-ttu-id="d732f-202">此結構會用於標記為 EXP_PROPERTYSTORAGE_SIG 的額外資料區段。</span><span class="sxs-lookup"><span data-stu-id="d732f-202">This structure is used for extra data sections that are tagged with EXP_PROPERTYSTORAGE_SIG.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-203"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-203"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-204">保存 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用的額外資料區塊。</span><span class="sxs-lookup"><span data-stu-id="d732f-204">Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span> <span data-ttu-id="d732f-205">它包含特殊的資料夾資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-205">It holds special folder information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-206"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-206"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-207">保存 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用的額外資料區塊。</span><span class="sxs-lookup"><span data-stu-id="d732f-207">Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span> <span data-ttu-id="d732f-208">它會保留圖示或目標的可展開環境字串。</span><span class="sxs-lookup"><span data-stu-id="d732f-208">It holds expandable environment strings for the icon or target.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-209"><a href="ext-button.md"><strong>EXT_BUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-209"><a href="ext-button.md"><strong>EXT_BUTTON</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-210">包含有關檔案管理員延伸模組 DLL 新增至 [檔案管理員] 工具列之按鈕的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-210">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-211"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>EXTRASEARCH</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-211"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>EXTRASEARCH</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-212">由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a> 列舉值物件用來傳回 Shell 資料夾物件所支援之搜尋物件的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-212">Used by an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a> enumerator object to return information on the search objects supported by a Shell Folder object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-213"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-213"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-214">包含 CFSTR_FILE_ATTRIBUTES_ARRAY 的剪貼簿格式定義。</span><span class="sxs-lookup"><span data-stu-id="d732f-214">Contains the clipboard format definition for CFSTR_FILE_ATTRIBUTES_ARRAY.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-215"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>FILEDESCRIPTOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-215"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>FILEDESCRIPTOR</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-216">描述在 Microsoft ActiveX <a href="dragdrop.md">拖放</a> 作業期間，透過剪貼簿所複製之檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="d732f-216">Describes the properties of a file that is being copied by means of the clipboard during a Microsoft ActiveX <a href="dragdrop.md">drag-and-drop</a> operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-217"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>FILEGROUPDESCRIPTOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-217"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>FILEGROUPDESCRIPTOR</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-218">定義 CF_FILEGROUPDESCRIPTOR 剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="d732f-218">Defines the CF_FILEGROUPDESCRIPTOR clipboard format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-219"><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-219"><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-220">包含 [active File Manager] 視窗中所選磁片磁碟機的相關資訊 ([目錄] 視窗或 [搜尋結果] 視窗) 。</span><span class="sxs-lookup"><span data-stu-id="d732f-220">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-221"><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-221"><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-222">在 [active 檔案管理員] 視窗中， ([目錄] 視窗或 [搜尋結果] 視窗) ，包含所選取檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-222">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-223"><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-223"><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-224">包含檔管理員用來加入功能表或工具列命令專案之說明字串的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-224">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-225"><a href="fms-load.md"><strong>FMS_LOAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-225"><a href="fms-load.md"><strong>FMS_LOAD</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-226">包含檔管理員用來新增由檔管理程式延伸模組 DLL 提供之自訂功能表的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-226">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="d732f-227">此結構也提供差異值，可供延伸模組 DLL 在檔案管理員載入功能表之後，用來操作自訂功能表。</span><span class="sxs-lookup"><span data-stu-id="d732f-227">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-228"><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-228"><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-229">包含要新增至 [檔案管理員] 工具列之自訂按鈕的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-229">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="d732f-230">這些按鈕是由檔案管理員延伸模組 DLL 提供。</span><span class="sxs-lookup"><span data-stu-id="d732f-230">The buttons are provided by a File Manager extension DLL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-231"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>FOLDERSETTINGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-231"><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>FOLDERSETTINGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-232">包含資料夾檢視資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-232">Contains folder view information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-233"><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>FVSHOWINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-233"><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>FVSHOWINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-234">包含檔案檢視器用來顯示檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-234">Contains information that the file viewer uses to display a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-235"><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-235"><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-236">包含已要求即時線上說明之專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-236">Contains information about an item for which context-sensitive Help has been requested.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-237"><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>HELPWININFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-237"><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>HELPWININFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-238">包含主要或次要說明視窗的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="d732f-238">Contains the size and position of either a primary or secondary Help window.</span></span> <span data-ttu-id="d732f-239">應用程式可以使用 HELP_SETWINPOS 值呼叫 <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a> 函數來設定這項資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-239">An application can set this information by calling the <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a> function with the HELP_SETWINPOS value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-240"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-240"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-241">由 Microsoft Internet Explorer 4.0 與 Microsoft Internet Explorer 4.01 用來保存元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-241">Used by Microsoft Internet Explorer 4.0 and Microsoft Internet Explorer 4.01 to hold information about a component.</span></span> <span data-ttu-id="d732f-242">在 Windows 2000 中，它會被 <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>元件</strong></a> 結構取代。</span><span class="sxs-lookup"><span data-stu-id="d732f-242">With Windows 2000, it is replaced by the <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>COMPONENT</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-243"><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-243"><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-244">包含專案識別碼的清單。</span><span class="sxs-lookup"><span data-stu-id="d732f-244">Contains a list of item identifiers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-245"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ITEMSPACING</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-245"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ITEMSPACING</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-246">儲存兩個可能大小的圖示間距尺寸，可供顯示：小型和大型。</span><span class="sxs-lookup"><span data-stu-id="d732f-246">Stores the dimensions of the two possible sizes of icon spacing that are available for display: small and large.</span></span> <span data-ttu-id="d732f-247">由 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>IShellFolderView：： GetItemSpacing</strong></a>使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-247">Used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>IShellFolderView::GetItemSpacing</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-248"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-248"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-249">定義已知資料夾的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-249">Defines the specifics of a known folder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-250"><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>LOGFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-250"><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>LOGFONT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-251">定義字型的屬性。</span><span class="sxs-lookup"><span data-stu-id="d732f-251">Defines the attributes of a font.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-252"><a href="mruinfo.md"><strong>MRUINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-252"><a href="mruinfo.md"><strong>MRUINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-253">包含定義最近使用的新 (MRU) 清單的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-253">Contains information that defines a new most recently used (MRU) list.</span></span> <span data-ttu-id="d732f-254">由 <a href="createmrulist.md"><strong>CreateMRUListW</strong></a>使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-254">Used by <a href="createmrulist.md"><strong>CreateMRUListW</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-255"><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>MULTIKEYHELP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-255"><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>MULTIKEYHELP</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-256">指定要搜尋的關鍵字，以及要在 Windows 說明中搜尋的關鍵字資料表。</span><span class="sxs-lookup"><span data-stu-id="d732f-256">Specifies a keyword to search for and the keyword table to be searched by Windows Help.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-257"><a href="/windows/win32/api/shellapi/ns-shellapi-nc_address"><strong>NC_ADDRESS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-257"><a href="/windows/win32/api/shellapi/ns-shellapi-nc_address"><strong>NC_ADDRESS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-258">包含描述網路位址的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-258">Contains information that describes a network address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-259"><a href="/windows/desktop/shell/hkey-type"><strong>NET_ADDRESS_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-259"><a href="/windows/desktop/shell/hkey-type"><strong>NET_ADDRESS_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-260">描述網路位址。</span><span class="sxs-lookup"><span data-stu-id="d732f-260">Describes a network address.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-261"><a href="/windows/win32/api/cpl/ns-cpl-newcplinfow"><strong>NEWCPLINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-261"><a href="/windows/win32/api/cpl/ns-cpl-newcplinfow"><strong>NEWCPLINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-262">包含主控台應用程式所支援之對話方塊的資源資訊和應用程式定義的值。</span><span class="sxs-lookup"><span data-stu-id="d732f-262">Contains resource information and an application-defined value for a dialog box supported by a Control Panel application.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-263"><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>NOTIFYICONDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-263"><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>NOTIFYICONDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-264">包含系統在通知區域中顯示通知所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-264">Contains information that the system needs to display notifications in the notification area.</span></span> <span data-ttu-id="d732f-265">由 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-265">Used by <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-266"><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>NOTIFYICONIDENTIFIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-266"><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>NOTIFYICONIDENTIFIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-267">包含 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a> 用來識別要取得周框矩形之圖示的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-267">Contains information used by <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a> to identify the icon for which to retrieve the bounding rectangle.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-268"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>NRESARRAY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-268"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>NRESARRAY</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-269">定義 CF_NETRESOURCE 剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="d732f-269">Defines the CF_NETRESOURCE clipboard format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-270"><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>NSTCCUSTOMDRAW</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-270"><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>NSTCCUSTOMDRAW</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-271"><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a>方法所使用的自訂繪圖結構。</span><span class="sxs-lookup"><span data-stu-id="d732f-271">Custom draw structure used by <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-272"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-272"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-273">保存 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用的額外資料區塊。</span><span class="sxs-lookup"><span data-stu-id="d732f-273">Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span> <span data-ttu-id="d732f-274">它會保存主控台屬性。</span><span class="sxs-lookup"><span data-stu-id="d732f-274">It holds console properties.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-275"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-275"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-276">保存 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>所使用的額外資料區塊。</span><span class="sxs-lookup"><span data-stu-id="d732f-276">Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.</span></span> <span data-ttu-id="d732f-277">它會保存主控台的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="d732f-277">It holds the console's code page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-278"><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-278"><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-279">識別印表機屬性頁中的特定屬性工作表，以及該屬性工作表是否應為強制回應。</span><span class="sxs-lookup"><span data-stu-id="d732f-279">Identifies a particular property sheet in a printer's property pages and whether that property sheet should be modal.</span></span> <span data-ttu-id="d732f-280">選擇性地搭配 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>SHInvokePrinterCommand</strong></a> 函式使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-280">Optionally used with the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>SHInvokePrinterCommand</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-281"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>OPENASINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-281"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>OPENASINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-282">儲存 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a> 函數的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-282">Stores information for the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-283"><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>重疊</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-283"><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>OVERLAPPED</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-284">包含用於非同步 (重迭) 輸入/輸出 (i/o) 的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-284">Contains information used in asynchronous (overlapped) input/output (I/O).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-285"><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>PARSEDURL</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-285"><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>PARSEDURL</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-286">由 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>ParseURL</strong></a> 函數用來傳回剖析的 URL。</span><span class="sxs-lookup"><span data-stu-id="d732f-286">Used by the <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>ParseURL</strong></a> function to return the parsed URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-287"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-287"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-288">指定資料夾快捷方式的目的檔案夾及其屬性。</span><span class="sxs-lookup"><span data-stu-id="d732f-288">Specifies a folder shortcut's target folder and its attributes.</span></span> <span data-ttu-id="d732f-289">此結構是由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3：： GetFolderTargetInfo</strong></a> 和 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3：： InitializeEx</strong></a>使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-289">This structure is used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3::GetFolderTargetInfo</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3::InitializeEx</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-290"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>PREVIEWHANDLERFRAMEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-290"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>PREVIEWHANDLERFRAMEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-291">快速鍵表格結構。</span><span class="sxs-lookup"><span data-stu-id="d732f-291">Accelerator table structure.</span></span> <span data-ttu-id="d732f-292">由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame：： GetWindowCoNtext</strong></a>使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-292">Used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame::GetWindowContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-293"><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>PROFILEINFO.TXT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-293"><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>PROFILEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-294">包含載入或卸載使用者設定檔時所使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-294">Contains information used when loading or unloading a user profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-295"><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-295"><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-296">提供有關應用程式發行者的已發行應用程式的資訊，以便在主控台中 <strong>新增/移除程式</strong> 。</span><span class="sxs-lookup"><span data-stu-id="d732f-296">Provides information about a published application from an application publisher to <strong>Add/Remove Programs</strong> in Control Panel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-297"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>QCMINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-297"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>QCMINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-298">包含將功能表項目合併到 Windows 檔案總管功能表的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-298">Contains information for merging menu items into Windows Explorer menus.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-299"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>QITAB</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-299"><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>QITAB</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-300">由 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>QISearch</strong></a> 函數用來描述單一介面。</span><span class="sxs-lookup"><span data-stu-id="d732f-300">Used by the <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>QISearch</strong></a> function to describe a single interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-301"><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-301"><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-302">代表序列化 <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> 結構之任意類型的記憶體範圍。</span><span class="sxs-lookup"><span data-stu-id="d732f-302">A range of memory of arbitrary type that represents a serialized <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> structure.</span></span> <span data-ttu-id="d732f-303">程式不應該檢查 <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a>的內容;相反地，它們應該使用 <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>StgSerializePropVariant</strong></a> 和 <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>StgDeserializePropVariant</strong></a> 函式來處理它。</span><span class="sxs-lookup"><span data-stu-id="d732f-303">Programs should not inspect the contents of a <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a>; instead, they should manipulate it with the <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>StgSerializePropVariant</strong></a> and <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>StgDeserializePropVariant</strong></a> functions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-304"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-304"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-305">此結構會與 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> 函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-305">This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-306"><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-306"><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-307">儲存專案的位置資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-307">Stores position information for an item.</span></span> <span data-ttu-id="d732f-308">搭配 message <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-308">Used with message <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-309"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-309"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-310">包含 HTML 說明檔的名稱和該檔案中的主題。</span><span class="sxs-lookup"><span data-stu-id="d732f-310">Contains the name of an HTML Help file and a topic in that file.</span></span> <span data-ttu-id="d732f-311">搭配 <a href="sfvm-gethelptopic.md"><strong>SFVM_GETHELPTOPIC</strong></a> 通知使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-311">Used with the <a href="sfvm-gethelptopic.md"><strong>SFVM_GETHELPTOPIC</strong></a> notification.</span></span> <span data-ttu-id="d732f-312">此結構需要 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="d732f-312">This structure requires Unicode strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-313"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-313"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-314">包含要加入至物件 <strong>屬性</strong> 表之頁面的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d732f-314">Contains the details of a page to be added to an object's <strong>Properties</strong> sheet.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-315"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>SHARDAPPIDINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-315"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>SHARDAPPIDINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-316">包含 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> 用來識別專案的資料（在此案例中為 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>），以及與其相關聯的處理常式。</span><span class="sxs-lookup"><span data-stu-id="d732f-316">Contains data used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> to identify both an item—in this case as an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>—and the process that it is associated with.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-317"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>SHARDAPPIDINFOIDLIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-317"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>SHARDAPPIDINFOIDLIST</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-318">包含 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> 用來識別專案的資料（在此案例中為絕對 PIDL），以及與它相關聯的處理常式。</span><span class="sxs-lookup"><span data-stu-id="d732f-318">Contains data used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> to identify both an item—in this case by an absolute PIDL—and the process that it is associated with.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-319"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>SHARDAPPIDINFOLINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-319"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>SHARDAPPIDINFOLINK</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-320">包含 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> 用來識別兩個專案的資料，在此案例中是透過 <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a>，以及與其相關聯的處理常式。</span><span class="sxs-lookup"><span data-stu-id="d732f-320">Contains data used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>SHAddToRecentDocs</strong></a> to identify both an item, in this case through an <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a>, and the process that it is associated with.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-321"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>SHChangeNotifyEntry</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-321"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>SHChangeNotifyEntry</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-322">包含和接收變更通知的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-322">Contains and receives information for change notifications.</span></span> <span data-ttu-id="d732f-323">此結構會搭配 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a> 函式和 <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> 通知一起使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-323">This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a> function and the <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-324"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-324"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-325">包含可識別特定檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-325">Contains information that identifies a particular file.</span></span> <span data-ttu-id="d732f-326"><a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider：： GetItemData</strong></a>會在要求特定檔案的資料時使用它。</span><span class="sxs-lookup"><span data-stu-id="d732f-326">It is used by <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider::GetItemData</strong></a> when requesting data for a particular file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-327"><a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-327"><a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-328">指定 Windows 檔案總管詳細資料檢視將顯示之資料行的 FMTID/PID 識別碼。</span><span class="sxs-lookup"><span data-stu-id="d732f-328">Specifies the FMTID/PID identifier of a column that will be displayed by the Windows Explorer Details view.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d732f-329">在 Windows Vista 中， <a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a> 被視為舊版的表單，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-329">As of Windows Vista, <a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a> is considered a legacy form and should not be used.</span></span> <span data-ttu-id="d732f-330">在其位置中，使用 <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> 結構。</span><span class="sxs-lookup"><span data-stu-id="d732f-330">In its place, use the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> structure.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-331"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>SHCOLUMNINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-331"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>SHCOLUMNINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-332">包含資料行屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-332">Contains information about the properties of a column.</span></span> <span data-ttu-id="d732f-333">它是由 <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>IColumnProvider：： GetColumnInfo</strong></a>所使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-333">It is used by <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>IColumnProvider::GetColumnInfo</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-334"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>SHCOLUMNINIT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-334"><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>SHCOLUMNINIT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-335">將初始化資訊傳遞給 <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>IColumnProvider：： Initialize</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="d732f-335">Passes initialization information to <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>IColumnProvider::Initialize</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-336"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>SHDESCRIPTIONID</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-336"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>SHDESCRIPTIONID</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-337">接收專案資料以回應 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a>的呼叫。</span><span class="sxs-lookup"><span data-stu-id="d732f-337">Receives item data in response to a call to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-338"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>SHDRAGIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-338"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>SHDRAGIMAGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-339">包含建立拖曳影像所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-339">Contains the information needed to create a drag image.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-340"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-340"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-341">定義 Shell 專案資源。</span><span class="sxs-lookup"><span data-stu-id="d732f-341">Defines Shell item resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-342"><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>SHELLDETAILS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-342"><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>SHELLDETAILS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-343">報告 Shell 資料夾中專案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-343">Reports detailed information on an item in a Shell folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-344"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>SHELLEXECUTEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-344"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>SHELLEXECUTEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-345">包含 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>所使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-345">Contains information used by <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-346"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>SHELLFLAGSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-346"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>SHELLFLAGSTATE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-347">包含一組表示目前 Shell 設定的旗標。</span><span class="sxs-lookup"><span data-stu-id="d732f-347">Contains a set of flags that indicate the current Shell settings.</span></span> <span data-ttu-id="d732f-348">此結構會與 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a> 函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-348">This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-349"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-349"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-350">包含 Shell 狀態的設定。</span><span class="sxs-lookup"><span data-stu-id="d732f-350">Contains settings for the Shell's state.</span></span> <span data-ttu-id="d732f-351">此結構會與 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> 函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-351">This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-352"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>SHFILEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-352"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>SHFILEINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-353">包含檔案物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-353">Contains information about a file object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-354"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>SHFILEOPSTRUCT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-354"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>SHFILEOPSTRUCT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-355">包含 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> 函數用來執行檔案作業的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-355">Contains information that the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> function uses to perform file operations.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d732f-356">從 Windows Vista 起，建議使用 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> 介面，而不是這個函式。</span><span class="sxs-lookup"><span data-stu-id="d732f-356">As of Windows Vista, the use of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> interface is recommended over this function.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-357"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>SHFOLDERCUSTOMSETTINGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-357"><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>SHFOLDERCUSTOMSETTINGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-358">保存自訂資料夾設定。</span><span class="sxs-lookup"><span data-stu-id="d732f-358">Holds custom folder settings.</span></span> <span data-ttu-id="d732f-359">此結構會與 <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>SHGetSetFolderCustomSettings</strong></a> 函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-359">This structure is used with the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>SHGetSetFolderCustomSettings</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-360"><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-360"><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-361">定義專案識別碼。</span><span class="sxs-lookup"><span data-stu-id="d732f-361">Defines an item identifier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-362"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>SHNAMEMAPPING</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-362"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>SHNAMEMAPPING</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-363">包含 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> 函式所移動、複製或重新命名之每個檔案的舊路徑名稱和新路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="d732f-363">Contains the old and new path names for each file that was moved, copied, or renamed by the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-364"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>SHQUERYRBINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-364"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>SHQUERYRBINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-365">包含 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a> 函數取出的大小和專案計數資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-365">Contains the size and item count information retrieved by the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-366"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>SHSTOCKICONINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-366"><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>SHSTOCKICONINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-367">接收用來取出股票殼圖示的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-367">Receives information used to retrieve a stock Shell icon.</span></span> <span data-ttu-id="d732f-368">此結構用於呼叫 <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a>中。</span><span class="sxs-lookup"><span data-stu-id="d732f-368">This structure is used in a call <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-369"><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>SLOWAPPINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-369"><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>SLOWAPPINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-370">提供在主控台中 <strong>新增/移除程式</strong> 的特殊應用程式資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-370">Provides specialized application information to <strong>Add/Remove Programs</strong> in Control Panel.</span></span> <span data-ttu-id="d732f-371">此結構不適用於已發佈的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d732f-371">This structure is not applicable to published applications.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-372"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>SMCSHCHANGENOTIFYSTRUCT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-372"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>SMCSHCHANGENOTIFYSTRUCT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-373">包含變更通知的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-373">Contains information about change notification.</span></span> <span data-ttu-id="d732f-374">它是由 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>IShellMenuCallback：： CallbackSM</strong></a>所使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-374">It is used by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>IShellMenuCallback::CallbackSM</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-375"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>SMDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-375"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>SMDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-376">包含來自功能表區的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-376">Contains information from a menu band.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-377"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>SMINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-377"><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>SMINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-378">包含來自功能表區之專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-378">Contains information about an item from a menu band.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-379"><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>SOFTDISTINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-379"><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>SOFTDISTINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-380">包含軟體更新的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-380">Contains information about a software update.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-381"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>SORTCOLUMN</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-381"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>SORTCOLUMN</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-382">儲存有關如何排序資料夾檢視中所顯示之資料行的資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-382">Stores information about how to sort a column that is displayed in the folder view.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-383"><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-383"><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-384">包含從 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> 介面方法傳回的字串。</span><span class="sxs-lookup"><span data-stu-id="d732f-384">Contains strings returned from the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> interface methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-385"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-385"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-386">保留 <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2：： CreateViewWindow2</strong></a> 方法的參數。</span><span class="sxs-lookup"><span data-stu-id="d732f-386">Holds the parameters for the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2::CreateViewWindow2</strong></a> method.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-387"><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-387"><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-388">定義排程同步處理的處理常式。</span><span class="sxs-lookup"><span data-stu-id="d732f-388">Defines a handler for a scheduled synchronization.</span></span> <span data-ttu-id="d732f-389">搭配 <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>ISyncSchedule：： AddItem</strong></a>使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-389">Used with <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>ISyncSchedule::AddItem</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-390"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-390"><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-391">描述衝突識別碼資訊結構。</span><span class="sxs-lookup"><span data-stu-id="d732f-391">Describes conflict ID information structure.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-392"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-392"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-393">提供在 <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>ISyncMgrSynchronize：： GetHandlerInfo</strong></a> 方法中使用之處理常式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-393">Provides information about the handler for use in the <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>ISyncMgrSynchronize::GetHandlerInfo</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-394"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-394"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-395">提供 <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> 介面所列舉之專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-395">Provides information about items being enumerated by the <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-396"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>SYNCMGRLOGERRORINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-396"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>SYNCMGRLOGERRORINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-397">提供在 <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback：： LogError</strong></a> 方法中使用的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-397">Provides error information for use in the <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback::LogError</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-398"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>SYNCMGRPROGRESSITEM</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-398"><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>SYNCMGRPROGRESSITEM</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-399">在進行同步處理時提供狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d732f-399">Provides status information while a synchronization is in progress.</span></span> <span data-ttu-id="d732f-400">此結構會與 <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>ISyncMgrSynchronizeCallback：:P rogress</strong></a> 方法搭配使用，並對應至單一同步處理專案。</span><span class="sxs-lookup"><span data-stu-id="d732f-400">This structure is used with the <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>ISyncMgrSynchronizeCallback::Progress</strong></a> method and corresponds to a single synchronization item.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-401"><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>TBINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-401"><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>TBINFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-402">搭配 <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> 通知使用，可指定要新增至工具列的按鈕數目，以及新增的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="d732f-402">Used with the <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> notification to specify the number of buttons to add to the toolbar, as well as how they're added.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-403"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-403"><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-404">由 <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> 介面的方法用來定義以視窗的縮圖標記法內嵌的工具列中使用的按鈕。</span><span class="sxs-lookup"><span data-stu-id="d732f-404">Used by methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>ITaskbarList3</strong></a> interface to define buttons used in a toolbar embedded in a window's thumbnail representation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-405"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>WALLPAPEROPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-405"><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>WALLPAPEROPT</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-406">包含壁紙顯示選項。</span><span class="sxs-lookup"><span data-stu-id="d732f-406">Contains the wallpaper display options.</span></span> <span data-ttu-id="d732f-407">搭配 <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> 介面的成員使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-407">Used with members of the <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-408"><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>WINDOWDATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-408"><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>WINDOWDATA</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-409">儲存視窗資料。</span><span class="sxs-lookup"><span data-stu-id="d732f-409">Stores window data.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-410"><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-410"><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-411">指定縮圖解壓縮的內容。</span><span class="sxs-lookup"><span data-stu-id="d732f-411">Specifies the context of a thumbnail extraction.</span></span> <span data-ttu-id="d732f-412">由 <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>IThumbnailSettings：： SetCoNtext</strong></a>使用。</span><span class="sxs-lookup"><span data-stu-id="d732f-412">Used by <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>IThumbnailSettings::SetContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d732f-413"><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-413"><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-414"><a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>IThumbnailCache：： GetThumbnail</strong></a>所使用的值，可指定用於解壓縮和顯示縮圖影像的選項。</span><span class="sxs-lookup"><span data-stu-id="d732f-414">Values used by <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>IThumbnailCache::GetThumbnail</strong></a> to specify options for the extraction and display of the thumbnail image.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d732f-415"><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a></span><span class="sxs-lookup"><span data-stu-id="d732f-415"><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a></span></span><br/></td>
<td><span data-ttu-id="d732f-416">包含系統縮圖快取中縮圖的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d732f-416">Contains a unique identifier for a thumbnail in the system thumbnail cache.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 
