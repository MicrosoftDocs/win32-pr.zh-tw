---
description: 如果電腦是在網路上執行 Windows 2000 Server 或更新版本，則使用者可以將其設定檔儲存在伺服器上。 這些設定檔稱為漫遊使用者設定檔。
title: 漫遊使用者設定檔
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973341"
---
# <a name="roaming-user-profiles"></a><span data-ttu-id="18e8e-104">漫遊使用者設定檔</span><span class="sxs-lookup"><span data-stu-id="18e8e-104">Roaming User Profiles</span></span>

<span data-ttu-id="18e8e-105">如果電腦是在網路上執行 Windows 2000 Server 或更新版本，則使用者可以將其設定檔儲存在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="18e8e-105">If a computer is running Windows 2000 Server or later on a network, users can store their profiles on the server.</span></span> <span data-ttu-id="18e8e-106">這些設定檔稱為 *漫遊使用者設定檔*。</span><span class="sxs-lookup"><span data-stu-id="18e8e-106">These profiles are called *roaming user profiles*.</span></span>

<span data-ttu-id="18e8e-107">漫遊使用者設定檔有下列優點：</span><span class="sxs-lookup"><span data-stu-id="18e8e-107">Roaming user profiles have the following advantages:</span></span>

-   <span data-ttu-id="18e8e-108">自動資源可用性。</span><span class="sxs-lookup"><span data-stu-id="18e8e-108">Automatic resource availability.</span></span> <span data-ttu-id="18e8e-109">當使用者登入網路上的任何電腦時，會自動使用使用者的唯一設定檔。</span><span class="sxs-lookup"><span data-stu-id="18e8e-109">A user's unique profile is automatically available when he or she logs on to any computer on the network.</span></span> <span data-ttu-id="18e8e-110">使用者不需要在網路上使用的每部電腦上建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="18e8e-110">Users do not need to create a profile on each computer they use on a network.</span></span>
-   <span data-ttu-id="18e8e-111">簡化的電腦更換與備份。</span><span class="sxs-lookup"><span data-stu-id="18e8e-111">Simplified computer replacement and backup.</span></span> <span data-ttu-id="18e8e-112">當使用者的電腦必須被取代時，就可以輕鬆地予以取代，因為所有使用者的設定檔資訊都是在網路上分開維護，而不受個別電腦的影響。</span><span class="sxs-lookup"><span data-stu-id="18e8e-112">When a user's computer must be replaced, it can be replaced easily because all of the user's profile information is maintained separately on the network, independent of an individual computer.</span></span> <span data-ttu-id="18e8e-113">當使用者第一次登入新電腦時，會將使用者設定檔的伺服器複本複製到新電腦。</span><span class="sxs-lookup"><span data-stu-id="18e8e-113">When the user logs on to the new computer for the first time, the server copy of the user's profile is copied to the new computer.</span></span>

<span data-ttu-id="18e8e-114">當使用者使用 [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) 函數登入時，不會自動載入使用者的設定檔。</span><span class="sxs-lookup"><span data-stu-id="18e8e-114">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="18e8e-115">若要以程式設計方式載入漫遊使用者設定檔，請使用 [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) 函數。</span><span class="sxs-lookup"><span data-stu-id="18e8e-115">To load a roaming user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="18e8e-116">若要卸載 **LoadUserProfile** 所載入的漫遊使用者設定檔，請呼叫 [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) 函數。</span><span class="sxs-lookup"><span data-stu-id="18e8e-116">To unload a roaming user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
