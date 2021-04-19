---
title: 設定檔管理員物件
description: 設定檔管理員物件
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows Media 格式 SDK，配置檔案管理員物件
- Advanced Systems Format (ASF) 、profile manager 物件
- ASF (Advanced Systems Format) ，profile manager 物件
- 物件，配置檔案管理員物件
- 設定檔，物件
- 設定檔，配置檔案管理員物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106969095"
---
# <a name="profile-manager-object"></a><span data-ttu-id="365de-109">設定檔管理員物件</span><span class="sxs-lookup"><span data-stu-id="365de-109">Profile Manager Object</span></span>

<span data-ttu-id="365de-110">設定檔是一組用來建立 ASF 檔案的媒體參數。</span><span class="sxs-lookup"><span data-stu-id="365de-110">A profile is a set of media parameters used to create an ASF file.</span></span> <span data-ttu-id="365de-111">配置檔案管理員物件會建立設定檔物件來進行編輯。</span><span class="sxs-lookup"><span data-stu-id="365de-111">The profile manager object creates profile objects for editing.</span></span> <span data-ttu-id="365de-112">您可以建立不含任何資料的設定檔物件，或是從現有的設定檔資料建立。</span><span class="sxs-lookup"><span data-stu-id="365de-112">Profile objects can be created without any data in them or built from existing profile data.</span></span> <span data-ttu-id="365de-113">配置檔案管理員物件也提供列舉支援的編解碼器，以及查詢這些編解碼器以取得相關資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="365de-113">The profile manager object also provides methods for enumerating supported codecs and querying those codecs for information.</span></span>

<span data-ttu-id="365de-114">配置檔案管理員物件是由 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函式所建立，它會將指標設定為 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) 介面。</span><span class="sxs-lookup"><span data-stu-id="365de-114">The profile manager object is created by the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function, which sets a pointer to an [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="365de-115">您可以藉由呼叫 **QueryInterface** 方法來取得配置檔案管理員物件的其他介面。</span><span class="sxs-lookup"><span data-stu-id="365de-115">The other interfaces of the profile manager object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="365de-116">配置檔案管理員物件支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="365de-116">The following interfaces are supported by the profile manager object.</span></span>



| <span data-ttu-id="365de-117">介面</span><span class="sxs-lookup"><span data-stu-id="365de-117">Interface</span></span>                                                      | <span data-ttu-id="365de-118">描述</span><span class="sxs-lookup"><span data-stu-id="365de-118">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="365de-119">**IWMCodecInfo**</span><span class="sxs-lookup"><span data-stu-id="365de-119">**IWMCodecInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | <span data-ttu-id="365de-120">抓取支援的編解碼器及其格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="365de-120">Retrieves information about supported codecs and their formats.</span></span>                                                                              |
| [<span data-ttu-id="365de-121">**IWMCodecInfo2**</span><span class="sxs-lookup"><span data-stu-id="365de-121">**IWMCodecInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | <span data-ttu-id="365de-122">抓取支援的編解碼器名稱和其格式的描述。</span><span class="sxs-lookup"><span data-stu-id="365de-122">Retrieves the names of the supported codecs and the descriptions of their formats.</span></span> <span data-ttu-id="365de-123">繼承 **IWMCodecInfo** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="365de-123">Inherits all of the methods of **IWMCodecInfo**.</span></span>          |
| [<span data-ttu-id="365de-124">**IWMCodecInfo3**</span><span class="sxs-lookup"><span data-stu-id="365de-124">**IWMCodecInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | <span data-ttu-id="365de-125">抓取編解碼器屬性和查詢編解碼器以取得支援的功能。</span><span class="sxs-lookup"><span data-stu-id="365de-125">Retrieves codec properties and queries codecs for supported features.</span></span> <span data-ttu-id="365de-126">繼承 **IWMCodecInfo** 和 **IWMCodecInfo2** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="365de-126">Inherits all of the methods of **IWMCodecInfo** and **IWMCodecInfo2**.</span></span> |
| [<span data-ttu-id="365de-127">**IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="365de-127">**IWMProfileManager**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | <span data-ttu-id="365de-128">建立新的設定檔、載入現有的設定檔，並儲存自訂設定檔。</span><span class="sxs-lookup"><span data-stu-id="365de-128">Creates new profiles, loads existing profiles, and saves custom profiles.</span></span>                                                                    |
| [<span data-ttu-id="365de-129">**IWMProfileManager2**</span><span class="sxs-lookup"><span data-stu-id="365de-129">**IWMProfileManager2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | <span data-ttu-id="365de-130">控制配置檔案管理員列舉的系統設定檔版本。</span><span class="sxs-lookup"><span data-stu-id="365de-130">Controls the version of system profiles enumerated by the profile manager.</span></span> <span data-ttu-id="365de-131">繼承 **IWMProfileManager** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="365de-131">Inherits all of the methods of **IWMProfileManager**.</span></span>             |
| [<span data-ttu-id="365de-132">**IWMProfileManagerLanguage**</span><span class="sxs-lookup"><span data-stu-id="365de-132">**IWMProfileManagerLanguage**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | <span data-ttu-id="365de-133">控制配置檔案管理員所剖析之系統設定檔的語言。</span><span class="sxs-lookup"><span data-stu-id="365de-133">Controls the language of the system profiles parsed by the profile manager.</span></span>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="365de-134">備註</span><span class="sxs-lookup"><span data-stu-id="365de-134">Remarks</span></span>

<span data-ttu-id="365de-135">當配置檔案管理員物件建立時，它會剖析所有系統設定檔，這可能需要幾秒鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="365de-135">When a profile manager object is created, it parses all of the system profiles, which can take several seconds.</span></span> <span data-ttu-id="365de-136">每次需要使用時建立和發行配置檔案管理員，將會對效能造成不良的影響。</span><span class="sxs-lookup"><span data-stu-id="365de-136">Creating and releasing a profile manager every time you need to use it will adversely affect performance.</span></span> <span data-ttu-id="365de-137">您應該在應用程式中建立配置檔案管理員一次，而且只有在不再需要使用它時，才將它釋放。</span><span class="sxs-lookup"><span data-stu-id="365de-137">You should create a profile manager once in your application and release it only when you no longer need to use it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="365de-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="365de-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="365de-139">**物件**</span><span class="sxs-lookup"><span data-stu-id="365de-139">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="365de-140">**設定檔物件**</span><span class="sxs-lookup"><span data-stu-id="365de-140">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="365de-141">**配置 檔**</span><span class="sxs-lookup"><span data-stu-id="365de-141">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




