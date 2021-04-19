---
title: 引數元素
description: 引數元素包含條件字串的其中一個部分。
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- 引數元素 Windows Media Player
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c4adc0b853054d448bc9955f3bd8c64115ac2ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987169"
---
# <a name="argument-element"></a><span data-ttu-id="11bf1-104">引數元素</span><span class="sxs-lookup"><span data-stu-id="11bf1-104">argument Element</span></span>

<span data-ttu-id="11bf1-105">**引數** 元素包含條件字串的其中一個部分。</span><span class="sxs-lookup"><span data-stu-id="11bf1-105">The **argument** element contains one portion of a condition string.</span></span> <span data-ttu-id="11bf1-106">條件字串通常有條件部分和值部分。</span><span class="sxs-lookup"><span data-stu-id="11bf1-106">A condition string typically has a condition portion and a value portion.</span></span> <span data-ttu-id="11bf1-107">例如，在條件字串「演出者等於 Joe」中，條件部分是「等於」，而值部分是「Joe」。</span><span class="sxs-lookup"><span data-stu-id="11bf1-107">For example, in the condition string "Artist Equals Joe", the condition portion is "Equals" and the value portion is "Joe".</span></span>

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a><span data-ttu-id="11bf1-108">屬性</span><span class="sxs-lookup"><span data-stu-id="11bf1-108">Attributes</span></span>

<span data-ttu-id="11bf1-109">需要 (**名稱**) </span><span class="sxs-lookup"><span data-stu-id="11bf1-109">**name** (required)</span></span>

<span data-ttu-id="11bf1-110">條件字串之一部分的名稱。</span><span class="sxs-lookup"><span data-stu-id="11bf1-110">The name of one portion of the condition string.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="11bf1-111">父/子項目</span><span class="sxs-lookup"><span data-stu-id="11bf1-111">Parent/Child Elements</span></span>



| <span data-ttu-id="11bf1-112">階層</span><span class="sxs-lookup"><span data-stu-id="11bf1-112">Hierarchy</span></span> | <span data-ttu-id="11bf1-113">元素</span><span class="sxs-lookup"><span data-stu-id="11bf1-113">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="11bf1-114">父代</span><span class="sxs-lookup"><span data-stu-id="11bf1-114">Parent</span></span>    | [<span data-ttu-id="11bf1-115">片段</span><span class="sxs-lookup"><span data-stu-id="11bf1-115">fragment</span></span>](fragment-element.md) |
| <span data-ttu-id="11bf1-116">子系</span><span class="sxs-lookup"><span data-stu-id="11bf1-116">Child</span></span>     | <span data-ttu-id="11bf1-117">無</span><span class="sxs-lookup"><span data-stu-id="11bf1-117">None</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="11bf1-118">備註</span><span class="sxs-lookup"><span data-stu-id="11bf1-118">Remarks</span></span>

<span data-ttu-id="11bf1-119">當 **片段** 專案的 **name** 屬性是媒體專案特性（如專輯演出者或內容類型）時，**片段** 專案必須包含兩個 **引數** 元素：一個指定條件，另一個指定值。</span><span class="sxs-lookup"><span data-stu-id="11bf1-119">When the **name** attribute of a **fragment** element is a media item characteristic such as Album Artist, or Genre, the **fragment** element must contain two **argument** elements: one that specifies a condition and another that specifies a value.</span></span> <span data-ttu-id="11bf1-120">下表顯示 **name** 屬性的兩個可能值，以及如何使用 **引數** 元素來指定條件和值。</span><span class="sxs-lookup"><span data-stu-id="11bf1-120">The following table shows two possible values for the **name** attribute and how **argument** elements are used to specify conditions and values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11bf1-121">屬性值</span><span class="sxs-lookup"><span data-stu-id="11bf1-121">Attribute value</span></span></th>
<th><span data-ttu-id="11bf1-122">Description</span><span class="sxs-lookup"><span data-stu-id="11bf1-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11bf1-123">條件</span><span class="sxs-lookup"><span data-stu-id="11bf1-123">Condition</span></span></td>
<td><span data-ttu-id="11bf1-124"><strong>引數</strong>元素的內容是條件字串的條件部分。</span><span class="sxs-lookup"><span data-stu-id="11bf1-124">The content of the <strong>argument</strong> element is the condition portion of a condition string.</span></span> <span data-ttu-id="11bf1-125">例如，在條件字串 &quot; 演出者等於 Joe &quot; ，條件部分 &quot; 等於 &quot; 。</span><span class="sxs-lookup"><span data-stu-id="11bf1-125">For example, in the condition string &quot;Artist Equals Joe&quot;, the condition portion is &quot;Equals&quot;.</span></span> <span data-ttu-id="11bf1-126">條件字串的條件部分必須是下列其中一項： Equals、不等於、Contains、不包含、小於、大於、是、不是、早于、大於、小於、大於、小於、小於或等於、小於、不超過、小於、等於、小於、小於。</span><span class="sxs-lookup"><span data-stu-id="11bf1-126">The condition portion of a condition string must be one of the following: Equals, Does Not Equal, Contains, Does Not Contain, Is Less Than, Is Greater Than, Is, Is Not, Is Before, Is Later Than, Is More Recent Than, Above, Below, Ascending, Descending, Random, Is At Least, Is No More Than.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bf1-127">值</span><span class="sxs-lookup"><span data-stu-id="11bf1-127">Value</span></span></td>
<td><span data-ttu-id="11bf1-128"><strong>引數</strong>元素的內容是條件字串的值部分。</span><span class="sxs-lookup"><span data-stu-id="11bf1-128">The content of the <strong>argument</strong> element is the value portion of a condition string.</span></span> <span data-ttu-id="11bf1-129">例如，在條件字串 &quot; 演出者等於 joe &quot; ，值部分為 &quot; joe &quot; 。例子：</span><span class="sxs-lookup"><span data-stu-id="11bf1-129">For example, in the condition string &quot;Artist Equals Joe&quot;, the value portion is &quot;Joe&quot;.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="11bf1-130">當 **片段** 專案的 **name** 屬性為 "limit total Size To" 或 "limit total Duration to" 時，**片段** 元素必須包含兩個 **引數** 元素：一個指定格式，另一個則指定數位。</span><span class="sxs-lookup"><span data-stu-id="11bf1-130">When the **name** attribute of a **fragment** element is "Limit Total Size To" or "Limit Total Duration To", the **fragment** element must contain two **argument** elements: one that specifies a format and one that specifies a number.</span></span> <span data-ttu-id="11bf1-131">下表顯示 [ **名稱** ] 屬性的兩個可能值，以及如何使用 **引數** 元素來限制播放清單的大小或持續時間。</span><span class="sxs-lookup"><span data-stu-id="11bf1-131">The following table shows two possible values for the **name** attribute and how **argument** elements are used to limit the size or duration of a playlist.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11bf1-132">屬性值</span><span class="sxs-lookup"><span data-stu-id="11bf1-132">Attribute value</span></span></th>
<th><span data-ttu-id="11bf1-133">描述</span><span class="sxs-lookup"><span data-stu-id="11bf1-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11bf1-134">格式</span><span class="sxs-lookup"><span data-stu-id="11bf1-134">Format</span></span></td>
<td><span data-ttu-id="11bf1-135">當<strong>片段</strong>專案的 [<strong>名稱</strong>] 屬性是 [ &quot; 限制大小總計] 時 &quot; ，<strong>引數</strong>元素的內容必須是下列其中一項： kb、mb 或 gb。當<strong>片段</strong>專案的<strong>name</strong>屬性是 [ &quot; 限制的總持續時間] 時 &quot; ，<strong>引數</strong>元素的內容必須是下列其中一項：秒、分鐘、小時或天。</span><span class="sxs-lookup"><span data-stu-id="11bf1-135">When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Size To&quot;, the content of the <strong>argument</strong> element must be one of the following: Kilobytes, Megabytes, or Gigabytes.When the <strong>name</strong> attribute of the <strong>fragment</strong> element is &quot;Limit Total Duration To&quot;, the content of the <strong>argument</strong> element must be one of the following: Seconds, Minutes, Hours, or Days.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bf1-136">Number</span><span class="sxs-lookup"><span data-stu-id="11bf1-136">Number</span></span></td>
<td><span data-ttu-id="11bf1-137"><strong>引數</strong>元素的內容是一個數位，可限制播放清單的大小或持續時間。例子：</span><span class="sxs-lookup"><span data-stu-id="11bf1-137">The content of the <strong>argument</strong> element is a number that limits the size or duration of the playlist.Examples:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="11bf1-138">當 **片段** 元素的 **name** 屬性為 "Limit items of items" 時，**片段** 元素必須包含一個指定專案數目的 **引數** 元素。</span><span class="sxs-lookup"><span data-stu-id="11bf1-138">When the **name** attribute of a **fragment** element is "Limit Number of Items", the **fragment** element must contain one **argument** element that specifies the number of items.</span></span> <span data-ttu-id="11bf1-139">下表說明如何使用 **name** 屬性的數值。</span><span class="sxs-lookup"><span data-stu-id="11bf1-139">The following table shows how to use the Number value of the **name** attribute.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11bf1-140">屬性值</span><span class="sxs-lookup"><span data-stu-id="11bf1-140">Attribute value</span></span></th>
<th><span data-ttu-id="11bf1-141">Description</span><span class="sxs-lookup"><span data-stu-id="11bf1-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11bf1-142">Number</span><span class="sxs-lookup"><span data-stu-id="11bf1-142">Number</span></span></td>
<td><span data-ttu-id="11bf1-143"><strong>引數</strong>元素的內容是一個數位，可限制播放清單中的專案數。例子：</span><span class="sxs-lookup"><span data-stu-id="11bf1-143">The content of the <strong>argument</strong> element is a number that limits the number of items in a playlist.Example:</span></span><br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="11bf1-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="11bf1-144">Requirements</span></span>



| <span data-ttu-id="11bf1-145">需求</span><span class="sxs-lookup"><span data-stu-id="11bf1-145">Requirement</span></span> | <span data-ttu-id="11bf1-146">值</span><span class="sxs-lookup"><span data-stu-id="11bf1-146">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="11bf1-147">版本</span><span class="sxs-lookup"><span data-stu-id="11bf1-147">Version</span></span><br/> | <span data-ttu-id="11bf1-148">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="11bf1-148">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11bf1-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11bf1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11bf1-150">**片段元素**</span><span class="sxs-lookup"><span data-stu-id="11bf1-150">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="11bf1-151">**Windows Media 播放清單元素參考**</span><span class="sxs-lookup"><span data-stu-id="11bf1-151">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





