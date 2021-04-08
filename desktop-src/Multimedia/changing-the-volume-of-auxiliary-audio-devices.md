---
title: 變更輔助 Audio-Devices 的數量
description: 變更輔助 Audio-Devices 的數量
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- 波形音訊，變更輔助音訊裝置音量
- 變更輔助音訊裝置音量
- 輔助音訊，變更裝置音量
- 輔助音訊介面
- 輔助音訊裝置，變更音量
- 輔助音訊、介面
- 輔助音訊、裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682362"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a><span data-ttu-id="bcf95-110">變更輔助 Audio-Devices 的數量</span><span class="sxs-lookup"><span data-stu-id="bcf95-110">Changing the Volume of Auxiliary Audio-Devices</span></span>

<span data-ttu-id="bcf95-111">Windows 提供下列功能來查詢及設定輔助音訊裝置的磁片區。</span><span class="sxs-lookup"><span data-stu-id="bcf95-111">Windows provides the following functions to query and set the volume for auxiliary audio devices.</span></span>



| <span data-ttu-id="bcf95-112">函式</span><span class="sxs-lookup"><span data-stu-id="bcf95-112">Function</span></span>                             | <span data-ttu-id="bcf95-113">描述</span><span class="sxs-lookup"><span data-stu-id="bcf95-113">Description</span></span>                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="bcf95-114">**auxGetVolume**</span><span class="sxs-lookup"><span data-stu-id="bcf95-114">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | <span data-ttu-id="bcf95-115">抓取指定之輔助輸出裝置的目前磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="bcf95-115">Retrieves the current volume setting of the specified auxiliary output device.</span></span> |
| [<span data-ttu-id="bcf95-116">**auxSetVolume**</span><span class="sxs-lookup"><span data-stu-id="bcf95-116">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | <span data-ttu-id="bcf95-117">設定指定之輔助輸出裝置的磁片區。</span><span class="sxs-lookup"><span data-stu-id="bcf95-117">Sets the volume of the specified auxiliary output device.</span></span>                      |



 

<span data-ttu-id="bcf95-118">並非所有輔助音訊裝置都支援磁片區變更。</span><span class="sxs-lookup"><span data-stu-id="bcf95-118">Not all auxiliary audio devices support volume changes.</span></span> <span data-ttu-id="bcf95-119">某些裝置可支援左側和右側通道上的個別磁片區變更。</span><span class="sxs-lookup"><span data-stu-id="bcf95-119">Some devices can support individual volume changes on both the left and the right channels.</span></span>

<span data-ttu-id="bcf95-120">磁片區是以雙聲道值指定，如同波形-音訊和 MIDI 音量控制功能。</span><span class="sxs-lookup"><span data-stu-id="bcf95-120">Volume is specified in a doubleword value, as with the waveform-audio and MIDI volume-control functions.</span></span> <span data-ttu-id="bcf95-121">當音訊格式為身歷聲時，上層16位會指定右聲道的相對磁片區，而較低的16位則會指定左邊通道的相對音量。</span><span class="sxs-lookup"><span data-stu-id="bcf95-121">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="bcf95-122">對於不支援左和右聲道音量控制的裝置，較低的16位會指定磁片區層級，而會忽略前16位。</span><span class="sxs-lookup"><span data-stu-id="bcf95-122">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="bcf95-123">磁片區層級值的範圍是從 0x0 (無聲) 至 0xFFFF (最大磁片區) ，而且會 logarithmically。</span><span class="sxs-lookup"><span data-stu-id="bcf95-123">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="bcf95-124">將磁片區層級從0x5000 增加至0x6000 時，觀察到的磁片區增加是相同的，因為它是從0x4000 到0x5000。</span><span class="sxs-lookup"><span data-stu-id="bcf95-124">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 