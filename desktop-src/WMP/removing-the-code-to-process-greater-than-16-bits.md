---
title: 移除程式碼以處理大於16個位的程式碼
description: 移除程式碼以處理大於16個位的程式碼
ms.assetid: 90c165e1-bc77-42a5-878d-056762c62991
keywords:
- Windows Media Player 外掛程式，Echo 範例 DoProcessOutput 方法
- 外掛程式，Echo 範例 DoProcessOutput 方法
- 數位信號處理外掛程式，Echo 範例 DoProcessOutput 方法
- DSP 外掛程式，Echo 範例 DoProcessOutput 方法
- Echo DSP 外掛程式範例，DoProcessOutput 方法
- Echo DSP 外掛程式範例，處理大於16個位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec33332ee332d0ca7b615844ba8ad5cd7b00eb2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840067"
---
# <a name="removing-the-code-to-process-greater-than-16-bits"></a><span data-ttu-id="40000-109">移除程式碼以處理大於16個位的程式碼</span><span class="sxs-lookup"><span data-stu-id="40000-109">Removing the Code to Process Greater than 16 Bits</span></span>

<span data-ttu-id="40000-110">因為此範例只會處理8位或16位的音訊，所以您必須修改 **CEcho：： ValidateMediaType** 中的程式碼，以 \_ 傳回 \_ \_ \_ 大於16位之媒體類型不接受的 sql-dmo E 類型。</span><span class="sxs-lookup"><span data-stu-id="40000-110">Because this sample only processes 8-bit or 16-bit audio, you need to modify the code in **CEcho::ValidateMediaType** to return DMO\_E\_TYPE\_NOT\_ACCEPTED for media types greater than 16 bits.</span></span> <span data-ttu-id="40000-111">若要完成這項工作，您必須變更 switch 區塊中的程式碼，以測試可延伸的型別 WAVE 格式的格式 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="40000-111">To accomplish this, you must change the code in the switch block that tests formats of type WAVE\_FORMAT\_EXTENSIBLE.</span></span> <span data-ttu-id="40000-112">將嚮導程式碼取代為下列範例程式碼：</span><span class="sxs-lookup"><span data-stu-id="40000-112">Replace the wizard code with the following example code:</span></span>


```C++
case WAVE_FORMAT_EXTENSIBLE:
    {
         // Sample size is greater than 16-bit or is multichannel.
        WAVEFORMATEXTENSIBLE *pWaveXT = (WAVEFORMATEXTENSIBLE *) pWave;

        if (KSDATAFORMAT_SUBTYPE_PCM != pWaveXT->SubFormat)
        {
            return DMO_E_TYPE_NOT_ACCEPTED;
        }
    }
    break;

```



<span data-ttu-id="40000-113">接下來，刪除或批註 **DoProcessOutput** 中處理高位解析度音訊的程式碼區段。</span><span class="sxs-lookup"><span data-stu-id="40000-113">Next, delete or comment out the sections of code in **DoProcessOutput** that handle high bit resolution audio.</span></span> <span data-ttu-id="40000-114">這些是以案例24和案例32為開頭的區段。</span><span class="sxs-lookup"><span data-stu-id="40000-114">These are the sections that begin with case 24 and case 32.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40000-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="40000-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40000-116">**執行 CEcho：:D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="40000-116">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




