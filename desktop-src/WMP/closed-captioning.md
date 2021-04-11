---
title: 隱藏式字幕功能
description: 隱藏式字幕功能
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- 'Windows Media Player，可同步的可存取媒體交換 (薩米文) '
- 'Windows Media Player 物件模型、已同步處理的可存取媒體交換 (薩米文) '
- '物件模型、同步的可存取媒體交換 (薩米) '
- 'Windows Media Player 行動裝置、已同步處理的可存取媒體交換 (薩米文) '
- 'Windows Media Player ActiveX 控制項、同步存取媒體交換 (薩米文) '
- 'Windows Media Player 的行動 ActiveX 控制項、已同步處理的可存取媒體交換 (薩米文) '
- 'ActiveX 控制項、同步的可存取媒體交換 (薩米) '
- Windows Media Player，遷移隱藏式輔助字幕
- Windows Media Player 物件模型、Smigrating 隱藏式輔助字幕
- 物件模型，遷移隱藏式輔助字幕
- Windows Media Player 行動裝置，遷移隱藏式輔助字幕
- Windows Media Player ActiveX 控制項、遷移隱藏式輔助字幕
- Windows Media Player 行動 ActiveX 控制項、遷移隱藏式輔助字幕
- ActiveX 控制項，遷移隱藏式輔助字幕
- 已同步處理的可存取媒體交換 (薩米) ，正在遷移隱藏式輔助字幕
- 薩米文 (同步處理可存取媒體交換) ，遷移隱藏式輔助字幕
- '遷移指南，同步處理的可存取媒體交換 (薩米) '
- 遷移指南，隱藏式輔助字幕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092564"
---
# <a name="closed-captioning"></a><span data-ttu-id="c73b2-121">隱藏式字幕功能</span><span class="sxs-lookup"><span data-stu-id="c73b2-121">Closed Captioning</span></span>

<span data-ttu-id="c73b2-122">Windows Media Player 6.4 ActiveX 控制項包含整合式隱藏式輔助字幕顯示面板，當它顯示時，會啟用同步的可存取媒體交換 (薩米) 隱藏式輔助字幕，並顯示隱藏的標題文字。</span><span class="sxs-lookup"><span data-stu-id="c73b2-122">The Windows Media Player 6.4 ActiveX control includes an integrated closed caption display panel that, when made visible, enables Synchronized Accessible Media Interchange (SAMI) closed captions and displays the closed caption text.</span></span> <span data-ttu-id="c73b2-123">Windows Media Player 7 或更新版本的控制項可讓您使用 HTML 元素，啟用以薩米的隱藏式輔助字幕顯示 **<DIV>** 。</span><span class="sxs-lookup"><span data-stu-id="c73b2-123">The Windows Media Player 7 or later control enables SAMI closed caption display by using an HTML **<DIV>** element.</span></span> <span data-ttu-id="c73b2-124">例如：</span><span class="sxs-lookup"><span data-stu-id="c73b2-124">For example:</span></span>


```C++
<DIV  ID = "CCDiv"></DIV>

```



<span data-ttu-id="c73b2-125">這項技術可提供您完整的彈性，因為您可以設計網頁以自訂的方式顯示隱藏式輔助字幕;隱藏式輔助字幕顯示不再需要位於 Windows Media Player 使用者介面旁的固定位置。</span><span class="sxs-lookup"><span data-stu-id="c73b2-125">This technique provides you with complete flexibility, since you can design your webpage to display closed captions in a customized manner; the closed caption display is no longer required to be in a fixed location adjacent to the Windows Media Player user interface.</span></span>

<span data-ttu-id="c73b2-126">建立區域以顯示隱藏式輔助字幕之後，請使用 *ClosedCaption*。**captioningID** 屬性，指定 Windows Media Player 呈現隱藏式輔助字幕文字的位置。</span><span class="sxs-lookup"><span data-stu-id="c73b2-126">Once you have created an area to display closed captions, use the *ClosedCaption*.**captioningID** property to specify the location where Windows Media Player renders the closed caption text.</span></span>


```C++
Player.closedCaption.captioningID = "CCDiv";

```



<span data-ttu-id="c73b2-127">Windows Media Player 軟體發展工具組 (SDK) 包含可顯示隱藏式輔助字幕文字之內嵌播放程式的工作範例。</span><span class="sxs-lookup"><span data-stu-id="c73b2-127">The Windows Media Player Software Development Kit (SDK) contains a working sample of an embedded Player that displays closed caption text.</span></span> <span data-ttu-id="c73b2-128">若要取得 SDK 範例，請從 Microsoft 網站下載並安裝完整的 Windows Media Player SDK。</span><span class="sxs-lookup"><span data-stu-id="c73b2-128">To get the SDK samples, download and install the complete Windows Media Player SDK from the Microsoft Web Site.</span></span> <span data-ttu-id="c73b2-129">如需隱藏式輔助字幕和薩米文的詳細資訊，請參閱 [Microsoft 協助工具網站](https://www.microsoft.com/enable/)。</span><span class="sxs-lookup"><span data-stu-id="c73b2-129">For more information about closed captions and SAMI, see the [Microsoft Accessibility website](https://www.microsoft.com/enable/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c73b2-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="c73b2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c73b2-131">**將隱藏式輔助字幕新增至數位媒體**</span><span class="sxs-lookup"><span data-stu-id="c73b2-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="c73b2-132">**ClosedCaption 物件**</span><span class="sxs-lookup"><span data-stu-id="c73b2-132">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="c73b2-133">**物件模型遷移指南**</span><span class="sxs-lookup"><span data-stu-id="c73b2-133">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




