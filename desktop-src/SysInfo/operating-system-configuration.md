---
description: Windows 目錄是包含以 Windows 為基礎的應用程式、初始化檔和說明檔的目錄。 GetWindowsDirectory 函式會捕獲此目錄的路徑。
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: 作業系統設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38aa2c2b6b4f6b3ac5caac78a89ad980a9bd074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193890"
---
# <a name="operating-system-configuration"></a><span data-ttu-id="85c34-104">作業系統設定</span><span class="sxs-lookup"><span data-stu-id="85c34-104">Operating System Configuration</span></span>

<span data-ttu-id="85c34-105">*Windows 目錄* 是包含以 windows 為基礎的應用程式、初始化檔和說明檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="85c34-105">The *Windows directory* is the directory that contains Windows-based applications, initialization files, and help files.</span></span> <span data-ttu-id="85c34-106">[**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)函式會捕獲此目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="85c34-106">The [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="85c34-107">*系統目錄* 是包含動態連結程式庫、驅動程式和字型檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="85c34-107">The *system directory* is the directory that contains dynamic-link libraries, drivers, and font files.</span></span> <span data-ttu-id="85c34-108">[**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)函式會捕獲此目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="85c34-108">The [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="85c34-109">[**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea)函式會捕獲目前登入系統的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="85c34-109">The [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) function retrieves the name of the user currently logged onto the system.</span></span> <span data-ttu-id="85c34-110">如果登錄中包含後者，使用者名稱可以是登入名稱或使用者的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="85c34-110">The user name is either the logon name or the user's full name, if the latter is included in the registry.</span></span>

<span data-ttu-id="85c34-111">*環境變數* 是代表系統某些元素的符號變數，例如路徑、檔案名或其他常值資料。</span><span class="sxs-lookup"><span data-stu-id="85c34-111">An *environment variable* is a symbolic variable that represents some element of the system, such as a path, a file name, or other literal data.</span></span> <span data-ttu-id="85c34-112">例如，環境變數路徑代表用來搜尋可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="85c34-112">For example, the environment variable PATH represents the directories in which to search for executable files.</span></span> <span data-ttu-id="85c34-113">當使用者登入時，系統會根據登錄的環境區段初始化環境變數。</span><span class="sxs-lookup"><span data-stu-id="85c34-113">When a user logs on, the system initializes environment variables based on the environment section of the registry.</span></span> <span data-ttu-id="85c34-114">[**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa)函式會捕獲指定環境變數的值。</span><span class="sxs-lookup"><span data-stu-id="85c34-114">The [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) function retrieves the values of specified environment variables.</span></span>

<span data-ttu-id="85c34-115">[**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo)介面會提供其他資訊。</span><span class="sxs-lookup"><span data-stu-id="85c34-115">Additional information is provided by the [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) interface.</span></span>

 

 
