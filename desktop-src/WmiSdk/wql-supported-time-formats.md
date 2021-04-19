---
description: 描述在 WQL WHERE 子句中支援使用的時間格式。
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: WQL-Supported 時間格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975030"
---
# <a name="wql-supported-time-formats"></a><span data-ttu-id="e4464-103">WQL-Supported 時間格式</span><span class="sxs-lookup"><span data-stu-id="e4464-103">WQL-Supported Time Formats</span></span>

<span data-ttu-id="e4464-104">除了 WMI DATETIME 格式之外，還支援下列日期格式以用於 WQL WHERE 子句。</span><span class="sxs-lookup"><span data-stu-id="e4464-104">In addition to the WMI DATETIME format, the following date formats are supported for use in the WQL WHERE clause.</span></span>



| <span data-ttu-id="e4464-105">格式</span><span class="sxs-lookup"><span data-stu-id="e4464-105">Format</span></span>                                    | <span data-ttu-id="e4464-106">描述</span><span class="sxs-lookup"><span data-stu-id="e4464-106">Description</span></span>                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4464-107">hh \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="e4464-107">hh\[ \]{AP}M</span></span><br/>                   | <span data-ttu-id="e4464-108">以12小時制顯示的小時，以及 AM 或 PM 指定。</span><span class="sxs-lookup"><span data-stu-id="e4464-108">Hour as shown on a twelve-hour clock, and AM or PM designation.</span></span><br/> <span data-ttu-id="e4464-109">4 PM</span><span class="sxs-lookup"><span data-stu-id="e4464-109">4 PM</span></span><br/>                                                                                                             |
| <span data-ttu-id="e4464-110">hh:mm</span><span class="sxs-lookup"><span data-stu-id="e4464-110">hh:mm</span></span><br/>                          | <span data-ttu-id="e4464-111">以冒號分隔的小時和分鐘數。</span><span class="sxs-lookup"><span data-stu-id="e4464-111">Colon-delimited hour and minutes.</span></span> <span data-ttu-id="e4464-112">未指定 AM 或 PM。</span><span class="sxs-lookup"><span data-stu-id="e4464-112">No AM or PM designation.</span></span><br/> <span data-ttu-id="e4464-113">3:23</span><span class="sxs-lookup"><span data-stu-id="e4464-113">3:23</span></span><br/>                                                                                                                  |
| <span data-ttu-id="e4464-114">hh： mm \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="e4464-114">hh:mm\[ \]{AP}M</span></span><br/>                | <span data-ttu-id="e4464-115">以冒號分隔的小時和分鐘、選擇性的空格，以及 AM 或 PM 指定。</span><span class="sxs-lookup"><span data-stu-id="e4464-115">Colon-delimited hour and minutes, optional space, and AM or PM designation.</span></span><br/> <span data-ttu-id="e4464-116">上午3:23</span><span class="sxs-lookup"><span data-stu-id="e4464-116">3:23 AM</span></span><br/>                                                                                              |
| <span data-ttu-id="e4464-117">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="e4464-117">hh:mm:ss</span></span><br/>                       | <span data-ttu-id="e4464-118">以冒號分隔的小時、分鐘和秒數。</span><span class="sxs-lookup"><span data-stu-id="e4464-118">Colon-delimited hour, minutes and seconds.</span></span> <span data-ttu-id="e4464-119">沒有 AM/PM 指定。</span><span class="sxs-lookup"><span data-stu-id="e4464-119">No AM/PM designation.</span></span><br/> <span data-ttu-id="e4464-120">3:23:00</span><span class="sxs-lookup"><span data-stu-id="e4464-120">3:23:00</span></span><br/>                                                                                                         |
| <span data-ttu-id="e4464-121">hh： mm： ss \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="e4464-121">hh:mm:ss\[ \]{AP}M</span></span><br/>             | <span data-ttu-id="e4464-122">以冒號分隔的小時、分鐘和秒、選擇性的空間和 AM/PM 指定。</span><span class="sxs-lookup"><span data-stu-id="e4464-122">Colon-delimited hour, minutes and seconds, optional space, and AM/PM designation.</span></span><br/> <span data-ttu-id="e4464-123">3：23：00</span><span class="sxs-lookup"><span data-stu-id="e4464-123">3:23:00PM</span></span><br/>                                                                                      |
| <span data-ttu-id="e4464-124">hh： mm： ss： uuu</span><span class="sxs-lookup"><span data-stu-id="e4464-124">hh:mm:ss:uuu</span></span><br/>                   | <span data-ttu-id="e4464-125">以冒號分隔的小時、分鐘和秒，以及三位數的位移，表示原始時區偏離 UTC 的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="e4464-125">Colon-delimited hour, minutes and seconds, and three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                                    |
| <span data-ttu-id="e4464-126">hh： mm： ss： \[ \[ u \] u \] u</span><span class="sxs-lookup"><span data-stu-id="e4464-126">hh:mm:ss:\[\[u\]u\]u</span></span><br/>           | <span data-ttu-id="e4464-127">以冒號分隔的小時、分鐘和秒數;以及一個、兩個或三位數的位移，表示原始時區偏離 UTC 的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="e4464-127">Colon-delimited hour, minutes and seconds; and one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                       |
| <span data-ttu-id="e4464-128">hh： mm： ss： uuu \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="e4464-128">hh:mm:ss:uuu\[ \]{AP}M</span></span><br/>         | <span data-ttu-id="e4464-129">以冒號分隔的小時、分和秒、三位數的位移，表示原始時區偏離 UTC 和 AM 或 PM 指定的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="e4464-129">Colon-delimited hour, minutes and seconds, three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC, and AM or PM designation.</span></span><br/>              |
| <span data-ttu-id="e4464-130">hh： mm： ss： \[ \[ u \] u \] u \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="e4464-130">hh:mm:ss:\[\[u\]u\]u\[ \]{AP}M</span></span><br/> | <span data-ttu-id="e4464-131">以冒號分隔的小時、分鐘和秒數;一個、兩個或三位數的位移，表示原始時區偏離 UTC 的分鐘數;和 AM 或 PM 指定。</span><span class="sxs-lookup"><span data-stu-id="e4464-131">Colon-delimited hour, minutes and seconds; one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC; and AM or PM designation.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e4464-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4464-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4464-133">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="e4464-133">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




