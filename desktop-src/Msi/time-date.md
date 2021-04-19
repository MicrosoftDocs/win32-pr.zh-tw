---
description: Time/Date 資料類型具有個別儲存的時間和日期，並使用不帶正負號的整數做為位欄位，如下所示。
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: 時間/日期
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974719"
---
# <a name="timedate"></a><span data-ttu-id="08037-103">時間/日期</span><span class="sxs-lookup"><span data-stu-id="08037-103">Time/Date</span></span>

<span data-ttu-id="08037-104">Time/Date 資料類型具有個別儲存的時間和日期，並使用不帶正負號的整數做為位欄位，如下所示。</span><span class="sxs-lookup"><span data-stu-id="08037-104">The Time/Date data type has the time and the date stored individually, using unsigned integers as bit fields, packed as follows.</span></span>

## <a name="time"></a><span data-ttu-id="08037-105">Time</span><span class="sxs-lookup"><span data-stu-id="08037-105">Time</span></span>

<span data-ttu-id="08037-106">時間會以不帶正負號的2位元組整數編碼，並具有下列位欄位。</span><span class="sxs-lookup"><span data-stu-id="08037-106">Time is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="08037-107">目錄</span><span class="sxs-lookup"><span data-stu-id="08037-107">Contents</span></span>           | <span data-ttu-id="08037-108">Bits</span><span class="sxs-lookup"><span data-stu-id="08037-108">Bits</span></span>        | <span data-ttu-id="08037-109">數值範圍</span><span class="sxs-lookup"><span data-stu-id="08037-109">Value range</span></span> |
|--------------------|-------------|-------------|
| <span data-ttu-id="08037-110">小時</span><span class="sxs-lookup"><span data-stu-id="08037-110">hours</span></span>              | <span data-ttu-id="08037-111">0 1 2 3 4</span><span class="sxs-lookup"><span data-stu-id="08037-111">0 1 2 3 4</span></span>   | <span data-ttu-id="08037-112">0–23</span><span class="sxs-lookup"><span data-stu-id="08037-112">0–23</span></span>        |
| <span data-ttu-id="08037-113">minutes</span><span class="sxs-lookup"><span data-stu-id="08037-113">minutes</span></span>            | <span data-ttu-id="08037-114">5 6 7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="08037-114">5 6 7 8 9 A</span></span> | <span data-ttu-id="08037-115">0–59</span><span class="sxs-lookup"><span data-stu-id="08037-115">0–59</span></span>        |
| <span data-ttu-id="08037-116">2秒間隔</span><span class="sxs-lookup"><span data-stu-id="08037-116">2-second intervals</span></span> | <span data-ttu-id="08037-117">B C D E F</span><span class="sxs-lookup"><span data-stu-id="08037-117">B C D E F</span></span>   | <span data-ttu-id="08037-118">0–29</span><span class="sxs-lookup"><span data-stu-id="08037-118">0–29</span></span>        |



 

## <a name="date"></a><span data-ttu-id="08037-119">Date</span><span class="sxs-lookup"><span data-stu-id="08037-119">Date</span></span>

<span data-ttu-id="08037-120">日期會以不帶正負號的2位元組整數編碼，並具有下列位欄位。</span><span class="sxs-lookup"><span data-stu-id="08037-120">Date is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="08037-121">目錄</span><span class="sxs-lookup"><span data-stu-id="08037-121">Contents</span></span> | <span data-ttu-id="08037-122">Bits</span><span class="sxs-lookup"><span data-stu-id="08037-122">Bits</span></span>          | <span data-ttu-id="08037-123">數值範圍</span><span class="sxs-lookup"><span data-stu-id="08037-123">Value range</span></span>              |
|----------|---------------|--------------------------|
| <span data-ttu-id="08037-124">year</span><span class="sxs-lookup"><span data-stu-id="08037-124">year</span></span>     | <span data-ttu-id="08037-125">0 1 2 3 4 5 6</span><span class="sxs-lookup"><span data-stu-id="08037-125">0 1 2 3 4 5 6</span></span> | <span data-ttu-id="08037-126">0– 119 (相對於 1980) </span><span class="sxs-lookup"><span data-stu-id="08037-126">0–119 (relative to 1980)</span></span> |
| <span data-ttu-id="08037-127">月</span><span class="sxs-lookup"><span data-stu-id="08037-127">month</span></span>    | <span data-ttu-id="08037-128">7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="08037-128">7 8 9 A</span></span>       | <span data-ttu-id="08037-129">1–12</span><span class="sxs-lookup"><span data-stu-id="08037-129">1–12</span></span>                     |
| <span data-ttu-id="08037-130">day</span><span class="sxs-lookup"><span data-stu-id="08037-130">day</span></span>      | <span data-ttu-id="08037-131">B C D E F</span><span class="sxs-lookup"><span data-stu-id="08037-131">B C D E F</span></span>     | <span data-ttu-id="08037-132">1–31</span><span class="sxs-lookup"><span data-stu-id="08037-132">1–31</span></span>                     |



 

 

 



