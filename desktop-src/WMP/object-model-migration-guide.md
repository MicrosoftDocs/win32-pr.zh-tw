---
title: 物件模型遷移指南
description: 物件模型遷移指南
ms.assetid: 2fd4f7ec-36b0-49da-9a11-546dd41c7a98
keywords:
- Windows Media Player，物件模型
- Windows Media Player，遷移指南
- Windows Media Player 物件模型，遷移指南
- 物件模型，遷移指南
- Windows Media Player ActiveX 控制項，遷移指南
- ActiveX 控制項，遷移指南
- Windows Media Player Mobile ActiveX 控制項，遷移指南
- Windows Media Player 行動裝置，物件模型
- Windows Media Player 行動裝置，遷移指南
- 遷移指南，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29c9be40e3cc252ed9461bcb18ea5bfed49bb58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021876"
---
# <a name="object-model-migration-guide"></a><span data-ttu-id="7b5b8-113">物件模型遷移指南</span><span class="sxs-lookup"><span data-stu-id="7b5b8-113">Object Model Migration Guide</span></span>

<span data-ttu-id="7b5b8-114">Windows Media Player 7 引進了新的物件模型，提供一組豐富的新功能，讓您可以用來增強網頁。</span><span class="sxs-lookup"><span data-stu-id="7b5b8-114">Windows Media Player 7 introduced a new object model that offers a rich new set of functionality that you can use to enhance your webpages.</span></span> <span data-ttu-id="7b5b8-115">後續版本已使用其他屬性、方法和事件擴充第7版物件模型。</span><span class="sxs-lookup"><span data-stu-id="7b5b8-115">Subsequent versions have extended the version 7 object model with additional properties, methods, and events.</span></span> <span data-ttu-id="7b5b8-116">不過，新的物件模型與 Windows Media Player 6.4 物件模型的差異很大，因此，如果您想要在專案中支援 Windows Media Player 7 和更新版本，您必須瞭解如何更新現有的程式碼。</span><span class="sxs-lookup"><span data-stu-id="7b5b8-116">However, the new object model differs substantially from the Windows Media Player 6.4 object model, so you need to understand how to update your existing code if you want to support Windows Media Player 7 and later in your projects.</span></span>

<span data-ttu-id="7b5b8-117">如需示範如何偵測使用者的 Windows Media Player 版本和目前瀏覽器的範例，請參閱此 SDK 所安裝的名稱為「偵測」的範例。</span><span class="sxs-lookup"><span data-stu-id="7b5b8-117">For a sample that demonstrates how to detect the user's Windows Media Player version and current browser, see the sample named "detection" that is installed with this SDK.</span></span> <span data-ttu-id="7b5b8-118">如需範例的詳細資訊，請參閱 [範例](samples.md)。</span><span class="sxs-lookup"><span data-stu-id="7b5b8-118">For more information about samples, see [Samples](samples.md).</span></span>

<span data-ttu-id="7b5b8-119">本指南將新的物件模型參考為 Windows Media Player 7 或更新版本的物件模型。</span><span class="sxs-lookup"><span data-stu-id="7b5b8-119">This guide refers to the new object model as the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="7b5b8-120">如需每個 Windows Media Player 版本中可用功能的詳細資訊，請參閱 [腳本的物件模型參考](object-model-reference-for-scripting.md)。</span><span class="sxs-lookup"><span data-stu-id="7b5b8-120">For details about which functionality is available in each version of Windows Media Player, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

<span data-ttu-id="7b5b8-121">下列主題涵蓋這些物件模型問題：</span><span class="sxs-lookup"><span data-stu-id="7b5b8-121">These object model issues are covered by the following topics:</span></span>

-   [<span data-ttu-id="7b5b8-122">物件模型之間的差異</span><span class="sxs-lookup"><span data-stu-id="7b5b8-122">Differences Between the Object Models</span></span>](differences-between-the-object-models.md)
-   [<span data-ttu-id="7b5b8-123">使用 Windows Media Player 7 或更新版本的物件模型</span><span class="sxs-lookup"><span data-stu-id="7b5b8-123">Using the Windows Media Player 7 or Later Object Model</span></span>](using-the-windows-media-player-7-or-later-object-model.md)
-   [<span data-ttu-id="7b5b8-124">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="7b5b8-124">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="7b5b8-125">播放清單</span><span class="sxs-lookup"><span data-stu-id="7b5b8-125">Playlists</span></span>](playlists.md)
-   [<span data-ttu-id="7b5b8-126">隱藏式輔助字幕</span><span class="sxs-lookup"><span data-stu-id="7b5b8-126">Closed Captioning</span></span>](closed-captioning.md)
-   [<span data-ttu-id="7b5b8-127">Dvd</span><span class="sxs-lookup"><span data-stu-id="7b5b8-127">DVD</span></span>](dvd.md)
-   [<span data-ttu-id="7b5b8-128">詳細的物件模型比較</span><span class="sxs-lookup"><span data-stu-id="7b5b8-128">Detailed Object Model Comparison</span></span>](detailed-object-model-comparison.md)

## <a name="related-topics"></a><span data-ttu-id="7b5b8-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b5b8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b5b8-130">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="7b5b8-130">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




