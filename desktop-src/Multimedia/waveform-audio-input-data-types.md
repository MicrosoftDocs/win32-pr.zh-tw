---
title: Waveform-Audio 輸入資料類型
description: Waveform-Audio 輸入資料類型
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- 波形音訊、輸入資料類型
- 波形-音訊介面、輸入資料類型
- 錄製波形音訊、輸入資料類型
- HWAVEIN 控制碼
- WAVEFORMATEX 結構
- WAVEHDR 結構
- WAVEINCAPS 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023407"
---
# <a name="waveform-audio-input-data-types"></a><span data-ttu-id="9b1dd-110">Waveform-Audio 輸入資料類型</span><span class="sxs-lookup"><span data-stu-id="9b1dd-110">Waveform-Audio Input Data Types</span></span>

<span data-ttu-id="9b1dd-111">下列資料類型是針對波形-音訊輸入函式所定義。</span><span class="sxs-lookup"><span data-stu-id="9b1dd-111">The following data types are defined for waveform-audio input functions.</span></span>



| <span data-ttu-id="9b1dd-112">類型</span><span class="sxs-lookup"><span data-stu-id="9b1dd-112">Type</span></span>                                 | <span data-ttu-id="9b1dd-113">Description</span><span class="sxs-lookup"><span data-stu-id="9b1dd-113">Description</span></span>                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b1dd-114">**HWAVEIN**</span><span class="sxs-lookup"><span data-stu-id="9b1dd-114">**HWAVEIN**</span></span>                          | <span data-ttu-id="9b1dd-115">開啟波形音訊輸入裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9b1dd-115">Handle of an open waveform-audio input device.</span></span>                                                                                                                  |
| [<span data-ttu-id="9b1dd-116">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="9b1dd-116">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | <span data-ttu-id="9b1dd-117">結構，指定特定波形音訊輸入裝置所支援的資料格式。</span><span class="sxs-lookup"><span data-stu-id="9b1dd-117">Structure that specifies the data formats supported by a particular waveform-audio input device.</span></span> <span data-ttu-id="9b1dd-118">此結構也可用於波形音訊輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="9b1dd-118">This structure is also used for waveform-audio output devices.</span></span> |
| [<span data-ttu-id="9b1dd-119">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="9b1dd-119">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | <span data-ttu-id="9b1dd-120">結構，用來做為波形音訊輸入資料區塊的標頭。</span><span class="sxs-lookup"><span data-stu-id="9b1dd-120">Structure used as a header for a block of waveform-audio input data.</span></span> <span data-ttu-id="9b1dd-121">此結構也可用於波形音訊輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="9b1dd-121">This structure is also used for waveform-audio output devices.</span></span>                             |
| [<span data-ttu-id="9b1dd-122">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="9b1dd-122">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | <span data-ttu-id="9b1dd-123">用來查詢特定波形音訊輸入裝置功能的結構。</span><span class="sxs-lookup"><span data-stu-id="9b1dd-123">Structure used to inquire about the capabilities of a particular waveform-audio input device.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="9b1dd-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b1dd-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b1dd-125">錄製波形音訊</span><span class="sxs-lookup"><span data-stu-id="9b1dd-125">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 