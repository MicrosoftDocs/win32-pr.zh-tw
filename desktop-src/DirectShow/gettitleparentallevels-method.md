---
description: GetTitleParentalLevels 方法會為指定的標題抓取家長管理層級。
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: GetTitleParentalLevels 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385706"
---
# <a name="gettitleparentallevels-method"></a><span data-ttu-id="88698-103">GetTitleParentalLevels 方法</span><span class="sxs-lookup"><span data-stu-id="88698-103">GetTitleParentalLevels Method</span></span>

> [!Note]  
> <span data-ttu-id="88698-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="88698-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="88698-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="88698-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="88698-106">`GetTitleParentalLevels`方法會針對指定的標題抓取家長管理層級。</span><span class="sxs-lookup"><span data-stu-id="88698-106">The `GetTitleParentalLevels` method retrieves the parental management levels for the specified title.</span></span>

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a><span data-ttu-id="88698-107">參數</span><span class="sxs-lookup"><span data-stu-id="88698-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88698-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="88698-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="88698-109">將標題指定為整數。</span><span class="sxs-lookup"><span data-stu-id="88698-109">Specifies the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88698-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="88698-110">Return Value</span></span>

<span data-ttu-id="88698-111">傳回整數值，其個別位表示在指定的標題中設定 (>PROCMONTRACE.PML) 的家長管理層級。</span><span class="sxs-lookup"><span data-stu-id="88698-111">Returns an integer value whose individual bits indicate which parental management levels (PML) are set in the specified title.</span></span>

## <a name="remarks"></a><span data-ttu-id="88698-112">備註</span><span class="sxs-lookup"><span data-stu-id="88698-112">Remarks</span></span>

<span data-ttu-id="88698-113">標題可能有章節或更短的區段，其 >PROCMONTRACE.PML 與標題的整體 >PROCMONTRACE.PML 不同。</span><span class="sxs-lookup"><span data-stu-id="88698-113">A title may have chapters or even short segments that have a PML different from the overall PML for the title.</span></span> <span data-ttu-id="88698-114">您可以使用這個方法來判斷播放指定的標題時，將會遇到的所有 PMLs。</span><span class="sxs-lookup"><span data-stu-id="88698-114">Use this method to determine all the PMLs that will be encountered when playing a specified title.</span></span> <span data-ttu-id="88698-115">傳回的整數是一組位旗標，定義如下表所示。</span><span class="sxs-lookup"><span data-stu-id="88698-115">The returned integer is a set of bit flags that are defined as shown in the table below.</span></span> <span data-ttu-id="88698-116">在 *iLevels* 和每個可能的值上執行位 and 運算。</span><span class="sxs-lookup"><span data-stu-id="88698-116">Perform a bitwise AND operation on *iLevels* and each possible value.</span></span> <span data-ttu-id="88698-117">如果作業傳回 **true**，表示會在此標題的某個時間點遇到 >procmontrace.pml。</span><span class="sxs-lookup"><span data-stu-id="88698-117">If the operation returns **true**, it means that PML will be encountered at some point in this title.</span></span>



| <span data-ttu-id="88698-118">值</span><span class="sxs-lookup"><span data-stu-id="88698-118">Value</span></span>  | <span data-ttu-id="88698-119">描述</span><span class="sxs-lookup"><span data-stu-id="88698-119">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="88698-120">0x100</span><span class="sxs-lookup"><span data-stu-id="88698-120">0x100</span></span>  | <span data-ttu-id="88698-121">DVD 父母層級1</span><span class="sxs-lookup"><span data-stu-id="88698-121">DVD Parental Level 1</span></span> |
| <span data-ttu-id="88698-122">0x200</span><span class="sxs-lookup"><span data-stu-id="88698-122">0x200</span></span>  | <span data-ttu-id="88698-123">DVD 父母層級2</span><span class="sxs-lookup"><span data-stu-id="88698-123">DVD Parental Level 2</span></span> |
| <span data-ttu-id="88698-124">0x400</span><span class="sxs-lookup"><span data-stu-id="88698-124">0x400</span></span>  | <span data-ttu-id="88698-125">DVD 家長監護層級3</span><span class="sxs-lookup"><span data-stu-id="88698-125">DVD Parental Level 3</span></span> |
| <span data-ttu-id="88698-126">0x800</span><span class="sxs-lookup"><span data-stu-id="88698-126">0x800</span></span>  | <span data-ttu-id="88698-127">DVD 家長監護層級4</span><span class="sxs-lookup"><span data-stu-id="88698-127">DVD Parental Level 4</span></span> |
| <span data-ttu-id="88698-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="88698-128">0x1000</span></span> | <span data-ttu-id="88698-129">DVD 父母層級5</span><span class="sxs-lookup"><span data-stu-id="88698-129">DVD Parental Level 5</span></span> |
| <span data-ttu-id="88698-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="88698-130">0x2000</span></span> | <span data-ttu-id="88698-131">DVD 父母層級6</span><span class="sxs-lookup"><span data-stu-id="88698-131">DVD Parental Level 6</span></span> |
| <span data-ttu-id="88698-132">0x4000</span><span class="sxs-lookup"><span data-stu-id="88698-132">0x4000</span></span> | <span data-ttu-id="88698-133">DVD 父母層級7</span><span class="sxs-lookup"><span data-stu-id="88698-133">DVD Parental Level 7</span></span> |
| <span data-ttu-id="88698-134">0x8000</span><span class="sxs-lookup"><span data-stu-id="88698-134">0x8000</span></span> | <span data-ttu-id="88698-135">DVD 父母層級8</span><span class="sxs-lookup"><span data-stu-id="88698-135">DVD Parental Level 8</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="88698-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88698-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88698-137">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="88698-137">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="88698-138">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="88698-138">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="88698-139">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="88698-139">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="88698-140">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="88698-140">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 



