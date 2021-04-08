---
title: 磁片區純量
description: 磁片區純量
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- 音樂檢測數位介面 (MIDI) 、磁片區純量
- MIDI (音樂檢測數位介面) 、磁片區純量
- MIDI 對應工具，磁片區純量
- 磁片區純量
- MIDI 對應程式，調整輸出層級
- 調整輸出層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39566a10ca909030b60ff197f009b6afe05ce51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022107"
---
# <a name="the-volume-scalar"></a><span data-ttu-id="0d417-109">磁片區純量</span><span class="sxs-lookup"><span data-stu-id="0d417-109">The Volume Scalar</span></span>

<span data-ttu-id="0d417-110">磁片區純量的用途是允許在合成器上不同修補程式的相對輸出層級之間進行調整。</span><span class="sxs-lookup"><span data-stu-id="0d417-110">The purpose of the volume scalar is to allow adjustments between the relative output levels of different patches on a synthesizer.</span></span> <span data-ttu-id="0d417-111">例如，如果合成器上的低音修補程式與其鋼琴修補程式比較得太遠，您可以變更安裝對應，將低音音量或鋼琴的音量向上調整。</span><span class="sxs-lookup"><span data-stu-id="0d417-111">For example, if the bass patch on a synthesizer is too loud compared with its piano patch, you can change the setup map to scale the bass volume down or the piano volume up.</span></span>

<span data-ttu-id="0d417-112">「磁片區純量」會指定一個百分比值，以變更所有遵循相關聯程式變更訊息的 MIDI 主要磁片區控制器訊息。</span><span class="sxs-lookup"><span data-stu-id="0d417-112">The volume scalar specifies a percentage value for changing all MIDI main-volume controller messages that follow an associated program-change message.</span></span> <span data-ttu-id="0d417-113">例如，如果磁片區純量值為50%，則 MIDI 對應程式會修改 MIDI 主要磁片區控制器訊息，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="0d417-113">For example, if the volume scalar value is 50%, the MIDI Mapper modifies MIDI main-volume controller messages as shown in the following illustration.</span></span>

![midi 對應程式映射](images/mmap-a04.gif)

 

 




