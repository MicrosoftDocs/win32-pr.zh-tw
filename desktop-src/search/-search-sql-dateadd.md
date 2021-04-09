---
description: DATEADD 函數會針對具有日期類型的相符屬性，執行時間和日期計算。 使用 DATEADD 函數，取得目前的指定時間量內的日期和時間。
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: DATEADD 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112433"
---
# <a name="dateadd-function"></a><span data-ttu-id="a6bfd-104">DATEADD 函數</span><span class="sxs-lookup"><span data-stu-id="a6bfd-104">DATEADD Function</span></span>

<span data-ttu-id="a6bfd-105">DATEADD 函數會針對具有日期類型的相符屬性，執行時間和日期計算。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-105">The DATEADD function performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="a6bfd-106">使用 DATEADD 函數，取得目前的指定時間量內的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-106">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6bfd-107">語法</span><span class="sxs-lookup"><span data-stu-id="a6bfd-107">Syntax</span></span>


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a><span data-ttu-id="a6bfd-108">引數</span><span class="sxs-lookup"><span data-stu-id="a6bfd-108">Arguments</span></span>

<span data-ttu-id="a6bfd-109">*DateTimeUnits*</span><span class="sxs-lookup"><span data-stu-id="a6bfd-109">*DateTimeUnits*</span></span>

<span data-ttu-id="a6bfd-110">指定 *日期時間* 參數的單位：年、季、月、周、日、小時、分鐘或秒。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-110">Specifies the units of the *DateTime* parameter: YEAR, QUARTER, MONTH, WEEK, DAY, HOUR, MINUTE, or SECOND.</span></span> <span data-ttu-id="a6bfd-111">此值會區分大小寫，而且參數周圍不需要引號。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-111">This value is case-sensitive, and quotation marks are not required around the parameter.</span></span>

<span data-ttu-id="a6bfd-112">*OffsetValue*</span><span class="sxs-lookup"><span data-stu-id="a6bfd-112">*OffsetValue*</span></span>

<span data-ttu-id="a6bfd-113">使用 *DateTimeUnits* 參數所指定的單位來指定時間位移。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-113">Specifies the time offset, in the units specified by the *DateTimeUnits* parameter.</span></span> <span data-ttu-id="a6bfd-114">**OffsetValue** 必須是負整數。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-114">**OffsetValue** must be a negative integer.</span></span> <span data-ttu-id="a6bfd-115">不支援負值。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-115">Positive values are not supported.</span></span>

<span data-ttu-id="a6bfd-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="a6bfd-116">*DateTime*</span></span>

<span data-ttu-id="a6bfd-117">指定要從中計算位移的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-117">Specifies a time stamp from which to calculate the offset.</span></span> <span data-ttu-id="a6bfd-118">這不可以是日期常值。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-118">This cannot be a date literal.</span></span> <span data-ttu-id="a6bfd-119">它必須是 GETGMTDATE 或另一個 DATEADD 函數的結果。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-119">It must be either GETGMTDATE or the result of another DATEADD function.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6bfd-120">備註</span><span class="sxs-lookup"><span data-stu-id="a6bfd-120">Remarks</span></span>

<span data-ttu-id="a6bfd-121">DATEADD 函數只能用在常值比較中，而且只能在比較運算子的右邊使用。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-121">The DATEADD function can be used only in literal value comparisons and only on the right side of the comparison operator.</span></span>

<span data-ttu-id="a6bfd-122">GETGMTDATE 函式會傳回目前的日期和時間，以格林尼治平均時間 (GMT) 。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-122">The GETGMTDATE function returns the current date and time in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="a6bfd-123">請記住，這個值可能不會與您電腦的當地時間相同。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-123">Remember that this value may not be the same as the local time of your computer.</span></span>

<span data-ttu-id="a6bfd-124">請勿使用 equals (=) 比較運算子，因為內部時程表示可能會產生會導致非預期比對結果的舍入錯誤。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-124">Do not use the equals (=) comparison operator because the internal time representation can produce rounding errors that result in unexpected matching results.</span></span>

<span data-ttu-id="a6bfd-125">您可以使用多個 DATEADD 函數來合併位移單位。</span><span class="sxs-lookup"><span data-stu-id="a6bfd-125">You can use multiple DATEADD functions to combine offset units.</span></span>

### <a name="examples"></a><span data-ttu-id="a6bfd-126">範例</span><span class="sxs-lookup"><span data-stu-id="a6bfd-126">Examples</span></span>

<span data-ttu-id="a6bfd-127">下列範例 WHERE 子句符合過去五天內修改過的檔：</span><span class="sxs-lookup"><span data-stu-id="a6bfd-127">The following example WHERE clause matches documents that were modified within the last five days:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



<span data-ttu-id="a6bfd-128">下列範例 WHERE 子句符合過去兩天內修改過的檔和四個小時：</span><span class="sxs-lookup"><span data-stu-id="a6bfd-128">The following example WHERE clause matches documents that were modified within the last two days and four hours:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a><span data-ttu-id="a6bfd-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="a6bfd-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a6bfd-130">**參考**</span><span class="sxs-lookup"><span data-stu-id="a6bfd-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a6bfd-131">常值比較</span><span class="sxs-lookup"><span data-stu-id="a6bfd-131">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="a6bfd-132">多重值 (陣列) 比較</span><span class="sxs-lookup"><span data-stu-id="a6bfd-132">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="a6bfd-133">**概念**</span><span class="sxs-lookup"><span data-stu-id="a6bfd-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a6bfd-134">全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="a6bfd-134">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="a6bfd-135">非全文檢索述詞</span><span class="sxs-lookup"><span data-stu-id="a6bfd-135">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



