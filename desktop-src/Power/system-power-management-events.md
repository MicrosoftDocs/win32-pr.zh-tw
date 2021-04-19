---
description: 系統電源管理事件是系統電源狀態的變更、裝置或系統的操作模式，或是電源設定的值。
ms.assetid: f73b072a-1f69-4e26-9712-dab428edca18
title: 系統電源管理事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab18fad9116cfff9e1cd35703e32a49e3b12c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971792"
---
# <a name="system-power-management-events"></a><span data-ttu-id="7b36d-103">系統電源管理事件</span><span class="sxs-lookup"><span data-stu-id="7b36d-103">System Power Management Events</span></span>

<span data-ttu-id="7b36d-104">系統電源管理事件是系統電源狀態的變更、裝置或系統的操作模式，或是電源設定的值。</span><span class="sxs-lookup"><span data-stu-id="7b36d-104">A system power management event is a change in the system power status, the operational mode of a device or the system, or the value of a power setting.</span></span> <span data-ttu-id="7b36d-105">因為這些事件可能會影響應用程式和可安裝驅動程式的操作，所以系統會廣播每個事件的通知，以通知所有應用程式和可安裝的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="7b36d-105">Because these events can affect the operation of applications and installable drivers, the system notifies all applications and installable drivers by broadcasting a notification for each event.</span></span> <span data-ttu-id="7b36d-106">應用程式和服務會使用 [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) 函數來註冊通知。</span><span class="sxs-lookup"><span data-stu-id="7b36d-106">Applications and services register for notifications by using the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function.</span></span> <span data-ttu-id="7b36d-107">通知是透過 [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) 訊息接收，其中包含電源管理事件和任何相關聯的事件特定資料。</span><span class="sxs-lookup"><span data-stu-id="7b36d-107">Notifications are received via the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message, which contains the power management event and any associated event-specific data.</span></span>

## <a name="system-power-status-events"></a><span data-ttu-id="7b36d-108">系統電源狀態事件</span><span class="sxs-lookup"><span data-stu-id="7b36d-108">System Power Status Events</span></span>

<span data-ttu-id="7b36d-109">電源供應器或系統電池狀態發生變更時，就會發生 *系統電源狀態事件* 。</span><span class="sxs-lookup"><span data-stu-id="7b36d-109">A *system power status event* occurs when there is a change in the power supply or in the system battery status.</span></span> <span data-ttu-id="7b36d-110">例如，每當使用者從電池切換至 AC 電源時，系統就會廣播 [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) 事件，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="7b36d-110">For example, the system broadcasts a [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) event whenever the user switches from battery to AC power or vice versa.</span></span> <span data-ttu-id="7b36d-111">當剩餘電池的電力下滑至使用者所指定的臨界值之下，或是如果電池的電力由指定百分比來變更時，系統也會廣播這個事件。</span><span class="sxs-lookup"><span data-stu-id="7b36d-111">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

## <a name="operational-mode-events"></a><span data-ttu-id="7b36d-112">操作模式事件</span><span class="sxs-lookup"><span data-stu-id="7b36d-112">Operational Mode Events</span></span>

<span data-ttu-id="7b36d-113">當耗電量有所變更時，例如系統因為閒置而切換到睡眠狀態，或是使用者手動讓系統進入睡眠狀態時，就會發生 *操作模式事件* 。</span><span class="sxs-lookup"><span data-stu-id="7b36d-113">An *operational mode event* occurs when there is a change in power consumption, such as the system switching to a sleep state due to inactivity or the user manually putting the system to sleep.</span></span> <span data-ttu-id="7b36d-114">系統會在進行耗電量的變更之前，先將這些變更的相關事件廣播。</span><span class="sxs-lookup"><span data-stu-id="7b36d-114">The system broadcasts events about these changes before the change in power consumption is made.</span></span> <span data-ttu-id="7b36d-115">例如，如果系統判斷它處於閒置狀態，它就會廣播 [PBT \_ APMSUSPEND](pbt-apmsuspend.md) 事件，通知應用程式和驅動程式即將暫停操作和睡眠，以節省電力。</span><span class="sxs-lookup"><span data-stu-id="7b36d-115">For example, if the system determines that it is idle, it broadcasts a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event that notifies applications and drivers that it is about to suspend operation and sleep to conserve power.</span></span> <span data-ttu-id="7b36d-116">應用程式和驅動程式可以藉由關閉檔案並儲存資料來準備睡眠，以避免潛在的資料遺失。</span><span class="sxs-lookup"><span data-stu-id="7b36d-116">Applications and drivers can prepare for sleep by closing files and saving data to avoid potential data loss.</span></span>

<span data-ttu-id="7b36d-117">當系統執行 *重要* 的暫止時，系統會立即進入睡眠狀態，因為有重大的狀況，例如嚴重的電池警報。</span><span class="sxs-lookup"><span data-stu-id="7b36d-117">When the system carries out a *critical suspension*, the system is immediately put to sleep due to a critical condition such as a critical battery alarm.</span></span> <span data-ttu-id="7b36d-118">相較于一般睡眠轉換，系統不會在執行重大暫停之前通知應用程式和驅動程式。</span><span class="sxs-lookup"><span data-stu-id="7b36d-118">In contrast to a normal sleep transition, the system does not notify applications and drivers before carrying out a critical suspension.</span></span> <span data-ttu-id="7b36d-119">因此，應用程式必須準備好處理重要的暫停。</span><span class="sxs-lookup"><span data-stu-id="7b36d-119">Therefore, applications must be prepared to handle critical suspensions.</span></span>

<span data-ttu-id="7b36d-120">當系統作業在暫止之後還原時，系統會通知所有的應用程式和驅動程式。</span><span class="sxs-lookup"><span data-stu-id="7b36d-120">When system operation is restored after having been suspended, the system notifies all applications and drivers.</span></span> <span data-ttu-id="7b36d-121">它也會指出系統是否正在從重大暫停中繼續，讓應用程式或驅動程式可以採取適當的步驟來還原其資料，並繼續操作。</span><span class="sxs-lookup"><span data-stu-id="7b36d-121">It also indicates whether the system is resuming from a critical suspension so the application or driver can take appropriate steps to restore its data and continue operation.</span></span>

<span data-ttu-id="7b36d-122">應用程式應該在不需要使用者介入的情況下，每次嘗試處理轉換進入睡眠狀態，因為使用者可能無法回應。</span><span class="sxs-lookup"><span data-stu-id="7b36d-122">Applications should make every attempt to handle the transition to the sleep state without any user intervention because it may not be possible for the user to respond.</span></span> <span data-ttu-id="7b36d-123">例如，筆記本電腦上的蓋可能會關閉。</span><span class="sxs-lookup"><span data-stu-id="7b36d-123">For example, the lid on the notebook computer may be closed.</span></span> <span data-ttu-id="7b36d-124">當應用程式收到系統即將進入睡眠狀態的通知時，它應該會快速執行任何必要的作業，並傳回訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="7b36d-124">When an application receives notification that the system is about to enter sleep, it should perform any necessary operations quickly and return out of the message loop.</span></span> <span data-ttu-id="7b36d-125">系統在處理此訊息前，每個應用程式最多允許2秒的時間。</span><span class="sxs-lookup"><span data-stu-id="7b36d-125">The system allows for a maximum of two seconds per application when handling this message before timing out.</span></span>

## <a name="power-setting-change-events"></a><span data-ttu-id="7b36d-126">電源設定變更事件</span><span class="sxs-lookup"><span data-stu-id="7b36d-126">Power Setting Change Events</span></span>

<span data-ttu-id="7b36d-127">當電源設定的值有所變更時，就會發生電源設定變更事件。</span><span class="sxs-lookup"><span data-stu-id="7b36d-127">A power setting change event occurs when there is a change in the value of a power setting.</span></span> <span data-ttu-id="7b36d-128">例如，使用者在主控台的電源選項應用程式中，將電源計劃從高效能變更為平衡。</span><span class="sxs-lookup"><span data-stu-id="7b36d-128">For example, the user changes the power plan from High Performance to Balanced in the Power Options application in Control Panel.</span></span> <span data-ttu-id="7b36d-129">在此情況下，系統會廣播指出電源計劃已變更的事件。</span><span class="sxs-lookup"><span data-stu-id="7b36d-129">In this case, the system would broadcast an event that indicates that the power plan has changed.</span></span> <span data-ttu-id="7b36d-130">此事件包含電源設定的新值。</span><span class="sxs-lookup"><span data-stu-id="7b36d-130">This event includes the new value for the power setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b36d-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b36d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b36d-132">關於電源管理</span><span class="sxs-lookup"><span data-stu-id="7b36d-132">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



