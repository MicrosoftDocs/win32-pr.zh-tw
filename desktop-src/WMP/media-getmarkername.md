---
title: GetMarkerName 方法
description: GetMarkerName 方法會在指定的索引處，抓取標記的名稱。
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- getMarkerName 方法 Windows Media Player
- getMarkerName 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getMarkerName 方法
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996471"
---
# <a name="mediagetmarkername-method"></a><span data-ttu-id="34fde-106">GetMarkerName 方法</span><span class="sxs-lookup"><span data-stu-id="34fde-106">Media.getMarkerName method</span></span>

<span data-ttu-id="34fde-107">**GetMarkerName** 方法會在指定的索引處，抓取標記的名稱。</span><span class="sxs-lookup"><span data-stu-id="34fde-107">The **getMarkerName** method retrieves the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="34fde-108">語法</span><span class="sxs-lookup"><span data-stu-id="34fde-108">Syntax</span></span>


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="34fde-109">參數</span><span class="sxs-lookup"><span data-stu-id="34fde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34fde-110">*markerNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34fde-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34fde-111">指定標記索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="34fde-111">**Number** (**long**) specifying a marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34fde-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="34fde-112">Return value</span></span>

<span data-ttu-id="34fde-113">這個方法會傳回 **字串**。</span><span class="sxs-lookup"><span data-stu-id="34fde-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="34fde-114">備註</span><span class="sxs-lookup"><span data-stu-id="34fde-114">Remarks</span></span>

<span data-ttu-id="34fde-115">如果指定的標記不存在，這個方法會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="34fde-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="34fde-116">某些數位媒體專案不包含標記。</span><span class="sxs-lookup"><span data-stu-id="34fde-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="34fde-117">使用 **markerCount** 來找出目前剪輯中有多少標記。</span><span class="sxs-lookup"><span data-stu-id="34fde-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="34fde-118">標記索引編號從1開始。</span><span class="sxs-lookup"><span data-stu-id="34fde-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="34fde-119">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="34fde-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="34fde-120">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="34fde-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="34fde-121">範例</span><span class="sxs-lookup"><span data-stu-id="34fde-121">Examples</span></span>

<span data-ttu-id="34fde-122">下列 JScript 範例會使用 *媒體*。**getMarkerName** ，以目前媒體專案中的標記名稱填入名為 MNAMES 的 HTML TEXTAREA 元素。</span><span class="sxs-lookup"><span data-stu-id="34fde-122">The following JScript example uses *Media*.**getMarkerName** to fill an HTML TEXTAREA element named MNAMES with the names of the markers in the current media item.</span></span> <span data-ttu-id="34fde-123">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="34fde-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="34fde-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="34fde-124">Requirements</span></span>



| <span data-ttu-id="34fde-125">需求</span><span class="sxs-lookup"><span data-stu-id="34fde-125">Requirement</span></span> | <span data-ttu-id="34fde-126">值</span><span class="sxs-lookup"><span data-stu-id="34fde-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34fde-127">版本</span><span class="sxs-lookup"><span data-stu-id="34fde-127">Version</span></span><br/> | <span data-ttu-id="34fde-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="34fde-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="34fde-129">DLL</span><span class="sxs-lookup"><span data-stu-id="34fde-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="34fde-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34fde-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34fde-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34fde-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34fde-132">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="34fde-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="34fde-133">**GetMarkerTime**</span><span class="sxs-lookup"><span data-stu-id="34fde-133">**Media.getMarkerTime**</span></span>](media-getmarkertime.md)
</dt> <dt>

[<span data-ttu-id="34fde-134">**MarkerCount**</span><span class="sxs-lookup"><span data-stu-id="34fde-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="34fde-135">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="34fde-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="34fde-136">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="34fde-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





