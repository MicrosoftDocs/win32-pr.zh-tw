---
description: Windows 10 可協助您的應用程式在行動裝置上執行時，將耗電量優化。
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: 電源管理的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996733"
---
# <a name="whats-new-in-power-management"></a><span data-ttu-id="180db-103">電源管理的新功能</span><span class="sxs-lookup"><span data-stu-id="180db-103">What's New in Power Management</span></span>

<span data-ttu-id="180db-104">Windows 10 可協助您的應用程式在行動裝置上執行時，將耗電量優化。</span><span class="sxs-lookup"><span data-stu-id="180db-104">Windows 10 helps your application optimize power consumption when it's running on a mobile device.</span></span>

## <a name="battery-saver"></a><span data-ttu-id="180db-105">省電模式</span><span class="sxs-lookup"><span data-stu-id="180db-105">Battery saver</span></span>

<span data-ttu-id="180db-106">在此版本中，當省電模式開啟或關閉時，您的應用程式可以收到通知。</span><span class="sxs-lookup"><span data-stu-id="180db-106">In this release, your application can be notified when battery saver is turned on or off.</span></span> <span data-ttu-id="180db-107">藉由回應不斷變化的電源，您的應用程式可以與省電模式協同合作，以節省能源並協助延長電池壽命。</span><span class="sxs-lookup"><span data-stu-id="180db-107">By responding to changing power conditions, your application can work in concert with battery saver to save energy and help extend battery life.</span></span> <span data-ttu-id="180db-108">如需有關省電模式的一般資訊，請參閱 [硬體元件指導方針中的省電模式 () ](/windows-hardware/design/component-guidelines/battery-saver)。</span><span class="sxs-lookup"><span data-stu-id="180db-108">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="180db-109">[**GUID \_省 \_ 電 \_ 狀態**](power-setting-guids.md) ：當省電模式開啟或關閉時，請使用這個新的 GUID 搭配 [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) 函式來通知。</span><span class="sxs-lookup"><span data-stu-id="180db-109">[**GUID\_POWER\_SAVING\_STATUS**](power-setting-guids.md) : Use this new GUID with the [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) function to be notified when battery saver is turned on or off.</span></span>

-   <span data-ttu-id="180db-110">[**系統 \_電源 \_ 狀態**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) ：已更新此結構以支援省電模式。</span><span class="sxs-lookup"><span data-stu-id="180db-110">[**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : This structure has been updated to support battery saver.</span></span> <span data-ttu-id="180db-111">第四個成員 **SystemStatusFlag** (先前命名為 **Reserved1**) ，現在指出省電模式是否已參與。</span><span class="sxs-lookup"><span data-stu-id="180db-111">The fourth member, **SystemStatusFlag** (previously named **Reserved1**), now indicates if battery saver is engaged or not.</span></span> <span data-ttu-id="180db-112">您可以使用 [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) 函式來取得此結構的指標。</span><span class="sxs-lookup"><span data-stu-id="180db-112">Use the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve a pointer to this structure.</span></span>

 

 
