---
title: MarkerCount
description: MarkerCount 屬性會抓取媒體專案中的標記數目。
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- MarkerCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987171"
---
# <a name="mediamarkercount"></a><span data-ttu-id="9d75a-104">MarkerCount</span><span class="sxs-lookup"><span data-stu-id="9d75a-104">Media.markerCount</span></span>

<span data-ttu-id="9d75a-105">**MarkerCount** 屬性會抓取媒體專案中的標記數目。</span><span class="sxs-lookup"><span data-stu-id="9d75a-105">The **markerCount** property retrieves the number of markers in the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d75a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d75a-106">Syntax</span></span>

<span data-ttu-id="9d75a-107">*玩家*。*currentMedia*。**markerCount**</span><span class="sxs-lookup"><span data-stu-id="9d75a-107">*player*.*currentMedia*.**markerCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="9d75a-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="9d75a-108">Possible Values</span></span>

<span data-ttu-id="9d75a-109">這個屬性是唯讀的 **數位** (**long**) 指定檔案中的標記數目。</span><span class="sxs-lookup"><span data-stu-id="9d75a-109">This property is a read-only **Number** (**long**) specifying the number of markers in the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d75a-110">備註</span><span class="sxs-lookup"><span data-stu-id="9d75a-110">Remarks</span></span>

<span data-ttu-id="9d75a-111">如果檔案沒有標記，或媒體專案與 *播放* 程式不同，則這個屬性會傳回零。**currentMedia**。</span><span class="sxs-lookup"><span data-stu-id="9d75a-111">This property returns zero if a file has no markers, or if the media item is not the same as *Player*.**currentMedia**.</span></span>

<span data-ttu-id="9d75a-112">標記數位從1開始。</span><span class="sxs-lookup"><span data-stu-id="9d75a-112">Marker numbers start at 1.</span></span>

<span data-ttu-id="9d75a-113">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="9d75a-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="9d75a-114">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="9d75a-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9d75a-115">範例</span><span class="sxs-lookup"><span data-stu-id="9d75a-115">Examples</span></span>

<span data-ttu-id="9d75a-116">下列 JScript 範例會使用 *媒體*。**markerCount** ，以取得目前媒體專案中的標記數目。</span><span class="sxs-lookup"><span data-stu-id="9d75a-116">The following JScript example uses *Media*.**markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="9d75a-117">該值接著會用來做為迴圈結構的上限，這會逐一查看標記清單來取出每個標記名稱。</span><span class="sxs-lookup"><span data-stu-id="9d75a-117">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name.</span></span> <span data-ttu-id="9d75a-118">名為 MNAMES 的 HTML TEXTAREA 元素會顯示目前媒體專案中的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="9d75a-118">An HTML TEXTAREA element named MNAMES displays the names of the markers in the current media item.</span></span> <span data-ttu-id="9d75a-119">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="9d75a-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="9d75a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d75a-120">Requirements</span></span>



| <span data-ttu-id="9d75a-121">需求</span><span class="sxs-lookup"><span data-stu-id="9d75a-121">Requirement</span></span> | <span data-ttu-id="9d75a-122">值</span><span class="sxs-lookup"><span data-stu-id="9d75a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d75a-123">版本</span><span class="sxs-lookup"><span data-stu-id="9d75a-123">Version</span></span><br/> | <span data-ttu-id="9d75a-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9d75a-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9d75a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9d75a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9d75a-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d75a-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d75a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d75a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d75a-128">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="9d75a-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="9d75a-129">**CurrentMedia**</span><span class="sxs-lookup"><span data-stu-id="9d75a-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="9d75a-130">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="9d75a-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="9d75a-131">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="9d75a-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





