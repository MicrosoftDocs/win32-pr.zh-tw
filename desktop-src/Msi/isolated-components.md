---
description: 安裝套件的作者可以指定安裝程式將共用檔案 (共用的) 應用程式複製到該應用程式的資料夾，而不是共用位置。
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: 隔離的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689736"
---
# <a name="isolated-components"></a><span data-ttu-id="d0df8-103">隔離的元件</span><span class="sxs-lookup"><span data-stu-id="d0df8-103">Isolated Components</span></span>

<span data-ttu-id="d0df8-104">安裝套件的作者可以指定安裝程式將共用檔案 (共用的) 應用程式複製到該應用程式的資料夾，而不是共用位置。</span><span class="sxs-lookup"><span data-stu-id="d0df8-104">Authors of installation packages can specify that the installer copy the shared files (commonly shared DLLs) of an application into that application's folder rather than to a shared location.</span></span> <span data-ttu-id="d0df8-105">只有應用程式才會使用這組私用的檔案 (Dll) 。</span><span class="sxs-lookup"><span data-stu-id="d0df8-105">This private set of files (DLLs) are then used only by the application.</span></span> <span data-ttu-id="d0df8-106">以這種方式將應用程式與共享的元件隔離，有下列優點：</span><span class="sxs-lookup"><span data-stu-id="d0df8-106">Isolating the application together with its shared components in this manner has the following advantages:</span></span>

-   <span data-ttu-id="d0df8-107">應用程式一律會使用所部署的共用檔案版本。</span><span class="sxs-lookup"><span data-stu-id="d0df8-107">The application always uses the versions of the shared files with which it was deployed.</span></span>
-   <span data-ttu-id="d0df8-108">安裝應用程式不會覆寫其他應用程式的其他版本的共用檔案。</span><span class="sxs-lookup"><span data-stu-id="d0df8-108">Installing the application does not overwrite other versions of the shared files by other applications.</span></span>
-   <span data-ttu-id="d0df8-109">後續使用不同版本的共用檔案安裝其他應用程式時，將無法覆寫此應用程式所使用的檔案。</span><span class="sxs-lookup"><span data-stu-id="d0df8-109">Subsequent installations of other applications using different versions of the shared files cannot overwrite the files used by this application.</span></span>

<span data-ttu-id="d0df8-110">由於目前的 COM 執行會在每個 CLSID/內容配對的登錄中保留單一完整路徑，因此它會強制所有應用程式使用相同版本的共用 DLL。</span><span class="sxs-lookup"><span data-stu-id="d0df8-110">Because the current implementation of COM keeps a single full path in the registry for each CLSID/Context pair, it forces all applications to use the same version of a shared DLL.</span></span> <span data-ttu-id="d0df8-111">為了讓應用程式保留 COM 伺服器的私用複本，Windows 2000 中的系統載入器會檢查是否存在。應用程式資料夾中的本機檔案。</span><span class="sxs-lookup"><span data-stu-id="d0df8-111">To enable an application to keep a private copy of a COM server, the system loader in Windows 2000 checks for the presence of a .LOCAL file in the application's folder.</span></span> <span data-ttu-id="d0df8-112">如果系統載入器偵測到。本機檔案，它會改變其搜尋邏輯，以偏好位於與應用程式相同資料夾中的 Dll。</span><span class="sxs-lookup"><span data-stu-id="d0df8-112">If the system loader detects a .LOCAL file, it alters its search logic to prefer DLLs located in the same folder as the application.</span></span>

<span data-ttu-id="d0df8-113">當 Windows Installer 執行[IsolateComponents 動作](isolatecomponents-action.md)時，它們會將元件的檔案複製 (通常是在 IsolatedComponent 資料表的元件共用資料行中指定的共用 DLL) ， \_ (通常是元件[](isolatedcomponent-table.md) \_ 應用程式資料行中所指定的 .exe 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="d0df8-113">When Windows Installer runs the [IsolateComponents action](isolatecomponents-action.md) they copy the files of the component (commonly a shared DLL) specified in the Component\_Shared column of the [IsolatedComponent table](isolatedcomponent-table.md) into the same folder as the component (commonly an .exe file) specified in the Component\_Application column.</span></span> <span data-ttu-id="d0df8-114">安裝程式會在此目錄中建立檔案（長度為零個位元組），具有元件應用程式金鑰檔的簡短檔案名 \_ (通常是與應用程式的 .exe) 的相同名稱。當地。</span><span class="sxs-lookup"><span data-stu-id="d0df8-114">The installer creates a file in this directory, zero bytes in length, having the short file name of the key file for Component\_Application (typically the name is the same as the application's .exe) appended with .LOCAL.</span></span> <span data-ttu-id="d0df8-115">安裝程式會使用該元件在其共用位置的註冊，且不會針對私人位置中的元件複本寫入任何註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="d0df8-115">The installer uses the registration for the component in its shared location and does not write any registration information for the copy of the component in the private location.</span></span>

<span data-ttu-id="d0df8-116">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d0df8-116">For more information, see:</span></span>

-   [<span data-ttu-id="d0df8-117">獨立元件的安裝</span><span class="sxs-lookup"><span data-stu-id="d0df8-117">Installation of Isolated Components</span></span>](installation-of-isolated-components.md)
-   [<span data-ttu-id="d0df8-118">重新安裝隔離的元件</span><span class="sxs-lookup"><span data-stu-id="d0df8-118">Reinstallation of Isolated Components</span></span>](reinstallation-of-isolated-components.md)
-   [<span data-ttu-id="d0df8-119">移除隔離的元件</span><span class="sxs-lookup"><span data-stu-id="d0df8-119">Removal of Isolated Components</span></span>](removal-of-isolated-components.md)
-   [<span data-ttu-id="d0df8-120">使用隔離的元件</span><span class="sxs-lookup"><span data-stu-id="d0df8-120">Using Isolated Components</span></span>](using-isolated-components.md)

 

 



