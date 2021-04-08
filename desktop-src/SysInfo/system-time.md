---
description: 系統時間是當日的目前日期和時間。
ms.assetid: 1a1e251e-2375-4134-bbd8-1e4670b9f9d2
title: 系統時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c727e8898fc2bc973d963c3a3c90524ca50958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853088"
---
# <a name="system-time"></a><span data-ttu-id="77078-103">系統時間</span><span class="sxs-lookup"><span data-stu-id="77078-103">System Time</span></span>

<span data-ttu-id="77078-104">*系統時間* 是當日的目前日期和時間。</span><span class="sxs-lookup"><span data-stu-id="77078-104">*System time* is the current date and time of day.</span></span> <span data-ttu-id="77078-105">系統會保留時間，讓您的應用程式可以立即存取精確的時間。</span><span class="sxs-lookup"><span data-stu-id="77078-105">The system keeps time so that your applications have ready access to accurate time.</span></span> <span data-ttu-id="77078-106">系統會以國際標準 *時間* 為基礎的系統時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="77078-106">The system bases system time on *coordinated universal time* (UTC).</span></span> <span data-ttu-id="77078-107">以 UTC 為基礎的時間已鬆散定義為目前在英國的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="77078-107">UTC-based time is loosely defined as the current date and time of day in Greenwich, England.</span></span>

<span data-ttu-id="77078-108">系統第一次啟動時，會將系統時間設定為以電腦的系統時鐘為基礎的值，然後定期更新時間。</span><span class="sxs-lookup"><span data-stu-id="77078-108">When the system first starts, it sets the system time to a value based on the real-time clock of the computer and then regularly updates the time.</span></span> <span data-ttu-id="77078-109">若要取得系統時間，請使用 [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime) 函數。</span><span class="sxs-lookup"><span data-stu-id="77078-109">To retrieve the system time, use the [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime) function.</span></span> <span data-ttu-id="77078-110">**GetSystemTime** 會將時間複製到 [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) 結構，其中包含月、日、年、工作日、小時、分、秒和毫秒的個別成員。</span><span class="sxs-lookup"><span data-stu-id="77078-110">**GetSystemTime** copies the time to a [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) structure that contains individual members for month, day, year, weekday, hour, minute, second, and milliseconds.</span></span> <span data-ttu-id="77078-111">您可以輕鬆地將此格式顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="77078-111">It is easy to display this format to a user.</span></span>

<span data-ttu-id="77078-112">您也可以使用 [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) 函數，以檔案時間格式取得系統時間。</span><span class="sxs-lookup"><span data-stu-id="77078-112">You can also obtain the system time in file time format using the [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) function.</span></span> <span data-ttu-id="77078-113">**GetSystemTimeAsFileTime** 會將時間複製到 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構。</span><span class="sxs-lookup"><span data-stu-id="77078-113">**GetSystemTimeAsFileTime** copies the time to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

<span data-ttu-id="77078-114">若要設定系統時間，請使用 [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime) 函數。</span><span class="sxs-lookup"><span data-stu-id="77078-114">To set the system time, use the [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime) function.</span></span> <span data-ttu-id="77078-115">**SetSystemTime** 會假設您已指定以 UTC 為基礎的時間。</span><span class="sxs-lookup"><span data-stu-id="77078-115">**SetSystemTime** assumes you have specified a UTC-based time.</span></span>

<span data-ttu-id="77078-116">[**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment)和 [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment)函式會使用每個時鐘中斷所套用的定期時間調整，將當日時間時鐘與另一個時間來源進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="77078-116">The [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment) and [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment) functions synchronize the time-of-day clock with another time source using a periodic time adjustment applied at each clock interrupt.</span></span>

<span data-ttu-id="77078-117">請注意，系統可以與時間來源進行同步處理，以定期重新整理時間。</span><span class="sxs-lookup"><span data-stu-id="77078-117">Note that the system can periodically refresh the time by synchronizing with a time source.</span></span> <span data-ttu-id="77078-118">因為系統時間可以向前或向後調整，所以請勿比較系統時間讀數來判斷經過的時間。</span><span class="sxs-lookup"><span data-stu-id="77078-118">Because the system time can be adjusted either forward or backward, do not compare system time readings to determine elapsed time.</span></span> <span data-ttu-id="77078-119">相反地，請使用 [Windows Time](windows-time.md)中所述的其中一個方法。</span><span class="sxs-lookup"><span data-stu-id="77078-119">Instead, use one of the methods described in [Windows Time](windows-time.md).</span></span>

 

 
