---
description: 下列 VSS 錯誤和狀態資訊會寫入至應用程式事件記錄檔：
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: VSS 錯誤記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113181"
---
# <a name="vss-error-logging"></a><span data-ttu-id="49be8-103">VSS 錯誤記錄</span><span class="sxs-lookup"><span data-stu-id="49be8-103">VSS Error Logging</span></span>

<span data-ttu-id="49be8-104">下列 VSS 錯誤和狀態資訊會寫入至應用程式事件記錄檔：</span><span class="sxs-lookup"><span data-stu-id="49be8-104">The following VSS error and state information is written to the Application Event Log:</span></span>

-   <span data-ttu-id="49be8-105">使用 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面產生的要求者錯誤</span><span class="sxs-lookup"><span data-stu-id="49be8-105">Requester errors produced using the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
-   <span data-ttu-id="49be8-106">使用 [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) 類別產生的寫入器錯誤，包括覆寫方法</span><span class="sxs-lookup"><span data-stu-id="49be8-106">Writer errors produced in using the [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class, including overriding methods</span></span>
-   <span data-ttu-id="49be8-107">預設提供者產生的錯誤</span><span class="sxs-lookup"><span data-stu-id="49be8-107">Default-provider-generated errors</span></span>
-   <span data-ttu-id="49be8-108">協調提供者、寫入器和要求者活動所產生的 VSS 服務錯誤 (例如產生事件) </span><span class="sxs-lookup"><span data-stu-id="49be8-108">VSS service errors generated in coordinating provider, writer, and requester activity (such as the generation of events)</span></span>

<span data-ttu-id="49be8-109">這些錯誤可能有許多原因，包括協力廠商程式碼的程式設計錯誤或與 VSS 相關的設定錯誤。</span><span class="sxs-lookup"><span data-stu-id="49be8-109">These errors might have a number of causes, including a programming error in third-party code or VSS-related configuration errors.</span></span>

<span data-ttu-id="49be8-110">VSS 驅動程式和較低層級的執行功能會將錯誤寫入系統記錄檔。</span><span class="sxs-lookup"><span data-stu-id="49be8-110">VSS drivers and lower-level implementation functionality write errors to the System Log.</span></span> <span data-ttu-id="49be8-111">協力廠商軟體 (要求者、提供者、寫入器) 可以選擇應用程式記錄檔、系統記錄檔或兩者來寫入錯誤記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="49be8-111">Third-party software (requester, provider, writer) can choose the Application Log, the System Log, or both, to write error log entries.</span></span>

<span data-ttu-id="49be8-112">建議高階應用程式 (例如使用者模式程式碼) 使用應用程式記錄檔。</span><span class="sxs-lookup"><span data-stu-id="49be8-112">It is recommended that high-level applications (such as user-mode code) use the Application Log.</span></span> <span data-ttu-id="49be8-113">較低層級的應用程式（例如硬體介面和驅動程式）應該使用系統記錄。</span><span class="sxs-lookup"><span data-stu-id="49be8-113">Lower-level applications, such as hardware interfaces and drivers, should use the System Log.</span></span>

 

 



