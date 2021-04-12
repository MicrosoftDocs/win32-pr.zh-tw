---
title: Windows Media Player 的 DSP 外掛程式
description: Windows Media Player 的 DSP 外掛程式
ms.assetid: 1c7202c4-ca66-491d-9a5f-26032cad1dcc
keywords:
- Windows Media Player、外掛程式
- Windows Media Player，DSP 外掛程式
- 'Windows Media Player 外掛程式、數位信號處理 (DSP) '
- '外掛程式，數位信號處理 (DSP) '
- 數位信號處理外掛程式，關於
- DSP 外掛程式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755088bce89530350997d2f543e30872f630e882
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462309"
---
# <a name="windows-media-player-dsp-plug-ins"></a><span data-ttu-id="6a87a-109">Windows Media Player 的 DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="6a87a-109">Windows Media Player DSP Plug-ins</span></span>

<span data-ttu-id="6a87a-110">Microsoft Windows Media Player 提供的架構可讓使用者安裝及啟動外掛程式程式，以新增數位信號處理 (DSP) 功能。</span><span class="sxs-lookup"><span data-stu-id="6a87a-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add digital signal processing (DSP) functionality.</span></span> <span data-ttu-id="6a87a-111">DSP 外掛程式是一種 Microsoft DirectX 媒體物件 (的) 或使用 COM 介面連接到播放程式的媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="6a87a-111">A DSP plug-in is a Microsoft DirectX Media Object (DMO) or a Media Foundation Transform (MFT) that connects to the Player by using COM interfaces.</span></span> <span data-ttu-id="6a87a-112">典型的 DSP 外掛程式可能是音訊等化器或影片色調控制項。</span><span class="sxs-lookup"><span data-stu-id="6a87a-112">A typical DSP plug-in might be an audio equalizer or a video tint control.</span></span> <span data-ttu-id="6a87a-113">SDK 的這個部分會提供您建立自己的 DSP 外掛程式所需的程式設計資訊。</span><span class="sxs-lookup"><span data-stu-id="6a87a-113">This section of the SDK provides the programming information you need to create your own DSP plug-in.</span></span>

<span data-ttu-id="6a87a-114">DSP 外掛程式檔分成下列三個區段。</span><span class="sxs-lookup"><span data-stu-id="6a87a-114">The DSP plug-in documentation is divided into the following three sections.</span></span>



| <span data-ttu-id="6a87a-115">區段</span><span class="sxs-lookup"><span data-stu-id="6a87a-115">Section</span></span>                                                                      | <span data-ttu-id="6a87a-116">描述</span><span class="sxs-lookup"><span data-stu-id="6a87a-116">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a87a-117">關於 DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="6a87a-117">About DSP Plug-ins</span></span>](about-dsp-plug-ins.md)                                 | <span data-ttu-id="6a87a-118">提供用於 DSP 外掛程式的架構總覽。閱讀本節，以瞭解與此技術相關的一般概念。</span><span class="sxs-lookup"><span data-stu-id="6a87a-118">Provides an overview of the architecture used for DSP plug-ins. Read this section to learn the general concepts involved with this technology.</span></span>  |
| [<span data-ttu-id="6a87a-119">DSP 外掛程式程式設計指南</span><span class="sxs-lookup"><span data-stu-id="6a87a-119">DSP Plug-ins Programming Guide</span></span>](dsp-plug-ins-programming-guide.md)         | <span data-ttu-id="6a87a-120">說明建立 DSP 外掛程式的必要動作。</span><span class="sxs-lookup"><span data-stu-id="6a87a-120">Explains what you need to do to create a DSP plug-in.</span></span> <span data-ttu-id="6a87a-121">本節包含範例程式碼和逐步執行程式。</span><span class="sxs-lookup"><span data-stu-id="6a87a-121">This section contains example code and step-by-step procedures.</span></span>                           |
| [<span data-ttu-id="6a87a-122">DSP 外掛程式程式設計參考</span><span class="sxs-lookup"><span data-stu-id="6a87a-122">DSP Plug-ins Programming Reference</span></span>](dsp-plug-ins-programming-reference.md) | <span data-ttu-id="6a87a-123">提供適用于 DSP 外掛程式的 Windows Media Player SDK 所支援的 COM 介面、方法和列舉類型的詳細參考。</span><span class="sxs-lookup"><span data-stu-id="6a87a-123">Provides a detailed reference for the COM interfaces, methods, and enumerated types supported by the Windows Media Player SDK for DSP plug-ins.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6a87a-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="6a87a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a87a-125">**Windows Media Player 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="6a87a-125">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




