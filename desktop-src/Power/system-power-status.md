---
description: 系統電源狀態指出電腦的電源來源是否為系統電池或 AC 電源。 針對使用電池的電腦，系統電源狀態也會指出電池的存留期，以及電池是否正在充電。
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: 系統電源狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977316"
---
# <a name="system-power-status"></a><span data-ttu-id="ebc34-104">系統電源狀態</span><span class="sxs-lookup"><span data-stu-id="ebc34-104">System Power Status</span></span>

<span data-ttu-id="ebc34-105">系統電源狀態指出電腦的電源來源是否為系統電池或 AC 電源。</span><span class="sxs-lookup"><span data-stu-id="ebc34-105">The system power status indicates whether the source of power for a computer is a system battery or AC power.</span></span> <span data-ttu-id="ebc34-106">針對使用電池的電腦，系統電源狀態也會指出電池的存留期，以及電池是否正在充電。</span><span class="sxs-lookup"><span data-stu-id="ebc34-106">For computers that use batteries, the system power status also indicates how much battery life remains and whether the battery is charging.</span></span>

<span data-ttu-id="ebc34-107">透過 [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) 函式註冊電源設定通知，即可抓取電源資訊。</span><span class="sxs-lookup"><span data-stu-id="ebc34-107">Power information is retrieved by registering for power setting notifications through the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function.</span></span> <span data-ttu-id="ebc34-108">此功能可讓應用程式註冊特定的電源設定，並在變更時收到通知。</span><span class="sxs-lookup"><span data-stu-id="ebc34-108">This function allows applications to register for specific power settings and be notified when they change.</span></span>

> [!Note]  
> <span data-ttu-id="ebc34-109">若要查詢沒有通知的電源狀態資訊，請使用 [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)。</span><span class="sxs-lookup"><span data-stu-id="ebc34-109">To query for power status information without notifications, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span></span>

 

<span data-ttu-id="ebc34-110">應用程式和可安裝的驅動程式通常會使用系統電源狀態來判斷是否可以繼續運作。</span><span class="sxs-lookup"><span data-stu-id="ebc34-110">Applications and installable drivers typically use the system power status to determine whether continued operation is feasible.</span></span> <span data-ttu-id="ebc34-111">例如，在應用程式執行背景作業（例如將檔案壓縮或分頁）之前，它應該檢查系統是否為電池。</span><span class="sxs-lookup"><span data-stu-id="ebc34-111">For example, before an application performs background operations such as compressing or paginating a file, it should check whether the system is on batteries.</span></span> <span data-ttu-id="ebc34-112">另一個範例是，開始進行冗長作業的應用程式應該檢查狀態，以判斷是否有足夠的電池電力來完成作業。</span><span class="sxs-lookup"><span data-stu-id="ebc34-112">As another example, an application that is beginning a lengthy operation should check the status to determine whether enough battery power exists to complete the operation.</span></span>

<span data-ttu-id="ebc34-113">根據預設，系統不會在睡眠轉換期間查詢應用程式或驅動程式。</span><span class="sxs-lookup"><span data-stu-id="ebc34-113">By default, the system does not query applications or drivers during sleep transitions.</span></span>

> [!Note]  
> <span data-ttu-id="ebc34-114">如果電力不足，應用程式可以要求使用者介入，或要求系統暫停本身。</span><span class="sxs-lookup"><span data-stu-id="ebc34-114">If power is low, an application can request user intervention or request that the system suspend itself.</span></span> <span data-ttu-id="ebc34-115">您可以使用 [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) 函數來暫停系統作業。</span><span class="sxs-lookup"><span data-stu-id="ebc34-115">You can suspend system operation by using the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ebc34-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebc34-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebc34-117">關於電源管理</span><span class="sxs-lookup"><span data-stu-id="ebc34-117">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



