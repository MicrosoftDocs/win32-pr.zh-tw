---
title: 關於 PlayerApplication 物件
description: 關於 PlayerApplication 物件
ms.assetid: 4b77bf16-d7e1-4119-91c2-46136db13e81
keywords:
- Windows Media Player，PlayerApplication 物件
- Windows Media Player 物件模型，PlayerApplication 物件
- 物件模型，PlayerApplication 物件
- Windows Media Player ActiveX 控制項，PlayerApplication 物件
- ActiveX 控制項，PlayerApplication 物件
- Windows Media Player 行動 ActiveX 控制項，PlayerApplication 物件
- Windows Media Player Mobile，PlayerApplication 物件
- PlayerApplication 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d197614ba75a51bdc8ec5398ca757e410f918a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840480"
---
# <a name="about-the-playerapplication-object"></a><span data-ttu-id="da375-111">關於 PlayerApplication 物件</span><span class="sxs-lookup"><span data-stu-id="da375-111">About the PlayerApplication Object</span></span>

<span data-ttu-id="da375-112">**PlayerApplication** 物件用於遠端 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="da375-112">The **PlayerApplication** object is used for remoting Windows Media Player.</span></span> <span data-ttu-id="da375-113">它提供切換遠端 Windows Media Player 控制項和播放程式完整模式所需的功能。</span><span class="sxs-lookup"><span data-stu-id="da375-113">It provides the functionality required to switch between a remoted Windows Media Player control and the full mode of the Player.</span></span>

<span data-ttu-id="da375-114">遠端功能可讓內嵌在 c + + 應用程式中的 Windows Media Player 控制項使用與播放程式相同的播放引擎。</span><span class="sxs-lookup"><span data-stu-id="da375-114">Remoting enables a Windows Media Player control embedded in a C++ application to use the same playback engine as the Player.</span></span> <span data-ttu-id="da375-115">這表示通常您會使用 COM 介面，在 c + + 程式碼中使用 **PlayerApplication** 物件。</span><span class="sxs-lookup"><span data-stu-id="da375-115">This means that usually you will use the **PlayerApplication** object in C++ code using the COM interfaces.</span></span> <span data-ttu-id="da375-116">不過，有一個特殊情況，您可以在其中內嵌 Windows Media Player 控制項，以將 Windows Media Player 的外觀顯示為其使用者介面。</span><span class="sxs-lookup"><span data-stu-id="da375-116">There is a special case, however, where you can embed the Windows Media Player control that displays a Windows Media Player skin as its user interface.</span></span> <span data-ttu-id="da375-117">在此情況下， **PlayerApplication** 可以使用面板程式碼中的 JScript 進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="da375-117">In this case, **PlayerApplication** can be programmed using JScript in the skin code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da375-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="da375-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da375-119">**指令碼語言的播放程式物件模型**</span><span class="sxs-lookup"><span data-stu-id="da375-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="da375-120">**PlayerApplication 物件**</span><span class="sxs-lookup"><span data-stu-id="da375-120">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> </dl>

 

 




