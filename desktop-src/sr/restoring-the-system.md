---
title: 還原系統
description: 隨著時間使用電腦，系統會在資料封存中收集還原點，而不需要使用者進行任何管理或介入。
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c5ff4aef88ec9eca591ee3c1afb1ad570689a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967200"
---
# <a name="restoring-the-system"></a><span data-ttu-id="6a9c5-103">還原系統</span><span class="sxs-lookup"><span data-stu-id="6a9c5-103">Restoring the System</span></span>

<span data-ttu-id="6a9c5-104">隨著時間使用電腦，系統會在資料封存中收集還原點，而不需要使用者進行任何管理或介入。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-104">As the computer is used over time, restore points are collected in the data archive without any management or intervention required by the user.</span></span> <span data-ttu-id="6a9c5-105">如果使用者需要將系統還原成先前的狀態，則使用者可以透過系統還原使用者介面看到可用的還原點。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-105">If the user ever needs to restore the system to a previous state, the available restore points are made visible to the user through the System Restore user interface.</span></span> <span data-ttu-id="6a9c5-106">使用者可以選擇這些還原點中的任何一個。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-106">The user can choose any of these restore points.</span></span> <span data-ttu-id="6a9c5-107">存取還原點封存的唯一方法是透過系統還原使用者介面和系統還原 API;這是為了保護資料的完整性，並防止使用者、應用程式或其他代理程式進行意外的變更。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-107">The only way to access this archive of restore points is through the System Restore user interface and the System Restore API; this is to protect data integrity and prevent accidental changes made by the user, applications, or other agents.</span></span>

<span data-ttu-id="6a9c5-108">若要還原系統，系統還原復原對受監視檔案進行的檔案變更，並在選取的還原點時重新擷取那個檔案狀態。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-108">To restore a system, System Restore undoes file changes made to monitored files, recapturing the file state at the time of the selected restore point.</span></span> <span data-ttu-id="6a9c5-109">然後，它會將目前的登錄取代為所選還原點所儲存的登錄。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-109">It then replaces the current registry with the one saved for the selected restore point.</span></span>

<span data-ttu-id="6a9c5-110">若要確保您的應用程式在還原之後具有所需的行為，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="6a9c5-110">To ensure that your application has the desired behavior after a restore, do the following:</span></span>

-   <span data-ttu-id="6a9c5-111">請勿將資訊儲存在登錄中，以防止使用者在系統還原時存取個人資料檔或應用程式。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-111">Do not store information in the registry that prevents user access to personal data files or applications on system restore.</span></span> <span data-ttu-id="6a9c5-112">否則，您必須提供一種機制，讓使用者可以下載並重新安裝應用程式，而不需要再次支付它們的費用。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-112">Otherwise, you must provide a mechanism by which the user can download and reinstall the applications without having to pay for them again.</span></span>
-   <span data-ttu-id="6a9c5-113">使用 [系統還原 API](system-restore-api.md) ，在安裝和卸載時建立有意義的還原點。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-113">Use the [System Restore API](system-restore-api.md) to create meaningful restore points at install and uninstall.</span></span>
-   <span data-ttu-id="6a9c5-114">在 Windows XP 中，要保護的主要應用程式二進位檔必須使用與 Filelist.xml 中使用的擴充功能一致的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-114">In Windows XP, the key application binaries to be protected must use extensions consistent with those used in Filelist.xml.</span></span> <span data-ttu-id="6a9c5-115">如需詳細資訊，請參閱 [監視](monitored-file-extensions.md)的副檔名。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-115">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span> <span data-ttu-id="6a9c5-116">Windows 7 和 Windows Vista 都不會使用此檔案。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-116">This file is not used by Windows 7 and Windows Vista.</span></span> <span data-ttu-id="6a9c5-117">請勿將受監視的擴充功能類型用於使用者可編輯的檔案。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-117">Do not use monitored extension types for user-editable files.</span></span> <span data-ttu-id="6a9c5-118">例如，如果您使用 .ini 副檔名來命名使用者的個人資料檔，則使用者可能會因為系統還原而遺失工作。</span><span class="sxs-lookup"><span data-stu-id="6a9c5-118">For example, if you name a user's personal data file using the extension .ini, the user may lose work as a result of a system restore.</span></span>

 

 




