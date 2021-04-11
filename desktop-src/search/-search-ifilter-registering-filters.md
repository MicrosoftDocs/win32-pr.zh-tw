---
description: 您必須註冊篩選處理常式。 您也可以透過登錄或使用 ILoadFilter 介面，找出給定副檔名的現有篩選處理常式。
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: 註冊篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112449"
---
# <a name="registering-filter-handlers"></a><span data-ttu-id="e4d74-104">註冊篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-104">Registering Filter Handlers</span></span>

<span data-ttu-id="e4d74-105">您必須註冊篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="e4d74-105">Your filter handler must be registered.</span></span> <span data-ttu-id="e4d74-106">您也可以透過登錄或使用 [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) 介面，找出給定副檔名的現有篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="e4d74-106">You can also locate an existing filter handler for a given file name extension either through the registry or by using the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface.</span></span>

<span data-ttu-id="e4d74-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="e4d74-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="e4d74-108">註冊 Windows Search 的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-108">Registering Filters Handlers for Windows Search</span></span>](#registering-filter-handlers)
  - [<span data-ttu-id="e4d74-109">註冊篩選處理常式的過時方法</span><span class="sxs-lookup"><span data-stu-id="e4d74-109">Obsolete Approach for Registering Filters Handlers</span></span>](#obsolete-approach-for-registering-filters-handlers)
- [<span data-ttu-id="e4d74-110">取代現有的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-110">Replacing Existing Filter Handlers</span></span>](#replacing-existing-filter-handlers)
- [<span data-ttu-id="e4d74-111">尋找指定副檔名的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-111">Finding a Filter Handler for a Given File Extension</span></span>](#finding-a-filter-handler-for-a-given-file-extension)
- [<span data-ttu-id="e4d74-112">其他資源</span><span class="sxs-lookup"><span data-stu-id="e4d74-112">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="e4d74-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4d74-113">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="e4d74-114">篩選處理常式是 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="e4d74-114">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

## <a name="registering-filters-handlers-for-windows-search"></a><span data-ttu-id="e4d74-115">註冊 Windows Search 的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-115">Registering Filters Handlers for Windows Search</span></span>

<span data-ttu-id="e4d74-116">下表列出您註冊新的通訊協定處理常式或尋找現有的通訊協定處理常式所需的 Guid。</span><span class="sxs-lookup"><span data-stu-id="e4d74-116">The GUIDs you need for registering a new protocol handler or to find an existing protocol handler are listed in the following table.</span></span>

| <span data-ttu-id="e4d74-117">GUID</span><span class="sxs-lookup"><span data-stu-id="e4d74-117">GUID</span></span>                                     | <span data-ttu-id="e4d74-118">已定義使用者或應用程式</span><span class="sxs-lookup"><span data-stu-id="e4d74-118">User or application defined</span></span> | <span data-ttu-id="e4d74-119">Description</span><span class="sxs-lookup"><span data-stu-id="e4d74-119">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d74-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span><span class="sxs-lookup"><span data-stu-id="e4d74-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span></span> | <span data-ttu-id="e4d74-121">應用程式</span><span class="sxs-lookup"><span data-stu-id="e4d74-121">Application</span></span>                 | <span data-ttu-id="e4d74-122">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)介面 GUID 是所有篩選處理常式的登錄機碼常數。</span><span class="sxs-lookup"><span data-stu-id="e4d74-122">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface GUID is a registry key constant for all filter handlers.</span></span> |
| <span data-ttu-id="e4d74-123">**{PersistentHandlerGUID}**</span><span class="sxs-lookup"><span data-stu-id="e4d74-123">**{PersistentHandlerGUID}**</span></span>              | <span data-ttu-id="e4d74-124">User</span><span class="sxs-lookup"><span data-stu-id="e4d74-124">User</span></span>                        | <span data-ttu-id="e4d74-125">這是持續性處理常式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e4d74-125">This is the GUID for the persistent handler.</span></span>                                                              |
| <span data-ttu-id="e4d74-126">**{FilterHandlerCLSID}**</span><span class="sxs-lookup"><span data-stu-id="e4d74-126">**{FilterHandlerCLSID}**</span></span>                 | <span data-ttu-id="e4d74-127">User</span><span class="sxs-lookup"><span data-stu-id="e4d74-127">User</span></span>                        | <span data-ttu-id="e4d74-128">這是篩選處理常式 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="e4d74-128">This is the class identifier (CLSID) for the filter handler.</span></span>                                              |
| <span data-ttu-id="e4d74-129">**{ApplicationGUID}**</span><span class="sxs-lookup"><span data-stu-id="e4d74-129">**{ApplicationGUID}**</span></span>                    | <span data-ttu-id="e4d74-130">User</span><span class="sxs-lookup"><span data-stu-id="e4d74-130">User</span></span>                        | <span data-ttu-id="e4d74-131">這是中繼 (匯總) GUID。</span><span class="sxs-lookup"><span data-stu-id="e4d74-131">This is an intermediate (aggregated) GUID.</span></span>                                                                |

<span data-ttu-id="e4d74-132">篩選處理常式必須在 HKEY \_ 本機電腦上註冊 \_ ，因為 SearchFilterHost.exe 正在系統帳戶下執行，因此無法存取 \_ 登入使用者的 HKEY 目前使用者的登錄機碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e4d74-132">Filter handlers must be registered in HKEY\_LOCAL\_MACHINE because SearchFilterHost.exe is running under the SYSTEM account and therefore cannot access registry keys for HKEY\_CURRENT\_USER for the logged-on user.</span></span> <span data-ttu-id="e4d74-133">此外，Users 群組必須擁有篩選處理常式 .dll 本身的讀取和執行存取權，因為 SearchFilterHost.exe 會移除所有的系統管理員許可權，而且只允許非系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="e4d74-133">In addition, the Users group must have read-and-execute access to the filter handler .dll itself because SearchFilterHost.exe removes all administrator rights and permits only non-administrator rights.</span></span> <span data-ttu-id="e4d74-134">因為預設 Visual Studio 專案位置是在目前使用者的目錄中，所以不會將讀取權限授與 Users 群組，所以您必須移動 .dll 或變更 Acl 以允許 SearchFilterHost.exe 存取。</span><span class="sxs-lookup"><span data-stu-id="e4d74-134">Because the default Visual Studio project location is in the current user's directory, and so does not give read permissions to the Users group, you must either move the .dll or change the ACLs to allow SearchFilterHost.exe access.</span></span>

<span data-ttu-id="e4d74-135">當您註冊新的篩選處理常式時，建議您使用描述性名稱，例如 HTML IFilter。</span><span class="sxs-lookup"><span data-stu-id="e4d74-135">When you register a new filter handler, we recommend that you use a descriptive name, for example, HTML IFilter.</span></span>

<span data-ttu-id="e4d74-136">**若要註冊新的篩選器處理常式：**</span><span class="sxs-lookup"><span data-stu-id="e4d74-136">**To register your new filter handler:**</span></span>

1. <span data-ttu-id="e4d74-137">指定將使用篩選處理常式的延伸模組和持續性處理常式 GUID：</span><span class="sxs-lookup"><span data-stu-id="e4d74-137">Specify the extension and persistent handler GUID that will use the filter handler:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. <span data-ttu-id="e4d74-138">使用下列索引鍵和值註冊您的篩選器處理常式：</span><span class="sxs-lookup"><span data-stu-id="e4d74-138">Register your filter handler with the following keys and values:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a><span data-ttu-id="e4d74-139">註冊篩選處理常式的過時方法</span><span class="sxs-lookup"><span data-stu-id="e4d74-139">Obsolete Approach for Registering Filters Handlers</span></span>

<span data-ttu-id="e4d74-140">不建議使用此方法。</span><span class="sxs-lookup"><span data-stu-id="e4d74-140">This approach is not recommended for use.</span></span> <span data-ttu-id="e4d74-141">您可以針對表示元件物件模型 (COM) 類別和/或副檔名的 CLSID 註冊篩選。</span><span class="sxs-lookup"><span data-stu-id="e4d74-141">Filters can be registered for a CLSID that represents a Component Object Model (COM) class, and/or for a file name extension.</span></span> <span data-ttu-id="e4d74-142">如果您需要註冊類別的篩選處理常式，以及類別內的副檔名不同的篩選處理常式，您可以註冊這兩個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="e4d74-142">You could register both filters if you need to register a filter handler for a class, and a different filter handler for a file name extension within the class.</span></span> <span data-ttu-id="e4d74-143">請注意，針對副檔名所註冊的篩選處理常式會優先于 CLSID 的篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="e4d74-143">Note that a filter handler registered for a file name extension takes precedence over a filter handler for a CLSID.</span></span>

<span data-ttu-id="e4d74-144">這些專案是標準的 OLE 登錄專案，最多可包含類別 **CLSID \\ {ApplicationGUID}** 的專案。</span><span class="sxs-lookup"><span data-stu-id="e4d74-144">These entries are standard OLE registry entries up to and including the entry for the class **CLSID\\{ApplicationGUID}**.</span></span> <span data-ttu-id="e4d74-145">DLL sample.dll 會針對 .txt 類別來執行物件行為。</span><span class="sxs-lookup"><span data-stu-id="e4d74-145">The DLL sample.dll implements running object behavior for the .txt class.</span></span> <span data-ttu-id="e4d74-146">請注意額外的專案 PersistentHandler。</span><span class="sxs-lookup"><span data-stu-id="e4d74-146">Note the extra entry, PersistentHandler.</span></span> <span data-ttu-id="e4d74-147">這個專案會指定負責代理範例類別之持續性物件要求的類別。</span><span class="sxs-lookup"><span data-stu-id="e4d74-147">This entry specifies the class that is responsible for brokering requests to the persistent objects of the sample class.</span></span> <span data-ttu-id="e4d74-148">**PersistentAddinsRegistered** 下的專案會識別為名為 **89BCB740-6119-101A-BCB7-00DD010655AF** (IID IFilter) 的介面負責的執行 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e4d74-148">The entry under **PersistentAddinsRegistered** identifies the implementation responsible for the interface named **89BCB740-6119-101A-BCB7-00DD010655AF**(IID\_IFilter).</span></span> <span data-ttu-id="e4d74-149">執行 **IID \_ IFilter** 的類別具有標準的 OLE 登錄專案。</span><span class="sxs-lookup"><span data-stu-id="e4d74-149">The class implementing **IID\_IFilter** has standard OLE registry entries.</span></span> <span data-ttu-id="e4d74-150">InprocServer32 DLL 是透過標準的 OLE 機制載入的。</span><span class="sxs-lookup"><span data-stu-id="e4d74-150">The InprocServer32 DLL is loaded through the standard OLE mechanism.</span></span>

<span data-ttu-id="e4d74-151">Windows Search 觀察為篩選處理常式指定的執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="e4d74-151">Windows Search observes the threading model specified for the filter handler.</span></span> <span data-ttu-id="e4d74-152">當執行緒模型設定為 [ **兩者**] 時，篩選處理常式必須為安全線程;否則，如果它不是安全線程，請指定 **公寓**。</span><span class="sxs-lookup"><span data-stu-id="e4d74-152">When the threading model is set to **Both**, the filter handler must be thread safe; otherwise, if it is not thread safe, specify **Apartment**.</span></span> <span data-ttu-id="e4d74-153">請注意，篩選處理常式應該一律為安全線程。</span><span class="sxs-lookup"><span data-stu-id="e4d74-153">Note that filter handlers should always be thread safe.</span></span>

<span data-ttu-id="e4d74-154">下列範例登錄專案適用于註冊類別和副檔名的篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="e4d74-154">The following example registry entries are for a filter handler registered for a class and file name extension.</span></span> <span data-ttu-id="e4d74-155">**{PersistentHandlerGUID}** 和 **{FilterHandlerCLSID}** 是用來做為變數，指出必須由篩選處理常式的建立者指定的值。</span><span class="sxs-lookup"><span data-stu-id="e4d74-155">**{PersistentHandlerGUID}** and **{FilterHandlerCLSID}** are used as variables indicating values that need to be specified by the creator of the filter handler.</span></span> <span data-ttu-id="e4d74-156">值的類型是 REG \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="e4d74-156">The values are of type REG\_SZ.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a><span data-ttu-id="e4d74-157">取代現有的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-157">Replacing Existing Filter Handlers</span></span>

<span data-ttu-id="e4d74-158">我們建議您不要將內建的篩選器處理常式取代為一般檔案類型，例如 .txt、.doc、.html、. url 等等，因為這樣做可能會對其他系統元件造成不良的影響。</span><span class="sxs-lookup"><span data-stu-id="e4d74-158">We recommend that you do not replace the built-in filter handlers for common file types such as .txt, .doc, .html, .url, and so forth, because doing so can have undesired effects on other system components.</span></span> <span data-ttu-id="e4d74-159">編制電子郵件訊息內文的索引取決於 .txt、.html 和 .rtf 篩選器處理常式，例如。</span><span class="sxs-lookup"><span data-stu-id="e4d74-159">Indexing email message bodies depends on the .txt, .html, and .rtf filter handlers, for example.</span></span>

<span data-ttu-id="e4d74-160">如果將檔案類型的新篩選處理常式安裝為現有篩選註冊的取代，則安裝程式應儲存目前的註冊，並在新的篩選器處理常式卸載時還原。</span><span class="sxs-lookup"><span data-stu-id="e4d74-160">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="e4d74-161">沒有任何機制可連結篩選。</span><span class="sxs-lookup"><span data-stu-id="e4d74-161">There is no mechanism to chain filters.</span></span> <span data-ttu-id="e4d74-162">因此，新的篩選處理常式會負責複寫舊篩選器的任何必要功能。</span><span class="sxs-lookup"><span data-stu-id="e4d74-162">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a><span data-ttu-id="e4d74-163">尋找指定副檔名的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-163">Finding a Filter Handler for a Given File Extension</span></span>

<span data-ttu-id="e4d74-164">您可以使用 [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) 介面來尋找給定副檔名的篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="e4d74-164">You can use the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface to find a filter handler for a given file name extension.</span></span> <span data-ttu-id="e4d74-165">下列範例登錄專案說明如何針對 HTML 檔案進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="e4d74-165">The following example registry entries illustrate how to do so for HTML files.</span></span> <span data-ttu-id="e4d74-166">在此範例中，會 nlhtml.dll HTML 檔案的篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="e4d74-166">In this example, the filter handler for HTML documents is nlhtml.dll.</span></span> <span data-ttu-id="e4d74-167">值的類型是 REG \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="e4d74-167">The values are of type REG\_SZ.</span></span>

<span data-ttu-id="e4d74-168">**若要尋找指定副檔名的篩選處理常式：**</span><span class="sxs-lookup"><span data-stu-id="e4d74-168">**To find the filter handler for a given file name extension:**</span></span>

1. <span data-ttu-id="e4d74-169">檢查已篩選之檔案類型的副檔名是否有在登錄專案 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別下註冊的持續性處理常式。</span><span class="sxs-lookup"><span data-stu-id="e4d74-169">Check whether the extension for the type of files that are filtered has a persistent handler registered under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.extension.</span></span> <span data-ttu-id="e4d74-170">如果是，請將此機碼視為 {PersistentHandlerGUID}。</span><span class="sxs-lookup"><span data-stu-id="e4d74-170">If so, let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. <span data-ttu-id="e4d74-171">如果沒有針對延伸模組註冊的持續性處理常式，請在登錄專案 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別下尋找與檔案類型相關聯的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="e4d74-171">If there is not a persistent handler registered for the extension, find the CLSID associated with the document type under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.</span></span> <span data-ttu-id="e4d74-172">讓此機碼為 {ApplicationGUID}。</span><span class="sxs-lookup"><span data-stu-id="e4d74-172">Let this key be {ApplicationGUID}.</span></span> <span data-ttu-id="e4d74-173">然後判斷是否已為 CLSID 註冊持續性處理常式：使用 {ApplicationGUID} 找出 \\ HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ clsid \\ {ApplicationGUID} 專案的持續性處理常式。</span><span class="sxs-lookup"><span data-stu-id="e4d74-173">Then determine whether a persistent handler is registered for the CLSID: using {ApplicationGUID} locate the persistent handler for the \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{ApplicationGUID} entry.</span></span> <span data-ttu-id="e4d74-174">讓此機碼為 {PersistentHandlerGUID}。</span><span class="sxs-lookup"><span data-stu-id="e4d74-174">Let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. <span data-ttu-id="e4d74-175">判斷持續性處理常式的 GUID：使用 {PersistentHandlerGUID} 尋找檔案類型的持續性處理常式 GUID。</span><span class="sxs-lookup"><span data-stu-id="e4d74-175">Determine the GUID of the persistent handler: using {PersistentHandlerGUID} find the persistent handler GUID for the document type.</span></span> <span data-ttu-id="e4d74-176">登錄專案 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID \\ {PersistentHandlerGUID} PersistentAddinsRegistered 89BCB740-6119-101A-BCB7-00DD010655AF 下的值會 \\ \\ 產生此檔案類型的持續性處理常式 GUID。</span><span class="sxs-lookup"><span data-stu-id="e4d74-176">The value under the registry entry HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{PersistentHandlerGUID}\\PersistentAddinsRegistered\\ 89BCB740-6119-101A-BCB7-00DD010655AF yields the persistent handler GUID for this document type.</span></span> <span data-ttu-id="e4d74-177">讓此機碼為 {FilterHandlerCLSID}。</span><span class="sxs-lookup"><span data-stu-id="e4d74-177">Let this key be {FilterHandlerCLSID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. <span data-ttu-id="e4d74-178">判斷篩選處理常式：使用上一個步驟中所決定的 {FilterHandlerCLSID} 在 [ \\ \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID \\ {FilterHandlerCLSID} \\ InprocServer32] 專案底下找到篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="e4d74-178">Determine the filter handler: using {FilterHandlerCLSID} that was determined in the previous step locate the filter handler under the entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{FilterHandlerCLSID}\\InprocServer32.</span></span> <span data-ttu-id="e4d74-179">在此範例中，使用的描述性篩選處理常式名稱是 HTML IFilter。</span><span class="sxs-lookup"><span data-stu-id="e4d74-179">In this example the descriptive filter handler name used is HTML IFilter.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a><span data-ttu-id="e4d74-180">其他資源</span><span class="sxs-lookup"><span data-stu-id="e4d74-180">Additional Resources</span></span>

- <span data-ttu-id="e4d74-181">[GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例會示範如何建立用來執行 **ifilter** 介面的 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)基礎類別。</span><span class="sxs-lookup"><span data-stu-id="e4d74-181">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) base class for implementing the **IFilter** interface.</span></span>
- <span data-ttu-id="e4d74-182">如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。</span><span class="sxs-lookup"><span data-stu-id="e4d74-182">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="e4d74-183">如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="e4d74-183">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="e4d74-184">若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e4d74-184">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4d74-185">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4d74-185">Related topics</span></span>

[<span data-ttu-id="e4d74-186">開發篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-186">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="e4d74-187">關於 Windows Search 中的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-187">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="e4d74-188">在 Windows Search 中建立篩選處理常式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="e4d74-188">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="e4d74-189">從篩選處理常式傳回屬性</span><span class="sxs-lookup"><span data-stu-id="e4d74-189">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="e4d74-190">Windows 隨附的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-190">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="e4d74-191">在 Windows Search 中執行篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-191">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="e4d74-192">測試篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="e4d74-192">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
