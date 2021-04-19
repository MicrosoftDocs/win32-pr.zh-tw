---
description: 地區設定 \_ SDURATION
ms.assetid: 45ffd7ed-f964-4948-8679-cf960b5c1e0e
title: LOCALE_SDURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00740d2f041794b36e8f0e0d8ad2d25723bc12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992205"
---
# <a name="locale_sduration"></a><span data-ttu-id="8df09-103">地區設定 \_ SDURATION</span><span class="sxs-lookup"><span data-stu-id="8df09-103">LOCALE\_SDURATION</span></span>

<span data-ttu-id="8df09-104">**Windows Vista 和更新版本：** 由下表所列格式圖片組成的時間持續時間格式。</span><span class="sxs-lookup"><span data-stu-id="8df09-104">**Windows Vista and later:** Time duration format composed of format pictures listed in the following table.</span></span> <span data-ttu-id="8df09-105">格式類似 [地區設定 \_ STIMEFORMAT](locale-stime-constants.md)的格式。</span><span class="sxs-lookup"><span data-stu-id="8df09-105">The format is similar to the format for [LOCALE\_STIMEFORMAT](locale-stime-constants.md).</span></span> <span data-ttu-id="8df09-106">針對地區 \_ 設定 STIMEFORMAT，此格式也可以包含以單引號括住的任何字元字串。</span><span class="sxs-lookup"><span data-stu-id="8df09-106">As for LOCALE\_STIMEFORMAT, this format can also include any string of characters enclosed in single quotes.</span></span> <span data-ttu-id="8df09-107">格式可包含，例如 "h:mm： ss" 或 "d ' h'h '. fff '"。</span><span class="sxs-lookup"><span data-stu-id="8df09-107">Formats can include, for example, "h:mm:ss", or "d'd 'h'h 'm'm 's.fff's'".</span></span> <span data-ttu-id="8df09-108">相較于地區 \_ 設定 STIMEFORMAT，有一秒的小數部分會有其他格式的圖片。</span><span class="sxs-lookup"><span data-stu-id="8df09-108">In comparison with LOCALE\_STIMEFORMAT, there are additional format pictures for fractions of a second.</span></span> <span data-ttu-id="8df09-109">因為這種格式是用於持續時間，而不是時間，所以不會指定12或24小時制的系統，也不會包含 AM/PM 指標。</span><span class="sxs-lookup"><span data-stu-id="8df09-109">Because this format is for duration, not time, it does not specify a 12- or 24-hour clock system, or include an AM/PM indicator.</span></span> <span data-ttu-id="8df09-110">例如，這個常數可能會用於顯示檔案時間的多媒體應用程式，或顯示完成時間的體育活動應用程式。</span><span class="sxs-lookup"><span data-stu-id="8df09-110">This constant might be used, for example, for a multi-media application that displays file time or a sporting event application that displays finish times.</span></span>



| <span data-ttu-id="8df09-111">值</span><span class="sxs-lookup"><span data-stu-id="8df09-111">Value</span></span> | <span data-ttu-id="8df09-112">意義</span><span class="sxs-lookup"><span data-stu-id="8df09-112">Meaning</span></span>                                                                                                                                                                                                                             |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8df09-113">h</span><span class="sxs-lookup"><span data-stu-id="8df09-113">h</span></span>     | <span data-ttu-id="8df09-114">單一位數小時沒有前置零的小時數</span><span class="sxs-lookup"><span data-stu-id="8df09-114">Hours without leading zeros for single-digit hours</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="8df09-115">hh</span><span class="sxs-lookup"><span data-stu-id="8df09-115">hh</span></span>    | <span data-ttu-id="8df09-116">單一位數小時的前置零小時</span><span class="sxs-lookup"><span data-stu-id="8df09-116">Hours with leading zeros for single-digit hours</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="8df09-117">m</span><span class="sxs-lookup"><span data-stu-id="8df09-117">m</span></span>     | <span data-ttu-id="8df09-118">單一位數分鐘沒有前置零的分鐘數</span><span class="sxs-lookup"><span data-stu-id="8df09-118">Minutes without leading zeros for single-digit minutes</span></span>                                                                                                                                                                              |
| <span data-ttu-id="8df09-119">mm</span><span class="sxs-lookup"><span data-stu-id="8df09-119">mm</span></span>    | <span data-ttu-id="8df09-120">單一位數分鐘的前置零分鐘</span><span class="sxs-lookup"><span data-stu-id="8df09-120">Minutes with leading zeros for single-digit minutes</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="8df09-121">s</span><span class="sxs-lookup"><span data-stu-id="8df09-121">s</span></span>     | <span data-ttu-id="8df09-122">單一位數秒沒有前置零的秒數</span><span class="sxs-lookup"><span data-stu-id="8df09-122">Seconds without leading zeros for single-digit seconds</span></span>                                                                                                                                                                              |
| <span data-ttu-id="8df09-123">ss</span><span class="sxs-lookup"><span data-stu-id="8df09-123">ss</span></span>    | <span data-ttu-id="8df09-124">以前置零表示的秒數（以秒為單位）</span><span class="sxs-lookup"><span data-stu-id="8df09-124">Seconds with leading zeros for single-digit seconds</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="8df09-125">f</span><span class="sxs-lookup"><span data-stu-id="8df09-125">f</span></span>     | <span data-ttu-id="8df09-126">十分之一秒</span><span class="sxs-lookup"><span data-stu-id="8df09-126">Tenths of a second</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="8df09-127">ff</span><span class="sxs-lookup"><span data-stu-id="8df09-127">ff</span></span>    | <span data-ttu-id="8df09-128">百分之一秒</span><span class="sxs-lookup"><span data-stu-id="8df09-128">Hundredths of a second</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="8df09-129">fff</span><span class="sxs-lookup"><span data-stu-id="8df09-129">fff</span></span>   | <span data-ttu-id="8df09-130">秒數秒;字元 "f" 最多可有九次 (.fffffffff) ，雖然頻率計時器的支援限制為100毫微秒;如果有九個字元，最後兩個數字一律為零</span><span class="sxs-lookup"><span data-stu-id="8df09-130">Thousandths of a second; character "f" can occur up to nine consecutive times (fffffffff), although support for frequency timers is limited to 100 nanoseconds; if nine characters are present, the last two digits are always zero</span></span> |



 

 

 



