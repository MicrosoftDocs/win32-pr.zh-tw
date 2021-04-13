---
title: 修補程式對應
description: 修補程式對應
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- 音樂檢測數位介面 (MIDI) 、MIDI 對應程式
- MIDI (的音樂檢測數位介面) 、MIDI 對應程式
- MIDI 對應程式，修補程式對應
- 修補程式對應
- MIDI 程式-變更訊息
- MIDI 磁片區-控制器訊息
- 程式變更訊息
- 磁片區控制器訊息
- MIDI 對應程式，程式變更訊息
- MIDI 對應程式，磁片區控制器訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300688"
---
# <a name="patch-maps"></a><span data-ttu-id="30ef3-113">修補程式對應</span><span class="sxs-lookup"><span data-stu-id="30ef3-113">Patch Maps</span></span>

<span data-ttu-id="30ef3-114">每個通道對應專案都可以有相關聯的 patch map。</span><span class="sxs-lookup"><span data-stu-id="30ef3-114">Each channel map entry can have an associated patch map.</span></span> <span data-ttu-id="30ef3-115">Patch maps 會影響 MIDI 程式-變更和磁片區控制器訊息。</span><span class="sxs-lookup"><span data-stu-id="30ef3-115">Patch maps affect MIDI program-change and volume-controller messages.</span></span> <span data-ttu-id="30ef3-116">程式變更訊息會指示合成器針對指定的通道變更檢測音效 (修補) 。</span><span class="sxs-lookup"><span data-stu-id="30ef3-116">Program-change messages tell a synthesizer to change the instrument sound (patch) for a specified channel.</span></span> <span data-ttu-id="30ef3-117">磁片區控制器訊息會設定通道的磁片區。</span><span class="sxs-lookup"><span data-stu-id="30ef3-117">Volume-controller messages set the volume for a channel.</span></span>

<span data-ttu-id="30ef3-118">Patch map 具有轉譯資料表，其中每個128程式變更值都有一個專案。</span><span class="sxs-lookup"><span data-stu-id="30ef3-118">A patch map has a translation table with an entry for each of the 128 program-change values.</span></span> <span data-ttu-id="30ef3-119">每個 patch map 都會指定下列各項：</span><span class="sxs-lookup"><span data-stu-id="30ef3-119">Each patch map specifies the following:</span></span>

-   <span data-ttu-id="30ef3-120">目的地程式-變更值。</span><span class="sxs-lookup"><span data-stu-id="30ef3-120">A destination program-change value.</span></span>
-   <span data-ttu-id="30ef3-121">磁片區純量。</span><span class="sxs-lookup"><span data-stu-id="30ef3-121">A volume scalar.</span></span> <span data-ttu-id="30ef3-122"> (需詳細資訊，請參閱磁片區純 [量](the-volume-scalar.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="30ef3-122">(For more information, see [The Volume Scalar](the-volume-scalar.md).)</span></span>
-   <span data-ttu-id="30ef3-123">選用的按鍵對應。</span><span class="sxs-lookup"><span data-stu-id="30ef3-123">An optional key map.</span></span> <span data-ttu-id="30ef3-124"> (需詳細資訊，請參閱 [金鑰組應](key-maps.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="30ef3-124">(For more information, see [Key Maps](key-maps.md).)</span></span>

<span data-ttu-id="30ef3-125">當 MIDI 對應程式收到程式變更訊息時，目的地程式-變更值會取代為訊息中的程式變更值。</span><span class="sxs-lookup"><span data-stu-id="30ef3-125">When program-change messages are received by the MIDI Mapper, the destination program-change value is substituted for the program-change value in the message.</span></span> <span data-ttu-id="30ef3-126">例如，如果程式-變更16的目的地程式-變更值為18，則 MIDI 對應程式會修改 MIDI 程式變更訊息，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="30ef3-126">For example, if the destination program-change value for program-change 16 is 18, the MIDI Mapper modifies the MIDI program-change message as shown in the following illustration.</span></span>

![midi 對應程式映射](images/mmap-a03.gif)

 

 




