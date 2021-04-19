---
title: IWMPMedia markerCount 屬性
description: MarkerCount 屬性會取得媒體專案中的標記數目。
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- markerCount 屬性 Windows Media Player
- markerCount 屬性 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，markerCount 屬性
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad591d8be66dcd20bc5e59d206a637d9b1181f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987934"
---
# <a name="iwmpmediamarkercount-property"></a><span data-ttu-id="ad120-106">IWMPMedia：： markerCount 屬性</span><span class="sxs-lookup"><span data-stu-id="ad120-106">IWMPMedia::markerCount property</span></span>

<span data-ttu-id="ad120-107">**MarkerCount** 屬性會取得媒體專案中的標記數目。</span><span class="sxs-lookup"><span data-stu-id="ad120-107">The **markerCount** property gets the number of markers in the media item.</span></span>

<span data-ttu-id="ad120-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ad120-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad120-109">語法</span><span class="sxs-lookup"><span data-stu-id="ad120-109">Syntax</span></span>


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="ad120-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ad120-110">Property value</span></span>

<span data-ttu-id="ad120-111">為標記計數的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="ad120-111">A **System.Int32** that is the marker count.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad120-112">備註</span><span class="sxs-lookup"><span data-stu-id="ad120-112">Remarks</span></span>

<span data-ttu-id="ad120-113">如果檔案沒有標記，或媒體專案與 AxWindowsMediaPlayer. currentMedia 中所指定的不同，則這個屬性會傳回零。</span><span class="sxs-lookup"><span data-stu-id="ad120-113">This property returns zero if a file has no markers, or if the media item is not the same as the one specified in AxWindowsMediaPlayer.currentMedia.</span></span>

<span data-ttu-id="ad120-114">標記數位從1開始。</span><span class="sxs-lookup"><span data-stu-id="ad120-114">Marker numbers start at 1.</span></span>

<span data-ttu-id="ad120-115">使用這個屬性之前，您必須擁有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="ad120-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="ad120-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="ad120-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ad120-117">範例</span><span class="sxs-lookup"><span data-stu-id="ad120-117">Examples</span></span>

<span data-ttu-id="ad120-118">下列範例會使用 **markerCount** 來取出目前媒體專案中的標記數目。</span><span class="sxs-lookup"><span data-stu-id="ad120-118">The following example uses **markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="ad120-119">該值接著會用來做為迴圈結構的上限，這會逐一查看標記清單以抓取每個標記名稱，並將其顯示在多行文字方塊中。</span><span class="sxs-lookup"><span data-stu-id="ad120-119">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name and display it in a multi-line text box.</span></span> <span data-ttu-id="ad120-120">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="ad120-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a><span data-ttu-id="ad120-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad120-121">Requirements</span></span>



| <span data-ttu-id="ad120-122">需求</span><span class="sxs-lookup"><span data-stu-id="ad120-122">Requirement</span></span> | <span data-ttu-id="ad120-123">值</span><span class="sxs-lookup"><span data-stu-id="ad120-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad120-124">版本</span><span class="sxs-lookup"><span data-stu-id="ad120-124">Version</span></span><br/>   | <span data-ttu-id="ad120-125">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="ad120-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ad120-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="ad120-126">Namespace</span></span><br/> | <span data-ttu-id="ad120-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ad120-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ad120-128">組件</span><span class="sxs-lookup"><span data-stu-id="ad120-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ad120-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="ad120-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad120-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad120-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad120-131">**AxWindowsMediaPlayer. currentMedia (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ad120-131">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ad120-132">**IWMPMedia 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ad120-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





