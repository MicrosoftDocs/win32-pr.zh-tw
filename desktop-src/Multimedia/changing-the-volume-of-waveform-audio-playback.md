---
title: 變更 Waveform-Audio 播放的音量
description: 變更 Waveform-Audio 播放的音量
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- 波形音訊，變更播放音量
- 波形-音訊介面，變更播放音量
- 波形音訊，播放音量
- 波形-音訊介面、播放音量
- 變更波形-音訊播放音量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f972b5bd8e6f0d4a0d7d5964f164429c5632b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682361"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a><span data-ttu-id="b912c-108">變更 Waveform-Audio 播放的音量</span><span class="sxs-lookup"><span data-stu-id="b912c-108">Changing the Volume of Waveform-Audio Playback</span></span>

<span data-ttu-id="b912c-109">Windows 提供下列功能來查詢及設定波形音訊輸出裝置的音量層級。</span><span class="sxs-lookup"><span data-stu-id="b912c-109">Windows provides the following functions to query and set the volume level of waveform-audio output devices.</span></span>



| <span data-ttu-id="b912c-110">函式</span><span class="sxs-lookup"><span data-stu-id="b912c-110">Function</span></span>                                     | <span data-ttu-id="b912c-111">描述</span><span class="sxs-lookup"><span data-stu-id="b912c-111">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="b912c-112">**waveOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="b912c-112">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | <span data-ttu-id="b912c-113">抓取指定之波形音訊輸出裝置的目前磁片區層級。</span><span class="sxs-lookup"><span data-stu-id="b912c-113">Retrieves the current volume level of the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="b912c-114">**waveOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="b912c-114">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | <span data-ttu-id="b912c-115">設定指定之波形音訊輸出裝置的音量層級。</span><span class="sxs-lookup"><span data-stu-id="b912c-115">Sets the volume level of the specified waveform-audio output device.</span></span>              |



 

<span data-ttu-id="b912c-116">並非所有波形音訊裝置都支援磁片區變更。</span><span class="sxs-lookup"><span data-stu-id="b912c-116">Not all waveform-audio devices support volume changes.</span></span> <span data-ttu-id="b912c-117">某些裝置支援左右通道上的個別音量控制。</span><span class="sxs-lookup"><span data-stu-id="b912c-117">Some devices support individual volume control on both the left and right channels.</span></span> <span data-ttu-id="b912c-118">如需如何判斷波形音訊裝置的音量控制功能的相關資訊，請參閱 [裝置和資料類型](devices-and-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="b912c-118">For information about how to determine the volume-control capabilities of waveform-audio devices, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="b912c-119">有些應用程式可讓使用者控制系統中所有音訊裝置的磁片區。</span><span class="sxs-lookup"><span data-stu-id="b912c-119">Some applications allow the user to control the volume for all audio devices in a system.</span></span> <span data-ttu-id="b912c-120"> (此類型的許多應用程式都使用音訊混音器服務;如需詳細資訊，請參閱 [音訊 Mixers](audio-mixers.md)。 ) 除非您的應用程式能夠使用這種主要音量控制，否則您應該先開啟音訊裝置，再變更其磁片區。</span><span class="sxs-lookup"><span data-stu-id="b912c-120">(Many applications of this type use the audio mixer services; for more information, see [Audio Mixers](audio-mixers.md).) Unless your application is capable of this kind of master volume control, you should open an audio device before changing its volume.</span></span> <span data-ttu-id="b912c-121">您也應該在變更磁片區層級之前先進行查詢，並儘快將磁片區層級還原至先前的層級。</span><span class="sxs-lookup"><span data-stu-id="b912c-121">You should also query the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="b912c-122">磁片區是以雙量值指定。</span><span class="sxs-lookup"><span data-stu-id="b912c-122">Volume is specified in a doubleword value.</span></span> <span data-ttu-id="b912c-123">當音訊格式為身歷聲時，上層16位會指定右聲道的相對磁片區，而較低的16位則會指定左邊通道的相對音量。</span><span class="sxs-lookup"><span data-stu-id="b912c-123">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="b912c-124">對於不支援左和右聲道音量控制的裝置，較低的16位會指定磁片區層級，而會忽略前16位。</span><span class="sxs-lookup"><span data-stu-id="b912c-124">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="b912c-125">磁片區層級值的範圍是從 0x0 (無聲) 至 0xFFFF (最大磁片區) ，而且會 logarithmically。</span><span class="sxs-lookup"><span data-stu-id="b912c-125">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="b912c-126">將磁片區層級從0x5000 增加至0x6000 時，觀察到的磁片區增加是相同的，因為它是從0x4000 到0x5000。</span><span class="sxs-lookup"><span data-stu-id="b912c-126">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 