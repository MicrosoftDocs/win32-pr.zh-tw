---
title: 使用自訂相互排除類型
description: 使用自訂相互排除類型
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- 相互排除，IWMMutualExclusion 介面
- 相互排除，自訂類型
- 設定檔，自訂相互排除類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092542"
---
# <a name="using-custom-mutual-exclusion-types"></a><span data-ttu-id="e41e5-107">使用自訂相互排除類型</span><span class="sxs-lookup"><span data-stu-id="e41e5-107">Using Custom Mutual Exclusion Types</span></span>

<span data-ttu-id="e41e5-108">您可以使用設定檔中的相互排除物件來符合自訂案例的需求。</span><span class="sxs-lookup"><span data-stu-id="e41e5-108">You can use mutual exclusion objects in a profile to meet the needs of custom scenarios.</span></span> <span data-ttu-id="e41e5-109">藉由將未知的 GUID 值 CLSID \_ WMMUTEX 傳遞 \_ 至 [**IWMMutualExclusion：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)，您會通知互斥物件您正在使用自訂案例。</span><span class="sxs-lookup"><span data-stu-id="e41e5-109">By passing the GUID value CLSID\_WMMUTEX\_Unknown to [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), you inform the mutual exclusion object that you are using a custom scenario.</span></span>

<span data-ttu-id="e41e5-110">當您讀取具有自訂互斥值的檔案時，您必須手動控制資料流程選取範圍。</span><span class="sxs-lookup"><span data-stu-id="e41e5-110">You must manually control stream selection when you read a file with a custom mutual exclusion value.</span></span> <span data-ttu-id="e41e5-111">讀取器物件將使用您新增至互斥的第一個資料流程作為預設值。</span><span class="sxs-lookup"><span data-stu-id="e41e5-111">The reader object will use the first stream you add to the mutual exclusion as the default.</span></span>

<span data-ttu-id="e41e5-112">使用下列步驟來建立自訂的互斥物件，並將其新增至設定檔：</span><span class="sxs-lookup"><span data-stu-id="e41e5-112">Use the following steps to create a custom mutual exclusion object and add it to a profile:</span></span>

1.  <span data-ttu-id="e41e5-113">藉由呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數來建立配置檔案管理員。</span><span class="sxs-lookup"><span data-stu-id="e41e5-113">Create a profile manager by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="e41e5-114">請從現有的設定檔開始，或建立一個全新的設定檔。</span><span class="sxs-lookup"><span data-stu-id="e41e5-114">Either start with an existing profile, or create an entirely new one.</span></span>
    -   <span data-ttu-id="e41e5-115">如果您使用現有的設定檔，請呼叫 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) 介面的其中一個 load 方法。</span><span class="sxs-lookup"><span data-stu-id="e41e5-115">If you are using an existing profile, call one of the load methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="e41e5-116">然後跳至步驟4。</span><span class="sxs-lookup"><span data-stu-id="e41e5-116">Then skip to step 4.</span></span>
    -   <span data-ttu-id="e41e5-117">如果您要建立全新的設定檔，請呼叫 [**IWMProfileManager：： CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile)。</span><span class="sxs-lookup"><span data-stu-id="e41e5-117">If you are creating an entirely new profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span>
3.  <span data-ttu-id="e41e5-118">藉由呼叫 [**IWMProfile：： CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)，將資料流程新增至新的設定檔。</span><span class="sxs-lookup"><span data-stu-id="e41e5-118">Add streams to the new profile by calling [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream).</span></span> <span data-ttu-id="e41e5-119">使用 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)的方法視需要設定資料流程。</span><span class="sxs-lookup"><span data-stu-id="e41e5-119">Configure the streams as needed using the methods of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span> <span data-ttu-id="e41e5-120">您也可以呼叫 **QueryInterface** 來存取資料流程設定物件中的其他介面。</span><span class="sxs-lookup"><span data-stu-id="e41e5-120">You can also call **QueryInterface** to access other interfaces in the stream configuration object.</span></span>

    <span data-ttu-id="e41e5-121">**CreateNewStream** 只會建立資料流程設定物件，且不會影響設定檔。</span><span class="sxs-lookup"><span data-stu-id="e41e5-121">**CreateNewStream** creates only a stream configuration object, and does not affect the profile.</span></span> <span data-ttu-id="e41e5-122">正確設定資料流程之後，您必須呼叫 [**IWMProfile：： AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) 將資料流程新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="e41e5-122">After a stream is configured properly, you must call [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add the stream to the profile.</span></span>

4.  <span data-ttu-id="e41e5-123">藉由呼叫 [**IWMProfile：： CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion)來建立相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="e41e5-123">Create a mutual exclusion object by calling [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).</span></span>
5.  <span data-ttu-id="e41e5-124">藉由呼叫 [**IWMStreamList：： AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (可直接從 [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)) 繼承的 [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)，將所需的資料流程新增至相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="e41e5-124">Add the desired streams to the mutual exclusion object by calling [**IWMStreamList::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (available directly from [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), which inherits from [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).</span></span>
6.  <span data-ttu-id="e41e5-125">藉由呼叫 [**IWMMutualExclusion：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)，將相互排除的型別設定為 custom。</span><span class="sxs-lookup"><span data-stu-id="e41e5-125">Set the type of mutual exclusion to custom by calling [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span> <span data-ttu-id="e41e5-126">將未知的 CLSID \_ WMMUTEX 傳遞 \_ 為類型 GUID。</span><span class="sxs-lookup"><span data-stu-id="e41e5-126">Pass the CLSID\_WMMUTEX\_Unknown as the type GUID.</span></span>
7.  <span data-ttu-id="e41e5-127">藉由呼叫 [**IWMProfile：： AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)，將設定的互斥物件新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="e41e5-127">Add the configured mutual exclusion object to the profile by calling [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e41e5-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="e41e5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e41e5-129">**IWMMutualExclusion 介面**</span><span class="sxs-lookup"><span data-stu-id="e41e5-129">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="e41e5-130">**IWMProfile 介面**</span><span class="sxs-lookup"><span data-stu-id="e41e5-130">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="e41e5-131">**IWMProfileManager 介面**</span><span class="sxs-lookup"><span data-stu-id="e41e5-131">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="e41e5-132">**IWMStreamConfig 介面**</span><span class="sxs-lookup"><span data-stu-id="e41e5-132">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[<span data-ttu-id="e41e5-133">**IWMStreamList 介面**</span><span class="sxs-lookup"><span data-stu-id="e41e5-133">**IWMStreamList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[<span data-ttu-id="e41e5-134">**使用相互排除**</span><span class="sxs-lookup"><span data-stu-id="e41e5-134">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="e41e5-135">**WMCreateProfileManager**</span><span class="sxs-lookup"><span data-stu-id="e41e5-135">**WMCreateProfileManager**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




