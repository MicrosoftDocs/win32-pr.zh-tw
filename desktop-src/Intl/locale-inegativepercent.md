---
description: 地區設定 \_ INEGATIVEPERCENT
ms.assetid: 3518bd71-631d-48f2-b17f-b2ed41d44484
title: LOCALE_INEGATIVEPERCENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b98ee0229dfbbd392fbc03d2a7b5e4b413b3fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943894"
---
# <a name="locale_inegativepercent"></a><span data-ttu-id="57bca-103">地區設定 \_ INEGATIVEPERCENT</span><span class="sxs-lookup"><span data-stu-id="57bca-103">LOCALE\_INEGATIVEPERCENT</span></span>

<span data-ttu-id="57bca-104">**Windows 7 和更新版本：** 地區設定的負百分比格式模式。</span><span class="sxs-lookup"><span data-stu-id="57bca-104">**Windows 7 and later:** Negative percentage formatting pattern for the locale.</span></span> <span data-ttu-id="57bca-105">只能指定一個模式。</span><span class="sxs-lookup"><span data-stu-id="57bca-105">Only one pattern can be indicated.</span></span> <span data-ttu-id="57bca-106">如果有一種以上的格式用於地區設定，請選擇慣用的選項。</span><span class="sxs-lookup"><span data-stu-id="57bca-106">If more than one format is used for the locale, choose the preferred option.</span></span> <span data-ttu-id="57bca-107">例如，如果 "-9%" 針對 "負九%" 顯示負百分比，則這個常數的適當選擇是0。</span><span class="sxs-lookup"><span data-stu-id="57bca-107">For example, if a negative percentage is displayed "-9 %" for "negative nine percent", the appropriate choice for this constant is 0.</span></span>



| <span data-ttu-id="57bca-108">值</span><span class="sxs-lookup"><span data-stu-id="57bca-108">Value</span></span> | <span data-ttu-id="57bca-109">格式</span><span class="sxs-lookup"><span data-stu-id="57bca-109">Format</span></span>                                                    |
|-------|-----------------------------------------------------------|
| <span data-ttu-id="57bca-110">0</span><span class="sxs-lookup"><span data-stu-id="57bca-110">0</span></span>     | <span data-ttu-id="57bca-111">負號、數位、空格、百分比;例如，-\# %</span><span class="sxs-lookup"><span data-stu-id="57bca-111">Negative sign, number, space, percent; for example, -\# %</span></span> |
| <span data-ttu-id="57bca-112">1</span><span class="sxs-lookup"><span data-stu-id="57bca-112">1</span></span>     | <span data-ttu-id="57bca-113">負號、數位、百分比;例如，-\#%</span><span class="sxs-lookup"><span data-stu-id="57bca-113">Negative sign, number, percent; for example, -\#%</span></span>         |
| <span data-ttu-id="57bca-114">2</span><span class="sxs-lookup"><span data-stu-id="57bca-114">2</span></span>     | <span data-ttu-id="57bca-115">負號、百分比、數位;例如，-%\#</span><span class="sxs-lookup"><span data-stu-id="57bca-115">Negative sign, percent, number; for example, -%\#</span></span>         |
| <span data-ttu-id="57bca-116">3</span><span class="sxs-lookup"><span data-stu-id="57bca-116">3</span></span>     | <span data-ttu-id="57bca-117">百分比、負號、數位;例如，%-\#</span><span class="sxs-lookup"><span data-stu-id="57bca-117">Percent, negative sign, number; for example, %-\#</span></span>         |
| <span data-ttu-id="57bca-118">4</span><span class="sxs-lookup"><span data-stu-id="57bca-118">4</span></span>     | <span data-ttu-id="57bca-119">百分比、數位、負號;例如，%\#-</span><span class="sxs-lookup"><span data-stu-id="57bca-119">Percent, number, negative sign; for example, %\#-</span></span>         |
| <span data-ttu-id="57bca-120">5</span><span class="sxs-lookup"><span data-stu-id="57bca-120">5</span></span>     | <span data-ttu-id="57bca-121">數位、負號、百分比;例如， \#-%</span><span class="sxs-lookup"><span data-stu-id="57bca-121">Number, negative sign, percent; for example, \#-%</span></span>         |
| <span data-ttu-id="57bca-122">6</span><span class="sxs-lookup"><span data-stu-id="57bca-122">6</span></span>     | <span data-ttu-id="57bca-123">Number、percent、負號;例如， \#%-</span><span class="sxs-lookup"><span data-stu-id="57bca-123">Number, percent, negative sign; for example, \#%-</span></span>         |
| <span data-ttu-id="57bca-124">7</span><span class="sxs-lookup"><span data-stu-id="57bca-124">7</span></span>     | <span data-ttu-id="57bca-125">負號、百分比、空格、數位;例如，-% \#</span><span class="sxs-lookup"><span data-stu-id="57bca-125">Negative sign, percent, space, number; for example, -% \#</span></span> |
| <span data-ttu-id="57bca-126">8</span><span class="sxs-lookup"><span data-stu-id="57bca-126">8</span></span>     | <span data-ttu-id="57bca-127">數位、空格、百分比、負號;例如， \# %-</span><span class="sxs-lookup"><span data-stu-id="57bca-127">Number, space, percent, negative sign; for example, \# %-</span></span> |
| <span data-ttu-id="57bca-128">9</span><span class="sxs-lookup"><span data-stu-id="57bca-128">9</span></span>     | <span data-ttu-id="57bca-129">百分比、空格、數位、負號;例如，% \#-</span><span class="sxs-lookup"><span data-stu-id="57bca-129">Percent, space, number, negative sign; for example, % \#-</span></span> |
| <span data-ttu-id="57bca-130">10</span><span class="sxs-lookup"><span data-stu-id="57bca-130">10</span></span>    | <span data-ttu-id="57bca-131">百分比、空格、負號、數位;例如，%-\#</span><span class="sxs-lookup"><span data-stu-id="57bca-131">Percent, space, negative sign, number; for example, % -\#</span></span> |
| <span data-ttu-id="57bca-132">11</span><span class="sxs-lookup"><span data-stu-id="57bca-132">11</span></span>    | <span data-ttu-id="57bca-133">Number、負號、空格、percent;例如， \# -%</span><span class="sxs-lookup"><span data-stu-id="57bca-133">Number, negative sign, space, percent; for example, \#- %</span></span> |



 

 

 



