---
title: 關於範例音訊 DSP 外掛程式
description: 關於範例音訊 DSP 外掛程式
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- Windows Media Player 外掛程式，範例
- 外掛程式，範例
- 數位信號處理外掛程式，範例
- DSP 外掛程式，範例
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式、音訊範例
- DSP 外掛程式、音訊範例
- 範例，DSP 外掛程式
- 音訊 DSP 外掛程式、範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edc3a5860c0c52837bfece16d2e709bf16d836d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300935"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="a8c1c-113">關於範例音訊 DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="a8c1c-113">About the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="a8c1c-114">範例音訊 DSP 外掛程式提供簡單的處理常式，可根據使用者在屬性頁中提供的因素來調整音訊的波幅。</span><span class="sxs-lookup"><span data-stu-id="a8c1c-114">The sample audio DSP plug-in provides a simple processing implementation that scales the amplitude of the audio by a factor provided by the user in the property page.</span></span> <span data-ttu-id="a8c1c-115">外掛程式接受介於0和1之間的值。</span><span class="sxs-lookup"><span data-stu-id="a8c1c-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="a8c1c-116">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="a8c1c-116">The default value is 1.</span></span> <span data-ttu-id="a8c1c-117">值為1時，不會影響音效;其他縮放因素是音訊樣本的乘數。</span><span class="sxs-lookup"><span data-stu-id="a8c1c-117">A value of 1 has no effect upon the sound; other scale factors are multipliers for the audio samples.</span></span> <span data-ttu-id="a8c1c-118">例如，值 .5 會導致磁片區中的6分貝減少。</span><span class="sxs-lookup"><span data-stu-id="a8c1c-118">For instance, a value of .5 would result in a 6 decibel decrease in volume.</span></span> <span data-ttu-id="a8c1c-119">值為零會導致無聲。</span><span class="sxs-lookup"><span data-stu-id="a8c1c-119">A value of zero results in silence.</span></span>

<span data-ttu-id="a8c1c-120">範例音訊 DSP 外掛程式適用于身歷聲或 mono PCM 音訊。</span><span class="sxs-lookup"><span data-stu-id="a8c1c-120">The sample audio DSP plug-in works with stereo or mono PCM audio.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8c1c-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8c1c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8c1c-122">**建立 DSP 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="a8c1c-122">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




