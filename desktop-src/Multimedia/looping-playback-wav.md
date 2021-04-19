---
title: '迴圈播放 (波形音訊) '
description: '迴圈播放 (波形音訊) '
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- 波形音訊，迴圈聲音
- 波形-音訊介面，迴圈聲音
- 波形音訊、迴圈播放
- 波形-音訊介面、迴圈播放
- 迴圈波形-音效
- 迴圈波形-音訊播放
- waveOutWrite 函式
- waveOutBreakLoop 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "107000447"
---
# <a name="looping-playback"></a><span data-ttu-id="a18e2-111">迴圈播放</span><span class="sxs-lookup"><span data-stu-id="a18e2-111">Looping Playback</span></span>

<span data-ttu-id="a18e2-112">使用 [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)函式傳遞至裝置的 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構中的 **dwLoops** 和 **dwFlags** 成員，可控制音效的迴圈。</span><span class="sxs-lookup"><span data-stu-id="a18e2-112">Looping a sound is controlled by the **dwLoops** and **dwFlags** members in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structures passed to the device with the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function.</span></span> <span data-ttu-id="a18e2-113">使用 **dwFlags** 成員中的 **WHDR \_ BEGINLOOP** 和 **WHDR \_ ENDLOOP** 旗標，指定迴圈的開始和結束資料區塊。</span><span class="sxs-lookup"><span data-stu-id="a18e2-113">Use the **WHDR\_BEGINLOOP** and **WHDR\_ENDLOOP** flags in the **dwFlags** member to specify the beginning and ending data blocks for looping.</span></span>

<span data-ttu-id="a18e2-114">若要迴圈單一資料區塊，請指定相同區塊的兩個旗標。</span><span class="sxs-lookup"><span data-stu-id="a18e2-114">To loop a single data block, specify both flags for the same block.</span></span> <span data-ttu-id="a18e2-115">若要指定迴圈的數目，請針對迴圈中的第一個區塊使用 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構中的 **dwLoops** 成員。</span><span class="sxs-lookup"><span data-stu-id="a18e2-115">To specify the number of loops, use the **dwLoops** member in the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure for the first block in the loop.</span></span>

<span data-ttu-id="a18e2-116">您可以呼叫 [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) 函數來停止迴圈音效。</span><span class="sxs-lookup"><span data-stu-id="a18e2-116">You can call the [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) function to stop a looping sound.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a18e2-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="a18e2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a18e2-118">播放 Waveform-Audio 檔案</span><span class="sxs-lookup"><span data-stu-id="a18e2-118">Playing Waveform-Audio Files</span></span>](playing-waveform-audio-files.md)
</dt> </dl>

 

 
