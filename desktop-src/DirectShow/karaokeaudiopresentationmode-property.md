---
description: KaraokeAudioPresentationMode 屬性會設定或抓取輔助的卡拉卡拉板頻道的向左喇叭混合。
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: KaraokeAudioPresentationMode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972513"
---
# <a name="karaokeaudiopresentationmode-property"></a><span data-ttu-id="df9ad-103">KaraokeAudioPresentationMode 屬性</span><span class="sxs-lookup"><span data-stu-id="df9ad-103">KaraokeAudioPresentationMode Property</span></span>

> [!Note]  
> <span data-ttu-id="df9ad-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="df9ad-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="df9ad-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="df9ad-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="df9ad-106">`KaraokeAudioPresentationMode`屬性會設定或抓取輔助的卡拉卡拉板頻道的向左喇叭混合。</span><span class="sxs-lookup"><span data-stu-id="df9ad-106">The `KaraokeAudioPresentationMode` property sets or retrieves the right-left speaker mix for the auxiliary karaoke channels.</span></span>

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a><span data-ttu-id="df9ad-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="df9ad-107">Return Value</span></span>

<span data-ttu-id="df9ad-108">傳回整數值，其中包含一組位旗標，指出輔助的卡拉標頻道如何 downmixed 至左右喇叭。</span><span class="sxs-lookup"><span data-stu-id="df9ad-108">Returns an integer value containing a set of bit flags indicating how the auxiliary karaoke channels are downmixed to the left and right speakers.</span></span>

## <a name="remarks"></a><span data-ttu-id="df9ad-109">備註</span><span class="sxs-lookup"><span data-stu-id="df9ad-109">Remarks</span></span>

<span data-ttu-id="df9ad-110">此屬性是讀取/寫入，預設值為零。</span><span class="sxs-lookup"><span data-stu-id="df9ad-110">This property is read/write with a default value of zero.</span></span>

<span data-ttu-id="df9ad-111">音訊頻道是以零為基礎，因此通道0和1通常代表右邊和左邊的喇叭頻道，而頻道2到4則是三個輔助的卡拉卡拉。</span><span class="sxs-lookup"><span data-stu-id="df9ad-111">Audio channels are zero-based, so channels 0 and 1 generally represent the right and left speaker channels and channels 2 through 4 are the three auxiliary karaoke channels.</span></span> <span data-ttu-id="df9ad-112">當 MSWebDVD 物件進入卡拉 ok 模式時，它會自動靜音通道2和更新版本。</span><span class="sxs-lookup"><span data-stu-id="df9ad-112">When the MSWebDVD object enters karaoke mode, it automatically mutes channels 2 and higher.</span></span> <span data-ttu-id="df9ad-113">使用位 **or** 運算設定適當的位，以便將輔助通道傳送給左邊的喇叭、右邊的喇叭、兩位喇叭都 () 上的兩個位，或是沒有任何喇叭 () 的兩個位。</span><span class="sxs-lookup"><span data-stu-id="df9ad-113">Use bitwise **OR** operations to set the appropriate bit in order to send an auxiliary channel to the left speaker, right speaker, both speakers (both bits on), or to no speakers (both bits off).</span></span> <span data-ttu-id="df9ad-114">只要 DVD 導覽器進入 [卡拉 ok] 模式，這些位都預設為關閉。</span><span class="sxs-lookup"><span data-stu-id="df9ad-114">These bits are all off by default whenever the DVD Navigator enters karaoke mode.</span></span> <span data-ttu-id="df9ad-115">下表提供了位的值及其對應的動作。</span><span class="sxs-lookup"><span data-stu-id="df9ad-115">The value of the bits and their corresponding action is given in the following table.</span></span>



| <span data-ttu-id="df9ad-116">值</span><span class="sxs-lookup"><span data-stu-id="df9ad-116">Value</span></span>  | <span data-ttu-id="df9ad-117">描述</span><span class="sxs-lookup"><span data-stu-id="df9ad-117">Description</span></span>                            |
|--------|----------------------------------------|
| <span data-ttu-id="df9ad-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="df9ad-118">0x0004</span></span> | <span data-ttu-id="df9ad-119">Downmix Channel 2 至左方喇叭</span><span class="sxs-lookup"><span data-stu-id="df9ad-119">Downmix Channel 2 to the left speaker</span></span>  |
| <span data-ttu-id="df9ad-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="df9ad-120">0x0008</span></span> | <span data-ttu-id="df9ad-121">Downmix Channel 3 至左方喇叭</span><span class="sxs-lookup"><span data-stu-id="df9ad-121">Downmix Channel 3 to the left speaker</span></span>  |
| <span data-ttu-id="df9ad-122">0x0010</span><span class="sxs-lookup"><span data-stu-id="df9ad-122">0x0010</span></span> | <span data-ttu-id="df9ad-123">Downmix Channel 4 至左方喇叭</span><span class="sxs-lookup"><span data-stu-id="df9ad-123">Downmix Channel 4 to the left speaker</span></span>  |
| <span data-ttu-id="df9ad-124">0x0400</span><span class="sxs-lookup"><span data-stu-id="df9ad-124">0x0400</span></span> | <span data-ttu-id="df9ad-125">Downmix Channel 2 到右邊的喇叭</span><span class="sxs-lookup"><span data-stu-id="df9ad-125">Downmix Channel 2 to the right speaker</span></span> |
| <span data-ttu-id="df9ad-126">0x0800</span><span class="sxs-lookup"><span data-stu-id="df9ad-126">0x0800</span></span> | <span data-ttu-id="df9ad-127">Downmix Channel 3 到右邊的喇叭</span><span class="sxs-lookup"><span data-stu-id="df9ad-127">Downmix Channel 3 to the right speaker</span></span> |
| <span data-ttu-id="df9ad-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="df9ad-128">0x1000</span></span> | <span data-ttu-id="df9ad-129">Downmix Channel 4 到右邊的喇叭</span><span class="sxs-lookup"><span data-stu-id="df9ad-129">Downmix Channel 4 to the right speaker</span></span> |



 

 

 



