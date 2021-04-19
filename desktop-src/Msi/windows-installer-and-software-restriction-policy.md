---
description: Windows Installer 已與 Microsoft Windows XP 中的軟體限制原則整合。
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Installer 和軟體限制原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975762"
---
# <a name="windows-installer-and-software-restriction-policy"></a><span data-ttu-id="8ab36-103">Windows Installer 和軟體限制原則</span><span class="sxs-lookup"><span data-stu-id="8ab36-103">Windows Installer and Software Restriction Policy</span></span>

<span data-ttu-id="8ab36-104">Windows Installer 已與 Microsoft Windows XP 中的軟體限制原則整合。</span><span class="sxs-lookup"><span data-stu-id="8ab36-104">Windows Installer is integrated with Software Restriction Policy in Microsoft Windows XP.</span></span> <span data-ttu-id="8ab36-105">軟體限制原則可透過群組原則來設定。</span><span class="sxs-lookup"><span data-stu-id="8ab36-105">Software Restriction Policy is configurable through group policy.</span></span> <span data-ttu-id="8ab36-106">軟體限制原則可讓系統管理員根據路徑、URL 區域、雜湊或發行者準則，限制系統管理員和非系統管理員執行檔案。</span><span class="sxs-lookup"><span data-stu-id="8ab36-106">Software Restriction Policy allows an administrator to restrict both administrators and nonadministrators from running files based upon the path, URL zone, hash, or publisher criteria.</span></span> <span data-ttu-id="8ab36-107">軟體限制原則有兩種層級：不受限制且不允許。</span><span class="sxs-lookup"><span data-stu-id="8ab36-107">Software Restriction Policy has two levels: unrestricted and disallowed.</span></span> <span data-ttu-id="8ab36-108">Windows Installer 只會安裝可在不受限制的層級執行的封裝。</span><span class="sxs-lookup"><span data-stu-id="8ab36-108">The Windows Installer only installs packages allowed to run at the unrestricted level.</span></span>

<span data-ttu-id="8ab36-109">您也必須允許修補程式或轉換在不受限制的層級上執行。</span><span class="sxs-lookup"><span data-stu-id="8ab36-109">Patches or transforms must also be allowed to run at the unrestricted level.</span></span> <span data-ttu-id="8ab36-110">如果封裝、修補程式或轉換設定為在與不受限制的層級上執行，則 Windows Installer 會顯示錯誤訊息，並在應用程式事件記錄檔中記錄一個專案。</span><span class="sxs-lookup"><span data-stu-id="8ab36-110">If a package, patch, or transform is configured to run at a level different from unrestricted, the Windows Installer displays an error message and logs an entry in the application event log.</span></span> <span data-ttu-id="8ab36-111">軟體限制原則會在應用程式第一次安裝時、套用新修補程式時，以及重新快取安裝套件時進行評估。</span><span class="sxs-lookup"><span data-stu-id="8ab36-111">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="8ab36-112">如果封裝、修補程式或轉換受到限制，Windows Installer 會顯示錯誤訊息，並將 [事件記錄](event-logging.md) 專案寫入應用程式事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="8ab36-112">If a package, patch, or transform is restricted, the Windows Installer displays an error message and writes an [Event Logging](event-logging.md) entry in the application event log.</span></span> <span data-ttu-id="8ab36-113">軟體限制原則會在應用程式第一次安裝時、套用新修補程式時，以及重新快取安裝套件時進行評估。</span><span class="sxs-lookup"><span data-stu-id="8ab36-113">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="8ab36-114">如需軟體限制原則的詳細資訊，請參閱產品檔集並 [搜尋 TechNet 網站](https://www.microsoft.com/technet/sitemap.mspx)。</span><span class="sxs-lookup"><span data-stu-id="8ab36-114">For more information on software restriction policy, consult the product documentation and [search the TechNet Site](https://www.microsoft.com/technet/sitemap.mspx).</span></span>

 

 



