---
title: Windows Media Player 消費者介面外掛程式
description: Windows Media Player 消費者介面外掛程式
ms.assetid: 71f53abe-310f-429a-bb23-5291bebdc432
keywords:
- Windows Media Player、外掛程式
- Windows Media Player，使用者介面外掛程式
- Windows Media Player 外掛程式、使用者介面
- 外掛程式，使用者介面
- 使用者介面外掛程式，關於
- UI 外掛程式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24050f24ef4412d3de9efd5faac6c2af90451dc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968422"
---
# <a name="windows-media-player-user-interface-plug-ins"></a><span data-ttu-id="dea28-109">Windows Media Player 消費者介面外掛程式</span><span class="sxs-lookup"><span data-stu-id="dea28-109">Windows Media Player User Interface Plug-ins</span></span>

<span data-ttu-id="dea28-110">Microsoft Windows Media Player 提供的架構可讓使用者安裝並啟動外掛程式程式，將使用者介面 (UI) 功能新增至播放程式的完整模式。</span><span class="sxs-lookup"><span data-stu-id="dea28-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add user interface (UI) functionality to the full mode of the player.</span></span> <span data-ttu-id="dea28-111">一般的 UI 外掛程式可讓使用者購買包含目前播放曲目的 CD，或存取演出者的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dea28-111">A typical UI plug-in might allow a user to buy the CD that contains the currently playing track or to access additional information about the artist.</span></span> <span data-ttu-id="dea28-112">Windows Media Player 軟體發展工具組 (SDK) 的這一節會提供您建立自己的 UI 外掛程式所需的程式設計資訊。</span><span class="sxs-lookup"><span data-stu-id="dea28-112">This section of the Windows Media Player Software Development Kit (SDK) provides you with the programming information you need to create your own UI plug-in.</span></span>

<span data-ttu-id="dea28-113">UI 外掛程式檔分為三個部分：</span><span class="sxs-lookup"><span data-stu-id="dea28-113">The UI plug-in documentation is divided into three sections:</span></span>



| <span data-ttu-id="dea28-114">區段</span><span class="sxs-lookup"><span data-stu-id="dea28-114">Section</span></span>                                                                                            | <span data-ttu-id="dea28-115">描述</span><span class="sxs-lookup"><span data-stu-id="dea28-115">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dea28-116">關於消費者介面外掛程式</span><span class="sxs-lookup"><span data-stu-id="dea28-116">About User Interface Plug-ins</span></span>](about-user-interface-plug-ins.md)                                 | <span data-ttu-id="dea28-117">提供用於 UI 外掛程式的架構總覽。閱讀本節，以瞭解與此技術相關的一般概念。</span><span class="sxs-lookup"><span data-stu-id="dea28-117">Provides an overview of the architecture used for UI plug-ins. Read this section to learn the general concepts involved with this technology.</span></span> |
| [<span data-ttu-id="dea28-118">消費者介面外掛程式程式設計指南</span><span class="sxs-lookup"><span data-stu-id="dea28-118">User Interface Plug-ins Programming Guide</span></span>](user-interface-plug-ins-programming-guide.md)         | <span data-ttu-id="dea28-119">說明建立 UI 外掛程式的必要動作。</span><span class="sxs-lookup"><span data-stu-id="dea28-119">Explains what you need to do to create a UI plug-in.</span></span> <span data-ttu-id="dea28-120">本節包含範例程式碼和逐步執行程式。</span><span class="sxs-lookup"><span data-stu-id="dea28-120">This section contains example code and step-by-step procedures.</span></span>                          |
| [<span data-ttu-id="dea28-121">消費者介面外掛程式程式設計參考</span><span class="sxs-lookup"><span data-stu-id="dea28-121">User Interface Plug-ins Programming Reference</span></span>](user-interface-plug-ins-programming-reference.md) | <span data-ttu-id="dea28-122">提供適用于 UI 外掛程式的 Windows Media Player SDK 所支援的 COM 介面和方法的詳細參考。</span><span class="sxs-lookup"><span data-stu-id="dea28-122">Provides a detailed reference for the COM interface and methods supported by the Windows Media Player SDK for UI plug-ins.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="dea28-123">Windows Media Player 10 行動版提供與桌面 Windows Media Player 相同的外掛程式模型。</span><span class="sxs-lookup"><span data-stu-id="dea28-123">Windows Media Player 10 Mobile provides the same plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="dea28-124">此外掛程式模型可讓您使用背景外掛程式來監視事件、顯示內容狀態等等。</span><span class="sxs-lookup"><span data-stu-id="dea28-124">This plug-in model enables you to use background plug-ins for monitoring events, displaying the status of properties, and so on.</span></span> <span data-ttu-id="dea28-125">本節中的程式設計指南說明如何使用桌面 Windows Media Player 外掛程式 Wizard 建立 Windows Media Player 10 Mobile 的背景 UI 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="dea28-125">The programming guide in this section describes how to create a background UI plug-in for Windows Media Player 10 Mobile by using the desktop Windows Media Player Plug-in Wizard.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dea28-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="dea28-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dea28-127">**Windows Media Player 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="dea28-127">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




