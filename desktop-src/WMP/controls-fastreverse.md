---
title: FastReverse 方法
description: FastReverse 方法會以反向方向啟動媒體專案的快速掃描。
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- fastReverse 方法 Windows Media Player
- fastReverse 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，fastReverse 方法
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987079"
---
# <a name="controlsfastreverse-method"></a><span data-ttu-id="9dee2-106">FastReverse 方法</span><span class="sxs-lookup"><span data-stu-id="9dee2-106">Controls.fastReverse method</span></span>

<span data-ttu-id="9dee2-107">**FastReverse** 方法會以反向方向啟動媒體專案的快速掃描。</span><span class="sxs-lookup"><span data-stu-id="9dee2-107">The **fastReverse** method starts fast scanning of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dee2-108">語法</span><span class="sxs-lookup"><span data-stu-id="9dee2-108">Syntax</span></span>


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a><span data-ttu-id="9dee2-109">參數</span><span class="sxs-lookup"><span data-stu-id="9dee2-109">Parameters</span></span>

<span data-ttu-id="9dee2-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9dee2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9dee2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9dee2-111">Return value</span></span>

<span data-ttu-id="9dee2-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9dee2-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dee2-113">備註</span><span class="sxs-lookup"><span data-stu-id="9dee2-113">Remarks</span></span>

<span data-ttu-id="9dee2-114">**FastReverse** 方法會以正常速度的五倍反向掃描剪輯，如果是影片檔案，則只會顯示主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="9dee2-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="9dee2-115">叫用 **fastReverse** 會變更 *設定*。**rate** 屬性為5.0。</span><span class="sxs-lookup"><span data-stu-id="9dee2-115">Invoking **fastReverse** changes the *Settings*.**rate** property to  5.0.</span></span> <span data-ttu-id="9dee2-116">如果之後變更了 **速率** ，或呼叫了 **播放** 或 **停止** ，Windows Media Player 將會停止快速反轉。</span><span class="sxs-lookup"><span data-stu-id="9dee2-116">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="9dee2-117">如果專案是播放清單的一部分， **fastReverse** 就會在目前的播放軌開始時停止。比方說，如果 track 3 是在 **fastReverse** 中，當到達 track 3 的開頭時，Windows Media Player 將不會移至「追蹤2」。</span><span class="sxs-lookup"><span data-stu-id="9dee2-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="9dee2-118">呼叫 **fastReverse** 時，播放次數不會遞增。</span><span class="sxs-lookup"><span data-stu-id="9dee2-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="9dee2-119">如果您在 **fastReverse** 生效時呼叫 **fastForward** ， **fastReverse** 將會停止，而且 **fastForward** 將會開始。</span><span class="sxs-lookup"><span data-stu-id="9dee2-119">If you call **fastForward** while **fastReverse** is in effect, **fastReverse** will be stopped and **fastForward** will begin.</span></span>

<span data-ttu-id="9dee2-120">這個方法不適用於即時廣播和特定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9dee2-120">This method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="9dee2-121">若要判斷您是否可以在剪輯中使用快速反轉，請呼叫 **isAvailable** ( "FastReverse" ) 。</span><span class="sxs-lookup"><span data-stu-id="9dee2-121">To determine whether you can use fast reverse in a clip, call **isAvailable**("FastReverse").</span></span>

## <a name="examples"></a><span data-ttu-id="9dee2-122">範例</span><span class="sxs-lookup"><span data-stu-id="9dee2-122">Examples</span></span>

<span data-ttu-id="9dee2-123">下列範例會建立 HTML BUTTON 專案，以使用 **fastReverse** 來啟動媒體專案的快速反向播放。</span><span class="sxs-lookup"><span data-stu-id="9dee2-123">The following example creates an HTML BUTTON element that uses **fastReverse** to start fast-reverse play of the media item.</span></span> <span data-ttu-id="9dee2-124">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="9dee2-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a><span data-ttu-id="9dee2-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9dee2-125">Requirements</span></span>



| <span data-ttu-id="9dee2-126">需求</span><span class="sxs-lookup"><span data-stu-id="9dee2-126">Requirement</span></span> | <span data-ttu-id="9dee2-127">值</span><span class="sxs-lookup"><span data-stu-id="9dee2-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9dee2-128">版本</span><span class="sxs-lookup"><span data-stu-id="9dee2-128">Version</span></span><br/> | <span data-ttu-id="9dee2-129">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9dee2-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9dee2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9dee2-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="9dee2-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dee2-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dee2-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9dee2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dee2-133">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="9dee2-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="9dee2-134">**FastForward**</span><span class="sxs-lookup"><span data-stu-id="9dee2-134">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="9dee2-135">**IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="9dee2-135">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="9dee2-136">**控制項. play**</span><span class="sxs-lookup"><span data-stu-id="9dee2-136">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="9dee2-137">**控制項。停止**</span><span class="sxs-lookup"><span data-stu-id="9dee2-137">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="9dee2-138">**設定。費率**</span><span class="sxs-lookup"><span data-stu-id="9dee2-138">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





