---
title: 取得和設定中繼資料和屬性
description: 取得和設定中繼資料和屬性
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Media 裝置管理員，屬性
- 裝置管理員，屬性
- 桌面應用程式，屬性
- 服務提供者，屬性
- 程式設計指南，屬性
- 屬性
- Windows Media 裝置管理員，中繼資料
- 裝置管理員，中繼資料
- 桌面應用程式，中繼資料
- 服務提供者，中繼資料
- 程式設計指南，中繼資料
- 中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840235"
---
# <a name="getting-and-setting-metadata-and-attributes"></a><span data-ttu-id="7f49e-115">取得和設定中繼資料和屬性</span><span class="sxs-lookup"><span data-stu-id="7f49e-115">Getting and Setting Metadata and Attributes</span></span>

<span data-ttu-id="7f49e-116">應用程式可以取得儲存體或裝置的兩種資訊：屬性和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7f49e-116">An application can get two kinds of information about a storage or device: attributes and metadata.</span></span> <span data-ttu-id="7f49e-117">屬性是較簡單的布林值，通常會描述檔案系統資訊，例如儲存體是否有子物件、是否可以重新命名、讀取或刪除等等。</span><span class="sxs-lookup"><span data-stu-id="7f49e-117">Attributes are simpler Boolean values that generally describe file system information, such as whether a storage has child objects, whether it can be renamed, read, or deleted, and so on.</span></span> <span data-ttu-id="7f49e-118">藉由呼叫 [**IWMDMStorage：： GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) 或 [**IWMDMStorage2：： GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2)，可將屬性視為旗標值來取出。</span><span class="sxs-lookup"><span data-stu-id="7f49e-118">Attributes are retrieved as flags values by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) or [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span></span> <span data-ttu-id="7f49e-119">藉由呼叫 [**IWMDMStorage3：： >setmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="7f49e-119">Attributes are set by calling [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span>

<span data-ttu-id="7f49e-120">應用程式也可以要求更複雜的資料 (數值、字串或) 為 *元* 資料的其他資料類型。</span><span class="sxs-lookup"><span data-stu-id="7f49e-120">An application can also request more complex data (numeric, string, or other data types) as *metadata*.</span></span> <span data-ttu-id="7f49e-121">中繼資料值是由唯一的字串名稱所識別。</span><span class="sxs-lookup"><span data-stu-id="7f49e-121">Metadata values are identified by unique string names.</span></span> <span data-ttu-id="7f49e-122">Windows Media 裝置管理員定義可用於要求值的字串常數清單;這些定義的值會列在 [中繼資料常數](metadata-constants.md)中。</span><span class="sxs-lookup"><span data-stu-id="7f49e-122">Windows Media Device Manager defines a list of string constants that can be used to request values; these defined values are listed in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="7f49e-123">服務提供者可以定義自己的常數，但呼叫的應用程式必須知道這些定義，才能要求或設定這些自訂中繼資料值。</span><span class="sxs-lookup"><span data-stu-id="7f49e-123">A service provider can define its own constants, but a calling application must be aware of these definitions in order to request or set these custom metadata values.</span></span> <span data-ttu-id="7f49e-124">應用程式會藉由呼叫 [**IWMDMStorage3：： GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) 或 [**IWMDMStorage4：： GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)來要求中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7f49e-124">The application requests metadata by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span>

<span data-ttu-id="7f49e-125">取得和設定中繼資料和屬性的一個重要層面，就是了解抓取值的來源。</span><span class="sxs-lookup"><span data-stu-id="7f49e-125">An important aspect of getting and setting metadata and attributes is understanding where the retrieved values come from.</span></span> <span data-ttu-id="7f49e-126">服務提供者或裝置可以從許多不同的位置取得這些值，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="7f49e-126">The service provider or the device can get these values from many different places, including the following:</span></span>

-   <span data-ttu-id="7f49e-127">從檔案標頭。</span><span class="sxs-lookup"><span data-stu-id="7f49e-127">From the file header.</span></span> <span data-ttu-id="7f49e-128">例如，在 ASF 檔案中，位元速率會儲存在檔案標頭中。</span><span class="sxs-lookup"><span data-stu-id="7f49e-128">For example, in an ASF file, the bit rate is stored in the file header.</span></span>
-   <span data-ttu-id="7f49e-129">從應用程式在呼叫方法時明確設定的值。</span><span class="sxs-lookup"><span data-stu-id="7f49e-129">From values set explicitly by the application when calling a method.</span></span> <span data-ttu-id="7f49e-130">這些值可能會儲存在服務提供者或裝置的外部中繼資料存放區中。</span><span class="sxs-lookup"><span data-stu-id="7f49e-130">These values may be saved in an external metadata store in the service provider or the device.</span></span> <span data-ttu-id="7f49e-131">當裝置中斷連線或關閉時，此存放區可能會或可能不會保存。</span><span class="sxs-lookup"><span data-stu-id="7f49e-131">This store may or may not persist when the device disconnects or turns off.</span></span> <span data-ttu-id="7f49e-132">例如，播放次數和使用者星級分級通常會儲存在電腦或裝置的外部商店中。</span><span class="sxs-lookup"><span data-stu-id="7f49e-132">For example, the play count and user star ratings are typically stored in external stores on the computer or device.</span></span>
-   <span data-ttu-id="7f49e-133">藉由檢查檔案系統所提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="7f49e-133">By examining information provided by the file system.</span></span> <span data-ttu-id="7f49e-134">例如，檔案是唯讀或資料夾是否有子系。</span><span class="sxs-lookup"><span data-stu-id="7f49e-134">For example, whether a file is read-only or whether a folder has children.</span></span>
-   <span data-ttu-id="7f49e-135">藉由開啟和剖析檔案資料。</span><span class="sxs-lookup"><span data-stu-id="7f49e-135">By opening and parsing the file data.</span></span>

<span data-ttu-id="7f49e-136">請務必瞭解，屬性可能會儲存在檔案標頭中的多個位置 (，也會儲存在本機存放區) 中，而且它可能會或可能無法編輯。</span><span class="sxs-lookup"><span data-stu-id="7f49e-136">It is important to realize that a property might be stored in more than one location (within the file header and also in a local store), and that it may or may not be editable.</span></span> <span data-ttu-id="7f49e-137">例如，變更檔案描述不一定是持續性;如果服務提供者將描述儲存在本機，則它不會保存在裝置上。</span><span class="sxs-lookup"><span data-stu-id="7f49e-137">For example, changing a file description may or may not be persistent; if the service provider stores the description locally, it will not persist on the device.</span></span> <span data-ttu-id="7f49e-138">同樣地，如果檔案描述是取自檔案標頭，則只有在服務提供者或裝置開啟並修改標頭資料時，才會有永久性的修改。</span><span class="sxs-lookup"><span data-stu-id="7f49e-138">Similarly, if the file description is taken from the file header, modifying this will only be persistent if the service provider or device opens and modifies the header data.</span></span> <span data-ttu-id="7f49e-139">大部分的應用程式會藉由變更所需的值來進行最佳嘗試，但不需依賴任何屬性來持續變更。</span><span class="sxs-lookup"><span data-stu-id="7f49e-139">Most applications make a best attempt by changing desired values, but do not depend on any properties to be persistently changed.</span></span>

<span data-ttu-id="7f49e-140">如需取得和設定值的詳細資訊，請參閱檔中的應用程式開發人員和服務提供者開發人員的適當章節。</span><span class="sxs-lookup"><span data-stu-id="7f49e-140">More information on getting and setting values is given in the appropriate sections for application developers and service provider developers later in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f49e-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f49e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f49e-142">**應用程式和服務提供者的一般工作**</span><span class="sxs-lookup"><span data-stu-id="7f49e-142">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




