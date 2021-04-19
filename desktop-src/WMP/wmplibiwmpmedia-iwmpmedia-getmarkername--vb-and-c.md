---
title: IWMPMedia getMarkerName 方法
description: GetMarkerName 方法會傳回指定索引處的標記名稱。
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- getMarkerName 方法 Windows Media Player
- getMarkerName 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，getMarkerName 方法
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987935"
---
# <a name="iwmpmediagetmarkername-method"></a><span data-ttu-id="40a35-106">IWMPMedia：： getMarkerName 方法</span><span class="sxs-lookup"><span data-stu-id="40a35-106">IWMPMedia::getMarkerName method</span></span>

<span data-ttu-id="40a35-107">**GetMarkerName** 方法會傳回指定索引處的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="40a35-107">The **getMarkerName** method returns the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a35-108">語法</span><span class="sxs-lookup"><span data-stu-id="40a35-108">Syntax</span></span>


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a><span data-ttu-id="40a35-109">參數</span><span class="sxs-lookup"><span data-stu-id="40a35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a35-110">*MarkerNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40a35-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40a35-111">是標記索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="40a35-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a35-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="40a35-112">Return value</span></span>

<span data-ttu-id="40a35-113">**System.string** ，這是標記名稱。</span><span class="sxs-lookup"><span data-stu-id="40a35-113">A **System.String** that is the marker name.</span></span>

## <a name="remarks"></a><span data-ttu-id="40a35-114">備註</span><span class="sxs-lookup"><span data-stu-id="40a35-114">Remarks</span></span>

<span data-ttu-id="40a35-115">如果指定的標記不存在，這個方法會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="40a35-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="40a35-116">有些媒體專案不包含標記。</span><span class="sxs-lookup"><span data-stu-id="40a35-116">Some media items do not contain markers.</span></span> <span data-ttu-id="40a35-117">使用 **markerCount** 來找出目前媒體專案中有多少標記。</span><span class="sxs-lookup"><span data-stu-id="40a35-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="40a35-118">標記索引編號從1開始。</span><span class="sxs-lookup"><span data-stu-id="40a35-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="40a35-119">在呼叫這個方法之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="40a35-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="40a35-120">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="40a35-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="40a35-121">範例</span><span class="sxs-lookup"><span data-stu-id="40a35-121">Examples</span></span>

<span data-ttu-id="40a35-122">下列程式碼範例會使用 **getMarkerName** ，以目前媒體專案中的標記名稱填滿多行文字方塊。</span><span class="sxs-lookup"><span data-stu-id="40a35-122">The following code example uses **getMarkerName** to fill a multi-line text box with the names of the markers in the current media item.</span></span> <span data-ttu-id="40a35-123">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="40a35-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a><span data-ttu-id="40a35-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="40a35-124">Requirements</span></span>



| <span data-ttu-id="40a35-125">需求</span><span class="sxs-lookup"><span data-stu-id="40a35-125">Requirement</span></span> | <span data-ttu-id="40a35-126">值</span><span class="sxs-lookup"><span data-stu-id="40a35-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40a35-127">版本</span><span class="sxs-lookup"><span data-stu-id="40a35-127">Version</span></span><br/>   | <span data-ttu-id="40a35-128">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="40a35-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="40a35-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="40a35-129">Namespace</span></span><br/> | <span data-ttu-id="40a35-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="40a35-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="40a35-131">組件</span><span class="sxs-lookup"><span data-stu-id="40a35-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="40a35-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="40a35-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a35-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40a35-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a35-134">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="40a35-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="40a35-135">**IWMPMedia. markerCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="40a35-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





