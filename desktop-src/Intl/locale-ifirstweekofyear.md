---
description: 地區設定 \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 7f391fb167a9362fc8770bbcc5a495170148b489
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "106982787"
---
# <a name="locale_ifirstweekofyear"></a><span data-ttu-id="e6480-103">地區設定 \_ IFIRSTWEEKOFYEAR</span><span class="sxs-lookup"><span data-stu-id="e6480-103">LOCALE\_IFIRSTWEEKOFYEAR</span></span>

<span data-ttu-id="e6480-104">年度的第一周。</span><span class="sxs-lookup"><span data-stu-id="e6480-104">The first week of the year.</span></span>



| <span data-ttu-id="e6480-105">值</span><span class="sxs-lookup"><span data-stu-id="e6480-105">Value</span></span> | <span data-ttu-id="e6480-106">意義</span><span class="sxs-lookup"><span data-stu-id="e6480-106">Meaning</span></span>                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6480-107">0</span><span class="sxs-lookup"><span data-stu-id="e6480-107">0</span></span>     | <span data-ttu-id="e6480-108">包含1/1 的周是年度的第一周。</span><span class="sxs-lookup"><span data-stu-id="e6480-108">Week containing 1/1 is the first week of the year.</span></span> <span data-ttu-id="e6480-109">請注意，如果1/1 落在一周的最後一天，這可能是一天。</span><span class="sxs-lookup"><span data-stu-id="e6480-109">Note that this can be a single day, if 1/1 falls on the last day of the week.</span></span> |
| <span data-ttu-id="e6480-110">1</span><span class="sxs-lookup"><span data-stu-id="e6480-110">1</span></span>     | <span data-ttu-id="e6480-111">1/1 之後的第一周，是一年的第一周。</span><span class="sxs-lookup"><span data-stu-id="e6480-111">First full week following 1/1 is the first week of the year.</span></span>                                                                     |
| <span data-ttu-id="e6480-112">2</span><span class="sxs-lookup"><span data-stu-id="e6480-112">2</span></span>     | <span data-ttu-id="e6480-113">第一周至少包含四天，這是年度的第一周。</span><span class="sxs-lookup"><span data-stu-id="e6480-113">First week containing at least four days is the first week of the year.</span></span> <span data-ttu-id="e6480-114">ISO 8601 相容。</span><span class="sxs-lookup"><span data-stu-id="e6480-114">ISO 8601 compatible.</span></span>                                     |

<span data-ttu-id="e6480-115">如果 LOCALE_IFIRSTWEEKOFYEAR 為2，LOCALE_IFIRSTDAYOFWEEK 為 0 (星期一) ，而 LOCALE_ICALENDARTYPE 為西曆，則第一周會遵循 ISO 8601 定義，其中第一周是在第一周的第一個星期四。</span><span class="sxs-lookup"><span data-stu-id="e6480-115">If LOCALE_IFIRSTWEEKOFYEAR is 2, LOCALE_IFIRSTDAYOFWEEK is 0 (Monday), and LOCALE_ICALENDARTYPE is Gregorian, then the first week follows the ISO 8601 definition where the first week is the week with the first Thursday of the Gregorian year in it.</span></span>


 

 

 



