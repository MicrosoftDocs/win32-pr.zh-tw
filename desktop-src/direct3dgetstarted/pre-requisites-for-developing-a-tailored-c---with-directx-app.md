---
title: 使用 DirectX 進行開發的必要條件
description: 當您開始使用 DirectX 開發 Windows 應用程式時，請記住此頁面上的必要條件。 這包括您在深入探索之前需要知道的技術。
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- DirectX 應用程式，必要條件
- DirectX 應用程式，Windows Store 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/16/2020
ms.locfileid: "104463976"
---
# <a name="prerequisites-for-developing-with-directx"></a><span data-ttu-id="3f083-106">使用 DirectX 進行開發的必要條件</span><span class="sxs-lookup"><span data-stu-id="3f083-106">Prerequisites for developing with DirectX</span></span>

<span data-ttu-id="3f083-107">當您開始使用 DirectX 開發 Windows 應用程式時，請記住此頁面上的必要條件。</span><span class="sxs-lookup"><span data-stu-id="3f083-107">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="3f083-108">這包括您在深入探索之前需要知道的技術。</span><span class="sxs-lookup"><span data-stu-id="3f083-108">This includes the technologies you need to know before you dive in.</span></span>

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a><span data-ttu-id="3f083-109">使用 DirectX 開發 Windows 遊戲應該知道什麼？</span><span class="sxs-lookup"><span data-stu-id="3f083-109">What should I know to develop a Windows game using DirectX?</span></span>

<span data-ttu-id="3f083-110">在使用 DirectX 開始開發 Windows Store 應用程式之前，您必須知道如何在 Windows 中使用 c + + 進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="3f083-110">Before you start to develop a Windows Store app using DirectX, you need to know how to program in Windows with C++.</span></span> <span data-ttu-id="3f083-111">使用 DirectX 的 Windows 應用程式是以較低層級的程式設計來開發，這表示您會暴露在作業系統的許多功能上。</span><span class="sxs-lookup"><span data-stu-id="3f083-111">Windows apps using DirectX are developed at a low level of programming, which means that you will be exposed to many features of the operating system.</span></span> <span data-ttu-id="3f083-112">這些包括記憶體和資源管理，以及圖形裝置本身的介面。</span><span class="sxs-lookup"><span data-stu-id="3f083-112">These include memory and resource management, and the interface for the graphics device itself.</span></span> <span data-ttu-id="3f083-113">如果您是遊戲或圖形應用程式開發的新手，您可能會發現這是一項挑戰。</span><span class="sxs-lookup"><span data-stu-id="3f083-113">If you are new to game or graphics app development, you may find this challenging.</span></span> <span data-ttu-id="3f083-114">但是您也會發現它可獲得獎勵，因為在此層級的學習遊戲開發，可為遊戲和圖形應用程式的設計與開發帶來更多的可能性。</span><span class="sxs-lookup"><span data-stu-id="3f083-114">But you will also find it rewarding, because learning game development at this level creates far, far greater possibilities for game and graphics app design and development.</span></span>

<span data-ttu-id="3f083-115">您也必須瞭解2D 和3D 圖形程式設計和數學的基本概念，因為您將使用的許多 Api 都是以這些原則為考慮而開發。</span><span class="sxs-lookup"><span data-stu-id="3f083-115">You'll also need to understand the basics of 2D and 3D graphics programming and mathematics, because many of the APIs you'll use were developed with these principles in mind.</span></span> <span data-ttu-id="3f083-116">如果您熟悉其參數和結果，您就可以更輕鬆地瞭解它們的參數和結果。</span><span class="sxs-lookup"><span data-stu-id="3f083-116">It'll be easier for you to understand their parameters and results if you are familiar with the operations behind them.</span></span>

<span data-ttu-id="3f083-117">您至少應該要理解下列各項：</span><span class="sxs-lookup"><span data-stu-id="3f083-117">At a minimum, you should have a grasp of the following:</span></span>

-   <span data-ttu-id="3f083-118">Windows C/c + + 程式設計。</span><span class="sxs-lookup"><span data-stu-id="3f083-118">Windows C/C++ programming.</span></span> <span data-ttu-id="3f083-119">這表示您瞭解指標和參考、事件和回呼，也可能是一些常見的程式庫（例如 ATL）。</span><span class="sxs-lookup"><span data-stu-id="3f083-119">This means that you understand pointers and references, events and callbacks, and perhaps a few of the common libraries like ATL.</span></span>
-   <span data-ttu-id="3f083-120">Win32 程式設計。</span><span class="sxs-lookup"><span data-stu-id="3f083-120">Win32 programming.</span></span> <span data-ttu-id="3f083-121">您瞭解 windows 的建立方式，以及如何處理使用者介面事件。</span><span class="sxs-lookup"><span data-stu-id="3f083-121">You understand how windows are created, and how user interface events are processed.</span></span> <span data-ttu-id="3f083-122">您也會瞭解 COM 和基本 Win32 Api 的一些相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3f083-122">You also understand a little bit about COM and essential Win32 APIs.</span></span>
-   <span data-ttu-id="3f083-123">線性代數和三角函數。</span><span class="sxs-lookup"><span data-stu-id="3f083-123">Linear algebra and trigonometry.</span></span> <span data-ttu-id="3f083-124">雖然不是必要的，但如果您熟悉這兩個數學專業領域的概念，就會有更多的時間，因為它們是許多3D 圖形程式設計的基礎。</span><span class="sxs-lookup"><span data-stu-id="3f083-124">While not essential, you'll have an easier time if you are familiar with concepts from these two math disciplines, because they are the foundation of much of 3D graphics programming.</span></span>
-   <span data-ttu-id="3f083-125">基本圖形術語和概念，例如點陣圖、材質、頂點、網格和等區。</span><span class="sxs-lookup"><span data-stu-id="3f083-125">Basic graphics terminology and concepts, such as bitmaps, textures, vertices, meshes, and viewports.</span></span>

## <a name="what-does-directx-provide-me"></a><span data-ttu-id="3f083-126">DirectX 提供的功能為何？</span><span class="sxs-lookup"><span data-stu-id="3f083-126">What does DirectX provide me?</span></span>

<span data-ttu-id="3f083-127">DirectX 是您將用來開發 Windows 遊戲的一組主要圖形 Api。</span><span class="sxs-lookup"><span data-stu-id="3f083-127">DirectX is the primary set of graphics APIs you'll use to develop Windows games.</span></span> <span data-ttu-id="3f083-128">以下是當您決定如何開發遊戲時，必須熟悉的功能類別。</span><span class="sxs-lookup"><span data-stu-id="3f083-128">Here are the categories of features that you must become familiar with when you decide how to develop your game.</span></span>



| <span data-ttu-id="3f083-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="3f083-129">Library</span></span>     | <span data-ttu-id="3f083-130">描述</span><span class="sxs-lookup"><span data-stu-id="3f083-130">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f083-131">Direct3D</span><span class="sxs-lookup"><span data-stu-id="3f083-131">Direct3D</span></span>    | <span data-ttu-id="3f083-132">一組強大、以效能為導向、硬體加速的程式庫，用於呈現3D 圖形。</span><span class="sxs-lookup"><span data-stu-id="3f083-132">A powerful, performance-oriented, hardware-accelerated set of libraries for rendering 3D graphics.</span></span>                                              |
| <span data-ttu-id="3f083-133">Direct2D</span><span class="sxs-lookup"><span data-stu-id="3f083-133">Direct2D</span></span>    | <span data-ttu-id="3f083-134">適用于硬體加速點陣圖和向量2D 繪圖的一組2D 圖形程式庫。</span><span class="sxs-lookup"><span data-stu-id="3f083-134">A set of 2D graphics libraries for hardware-accelerated bitmap and vector 2D drawing.</span></span>                                                           |
| <span data-ttu-id="3f083-135">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="3f083-135">DirectXMath</span></span> | <span data-ttu-id="3f083-136">2D 和3D 圖形中所使用之常見、優化數學運算的程式庫，例如向量和矩陣作業。</span><span class="sxs-lookup"><span data-stu-id="3f083-136">A library of common, optimized math operations used in 2D and 3D graphics, such as vector and matrix operations.</span></span>                                |
| <span data-ttu-id="3f083-137">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="3f083-137">DirectWrite</span></span> | <span data-ttu-id="3f083-138">2D 文字轉譯和版面配置 Api 的程式庫。</span><span class="sxs-lookup"><span data-stu-id="3f083-138">A library of 2D text rendering and layout APIs.</span></span> <span data-ttu-id="3f083-139">它支援硬體加速和軟體點陣化。</span><span class="sxs-lookup"><span data-stu-id="3f083-139">It supports both hardware acceleration and software rasterization.</span></span>                              |
| <span data-ttu-id="3f083-140">XAudio2</span><span class="sxs-lookup"><span data-stu-id="3f083-140">XAudio2</span></span>     | <span data-ttu-id="3f083-141">適用于 Microsoft Windows 的低層級跨平臺音訊 API，可為遊戲開發提供信號處理和音訊混合基礎。</span><span class="sxs-lookup"><span data-stu-id="3f083-141">A low-level, cross-platform audio API for Microsoft Windows that provides a signal processing and audio mixing foundation for game development.</span></span> |
| <span data-ttu-id="3f083-142">XInput</span><span class="sxs-lookup"><span data-stu-id="3f083-142">XInput</span></span>      | <span data-ttu-id="3f083-143">支援各種傳統遊戲控制項的程式庫，並強調 Xbox 360 控制器模型。</span><span class="sxs-lookup"><span data-stu-id="3f083-143">A library that supports various traditional gaming controls, with an emphasis on the Xbox 360 controller model.</span></span>                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a><span data-ttu-id="3f083-144">使用 DirectX 開發 Windows 遊戲需要哪些工具？</span><span class="sxs-lookup"><span data-stu-id="3f083-144">What tools do I need to develop a Windows game with DirectX?</span></span>

<span data-ttu-id="3f083-145">若要開始進行本教學課程，您需要：</span><span class="sxs-lookup"><span data-stu-id="3f083-145">To get started with this tutorial, you need:</span></span>

-   <span data-ttu-id="3f083-146">Windows 8.1 或更高</span><span class="sxs-lookup"><span data-stu-id="3f083-146">Windows 8.1 or greater</span></span>
-   <span data-ttu-id="3f083-147">Microsoft Visual Studio 2013 或更高版本</span><span class="sxs-lookup"><span data-stu-id="3f083-147">Microsoft Visual Studio 2013 or greater</span></span>

 

 




