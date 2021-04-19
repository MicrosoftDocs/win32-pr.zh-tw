---
title: Echo 範例總覽
description: Echo 範例總覽
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Windows Media Player 外掛程式，Echo 範例總覽
- 外掛程式，Echo 範例總覽
- 數位信號處理外掛程式，Echo 範例總覽
- DSP 外掛程式，Echo 範例總覽
- Echo DSP 外掛程式範例，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976322"
---
# <a name="echo-sample-overview"></a><span data-ttu-id="449ac-108">Echo 範例總覽</span><span class="sxs-lookup"><span data-stu-id="449ac-108">Echo Sample Overview</span></span>

<span data-ttu-id="449ac-109">本指南建立 Windows Media Player 的 DSP 外掛程式，以在播放期間于 PCM 音訊中建立 echo 效果。</span><span class="sxs-lookup"><span data-stu-id="449ac-109">This guide builds a Windows Media Player DSP plug-in that creates an echo effect in PCM audio during playback.</span></span> <span data-ttu-id="449ac-110">外掛程式的目標如下：</span><span class="sxs-lookup"><span data-stu-id="449ac-110">The goals for the plug-in are as follows:</span></span>

-   <span data-ttu-id="449ac-111">外掛程式只會處理8位或16位 PCM 音訊。</span><span class="sxs-lookup"><span data-stu-id="449ac-111">The plug-in processes 8-bit or 16-bit PCM audio only.</span></span>
-   <span data-ttu-id="449ac-112">它支援介於10毫秒之間的延遲時間 (ms) 和2000毫秒 (2 秒的) 。</span><span class="sxs-lookup"><span data-stu-id="449ac-112">It supports a delay time between 10 milliseconds (ms) and 2000 ms (2 seconds).</span></span> <span data-ttu-id="449ac-113">這代表大部分應用程式的實際範圍。</span><span class="sxs-lookup"><span data-stu-id="449ac-113">This represents a practical range for most applications.</span></span>
-   <span data-ttu-id="449ac-114">它支援混合原始信號與延遲信號。</span><span class="sxs-lookup"><span data-stu-id="449ac-114">It supports mixing of the original signal with the delay signal.</span></span>
-   <span data-ttu-id="449ac-115">它提供了屬性頁的執行，可讓使用者提供延遲時間的值，以及相對於整體音訊信號層級的延遲信號百分比值。</span><span class="sxs-lookup"><span data-stu-id="449ac-115">It provides a property page implementation that allows the user to provide a value for the delay time and a value for the percentage of delay signal relative to the overall audio signal level.</span></span>
-   <span data-ttu-id="449ac-116">您可以藉由修改 Windows Media Player 外掛程式 Wizard 音訊 DSP 外掛程式範例來建立程式碼。</span><span class="sxs-lookup"><span data-stu-id="449ac-116">The code is created by modifying the Windows Media Player Plug-in Wizard audio DSP plug-in sample.</span></span>

<span data-ttu-id="449ac-117">Echo 範例不包含在 Windows Media Player SDK 中;它是您所建立的範例。</span><span class="sxs-lookup"><span data-stu-id="449ac-117">The Echo sample is not included with the Windows Media Player SDK; it is a sample that you create.</span></span> <span data-ttu-id="449ac-118">若要建立 Echo 範例，您必須從 Windows Media Player 外掛程式 Wizard 中的預設專案開始。</span><span class="sxs-lookup"><span data-stu-id="449ac-118">To create the Echo sample, you must start with the default project from the Windows Media Player Plug-in Wizard.</span></span> <span data-ttu-id="449ac-119">您可以將專案命名為任何您喜歡的專案;本檔假設專案命名為 Echo。</span><span class="sxs-lookup"><span data-stu-id="449ac-119">You can name the project whatever you like; this documentation assumes the project is named Echo.</span></span> <span data-ttu-id="449ac-120">如需使用 wizard 的詳細資訊，請參閱 [建立 DSP 外掛程式](building-a-dsp-plug-in.md)。</span><span class="sxs-lookup"><span data-stu-id="449ac-120">For details about using the wizard, see [Building a DSP Plug-in](building-a-dsp-plug-in.md).</span></span>

<span data-ttu-id="449ac-121">下一節將概述範例如何建立回應效果：</span><span class="sxs-lookup"><span data-stu-id="449ac-121">The following section provides an overview of how the sample creates an echo effect:</span></span>

-   [<span data-ttu-id="449ac-122">Echo 範例的運作方式</span><span class="sxs-lookup"><span data-stu-id="449ac-122">How the Echo Sample Works</span></span>](how-the-echo-sample-works.md)

## <a name="related-topics"></a><span data-ttu-id="449ac-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="449ac-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="449ac-124">**Echo 範例**</span><span class="sxs-lookup"><span data-stu-id="449ac-124">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




