---
title: MediaCollectionMediaAdded 事件
description: 當媒體專案加入至本機程式庫時，就會發生 MediaCollectionMediaAdded 事件。 |MediaCollectionMediaAdded 事件
ms.assetid: 01696d28-e83b-4fd2-8e88-2871831b61e7
keywords:
- MediaCollectionMediaAdded 事件 Windows Media Player
- MediaCollectionMediaAdded 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaCollectionMediaAdded 事件
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18dd0536f508090c46f9fc5a9059c809f50091d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000471"
---
# <a name="playermediacollectionmediaadded-event"></a><span data-ttu-id="68f4b-107">MediaCollectionMediaAdded 事件</span><span class="sxs-lookup"><span data-stu-id="68f4b-107">Player.MediaCollectionMediaAdded event</span></span>

<span data-ttu-id="68f4b-108">當媒體專案加入至本機程式庫時，就會發生 MediaCollectionMediaAdded 事件。</span><span class="sxs-lookup"><span data-stu-id="68f4b-108">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f4b-109">語法</span><span class="sxs-lookup"><span data-stu-id="68f4b-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaAdded(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="68f4b-110">參數</span><span class="sxs-lookup"><span data-stu-id="68f4b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68f4b-111">*pdispMedia*</span><span class="sxs-lookup"><span data-stu-id="68f4b-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="68f4b-112">已新增的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="68f4b-112">**Media** object that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68f4b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="68f4b-113">Return value</span></span>

<span data-ttu-id="68f4b-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="68f4b-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68f4b-115">備註</span><span class="sxs-lookup"><span data-stu-id="68f4b-115">Remarks</span></span>

<span data-ttu-id="68f4b-116">只有本機程式庫才會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="68f4b-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="68f4b-117">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="68f4b-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="68f4b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="68f4b-118">Requirements</span></span>



| <span data-ttu-id="68f4b-119">需求</span><span class="sxs-lookup"><span data-stu-id="68f4b-119">Requirement</span></span> | <span data-ttu-id="68f4b-120">值</span><span class="sxs-lookup"><span data-stu-id="68f4b-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68f4b-121">版本</span><span class="sxs-lookup"><span data-stu-id="68f4b-121">Version</span></span><br/> | <span data-ttu-id="68f4b-122">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="68f4b-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="68f4b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="68f4b-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="68f4b-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68f4b-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68f4b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68f4b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f4b-126">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="68f4b-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="68f4b-127">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="68f4b-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="68f4b-128">**MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="68f4b-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





