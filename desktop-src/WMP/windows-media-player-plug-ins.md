---
title: Windows Media Player 外掛程式
description: Windows Media Player 外掛程式
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Windows Media Player、外掛程式
- Windows Media Player 外掛程式，關於
- 外掛程式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969115"
---
# <a name="windows-media-player-plug-ins"></a><span data-ttu-id="639c9-106">Windows Media Player 外掛程式</span><span class="sxs-lookup"><span data-stu-id="639c9-106">Windows Media Player Plug-ins</span></span>

<span data-ttu-id="639c9-107">Microsoft Windows Media Player 公開介面，可讓您以數種方式擴充功能。</span><span class="sxs-lookup"><span data-stu-id="639c9-107">Microsoft Windows Media Player exposes interfaces that allow you to extend functionality in several ways.</span></span> <span data-ttu-id="639c9-108">下列各節說明支援的外掛程式架構，以及建立外掛程式的程式：</span><span class="sxs-lookup"><span data-stu-id="639c9-108">The following sections describe the supported plug-in architectures and the process of building a plug-in:</span></span>



| <span data-ttu-id="639c9-109">區段</span><span class="sxs-lookup"><span data-stu-id="639c9-109">Section</span></span>                                                                                                         | <span data-ttu-id="639c9-110">描述</span><span class="sxs-lookup"><span data-stu-id="639c9-110">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="639c9-111">建立外掛程式</span><span class="sxs-lookup"><span data-stu-id="639c9-111">Building a Plug-in</span></span>](building-a-plug-in.md)                                                                    | <span data-ttu-id="639c9-112">您可以使用 Visual Studio 和 Windows Media Player 外掛程式嚮導來建立數種類型的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="639c9-112">You can build several types of plug-ins by using Visual Studio and the Windows Media Player plug-in wizard.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="639c9-113">Windows Media Player 自訂視覺效果</span><span class="sxs-lookup"><span data-stu-id="639c9-113">Windows Media Player Custom Visualizations</span></span>](windows-media-player-custom-visualizations.md)                    | <span data-ttu-id="639c9-114">Windows Media Player 的視覺效果是元件物件模型 (COM) 物件，可用來顯示與播放程式媒體播放播放音訊部分同步的視覺效果影像。</span><span class="sxs-lookup"><span data-stu-id="639c9-114">Windows Media Player visualizations are Component Object Model (COM) objects used to display visual imagery that is synchronized to the audio portion of the media playback of the player.</span></span> <span data-ttu-id="639c9-115">您可以使用 Microsoft Visual C++ 來建立自訂視覺效果。</span><span class="sxs-lookup"><span data-stu-id="639c9-115">Custom visualizations can be created using Microsoft Visual C++.</span></span>                                             |
| [<span data-ttu-id="639c9-116">Windows Media Player 消費者介面外掛程式</span><span class="sxs-lookup"><span data-stu-id="639c9-116">Windows Media Player User Interface Plug-ins</span></span>](windows-media-player-user-interface-plug-ins.md)                | <span data-ttu-id="639c9-117">Windows Media Player 的使用者介面外掛程式會將新功能新增至完整模式播放程式的 [ **立即播放** ] 窗格。</span><span class="sxs-lookup"><span data-stu-id="639c9-117">Windows Media Player user interface plug-ins add new functionality to the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="639c9-118">您可以建立使用視覺效果區域、個別視窗、設定區域、中繼資料區域或背景外掛程式的外掛程式，以公開沒有可見的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="639c9-118">You can create plug-ins that use the visualization area, a separate window, the settings area, the metadata area, or background plug-ins that expose no visible user interface.</span></span> |
| [<span data-ttu-id="639c9-119">Windows Media Player 的 DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="639c9-119">Windows Media Player DSP Plug-ins</span></span>](windows-media-player-dsp-plug-ins.md)                                      | <span data-ttu-id="639c9-120">Windows Media Player 的 DSP 外掛程式會在播放程式呈現音訊和影片之前，修改或處理音訊和影片資料。</span><span class="sxs-lookup"><span data-stu-id="639c9-120">Windows Media Player DSP plug-ins modify or process audio and video data before it is rendered by the Player.</span></span> <span data-ttu-id="639c9-121">DSP 外掛程式是透過 COM 介面連接到播放程式的 DirectX 媒體物件 (SQL-DMO) 。</span><span class="sxs-lookup"><span data-stu-id="639c9-121">DSP plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                                           |
| <span data-ttu-id="639c9-122">[Windows Media Player 轉譯外掛程式 (已淘汰) ](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="639c9-122">[Windows Media Player Rendering Plug-ins (deprecated)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span></span> | <span data-ttu-id="639c9-123">如有必要，Windows Media Player 轉譯外掛程式解碼 () 和轉譯 Windows Media 格式資料流程中包含的自訂資料。</span><span class="sxs-lookup"><span data-stu-id="639c9-123">Windows Media Player rendering plug-ins decode (if necessary) and render custom data contained in a Windows Media format stream.</span></span> <span data-ttu-id="639c9-124">轉譯外掛程式是透過 COM 介面連接到播放程式的 DirectX 媒體物件 (SQL-DMO) 。</span><span class="sxs-lookup"><span data-stu-id="639c9-124">Rendering plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                  |
| [<span data-ttu-id="639c9-125">Windows Media Player 轉換外掛程式</span><span class="sxs-lookup"><span data-stu-id="639c9-125">Windows Media Player Conversion Plug-ins</span></span>](windows-media-player-conversion-plug-ins.md)                        | <span data-ttu-id="639c9-126">Windows Media Player 轉換外掛程式會將使用 Microsoft 未提供的技術所建立的數位媒體檔案轉換成 Advanced Systems 格式 (ASF) 。</span><span class="sxs-lookup"><span data-stu-id="639c9-126">Windows Media Player conversion plug-ins convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="639c9-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="639c9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="639c9-128">**Windows Media Player SDK**</span><span class="sxs-lookup"><span data-stu-id="639c9-128">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 