---
title: BufferingCount
description: BufferingCount 屬性會捕獲在播放播放期間緩衝處理的次數。
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- BufferingCount Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999155"
---
# <a name="networkbufferingcount"></a><span data-ttu-id="c7270-104">BufferingCount</span><span class="sxs-lookup"><span data-stu-id="c7270-104">Network.bufferingCount</span></span>

<span data-ttu-id="c7270-105">**BufferingCount** 屬性會捕獲在播放播放期間緩衝處理的次數。</span><span class="sxs-lookup"><span data-stu-id="c7270-105">The **bufferingCount** property retrieves the number of times buffering occurred during clip playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7270-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7270-106">Syntax</span></span>

<span data-ttu-id="c7270-107">*玩家*。*網路*。**bufferingCount**</span><span class="sxs-lookup"><span data-stu-id="c7270-107">*player*.*network*.**bufferingCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c7270-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="c7270-108">Possible Values</span></span>

<span data-ttu-id="c7270-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="c7270-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7270-110">備註</span><span class="sxs-lookup"><span data-stu-id="c7270-110">Remarks</span></span>

<span data-ttu-id="c7270-111">每次播放都會停止並重新啟動，這個屬性會設定為零。</span><span class="sxs-lookup"><span data-stu-id="c7270-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="c7270-112">如果播放暫停，則不會重設。</span><span class="sxs-lookup"><span data-stu-id="c7270-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="c7270-113">緩衝處理只適用于串流內容。</span><span class="sxs-lookup"><span data-stu-id="c7270-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="c7270-114">這個屬性只會在執行時間于 *播放玩家* 時傳回有效的資訊。已設定 **URL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c7270-114">This property returns valid information only during run time when the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="c7270-115">範例</span><span class="sxs-lookup"><span data-stu-id="c7270-115">Examples</span></span>

<span data-ttu-id="c7270-116">下列 JScript 範例會使用 *網路*。**bufferingCount** ，以顯示在播放期間進行緩衝處理的次數。</span><span class="sxs-lookup"><span data-stu-id="c7270-116">The following JScript example uses *Network*.**bufferingCount** to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="c7270-117">這項資訊會顯示在以 ID = "CB" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="c7270-117">The information is displayed in an HTML DIV created with ID = "CB".</span></span> <span data-ttu-id="c7270-118">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="c7270-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="c7270-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7270-119">Requirements</span></span>



| <span data-ttu-id="c7270-120">需求</span><span class="sxs-lookup"><span data-stu-id="c7270-120">Requirement</span></span> | <span data-ttu-id="c7270-121">值</span><span class="sxs-lookup"><span data-stu-id="c7270-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7270-122">版本</span><span class="sxs-lookup"><span data-stu-id="c7270-122">Version</span></span><br/> | <span data-ttu-id="c7270-123">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c7270-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c7270-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c7270-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c7270-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7270-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7270-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7270-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7270-127">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="c7270-127">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="c7270-128">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="c7270-128">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





