---
title: MaxBandwidth
description: MaxBandwidth 屬性會指定或抓取允許的最大頻寬。
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- MaxBandwidth Windows Media Player
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986164"
---
# <a name="networkmaxbandwidth"></a><span data-ttu-id="7bece-104">MaxBandwidth</span><span class="sxs-lookup"><span data-stu-id="7bece-104">Network.maxBandwidth</span></span>

<span data-ttu-id="7bece-105">**MaxBandwidth** 屬性會指定或抓取允許的最大頻寬。</span><span class="sxs-lookup"><span data-stu-id="7bece-105">The **maxBandwidth** property specifies or retrieves the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bece-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bece-106">Syntax</span></span>

<span data-ttu-id="7bece-107">*玩家*。*網路*。**maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="7bece-107">*player*.*network*.**maxBandwidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="7bece-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="7bece-108">Possible Values</span></span>

<span data-ttu-id="7bece-109">這個屬性是 (**長**) 的讀取/寫入 **號碼**。</span><span class="sxs-lookup"><span data-stu-id="7bece-109">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="7bece-110">備註</span><span class="sxs-lookup"><span data-stu-id="7bece-110">Remarks</span></span>

<span data-ttu-id="7bece-111">此屬性沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="7bece-111">This property has no default value.</span></span> <span data-ttu-id="7bece-112">當 Windows Media Player 現正播放時，可以指定其值，但在目前的媒體專案發行之前，只要開啟另一個媒體專案或呼叫 *Player*，變更就不會生效。**關閉**。</span><span class="sxs-lookup"><span data-stu-id="7bece-112">Its value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling *Player*.**close**.</span></span> <span data-ttu-id="7bece-113">Windows Media Player 嘗試達到可能的最高頻寬。</span><span class="sxs-lookup"><span data-stu-id="7bece-113">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="7bece-114">只有在設定值的情況下，才會減少任何頻寬。</span><span class="sxs-lookup"><span data-stu-id="7bece-114">Only in the case of the value being set will any bandwidth reduction occur.</span></span>

<span data-ttu-id="7bece-115">這項設定有助於減少使用的頻寬量，特別是在多位元率 (MBR) 串流的情況下。</span><span class="sxs-lookup"><span data-stu-id="7bece-115">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="7bece-116">MBR 資料流程包含多個具有不同位速率的資料流程。</span><span class="sxs-lookup"><span data-stu-id="7bece-116">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="7bece-117">在某些情況下，您可能會想要使用比用戶端所需的位元速率低的資料流程。</span><span class="sxs-lookup"><span data-stu-id="7bece-117">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="7bece-118">在此情況下，設定 **maxBandwidth** 屬性將會選取較低的位元速率串流。</span><span class="sxs-lookup"><span data-stu-id="7bece-118">In this case, setting the **maxBandwidth** property will select a lower bit-rate stream.</span></span>

<span data-ttu-id="7bece-119">例如，MBR 串流可能包含以每秒 20 kb 編碼的資料流程 (Kbps) 、37 Kbps 和 200 Kbps。</span><span class="sxs-lookup"><span data-stu-id="7bece-119">For example, an MBR stream could include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="7bece-120">將 **maxBandwidth** 屬性設定為 50000 (50 Kbps) 將會選取 37 kbps 資料流程，而不是 200 kbps 串流。</span><span class="sxs-lookup"><span data-stu-id="7bece-120">Setting the **maxBandwidth** property to 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bece-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7bece-121">Requirements</span></span>



| <span data-ttu-id="7bece-122">需求</span><span class="sxs-lookup"><span data-stu-id="7bece-122">Requirement</span></span> | <span data-ttu-id="7bece-123">值</span><span class="sxs-lookup"><span data-stu-id="7bece-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7bece-124">版本</span><span class="sxs-lookup"><span data-stu-id="7bece-124">Version</span></span><br/> | <span data-ttu-id="7bece-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7bece-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7bece-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7bece-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="7bece-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bece-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bece-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7bece-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bece-129">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="7bece-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="7bece-130">**Player. 關閉**</span><span class="sxs-lookup"><span data-stu-id="7bece-130">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





