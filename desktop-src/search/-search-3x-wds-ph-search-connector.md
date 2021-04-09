---
description: Windows 檔案總管透過登錄機碼專案來控制通訊協定處理常式的搜尋連接器建立。 透過登錄，實施者和協力廠商可讓新的和舊版通訊協定處理常式參與 Windows 7 搜尋。
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: 建立通訊協定處理常式的搜尋連接器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112481"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a><span data-ttu-id="bd8fa-104">建立通訊協定處理常式的搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="bd8fa-104">Creating a Search Connector for a Protocol Handler</span></span>

<span data-ttu-id="bd8fa-105">Windows 檔案總管透過登錄機碼專案來控制通訊協定處理常式的搜尋連接器建立。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-105">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries.</span></span> <span data-ttu-id="bd8fa-106">透過登錄，實施者和協力廠商可讓新的和舊版通訊協定處理常式參與 Windows 7 搜尋。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-106">Through the registry both implementers and third parties can enable new and legacy protocol handlers to participate in Windows 7 Search.</span></span>

<span data-ttu-id="bd8fa-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="bd8fa-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="bd8fa-108">關於 Windows 7 中通訊協定處理常式的搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="bd8fa-108">About Search Connectors for Protocol Handlers in Windows 7</span></span>](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [<span data-ttu-id="bd8fa-109">啟用通訊協定處理常式以參與搜尋</span><span class="sxs-lookup"><span data-stu-id="bd8fa-109">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
    -   [<span data-ttu-id="bd8fa-110">停用通訊協定處理常式搜尋連接器建立</span><span class="sxs-lookup"><span data-stu-id="bd8fa-110">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
    -   [<span data-ttu-id="bd8fa-111">自訂通訊協定處理常式搜尋連接器的名稱、描述或 FolderType</span><span class="sxs-lookup"><span data-stu-id="bd8fa-111">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [<span data-ttu-id="bd8fa-112">使用登錄字串重新導向</span><span class="sxs-lookup"><span data-stu-id="bd8fa-112">Using Registry String Redirection</span></span>](#using-registry-string-redirection)
    -   [<span data-ttu-id="bd8fa-113">還原已刪除的通訊協定處理常式搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="bd8fa-113">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)
-   [<span data-ttu-id="bd8fa-114">其他資源</span><span class="sxs-lookup"><span data-stu-id="bd8fa-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="bd8fa-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd8fa-115">Related topics</span></span>](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a><span data-ttu-id="bd8fa-116">關於 Windows 7 中通訊協定處理常式的搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="bd8fa-116">About Search Connectors for Protocol Handlers in Windows 7</span></span>

<span data-ttu-id="bd8fa-117">在 Windows 7 中，搜尋 [ **開始** ] 功能表或 Windows 檔案總管只包含索引位置中的檔案，以及非檔案系統專案，例如遠端資料存放區或具有搜尋連接器的通訊協定處理常式專案。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-117">In Windows 7, searches from the **Start** menu or Windows Explorer include only files in indexed locations, and non-file system items such as remote data stores or protocol handler items that have a search connector.</span></span> <span data-ttu-id="bd8fa-118">除了在 [ **開始** ] 功能表和 Shell 搜尋範圍中包含通訊協定處理常式專案之外，搜尋連接器還可讓 [ **開始** ] 功能表在 [ **開始** ] 功能表結果中將通訊協定處理常式專案群組在一起，得到的好處是使用者可以按一下群組標頭，並只從通訊協定處理常式來查看結果。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-118">In addition to including the protocol handler items in the scope of **Start** menu and Shell searches, the search connector enables the **Start** menu to group protocol handler items together in **Start** menu results, with the resulting benefit that the user can click the group header and view results from only the protocol handler.</span></span> <span data-ttu-id="bd8fa-119">或者，使用者可以流覽至 [ **搜尋** ] 資料夾，開啟搜尋連接器檔案，然後執行僅包含與該搜尋連接器相關聯之特定通訊協定處理常式中專案的搜尋。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-119">Alternatively, the user can navigate to the **Searches** folder, open the search connector file, and perform a search that includes only items from the specific protocol handler associated with that search connector.</span></span>

<span data-ttu-id="bd8fa-120">當使用者第一次啟動註冊通訊協定處理常式的應用程式時，Windows 檔案總管會針對使用者 **搜尋** 資料夾中的通訊協定處理常式產生搜尋連接器檔案 (. searchConnector-ms) 。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-120">When a user first starts an application that registers a protocol handler, Windows Explorer generates a search connector file (.searchConnector-ms) for the protocol handler in the user's **Searches** folder.</span></span> <span data-ttu-id="bd8fa-121">具有通訊協定處理常式的應用程式可以選擇停用此行為，或自訂通訊協定處理常式搜尋連接器的名稱和描述。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-121">Applications with protocol handlers can choose to disable this behavior or customize the name and description of the protocol handler search connector.</span></span>

> [!Note]  
> <span data-ttu-id="bd8fa-122">使用者 **搜尋** 資料夾的位置是% userprofile% \\ 搜尋或 FOLDERID \_ SavedSearches。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-122">The location of the user's **Searches** folder is %userprofile%\\Searches, or FOLDERID\_SavedSearches.</span></span> <span data-ttu-id="bd8fa-123">FOLDERID SavedSearches 的 GUID \_ 是 {7d1d3a04-debb-4115-95cf-2f29da2920da}。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-123">The GUID for FOLDERID\_SavedSearches is {7d1d3a04-debb-4115-95cf-2f29da2920da}.</span></span>

 

<span data-ttu-id="bd8fa-124">Windows 檔案總管會透過下列各節所述的登錄機碼專案，控制通訊協定處理常式的搜尋連接器建立：</span><span class="sxs-lookup"><span data-stu-id="bd8fa-124">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries described in the following sections:</span></span>

-   [<span data-ttu-id="bd8fa-125">啟用通訊協定處理常式以參與搜尋</span><span class="sxs-lookup"><span data-stu-id="bd8fa-125">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
-   [<span data-ttu-id="bd8fa-126">停用通訊協定處理常式搜尋連接器建立</span><span class="sxs-lookup"><span data-stu-id="bd8fa-126">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
-   [<span data-ttu-id="bd8fa-127">自訂通訊協定處理常式搜尋連接器的名稱、描述或 FolderType</span><span class="sxs-lookup"><span data-stu-id="bd8fa-127">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [<span data-ttu-id="bd8fa-128">還原已刪除的通訊協定處理常式搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="bd8fa-128">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> <span data-ttu-id="bd8fa-129">沒有以程式設計方式為通訊協定處理常式建立搜尋連接器。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-129">There are no programmatic means to create a search connector for a protocol handler.</span></span> <span data-ttu-id="bd8fa-130">它們必須透過登錄設定。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-130">They must be configured through the registry.</span></span>

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a><span data-ttu-id="bd8fa-131">啟用通訊協定處理常式以參與搜尋</span><span class="sxs-lookup"><span data-stu-id="bd8fa-131">Enabling Protocol Handlers to Participate in Search</span></span>

<span data-ttu-id="bd8fa-132">下表列出登錄機碼及其可能的值。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-132">Registry keys and their possible values are outlined in the following table.</span></span> <span data-ttu-id="bd8fa-133">通訊協定處理常式可以填入部分或所有登錄機碼 <protocol> ，其中以其通訊協定的實際名稱（例如 MAPI、檔案或 csc）取代。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-133">A protocol handler can populate some or all of these registry keys where <protocol> is replaced with the actual name of its protocol, such as MAPI, file, or csc, for example.</span></span>



| <span data-ttu-id="bd8fa-134">登錄機碼</span><span class="sxs-lookup"><span data-stu-id="bd8fa-134">Registry key</span></span>                                                                                                                 | <span data-ttu-id="bd8fa-135">可能的值 (s) </span><span class="sxs-lookup"><span data-stu-id="bd8fa-135">Possible value(s)</span></span>                                                                                                                     | <span data-ttu-id="bd8fa-136">類型</span><span class="sxs-lookup"><span data-stu-id="bd8fa-136">Type</span></span>       | <span data-ttu-id="bd8fa-137">註解</span><span class="sxs-lookup"><span data-stu-id="bd8fa-137">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd8fa-138">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ 版本</span><span class="sxs-lookup"><span data-stu-id="bd8fa-138">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Version</span></span>                     | <span data-ttu-id="bd8fa-139">預設)  (不存在。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-139">Does not exist (default).</span></span> <span data-ttu-id="bd8fa-140">否則為1或更大。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-140">Otherwise it is 1 or greater.</span></span>                                                                               | <span data-ttu-id="bd8fa-141">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="bd8fa-141">REG\_DWORD</span></span> | <span data-ttu-id="bd8fa-142">此值可用來偵測已處理之搜尋根的位置範本註冊變更。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-142">This value is used to detect changes to the location template registrations for search roots that have already been processed.</span></span> <span data-ttu-id="bd8fa-143">如果不存在，請使用0做為預設值。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-143">If does not exist, use 0 as a default.</span></span> <span data-ttu-id="bd8fa-144">或者，將版本遞增以通知 Windows 檔案總管因為已安裝較新版本的通訊協定處理常式，所以應重新產生搜尋連接器。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-144">Alternatively, increment the version to inform Windows Explorer that the search connector should be regenerated because a newer version of the protocol handler has been installed.</span></span> |
| <span data-ttu-id="bd8fa-145">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ DoNotCreateSearchConnectors</span><span class="sxs-lookup"><span data-stu-id="bd8fa-145">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\DoNotCreateSearchConnectors</span></span> | <span data-ttu-id="bd8fa-146">預設)  (不存在。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-146">Does not exist (default).</span></span> <span data-ttu-id="bd8fa-147">否則設定為1。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-147">Otherwise set to 1.</span></span>                                                                                         | <span data-ttu-id="bd8fa-148">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="bd8fa-148">REG\_DWORD</span></span> | <span data-ttu-id="bd8fa-149">如果不存在，請在 [搜尋] 資料夾中建立 searchconnector （ms）檔案。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-149">If it does not exist, create a .searchconnector-ms file in the Searches folder.</span></span> <span data-ttu-id="bd8fa-150">如果是1，則標示為已處理且不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-150">If 1, mark as processed and do nothing.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="bd8fa-151">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ 預設 \\ 描述</span><span class="sxs-lookup"><span data-stu-id="bd8fa-151">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Description</span></span>        | <span data-ttu-id="bd8fa-152">可當地語系化的字串，其中包含搜尋連接器的描述。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-152">A localizable string containing the description of the search connector.</span></span>                                                              | <span data-ttu-id="bd8fa-153">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="bd8fa-153">REG\_SZ</span></span>    | <span data-ttu-id="bd8fa-154">選擇性。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-154">Optional.</span></span> <span data-ttu-id="bd8fa-155">它會用在 searchconnector-ms 檔案的 Description 元素中。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-155">It is used in the Description element of the .searchconnector-ms file.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="bd8fa-156">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ 預設 \\ 名稱</span><span class="sxs-lookup"><span data-stu-id="bd8fa-156">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Name</span></span>               | <span data-ttu-id="bd8fa-157">用來命名搜尋連接器的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-157">A localized string to name the search connector.</span></span> <span data-ttu-id="bd8fa-158">用來作為 searchconnector-ms 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-158">Used as the name of the .searchconnector-ms file.</span></span>                                    | <span data-ttu-id="bd8fa-159">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="bd8fa-159">REG\_SZ</span></span>    | <span data-ttu-id="bd8fa-160">每個位置都必須有唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-160">Each location must have a unique name.</span></span> <span data-ttu-id="bd8fa-161">如果沒有這個值，就會使用通訊協定處理常式 [IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 所提供的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-161">In the absence of this value, the display name provided by the protocol handler's [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) will be used.</span></span>                                                                                                                             |
| <span data-ttu-id="bd8fa-162">HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ 預設 \\ FolderType</span><span class="sxs-lookup"><span data-stu-id="bd8fa-162">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\FolderType</span></span>         | <span data-ttu-id="bd8fa-163">GUID，可識別要套用至搜尋連接器的 [FOLDERTYPEID](../shell/foldertypeid.md) 。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-163">A GUID identifying the [FOLDERTYPEID](../shell/foldertypeid.md) to apply to the search connector.</span></span> | <span data-ttu-id="bd8fa-164">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="bd8fa-164">REG\_SZ</span></span>    | <span data-ttu-id="bd8fa-165">選擇性。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-165">Optional.</span></span> <span data-ttu-id="bd8fa-166">用於 searchconnector-ms 檔案的 folderType 元素，以指出應該使用哪些範本來顯示結果。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-166">Used in the folderType element of the .searchconnector-ms file to indicate what templates should be used to display results.</span></span> <span data-ttu-id="bd8fa-167">例如，FOLDERTYPEID Documents 的 GUID 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-167">For example, the GUID value of FOLDERTYPEID\_Documents.</span></span>                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a><span data-ttu-id="bd8fa-168">停用通訊協定處理常式搜尋連接器建立</span><span class="sxs-lookup"><span data-stu-id="bd8fa-168">Disabling Protocol Handler Search Connector Creation</span></span>

<span data-ttu-id="bd8fa-169">如果您的應用程式透過通訊協定處理常式公開專案以用於應用程式本身，而您不想透過 [ **開始** ] 功能表中的 Shell (公開專案，並 Windows 檔案總管搜尋) ，則需要停用您的通訊協定處理常式建立搜尋連接器。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-169">If your application exposes items through a protocol handler for use in the application itself and you do not want to expose the items through the Shell (in **Start** menu and Windows Explorer searches), you need to disable the creation of a search connector for your protocol handler.</span></span>

<span data-ttu-id="bd8fa-170">若要停用搜尋連接器建立，請將 DoNotCreateSearchConnectors 設定為 0x00000001 (1) ，如下列登錄機碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-170">To disable search connector creation set DoNotCreateSearchConnectors to 0x00000001(1), as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

<span data-ttu-id="bd8fa-171">如果 DoNotCreateSearchConnectors 設定為1，則建議您在通訊協定處理常式公開的每個專案上公開 [OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) 屬性，並將這個屬性的值設為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-171">If DoNotCreateSearchConnectors is set to 1, then we recommend that you expose the [System.Shell.OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) property on each item exposed by the protocol handler, and set the value of this property to **TRUE**.</span></span> <span data-ttu-id="bd8fa-172">這樣做會讓通訊協定處理常式專案無法出現在 [開始 **] 功能表檔案** 群組之下。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-172">Doing so will prevent the protocol handler items from appearing under the **Start** menu **Files** group.</span></span>

<span data-ttu-id="bd8fa-173">如果 DoNotCreateSearchConnectors 存在且設定為零，則 Windows 檔案總管會為通訊協定處理常式建立搜尋連接器，並在 [ **開始** ] 功能表中傳回通訊協定處理常式專案，並 Windows 檔案總管搜尋。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-173">If DoNotCreateSearchConnectors is present and set to zero, then Windows Explorer will create a search connector for the protocol handler, and the protocol handler items will be returned in in **Start** menu and Windows Explorer searches.</span></span>

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a><span data-ttu-id="bd8fa-174">自訂通訊協定處理常式搜尋連接器的名稱、描述或 FolderType</span><span class="sxs-lookup"><span data-stu-id="bd8fa-174">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>

<span data-ttu-id="bd8fa-175">搜尋連接器名稱不僅會用來識別 [ **搜尋** ] 資料夾中的搜尋連接器，而是用來做為 [ **開始** ] 功能表搜尋結果的群組標頭。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-175">The search connector name is used not only to identify the search connector in the **Searches** folder, but as the group header for the results in **Start** menu searches.</span></span> <span data-ttu-id="bd8fa-176">因此，請務必提供搜尋連接器的描述性名稱。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-176">Hence, it is important to provide a descriptive name for the search connector.</span></span> <span data-ttu-id="bd8fa-177">如果登錄機碼中未提供名稱，根據預設，Windows 檔案總管會使用 [IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 為通訊協定處理常式的搜尋根目錄和空白描述所提供的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-177">If a name is not provided in the registry key, by default Windows Explorer uses the name provided by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) for the protocol handler's search root and blank description.</span></span> <span data-ttu-id="bd8fa-178">您可以透過登錄機碼專案覆寫預設名稱，而不需要重新命名 IShellFolder 介面。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-178">You can override the default name through a registry key entry without having to rename the IShellFolder Interface.</span></span> <span data-ttu-id="bd8fa-179">雖然它看起來不像搜尋連接器名稱，您也可以提供自己的描述來覆寫搜尋連接器的描述。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-179">Although it is not as visible as the search connector name, you can also override the description for the search connector by providing your own description.</span></span>

<span data-ttu-id="bd8fa-180">若要覆寫預設名稱或描述，請設定下列登錄範例所示的專案。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-180">To override the default name or description, set the entries as shown in the following registry example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

<span data-ttu-id="bd8fa-181">此外，FolderType 專案可以設定為其中一個 [FOLDERTYPEID](../shell/foldertypeid.md) guid。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-181">In addition, the FolderType entry can be set to one of the [FOLDERTYPEID](../shell/foldertypeid.md) GUIDs.</span></span> <span data-ttu-id="bd8fa-182">值應該是實際的 GUID，而不是其名稱。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-182">The value should be the actual GUID, and not its name.</span></span> <span data-ttu-id="bd8fa-183">例如，{94d6ddcc-4a68-4175-a374-bd584a510b78}，而不是 FOLDERTYPEID \_ 音樂。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-183">For example, {94d6ddcc-4a68-4175-a374-bd584a510b78} rather than FOLDERTYPEID\_Music.</span></span> <span data-ttu-id="bd8fa-184">FOLDERTYPEID 的 GUID 可以在 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)的 Shlguid .h 標頭檔中取得。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-184">The GUID for a FOLDERTYPEID can be obtained in the Shlguid.h header file in the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a><span data-ttu-id="bd8fa-185">使用登錄字串重新導向</span><span class="sxs-lookup"><span data-stu-id="bd8fa-185">Using Registry String Redirection</span></span>

<span data-ttu-id="bd8fa-186">您可以使用重新 [導向的字串](../intl/using-registry-string-redirection.md) ，以確保您為搜尋連接器提供的名稱可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-186">You can use a [redirected string](../intl/using-registry-string-redirection.md) to ensure that the name you provide for the search connector can be localized.</span></span> <span data-ttu-id="bd8fa-187">您可以為名稱和描述登錄機碼包含可當地語系化的字串，而不是在登錄中輸入實際的字串。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-187">You can include localizable strings for the name and description registry keys instead of entering the actual string into the registry.</span></span>

<span data-ttu-id="bd8fa-188">若要針對名稱或描述值包含可當地語系化的字串，請設定下列登錄機碼範例所示的值。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-188">To include a localizable string for the Name or Description values, set the value as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

<span data-ttu-id="bd8fa-189">可當地語系化的字串採用下列格式：</span><span class="sxs-lookup"><span data-stu-id="bd8fa-189">The localizable string takes the following format:</span></span>

-   <span data-ttu-id="bd8fa-190">@dllname.dll、-resourceID、where：</span><span class="sxs-lookup"><span data-stu-id="bd8fa-190">@dllname.dll,-resourceID, where:</span></span>
    -   <span data-ttu-id="bd8fa-191">@dllname.dll 這是包含字串資源之 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-191">@dllname.dll is the path to the DLL that contains the string resource</span></span>
    -   <span data-ttu-id="bd8fa-192">resourceID 是字串資源的整數資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bd8fa-192">resourceID is the integer resource ID of the string resource</span></span>

<span data-ttu-id="bd8fa-193">[SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring)函式中描述間接字串的格式，以及附加版本修飾詞的間接字串。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-193">The format for an indirect string, and an indirect string appended with a version modifier, is described in [SHLoadIndirectString Function](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span>

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a><span data-ttu-id="bd8fa-194">還原已刪除的通訊協定處理常式搜尋連接器</span><span class="sxs-lookup"><span data-stu-id="bd8fa-194">Restoring a Deleted Protocol Handler Search Connector</span></span>

<span data-ttu-id="bd8fa-195">由於搜尋連接器是使用者電腦上的檔案，因此可能會被錯誤地刪除。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-195">Because search connectors are files on the user's computer, they can be mistakenly deleted.</span></span> <span data-ttu-id="bd8fa-196">若要還原所有已刪除的通訊協定處理常式搜尋連接器，請還原預設程式庫。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-196">To restore all deleted protocol handler search connectors, restore the default libraries.</span></span> <span data-ttu-id="bd8fa-197">若要這麼做，請開啟 Windows 檔案總管，以滑鼠右鍵按一下 [連結 **庫** ] 資料夾，然後選取 [ **還原預設程式庫**]。</span><span class="sxs-lookup"><span data-stu-id="bd8fa-197">To so do, open Windows Explorer, right-click the **Libraries** folder, and then select **Restore Default Libraries**.</span></span>

![顯示 [還原預設程式庫] 功能表選項的螢幕擷取畫面](images/libraries.png)

## <a name="additional-resources"></a><span data-ttu-id="bd8fa-199">其他資源</span><span class="sxs-lookup"><span data-stu-id="bd8fa-199">Additional Resources</span></span>

-   [<span data-ttu-id="bd8fa-200">IShellItem：： GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="bd8fa-200">IShellItem::GetDisplayName</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [<span data-ttu-id="bd8fa-201">SIGDN \_ NORMALDISPLAY</span><span class="sxs-lookup"><span data-stu-id="bd8fa-201">SIGDN\_NORMALDISPLAY</span></span>](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a><span data-ttu-id="bd8fa-202">相關主題</span><span class="sxs-lookup"><span data-stu-id="bd8fa-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bd8fa-203">**概念**</span><span class="sxs-lookup"><span data-stu-id="bd8fa-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bd8fa-204">瞭解通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="bd8fa-204">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="bd8fa-205">開發通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="bd8fa-205">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="bd8fa-206">通知索引變更</span><span class="sxs-lookup"><span data-stu-id="bd8fa-206">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="bd8fa-207">新增圖示和快顯功能表</span><span class="sxs-lookup"><span data-stu-id="bd8fa-207">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="bd8fa-208">程式碼範例：通訊協定處理常式的 Shell 擴充功能</span><span class="sxs-lookup"><span data-stu-id="bd8fa-208">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="bd8fa-209">安裝和註冊通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="bd8fa-209">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="bd8fa-210">偵錯工具通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="bd8fa-210">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
