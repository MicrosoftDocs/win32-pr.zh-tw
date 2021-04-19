---
description: 在系統開機期間，SCM 會啟動所有自動啟動服務及其相依的服務。 例如，如果自動啟動服務相依于需求啟動服務，則也會自動啟動「需求啟動」服務。
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: 自動啟動服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970390"
---
# <a name="automatically-starting-services"></a><span data-ttu-id="0642e-104">自動啟動服務</span><span class="sxs-lookup"><span data-stu-id="0642e-104">Automatically Starting Services</span></span>

<span data-ttu-id="0642e-105">在系統開機期間，SCM 會啟動所有自動啟動服務及其相依的服務。</span><span class="sxs-lookup"><span data-stu-id="0642e-105">During system boot, the SCM starts all auto-start services and the services on which they depend.</span></span> <span data-ttu-id="0642e-106">例如，如果自動啟動服務相依于需求啟動服務，則也會自動啟動「需求啟動」服務。</span><span class="sxs-lookup"><span data-stu-id="0642e-106">For example, if an auto-start service depends on a demand-start service, the demand-start service is also started automatically.</span></span>

<span data-ttu-id="0642e-107">載入順序取決於下列各項：</span><span class="sxs-lookup"><span data-stu-id="0642e-107">The load order is determined by the following:</span></span>

1.  <span data-ttu-id="0642e-108">群組在 [載入順序群組] 清單中的順序。</span><span class="sxs-lookup"><span data-stu-id="0642e-108">The order of groups in the load ordering group list.</span></span> <span data-ttu-id="0642e-109">這項資訊會儲存在下列登錄機碼的 **ServiceGroupOrder** 值中：</span><span class="sxs-lookup"><span data-stu-id="0642e-109">This information is stored in the **ServiceGroupOrder** value in the following registry key:</span></span>

    <span data-ttu-id="0642e-110">**HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 控制項**</span><span class="sxs-lookup"><span data-stu-id="0642e-110">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

    <span data-ttu-id="0642e-111">若要指定服務的載入順序群組，請使用 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)或 [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)函數的 *lpLoadOrderGroup* 參數。</span><span class="sxs-lookup"><span data-stu-id="0642e-111">To specify the load ordering group for a service, use the *lpLoadOrderGroup* parameter of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) or [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) function.</span></span>

2.  <span data-ttu-id="0642e-112">在標記順序向量中指定之群組內的服務順序。</span><span class="sxs-lookup"><span data-stu-id="0642e-112">The order of services within a group specified in the tags order vector.</span></span> <span data-ttu-id="0642e-113">這項資訊會儲存在下列登錄機碼的 **GroupOrderList** 值中：</span><span class="sxs-lookup"><span data-stu-id="0642e-113">This information is stored in the **GroupOrderList** value in the following registry key:</span></span>

    <span data-ttu-id="0642e-114">**HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 控制項**</span><span class="sxs-lookup"><span data-stu-id="0642e-114">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control**</span></span>

3.  <span data-ttu-id="0642e-115">針對每項服務列出的相依性。</span><span class="sxs-lookup"><span data-stu-id="0642e-115">The dependencies listed for each service.</span></span>

<span data-ttu-id="0642e-116">當開機完成時，系統會執行下列登錄機碼的 **BootVerificationProgram** 值所指定的開機驗證程式： **HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 控制項**。</span><span class="sxs-lookup"><span data-stu-id="0642e-116">When the boot is complete, the system executes the boot verification program specified by the **BootVerificationProgram** value of the following registry key: **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control**.</span></span>

<span data-ttu-id="0642e-117">依預設，未設定此值。</span><span class="sxs-lookup"><span data-stu-id="0642e-117">By default, this value is not set.</span></span> <span data-ttu-id="0642e-118">系統只會報告第一位使用者登入之後開機是否成功。</span><span class="sxs-lookup"><span data-stu-id="0642e-118">The system simply reports that the boot was successful after the first user has logged on.</span></span> <span data-ttu-id="0642e-119">您可以提供開機驗證程式來檢查系統是否有問題，並使用 [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) 功能將開機狀態回報給 SCM。</span><span class="sxs-lookup"><span data-stu-id="0642e-119">You can supply a boot verification program that checks the system for problems and reports the boot status to the SCM using the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>

<span data-ttu-id="0642e-120">成功開機之後，系統會將資料庫的複本儲存在最後已知良好的 (LKG) 設定中。</span><span class="sxs-lookup"><span data-stu-id="0642e-120">After a successful boot, the system saves a clone of the database in the last-known-good (LKG) configuration.</span></span> <span data-ttu-id="0642e-121">如果對使用中資料庫所做的變更導致系統重新開機失敗，系統就可以還原此資料庫複本。</span><span class="sxs-lookup"><span data-stu-id="0642e-121">The system can restore this copy of the database if changes made to the active database cause the system reboot to fail.</span></span> <span data-ttu-id="0642e-122">以下是此資料庫的登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="0642e-122">The following is the registry key for this database:</span></span>

<span data-ttu-id="0642e-123">**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ ControlSet *XXX* \\ Services**</span><span class="sxs-lookup"><span data-stu-id="0642e-123">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\ControlSet *XXX*\\Services**</span></span>

<span data-ttu-id="0642e-124">其中 *XXX* 是儲存在下列登錄值中的值： **HKEY \_ LOCAL \_ MACHINE \\ System \\ Select \\ LastKnownGood**。</span><span class="sxs-lookup"><span data-stu-id="0642e-124">where *XXX* is the value saved in the following registry value: **HKEY\_LOCAL\_MACHINE\\System\\Select\\LastKnownGood**.</span></span>

<span data-ttu-id="0642e-125">如果自動啟動服務的服務 \_ 錯誤 \_ 嚴重錯誤控制層級無法啟動，SCM 會使用 LKG 設定來重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="0642e-125">If an auto-start service with a SERVICE\_ERROR\_CRITICAL error control level fails to start, the SCM reboots the computer using the LKG configuration.</span></span> <span data-ttu-id="0642e-126">如果 LKG 設定已在使用中，則開機會失敗。</span><span class="sxs-lookup"><span data-stu-id="0642e-126">If the LKG configuration is already being used, the boot fails.</span></span>

<span data-ttu-id="0642e-127">自動啟動服務可以設定為延遲的自動啟動服務，方法是呼叫 [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) 函式與服務設定 \_ 延遲的 \_ \_ 自動 \_ 啟動 \_ 資訊。</span><span class="sxs-lookup"><span data-stu-id="0642e-127">An auto-start service can be configured as a delayed auto-start service by calling the [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function with SERVICE\_CONFIG\_DELAYED\_AUTO\_START\_INFO.</span></span> <span data-ttu-id="0642e-128">此變更會在下一次系統開機之後生效。</span><span class="sxs-lookup"><span data-stu-id="0642e-128">This change takes effect after the next system boot.</span></span> <span data-ttu-id="0642e-129">如需詳細資訊，請參閱 [**服務 \_ 延遲的 \_ 自動 \_ 啟動 \_ 資訊**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info)。</span><span class="sxs-lookup"><span data-stu-id="0642e-129">For more information, see [**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).</span></span>

 

 



