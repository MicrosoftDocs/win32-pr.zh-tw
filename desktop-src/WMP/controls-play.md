---
title: 控制項. play 方法
description: Play 方法會導致目前的媒體專案開始播放，或繼續播放暫停的專案。
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- play 方法 Windows Media Player
- play 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player、play 方法
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999655"
---
# <a name="controlsplay-method"></a><span data-ttu-id="fb193-106">控制項. play 方法</span><span class="sxs-lookup"><span data-stu-id="fb193-106">Controls.play method</span></span>

<span data-ttu-id="fb193-107">**Play** 方法會導致目前的媒體專案開始播放，或繼續播放暫停的專案。</span><span class="sxs-lookup"><span data-stu-id="fb193-107">The **play** method causes the current media item to start playing, or resumes play of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb193-108">語法</span><span class="sxs-lookup"><span data-stu-id="fb193-108">Syntax</span></span>


```JScript
Controls.play()
```



## <a name="parameters"></a><span data-ttu-id="fb193-109">參數</span><span class="sxs-lookup"><span data-stu-id="fb193-109">Parameters</span></span>

<span data-ttu-id="fb193-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fb193-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb193-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb193-111">Return value</span></span>

<span data-ttu-id="fb193-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fb193-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb193-113">備註</span><span class="sxs-lookup"><span data-stu-id="fb193-113">Remarks</span></span>

<span data-ttu-id="fb193-114">如果在快速轉送或倒轉時呼叫這個方法，則 *設定* 的值。**速率** 設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="fb193-114">If this method is called while fast-forwarding or rewinding, the value of *Settings*.**rate** is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="fb193-115">範例</span><span class="sxs-lookup"><span data-stu-id="fb193-115">Examples</span></span>

<span data-ttu-id="fb193-116">下列範例會建立 HTML BUTTON 專案，此專案會使用 **播放** 來播放目前的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="fb193-116">The following example creates an HTML BUTTON element that uses **play** to play the current media item.</span></span> <span data-ttu-id="fb193-117">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="fb193-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="fb193-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb193-118">Requirements</span></span>



| <span data-ttu-id="fb193-119">需求</span><span class="sxs-lookup"><span data-stu-id="fb193-119">Requirement</span></span> | <span data-ttu-id="fb193-120">值</span><span class="sxs-lookup"><span data-stu-id="fb193-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb193-121">版本</span><span class="sxs-lookup"><span data-stu-id="fb193-121">Version</span></span><br/> | <span data-ttu-id="fb193-122">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="fb193-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fb193-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fb193-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb193-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb193-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb193-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb193-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb193-126">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="fb193-126">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





