---
description: 下列通知適用于 SetupInstallFile、SetupInstallFileEx 和 SetupInstallFromInfSection 函數。 如需有關通知格式和使用的詳細資訊，請參閱通知。
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: INF 檔案通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944355"
---
# <a name="inf-file-notifications"></a><span data-ttu-id="b8552-104">INF 檔案通知</span><span class="sxs-lookup"><span data-stu-id="b8552-104">INF File Notifications</span></span>

<span data-ttu-id="b8552-105">下列通知適用于 [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)、 [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)和 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) 函數。</span><span class="sxs-lookup"><span data-stu-id="b8552-105">The following notifications are used with the [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) functions.</span></span> <span data-ttu-id="b8552-106">如需有關通知格式和使用的詳細資訊，請參閱 [通知](notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="b8552-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="b8552-107">通知</span><span class="sxs-lookup"><span data-stu-id="b8552-107">Notification</span></span>                                                      | <span data-ttu-id="b8552-108">Description</span><span class="sxs-lookup"><span data-stu-id="b8552-108">Description</span></span>                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8552-109">**SPFILENOTIFY \_ FILEOPDELAYED**</span><span class="sxs-lookup"><span data-stu-id="b8552-109">**SPFILENOTIFY\_FILEOPDELAYED**</span></span>](spfilenotify-fileopdelayed.md) | <span data-ttu-id="b8552-110">檔案正在使用中，而目前的操作會延遲到系統重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="b8552-110">The file is in use, and the current operation is delayed until the system is rebooted.</span></span> |
| [<span data-ttu-id="b8552-111">**SPFILENOTIFY \_ LANGMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="b8552-111">**SPFILENOTIFY\_LANGMISMATCH**</span></span>](spfilenotify-langmismatch.md)   | <span data-ttu-id="b8552-112">目前檔案的語言與系統語言不符。</span><span class="sxs-lookup"><span data-stu-id="b8552-112">The language of the current file does not match the system language.</span></span>                   |
| [<span data-ttu-id="b8552-113">**SPFILENOTIFY \_ TARGETEXISTS**</span><span class="sxs-lookup"><span data-stu-id="b8552-113">**SPFILENOTIFY\_TARGETEXISTS**</span></span>](spfilenotify-targetexists.md)   | <span data-ttu-id="b8552-114">目標上已有指定檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="b8552-114">A copy of the specified file already exists on the target.</span></span>                             |
| [<span data-ttu-id="b8552-115">**SPFILENOTIFY \_ TARGETNEWER**</span><span class="sxs-lookup"><span data-stu-id="b8552-115">**SPFILENOTIFY\_TARGETNEWER**</span></span>](spfilenotify-targetnewer.md)     | <span data-ttu-id="b8552-116">目標上有較新版本的指定檔案。</span><span class="sxs-lookup"><span data-stu-id="b8552-116">A newer version of the specified file exists on the target.</span></span>                            |



 

> [!Note]  
> <span data-ttu-id="b8552-117">因為 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) 會建立並認可內部檔案佇列，所以它也會使用檔案 [佇列通知](file-queue-notifications.md)。</span><span class="sxs-lookup"><span data-stu-id="b8552-117">Because [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) creates and commits an internal file queue, it also uses the [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 

 



