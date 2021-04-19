---
title: PositionChange 事件
description: 當媒體專案目前的位置已變更時，就會發生 PositionChange 事件。
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- PositionChange 事件 Windows Media Player
- PositionChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，PositionChange 事件
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999219"
---
# <a name="playerpositionchange-event"></a><span data-ttu-id="e5b55-106">PositionChange 事件</span><span class="sxs-lookup"><span data-stu-id="e5b55-106">Player.PositionChange event</span></span>

<span data-ttu-id="e5b55-107">當媒體專案目前的位置已變更時，就會發生 **PositionChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="e5b55-107">The **PositionChange** event occurs when the current position of the media item has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b55-108">語法</span><span class="sxs-lookup"><span data-stu-id="e5b55-108">Syntax</span></span>


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a><span data-ttu-id="e5b55-109">參數</span><span class="sxs-lookup"><span data-stu-id="e5b55-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b55-110">*oldPosition*</span><span class="sxs-lookup"><span data-stu-id="e5b55-110">*oldPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="e5b55-111">指定舊位置)  (**雙精度浮** 點數。</span><span class="sxs-lookup"><span data-stu-id="e5b55-111">Number (**double**) specifying the old position.</span></span>

</dd> <dt>

<span data-ttu-id="e5b55-112">*newPosition*</span><span class="sxs-lookup"><span data-stu-id="e5b55-112">*newPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="e5b55-113">) 指定新位置 (**雙精度浮\*\*\*\*點數**。</span><span class="sxs-lookup"><span data-stu-id="e5b55-113">**Number** (**double**) specifying the new position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b55-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5b55-114">Return value</span></span>

<span data-ttu-id="e5b55-115">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e5b55-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5b55-116">備註</span><span class="sxs-lookup"><span data-stu-id="e5b55-116">Remarks</span></span>

<span data-ttu-id="e5b55-117">此事件不會在播放期間定期引發。</span><span class="sxs-lookup"><span data-stu-id="e5b55-117">This event is not raised routinely during playback.</span></span> <span data-ttu-id="e5b55-118">只有在主動變更播放媒體專案目前的位置，例如使用者移動搜尋控制碼或指定 *控制項* 值的程式碼時，才會發生此問題。**currentPosition**。</span><span class="sxs-lookup"><span data-stu-id="e5b55-118">It only occurs when something actively changes the current position of the playing media item, such as the user moving the seek handle or code specifying a value for *Controls*.**currentPosition**.</span></span>

<span data-ttu-id="e5b55-119">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="e5b55-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="e5b55-120">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="e5b55-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="e5b55-121">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="e5b55-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b55-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5b55-122">Requirements</span></span>



| <span data-ttu-id="e5b55-123">需求</span><span class="sxs-lookup"><span data-stu-id="e5b55-123">Requirement</span></span> | <span data-ttu-id="e5b55-124">值</span><span class="sxs-lookup"><span data-stu-id="e5b55-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b55-125">版本</span><span class="sxs-lookup"><span data-stu-id="e5b55-125">Version</span></span><br/> | <span data-ttu-id="e5b55-126">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e5b55-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e5b55-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e5b55-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="e5b55-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5b55-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b55-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5b55-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b55-130">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="e5b55-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





