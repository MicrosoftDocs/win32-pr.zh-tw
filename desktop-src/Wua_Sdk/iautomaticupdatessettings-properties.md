---
description: IAutomaticUpdatesSettings 介面會定義下列屬性。
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: IAutomaticUpdatesSettings 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943488"
---
# <a name="iautomaticupdatessettings-properties"></a><span data-ttu-id="5e16e-103">IAutomaticUpdatesSettings 屬性</span><span class="sxs-lookup"><span data-stu-id="5e16e-103">IAutomaticUpdatesSettings Properties</span></span>

<span data-ttu-id="5e16e-104">[**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="5e16e-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following properties.</span></span>



| <span data-ttu-id="5e16e-105">屬性</span><span class="sxs-lookup"><span data-stu-id="5e16e-105">Property</span></span>                                                                                 | <span data-ttu-id="5e16e-106">描述</span><span class="sxs-lookup"><span data-stu-id="5e16e-106">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e16e-107">**NotificationLevel**</span><span class="sxs-lookup"><span data-stu-id="5e16e-107">**NotificationLevel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | <span data-ttu-id="5e16e-108">取得和設定如何通知使用者有關自動更新事件的通知。</span><span class="sxs-lookup"><span data-stu-id="5e16e-108">Gets and sets how users are notified about Automatic Update events.</span></span>                              |
| [<span data-ttu-id="5e16e-109">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="5e16e-109">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | <span data-ttu-id="5e16e-110">取得布林值，指出自動更新設定是否為唯讀。</span><span class="sxs-lookup"><span data-stu-id="5e16e-110">Gets a Boolean value that indicates whether the Automatic Update settings are read-only.</span></span>         |
| [<span data-ttu-id="5e16e-111">**必要**</span><span class="sxs-lookup"><span data-stu-id="5e16e-111">**Required**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | <span data-ttu-id="5e16e-112">取得布林值，指出群組原則是否需要自動更新服務。</span><span class="sxs-lookup"><span data-stu-id="5e16e-112">Gets a Boolean value that indicates whether Group Policy requires the Automatic Updates service.</span></span> |
| [<span data-ttu-id="5e16e-113">**ScheduledInstallationDay**</span><span class="sxs-lookup"><span data-stu-id="5e16e-113">**ScheduledInstallationDay**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | <span data-ttu-id="5e16e-114">取得和設定自動更新安裝或卸載更新的星期幾。</span><span class="sxs-lookup"><span data-stu-id="5e16e-114">Gets and sets the days of the week on which Automatic Updates installs or uninstalls updates.</span></span>    |
| [<span data-ttu-id="5e16e-115">**ScheduledInstallationTime**</span><span class="sxs-lookup"><span data-stu-id="5e16e-115">**ScheduledInstallationTime**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | <span data-ttu-id="5e16e-116">取得和設定自動更新安裝或卸載更新的時間。</span><span class="sxs-lookup"><span data-stu-id="5e16e-116">Gets and sets the time at which Automatic Updates installs or uninstalls updates.</span></span>                |



 

> [!Note]  
> <span data-ttu-id="5e16e-117">Windows 8、Windows 8.1、Windows Server 2012 和 Windows Server 2012 R2 僅提供有限的 [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) 和 [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)支援。</span><span class="sxs-lookup"><span data-stu-id="5e16e-117">Windows 8, Windows 8.1, Windows Server 2012, and Windows Server 2012 R2 provide only limited support for [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) and [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="5e16e-118">如果電腦已透過群組原則設定為使用排程的安裝日期和時間，則 **ScheduledInstallationDay** 和 **ScheduledInstallationTime** 屬性會傳回此排程的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="5e16e-118">If the computer has been configured through Group Policy to use a scheduled installation day and time, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return this scheduled day and time.</span></span> <span data-ttu-id="5e16e-119">如果電腦尚未透過群組原則設定， **ScheduledInstallationDay** 和 **ScheduledInstallationTime** 屬性會傳回預設值和不可靠的值。</span><span class="sxs-lookup"><span data-stu-id="5e16e-119">If the computer hasn't been configured through Group Policy in this way, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return default and unreliable values.</span></span> <span data-ttu-id="5e16e-120">如果您嘗試修改這些作業系統上的排程安裝日期和時間， **ScheduledInstallationDay** 和 **ScheduledInstallationTime** 似乎會成功，但是沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="5e16e-120">If you try to modify the scheduled installation day and time on these operating systems, **ScheduledInstallationDay** and **ScheduledInstallationTime** appear to succeed but have no effect.</span></span>

 

 

 



