---
title: GetMarkerTime 方法
description: GetMarkerTime 方法會抓取位於指定索引處之標記的時間。
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- getMarkerTime 方法 Windows Media Player
- getMarkerTime 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getMarkerTime 方法
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000942"
---
# <a name="mediagetmarkertime-method"></a><span data-ttu-id="cf1a9-106">GetMarkerTime 方法</span><span class="sxs-lookup"><span data-stu-id="cf1a9-106">Media.getMarkerTime method</span></span>

<span data-ttu-id="cf1a9-107">**GetMarkerTime** 方法會抓取位於指定索引處之標記的時間。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-107">The **getMarkerTime** method retrieves the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf1a9-108">語法</span><span class="sxs-lookup"><span data-stu-id="cf1a9-108">Syntax</span></span>


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="cf1a9-109">參數</span><span class="sxs-lookup"><span data-stu-id="cf1a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf1a9-110">*markerNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf1a9-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf1a9-111">指定標記索引的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-111">**Number** (**long**) specifying the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf1a9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf1a9-112">Return value</span></span>

<span data-ttu-id="cf1a9-113">這個方法會傳回 **數位** (**雙精度**) 指定從剪輯開頭開始的標記位置（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-113">This method returns a **Number** (**double**) specifying the location of the marker in seconds from the beginning of the clip.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf1a9-114">備註</span><span class="sxs-lookup"><span data-stu-id="cf1a9-114">Remarks</span></span>

<span data-ttu-id="cf1a9-115">如果指定的標記不存在，這個方法會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="cf1a9-116">某些數位媒體專案不包含標記。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="cf1a9-117">使用 **markerCount** 來找出目前剪輯中有多少標記。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="cf1a9-118">標記索引編號從1開始。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="cf1a9-119">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="cf1a9-120">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cf1a9-121">範例</span><span class="sxs-lookup"><span data-stu-id="cf1a9-121">Examples</span></span>

<span data-ttu-id="cf1a9-122">下列 JScript 範例會使用 *媒體*。**getMarkerTime** ，以每個標記的位置填入名為 MTIMES 的 HTML TEXTAREA 元素。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-122">The following JScript example uses *Media*.**getMarkerTime** to fill an HTML TEXTAREA element named MTIMES with the location of each marker.</span></span> <span data-ttu-id="cf1a9-123">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="cf1a9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf1a9-124">Requirements</span></span>



| <span data-ttu-id="cf1a9-125">需求</span><span class="sxs-lookup"><span data-stu-id="cf1a9-125">Requirement</span></span> | <span data-ttu-id="cf1a9-126">值</span><span class="sxs-lookup"><span data-stu-id="cf1a9-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1a9-127">版本</span><span class="sxs-lookup"><span data-stu-id="cf1a9-127">Version</span></span><br/> | <span data-ttu-id="cf1a9-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="cf1a9-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cf1a9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cf1a9-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf1a9-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf1a9-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf1a9-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf1a9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf1a9-132">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="cf1a9-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="cf1a9-133">**GetMarkerName**</span><span class="sxs-lookup"><span data-stu-id="cf1a9-133">**Media.getMarkerName**</span></span>](media-getmarkername.md)
</dt> <dt>

[<span data-ttu-id="cf1a9-134">**MarkerCount**</span><span class="sxs-lookup"><span data-stu-id="cf1a9-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="cf1a9-135">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="cf1a9-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="cf1a9-136">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="cf1a9-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





