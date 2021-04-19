---
description: 音訊捕捉和呈現介面
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: 音訊捕捉和呈現介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106966620"
---
# <a name="audio-capture-and-rendering-interfaces"></a><span data-ttu-id="8a02d-103">音訊捕捉和呈現介面</span><span class="sxs-lookup"><span data-stu-id="8a02d-103">Audio Capture and Rendering Interfaces</span></span>

<span data-ttu-id="8a02d-104">這些介面支援在 DirectShow 中進行音訊捕獲和轉譯</span><span class="sxs-lookup"><span data-stu-id="8a02d-104">These interfaces support audio capture and rendering in DirectShow</span></span>



| <span data-ttu-id="8a02d-105">介面</span><span class="sxs-lookup"><span data-stu-id="8a02d-105">Interface</span></span>                                              | <span data-ttu-id="8a02d-106">描述</span><span class="sxs-lookup"><span data-stu-id="8a02d-106">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a02d-107">**IAMAudioInputMixer**</span><span class="sxs-lookup"><span data-stu-id="8a02d-107">**IAMAudioInputMixer**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | <span data-ttu-id="8a02d-108">存取系統音效卡上的類比輸入，並調整特性，例如 mono 或身歷聲、混合層級、平移層級、音量、高音和低音。</span><span class="sxs-lookup"><span data-stu-id="8a02d-108">Access the analog inputs on the system's sound card and adjust characteristics, such as mono or stereo, mix level, pan level, loudness, treble, and bass.</span></span> |
| [<span data-ttu-id="8a02d-109">**IAMAudioRendererStats**</span><span class="sxs-lookup"><span data-stu-id="8a02d-109">**IAMAudioRendererStats**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | <span data-ttu-id="8a02d-110">取得有關音訊轉譯的統計效能資訊。</span><span class="sxs-lookup"><span data-stu-id="8a02d-110">Get statistical performance information about audio renderering.</span></span>                                                                                          |
| [<span data-ttu-id="8a02d-111">**IAMBufferNegotiation**</span><span class="sxs-lookup"><span data-stu-id="8a02d-111">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | <span data-ttu-id="8a02d-112">控制音訊捕獲篩選器如何配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8a02d-112">Control how the audio capture filter allocates buffers.</span></span>                                                                                                   |
| [<span data-ttu-id="8a02d-113">**IAMClockSlave**</span><span class="sxs-lookup"><span data-stu-id="8a02d-113">**IAMClockSlave**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | <span data-ttu-id="8a02d-114">當音訊轉譯器符合其他時鐘的速率時，控制其容錯。</span><span class="sxs-lookup"><span data-stu-id="8a02d-114">Control the tolerance of an audio renderer when it matches rates with another clock.</span></span>                                                                      |
| [<span data-ttu-id="8a02d-115">**IAMDirectSound**</span><span class="sxs-lookup"><span data-stu-id="8a02d-115">**IAMDirectSound**</span></span>](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | <span data-ttu-id="8a02d-116">讓應用程式指定哪個視窗擁有控制 DirectSound 音訊播放的焦點。</span><span class="sxs-lookup"><span data-stu-id="8a02d-116">Enables an application to specify which window has focus for controlling DirectSound audio playback.</span></span>                                                      |
| [<span data-ttu-id="8a02d-117">**IAMResourceControl**</span><span class="sxs-lookup"><span data-stu-id="8a02d-117">**IAMResourceControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | <span data-ttu-id="8a02d-118">在需要時保存音訊裝置資源。</span><span class="sxs-lookup"><span data-stu-id="8a02d-118">Hold an audio device resource before it is needed.</span></span>                                                                                                        |
| [<span data-ttu-id="8a02d-119">**IAMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="8a02d-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | <span data-ttu-id="8a02d-120">查詢並設定捕獲篩選器的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="8a02d-120">Query and set the capture filter's output format.</span></span>                                                                                                         |
| [<span data-ttu-id="8a02d-121">**IBasicAudio**</span><span class="sxs-lookup"><span data-stu-id="8a02d-121">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | <span data-ttu-id="8a02d-122">設定音訊輸出音量和餘額。</span><span class="sxs-lookup"><span data-stu-id="8a02d-122">Set audio output volume and balance.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="8a02d-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a02d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a02d-124">介面</span><span class="sxs-lookup"><span data-stu-id="8a02d-124">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



