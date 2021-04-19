---
title: Controls. pause 方法
description: Pause 方法會暫停播放媒體專案。 |Controls. pause 方法
ms.assetid: 7307a3b2-e5d6-4067-bdb5-38011565142a
keywords:
- pause 方法 Windows Media Player
- pause 方法 Windows Media Player、Controls 類別
- 控制項類別 Windows Media Player、pause 方法
topic_type:
- apiref
api_name:
- Controls.pause
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 898efb51355a1301bc76717f6d0184d0b30d619d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979517"
---
# <a name="controlspause-method"></a><span data-ttu-id="8c914-107">Controls. pause 方法</span><span class="sxs-lookup"><span data-stu-id="8c914-107">Controls.pause method</span></span>

<span data-ttu-id="8c914-108">**Pause** 方法會暫停播放媒體專案。</span><span class="sxs-lookup"><span data-stu-id="8c914-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c914-109">語法</span><span class="sxs-lookup"><span data-stu-id="8c914-109">Syntax</span></span>


```JScript
Controls.pause()
```



## <a name="parameters"></a><span data-ttu-id="8c914-110">參數</span><span class="sxs-lookup"><span data-stu-id="8c914-110">Parameters</span></span>

<span data-ttu-id="8c914-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8c914-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c914-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c914-112">Return value</span></span>

<span data-ttu-id="8c914-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8c914-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c914-114">備註</span><span class="sxs-lookup"><span data-stu-id="8c914-114">Remarks</span></span>

<span data-ttu-id="8c914-115">當檔案暫停時，Windows Media Player 不會提供任何系統資源，例如音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="8c914-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="8c914-116">某些媒體類型無法暫停，例如即時資料流。</span><span class="sxs-lookup"><span data-stu-id="8c914-116">Certain media types cannot be paused, such as live streams.</span></span> <span data-ttu-id="8c914-117">若要判斷特定媒體類型是否可以暫停，請使用 *控制項*。**isAvailable ( ' Pause ' )**。</span><span class="sxs-lookup"><span data-stu-id="8c914-117">To determine whether a particular media type can be paused, use *Controls*.**isAvailable('Pause')**.</span></span>

## <a name="examples"></a><span data-ttu-id="8c914-118">範例</span><span class="sxs-lookup"><span data-stu-id="8c914-118">Examples</span></span>

<span data-ttu-id="8c914-119">下列範例會建立 HTML BUTTON 專案，以使用 **pause** 來暫停播放。</span><span class="sxs-lookup"><span data-stu-id="8c914-119">The following example creates an HTML BUTTON element that uses **pause** to pause playback.</span></span> <span data-ttu-id="8c914-120">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c914-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PAUSE"  NAME = "PAUSE"  VALUE = "||"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Pause'))

            /* Pause the Player. */
            Player.controls.pause();
">
```



## <a name="requirements"></a><span data-ttu-id="8c914-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c914-121">Requirements</span></span>



| <span data-ttu-id="8c914-122">需求</span><span class="sxs-lookup"><span data-stu-id="8c914-122">Requirement</span></span> | <span data-ttu-id="8c914-123">值</span><span class="sxs-lookup"><span data-stu-id="8c914-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c914-124">版本</span><span class="sxs-lookup"><span data-stu-id="8c914-124">Version</span></span><br/> | <span data-ttu-id="8c914-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8c914-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8c914-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8c914-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c914-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c914-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c914-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c914-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c914-129">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="8c914-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="8c914-130">**IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="8c914-130">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> </dl>

 

 





