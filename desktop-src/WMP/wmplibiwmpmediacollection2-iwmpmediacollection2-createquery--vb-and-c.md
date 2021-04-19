---
title: IWMPMediaCollection2 createQuery 方法
description: CreateQuery 方法會傳回代表新查詢的 IWMPQuery 介面。
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- createQuery 方法 Windows Media Player
- createQuery 方法 Windows Media Player，IWMPMediaCollection2 介面
- IWMPMediaCollection2 介面 Windows Media Player，createQuery 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318b27a20ba801e1fbed58ff79c5bed7841f8c29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995089"
---
# <a name="iwmpmediacollection2createquery-method"></a><span data-ttu-id="2ee12-106">IWMPMediaCollection2：： createQuery 方法</span><span class="sxs-lookup"><span data-stu-id="2ee12-106">IWMPMediaCollection2::createQuery method</span></span>

<span data-ttu-id="2ee12-107">`createQuery`方法會傳回代表新查詢的 **IWMPQuery** 介面。</span><span class="sxs-lookup"><span data-stu-id="2ee12-107">The `createQuery` method returns an **IWMPQuery** interface that represents a new query.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ee12-108">語法</span><span class="sxs-lookup"><span data-stu-id="2ee12-108">Syntax</span></span>


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a><span data-ttu-id="2ee12-109">參數</span><span class="sxs-lookup"><span data-stu-id="2ee12-109">Parameters</span></span>

<span data-ttu-id="2ee12-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2ee12-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ee12-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ee12-111">Return value</span></span>

<span data-ttu-id="2ee12-112">**WMPLib IWMPQuery** 介面，表示新的空白查詢。</span><span class="sxs-lookup"><span data-stu-id="2ee12-112">A **WMPLib.IWMPQuery** interface that represents a new, empty query.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ee12-113">備註</span><span class="sxs-lookup"><span data-stu-id="2ee12-113">Remarks</span></span>

<span data-ttu-id="2ee12-114">建立新的查詢是建立複合查詢的第一個步驟。</span><span class="sxs-lookup"><span data-stu-id="2ee12-114">Creating a new query is the first step toward creating a compound query.</span></span>

## <a name="examples"></a><span data-ttu-id="2ee12-115">範例</span><span class="sxs-lookup"><span data-stu-id="2ee12-115">Examples</span></span>

<span data-ttu-id="2ee12-116">下列範例會使用 `createQuery` 來取得初始化為 null 的 **IWMPQuery** 介面。</span><span class="sxs-lookup"><span data-stu-id="2ee12-116">The following example uses `createQuery` to get an **IWMPQuery** interface that is initialized to null.</span></span> <span data-ttu-id="2ee12-117">因為此查詢並未加入任何條件，所以當它當做 **getStringCollectionByQuery** 方法中的引數使用時，方法會傳回包含指定媒體類型之所有媒體專案的字串集合。</span><span class="sxs-lookup"><span data-stu-id="2ee12-117">Because this query has no conditions added to it, when it is used as an argument in the **getStringCollectionByQuery** method, the method will return a string collection that contains all of the media items of the specified media type.</span></span> <span data-ttu-id="2ee12-118">接著會在清單方塊中顯示字串集合。</span><span class="sxs-lookup"><span data-stu-id="2ee12-118">The string collection is then displayed in a list box.</span></span>


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="2ee12-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ee12-119">Requirements</span></span>



| <span data-ttu-id="2ee12-120">需求</span><span class="sxs-lookup"><span data-stu-id="2ee12-120">Requirement</span></span> | <span data-ttu-id="2ee12-121">值</span><span class="sxs-lookup"><span data-stu-id="2ee12-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee12-122">版本</span><span class="sxs-lookup"><span data-stu-id="2ee12-122">Version</span></span><br/>   | <span data-ttu-id="2ee12-123">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="2ee12-123">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="2ee12-124">命名空間</span><span class="sxs-lookup"><span data-stu-id="2ee12-124">Namespace</span></span><br/> | <span data-ttu-id="2ee12-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2ee12-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2ee12-126">組件</span><span class="sxs-lookup"><span data-stu-id="2ee12-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2ee12-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="2ee12-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ee12-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ee12-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee12-129">**IWMPMediaCollection2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2ee12-129">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ee12-130">**IWMPQuery 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2ee12-130">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





