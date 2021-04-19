---
title: Media Player. 緩衝事件
description: 當 Windows Media Player 控制項開始或結束緩衝或下載時，就會發生緩衝事件。 |Media Player. 緩衝事件
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- 緩衝事件 Windows Media Player
- 緩衝事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player、緩衝事件
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995698"
---
# <a name="playerbuffering-event"></a><span data-ttu-id="a1b35-107">Media Player. 緩衝事件</span><span class="sxs-lookup"><span data-stu-id="a1b35-107">Player.Buffering event</span></span>

<span data-ttu-id="a1b35-108">當 Windows Media Player 控制項開始或結束緩衝或下載時，就會發生 **緩衝** 事件。</span><span class="sxs-lookup"><span data-stu-id="a1b35-108">The **Buffering** event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b35-109">語法</span><span class="sxs-lookup"><span data-stu-id="a1b35-109">Syntax</span></span>


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a><span data-ttu-id="a1b35-110">參數</span><span class="sxs-lookup"><span data-stu-id="a1b35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b35-111">*開始*</span><span class="sxs-lookup"><span data-stu-id="a1b35-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b35-112">包含下列其中一個值的 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="a1b35-112">**Boolean** containing one of the following values.</span></span>



| <span data-ttu-id="a1b35-113">值</span><span class="sxs-lookup"><span data-stu-id="a1b35-113">Value</span></span> | <span data-ttu-id="a1b35-114">描述</span><span class="sxs-lookup"><span data-stu-id="a1b35-114">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="a1b35-115">true</span><span class="sxs-lookup"><span data-stu-id="a1b35-115">true</span></span>  | <span data-ttu-id="a1b35-116">已開始緩衝。</span><span class="sxs-lookup"><span data-stu-id="a1b35-116">Buffering has started.</span></span> |
| <span data-ttu-id="a1b35-117">false</span><span class="sxs-lookup"><span data-stu-id="a1b35-117">false</span></span> | <span data-ttu-id="a1b35-118">緩衝處理已結束。</span><span class="sxs-lookup"><span data-stu-id="a1b35-118">Buffering has ended.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b35-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1b35-119">Return value</span></span>

<span data-ttu-id="a1b35-120">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a1b35-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1b35-121">備註</span><span class="sxs-lookup"><span data-stu-id="a1b35-121">Remarks</span></span>

<span data-ttu-id="a1b35-122">您可以使用此事件來判斷何時啟動或停止緩衝或下載。</span><span class="sxs-lookup"><span data-stu-id="a1b35-122">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="a1b35-123">您可以針對案例和測試 *網路* 使用相同的事件區塊。**bufferingProgress** 和 *網路*。**downloadProgress** ，以判斷 Windows Media Player 目前是否正在緩衝或正在下載內容。</span><span class="sxs-lookup"><span data-stu-id="a1b35-123">You can use the same event block for both cases and test *Network*.**bufferingProgress** and *Network*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

<span data-ttu-id="a1b35-124">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="a1b35-124">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file by using the parameter name given.</span></span> <span data-ttu-id="a1b35-125">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="a1b35-125">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b35-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1b35-126">Requirements</span></span>



| <span data-ttu-id="a1b35-127">需求</span><span class="sxs-lookup"><span data-stu-id="a1b35-127">Requirement</span></span> | <span data-ttu-id="a1b35-128">值</span><span class="sxs-lookup"><span data-stu-id="a1b35-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b35-129">版本</span><span class="sxs-lookup"><span data-stu-id="a1b35-129">Version</span></span><br/> | <span data-ttu-id="a1b35-130">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a1b35-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a1b35-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a1b35-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="a1b35-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1b35-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b35-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1b35-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b35-134">**BufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="a1b35-134">**Network.bufferingProgress**</span></span>](network-bufferingprogress.md)
</dt> <dt>

[<span data-ttu-id="a1b35-135">**DownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="a1b35-135">**Network.downloadProgress**</span></span>](network-downloadprogress.md)
</dt> <dt>

[<span data-ttu-id="a1b35-136">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="a1b35-136">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





