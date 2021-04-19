---
title: 外觀建立指南
description: 外觀建立指南
ms.assetid: 86c77764-5c8c-4493-ac2d-15268c1ba564
keywords:
- Windows Media Player，外觀
- Windows Media Player 的外觀，建立指南
- 外觀，建立指南
- 建立外觀，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214accedf24bd80449bf8952bc9268f9b9bf49d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968029"
---
# <a name="skin-creation-guide"></a><span data-ttu-id="39244-107">外觀建立指南</span><span class="sxs-lookup"><span data-stu-id="39244-107">Skin Creation Guide</span></span>

<span data-ttu-id="39244-108">本指南是如何建立不同類型之外觀的一系列詳細說明。</span><span class="sxs-lookup"><span data-stu-id="39244-108">This guide is a series of detailed explanations of how to create different kinds of skins.</span></span> <span data-ttu-id="39244-109">如需有關面板的一般資訊，請參閱 [關於外觀](about-skins.md)。</span><span class="sxs-lookup"><span data-stu-id="39244-109">For more general information on skins, see [About Skins](about-skins.md).</span></span> <span data-ttu-id="39244-110">如需有關面板中所使用之每個屬性、方法和事件的特定詳細資料，請參閱面板程式 [設計參考](skin-programming-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="39244-110">For specific details about every attribute, method, and event used in skins, see the [Skin Programming Reference](skin-programming-reference.md).</span></span> <span data-ttu-id="39244-111">當您在面板的程式設計方面有更多的相關資訊時，您可能會想要閱讀此 SDK 中涵蓋 [Windows Media Player 物件模型](windows-media-player-object-model.md)的部分。</span><span class="sxs-lookup"><span data-stu-id="39244-111">As you get more involved in the programming of your skin, you may want to read the part of this SDK covering the [Windows Media Player Object Model](windows-media-player-object-model.md).</span></span>

<span data-ttu-id="39244-112">在本指南中，會為 Adobe Photoshop 5.5 （熱門的藝術操作程式）提供建立藝術的相關指示。</span><span class="sxs-lookup"><span data-stu-id="39244-112">In this guide, instructions for creating the art will be given for Adobe Photoshop 5.5, a popular art manipulation program.</span></span> <span data-ttu-id="39244-113">如果您有類似的藝術節目，例如 Jasc 油漆店 Pro 或 Sonic Foundry Viscosity，則特定的指示可能會有所不同，但概念會相同。</span><span class="sxs-lookup"><span data-stu-id="39244-113">The specific instructions may be different if you have a similar art program such as Jasc Paint Shop Pro or Sonic Foundry Viscosity, but the concepts will be the same.</span></span> <span data-ttu-id="39244-114">因為有兩個原因，所以選擇了 Photoshop：它是適用于商業演出者的熱門程式，且適用于圖層。</span><span class="sxs-lookup"><span data-stu-id="39244-114">Photoshop was chosen for two reasons: it is a popular art program for commercial artists, and it works with layers.</span></span> <span data-ttu-id="39244-115">您將在教學課程中看到，圖層在建立面板時非常有用。</span><span class="sxs-lookup"><span data-stu-id="39244-115">As you will see in the tutorials, layers are very useful for skin creation.</span></span>

<span data-ttu-id="39244-116">本指南將涵蓋下列工作。</span><span class="sxs-lookup"><span data-stu-id="39244-116">This guide will cover the following tasks.</span></span>



| <span data-ttu-id="39244-117">Task</span><span class="sxs-lookup"><span data-stu-id="39244-117">Task</span></span>                                                     | <span data-ttu-id="39244-118">Description</span><span class="sxs-lookup"><span data-stu-id="39244-118">Description</span></span>                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39244-119">建立您的第一個外觀</span><span class="sxs-lookup"><span data-stu-id="39244-119">Building Your First Skin</span></span>](building-your-first-skin.md) | <span data-ttu-id="39244-120">啟動和停止 Windows Media Player 的簡單面板逐步解說。</span><span class="sxs-lookup"><span data-stu-id="39244-120">A walk-through of a simple skin that starts and stops Windows Media Player.</span></span>                     |
| [<span data-ttu-id="39244-121">新增播放清單</span><span class="sxs-lookup"><span data-stu-id="39244-121">Adding a Playlist</span></span>](adding-a-playlist.md)               | <span data-ttu-id="39244-122">如何使用簡單的播放清單。</span><span class="sxs-lookup"><span data-stu-id="39244-122">How to use a simple playlist.</span></span>                                                                   |
| [<span data-ttu-id="39244-123">選擇檔案</span><span class="sxs-lookup"><span data-stu-id="39244-123">Choosing Files</span></span>](choosing-files.md)                     | <span data-ttu-id="39244-124">如何使用 [開啟檔案] 對話方塊來挑選檔案。</span><span class="sxs-lookup"><span data-stu-id="39244-124">How to pick files with an open file dialog box.</span></span>                                                 |
| [<span data-ttu-id="39244-125">新增影片</span><span class="sxs-lookup"><span data-stu-id="39244-125">Adding Video</span></span>](adding-video.md)                         | <span data-ttu-id="39244-126">如何將影片視窗放入您的外觀。</span><span class="sxs-lookup"><span data-stu-id="39244-126">How to put a video window into your skin.</span></span>                                                       |
| [<span data-ttu-id="39244-127">新增視覺效果</span><span class="sxs-lookup"><span data-stu-id="39244-127">Adding Visualizations</span></span>](adding-visualizations.md)       | <span data-ttu-id="39244-128">如何新增視覺效果。</span><span class="sxs-lookup"><span data-stu-id="39244-128">How to add visualizations.</span></span>                                                                      |
| [<span data-ttu-id="39244-129">新增滑杆</span><span class="sxs-lookup"><span data-stu-id="39244-129">Adding a Slider</span></span>](adding-a-slider.md)                   | <span data-ttu-id="39244-130">如何使用滑杆來追蹤媒體內容的進度 .。。然後讓使用者變更！</span><span class="sxs-lookup"><span data-stu-id="39244-130">How to use a slider to track the progress of your media content ... and let the user change it!</span></span> |
| [<span data-ttu-id="39244-131">建立自訂滑杆</span><span class="sxs-lookup"><span data-stu-id="39244-131">Creating Custom Sliders</span></span>](creating-custom-sliders.md)   | <span data-ttu-id="39244-132">如何使用自訂滑杆控制磁片區。</span><span class="sxs-lookup"><span data-stu-id="39244-132">How to control the volume with a custom slider.</span></span>                                                 |
| [<span data-ttu-id="39244-133">其他外觀範例</span><span class="sxs-lookup"><span data-stu-id="39244-133">Other Skin Samples</span></span>](other-skin-samples.md)             | <span data-ttu-id="39244-134">請參閱 SDK 的範例一節。</span><span class="sxs-lookup"><span data-stu-id="39244-134">See the samples section of the SDK.</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="39244-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="39244-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39244-136">**Windows Media Player 的外觀**</span><span class="sxs-lookup"><span data-stu-id="39244-136">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




