---
title: 使用設定檔
description: 使用設定檔
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- Windows Media Format SDK，設定檔
- Windows Media Format SDK，IWMCodecInfo3 介面
- 設定檔，關於
- 設定檔，Windows Media Format SDK
- 設定檔，IWMCodecInfo3
- IWMCodecInfo3，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664bbafd6c628588aa3b45b0a62a216db7bd7749
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374446"
---
# <a name="working-with-profiles"></a><span data-ttu-id="90658-109">使用設定檔</span><span class="sxs-lookup"><span data-stu-id="90658-109">Working with Profiles</span></span>

<span data-ttu-id="90658-110">本節說明如何設計、建立和修改設定檔。</span><span class="sxs-lookup"><span data-stu-id="90658-110">This section describes how to design, create, and modify profiles.</span></span> <span data-ttu-id="90658-111">每個設定檔都會描述組成檔案的資料流程，以及彼此之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="90658-111">Each profile describes the streams that will make up a file and their relationships with each other.</span></span> <span data-ttu-id="90658-112">設定檔物件包含每個資料流程的資料流程設定資訊、無法同時傳遞的資料流程的相互排除資訊、頻寬共用資訊，以及串流優先順序資訊。</span><span class="sxs-lookup"><span data-stu-id="90658-112">A profile object contains stream configuration information for each stream, mutual exclusion information for streams that cannot be delivered simultaneously, bandwidth sharing information, and stream prioritization information.</span></span>

<span data-ttu-id="90658-113">設定檔的主要用途是將資料流程設定資訊提供給寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="90658-113">The main purpose of profiles is to provide stream configuration information to the writer object.</span></span> <span data-ttu-id="90658-114">寫入器會使用設定檔中的資訊，與編解碼器進行協調以壓縮輸入。</span><span class="sxs-lookup"><span data-stu-id="90658-114">The writer uses the information in a profile to coordinate with the codecs the process of compressing inputs.</span></span> <span data-ttu-id="90658-115">當您設定壓縮的媒體資料流程時，您會指定用來壓縮資料的編解碼器，以及編解碼器使用的設定。</span><span class="sxs-lookup"><span data-stu-id="90658-115">When you configure a compressed media stream, you specify the codec used to compress the data and the settings the codec uses.</span></span> <span data-ttu-id="90658-116">您也可以建立未壓縮資料流程的設定檔。</span><span class="sxs-lookup"><span data-stu-id="90658-116">You can also create profiles for uncompressed streams.</span></span> <span data-ttu-id="90658-117">支援數個未壓縮的資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="90658-117">Several uncompressed stream types are supported.</span></span> <span data-ttu-id="90658-118">雖然它們不需要編解碼器，但這些類型對串流設定有自己的需求。</span><span class="sxs-lookup"><span data-stu-id="90658-118">Even though they do not require a codec, these types have their own requirements for stream configuration.</span></span> <span data-ttu-id="90658-119">如需詳細資訊，請參閱設定 [資料流程](configuring-streams.md) 和 [使用未壓縮的音訊和影片串流](using-uncompressed-audio-and-video-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="90658-119">For more information, see [Configuring Streams](configuring-streams.md) and [Using Uncompressed Audio and Video Streams](using-uncompressed-audio-and-video-streams.md).</span></span>

<span data-ttu-id="90658-120">使用其中一個 Windows Media 編解碼器的資料流程設定資訊，必須使用 [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) 介面的方法，從編解碼器取得。</span><span class="sxs-lookup"><span data-stu-id="90658-120">Stream configuration information for a stream using one of the Windows Media codecs must be obtained from the codec by using the methods of the [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) interface.</span></span> <span data-ttu-id="90658-121">針對視頻編解碼器，使用串流格式的程式與音訊編解碼器的程式不同，但在這兩種情況下，您都必須從編解碼器取得格式開始。</span><span class="sxs-lookup"><span data-stu-id="90658-121">The procedure for using stream formats is different for video codecs than it is for audio codecs, but in both cases you must begin by obtaining the format from the codec.</span></span> <span data-ttu-id="90658-122">您永遠不應該嘗試使用其中一種 Windows Media 編解碼器來手動設定串流，因為設定檔中的小錯誤可能會對 ASF 檔案造成深遠的影響。</span><span class="sxs-lookup"><span data-stu-id="90658-122">You should never try to manually configure a stream using one of the Windows Media codecs, because small errors in the profile can have a profound effect on the ASF file.</span></span>

<span data-ttu-id="90658-123">建立及/或修改設定檔的基本步驟如下：</span><span class="sxs-lookup"><span data-stu-id="90658-123">The basic steps in creating and/or modifying profiles are:</span></span>

1.  <span data-ttu-id="90658-124">建立空的設定檔，或載入現有的設定檔以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="90658-124">Create an empty profile, or load an existing profile to edit.</span></span>
2.  <span data-ttu-id="90658-125">若有需要，請根據從將用來編碼串流的編解碼器所支援的設定檔資料，設定每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="90658-125">Configure each of the streams, if required, based on supported profile data retrieved from the codec that will be used to encode the stream.</span></span>
3.  <span data-ttu-id="90658-126">如有需要，請設定相互排除。</span><span class="sxs-lookup"><span data-stu-id="90658-126">Configure mutual exclusion, if needed.</span></span>
4.  <span data-ttu-id="90658-127">視需要設定頻寬共用。</span><span class="sxs-lookup"><span data-stu-id="90658-127">Configure bandwidth sharing, if needed.</span></span>
5.  <span data-ttu-id="90658-128">在檔案中設定資料流程的優先順序（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="90658-128">Set the priority of the streams in the file, if required.</span></span>

<span data-ttu-id="90658-129">下列各節說明建立和編輯設定檔的程式。</span><span class="sxs-lookup"><span data-stu-id="90658-129">The following sections explain the process of creating and editing profiles.</span></span>



| <span data-ttu-id="90658-130">區段</span><span class="sxs-lookup"><span data-stu-id="90658-130">Section</span></span>                                                        | <span data-ttu-id="90658-131">描述</span><span class="sxs-lookup"><span data-stu-id="90658-131">Description</span></span>                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90658-132">設計設定檔</span><span class="sxs-lookup"><span data-stu-id="90658-132">Designing Profiles</span></span>](designing-profiles.md)                   | <span data-ttu-id="90658-133">說明如何設計設定檔。</span><span class="sxs-lookup"><span data-stu-id="90658-133">Describes how to design a profile.</span></span>                                                                 |
| [<span data-ttu-id="90658-134">建立設定檔</span><span class="sxs-lookup"><span data-stu-id="90658-134">Creating Profiles</span></span>](creating-profiles.md)                     | <span data-ttu-id="90658-135">說明如何建立空白的設定檔。</span><span class="sxs-lookup"><span data-stu-id="90658-135">Describes how to create an empty profile.</span></span>                                                          |
| [<span data-ttu-id="90658-136">設定資料流程</span><span class="sxs-lookup"><span data-stu-id="90658-136">Configuring Streams</span></span>](configuring-streams.md)                 | <span data-ttu-id="90658-137">描述如何設定資料流程，並將它們包含在設定檔中。</span><span class="sxs-lookup"><span data-stu-id="90658-137">Describes how to configure streams and include them in a profile.</span></span>                                  |
| [<span data-ttu-id="90658-138">使用相互排除</span><span class="sxs-lookup"><span data-stu-id="90658-138">Using Mutual Exclusion</span></span>](using-mutual-exclusion.md)           | <span data-ttu-id="90658-139">描述如何建立相互排除物件，並將它們包含在設定檔中。</span><span class="sxs-lookup"><span data-stu-id="90658-139">Describes how to create mutual exclusion objects and include them in a profile.</span></span>                    |
| [<span data-ttu-id="90658-140">使用頻寬共用</span><span class="sxs-lookup"><span data-stu-id="90658-140">Using Bandwidth Sharing</span></span>](using-bandwidth-sharing.md)         | <span data-ttu-id="90658-141">說明如何使用設定檔中的頻寬共用。</span><span class="sxs-lookup"><span data-stu-id="90658-141">Describes how to use bandwidth sharing in a profile.</span></span>                                               |
| [<span data-ttu-id="90658-142">使用資料流程優先順序</span><span class="sxs-lookup"><span data-stu-id="90658-142">Using Stream Prioritization</span></span>](using-stream-prioritization.md) | <span data-ttu-id="90658-143">描述如何在設定檔中使用資料流程優先權。</span><span class="sxs-lookup"><span data-stu-id="90658-143">Describes how to use stream prioritization in a profile.</span></span>                                           |
| [<span data-ttu-id="90658-144">正在儲存設定檔</span><span class="sxs-lookup"><span data-stu-id="90658-144">Saving Profiles</span></span>](saving-profiles.md)                         | <span data-ttu-id="90658-145">說明如何將自訂設定檔儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="90658-145">Describes how to save your custom profiles to a file.</span></span>                                              |
| [<span data-ttu-id="90658-146">使用系統設定檔</span><span class="sxs-lookup"><span data-stu-id="90658-146">Using System Profiles</span></span>](using-system-profiles.md)             | <span data-ttu-id="90658-147">描述如何使用系統設定檔，以節省建立設定檔的時間和精力。</span><span class="sxs-lookup"><span data-stu-id="90658-147">Describes how to work with system profiles to save time and effort in creating profiles.</span></span>           |
| [<span data-ttu-id="90658-148">管理封包大小</span><span class="sxs-lookup"><span data-stu-id="90658-148">Managing Packet Size</span></span>](managing-packet-size.md)               | <span data-ttu-id="90658-149">討論如何在使用您的設定檔所建立的檔案資料流程中控制封包大小。</span><span class="sxs-lookup"><span data-stu-id="90658-149">Discusses how to control the size of packets in the data streams of files made using your profile.</span></span> |



 

<span data-ttu-id="90658-150">**注意** 舊版 Windows Media 格式 SDK 的使用者可能習慣使用系統設定檔，而不需要修改來建立檔案。</span><span class="sxs-lookup"><span data-stu-id="90658-150">**Note** Users of previous versions of the Windows Media Format SDK may be accustomed to using system profiles without modification to create their files.</span></span> <span data-ttu-id="90658-151">Windows Media Format 9 系列 SDK 或更新版本不包含任何使用 Windows Media 9 系列或更新版本編解碼器的新系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="90658-151">The Windows Media Format 9 Series SDK or later does not include any new system profiles that use the Windows Media 9 Series or later codecs.</span></span> <span data-ttu-id="90658-152">這是因為必須有越來越多的設定檔，才能涵蓋編解碼器現在提供的各種功能。</span><span class="sxs-lookup"><span data-stu-id="90658-152">This is because of the increasing number of profiles that would be needed to cover the various features now offered by the codecs.</span></span> <span data-ttu-id="90658-153">您仍然可以使用第8版系統設定檔作為設定檔的起點。</span><span class="sxs-lookup"><span data-stu-id="90658-153">You can still use the version 8 system profiles as a starting place for your profiles.</span></span> <span data-ttu-id="90658-154">如需詳細資訊，請參閱 [使用系統設定檔](using-system-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="90658-154">For more information see [Using System Profiles](using-system-profiles.md).</span></span> <span data-ttu-id="90658-155">如需將設定檔的目標設為特定傳遞裝置之新機制的相關資訊，請參閱 [使用裝置一致性範本](working-with-device-conformance-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="90658-155">For information about the new mechanism for targeting profiles to specific delivery devices, see [Working with Device Conformance Templates](working-with-device-conformance-templates.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90658-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="90658-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90658-157">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="90658-157">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="90658-158">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="90658-158">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




