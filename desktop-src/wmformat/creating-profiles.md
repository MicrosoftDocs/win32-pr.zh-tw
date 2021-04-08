---
title: 建立設定檔
description: 建立設定檔
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows Media Format SDK，設定檔
- 設定檔，建立
- 設定檔，IWMProfileManager 介面
- IWMProfileManager，建立設定檔
- 設定檔，WMCreateProfileManager 函式
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023013"
---
# <a name="creating-profiles"></a><span data-ttu-id="39845-109">建立設定檔</span><span class="sxs-lookup"><span data-stu-id="39845-109">Creating Profiles</span></span>

<span data-ttu-id="39845-110">在許多情況下，您會想要建立一個空白設定檔來設定您的需求。</span><span class="sxs-lookup"><span data-stu-id="39845-110">In many cases, you will want to create an empty profile to configure for your needs.</span></span> <span data-ttu-id="39845-111">在其他情況下，您可以更輕鬆地編輯現有的設定檔，例如系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="39845-111">In other cases it is easier to edit an existing profile, like a system profile.</span></span> <span data-ttu-id="39845-112">如需使用系統設定檔的詳細資訊，請參閱 [使用系統設定檔](using-system-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="39845-112">For more information about using system profiles, see [Using System Profiles](using-system-profiles.md).</span></span>

<span data-ttu-id="39845-113">建立可供您設定的空白設定檔需要設定檔管理員物件。</span><span class="sxs-lookup"><span data-stu-id="39845-113">Creating an empty profile, ready for you to configure, requires a profile manager object.</span></span> <span data-ttu-id="39845-114">若要取得配置檔案管理員物件的 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) 介面，請呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數。</span><span class="sxs-lookup"><span data-stu-id="39845-114">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>

<span data-ttu-id="39845-115">若要建立空的設定檔，請呼叫 [**IWMProfileManager：： CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile)。</span><span class="sxs-lookup"><span data-stu-id="39845-115">To create an empty profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span> <span data-ttu-id="39845-116">當您建立空白設定檔時，您唯一指定的就是設定檔所符合的 Windows Media 格式 SDK 版本。</span><span class="sxs-lookup"><span data-stu-id="39845-116">When you create an empty profile, the only thing you specify is the version of the Windows Media Format SDK with which the profile complies.</span></span> <span data-ttu-id="39845-117">除非您有特定的需要使用舊版，否則您應該一律使用最新版本。</span><span class="sxs-lookup"><span data-stu-id="39845-117">Unless you have a specific need to use a previous version, you should always use the latest version.</span></span> <span data-ttu-id="39845-118">版本會指示設定檔的結構;先前的版本不支援某些屬性。</span><span class="sxs-lookup"><span data-stu-id="39845-118">The version dictates the structure of the profile; previous versions did not support some properties.</span></span>

<span data-ttu-id="39845-119">下列範例程式碼顯示如何建立新的設定檔。</span><span class="sxs-lookup"><span data-stu-id="39845-119">The following example code shows how to create a new profile.</span></span> <span data-ttu-id="39845-120">若要在您的應用程式中編譯此程式碼，請包含 stdio.h .h。</span><span class="sxs-lookup"><span data-stu-id="39845-120">To compile this code in your application, include stdio.h.</span></span> <span data-ttu-id="39845-121">如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="39845-121">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="39845-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="39845-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39845-123">**IWMProfile 介面**</span><span class="sxs-lookup"><span data-stu-id="39845-123">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="39845-124">**IWMProfileManager 介面**</span><span class="sxs-lookup"><span data-stu-id="39845-124">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="39845-125">**使用設定檔**</span><span class="sxs-lookup"><span data-stu-id="39845-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




