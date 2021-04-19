---
title: IWMPQuery beginNextGroup 方法
description: BeginNextGroup 方法會開始新的條件群組。 |IWMPQuery beginNextGroup 方法
ms.assetid: 15d20c9f-2ce7-4a86-9054-b7317ebe1a0a
keywords:
- beginNextGroup 方法 Windows Media Player
- beginNextGroup 方法 Windows Media Player，IWMPQuery 介面
- IWMPQuery 介面 Windows Media Player，beginNextGroup 方法
topic_type:
- apiref
api_name:
- IWMPQuery.beginNextGroup
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866727f821fb40b6bf09f3ee2cf0231c4ffc3005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997020"
---
# <a name="iwmpquerybeginnextgroup-method"></a><span data-ttu-id="b9894-107">IWMPQuery：： beginNextGroup 方法</span><span class="sxs-lookup"><span data-stu-id="b9894-107">IWMPQuery::beginNextGroup method</span></span>

<span data-ttu-id="b9894-108">**BeginNextGroup** 方法會開始新的條件群組。</span><span class="sxs-lookup"><span data-stu-id="b9894-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9894-109">語法</span><span class="sxs-lookup"><span data-stu-id="b9894-109">Syntax</span></span>


```CSharp
public void beginNextGroup();
```


```VB

Public Sub beginNextGroup()
Implements IWMPQuery.beginNextGroup
```





## <a name="parameters"></a><span data-ttu-id="b9894-110">參數</span><span class="sxs-lookup"><span data-stu-id="b9894-110">Parameters</span></span>

<span data-ttu-id="b9894-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b9894-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9894-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9894-112">Return value</span></span>

<span data-ttu-id="b9894-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b9894-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9894-114">備註</span><span class="sxs-lookup"><span data-stu-id="b9894-114">Remarks</span></span>

<span data-ttu-id="b9894-115">開始新的條件群組即表示您已完成目前的條件群組。</span><span class="sxs-lookup"><span data-stu-id="b9894-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="b9894-116">新的條件群組一律會使用 **或** 邏輯串連至先前的條件群組。</span><span class="sxs-lookup"><span data-stu-id="b9894-116">The new condition group is always concatenated to the previous condition group by using **OR** logic.</span></span>

## <a name="examples"></a><span data-ttu-id="b9894-117">範例</span><span class="sxs-lookup"><span data-stu-id="b9894-117">Examples</span></span>

<span data-ttu-id="b9894-118">下列範例會合並兩個包含條件的群組，以建立複雜的查詢。</span><span class="sxs-lookup"><span data-stu-id="b9894-118">The following example creates a complex query by combing two groups that each contain a condition.</span></span> <span data-ttu-id="b9894-119">查詢的結果會以字串集合的形式解壓縮，並顯示在清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="b9894-119">The results of the query are extracted as a string collection and displayed in a list box.</span></span> <span data-ttu-id="b9894-120">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="b9894-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");

// Begin another Query group.
q.beginNextGroup();

// Add a condition to the new group understanding that it will be combined with the
// first group using OR logic.
q.addCondition("Title", "Contains", "Capriol");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    complexQueryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

' Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi")

' Begin another Query group.
q.beginNextGroup()

' Add a condition to the new group understanding that it will be combined with the
' first group using OR logic.
q.addCondition("Title", "Contains", "Capriol")

' Query the media collection and get a string collection containing the result.
' In this case, the string collection will contain the titles of all audio items that
' match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery("Title", q, "audio", "", False)

' Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    complexQueryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="b9894-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9894-121">Requirements</span></span>



| <span data-ttu-id="b9894-122">需求</span><span class="sxs-lookup"><span data-stu-id="b9894-122">Requirement</span></span> | <span data-ttu-id="b9894-123">值</span><span class="sxs-lookup"><span data-stu-id="b9894-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9894-124">版本</span><span class="sxs-lookup"><span data-stu-id="b9894-124">Version</span></span><br/>   | <span data-ttu-id="b9894-125">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="b9894-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="b9894-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="b9894-126">Namespace</span></span><br/> | <span data-ttu-id="b9894-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b9894-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b9894-128">組件</span><span class="sxs-lookup"><span data-stu-id="b9894-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b9894-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="b9894-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9894-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9894-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9894-131">**IWMPMediaCollection2. createQuery (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b9894-131">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9894-132">**IWMPMediaCollection2. getPlaylistByQuery (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b9894-132">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9894-133">**IWMPMediaCollection2. getStringCollectionByQuery (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b9894-133">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9894-134">**IWMPQuery 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="b9894-134">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





