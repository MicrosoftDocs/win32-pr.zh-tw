---
description: 裝置電源 API 可讓您輕鬆地判斷哪些裝置能夠從睡眠狀態喚醒系統，以及哪些睡眠狀態是這些裝置支援喚醒的裝置。 如需睡眠狀態的詳細資訊，請參閱系統電源狀態。
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: 裝置電源管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944242"
---
# <a name="device-power-management"></a><span data-ttu-id="59d2a-104">裝置電源管理</span><span class="sxs-lookup"><span data-stu-id="59d2a-104">Device Power Management</span></span>

<span data-ttu-id="59d2a-105">裝置電源 API 可讓您輕鬆地判斷哪些裝置能夠從睡眠狀態喚醒系統，以及哪些睡眠狀態是這些裝置支援喚醒的裝置。</span><span class="sxs-lookup"><span data-stu-id="59d2a-105">The Device Power API makes it easy to determine which devices are able to wake the system from a sleep state, and which sleep states those devices support waking from.</span></span> <span data-ttu-id="59d2a-106">如需睡眠狀態的詳細資訊，請參閱 [系統電源狀態](system-power-states.md)。</span><span class="sxs-lookup"><span data-stu-id="59d2a-106">For more information about sleep states, see [System Power States](system-power-states.md).</span></span>

<span data-ttu-id="59d2a-107">您可以使用 [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) 函式，在裝置清單中搜尋符合指定準則的裝置。</span><span class="sxs-lookup"><span data-stu-id="59d2a-107">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function can be used to search the device list for devices that match specified criteria.</span></span> <span data-ttu-id="59d2a-108">準則可能包括裝置支援系統狀態的能力，或從該狀態喚醒。</span><span class="sxs-lookup"><span data-stu-id="59d2a-108">The criteria may include the device's ability to support a system state, or wake from that state.</span></span> <span data-ttu-id="59d2a-109">目前支援的旗標可在 WinNT 和 DevPower 中找到。</span><span class="sxs-lookup"><span data-stu-id="59d2a-109">Currently supported flags can be found in WinNT.h and DevPower.h.</span></span>

<span data-ttu-id="59d2a-110">[**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate)函式會啟用或停用指定的裝置，使其無法從睡眠狀態喚醒系統。</span><span class="sxs-lookup"><span data-stu-id="59d2a-110">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function enables or disables a specified device from waking the system from a sleep state.</span></span>

<span data-ttu-id="59d2a-111">裝置電源 API 可讓開發人員藉由提供使用者有關系統正在執行之工作的詳細資訊，以及對系統中的裝置進行更多的控制，來創造更好的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="59d2a-111">The Device Power API allows developers to create a better user experience by giving the user more information about what the system is doing, and more control over the devices in the system.</span></span> <span data-ttu-id="59d2a-112">裝置電源在電力耗用量很重要的情況下很有用，例如在以電池執行的可攜式裝置中。</span><span class="sxs-lookup"><span data-stu-id="59d2a-112">Device Power is useful in situations where power consumption is critical, such as in portable devices running on batteries.</span></span> <span data-ttu-id="59d2a-113">例如，在桌上型電腦中使用的電源管理配置可能不是膝上型電腦的最佳配置，因此使用者可能會想要停用某些裝置，使其無法喚醒系統。</span><span class="sxs-lookup"><span data-stu-id="59d2a-113">For example, the power management scheme used in a desktop computer may not be the optimal scheme for a laptop computer, so the user may want to disable certain devices from waking the system.</span></span> <span data-ttu-id="59d2a-114">這可以節省能源，因為當系統處於睡眠模式時，已停用的裝置將不會繪製電源。</span><span class="sxs-lookup"><span data-stu-id="59d2a-114">This can conserve energy because the disabled devices will not draw power while the system is in sleep mode.</span></span>

<span data-ttu-id="59d2a-115">如需範例，請參閱 [使用裝置電源 API](using-the-device-power-api.md)。</span><span class="sxs-lookup"><span data-stu-id="59d2a-115">For an example, see [Using the Device Power API](using-the-device-power-api.md).</span></span>

 

 



