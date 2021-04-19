---
title: Controls. stop 方法
description: Stop 方法會停止播放媒體專案。 |Controls. stop 方法
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- stop 方法 Windows Media Player
- stop 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，stop 方法
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992896"
---
# <a name="controlsstop-method"></a><span data-ttu-id="07c45-107">Controls. stop 方法</span><span class="sxs-lookup"><span data-stu-id="07c45-107">Controls.stop method</span></span>

<span data-ttu-id="07c45-108">**Stop** 方法會停止播放媒體專案。</span><span class="sxs-lookup"><span data-stu-id="07c45-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c45-109">語法</span><span class="sxs-lookup"><span data-stu-id="07c45-109">Syntax</span></span>


```JScript
Controls.stop()
```



## <a name="parameters"></a><span data-ttu-id="07c45-110">參數</span><span class="sxs-lookup"><span data-stu-id="07c45-110">Parameters</span></span>

<span data-ttu-id="07c45-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="07c45-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07c45-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="07c45-112">Return value</span></span>

<span data-ttu-id="07c45-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="07c45-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07c45-114">備註</span><span class="sxs-lookup"><span data-stu-id="07c45-114">Remarks</span></span>

<span data-ttu-id="07c45-115">這個方法會使 Windows Media Player 釋出它所使用的任何系統資源，例如音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="07c45-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="07c45-116">但目前的媒體專案則不會釋出。</span><span class="sxs-lookup"><span data-stu-id="07c45-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="07c45-117">當播放程式停止時，播放軌會倒轉至一開始。</span><span class="sxs-lookup"><span data-stu-id="07c45-117">When the player is stopped, the track rewinds to the beginning.</span></span> <span data-ttu-id="07c45-118">然後呼叫 **play** 將開始播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="07c45-118">Calling **play** will then begin playback of the clip from the beginning.</span></span> <span data-ttu-id="07c45-119">若要在不變更目前位置的情況下暫停播放操作，請使用 **pause** 方法。</span><span class="sxs-lookup"><span data-stu-id="07c45-119">To halt a play operation without changing the current position, use the **pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="07c45-120">範例</span><span class="sxs-lookup"><span data-stu-id="07c45-120">Examples</span></span>

<span data-ttu-id="07c45-121">下列範例會建立 HTML BUTTON 元素，以使用 **stop** 停止播放。</span><span class="sxs-lookup"><span data-stu-id="07c45-121">The following example creates an HTML BUTTON element that uses **stop** to stop playback.</span></span> <span data-ttu-id="07c45-122">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="07c45-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
">

```



## <a name="requirements"></a><span data-ttu-id="07c45-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="07c45-123">Requirements</span></span>



| <span data-ttu-id="07c45-124">需求</span><span class="sxs-lookup"><span data-stu-id="07c45-124">Requirement</span></span> | <span data-ttu-id="07c45-125">值</span><span class="sxs-lookup"><span data-stu-id="07c45-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="07c45-126">版本</span><span class="sxs-lookup"><span data-stu-id="07c45-126">Version</span></span><br/> | <span data-ttu-id="07c45-127">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="07c45-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="07c45-128">DLL</span><span class="sxs-lookup"><span data-stu-id="07c45-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="07c45-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07c45-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c45-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07c45-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c45-131">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="07c45-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="07c45-132">**控制項。下一步**</span><span class="sxs-lookup"><span data-stu-id="07c45-132">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="07c45-133">**控制項。暫停**</span><span class="sxs-lookup"><span data-stu-id="07c45-133">**Controls.pause**</span></span>](controls-pause.md)
</dt> <dt>

[<span data-ttu-id="07c45-134">**控制項。上一個**</span><span class="sxs-lookup"><span data-stu-id="07c45-134">**Controls.previous**</span></span>](controls-previous.md)
</dt> </dl>

 

 





