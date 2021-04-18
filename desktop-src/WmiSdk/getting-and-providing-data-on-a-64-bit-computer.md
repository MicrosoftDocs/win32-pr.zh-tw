---
description: 存取標準 WMI 32 位提供者的用戶端應用程式和腳本在64位作業系統上執行時，會繼續正常運作。
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: 在64位電腦上取得和提供資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559845"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a><span data-ttu-id="8657a-103">在64位電腦上取得和提供資料</span><span class="sxs-lookup"><span data-stu-id="8657a-103">Getting and Providing Data on a 64-bit Computer</span></span>

<span data-ttu-id="8657a-104">存取標準 WMI 32 位提供者的用戶端應用程式和腳本在64位作業系統上執行時，會繼續正常運作。</span><span class="sxs-lookup"><span data-stu-id="8657a-104">Client applications and scripts that access standard WMI 32-bit providers continue to operate normally when running on a 64-bit operating system.</span></span> <span data-ttu-id="8657a-105">只有兩個預先安裝的提供者（ [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 和 [View provider](view-provider.md)）具有與32位版本並存執行的64位版本。</span><span class="sxs-lookup"><span data-stu-id="8657a-105">Only two preinstalled providers, the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) and the [View provider](view-provider.md), have 64-bit versions which run side-by-side with the 32-bit versions.</span></span> <span data-ttu-id="8657a-106">不過，要求32位 Windows Driver Model (WDM) 實例的32位應用程式會收到64位作業系統上的預設64位 WDM 類別實例。</span><span class="sxs-lookup"><span data-stu-id="8657a-106">However, a 32-bit application that requests 32-bit Windows Driver Model (WDM) instances receives the default 64-bit WDM class instances on a 64-bit operating system.</span></span>

## <a name="accessing-default-and-nondefault-provider-data"></a><span data-ttu-id="8657a-107">存取預設和非預設的提供者資料</span><span class="sxs-lookup"><span data-stu-id="8657a-107">Accessing Default and Nondefault Provider Data</span></span>

<span data-ttu-id="8657a-108">一般而言，提供者寫入器不會同時在相同的作業系統中包含32位和64位版本的提供者。</span><span class="sxs-lookup"><span data-stu-id="8657a-108">Generally, provider writers do not include both 32-bit and 64-bit versions of a provider in the same operating system.</span></span> <span data-ttu-id="8657a-109">如果沒有64位提供者存在，32位提供者可以繼續透過 WOW64 的功能執行。</span><span class="sxs-lookup"><span data-stu-id="8657a-109">If no 64-bit provider exists, a 32-bit provider can continue to run through the facilities of WOW64.</span></span> <span data-ttu-id="8657a-110">64位提供者同樣可以提供資料給32位應用程式。</span><span class="sxs-lookup"><span data-stu-id="8657a-110">A 64-bit provider can likewise supply data to a 32-bit application.</span></span> <span data-ttu-id="8657a-111">如需詳細資訊，請參閱 [在64位平臺上提供 WMI 資料](providing-wmi-data-on-a-64-bit-platform.md)。</span><span class="sxs-lookup"><span data-stu-id="8657a-111">For more information, see [Providing WMI Data on a 64-bit Platform](providing-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="8657a-112">如果有兩個版本，用戶端應用程式和腳本可以使用 [COM API](com-api-for-wmi.md) 和 [腳本 API](scripting-api-for-wmi.md) 中提供的內容參數，明確地連接到特定非預設的 WMI 提供者（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="8657a-112">If two versions exist, client applications and scripts can use the context parameters available in the [COM API](com-api-for-wmi.md) and the [Scripting API](scripting-api-for-wmi.md) to connect explicitly to a specific nondefault WMI provider, if it is available.</span></span> <span data-ttu-id="8657a-113">如需詳細資訊，請參閱 [在64位平臺上要求 WMI 資料](requesting-wmi-data-on-a-64-bit-platform.md)。</span><span class="sxs-lookup"><span data-stu-id="8657a-113">For more information, see [Requesting WMI Data on a 64-bit Platform](requesting-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="8657a-114">下圖顯示預設和非預設的連線，使用登錄作為範例，讓兩個提供者可以並存于64位平臺上。</span><span class="sxs-lookup"><span data-stu-id="8657a-114">The following diagram shows the default and nondefault connections, using the registry as an example for which two providers can exist side-by-side on a 64-bit platform.</span></span>

![64位平臺上的預設和非預設連接](images/32-64bit-registry.png)

## <a name="related-topics"></a><span data-ttu-id="8657a-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="8657a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8657a-117">在64位平臺上要求 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="8657a-117">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="8657a-118">在64位平臺上提供 WMI 資料</span><span class="sxs-lookup"><span data-stu-id="8657a-118">Providing WMI Data on a 64-bit Platform</span></span>](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
