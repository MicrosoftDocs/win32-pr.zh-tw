---
title: AddCondition 方法
description: AddCondition 方法會使用和邏輯，將條件加入至查詢物件。
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- addCondition 方法 Windows Media Player
- addCondition 方法 Windows Media Player，查詢類別
- 查詢類別 Windows Media Player，addCondition 方法
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994212"
---
# <a name="queryaddcondition-method"></a><span data-ttu-id="4d6b6-106">AddCondition 方法</span><span class="sxs-lookup"><span data-stu-id="4d6b6-106">Query.addCondition method</span></span>

<span data-ttu-id="4d6b6-107">**AddCondition** 方法會使用和邏輯，將條件加入至 **查詢** 物件。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-107">The **addCondition** method adds a condition to the **Query** object using AND logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d6b6-108">語法</span><span class="sxs-lookup"><span data-stu-id="4d6b6-108">Syntax</span></span>


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="4d6b6-109">參數</span><span class="sxs-lookup"><span data-stu-id="4d6b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d6b6-110">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d6b6-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d6b6-111">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="4d6b6-112">*運算子* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d6b6-112">*operator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d6b6-113">包含運算子的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-113">**String** containing the operator.</span></span> <span data-ttu-id="4d6b6-114">如需支援的值，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="4d6b6-115">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d6b6-115">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d6b6-116">包含屬性值的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-116">**String** containing the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d6b6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d6b6-117">Return value</span></span>

<span data-ttu-id="4d6b6-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d6b6-119">備註</span><span class="sxs-lookup"><span data-stu-id="4d6b6-119">Remarks</span></span>

<span data-ttu-id="4d6b6-120">使用 **查詢** 的複合查詢不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-120">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="4d6b6-121">您可以在 [[字母屬性參考](alphabetical-attribute-reference.md)] 區段中找到 *屬性* 參數值的清單。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-121">A list of values for the *attribute* parameter can be found in the [Alphabetical Attribute Reference](alphabetical-attribute-reference.md) section.</span></span>

<span data-ttu-id="4d6b6-122">**查詢** 物件中包含的條件會組織成條件群組。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-122">Conditions contained in a **Query** object are organized into condition groups.</span></span> <span data-ttu-id="4d6b6-123">條件群組內的多個條件一律會使用和邏輯串連。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-123">Multiple conditions within a condition group are always concatenated using AND logic.</span></span> <span data-ttu-id="4d6b6-124">條件群組一律會使用或邏輯互相串連。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-124">Condition groups are always concatenated to each other using OR logic.</span></span> <span data-ttu-id="4d6b6-125">若要啟動新的條件群組，請呼叫 **beginNextGroup**。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-125">To start a new condition group, call **Query.beginNextGroup**.</span></span>

<span data-ttu-id="4d6b6-126">下表列出 *運算子* 支援的值。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-126">The following table lists the supported values for *operator*.</span></span>



| <span data-ttu-id="4d6b6-127">運算子</span><span class="sxs-lookup"><span data-stu-id="4d6b6-127">Operator</span></span>            | <span data-ttu-id="4d6b6-128">適用於</span><span class="sxs-lookup"><span data-stu-id="4d6b6-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="4d6b6-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="4d6b6-129">BeginsWith</span></span>          | <span data-ttu-id="4d6b6-130">字串</span><span class="sxs-lookup"><span data-stu-id="4d6b6-130">Strings</span></span>        |
| <span data-ttu-id="4d6b6-131">包含</span><span class="sxs-lookup"><span data-stu-id="4d6b6-131">Contains</span></span>            | <span data-ttu-id="4d6b6-132">字串</span><span class="sxs-lookup"><span data-stu-id="4d6b6-132">Strings</span></span>        |
| <span data-ttu-id="4d6b6-133">等於</span><span class="sxs-lookup"><span data-stu-id="4d6b6-133">Equals</span></span>              | <span data-ttu-id="4d6b6-134">所有類型</span><span class="sxs-lookup"><span data-stu-id="4d6b6-134">All types</span></span>      |
| <span data-ttu-id="4d6b6-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="4d6b6-135">GreaterThan</span></span>         | <span data-ttu-id="4d6b6-136">數位、日期</span><span class="sxs-lookup"><span data-stu-id="4d6b6-136">Numbers, Dates</span></span> |
| <span data-ttu-id="4d6b6-137">GreaterThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="4d6b6-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="4d6b6-138">數位、日期</span><span class="sxs-lookup"><span data-stu-id="4d6b6-138">Numbers, Dates</span></span> |
| <span data-ttu-id="4d6b6-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="4d6b6-139">LessThan</span></span>            | <span data-ttu-id="4d6b6-140">數位、日期</span><span class="sxs-lookup"><span data-stu-id="4d6b6-140">Numbers, Dates</span></span> |
| <span data-ttu-id="4d6b6-141">LessThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="4d6b6-141">LessThanOrEquals</span></span>    | <span data-ttu-id="4d6b6-142">數位、日期</span><span class="sxs-lookup"><span data-stu-id="4d6b6-142">Numbers, Dates</span></span> |
| <span data-ttu-id="4d6b6-143">NotBeginsWith</span><span class="sxs-lookup"><span data-stu-id="4d6b6-143">NotBeginsWith</span></span>       | <span data-ttu-id="4d6b6-144">字串</span><span class="sxs-lookup"><span data-stu-id="4d6b6-144">Strings</span></span>        |
| <span data-ttu-id="4d6b6-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="4d6b6-145">NotContains</span></span>         | <span data-ttu-id="4d6b6-146">字串</span><span class="sxs-lookup"><span data-stu-id="4d6b6-146">Strings</span></span>        |
| <span data-ttu-id="4d6b6-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="4d6b6-147">NotEquals</span></span>           | <span data-ttu-id="4d6b6-148">所有類型</span><span class="sxs-lookup"><span data-stu-id="4d6b6-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="4d6b6-149">範例</span><span class="sxs-lookup"><span data-stu-id="4d6b6-149">Examples</span></span>

<span data-ttu-id="4d6b6-150">下列 JScript 範例會使用 **addCondition** 和 **beginNextGroup** 來執行範例查詢。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-150">The following JScript example uses **Query.addCondition** and **Query.beginNextGroup** to perform an example query.</span></span>


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a><span data-ttu-id="4d6b6-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d6b6-151">Requirements</span></span>



| <span data-ttu-id="4d6b6-152">需求</span><span class="sxs-lookup"><span data-stu-id="4d6b6-152">Requirement</span></span> | <span data-ttu-id="4d6b6-153">值</span><span class="sxs-lookup"><span data-stu-id="4d6b6-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d6b6-154">版本</span><span class="sxs-lookup"><span data-stu-id="4d6b6-154">Version</span></span><br/> | <span data-ttu-id="4d6b6-155">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="4d6b6-155">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="4d6b6-156">DLL</span><span class="sxs-lookup"><span data-stu-id="4d6b6-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="4d6b6-157"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d6b6-157"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d6b6-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d6b6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d6b6-159">**MediaCollection. createQuery**</span><span class="sxs-lookup"><span data-stu-id="4d6b6-159">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="4d6b6-160">**MediaCollection.getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="4d6b6-160">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="4d6b6-161">**MediaCollection.getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="4d6b6-161">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="4d6b6-162">**Query 物件**</span><span class="sxs-lookup"><span data-stu-id="4d6b6-162">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="4d6b6-163">**BeginNextGroup**</span><span class="sxs-lookup"><span data-stu-id="4d6b6-163">**Query.beginNextGroup**</span></span>](query-beginnextgroup.md)
</dt> </dl>

 

 





