---
title: MediaCollectionMediaRemoved 事件
description: 從本機程式庫移除媒體專案時，就會發生 MediaCollectionMediaRemoved 事件。 |MediaCollectionMediaRemoved 事件
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- MediaCollectionMediaRemoved 事件 Windows Media Player
- MediaCollectionMediaRemoved 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，MediaCollectionMediaRemoved 事件
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993543"
---
# <a name="playermediacollectionmediaremoved-event"></a><span data-ttu-id="aa9dc-107">MediaCollectionMediaRemoved 事件</span><span class="sxs-lookup"><span data-stu-id="aa9dc-107">Player.MediaCollectionMediaRemoved event</span></span>

<span data-ttu-id="aa9dc-108">從本機程式庫移除媒體專案時，就會發生 MediaCollectionMediaRemoved 事件。</span><span class="sxs-lookup"><span data-stu-id="aa9dc-108">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9dc-109">語法</span><span class="sxs-lookup"><span data-stu-id="aa9dc-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="aa9dc-110">參數</span><span class="sxs-lookup"><span data-stu-id="aa9dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa9dc-111">*pdispMedia*</span><span class="sxs-lookup"><span data-stu-id="aa9dc-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="aa9dc-112">已移除的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="aa9dc-112">**Media** object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa9dc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="aa9dc-113">Return value</span></span>

<span data-ttu-id="aa9dc-114">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aa9dc-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa9dc-115">備註</span><span class="sxs-lookup"><span data-stu-id="aa9dc-115">Remarks</span></span>

<span data-ttu-id="aa9dc-116">只有本機程式庫才會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="aa9dc-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="aa9dc-117">**Windows Media Player 10** 行動裝置版：不支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aa9dc-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa9dc-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa9dc-118">Requirements</span></span>



| <span data-ttu-id="aa9dc-119">需求</span><span class="sxs-lookup"><span data-stu-id="aa9dc-119">Requirement</span></span> | <span data-ttu-id="aa9dc-120">值</span><span class="sxs-lookup"><span data-stu-id="aa9dc-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9dc-121">版本</span><span class="sxs-lookup"><span data-stu-id="aa9dc-121">Version</span></span><br/> | <span data-ttu-id="aa9dc-122">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="aa9dc-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="aa9dc-123">DLL</span><span class="sxs-lookup"><span data-stu-id="aa9dc-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="aa9dc-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa9dc-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9dc-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa9dc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9dc-126">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="aa9dc-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="aa9dc-127">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="aa9dc-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="aa9dc-128">**MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="aa9dc-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





