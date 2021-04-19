---
title: CurrentMarker
description: CurrentMarker 屬性會指定或抓取目前的標記編號。
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- CurrentMarker Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995366"
---
# <a name="controlscurrentmarker"></a><span data-ttu-id="8e7db-104">CurrentMarker</span><span class="sxs-lookup"><span data-stu-id="8e7db-104">Controls.currentMarker</span></span>

<span data-ttu-id="8e7db-105">**CurrentMarker** 屬性會指定或抓取目前的標記編號。</span><span class="sxs-lookup"><span data-stu-id="8e7db-105">The **currentMarker** property specifies or retrieves the current marker number.</span></span>

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a><span data-ttu-id="8e7db-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="8e7db-106">Possible Values</span></span>

<span data-ttu-id="8e7db-107">此屬性是讀取/寫入 **號碼** (**長**) ，預設值為零。</span><span class="sxs-lookup"><span data-stu-id="8e7db-107">This property is a read/write **Number** (**long**) with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e7db-108">備註</span><span class="sxs-lookup"><span data-stu-id="8e7db-108">Remarks</span></span>

<span data-ttu-id="8e7db-109">設定 **currentMarker** 會導致播放從指定的標記開始。</span><span class="sxs-lookup"><span data-stu-id="8e7db-109">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="8e7db-110">在嘗試設定 **currentMarker** 之前，請先判斷檔案是否有標記以及使用 **markerCount** 有多少標記。</span><span class="sxs-lookup"><span data-stu-id="8e7db-110">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **markerCount**.</span></span> <span data-ttu-id="8e7db-111">如果檔案沒有標記，請將 **currentMarker** 設定為任何值，但不會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="8e7db-111">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="8e7db-112">將 **currentMarker** 設定為大於 **markerCount** 的數位也會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="8e7db-112">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="8e7db-113">**CurrentMarker** 屬性一律會傳回目前的或最後一個標記，這表示實際的檔案位置可以是目前標記或下一個標記之前的位置。</span><span class="sxs-lookup"><span data-stu-id="8e7db-113">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="8e7db-114">標記從1開始編號，因此，如果檔案有標記，您可以將 **currentMarker** 設定為零，將檔案位置變更為零。</span><span class="sxs-lookup"><span data-stu-id="8e7db-114">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="8e7db-115">直到目前的媒體專案設定 (使用 *Player* 為止。**URL** 或 *播放機*。**currentMedia**) ， **currentMarker** 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8e7db-115">Until the current media item is set (using *Player*.**URL** or *Player*.**currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="8e7db-116">範例</span><span class="sxs-lookup"><span data-stu-id="8e7db-116">Examples</span></span>

<span data-ttu-id="8e7db-117">下列 JScript 範例會使用 **currentMarker** ，從對應至 HTML SELECT 元素 **selectedIndex** 屬性的標記開始播放影片。</span><span class="sxs-lookup"><span data-stu-id="8e7db-117">The following JScript example uses **currentMarker** to start video playback from the marker that corresponds to the **selectedIndex** property of an HTML SELECT element.</span></span> <span data-ttu-id="8e7db-118">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="8e7db-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="8e7db-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e7db-119">Requirements</span></span>



| <span data-ttu-id="8e7db-120">需求</span><span class="sxs-lookup"><span data-stu-id="8e7db-120">Requirement</span></span> | <span data-ttu-id="8e7db-121">值</span><span class="sxs-lookup"><span data-stu-id="8e7db-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e7db-122">版本</span><span class="sxs-lookup"><span data-stu-id="8e7db-122">Version</span></span><br/> | <span data-ttu-id="8e7db-123">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8e7db-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8e7db-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8e7db-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="8e7db-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e7db-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e7db-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e7db-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e7db-127">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="8e7db-127">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="8e7db-128">**MarkerCount**</span><span class="sxs-lookup"><span data-stu-id="8e7db-128">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="8e7db-129">**CurrentMedia**</span><span class="sxs-lookup"><span data-stu-id="8e7db-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="8e7db-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="8e7db-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





