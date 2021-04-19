---
description: 電池可提供可攜式電腦的電源，以及在不斷電供應系統供應 (UPS) 上執行的電腦。
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: 電池資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f9838a2a95db037b9655f116f07e3cf2e072d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999894"
---
# <a name="battery-information"></a><span data-ttu-id="fb6e2-103">電池資訊</span><span class="sxs-lookup"><span data-stu-id="fb6e2-103">Battery Information</span></span>

<span data-ttu-id="fb6e2-104">電池可提供可攜式電腦的電源，以及在不斷電供應系統供應 (UPS) 上執行的電腦。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-104">Batteries can provide power for portable computers and computers running on an uninterruptible power supply (UPS).</span></span> <span data-ttu-id="fb6e2-105">在這些電腦上，作業系統會提供電池狀態的相關資訊，讓應用程式可以為使用者提供實用的功能。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-105">On these computers, the operating system provides information on the state of the battery so applications can provide useful functions for the user.</span></span> <span data-ttu-id="fb6e2-106"> (不支援某些較舊的非標準電池系統和 Ups。 ) </span><span class="sxs-lookup"><span data-stu-id="fb6e2-106">(Some older nonstandard battery systems and UPSs are not supported.)</span></span>

<span data-ttu-id="fb6e2-107">請注意，此總覽假設您已經熟悉 [裝置管理](/windows/desktop/DevIO/device-management)。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-107">Note that this overview assumes you are familiar with [device management](/windows/desktop/DevIO/device-management).</span></span>

<span data-ttu-id="fb6e2-108">若要取得電池狀態的相關資訊，請使用 [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) 函式，此函式會傳回系統中所有電源來源的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-108">To obtain information about the battery status, use the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function, which returns general information about all power sources in the system.</span></span> <span data-ttu-id="fb6e2-109">您應該盡可能使用 **GetSystemPowerStatus** 。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-109">You should use **GetSystemPowerStatus** whenever possible.</span></span>

<span data-ttu-id="fb6e2-110">不過，在某些情況下，需要每個個別電池的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-110">In some cases, however, detailed information about each individual battery is necessary.</span></span> <span data-ttu-id="fb6e2-111">基於這個目的，每個電池裝置都會公開一個 IOCTL 介面。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-111">For this purpose, each battery device exposes an IOCTL interface.</span></span> <span data-ttu-id="fb6e2-112">下列 IOCTL 作業會使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數來執行：</span><span class="sxs-lookup"><span data-stu-id="fb6e2-112">The following IOCTL operations are performed using the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function:</span></span>

<dl>

[<span data-ttu-id="fb6e2-113">**IOCTL \_ 電池 \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="fb6e2-113">**IOCTL\_BATTERY\_QUERY\_INFORMATION**</span></span>](ioctl-battery-query-information.md)  
[<span data-ttu-id="fb6e2-114">**IOCTL \_ 電池 \_ 查詢 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="fb6e2-114">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)  
[<span data-ttu-id="fb6e2-115">**IOCTL \_ 電池 \_ 查詢 \_ 標記**</span><span class="sxs-lookup"><span data-stu-id="fb6e2-115">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)  
[<span data-ttu-id="fb6e2-116">**IOCTL \_ 電池 \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="fb6e2-116">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)  
</dl>

<span data-ttu-id="fb6e2-117">若要使用此介面，應用程式必須遵循幾個步驟。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-117">To use this interface, an application must follow several steps.</span></span> <span data-ttu-id="fb6e2-118">首先，它必須使用安裝程式常式來列舉具有電池類別介面的所有裝置。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-118">First, it must use setup routines to enumerate all devices that have a battery class interface.</span></span> <span data-ttu-id="fb6e2-119">請注意，這些裝置代表電池埠，而不是系統中的實際電池。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-119">Note that these devices represent the battery ports, not actual batteries present in the system.</span></span> <span data-ttu-id="fb6e2-120">然後，應用程式必須開啟每個裝置的控制碼，讓它可以使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式將要求傳送至裝置，然後取得所插入之任何電池的標記。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-120">The application must then open a handle to each device so it can use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function to send requests to the device, and then acquire tags for any batteries that are inserted.</span></span> <span data-ttu-id="fb6e2-121">完成這些步驟之後，應用程式就可以將查詢傳送到每部電池裝置。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-121">After completing these steps, the application can send queries to each battery device.</span></span>

## <a name="battery-tags"></a><span data-ttu-id="fb6e2-122">電池標記</span><span class="sxs-lookup"><span data-stu-id="fb6e2-122">Battery Tags</span></span>

<span data-ttu-id="fb6e2-123">因為每個電池裝置都代表可插入電池的位置，所以必須有一種方式來判斷電池何時移除、更換、更換或變更為其他任何方式。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-123">Because each battery device represents a slot into which a battery can be inserted, there must be a way to determine when the battery is removed and reinserted, replaced, or changed in any other way.</span></span> <span data-ttu-id="fb6e2-124">若要這樣做，特定位置中的每個電池都會被指派一個標記。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-124">To do this, each battery in a particular slot is assigned a tag.</span></span> <span data-ttu-id="fb6e2-125">所有查詢都必須使用這個標記來取得資訊。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-125">This tag must be used for all queries for information.</span></span> <span data-ttu-id="fb6e2-126">如果應用程式所提供的標記與電池不符，則查詢會失敗，並向應用程式指出電池已變更。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-126">If the tag provided by the application does not match the battery, the query fails, indicating to the application that the battery has changed in some way.</span></span> <span data-ttu-id="fb6e2-127">若要成功完成查詢，需要新的電池標記。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-127">To successfully complete the query, a new battery tag is required.</span></span> <span data-ttu-id="fb6e2-128">使用 [**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md) 作業取得標記。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-128">Acquire the tag using the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation.</span></span> <span data-ttu-id="fb6e2-129">如果該位置中有電池，則傳回的標記可傳遞給任何其他電池 IOCTLs 來執行其他功能。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-129">If a battery is present in that slot, the tag returned can be passed to any of the other battery IOCTLs to perform other functions.</span></span> <span data-ttu-id="fb6e2-130">在多電池系統上，每個電池裝置 (位置) 會獨立發出電池標籤，因此來自兩個不同裝置的標籤有時可能相同。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-130">On a multi-battery system, each battery device (slot) issues battery tags independently, so the tag from two separate devices could at times be identical.</span></span>

<span data-ttu-id="fb6e2-131">電池標籤的變更不一定表示已移除並重新插入或更換電池。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-131">A change in the battery tag does not necessarily mean that the battery was removed and reinserted or replaced.</span></span> <span data-ttu-id="fb6e2-132">如果任何通常是靜態的資料有變更，就可以產生新的標記。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-132">A new tag can be generated if there is a change in any of the data that would normally be static.</span></span> <span data-ttu-id="fb6e2-133">例如，當電池充電完成時，最後一次完全收費的容量可能已變更。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-133">For example, when a battery is done charging, the last fully charged capacity may have changed.</span></span> <span data-ttu-id="fb6e2-134">如果電池通訊暫時遺失，或從 BIOS 發出不當的通知，標記也會變更。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-134">The tag can also change if battery communication was temporarily lost or if there was an improper notification from the BIOS.</span></span> <span data-ttu-id="fb6e2-135">在某些系統上，每次 AC 狀態變更時，可能會更新電池標記。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-135">On some systems, the battery tag may be updated whenever the AC status changes.</span></span> <span data-ttu-id="fb6e2-136">此行為是因為電池系統的特性而不常見。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-136">This behavior is due to a characteristic of the battery system and isn't common.</span></span>

<span data-ttu-id="fb6e2-137">只要更新電池標籤，就應該將電池視為新電池，並重新讀取所有快取的資料。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-137">Whenever the battery tag is updated, the battery should be treated as if it were a new battery and all cached data should be re-read.</span></span> <span data-ttu-id="fb6e2-138">如果應用程式需要知道相同的實體電池是否存在，則應該在使用 **BatteryUniqueID** 資訊層級進行呼叫時，檢查 [**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md)的輸出緩衝區中的 **BatteryUniqueID** 值。</span><span class="sxs-lookup"><span data-stu-id="fb6e2-138">If an application needs to know if the same physical battery is present, it should check the value of **BatteryUniqueID** in the output buffer of [**IOCTL\_BATTERY\_QUERY\_INFORMATION**](ioctl-battery-query-information.md) when called with the **BatteryUniqueID** information level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb6e2-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="fb6e2-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb6e2-140">關於電源管理</span><span class="sxs-lookup"><span data-stu-id="fb6e2-140">About Power Management</span></span>](about-power-management.md)
</dt> <dt>

[<span data-ttu-id="fb6e2-141">列舉電池裝置</span><span class="sxs-lookup"><span data-stu-id="fb6e2-141">Enumerating Battery Devices</span></span>](enumerating-battery-devices.md)
</dt> </dl>

 

 
