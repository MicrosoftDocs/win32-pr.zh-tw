---
title: IsAvailable
description: IsAvailable 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。 |IsAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- IsAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976147"
---
# <a name="controlsisavailable"></a><span data-ttu-id="68468-105">IsAvailable</span><span class="sxs-lookup"><span data-stu-id="68468-105">Controls.isAvailable</span></span>

<span data-ttu-id="68468-106">**IsAvailable** 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="68468-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="68468-107">參數</span><span class="sxs-lookup"><span data-stu-id="68468-107">Parameters</span></span>

<span data-ttu-id="68468-108">*name*</span><span class="sxs-lookup"><span data-stu-id="68468-108">*name*</span></span>

<span data-ttu-id="68468-109">包含下列其中一個值的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="68468-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="68468-110">String</span><span class="sxs-lookup"><span data-stu-id="68468-110">String</span></span>          | <span data-ttu-id="68468-111">Description</span><span class="sxs-lookup"><span data-stu-id="68468-111">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68468-112">currentItem</span><span class="sxs-lookup"><span data-stu-id="68468-112">currentItem</span></span>     | <span data-ttu-id="68468-113">判斷使用者是否可以設定 **currentItem** 屬性。</span><span class="sxs-lookup"><span data-stu-id="68468-113">Determines whether the user can set the **currentItem** property.</span></span>                                                                                                 |
| <span data-ttu-id="68468-114">currentMarker</span><span class="sxs-lookup"><span data-stu-id="68468-114">currentMarker</span></span>   | <span data-ttu-id="68468-115">決定使用者是否可以搜尋特定標記。</span><span class="sxs-lookup"><span data-stu-id="68468-115">Determines whether the user can seek to a specific marker.</span></span>                                                                                                        |
| <span data-ttu-id="68468-116">currentPosition</span><span class="sxs-lookup"><span data-stu-id="68468-116">currentPosition</span></span> | <span data-ttu-id="68468-117">決定使用者是否可以搜尋檔案中的特定位置。</span><span class="sxs-lookup"><span data-stu-id="68468-117">Determines whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="68468-118">有些檔案不支援搜尋。</span><span class="sxs-lookup"><span data-stu-id="68468-118">Some files do not support seeking.</span></span>                                                       |
| <span data-ttu-id="68468-119">fastForward</span><span class="sxs-lookup"><span data-stu-id="68468-119">fastForward</span></span>     | <span data-ttu-id="68468-120">判斷檔案是否支援快速轉送以及是否可叫用該功能。</span><span class="sxs-lookup"><span data-stu-id="68468-120">Determines whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="68468-121">許多檔案類型 (或即時資料流) 不支援 fastForward。</span><span class="sxs-lookup"><span data-stu-id="68468-121">Many file types (or live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="68468-122">fastReverse</span><span class="sxs-lookup"><span data-stu-id="68468-122">fastReverse</span></span>     | <span data-ttu-id="68468-123">判斷檔案是否支援 fastReverse，以及是否可叫用該功能。</span><span class="sxs-lookup"><span data-stu-id="68468-123">Determines whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="68468-124">許多檔案類型 (或即時資料流) 不支援 fastReverse。</span><span class="sxs-lookup"><span data-stu-id="68468-124">Many file types (or live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="68468-125">下一步</span><span class="sxs-lookup"><span data-stu-id="68468-125">next</span></span>            | <span data-ttu-id="68468-126">決定使用者是否可以搜尋播放清單中的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="68468-126">Determines whether the user can seek to the next entry in a playlist.</span></span>                                                                                             |
| <span data-ttu-id="68468-127">pause</span><span class="sxs-lookup"><span data-stu-id="68468-127">pause</span></span>           | <span data-ttu-id="68468-128">判斷 **pause** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="68468-128">Determines whether the **pause** method is available.</span></span>                                                                                                             |
| <span data-ttu-id="68468-129">玩遊戲</span><span class="sxs-lookup"><span data-stu-id="68468-129">play</span></span>            | <span data-ttu-id="68468-130">判斷 **播放** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="68468-130">Determines whether the **play** method is available.</span></span>                                                                                                              |
| <span data-ttu-id="68468-131">previous</span><span class="sxs-lookup"><span data-stu-id="68468-131">previous</span></span>        | <span data-ttu-id="68468-132">決定使用者是否可以搜尋播放清單中的上一個專案。</span><span class="sxs-lookup"><span data-stu-id="68468-132">Determines whether the user can seek to the previous entry in a playlist.</span></span>                                                                                         |
| <span data-ttu-id="68468-133">步驟</span><span class="sxs-lookup"><span data-stu-id="68468-133">step</span></span>            | <span data-ttu-id="68468-134">判斷 **步驟** 方法在播放期間是否可用。</span><span class="sxs-lookup"><span data-stu-id="68468-134">Determines whether the **step** method is available during playback.</span></span>                                                                                              |
| <span data-ttu-id="68468-135">stop</span><span class="sxs-lookup"><span data-stu-id="68468-135">stop</span></span>            | <span data-ttu-id="68468-136">判斷 **停止** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="68468-136">Determines whether the **stop** method is available.</span></span>                                                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="68468-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="68468-137">Return Values</span></span>

<span data-ttu-id="68468-138">這個方法會傳回 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="68468-138">This method returns a **Boolean** value.</span></span>

## <a name="examples"></a><span data-ttu-id="68468-139">範例</span><span class="sxs-lookup"><span data-stu-id="68468-139">Examples</span></span>

<span data-ttu-id="68468-140">下列範例會建立 HTML BUTTON 元素，以搜尋目前媒體專案的開始位置。</span><span class="sxs-lookup"><span data-stu-id="68468-140">The following example creates an HTML BUTTON element that seeks to the starting position of the current media item.</span></span> <span data-ttu-id="68468-141">JScript 程式碼會使用 **isAvailable** 來驗證檔案是否支援搜尋作業。</span><span class="sxs-lookup"><span data-stu-id="68468-141">The JScript code uses **isAvailable** to verify that the file supports the seek operation.</span></span> <span data-ttu-id="68468-142">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="68468-142">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a><span data-ttu-id="68468-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="68468-143">Requirements</span></span>



| <span data-ttu-id="68468-144">需求</span><span class="sxs-lookup"><span data-stu-id="68468-144">Requirement</span></span> | <span data-ttu-id="68468-145">值</span><span class="sxs-lookup"><span data-stu-id="68468-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68468-146">版本</span><span class="sxs-lookup"><span data-stu-id="68468-146">Version</span></span><br/> | <span data-ttu-id="68468-147">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="68468-147">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="68468-148">DLL</span><span class="sxs-lookup"><span data-stu-id="68468-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="68468-149"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68468-149"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68468-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68468-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68468-151">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="68468-151">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





