---
description: 當使用者第一次登入電腦時，系統會自動為每位使用者建立本機使用者設定檔。 系統會自動在本機電腦上的使用者設定檔中維護每個使用者工作環境的設定。
title: 本機使用者設定檔
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba330189b11875198ce40ffdb9dd34925e3adc4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973380"
---
# <a name="local-user-profiles"></a><span data-ttu-id="b36e8-104">本機使用者設定檔</span><span class="sxs-lookup"><span data-stu-id="b36e8-104">Local User Profiles</span></span>

<span data-ttu-id="b36e8-105">Windows 安全性需要電腦上每個使用者帳戶的使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="b36e8-105">Windows security requires a user profile for each user account on a computer.</span></span> <span data-ttu-id="b36e8-106">當使用者第一次登入電腦時，系統會自動為每位使用者建立 *本機使用者設定檔* 。</span><span class="sxs-lookup"><span data-stu-id="b36e8-106">The system automatically creates a *local user profile* for each user when the user logs on to the computer for the first time.</span></span> <span data-ttu-id="b36e8-107">系統會自動在本機電腦上的使用者設定檔中維護每個使用者工作環境的設定。</span><span class="sxs-lookup"><span data-stu-id="b36e8-107">The system automatically maintains the settings for each user's work environment in a user profile on the local computer.</span></span>

<span data-ttu-id="b36e8-108">Windows Vista 和更新版本：使用者設定檔是透過 [ **使用者帳戶** ] 控制台專案進行管理。</span><span class="sxs-lookup"><span data-stu-id="b36e8-108">Windows Vista and later: User profiles are managed through the **User Accounts** control panel item.</span></span>

<span data-ttu-id="b36e8-109">Windows 2000 和 Windows XP：若要複製或刪除使用者設定檔，請從主控台選取 [**系統**]，然後選取 [ **Advanced** ] 索引標籤，然後在 [**使用者設定檔**] 區域中選取 [**設定**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="b36e8-109">Windows 2000 and Windows XP: To copy or delete a user profile, select **System** from the Control Panel, then the **Advanced** tab, and then the **Settings** button in the **User Profile** area.</span></span>

<span data-ttu-id="b36e8-110">當使用者使用 [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) 函數登入時，不會自動載入使用者的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b36e8-110">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="b36e8-111">若要以程式設計方式載入使用者設定檔，請使用 [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) 函數。</span><span class="sxs-lookup"><span data-stu-id="b36e8-111">To load a user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="b36e8-112">若要卸載 **LoadUserProfile** 所載入的使用者設定檔，請呼叫 [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) 函數。</span><span class="sxs-lookup"><span data-stu-id="b36e8-112">To unload a user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
