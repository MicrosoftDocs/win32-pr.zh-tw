---
title: IWMPQuery addCondition 方法
description: AddCondition 方法會使用和邏輯，將條件加入至複合查詢。
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- addCondition 方法 Windows Media Player
- addCondition 方法 Windows Media Player，IWMPQuery 介面
- IWMPQuery 介面 Windows Media Player，addCondition 方法
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984772"
---
# <a name="iwmpqueryaddcondition-method"></a><span data-ttu-id="0600c-106">IWMPQuery：： addCondition 方法</span><span class="sxs-lookup"><span data-stu-id="0600c-106">IWMPQuery::addCondition method</span></span>

<span data-ttu-id="0600c-107">**AddCondition** 方法會使用 **和** 邏輯，將條件加入至複合查詢。</span><span class="sxs-lookup"><span data-stu-id="0600c-107">The **addCondition** method adds a condition to the compound query using **AND** logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="0600c-108">語法</span><span class="sxs-lookup"><span data-stu-id="0600c-108">Syntax</span></span>


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a><span data-ttu-id="0600c-109">參數</span><span class="sxs-lookup"><span data-stu-id="0600c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0600c-110">*bstrAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0600c-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0600c-111">System.string，此為要加入至查詢的屬性名稱 **。**</span><span class="sxs-lookup"><span data-stu-id="0600c-111">A **System.String** that is the name of the attribute to be added to the query.</span></span>

</dd> <dt>

<span data-ttu-id="0600c-112">*bstrOperator* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0600c-112">*bstrOperator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0600c-113">作為運算子的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="0600c-113">A **System.String** that is the operator.</span></span> <span data-ttu-id="0600c-114">如需支援的值，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0600c-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="0600c-115">*bstrValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0600c-115">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0600c-116">表示屬性值的 **system.string** 。</span><span class="sxs-lookup"><span data-stu-id="0600c-116">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0600c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0600c-117">Return value</span></span>

<span data-ttu-id="0600c-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0600c-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0600c-119">備註</span><span class="sxs-lookup"><span data-stu-id="0600c-119">Remarks</span></span>

<span data-ttu-id="0600c-120">複合查詢中包含的條件會組織成條件群組。</span><span class="sxs-lookup"><span data-stu-id="0600c-120">Conditions contained in a compound query are organized into condition groups.</span></span> <span data-ttu-id="0600c-121">條件群組內的多個條件一律會使用 **和** 邏輯串連。</span><span class="sxs-lookup"><span data-stu-id="0600c-121">Multiple conditions within a condition group are always concatenated by using **AND** logic.</span></span> <span data-ttu-id="0600c-122">條件群組一律會使用 **或** 邏輯互相串連。</span><span class="sxs-lookup"><span data-stu-id="0600c-122">Condition groups are always concatenated to each other by using **OR** logic.</span></span> <span data-ttu-id="0600c-123">若要啟動新的條件群組，請呼叫 [IWMPQuery. beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md)。</span><span class="sxs-lookup"><span data-stu-id="0600c-123">To start a new condition group, call [IWMPQuery.beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span></span>

<span data-ttu-id="0600c-124">使用 **IWMPQuery** 的複合查詢不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="0600c-124">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="0600c-125">*BstrAttribute* 參數的值清單可以在 [依字母順序的屬性參考](alphabetical-attribute-reference.md)中找到。</span><span class="sxs-lookup"><span data-stu-id="0600c-125">A list of values for the *bstrAttribute* parameter can be found in [Alphabetical Attribute Reference](alphabetical-attribute-reference.md).</span></span>

<span data-ttu-id="0600c-126">下表列出支援的 *bstrOperator* 值。</span><span class="sxs-lookup"><span data-stu-id="0600c-126">The following table lists the supported values for *bstrOperator*.</span></span>



| <span data-ttu-id="0600c-127">String</span><span class="sxs-lookup"><span data-stu-id="0600c-127">String</span></span>              | <span data-ttu-id="0600c-128">適用於</span><span class="sxs-lookup"><span data-stu-id="0600c-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="0600c-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="0600c-129">BeginsWith</span></span>          | <span data-ttu-id="0600c-130">字串</span><span class="sxs-lookup"><span data-stu-id="0600c-130">Strings</span></span>        |
| <span data-ttu-id="0600c-131">包含</span><span class="sxs-lookup"><span data-stu-id="0600c-131">Contains</span></span>            | <span data-ttu-id="0600c-132">字串</span><span class="sxs-lookup"><span data-stu-id="0600c-132">Strings</span></span>        |
| <span data-ttu-id="0600c-133">等於</span><span class="sxs-lookup"><span data-stu-id="0600c-133">Equals</span></span>              | <span data-ttu-id="0600c-134">所有類型</span><span class="sxs-lookup"><span data-stu-id="0600c-134">All types</span></span>      |
| <span data-ttu-id="0600c-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="0600c-135">GreaterThan</span></span>         | <span data-ttu-id="0600c-136">數位、日期</span><span class="sxs-lookup"><span data-stu-id="0600c-136">Numbers, Dates</span></span> |
| <span data-ttu-id="0600c-137">GreaterThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="0600c-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="0600c-138">數位、日期</span><span class="sxs-lookup"><span data-stu-id="0600c-138">Numbers, Dates</span></span> |
| <span data-ttu-id="0600c-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="0600c-139">LessThan</span></span>            | <span data-ttu-id="0600c-140">數位、日期</span><span class="sxs-lookup"><span data-stu-id="0600c-140">Numbers, Dates</span></span> |
| <span data-ttu-id="0600c-141">LessThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="0600c-141">LessThanOrEquals</span></span>    | <span data-ttu-id="0600c-142">數位、日期</span><span class="sxs-lookup"><span data-stu-id="0600c-142">Numbers, Dates</span></span> |
| <span data-ttu-id="0600c-143">NotBeginsWith</span><span class="sxs-lookup"><span data-stu-id="0600c-143">NotBeginsWith</span></span>       | <span data-ttu-id="0600c-144">字串</span><span class="sxs-lookup"><span data-stu-id="0600c-144">Strings</span></span>        |
| <span data-ttu-id="0600c-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="0600c-145">NotContains</span></span>         | <span data-ttu-id="0600c-146">字串</span><span class="sxs-lookup"><span data-stu-id="0600c-146">Strings</span></span>        |
| <span data-ttu-id="0600c-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="0600c-147">NotEquals</span></span>           | <span data-ttu-id="0600c-148">所有類型</span><span class="sxs-lookup"><span data-stu-id="0600c-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="0600c-149">範例</span><span class="sxs-lookup"><span data-stu-id="0600c-149">Examples</span></span>

<span data-ttu-id="0600c-150">下列範例會建立查詢，在其中加入兩個條件，然後使用該查詢將查詢結果以字串集合的形式解壓縮。</span><span class="sxs-lookup"><span data-stu-id="0600c-150">The following example creates a query, adds two conditions to it, and uses that query to extract the results of the query as a string collection.</span></span> <span data-ttu-id="0600c-151">結果會顯示在清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="0600c-151">The results are then displayed in a list box.</span></span> <span data-ttu-id="0600c-152">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="0600c-152">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="0600c-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="0600c-153">Requirements</span></span>



| <span data-ttu-id="0600c-154">需求</span><span class="sxs-lookup"><span data-stu-id="0600c-154">Requirement</span></span> | <span data-ttu-id="0600c-155">值</span><span class="sxs-lookup"><span data-stu-id="0600c-155">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0600c-156">版本</span><span class="sxs-lookup"><span data-stu-id="0600c-156">Version</span></span><br/>   | <span data-ttu-id="0600c-157">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="0600c-157">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="0600c-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="0600c-158">Namespace</span></span><br/> | <span data-ttu-id="0600c-159">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0600c-159">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0600c-160">組件</span><span class="sxs-lookup"><span data-stu-id="0600c-160">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0600c-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="0600c-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0600c-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0600c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0600c-163">**依字母順序排列屬性參考**</span><span class="sxs-lookup"><span data-stu-id="0600c-163">**Alphabetical Attribute Reference**</span></span>](alphabetical-attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="0600c-164">**IWMPMediaCollection2. createQuery (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0600c-164">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0600c-165">**IWMPMediaCollection2. getPlaylistByQuery (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0600c-165">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0600c-166">**IWMPMediaCollection2. getStringCollectionByQuery (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="0600c-166">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0600c-167">**IWMPQuery 介面**</span><span class="sxs-lookup"><span data-stu-id="0600c-167">**IWMPQuery Interface**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





