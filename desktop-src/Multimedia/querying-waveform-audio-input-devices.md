---
title: 查詢 Waveform-Audio 輸入裝置
description: 查詢 Waveform-Audio 輸入裝置
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- 波形音訊，查詢輸入裝置
- 波形-音訊介面，查詢輸入裝置
- 錄製波形音訊，查詢輸入裝置
- 查詢波形音訊輸入裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933177"
---
# <a name="querying-waveform-audio-input-devices"></a><span data-ttu-id="2b1ed-107">查詢 Waveform-Audio 輸入裝置</span><span class="sxs-lookup"><span data-stu-id="2b1ed-107">Querying Waveform-Audio Input Devices</span></span>

<span data-ttu-id="2b1ed-108">錄製波形音訊之前，您應該呼叫 [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) 函式來判斷系統的波形音訊輸入功能。</span><span class="sxs-lookup"><span data-stu-id="2b1ed-108">Before recording waveform audio, you should call the [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) function to determine the waveform-audio input capabilities of the system.</span></span> <span data-ttu-id="2b1ed-109">此函式會以指定裝置功能的相關資訊填入 [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) 結構。</span><span class="sxs-lookup"><span data-stu-id="2b1ed-109">This function fills a [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) structure with information about the capabilities of a specified device.</span></span> <span data-ttu-id="2b1ed-110">這項資訊包括製造商和產品識別碼、裝置的產品名稱，以及設備磁碟機的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="2b1ed-110">This information includes the manufacturer and product identifiers, a product name for the device, and the version number of the device driver.</span></span> <span data-ttu-id="2b1ed-111">此外， **WAVEINCAPS** 結構會提供裝置所支援之標準波形-音訊格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2b1ed-111">In addition, the **WAVEINCAPS** structure provides information about the standard waveform-audio formats that the device supports.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b1ed-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b1ed-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b1ed-113">錄製波形音訊</span><span class="sxs-lookup"><span data-stu-id="2b1ed-113">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 