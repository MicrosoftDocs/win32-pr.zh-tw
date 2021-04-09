---
title: 音訊緩衝區
description: 音訊緩衝區
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672319"
---
# <a name="audio-buffers"></a><span data-ttu-id="0a10d-107">音訊緩衝區</span><span class="sxs-lookup"><span data-stu-id="0a10d-107">Audio Buffers</span></span>

<span data-ttu-id="0a10d-108">您可以用三種方式控制捕捉作業的音訊部分：</span><span class="sxs-lookup"><span data-stu-id="0a10d-108">You can control the audio portion of a capture operation in three ways:</span></span>

-   <span data-ttu-id="0a10d-109">從捕捉作業中包含或排除音訊。</span><span class="sxs-lookup"><span data-stu-id="0a10d-109">Include or exclude audio from the capture operation.</span></span>
-   <span data-ttu-id="0a10d-110">要求特定數目的音訊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0a10d-110">Request a specific number of audio buffers.</span></span>
-   <span data-ttu-id="0a10d-111">要求音訊緩衝區是特定的大小。</span><span class="sxs-lookup"><span data-stu-id="0a10d-111">Request that audio buffers be a specific size.</span></span>

<span data-ttu-id="0a10d-112">您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得音訊緩衝區的設定。</span><span class="sxs-lookup"><span data-stu-id="0a10d-112">You can retrieve the settings for audio buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="0a10d-113">[**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **fCaptureAudio** 成員會指定是否要在捕捉作業中包含或排除音訊。</span><span class="sxs-lookup"><span data-stu-id="0a10d-113">The **fCaptureAudio** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure specifies whether audio is included or excluded from the capture operation.</span></span> <span data-ttu-id="0a10d-114">目前要求的音訊緩衝區數目會儲存在 **wNumAudioRequested** 成員中，而目前的音訊緩衝區大小會儲存在 **dwAudioBufferSize** 成員中。</span><span class="sxs-lookup"><span data-stu-id="0a10d-114">The current requested number of audio buffers is stored in the **wNumAudioRequested** member, and the current audio buffer size is stored in the **dwAudioBufferSize** member.</span></span> <span data-ttu-id="0a10d-115">您可以指定是否要包含音訊捕捉、透過更新這些成員來指定音訊緩衝區的大小和數目，並使用 [ [**WM \_ CAP \_ SET \_ SEQUENCE 設定 \_**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ] 宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="0a10d-115">You can specify whether to include audio capture, specify the size and number of audio buffers by updating these members, and send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

<span data-ttu-id="0a10d-116">根據預設，音訊會包含在捕獲操作中，並配置四個音訊緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0a10d-116">By default, audio is included in the capture operation, and four audio buffers are allocated.</span></span> <span data-ttu-id="0a10d-117">**FCaptureAudio** 的預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0a10d-117">The default value of **fCaptureAudio** is **TRUE**.</span></span> <span data-ttu-id="0a10d-118">預設的緩衝區大小 (**dwAudioBufferSize**) 的值可以包含0.5 秒的音訊資料或10k （以較大者為准）。</span><span class="sxs-lookup"><span data-stu-id="0a10d-118">The default buffer size (the value of **dwAudioBufferSize**) can contain 0.5 seconds of audio data or 10K, whichever is greater.</span></span>

 

 




