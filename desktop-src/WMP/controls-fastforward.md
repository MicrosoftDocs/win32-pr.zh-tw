---
title: FastForward 方法
description: FastForward 方法會以正向方向啟動媒體專案的快速播放。 |FastForward 方法
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- fastForward 方法 Windows Media Player
- fastForward 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，fastForward 方法
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995699"
---
# <a name="controlsfastforward-method"></a><span data-ttu-id="9de46-107">FastForward 方法</span><span class="sxs-lookup"><span data-stu-id="9de46-107">Controls.fastForward method</span></span>

<span data-ttu-id="9de46-108">**FastForward** 方法會以正向方向啟動媒體專案的快速播放。</span><span class="sxs-lookup"><span data-stu-id="9de46-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="9de46-109">語法</span><span class="sxs-lookup"><span data-stu-id="9de46-109">Syntax</span></span>


```JScript
Controls.fastForward()
```



## <a name="parameters"></a><span data-ttu-id="9de46-110">參數</span><span class="sxs-lookup"><span data-stu-id="9de46-110">Parameters</span></span>

<span data-ttu-id="9de46-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9de46-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9de46-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9de46-112">Return value</span></span>

<span data-ttu-id="9de46-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9de46-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9de46-114">備註</span><span class="sxs-lookup"><span data-stu-id="9de46-114">Remarks</span></span>

<span data-ttu-id="9de46-115">**FastForward** 方法會以正常速度的五倍來播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="9de46-115">The **fastForward** method plays the clip back at five times the normal speed.</span></span> <span data-ttu-id="9de46-116">叫用 **fastForward** 會變更 *設定*。**rate** 屬性為5.0。</span><span class="sxs-lookup"><span data-stu-id="9de46-116">Invoking **fastForward** changes the *Settings*.**rate** property to 5.0.</span></span> <span data-ttu-id="9de46-117">如果之後變更了 **速率** ，或呼叫了 **播放** 或 **停止** ，Windows Media Player 將會停止快速轉送。</span><span class="sxs-lookup"><span data-stu-id="9de46-117">If **rate** is subsequently changed, or if **play** or **stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="9de46-118">**FastForward** 方法不適用於即時廣播和特定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9de46-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="9de46-119">若要判斷您是否可以在剪輯中向前快轉，請呼叫 **isAvailable** ( "FastForward" ) 。</span><span class="sxs-lookup"><span data-stu-id="9de46-119">To determine whether you can fast forward in a clip, call **isAvailable**("FastForward").</span></span>

## <a name="examples"></a><span data-ttu-id="9de46-120">範例</span><span class="sxs-lookup"><span data-stu-id="9de46-120">Examples</span></span>

<span data-ttu-id="9de46-121">下列範例會建立 HTML BUTTON 專案，以使用 **fastForward** 來啟動媒體專案的快速播放。</span><span class="sxs-lookup"><span data-stu-id="9de46-121">The following example creates an HTML BUTTON element that uses **fastForward** to start fast play of the media item.</span></span> <span data-ttu-id="9de46-122">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="9de46-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
">

```



## <a name="requirements"></a><span data-ttu-id="9de46-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9de46-123">Requirements</span></span>



| <span data-ttu-id="9de46-124">需求</span><span class="sxs-lookup"><span data-stu-id="9de46-124">Requirement</span></span> | <span data-ttu-id="9de46-125">值</span><span class="sxs-lookup"><span data-stu-id="9de46-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9de46-126">版本</span><span class="sxs-lookup"><span data-stu-id="9de46-126">Version</span></span><br/> | <span data-ttu-id="9de46-127">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="9de46-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9de46-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9de46-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="9de46-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9de46-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de46-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9de46-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de46-131">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="9de46-131">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="9de46-132">**IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="9de46-132">**Controls.isAvailable**</span></span>](controls-isavailable.md)
</dt> <dt>

[<span data-ttu-id="9de46-133">**控制項. play**</span><span class="sxs-lookup"><span data-stu-id="9de46-133">**Controls.play**</span></span>](controls-play.md)
</dt> <dt>

[<span data-ttu-id="9de46-134">**控制項。停止**</span><span class="sxs-lookup"><span data-stu-id="9de46-134">**Controls.stop**</span></span>](controls-stop.md)
</dt> <dt>

[<span data-ttu-id="9de46-135">**設定。費率**</span><span class="sxs-lookup"><span data-stu-id="9de46-135">**Settings.rate**</span></span>](settings-rate.md)
</dt> </dl>

 

 





