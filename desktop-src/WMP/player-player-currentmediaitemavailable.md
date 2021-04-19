---
title: CurrentMediaItemAvailable 事件
description: 當目前媒體專案中的圖形中繼資料專案變成可用時，就會發生 CurrentMediaItemAvailable 事件。 |CurrentMediaItemAvailable 事件
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- CurrentMediaItemAvailable 事件 Windows Media Player
- CurrentMediaItemAvailable 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，CurrentMediaItemAvailable 事件
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990045"
---
# <a name="playercurrentmediaitemavailable-event"></a><span data-ttu-id="4474b-107">CurrentMediaItemAvailable 事件</span><span class="sxs-lookup"><span data-stu-id="4474b-107">Player.CurrentMediaItemAvailable event</span></span>

<span data-ttu-id="4474b-108">當目前媒體專案中的圖形中繼資料專案變成可用時，就會發生 **CurrentMediaItemAvailable** 事件。</span><span class="sxs-lookup"><span data-stu-id="4474b-108">The **CurrentMediaItemAvailable** event occurs when a graphic metadata item in the current media item becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="4474b-109">語法</span><span class="sxs-lookup"><span data-stu-id="4474b-109">Syntax</span></span>


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="4474b-110">參數</span><span class="sxs-lookup"><span data-stu-id="4474b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4474b-111">*bstrItemName*</span><span class="sxs-lookup"><span data-stu-id="4474b-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="4474b-112">包含目前媒體專案名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="4474b-112">**String** containing the name of the current media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4474b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4474b-113">Return value</span></span>

<span data-ttu-id="4474b-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4474b-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4474b-115">備註</span><span class="sxs-lookup"><span data-stu-id="4474b-115">Remarks</span></span>

<span data-ttu-id="4474b-116">因為播放可以在媒體專案完全下載之前開始播放，所以媒體專案中包含的任何元資料圖形 (例如專輯封面) 在開始播放時可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="4474b-116">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="4474b-117">此事件會在元資料圖形專案完成下載時發出警示。</span><span class="sxs-lookup"><span data-stu-id="4474b-117">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="4474b-118">然後，您可以藉由將 *bstrItemName* 的值傳遞給 *MediaCollection*，來取得 **媒體** 物件。**getByName** 方法，之後您就可以使用 *媒體* 來存取元資料圖形專案。**getItemInfoByType** 並為屬性名稱指定 **WM/圖片**。</span><span class="sxs-lookup"><span data-stu-id="4474b-118">You can then retrieve the **Media** object by passing the value of *bstrItemName* to the *MediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *Media*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

<span data-ttu-id="4474b-119">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="4474b-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="4474b-120">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="4474b-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="4474b-121">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4474b-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4474b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4474b-122">Requirements</span></span>



| <span data-ttu-id="4474b-123">需求</span><span class="sxs-lookup"><span data-stu-id="4474b-123">Requirement</span></span> | <span data-ttu-id="4474b-124">值</span><span class="sxs-lookup"><span data-stu-id="4474b-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4474b-125">版本</span><span class="sxs-lookup"><span data-stu-id="4474b-125">Version</span></span><br/> | <span data-ttu-id="4474b-126">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="4474b-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4474b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4474b-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="4474b-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4474b-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4474b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4474b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4474b-130">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="4474b-130">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="4474b-131">**GetItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="4474b-131">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="4474b-132">**MediaCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="4474b-132">**MediaCollection.getByName**</span></span>](mediacollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="4474b-133">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="4474b-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





