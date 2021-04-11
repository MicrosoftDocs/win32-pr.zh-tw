---
title: 執行 CEcho DoProcessOutput
description: 執行 CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Windows Media Player 外掛程式，Echo 範例 DoProcessOutput 方法
- 外掛程式，Echo 範例 DoProcessOutput 方法
- 數位信號處理外掛程式，Echo 範例 DoProcessOutput 方法
- DSP 外掛程式，Echo 範例 DoProcessOutput 方法
- Echo DSP 外掛程式範例，DoProcessOutput 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff40246a6a0ccda2b3f17b12924c44cb79fa4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022082"
---
# <a name="implementing-cechodoprocessoutput"></a><span data-ttu-id="cad2a-108">執行 CEcho：:D oProcessOutput</span><span class="sxs-lookup"><span data-stu-id="cad2a-108">Implementing CEcho::DoProcessOutput</span></span>

<span data-ttu-id="cad2a-109">**DoProcessOutput** 方法會執行數位信號處理。</span><span class="sxs-lookup"><span data-stu-id="cad2a-109">The **DoProcessOutput** method performs the digital signal processing.</span></span> <span data-ttu-id="cad2a-110">這是對 Windows Media Player 所提供的資料進行變更的方法。</span><span class="sxs-lookup"><span data-stu-id="cad2a-110">This is the method that makes the changes to the data provided by Windows Media Player.</span></span> <span data-ttu-id="cad2a-111">這是此方法的結果，當您的 Echo 範例外掛程式完成時，您會收到回應的回應。</span><span class="sxs-lookup"><span data-stu-id="cad2a-111">It is the results of this method that you will hear as an echo effect when your Echo sample plug-in is complete.</span></span>

<span data-ttu-id="cad2a-112">在此範例中，外掛程式只會處理8位或16位的音訊。</span><span class="sxs-lookup"><span data-stu-id="cad2a-112">For this sample, the plug-in will only process 8-bit or 16-bit audio.</span></span> <span data-ttu-id="cad2a-113">您將需要對外掛程式的 wizard 範例程式碼進行一些變更，以移除處理較高位深度音訊的區段。</span><span class="sxs-lookup"><span data-stu-id="cad2a-113">You will need to make some changes to the plug-in wizard sample code to remove the sections that process higher bit depth audio.</span></span> <span data-ttu-id="cad2a-114">不過，請務必研究這些區段，因為您可能會決定為這些格式新增您自己的 echo 執行。</span><span class="sxs-lookup"><span data-stu-id="cad2a-114">It is worthwhile to study these sections, however, because you may decide to add your own echo implementation for those formats.</span></span>

<span data-ttu-id="cad2a-115">下列各節詳細說明您需要對程式碼進行的變更：</span><span class="sxs-lookup"><span data-stu-id="cad2a-115">The following sections detail the changes you need to make to the code:</span></span>

-   [<span data-ttu-id="cad2a-116">移除程式碼以處理大於16個位的程式碼</span><span class="sxs-lookup"><span data-stu-id="cad2a-116">Removing the Code to Process Greater than 16 Bits</span></span>](removing-the-code-to-process-greater-than-16-bits.md)
-   [<span data-ttu-id="cad2a-117">處理音訊資料</span><span class="sxs-lookup"><span data-stu-id="cad2a-117">Processing the Audio Data</span></span>](processing-the-audio-data.md)
-   [<span data-ttu-id="cad2a-118">要執行處理的變數</span><span class="sxs-lookup"><span data-stu-id="cad2a-118">Variables to Perform Processing</span></span>](variables-to-perform-processing.md)
-   [<span data-ttu-id="cad2a-119">建立 Echo 效果</span><span class="sxs-lookup"><span data-stu-id="cad2a-119">Creating the Echo Effect</span></span>](creating-the-echo-effect.md)

## <a name="related-topics"></a><span data-ttu-id="cad2a-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="cad2a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cad2a-121">**Echo 範例**</span><span class="sxs-lookup"><span data-stu-id="cad2a-121">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




