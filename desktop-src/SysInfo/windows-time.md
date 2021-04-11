---
description: Windows time 是自上次啟動系統以來經過的毫秒數。
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Windows Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af776e2cc5a36993f6be0e0776d5b73fab6622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115168"
---
# <a name="windows-time"></a><span data-ttu-id="f1952-103">Windows Time</span><span class="sxs-lookup"><span data-stu-id="f1952-103">Windows Time</span></span>

<span data-ttu-id="f1952-104">*Windows time* 是自上次啟動系統以來經過的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="f1952-104">*Windows time* is the number of milliseconds elapsed since the system was last started.</span></span> <span data-ttu-id="f1952-105">這種格式的存在主要是為了與16位 Windows 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="f1952-105">This format exists primarily for backward compatibility with 16-bit Windows.</span></span> <span data-ttu-id="f1952-106">為了確保為16位 Windows 設計的應用程式可繼續順利執行， [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 函數會傳回目前的 Windows 時間。</span><span class="sxs-lookup"><span data-stu-id="f1952-106">To ensure that applications designed for 16-bit Windows continue to run successfully, the [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function returns the current Windows time.</span></span>

<span data-ttu-id="f1952-107">您通常會使用 [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 或 [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) 函數，將目前的 Windows 時間與 [**GetMessageTime**](/windows/win32/api/winuser/nf-winuser-getmessagetime) 函式所傳回的時間進行比較。</span><span class="sxs-lookup"><span data-stu-id="f1952-107">You typically use the [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) or [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) function to compare the current Windows time with the time returned by the [**GetMessageTime**](/windows/win32/api/winuser/nf-winuser-getmessagetime) function.</span></span> <span data-ttu-id="f1952-108">**GetMessageTime** 會傳回指定的訊息建立時的 Windows 時間。</span><span class="sxs-lookup"><span data-stu-id="f1952-108">**GetMessageTime** returns the Windows time when the specified message was created.</span></span> <span data-ttu-id="f1952-109">**GetTickCount** 和 **GetTickCount64** 僅限於系統計時器的解析度，大約10毫秒到16毫秒。</span><span class="sxs-lookup"><span data-stu-id="f1952-109">**GetTickCount** and **GetTickCount64** are limited to the resolution of the system timer, which is approximately 10 milliseconds to 16 milliseconds.</span></span> <span data-ttu-id="f1952-110">**GetTickCount** 或 **GetTickCount64** 所取出的經過時間，包括系統花在睡眠或休眠狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="f1952-110">The elapsed time retrieved by **GetTickCount** or **GetTickCount64** includes time the system spends in sleep or hibernation.</span></span>

<span data-ttu-id="f1952-111">如果您需要較高的解析度計時器，請使用 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) 函數、 [多媒體計時器](/windows/desktop/Multimedia/multimedia-timers)或 [高解析度計時器](../winmsg/about-timers.md)。</span><span class="sxs-lookup"><span data-stu-id="f1952-111">If you need a higher resolution timer, use the [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) function, a [multimedia timer](/windows/desktop/Multimedia/multimedia-timers), or a [high-resolution timer](../winmsg/about-timers.md).</span></span> <span data-ttu-id="f1952-112">**QueryUnbiasedInterruptTime** 函式所抓取的經過時間只包含系統花在工作狀態的時間。</span><span class="sxs-lookup"><span data-stu-id="f1952-112">The elapsed time retrieved by the **QueryUnbiasedInterruptTime** function includes only time that the system spends in the working state.</span></span>

<span data-ttu-id="f1952-113">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP/2000：** 從 Windows 7 和 Windows Server 2008 R2 開始，可以使用 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) 函數。</span><span class="sxs-lookup"><span data-stu-id="f1952-113">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP/2000:** The [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) function is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="f1952-114">您可以使用 [系統執行時間] 效能計數器來取得自電腦啟動以來經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="f1952-114">You can use the System Up Time performance counter to obtain the number of seconds elapsed since the computer was started.</span></span> <span data-ttu-id="f1952-115">您可以從登錄機碼 **HKEY \_ 效能 \_ 資料** 的效能資料中抓取此效能計數器。</span><span class="sxs-lookup"><span data-stu-id="f1952-115">This performance counter can be retrieved from the performance data in the registry key **HKEY\_PERFORMANCE\_DATA**.</span></span> <span data-ttu-id="f1952-116">傳回的值是8位元組值。</span><span class="sxs-lookup"><span data-stu-id="f1952-116">The value returned is an 8-byte value.</span></span> <span data-ttu-id="f1952-117">如需相關資訊，請參閱 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal)。</span><span class="sxs-lookup"><span data-stu-id="f1952-117">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

 

 
