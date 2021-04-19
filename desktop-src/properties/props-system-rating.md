---
description: 使用介於1到99之間的整數值的評等系統。 這是 Windows Vista Shell 所使用的分級系統。
ms.assetid: a6288d29-1ef3-4da1-bd30-577336ab6817
title: 系統評分
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e411e313f0fa6042a8cbe3a076a7166928020af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993104"
---
# <a name="systemrating"></a><span data-ttu-id="2d0f9-104">系統評分</span><span class="sxs-lookup"><span data-stu-id="2d0f9-104">System.Rating</span></span>

<span data-ttu-id="2d0f9-105">使用介於1到99之間的整數值的評等系統。</span><span class="sxs-lookup"><span data-stu-id="2d0f9-105">A rating system that uses integer values between 1 and 99.</span></span> <span data-ttu-id="2d0f9-106">這是 Windows Vista Shell 所使用的分級系統。</span><span class="sxs-lookup"><span data-stu-id="2d0f9-106">This is the rating system used by the Windows Vista Shell.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="2d0f9-107">Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版</span><span class="sxs-lookup"><span data-stu-id="2d0f9-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = OneStar
            minValue = 1
            setValue = 1
            defineMaxValue = 12
            text = 1 Star
            defineToken = RATING_ONE_STAR
         enumRange
            name = TwoStars
            minValue = 13
            setValue = 25
            defineMaxValue = 37
            text = 2 Stars
            defineToken = RATING_TWO_STARS
         enumRange
            name = ThreeStars
            minValue = 38
            setValue = 50
            defineMaxValue = 62
            text = 3 Stars
            defineToken = RATING_THREE_STARS
         enumRange
            name = FourStars
            minValue = 63
            setValue = 75
            defineMaxValue = 87
            text = 4 Stars
            defineToken = RATING_FOUR_STARS
         enumRange
            name = FiveStars
            minValue = 88
            setValue = 99
            defineMaxValue = 99
            text = 5 Stars
            defineToken = RATING_FIVE_STARS
         enumRange
            name
            minValue = 100
```

## <a name="windows-vista"></a><span data-ttu-id="2d0f9-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d0f9-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Rating
   shellPKey = PKEY_Rating
   formatID = 64440492-4C8B-11D1-8B70-080036B11A03
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            defineMinName = RATING_UNRATED_MIN
            setValue = 0
            defineSetName = RATING_UNRATED_SET
            defineMaxValue = 0
            defineMaxName = RATING_UNRATED_MAX
            text = Unrated
         enumRange
            minValue = 1
            defineMinName = RATING_ONE_STAR_MIN
            setValue = 1
            defineSetName = RATING_ONE_STAR_SET
            defineMaxValue = 12
            defineMaxName = RATING_ONE_STAR_MAX
            text = 1 Star
         enumRange
            minValue = 13
            defineMinName = RATING_TWO_STARS_MIN
            setValue = 25
            defineSetName = RATING_TWO_STARS_SET
            defineMaxValue = 37
            defineMaxName = RATING_TWO_STARS_MAX
            text = 2 Stars
         enumRange
            minValue = 38
            defineMinName = RATING_THREE_STARS_MIN
            setValue = 50
            defineSetName = RATING_THREE_STARS_SET
            defineMaxValue = 62
            defineMaxName = RATING_THREE_STARS_MAX
            text = 3 Stars
         enumRange
            minValue = 63
            defineMinName = RATING_FOUR_STARS_MIN
            setValue = 75
            defineSetName = RATING_FOUR_STARS_SET
            defineMaxValue = 87
            defineMaxName = RATING_FOUR_STARS_MAX
            text = 4 Stars
         enumRange
            minValue = 88
            defineMinName = RATING_FIVE_STARS_MIN
            setValue = 99
            defineSetName = RATING_FIVE_STARS_SET
            defineMaxValue = 99
            defineMaxName = RATING_FIVE_STARS_MAX
            text = 5 Stars
         enumRange
            minValue = 100
```

## <a name="remarks"></a><span data-ttu-id="2d0f9-109">備註</span><span class="sxs-lookup"><span data-stu-id="2d0f9-109">Remarks</span></span>

<span data-ttu-id="2d0f9-110">PKEY 值定義于 Propkey 中。</span><span class="sxs-lookup"><span data-stu-id="2d0f9-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="2d0f9-111">若要與使用值介於1到5之間的分級系統相容，請參閱 [SimpleRating](./props-system-simplerating.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="2d0f9-111">For compatibility with ratings systems that use values between 1 and 5, see the property [System.SimpleRating](./props-system-simplerating.md).</span></span> <span data-ttu-id="2d0f9-112">不過請注意，Windows Vista Shell 中不會使用 SimpleRating。</span><span class="sxs-lookup"><span data-stu-id="2d0f9-112">Note, however, that System.SimpleRating is not used in the Windows Vista Shell.</span></span>

<span data-ttu-id="2d0f9-113">下表說明 Shell UI 中所使用的星星評等系統，其代表的是 [system. 評分]() 值。</span><span class="sxs-lookup"><span data-stu-id="2d0f9-113">The following table describes what the star rating system used in the Shell UI means in terms of the [System.Rating]() value.</span></span>



| <span data-ttu-id="2d0f9-114">系統評分</span><span class="sxs-lookup"><span data-stu-id="2d0f9-114">System.Rating</span></span> | <span data-ttu-id="2d0f9-115">星級評等</span><span class="sxs-lookup"><span data-stu-id="2d0f9-115">Star Rating</span></span> |
|---------------|-------------|
| <span data-ttu-id="2d0f9-116">1-12</span><span class="sxs-lookup"><span data-stu-id="2d0f9-116">1-12</span></span>          | <span data-ttu-id="2d0f9-117">1 顆星</span><span class="sxs-lookup"><span data-stu-id="2d0f9-117">1 Star</span></span>      |
| <span data-ttu-id="2d0f9-118">13-37</span><span class="sxs-lookup"><span data-stu-id="2d0f9-118">13-37</span></span>         | <span data-ttu-id="2d0f9-119">2 顆星</span><span class="sxs-lookup"><span data-stu-id="2d0f9-119">2 Stars</span></span>     |
| <span data-ttu-id="2d0f9-120">38-62</span><span class="sxs-lookup"><span data-stu-id="2d0f9-120">38-62</span></span>         | <span data-ttu-id="2d0f9-121">3 顆星</span><span class="sxs-lookup"><span data-stu-id="2d0f9-121">3 Stars</span></span>     |
| <span data-ttu-id="2d0f9-122">63-87</span><span class="sxs-lookup"><span data-stu-id="2d0f9-122">63-87</span></span>         | <span data-ttu-id="2d0f9-123">4 顆星</span><span class="sxs-lookup"><span data-stu-id="2d0f9-123">4 Stars</span></span>     |
| <span data-ttu-id="2d0f9-124">88-99</span><span class="sxs-lookup"><span data-stu-id="2d0f9-124">88-99</span></span>         | <span data-ttu-id="2d0f9-125">5 顆星</span><span class="sxs-lookup"><span data-stu-id="2d0f9-125">5 Stars</span></span>     |



 

<span data-ttu-id="2d0f9-126">當使用者在 UI 中選擇星狀分級值來評分專案時，系統會指派實際的 [系統評分]() 值，如下表所示：</span><span class="sxs-lookup"><span data-stu-id="2d0f9-126">When a user rates an item by choosing a star rating value in the UI, actual [System.Rating]() values are assigned as shown in this table:</span></span>



| <span data-ttu-id="2d0f9-127">星級評等</span><span class="sxs-lookup"><span data-stu-id="2d0f9-127">Star Rating</span></span> | <span data-ttu-id="2d0f9-128">透過 UI 指派的值</span><span class="sxs-lookup"><span data-stu-id="2d0f9-128">Value Assigned Through UI</span></span> |
|-------------|---------------------------|
| <span data-ttu-id="2d0f9-129">1 顆星</span><span class="sxs-lookup"><span data-stu-id="2d0f9-129">1 Star</span></span>      | <span data-ttu-id="2d0f9-130">1</span><span class="sxs-lookup"><span data-stu-id="2d0f9-130">1</span></span>                         |
| <span data-ttu-id="2d0f9-131">2 顆星</span><span class="sxs-lookup"><span data-stu-id="2d0f9-131">2 Stars</span></span>     | <span data-ttu-id="2d0f9-132">25</span><span class="sxs-lookup"><span data-stu-id="2d0f9-132">25</span></span>                        |
| <span data-ttu-id="2d0f9-133">3 顆星</span><span class="sxs-lookup"><span data-stu-id="2d0f9-133">3 Stars</span></span>     | <span data-ttu-id="2d0f9-134">50</span><span class="sxs-lookup"><span data-stu-id="2d0f9-134">50</span></span>                        |
| <span data-ttu-id="2d0f9-135">4 顆星</span><span class="sxs-lookup"><span data-stu-id="2d0f9-135">4 Stars</span></span>     | <span data-ttu-id="2d0f9-136">75</span><span class="sxs-lookup"><span data-stu-id="2d0f9-136">75</span></span>                        |
| <span data-ttu-id="2d0f9-137">5 顆星</span><span class="sxs-lookup"><span data-stu-id="2d0f9-137">5 Stars</span></span>     | <span data-ttu-id="2d0f9-138">99</span><span class="sxs-lookup"><span data-stu-id="2d0f9-138">99</span></span>                        |



 

<span data-ttu-id="2d0f9-139">如果您的檔案有 [SimpleRating](./props-system-simplerating.md) 值，而不是 [system. 評分]() 值，請使用下表來轉換和指定 system.object 的值。</span><span class="sxs-lookup"><span data-stu-id="2d0f9-139">If your file has a [System.SimpleRating](./props-system-simplerating.md) value rather than a [System.Rating]() value, use the table below to convert and specify values for System.Rating.</span></span>



| <span data-ttu-id="2d0f9-140">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="2d0f9-140">System.SimpleRating</span></span> | <span data-ttu-id="2d0f9-141">系統評分</span><span class="sxs-lookup"><span data-stu-id="2d0f9-141">System.Rating</span></span> |
|---------------------|---------------|
| <span data-ttu-id="2d0f9-142">1</span><span class="sxs-lookup"><span data-stu-id="2d0f9-142">1</span></span>                   | <span data-ttu-id="2d0f9-143">1</span><span class="sxs-lookup"><span data-stu-id="2d0f9-143">1</span></span>             |
| <span data-ttu-id="2d0f9-144">2</span><span class="sxs-lookup"><span data-stu-id="2d0f9-144">2</span></span>                   | <span data-ttu-id="2d0f9-145">25</span><span class="sxs-lookup"><span data-stu-id="2d0f9-145">25</span></span>            |
| <span data-ttu-id="2d0f9-146">3</span><span class="sxs-lookup"><span data-stu-id="2d0f9-146">3</span></span>                   | <span data-ttu-id="2d0f9-147">50</span><span class="sxs-lookup"><span data-stu-id="2d0f9-147">50</span></span>            |
| <span data-ttu-id="2d0f9-148">4</span><span class="sxs-lookup"><span data-stu-id="2d0f9-148">4</span></span>                   | <span data-ttu-id="2d0f9-149">75</span><span class="sxs-lookup"><span data-stu-id="2d0f9-149">75</span></span>            |
| <span data-ttu-id="2d0f9-150">5</span><span class="sxs-lookup"><span data-stu-id="2d0f9-150">5</span></span>                   | <span data-ttu-id="2d0f9-151">99</span><span class="sxs-lookup"><span data-stu-id="2d0f9-151">99</span></span>            |



 

<span data-ttu-id="2d0f9-152">如果您的檔案同時具有 system.string 和[SimpleRating](./props-system-simplerating.md)保存值，請一律在直接要求時[使用 system.]()分級值，而不需參考 SimpleRating。</span><span class="sxs-lookup"><span data-stu-id="2d0f9-152">If your file has both [System.Rating]() and [System.SimpleRating](./props-system-simplerating.md) persisted values, always use the System.Rating value when it is directly requested, without reference to System.SimpleRating.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d0f9-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d0f9-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d0f9-154">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2d0f9-154">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-155">searchInfo</span><span class="sxs-lookup"><span data-stu-id="2d0f9-155">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-156">labelInfo</span><span class="sxs-lookup"><span data-stu-id="2d0f9-156">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-157">typeInfo</span><span class="sxs-lookup"><span data-stu-id="2d0f9-157">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-158">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2d0f9-158">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-159">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2d0f9-159">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-160">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="2d0f9-160">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-161">>cultureinfo.numberformat</span><span class="sxs-lookup"><span data-stu-id="2d0f9-161">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-162">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2d0f9-162">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-163">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="2d0f9-163">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-164">drawControl</span><span class="sxs-lookup"><span data-stu-id="2d0f9-164">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-165">editControl</span><span class="sxs-lookup"><span data-stu-id="2d0f9-165">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-166">filterControl</span><span class="sxs-lookup"><span data-stu-id="2d0f9-166">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2d0f9-167">queryControl</span><span class="sxs-lookup"><span data-stu-id="2d0f9-167">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
