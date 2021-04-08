---
title: 使用 DirectX 建立您的第一個 Windows 應用程式
description: 本節說明為什麼您會使用 c + + 模型進行 Windows Store 應用程式開發，並提供開始進行 DirectX 應用程式開發的基本教學課程和程式。
ms.assetid: b632ba9c-1c30-4d21-ac79-7f2a193956fe
keywords:
- DirectX 應用程式，使用者入門
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5e3afed57244789c0e3e06ab71ec39e581305c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670968"
---
# <a name="create-your-first-windows-app-using-directx"></a><span data-ttu-id="b26c3-104">使用 DirectX 建立您的第一個 Windows 應用程式</span><span class="sxs-lookup"><span data-stu-id="b26c3-104">Create your first Windows app using DirectX</span></span>

<span data-ttu-id="b26c3-105">如果您知道 DirectX，可以使用原生 c + + 和 HLSL 開發 DirectX 應用程式，以充分利用圖形硬體。</span><span class="sxs-lookup"><span data-stu-id="b26c3-105">If you know DirectX, you can develop a DirectX app using native C++ and HLSL to take full advantage of graphics hardware.</span></span>

<span data-ttu-id="b26c3-106">使用這個基本教學課程來開始進行 DirectX 應用程式開發，然後使用藍圖繼續探索 DirectX。</span><span class="sxs-lookup"><span data-stu-id="b26c3-106">Use this basic tutorial to get started with DirectX app development, then use the roadmap to continue exploring DirectX.</span></span>

## <a name="windows-desktop-app-with-c-and-directx"></a><span data-ttu-id="b26c3-107">使用 c + + 和 DirectX 的 Windows 傳統型應用程式</span><span class="sxs-lookup"><span data-stu-id="b26c3-107">Windows desktop app with C++ and DirectX</span></span>

<span data-ttu-id="b26c3-108">具有 DirectX 的 Windows 傳統型應用程式是使用原生 c + + 和 DirectX Api 開發的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b26c3-108">A Windows desktop app with DirectX is an app developed using native C++ and DirectX APIs.</span></span> <span data-ttu-id="b26c3-109">此模型比以 managed framework 撰寫的應用程式更複雜，但可提供更大的彈性，並更有效地存取系統資源，尤其是圖形裝置。</span><span class="sxs-lookup"><span data-stu-id="b26c3-109">This model is more complex than an app written in a managed framework, but it provides greater flexibility and greater access to system resources especially graphics devices.</span></span> <span data-ttu-id="b26c3-110">因此，這對有經驗的開發人員而言是很好的模型。</span><span class="sxs-lookup"><span data-stu-id="b26c3-110">So, it is a good model for the experienced developer.</span></span>

## <a name="why-develop-a-windows-app-with-directx"></a><span data-ttu-id="b26c3-111">為什麼要使用 DirectX 來開發 Windows 應用程式？</span><span class="sxs-lookup"><span data-stu-id="b26c3-111">Why develop a Windows app with DirectX?</span></span>

<span data-ttu-id="b26c3-112">答案很簡單：您想要製作圖形或多媒體密集的遊戲，並且可以使用許多圖形裝置支援的功能。</span><span class="sxs-lookup"><span data-stu-id="b26c3-112">The answer is simple: you want to make a game that is graphics- or multimedia-intensive, and can use the features that many graphics devices support.</span></span> <span data-ttu-id="b26c3-113">如果您不熟悉遊戲開發或 Windows 開發和 C/c + +，就不容易這麼做，但是有一些好消息： DirectX 11 是 Microsoft DirectX 最簡單且最一致的版本。</span><span class="sxs-lookup"><span data-stu-id="b26c3-113">This won't be easy if you are new to game development or to Windows development and C/C++, but there's some good news: DirectX 11 is the simplest and most cohesive version of Microsoft DirectX yet.</span></span> <span data-ttu-id="b26c3-114">它也是功能強大且功能豐富的功能。</span><span class="sxs-lookup"><span data-stu-id="b26c3-114">It's also the most powerful and feature-rich.</span></span> <span data-ttu-id="b26c3-115">如果您的目標是要開發遊戲開發，並學習最先進的轉譯技巧，那麼 DirectX 就能為您提供機會。</span><span class="sxs-lookup"><span data-stu-id="b26c3-115">If your goal is to master game development and learn the most advanced rendering techniques, then DirectX can provide the opportunity for you to do that.</span></span>

<span data-ttu-id="b26c3-116">話雖如此，您必須規劃遊戲 (或互動式的即時應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="b26c3-116">That said, planning your game (or interactive, real-time app) is essential.</span></span> <span data-ttu-id="b26c3-117">如果您不熟悉遊戲開發，而您的遊戲沒有要求圖形需求，請考慮改用 .NET framework 進行開發。</span><span class="sxs-lookup"><span data-stu-id="b26c3-117">If you are new to game development, and your game doesn't have demanding graphics requirements, consider developing it with the .NET framework instead.</span></span> <span data-ttu-id="b26c3-118">此外，許多「中介軟體」圖形和遊戲開發套件適用于 Windows 平臺，而有些則不需要大量的程式設計技能。</span><span class="sxs-lookup"><span data-stu-id="b26c3-118">Also, many "middleware" graphics and game development packages are available for Windows platforms, and some do not require significant programming skills.</span></span>

<span data-ttu-id="b26c3-119">如果您有信心，或只想要使用高精確度圖形 (或具有複雜圖形內容) 的應用程式，請繼續閱讀！</span><span class="sxs-lookup"><span data-stu-id="b26c3-119">If you are confident, or simply have a dream of making a game with high-fidelity graphics (or an app with complex graphics content), then read on!</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b26c3-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="b26c3-120">In this section</span></span>



| <span data-ttu-id="b26c3-121">主題</span><span class="sxs-lookup"><span data-stu-id="b26c3-121">Topic</span></span>                                                                                                                     | <span data-ttu-id="b26c3-122">描述</span><span class="sxs-lookup"><span data-stu-id="b26c3-122">Description</span></span>                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b26c3-123">使用 DirectX 進行開發的必要條件</span><span class="sxs-lookup"><span data-stu-id="b26c3-123">Prerequisites for developing with DirectX</span></span>](pre-requisites-for-developing-a-tailored-c---with-directx-app.md)<br/> | <span data-ttu-id="b26c3-124">當您開始使用 DirectX 開發 Windows 應用程式時，請記住此頁面上的必要條件。</span><span class="sxs-lookup"><span data-stu-id="b26c3-124">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="b26c3-125">這包括您在深入探索之前需要知道的技術。</span><span class="sxs-lookup"><span data-stu-id="b26c3-125">This includes the technologies you need to know before you dive in.</span></span><br/>                            |
| [<span data-ttu-id="b26c3-126">開始使用適用于 Windows 的 DirectX</span><span class="sxs-lookup"><span data-stu-id="b26c3-126">Get started with DirectX for Windows</span></span>](getting-started-with-a-directx-game.md)<br/>                                | <span data-ttu-id="b26c3-127">建立適用于 Windows 的 DirectX 遊戲是新開發人員的挑戰。</span><span class="sxs-lookup"><span data-stu-id="b26c3-127">Creating a DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="b26c3-128">在這裡，我們將快速審視相關的概念，以及使用 DirectX 和 c + + 開始開發遊戲時必須採取的步驟。</span><span class="sxs-lookup"><span data-stu-id="b26c3-128">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span><br/> |
| [<span data-ttu-id="b26c3-129">桌面 DirectX 應用程式的藍圖</span><span class="sxs-lookup"><span data-stu-id="b26c3-129">Roadmap for Desktop DirectX apps</span></span>](roadmap-for-metro-style-apps-using-directx.md)<br/>                             | <span data-ttu-id="b26c3-130">以下是可協助您開始使用 DirectX 和 c + + 開發需要大量圖形的桌面應用程式（例如遊戲）的重要資源。</span><span class="sxs-lookup"><span data-stu-id="b26c3-130">Here are key resources to help you get started with using DirectX and C++ to develop graphics-intensive Desktop apps, like games.</span></span> <br/>                                                                 |



 

 

 





