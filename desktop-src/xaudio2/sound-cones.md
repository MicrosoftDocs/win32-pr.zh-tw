---
description: 描述導向音效音量的模型。
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: 音效圓錐
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996946"
---
# <a name="sound-cones"></a><span data-ttu-id="06c03-103">音效圓錐</span><span class="sxs-lookup"><span data-stu-id="06c03-103">Sound Cones</span></span>

<span data-ttu-id="06c03-104">描述導向音效音量的模型。</span><span class="sxs-lookup"><span data-stu-id="06c03-104">A model that describes the loudness of oriented sound.</span></span>

<span data-ttu-id="06c03-105">沒有方向的音效在所有方向的指定距離都有相同的波幅。</span><span class="sxs-lookup"><span data-stu-id="06c03-105">A sound with no orientation has the same amplitude at a given distance in all directions.</span></span> <span data-ttu-id="06c03-106">方向的音效會以方向 loudest。</span><span class="sxs-lookup"><span data-stu-id="06c03-106">A sound with an orientation is loudest in the direction of orientation.</span></span> <span data-ttu-id="06c03-107">描述導向音效音量的模型稱為「音效錐形」。</span><span class="sxs-lookup"><span data-stu-id="06c03-107">The model that describes the loudness of the oriented sound is called a sound cone.</span></span> <span data-ttu-id="06c03-108">音效的錐形是由內部 (或內部) 錐形和 (外部) 錐形所組成。</span><span class="sxs-lookup"><span data-stu-id="06c03-108">Sound cones are made up of an inside (or inner) cone and an outside (or outer) cone.</span></span> <span data-ttu-id="06c03-109">外的錐形角度必須一律等於或大於內錐角度。</span><span class="sxs-lookup"><span data-stu-id="06c03-109">The outside cone angle must always be equal to or greater than the inside cone angle.</span></span>

<span data-ttu-id="06c03-110">在內部錐形內的任何角度，音效的音量會設定為內部錐量。</span><span class="sxs-lookup"><span data-stu-id="06c03-110">At any angle within the inner cone, the volume of the sound is set to the inner cone volume.</span></span> <span data-ttu-id="06c03-111">這會考慮緩衝區的基本磁碟區、接聽程式的距離、接聽程式的方向（如果接聽程式有自己的錐形）等等。</span><span class="sxs-lookup"><span data-stu-id="06c03-111">This takes into account the basic volume of the buffer, the distance from the listener, the listener's orientation if the listener has its own cone, and so on.</span></span>

<span data-ttu-id="06c03-112">在外部錐形以外的任何角度，標準磁片區是由應用程式所設定的因素所衰減。</span><span class="sxs-lookup"><span data-stu-id="06c03-112">At any angle outside the outer cone, the normal volume is attenuated by a factor set by the application.</span></span> <span data-ttu-id="06c03-113">外部錐形音量層級是以線性振幅 scaler 表示： 1.0 f 代表未套用至原始信號的衰減，0.5 f 代表6個資料庫的衰減，而 0.0 f 表示無回應。</span><span class="sxs-lookup"><span data-stu-id="06c03-113">The outside cone volume level is expressed as a linear amplitude scaler: 1.0 f represents no attenuation applied to the original signal, 0.5 f denotes an attenuation of 6 dB, and 0.0 f results in silence.</span></span> <span data-ttu-id="06c03-114">也允許放大 (磁片區 > 1.0 f) ，且不會壓制。</span><span class="sxs-lookup"><span data-stu-id="06c03-114">Amplification (volume > 1.0 f) is also allowed, and is not clamped.</span></span> <span data-ttu-id="06c03-115">有效的磁片區範圍實際上是 0.0 f 到 2.0 f。</span><span class="sxs-lookup"><span data-stu-id="06c03-115">The valid volume range is actually 0.0 f to 2.0 f.</span></span>

<span data-ttu-id="06c03-116">內部和外部圓錐之間的範圍是從內部和外部的磁片區轉換到外部磁片區。</span><span class="sxs-lookup"><span data-stu-id="06c03-116">Between the inner and outer cones is a zone of transition from the inside volume to the outside volume.</span></span> <span data-ttu-id="06c03-117">當角度增加時，音量會接近錐形的外部音量。</span><span class="sxs-lookup"><span data-stu-id="06c03-117">The volume approaches the cone's outer volume as the angle increases.</span></span>

<span data-ttu-id="06c03-118">圓錐可能會影響磁片區以外的參數。</span><span class="sxs-lookup"><span data-stu-id="06c03-118">Cones can affect parameters other than volume.</span></span> <span data-ttu-id="06c03-119">低通過篩選和送出行程的傳送層級可能也會受到影響，讓技術更有其更大的影響。</span><span class="sxs-lookup"><span data-stu-id="06c03-119">Low pass filter and reverb send level may also be affected, making the technique even more dramatic.</span></span> <span data-ttu-id="06c03-120">例如，在接聽程式上有一個錐形，可以指定接聽程式後方的所有音效都有一點 muffled，而且有稍微更高的待命至直接比率內容。</span><span class="sxs-lookup"><span data-stu-id="06c03-120">For example, with a cone on the listener, one can specify all sounds behind the listener get a bit muffled, and have slightly higher reverb-to-direct ratio content.</span></span> <span data-ttu-id="06c03-121">這些會提供更多的提示，指出音效位於使用者後方。</span><span class="sxs-lookup"><span data-stu-id="06c03-121">These provide more cues that the sound is behind the user.</span></span> <span data-ttu-id="06c03-122">這可增強您的真實性。</span><span class="sxs-lookup"><span data-stu-id="06c03-122">This enhances realism.</span></span>

<span data-ttu-id="06c03-123">下圖顯示音效圓錐的概念。</span><span class="sxs-lookup"><span data-stu-id="06c03-123">The following illustration shows the concept of sound cones.</span></span>

![音效圓錐](images/common-audio-concepts-sound-cones.png)

<span data-ttu-id="06c03-125">適當地設計音效圓錐可以為您的應用程式增加大幅效果。</span><span class="sxs-lookup"><span data-stu-id="06c03-125">Designing sound cones properly can add dramatic effects to your application.</span></span> <span data-ttu-id="06c03-126">例如，您可以在房間中央放置音效來源，將其方向設定為走廊中的開放門。</span><span class="sxs-lookup"><span data-stu-id="06c03-126">For example, you could position a sound source in the center of a room, setting its orientation toward an open door in a hallway.</span></span> <span data-ttu-id="06c03-127">然後設定在錐形內的角度，使其延伸至門口的寬度、讓外的錐形更寬一點，最後將外部錐形的音量設定為聽不清楚。</span><span class="sxs-lookup"><span data-stu-id="06c03-127">Then set the angle of the inside cone so that it extends to the width of the doorway, make the outside cone a bit wider, and finally set the outside cone volume to inaudible.</span></span> <span data-ttu-id="06c03-128">在走廊時移動的接聽程式，只會在接近門口的時候開始聆聽音效。</span><span class="sxs-lookup"><span data-stu-id="06c03-128">A listener moving along the hallway will begin to hear the sound only when near the doorway.</span></span> <span data-ttu-id="06c03-129">當接聽程式傳入開啟門之前，會 loudest 音效。</span><span class="sxs-lookup"><span data-stu-id="06c03-129">The sound will be loudest as the listener passes in front of the open door.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06c03-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="06c03-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06c03-131">常見的音訊概念</span><span class="sxs-lookup"><span data-stu-id="06c03-131">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="06c03-132">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="06c03-132">X3DAudio</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="06c03-133">**X3DAUDIO \_ 圓錐**</span><span class="sxs-lookup"><span data-stu-id="06c03-133">**X3DAUDIO\_CONE**</span></span>](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



