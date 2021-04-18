---
title: IWMProfile 介面
description: IWMProfile 介面是設定檔物件的主要介面。
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- IWMProfile 介面 windows 媒體格式
- IWMProfile 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "106966069"
---
# <a name="iwmprofile-interface"></a><span data-ttu-id="28cc1-105">IWMProfile 介面</span><span class="sxs-lookup"><span data-stu-id="28cc1-105">IWMProfile interface</span></span>

<span data-ttu-id="28cc1-106">**IWMProfile** 介面是 [*設定檔*](wmformat-glossary.md)物件的主要介面。</span><span class="sxs-lookup"><span data-stu-id="28cc1-106">The **IWMProfile** interface is the primary interface for a [*profile*](wmformat-glossary.md) object.</span></span> <span data-ttu-id="28cc1-107">設定檔物件是用來設定自訂設定檔。</span><span class="sxs-lookup"><span data-stu-id="28cc1-107">A profile object is used to configure custom profiles.</span></span> <span data-ttu-id="28cc1-108">您可以使用 **IWMProfile** 來建立、刪除或修改串流設定物件和相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="28cc1-108">You can use **IWMProfile** to create, delete, or modify stream configuration objects and mutual exclusion objects.</span></span> <span data-ttu-id="28cc1-109">您也可以設定和取得設定檔的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="28cc1-109">You can also set and retrieve general information about the profile.</span></span> <span data-ttu-id="28cc1-110">若要存取設定檔物件的所有功能，您應該使用繼承自 **IWMProfile** 和 [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)的 [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)。</span><span class="sxs-lookup"><span data-stu-id="28cc1-110">To access all the features of the profile object, you should use [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), which inherits from **IWMProfile** and [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span></span>

<span data-ttu-id="28cc1-111">**IWMProfile** 也可以透過 reader 物件來存取，您可以在其中使用它來取得讀取器中所載入之檔案的資料流程相關資訊。</span><span class="sxs-lookup"><span data-stu-id="28cc1-111">**IWMProfile** is also accessible through the reader object, where you can use it to get information about the streams of a file that is loaded in the reader.</span></span> <span data-ttu-id="28cc1-112">從讀取器存取 **IWMProfile** 時，您可以對設定檔進行變更，但不能將任何變更儲存到檔案中。</span><span class="sxs-lookup"><span data-stu-id="28cc1-112">When accessing **IWMProfile** from the reader, you can make changes to the profile, but none of the changes can be saved to the file.</span></span> <span data-ttu-id="28cc1-113">使用現有檔案的設定檔作為新設定檔的基礎通常很方便。</span><span class="sxs-lookup"><span data-stu-id="28cc1-113">It is often handy to use the profile of an existing file as the foundation of a new profile.</span></span> <span data-ttu-id="28cc1-114">同步讀取器以與讀取器相同的方式支援 **IWMProfile** 。</span><span class="sxs-lookup"><span data-stu-id="28cc1-114">The synchronous reader supports **IWMProfile** in the same way as the reader.</span></span>

<span data-ttu-id="28cc1-115">透過讀取器或同步讀取器取得的設定檔資訊不是來自 prx 檔案。</span><span class="sxs-lookup"><span data-stu-id="28cc1-115">The profile information obtained through the reader or synchronous reader does not come from a .prx file.</span></span> <span data-ttu-id="28cc1-116">讀取器會使用 ASF 檔案中的資訊來組合串流設定。</span><span class="sxs-lookup"><span data-stu-id="28cc1-116">The reader uses the information in the ASF file to assemble the stream configurations.</span></span> <span data-ttu-id="28cc1-117">因此，某些設定檔資訊（例如名稱和描述）無法透過讀取器使用。</span><span class="sxs-lookup"><span data-stu-id="28cc1-117">Thus certain profile information, like the name and description, are not available through the reader.</span></span>

<span data-ttu-id="28cc1-118">有幾種方式可以取得 **IWMProfile** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="28cc1-118">There are several ways to obtain a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="28cc1-119">配置檔案管理員有方法可建立新的設定檔，以及存取現有的設定檔。</span><span class="sxs-lookup"><span data-stu-id="28cc1-119">The profile manager has methods to create a new profile and to access existing profiles.</span></span> <span data-ttu-id="28cc1-120">所有這些方法都會設定 **IWMProfile** 指標。</span><span class="sxs-lookup"><span data-stu-id="28cc1-120">All of these methods set an **IWMProfile** pointer.</span></span> <span data-ttu-id="28cc1-121">讀取檔案時，可以藉由呼叫任何讀取器介面的 **QueryInterface** 方法來取得 **IWMProfile** 的指標。</span><span class="sxs-lookup"><span data-stu-id="28cc1-121">When reading a file, a pointer to **IWMProfile** can be obtained by calling the **QueryInterface** method of any reader interface.</span></span> <span data-ttu-id="28cc1-122">同樣地，同步讀取器物件的任何介面都可以透過呼叫 **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)來取得指標。</span><span class="sxs-lookup"><span data-stu-id="28cc1-122">Likewise, any interface of the synchronous reader object can obtain a pointer with a call to **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span></span>

## <a name="members"></a><span data-ttu-id="28cc1-123">成員</span><span class="sxs-lookup"><span data-stu-id="28cc1-123">Members</span></span>

<span data-ttu-id="28cc1-124">**IWMProfile** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="28cc1-124">The **IWMProfile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="28cc1-125">**IWMProfile** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="28cc1-125">**IWMProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="28cc1-126">方法</span><span class="sxs-lookup"><span data-stu-id="28cc1-126">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="28cc1-127">方法</span><span class="sxs-lookup"><span data-stu-id="28cc1-127">Methods</span></span>

<span data-ttu-id="28cc1-128">**IWMProfile** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="28cc1-128">The **IWMProfile** interface has these methods.</span></span>



| <span data-ttu-id="28cc1-129">方法</span><span class="sxs-lookup"><span data-stu-id="28cc1-129">Method</span></span>                                                                  | <span data-ttu-id="28cc1-130">描述</span><span class="sxs-lookup"><span data-stu-id="28cc1-130">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28cc1-131">**AddMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="28cc1-131">**AddMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | <span data-ttu-id="28cc1-132">將相互排除物件新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="28cc1-132">Adds a mutual exclusion object to the profile.</span></span><br/>                                   |
| [<span data-ttu-id="28cc1-133">**AddStream**</span><span class="sxs-lookup"><span data-stu-id="28cc1-133">**AddStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | <span data-ttu-id="28cc1-134">將資料流程新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="28cc1-134">Adds a stream to the profile.</span></span><br/>                                                    |
| [<span data-ttu-id="28cc1-135">**CreateNewMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="28cc1-135">**CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="28cc1-136">建立設定檔的相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="28cc1-136">Creates a mutual exclusion object for the profile.</span></span><br/>                               |
| [<span data-ttu-id="28cc1-137">**CreateNewStream**</span><span class="sxs-lookup"><span data-stu-id="28cc1-137">**CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | <span data-ttu-id="28cc1-138">建立設定檔的串流設定物件。</span><span class="sxs-lookup"><span data-stu-id="28cc1-138">Creates a stream configuration object for the profile.</span></span><br/>                           |
| [<span data-ttu-id="28cc1-139">**GetDescription**</span><span class="sxs-lookup"><span data-stu-id="28cc1-139">**GetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | <span data-ttu-id="28cc1-140">捕獲設定檔的描述。</span><span class="sxs-lookup"><span data-stu-id="28cc1-140">Retrieves the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="28cc1-141">**GetMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="28cc1-141">**GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="28cc1-142">從設定檔抓取相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="28cc1-142">Retrieves a mutual exclusion object from the profile.</span></span><br/>                            |
| [<span data-ttu-id="28cc1-143">**GetMutualExclusionCount**</span><span class="sxs-lookup"><span data-stu-id="28cc1-143">**GetMutualExclusionCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | <span data-ttu-id="28cc1-144">捕獲設定檔中互斥物件的數目。</span><span class="sxs-lookup"><span data-stu-id="28cc1-144">Retrieves the number of mutual exclusion objects in the profile.</span></span><br/>                 |
| [<span data-ttu-id="28cc1-145">**GetName**</span><span class="sxs-lookup"><span data-stu-id="28cc1-145">**GetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | <span data-ttu-id="28cc1-146">捕獲設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="28cc1-146">Retrieves the name of the profile.</span></span><br/>                                               |
| [<span data-ttu-id="28cc1-147">**GetStream**</span><span class="sxs-lookup"><span data-stu-id="28cc1-147">**GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | <span data-ttu-id="28cc1-148">使用自設定檔中的索引編號來抓取資料流程。</span><span class="sxs-lookup"><span data-stu-id="28cc1-148">Retrieves a stream, using an index number, from the profile.</span></span><br/>                     |
| [<span data-ttu-id="28cc1-149">**GetStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="28cc1-149">**GetStreamByNumber**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | <span data-ttu-id="28cc1-150">使用來自設定檔的資料流程數目來抓取資料流程。</span><span class="sxs-lookup"><span data-stu-id="28cc1-150">Retrieves a stream, using the number of the stream, from the profile.</span></span><br/>            |
| [<span data-ttu-id="28cc1-151">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="28cc1-151">**GetStreamCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | <span data-ttu-id="28cc1-152">捕獲設定檔中的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="28cc1-152">Retrieves the number of streams in the profile.</span></span><br/>                                  |
| [<span data-ttu-id="28cc1-153">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="28cc1-153">**GetVersion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | <span data-ttu-id="28cc1-154">捕獲設定檔中 Microsoft Windows Media Services 的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="28cc1-154">Retrieves the version number of Microsoft Windows Media Services in the profile.</span></span><br/> |
| [<span data-ttu-id="28cc1-155">**ReconfigStream**</span><span class="sxs-lookup"><span data-stu-id="28cc1-155">**ReconfigStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | <span data-ttu-id="28cc1-156">啟用要包含在設定檔中的串流設定變更。</span><span class="sxs-lookup"><span data-stu-id="28cc1-156">Enables changes made to a stream configuration to be included in the profile.</span></span><br/>    |
| [<span data-ttu-id="28cc1-157">**RemoveMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="28cc1-157">**RemoveMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | <span data-ttu-id="28cc1-158">從設定檔中移除相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="28cc1-158">Removes a mutual exclusion object from the profile.</span></span><br/>                              |
| [<span data-ttu-id="28cc1-159">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="28cc1-159">**RemoveStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | <span data-ttu-id="28cc1-160">從設定檔移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="28cc1-160">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="28cc1-161">**RemoveStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="28cc1-161">**RemoveStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | <span data-ttu-id="28cc1-162">從設定檔移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="28cc1-162">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="28cc1-163">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="28cc1-163">**SetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | <span data-ttu-id="28cc1-164">指定設定檔的描述。</span><span class="sxs-lookup"><span data-stu-id="28cc1-164">Specifies the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="28cc1-165">**SetName**</span><span class="sxs-lookup"><span data-stu-id="28cc1-165">**SetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | <span data-ttu-id="28cc1-166">指定設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="28cc1-166">Specifies the name of the profile.</span></span><br/>                                               |



 

<span data-ttu-id="28cc1-167">如需有關使用此介面的 QueryInterface 方法可取得哪些介面的詳細資訊，請參閱此介面執行所在物件的主題。</span><span class="sxs-lookup"><span data-stu-id="28cc1-167">For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.</span></span>

## <a name="see-also"></a><span data-ttu-id="28cc1-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28cc1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28cc1-169">**介面**</span><span class="sxs-lookup"><span data-stu-id="28cc1-169">**Interfaces**</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="28cc1-170">**IWMProfileManager 介面**</span><span class="sxs-lookup"><span data-stu-id="28cc1-170">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="28cc1-171">**設定檔管理員物件**</span><span class="sxs-lookup"><span data-stu-id="28cc1-171">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="28cc1-172">**讀取器物件**</span><span class="sxs-lookup"><span data-stu-id="28cc1-172">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="28cc1-173">**同步讀取器物件**</span><span class="sxs-lookup"><span data-stu-id="28cc1-173">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="28cc1-174">**使用設定檔**</span><span class="sxs-lookup"><span data-stu-id="28cc1-174">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

