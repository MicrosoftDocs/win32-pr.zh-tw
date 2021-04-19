---
title: PlaylistChange 事件
description: 當播放清單變更時，就會發生 PlaylistChange 事件。 |PlaylistChange 事件
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- PlaylistChange 事件 Windows Media Player
- PlaylistChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，PlaylistChange 事件
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993486"
---
# <a name="playerplaylistchange-event"></a><span data-ttu-id="10883-107">PlaylistChange 事件</span><span class="sxs-lookup"><span data-stu-id="10883-107">Player.PlaylistChange event</span></span>

<span data-ttu-id="10883-108">當播放清單變更時，就會發生 **PlaylistChange** 事件。</span><span class="sxs-lookup"><span data-stu-id="10883-108">The **PlaylistChange** event occurs when a playlist changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="10883-109">語法</span><span class="sxs-lookup"><span data-stu-id="10883-109">Syntax</span></span>


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a><span data-ttu-id="10883-110">參數</span><span class="sxs-lookup"><span data-stu-id="10883-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10883-111">*播放 清單*</span><span class="sxs-lookup"><span data-stu-id="10883-111">*Playlist*</span></span> 
</dt> <dd>

<span data-ttu-id="10883-112">變更的 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="10883-112">**Playlist** object which changed.</span></span>

</dd> <dt>

<span data-ttu-id="10883-113">*change*</span><span class="sxs-lookup"><span data-stu-id="10883-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="10883-114">**Number** (**long**) 指出播放清單所發生的變更類型。</span><span class="sxs-lookup"><span data-stu-id="10883-114">**Number** (**long**) indicating the type of change that occurred to the playlist.</span></span> <span data-ttu-id="10883-115">包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="10883-115">Contains one of the following values.</span></span>



| <span data-ttu-id="10883-116">Number</span><span class="sxs-lookup"><span data-stu-id="10883-116">Number</span></span> | <span data-ttu-id="10883-117">Name</span><span class="sxs-lookup"><span data-stu-id="10883-117">Name</span></span>          |
|--------|---------------|
| <span data-ttu-id="10883-118">0</span><span class="sxs-lookup"><span data-stu-id="10883-118">0</span></span>      | <span data-ttu-id="10883-119">Unknown</span><span class="sxs-lookup"><span data-stu-id="10883-119">Unknown</span></span>       |
| <span data-ttu-id="10883-120">1</span><span class="sxs-lookup"><span data-stu-id="10883-120">1</span></span>      | <span data-ttu-id="10883-121">清除</span><span class="sxs-lookup"><span data-stu-id="10883-121">Clear</span></span>         |
| <span data-ttu-id="10883-122">2</span><span class="sxs-lookup"><span data-stu-id="10883-122">2</span></span>      | <span data-ttu-id="10883-123">InfoChange</span><span class="sxs-lookup"><span data-stu-id="10883-123">InfoChange</span></span>    |
| <span data-ttu-id="10883-124">3</span><span class="sxs-lookup"><span data-stu-id="10883-124">3</span></span>      | <span data-ttu-id="10883-125">移動</span><span class="sxs-lookup"><span data-stu-id="10883-125">Move</span></span>          |
| <span data-ttu-id="10883-126">4</span><span class="sxs-lookup"><span data-stu-id="10883-126">4</span></span>      | <span data-ttu-id="10883-127">刪除</span><span class="sxs-lookup"><span data-stu-id="10883-127">Delete</span></span>        |
| <span data-ttu-id="10883-128">5</span><span class="sxs-lookup"><span data-stu-id="10883-128">5</span></span>      | <span data-ttu-id="10883-129">插入</span><span class="sxs-lookup"><span data-stu-id="10883-129">Insert</span></span>        |
| <span data-ttu-id="10883-130">6</span><span class="sxs-lookup"><span data-stu-id="10883-130">6</span></span>      | <span data-ttu-id="10883-131">Append</span><span class="sxs-lookup"><span data-stu-id="10883-131">Append</span></span>        |
| <span data-ttu-id="10883-132">7</span><span class="sxs-lookup"><span data-stu-id="10883-132">7</span></span>      | <span data-ttu-id="10883-133">不支援</span><span class="sxs-lookup"><span data-stu-id="10883-133">Not supported</span></span> |
| <span data-ttu-id="10883-134">8</span><span class="sxs-lookup"><span data-stu-id="10883-134">8</span></span>      | <span data-ttu-id="10883-135">NameChange</span><span class="sxs-lookup"><span data-stu-id="10883-135">NameChange</span></span>    |
| <span data-ttu-id="10883-136">9</span><span class="sxs-lookup"><span data-stu-id="10883-136">9</span></span>      | <span data-ttu-id="10883-137">不支援</span><span class="sxs-lookup"><span data-stu-id="10883-137">Not supported</span></span> |
| <span data-ttu-id="10883-138">10</span><span class="sxs-lookup"><span data-stu-id="10883-138">10</span></span>     | <span data-ttu-id="10883-139">Sort</span><span class="sxs-lookup"><span data-stu-id="10883-139">Sort</span></span>          |



 

<span data-ttu-id="10883-140">C 樣式的列舉常數可以藉由在名稱值前面加上 "wmplc" 來衍生。</span><span class="sxs-lookup"><span data-stu-id="10883-140">The C-style enumeration constant can be derived by prefixing the name value with "wmplc".</span></span> <span data-ttu-id="10883-141">例如，移動狀態的常數是 **wmplcMove**。</span><span class="sxs-lookup"><span data-stu-id="10883-141">For example, the constant for the Move state is **wmplcMove**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10883-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="10883-142">Return value</span></span>

<span data-ttu-id="10883-143">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="10883-143">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10883-144">備註</span><span class="sxs-lookup"><span data-stu-id="10883-144">Remarks</span></span>

<span data-ttu-id="10883-145">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="10883-145">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="10883-146">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="10883-146">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="10883-147">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="10883-147">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="10883-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="10883-148">Requirements</span></span>



| <span data-ttu-id="10883-149">需求</span><span class="sxs-lookup"><span data-stu-id="10883-149">Requirement</span></span> | <span data-ttu-id="10883-150">值</span><span class="sxs-lookup"><span data-stu-id="10883-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10883-151">版本</span><span class="sxs-lookup"><span data-stu-id="10883-151">Version</span></span><br/> | <span data-ttu-id="10883-152">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="10883-152">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="10883-153">DLL</span><span class="sxs-lookup"><span data-stu-id="10883-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="10883-154"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10883-154"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10883-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10883-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10883-156">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="10883-156">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





