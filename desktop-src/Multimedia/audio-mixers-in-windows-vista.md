---
title: Windows Vista 中的音訊 Mixers
description: Windows Vista 中的音訊 Mixers
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- 多媒體音訊，Windows Vista 音訊 mixers
- 音訊、Windows Vista 音訊 mixers
- 音訊 mixers，Windows Vista
- mixers，Windows Vista
- Windows Vista 音訊 mixers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104571208"
---
# <a name="audio-mixers-in-windows-vista"></a><span data-ttu-id="b3a19-108">Windows Vista 中的音訊 Mixers</span><span class="sxs-lookup"><span data-stu-id="b3a19-108">Audio Mixers in Windows Vista</span></span>

<span data-ttu-id="b3a19-109">從 Windows Vista 開始，某些混音器控制項是在軟體中執行，而不是在硬體中。</span><span class="sxs-lookup"><span data-stu-id="b3a19-109">Starting in Windows Vista, some mixer controls are implemented in software rather than hardware.</span></span> <span data-ttu-id="b3a19-110">例如，磁片區控制項會使用 Windows 音訊會話 API 來執行 (WASAPI) 。</span><span class="sxs-lookup"><span data-stu-id="b3a19-110">For example, the volume controls are implemented using the Windows audio session API (WASAPI).</span></span> <span data-ttu-id="b3a19-111">這些控制項不會直接影響硬體設定。</span><span class="sxs-lookup"><span data-stu-id="b3a19-111">These controls do not directly affect hardware settings.</span></span> <span data-ttu-id="b3a19-112">此外，它們與進程特定的音訊會話相關聯，因此變更會影響呼叫應用程式，但不會影響其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="b3a19-112">In addition, they are associated with a process-specific audio session, so changes affect the calling application but do not affect other applications.</span></span>

<span data-ttu-id="b3a19-113">每個音訊端點裝置都有一個標準混音器版面配置，並在軟體中執行。</span><span class="sxs-lookup"><span data-stu-id="b3a19-113">Each audio endpoint device has a standard mixer layout, implemented in software.</span></span>

-   <span data-ttu-id="b3a19-114">每個音訊轉譯端點都包含一個包含下列各項的目的地行：</span><span class="sxs-lookup"><span data-stu-id="b3a19-114">Each audio rendering endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="b3a19-115">音量控制</span><span class="sxs-lookup"><span data-stu-id="b3a19-115">Volume control</span></span>
    -   <span data-ttu-id="b3a19-116">靜音控制</span><span class="sxs-lookup"><span data-stu-id="b3a19-116">Mute control</span></span>
    -   <span data-ttu-id="b3a19-117">來源行：波形-音訊輸出。</span><span class="sxs-lookup"><span data-stu-id="b3a19-117">Source line: Waveform-audio output.</span></span>
    -   <span data-ttu-id="b3a19-118">來源行：音訊 CD。</span><span class="sxs-lookup"><span data-stu-id="b3a19-118">Source line: Audio CD.</span></span>
-   <span data-ttu-id="b3a19-119">每個音訊捕獲端點都包含一個目的地行，其中包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="b3a19-119">Each audio capture endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="b3a19-120">音量控制</span><span class="sxs-lookup"><span data-stu-id="b3a19-120">Volume control</span></span>
    -   <span data-ttu-id="b3a19-121">靜音控制</span><span class="sxs-lookup"><span data-stu-id="b3a19-121">Mute control</span></span>
    -   <span data-ttu-id="b3a19-122">來源行：波形-音訊輸入。</span><span class="sxs-lookup"><span data-stu-id="b3a19-122">Source line: Waveform-audio input.</span></span> <span data-ttu-id="b3a19-123">元件類型取決於輸入裝置，例如麥克風。</span><span class="sxs-lookup"><span data-stu-id="b3a19-123">The component type depends on the input device— for example, a microphone.</span></span>

<span data-ttu-id="b3a19-124">每個原始程式列都包含音量控制項和靜音控制項。</span><span class="sxs-lookup"><span data-stu-id="b3a19-124">Each source line contains a volume control and a mute control.</span></span> <span data-ttu-id="b3a19-125">下圖顯示呈現端點和捕捉端點的元件。</span><span class="sxs-lookup"><span data-stu-id="b3a19-125">The following diagram shows the components of render endpoints and capture endpoints.</span></span>

![預設混音器版面配置](images/mixer1.gif)

<span data-ttu-id="b3a19-127">端點的所有控制項都可操作相同的基礎軟體控制項。</span><span class="sxs-lookup"><span data-stu-id="b3a19-127">All of the controls for an endpoint manipulate the same underlying software control.</span></span> <span data-ttu-id="b3a19-128">因此，如果您變更某個控制項的設定，您將會在其他控制項上收到控制項變更通知。</span><span class="sxs-lookup"><span data-stu-id="b3a19-128">Therefore, if you change the settings on one control, you will receive a control change notification on the other controls.</span></span> <span data-ttu-id="b3a19-129"> (參閱 [**MM \_ MIXM \_ 控制項 \_ 變更**](mm-mixm-control-change.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="b3a19-129">(See [**MM\_MIXM\_CONTROL\_CHANGE**](mm-mixm-control-change.md).)</span></span>

<span data-ttu-id="b3a19-130">此標準版面配置是為了與使用音訊混音器功能的現有應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="b3a19-130">This standard layout is provided for compatibility with existing applications that use the audio mixer functions.</span></span> <span data-ttu-id="b3a19-131">新的應用程式應該避免使用這些功能。</span><span class="sxs-lookup"><span data-stu-id="b3a19-131">New applications should avoid using these functions.</span></span>

 

 




