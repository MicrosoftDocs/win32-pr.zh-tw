---
description: 下列 API 元素會與使用者設定檔搭配使用。
title: 使用者設定檔參考
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5d4c4f585eda66674059f402dbd73f106a3e4f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973728"
---
# <a name="user-profiles-reference"></a><span data-ttu-id="00a5b-103">使用者設定檔參考</span><span class="sxs-lookup"><span data-stu-id="00a5b-103">User Profiles Reference</span></span>

<span data-ttu-id="00a5b-104">下列 API 元素會與使用者設定檔搭配使用。</span><span class="sxs-lookup"><span data-stu-id="00a5b-104">The following API elements are used with user profiles.</span></span>

## <a name="functions"></a><span data-ttu-id="00a5b-105">函式</span><span class="sxs-lookup"><span data-stu-id="00a5b-105">Functions</span></span>



| <span data-ttu-id="00a5b-106">函式</span><span class="sxs-lookup"><span data-stu-id="00a5b-106">Function</span></span>                                                                   | <span data-ttu-id="00a5b-107">描述</span><span class="sxs-lookup"><span data-stu-id="00a5b-107">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00a5b-108">**CreateEnvironmentBlock**</span><span class="sxs-lookup"><span data-stu-id="00a5b-108">**CreateEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | <span data-ttu-id="00a5b-109">抓取指定使用者的環境變數。</span><span class="sxs-lookup"><span data-stu-id="00a5b-109">Retrieves the environment variables for the specified user.</span></span>                                                   |
| [<span data-ttu-id="00a5b-110">**CreateProfile**</span><span class="sxs-lookup"><span data-stu-id="00a5b-110">**CreateProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | <span data-ttu-id="00a5b-111">建立新的使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="00a5b-111">Creates a new user profile.</span></span> <span data-ttu-id="00a5b-112"> (Windows Vista 及更新版本。 ) </span><span class="sxs-lookup"><span data-stu-id="00a5b-112">(Windows Vista and later only.)</span></span>                                                   |
| [<span data-ttu-id="00a5b-113">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="00a5b-113">**DeleteProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | <span data-ttu-id="00a5b-114">從指定的電腦刪除使用者設定檔和所有使用者相關的設定。</span><span class="sxs-lookup"><span data-stu-id="00a5b-114">Deletes the user profile and all user-related settings from the specified computer.</span></span>                           |
| [<span data-ttu-id="00a5b-115">**DestroyEnvironmentBlock**</span><span class="sxs-lookup"><span data-stu-id="00a5b-115">**DestroyEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | <span data-ttu-id="00a5b-116">釋放 [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) 函數所建立的環境變數。</span><span class="sxs-lookup"><span data-stu-id="00a5b-116">Frees environment variables created by the [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) function.</span></span> |
| [<span data-ttu-id="00a5b-117">**ExpandEnvironmentStringsForUser**</span><span class="sxs-lookup"><span data-stu-id="00a5b-117">**ExpandEnvironmentStringsForUser**</span></span>](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | <span data-ttu-id="00a5b-118">使用針對指定使用者所建立的環境區塊來展開來源字串。</span><span class="sxs-lookup"><span data-stu-id="00a5b-118">Expands the source string by using the environment block established for the specified user.</span></span>                  |
| [<span data-ttu-id="00a5b-119">**GetAllUsersProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="00a5b-119">**GetAllUsersProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | <span data-ttu-id="00a5b-120">抓取所有使用者設定檔之根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="00a5b-120">Retrieves the path to the root of the All Users profile.</span></span>                                                      |
| [<span data-ttu-id="00a5b-121">**GetDefaultUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="00a5b-121">**GetDefaultUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | <span data-ttu-id="00a5b-122">抓取預設使用者設定檔之根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="00a5b-122">Retrieves the path to the root of the Default User profile.</span></span>                                                   |
| [<span data-ttu-id="00a5b-123">**GetProfilesDirectory**</span><span class="sxs-lookup"><span data-stu-id="00a5b-123">**GetProfilesDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | <span data-ttu-id="00a5b-124">抓取儲存所有使用者設定檔之根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="00a5b-124">Retrieves the path to the root directory where all user profiles are stored.</span></span>                                  |
| [<span data-ttu-id="00a5b-125">**GetProfileType**</span><span class="sxs-lookup"><span data-stu-id="00a5b-125">**GetProfileType**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | <span data-ttu-id="00a5b-126">抓取為目前使用者載入的配置檔案類型。</span><span class="sxs-lookup"><span data-stu-id="00a5b-126">Retrieves the type of profile loaded for the current user.</span></span>                                                    |
| [<span data-ttu-id="00a5b-127">**GetUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="00a5b-127">**GetUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | <span data-ttu-id="00a5b-128">抓取指定使用者設定檔之根目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="00a5b-128">Retrieves the path to the root directory of the specified user's profile.</span></span>                                     |
| [<span data-ttu-id="00a5b-129">**LoadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="00a5b-129">**LoadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | <span data-ttu-id="00a5b-130">載入指定的使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="00a5b-130">Loads the specified user's profile.</span></span>                                                                           |
| [<span data-ttu-id="00a5b-131">**UnloadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="00a5b-131">**UnloadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | <span data-ttu-id="00a5b-132">卸載 [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) 函數所載入的使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="00a5b-132">Unloads a user's profile that was loaded by the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span>          |



 

<span data-ttu-id="00a5b-133">不支援 [**CreateUserProfileEx**](createuserprofileex.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="00a5b-133">The [**CreateUserProfileEx**](createuserprofileex.md) function is not supported.</span></span>

## <a name="structures"></a><span data-ttu-id="00a5b-134">結構</span><span class="sxs-lookup"><span data-stu-id="00a5b-134">Structures</span></span>



| <span data-ttu-id="00a5b-135">結構</span><span class="sxs-lookup"><span data-stu-id="00a5b-135">Structure</span></span>                          | <span data-ttu-id="00a5b-136">Description</span><span class="sxs-lookup"><span data-stu-id="00a5b-136">Description</span></span>                                |
|------------------------------------|--------------------------------------------|
| [<span data-ttu-id="00a5b-137">**PROFILEINFO.TXT**</span><span class="sxs-lookup"><span data-stu-id="00a5b-137">**PROFILEINFO**</span></span>](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | <span data-ttu-id="00a5b-138">包含使用者設定檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="00a5b-138">Contains information about a user profile.</span></span> |



 

 

 



