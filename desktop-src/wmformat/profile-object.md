---
title: 設定檔物件
description: 設定檔物件
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- Windows Media 格式 SDK，設定檔物件
- Advanced Systems Format (ASF) 、profile 物件
- ASF (Advanced 系統格式) ，設定檔物件
- 物件，設定檔物件
- 設定檔，物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103841967"
---
# <a name="profile-object"></a><span data-ttu-id="39bab-108">設定檔物件</span><span class="sxs-lookup"><span data-stu-id="39bab-108">Profile Object</span></span>

<span data-ttu-id="39bab-109">設定檔物件會管理設定檔的設定。</span><span class="sxs-lookup"><span data-stu-id="39bab-109">A profile object manages the settings of a profile.</span></span> <span data-ttu-id="39bab-110">您可以為現有的設定檔資料建立設定檔物件，也可以建立空的，以便接收新資料。</span><span class="sxs-lookup"><span data-stu-id="39bab-110">Profile objects can be created for existing profile data or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="39bab-111">在載入檔案以進行讀取時，讀取器物件也會建立設定檔物件 (和同步讀取器物件) 。</span><span class="sxs-lookup"><span data-stu-id="39bab-111">A profile object is also created by the reader object (and the synchronous reader object) when a file is loaded for reading.</span></span> <span data-ttu-id="39bab-112">在此情況下，物件會填入儲存在檔案標頭中的設定檔資訊。</span><span class="sxs-lookup"><span data-stu-id="39bab-112">In this case the object is populated with the profile information stored in the header of the file.</span></span>

<span data-ttu-id="39bab-113">若要儲存設定檔物件的內容，您必須呼叫 [**IWMProfileManager：： SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile)。</span><span class="sxs-lookup"><span data-stu-id="39bab-113">To save the contents of a profile object, you must call [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span></span>

<span data-ttu-id="39bab-114">設定檔包含多個物件，可控制設定檔 (的各個層面，例如資料流程) 。</span><span class="sxs-lookup"><span data-stu-id="39bab-114">A profile contains multiple objects that control various aspects of the profile (such as streams).</span></span> <span data-ttu-id="39bab-115">所有這些物件都是設定檔物件的從屬物件。</span><span class="sxs-lookup"><span data-stu-id="39bab-115">All of these objects are subordinate to the profile object.</span></span> <span data-ttu-id="39bab-116">您不會像使用此 SDK 的主要物件一樣，建立具有建立功能的這些物件。</span><span class="sxs-lookup"><span data-stu-id="39bab-116">You do not create these objects with creation functions as you would with the major objects of this SDK.</span></span> <span data-ttu-id="39bab-117">但是，設定檔物件的介面會包含建立從屬物件的方法。</span><span class="sxs-lookup"><span data-stu-id="39bab-117">Instead, the interfaces of the profile object contain methods that create the subordinate objects.</span></span>

<span data-ttu-id="39bab-118">若要建立設定檔物件，請呼叫下列其中一種方法。</span><span class="sxs-lookup"><span data-stu-id="39bab-118">To create a profile object, call one of the following methods.</span></span>



| <span data-ttu-id="39bab-119">方法</span><span class="sxs-lookup"><span data-stu-id="39bab-119">Method</span></span>                                                                                | <span data-ttu-id="39bab-120">描述</span><span class="sxs-lookup"><span data-stu-id="39bab-120">Description</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39bab-121">**IWMProfileManager::CreateEmptyProfile**</span><span class="sxs-lookup"><span data-stu-id="39bab-121">**IWMProfileManager::CreateEmptyProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | <span data-ttu-id="39bab-122">建立沒有任何設定檔資料的設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="39bab-122">Creates a profile object without any profile data.</span></span>                                                                                                              |
| [<span data-ttu-id="39bab-123">**IWMProfileManager::LoadProfileByData**</span><span class="sxs-lookup"><span data-stu-id="39bab-123">**IWMProfileManager::LoadProfileByData**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | <span data-ttu-id="39bab-124">建立設定檔物件，其填入儲存為字串之設定檔中的資料。</span><span class="sxs-lookup"><span data-stu-id="39bab-124">Creates a profile object populated with data from a profile saved as a string.</span></span> <span data-ttu-id="39bab-125">這是使用自訂設定檔中的資料建立設定檔物件的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="39bab-125">This is the only way to create a profile object with data from a custom profile.</span></span> |
| [<span data-ttu-id="39bab-126">**IWMProfileManager::LoadProfileByID**</span><span class="sxs-lookup"><span data-stu-id="39bab-126">**IWMProfileManager::LoadProfileByID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | <span data-ttu-id="39bab-127">建立以系統設定檔中的資料填入的設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="39bab-127">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="39bab-128">使用 GUID 來識別所需的系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="39bab-128">Uses the GUID to identify the desired system profile.</span></span>                                       |
| [<span data-ttu-id="39bab-129">**IWMProfileManager::LoadSystemProfile**</span><span class="sxs-lookup"><span data-stu-id="39bab-129">**IWMProfileManager::LoadSystemProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | <span data-ttu-id="39bab-130">建立以系統設定檔中的資料填入的設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="39bab-130">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="39bab-131">使用設定檔索引來識別所需的系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="39bab-131">Uses the profile index to identify the desired system profile.</span></span>                              |



 

<span data-ttu-id="39bab-132">上表中的所有方法都會設定 **IWMProfile** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="39bab-132">All of the methods in the preceding table set a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="39bab-133">您可以藉由呼叫 **QueryInterface** 方法來取得設定檔物件的其他介面。</span><span class="sxs-lookup"><span data-stu-id="39bab-133">The other interfaces of the profile object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="39bab-134">每個設定檔物件都支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="39bab-134">The following interfaces are supported by every profile object.</span></span>



| <span data-ttu-id="39bab-135">介面</span><span class="sxs-lookup"><span data-stu-id="39bab-135">Interface</span></span>                                  | <span data-ttu-id="39bab-136">描述</span><span class="sxs-lookup"><span data-stu-id="39bab-136">Description</span></span>                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39bab-137">**IWMLanguageList**</span><span class="sxs-lookup"><span data-stu-id="39bab-137">**IWMLanguageList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | <span data-ttu-id="39bab-138">管理 ASF 檔案所支援的語言清單。</span><span class="sxs-lookup"><span data-stu-id="39bab-138">Manages a list of languages supported by an ASF file.</span></span>                                                                                             |
| [<span data-ttu-id="39bab-139">**IWMPacketSize**</span><span class="sxs-lookup"><span data-stu-id="39bab-139">**IWMPacketSize**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | <span data-ttu-id="39bab-140">控制檔案中封包的大小上限。</span><span class="sxs-lookup"><span data-stu-id="39bab-140">Controls the maximum size of packets in a file.</span></span>                                                                                                   |
| [<span data-ttu-id="39bab-141">**IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="39bab-141">**IWMPacketSize2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | <span data-ttu-id="39bab-142">控制檔案中封包的大小下限。</span><span class="sxs-lookup"><span data-stu-id="39bab-142">Controls the minimum size of packets in a file.</span></span> <span data-ttu-id="39bab-143">繼承 **IWMPacketSize** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="39bab-143">Inherits all of the methods of **IWMPacketSize**.</span></span>                                                 |
| [<span data-ttu-id="39bab-144">**IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="39bab-144">**IWMProfile**</span></span>](iwmprofile.md)           | <span data-ttu-id="39bab-145">控制設定檔中包含的基本設定和物件。</span><span class="sxs-lookup"><span data-stu-id="39bab-145">Controls the basic settings and objects included in a profile.</span></span>                                                                                    |
| [<span data-ttu-id="39bab-146">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="39bab-146">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | <span data-ttu-id="39bab-147">抓取與設定檔相關聯 (GUID) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="39bab-147">Retrieves the globally unique identifier (GUID) associated with the profile.</span></span> <span data-ttu-id="39bab-148">繼承 **IWMProfile** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="39bab-148">Inherits all of the methods of **IWMProfile**.</span></span>                       |
| [<span data-ttu-id="39bab-149">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="39bab-149">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | <span data-ttu-id="39bab-150">控制設定檔中的頻寬共用和串流優先順序資訊。</span><span class="sxs-lookup"><span data-stu-id="39bab-150">Controls bandwidth sharing and stream prioritization information in a profile.</span></span> <span data-ttu-id="39bab-151">繼承 **IWMProfile** 和 **IWMProfile2** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="39bab-151">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="39bab-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="39bab-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39bab-153">**物件**</span><span class="sxs-lookup"><span data-stu-id="39bab-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="39bab-154">**設定檔管理員物件**</span><span class="sxs-lookup"><span data-stu-id="39bab-154">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="39bab-155">**配置 檔**</span><span class="sxs-lookup"><span data-stu-id="39bab-155">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




