---
title: 載入系統設定檔
description: 載入系統設定檔
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- 設定檔，系統
- 系統設定檔，載入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e745cb2fed32d650a22febef827ed7662f4448
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374455"
---
# <a name="to-load-a-system-profile"></a><span data-ttu-id="7643e-105">載入系統設定檔</span><span class="sxs-lookup"><span data-stu-id="7643e-105">To Load a System Profile</span></span>

<span data-ttu-id="7643e-106">若要變更系統設定檔，您必須將它載入至設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="7643e-106">To make changes to a system profile, you must load it into a profile object.</span></span> <span data-ttu-id="7643e-107">配置檔案管理員提供兩種載入系統設定檔的選項：依識別碼和依索引。</span><span class="sxs-lookup"><span data-stu-id="7643e-107">The profile manager provides two options for loading system profiles: by identifier, and by index.</span></span>

<span data-ttu-id="7643e-108">系統設定檔識別碼是在建立時指派給系統設定檔的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="7643e-108">A system profile identifier is a GUID value assigned to the system profile when it was created.</span></span> <span data-ttu-id="7643e-109">如需與第8版系統設定檔相關聯的 GUID 常數清單，請參閱 [系統設定檔](system-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="7643e-109">For a list of the GUID constants associated with the version 8 system profiles, see [System Profiles](system-profiles.md).</span></span> <span data-ttu-id="7643e-110">您可以在標頭檔 WMSysPrf 中找到先前版本的 GUID 常數。</span><span class="sxs-lookup"><span data-stu-id="7643e-110">You can find the GUID constants for previous versions in the header file WMSysPrf.h.</span></span> <span data-ttu-id="7643e-111">如需 Windows Media Format SDK 隨附的這個檔案和其他標頭檔的詳細資訊，請參閱連結 [庫檔案和編譯器設定](library-files-and-compiler-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="7643e-111">For more information about this and other header files included with the Windows Media Format SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

<span data-ttu-id="7643e-112">下列範例程式碼示範如何使用系統設定檔識別碼載入系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="7643e-112">The following example code demonstrates how to load a system profile using the system profile identifier.</span></span> <span data-ttu-id="7643e-113">若要讓此程式碼能夠運作，您必須包含 WMSysPrf .h 和 stdio.h。</span><span class="sxs-lookup"><span data-stu-id="7643e-113">For this code to work, you must include WMSysPrf.h and stdio.h.</span></span> <span data-ttu-id="7643e-114">如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="7643e-114">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
IWMProfileManager* pProfileMgr = NULL;
IWMProfile*        pProfile    = NULL;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager.
hr = WMCreateProfileManager(&pProfileMgr);

// Retrieve the data for the general-purpose broadband video profile.
hr = pProfileMgr->LoadProfileByID(WMProfile_V80_100Video, &pProfile);

// TODO: Perform whatever customizations are needed. For details about
// editing profiles, see Using Custom Profiles.

// Clean up.
pProfile->Release();
pProfile = NULL;
pProfileMgr->Release();
pProfileMgr = NULL;
```



<span data-ttu-id="7643e-115">如果您不知道要使用哪一個設定檔，您可以使用 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)介面的 [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount)和 [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)方法，逐一查看特定版本的所有系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="7643e-115">If you do not know which profile you want to use, you can iterate through all of the system profiles of a particular version using the [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="7643e-116">這些方法一次只處理一個版本的系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="7643e-116">These methods only deal with one version of the system profiles at a time.</span></span> <span data-ttu-id="7643e-117">如需變更系統設定檔版本的詳細資訊，請參閱 [變更系統設定檔版本](to-change-system-profile-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="7643e-117">For more information about changing the system profile version, see [To Change System Profile Versions](to-change-system-profile-versions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7643e-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="7643e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7643e-119">**使用系統設定檔**</span><span class="sxs-lookup"><span data-stu-id="7643e-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




