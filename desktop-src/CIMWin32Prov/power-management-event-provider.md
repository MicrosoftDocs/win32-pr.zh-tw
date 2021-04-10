---
description: 電源管理提供者可讓 WMI 建立 Windows 電源管理通訊協定的模型。
ms.assetid: 18ff116b-22a8-4ee3-b2fd-427eb8643e6b
ms.tgt_platform: multiple
title: 電源管理事件提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb515c072161a9973d0f5554a1e0a3118674ed6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111641"
---
# <a name="power-management-event-provider"></a><span data-ttu-id="3db4c-103">電源管理事件提供者</span><span class="sxs-lookup"><span data-stu-id="3db4c-103">Power Management Event Provider</span></span>

<span data-ttu-id="3db4c-104">電源管理提供者可讓 WMI 建立 Windows 電源管理通訊協定的模型。</span><span class="sxs-lookup"><span data-stu-id="3db4c-104">The Power Management provider allows WMI to model the Windows power management protocols.</span></span> <span data-ttu-id="3db4c-105">作為事件提供者，電源管理提供者會將資訊提供給 [**Win32 \_ PowerManagementEvent**](win32-powermanagementevent.md) 類別，以描述電源狀態變更所造成的電源管理事件。</span><span class="sxs-lookup"><span data-stu-id="3db4c-105">As an event provider, the Power Management provider supplies information to the [**Win32\_PowerManagementEvent**](win32-powermanagementevent.md) class to describe power management events that result from power state changes.</span></span> <span data-ttu-id="3db4c-106">這些狀態變更與 advanced 電源管理 (APM) 或 advanced configuration and power interface (ACPI) 系統管理通訊協定相關聯。</span><span class="sxs-lookup"><span data-stu-id="3db4c-106">These state changes are associated with either the advanced power management (APM) or the advanced configuration and power interface (ACPI) system management protocols.</span></span> <span data-ttu-id="3db4c-107">[**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)實例名稱是「MS \_ 電源 \_ 管理 \_ 事件 \_ 提供者」。</span><span class="sxs-lookup"><span data-stu-id="3db4c-107">The [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider) instance name is "MS\_Power\_Management\_Event\_Provider".</span></span>

## <a name="related-topics"></a><span data-ttu-id="3db4c-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="3db4c-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3db4c-109">WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="3db4c-109">WMI Providers</span></span>](/windows/desktop/WmiSdk/wmi-providers)
</dt> </dl>

 

 
