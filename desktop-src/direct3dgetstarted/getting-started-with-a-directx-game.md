---
title: 開始使用適用于 Windows 的 DirectX
description: 建立適用于 Windows 的 Microsoft DirectX 遊戲是新開發人員的挑戰。 在這裡，我們將快速審視相關的概念，以及使用 DirectX 和 c + + 開始開發遊戲時必須採取的步驟。
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967905"
---
# <a name="get-started-with-directx-for-windows"></a><span data-ttu-id="22946-104">開始使用適用于 Windows 的 DirectX</span><span class="sxs-lookup"><span data-stu-id="22946-104">Get started with DirectX for Windows</span></span>

<span data-ttu-id="22946-105">建立適用于 Windows 的 Microsoft DirectX 遊戲是新開發人員的挑戰。</span><span class="sxs-lookup"><span data-stu-id="22946-105">Creating a Microsoft DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="22946-106">在這裡，我們將快速審視相關的概念，以及使用 DirectX 和 c + + 開始開發遊戲時必須採取的步驟。</span><span class="sxs-lookup"><span data-stu-id="22946-106">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span>

<span data-ttu-id="22946-107">讓我們開始這次的教學。</span><span class="sxs-lookup"><span data-stu-id="22946-107">Let's get started.</span></span>

## <a name="what-skills-do-you-need"></a><span data-ttu-id="22946-108">您需要哪些技能？</span><span class="sxs-lookup"><span data-stu-id="22946-108">What skills do you need?</span></span>

<span data-ttu-id="22946-109">若要開發適用于 Windows 的 DirectX 遊戲，您必須具備一些基本技巧。</span><span class="sxs-lookup"><span data-stu-id="22946-109">To develop a game in DirectX for Windows, you must have a few basic skills.</span></span> <span data-ttu-id="22946-110">具體來說，您必須能夠：</span><span class="sxs-lookup"><span data-stu-id="22946-110">Specifically, you must be able to:</span></span>

-   <span data-ttu-id="22946-111">讀寫新式 c + + 程式碼 (c + + 11 提供最) 的功能，並熟悉基本的 c + + 設計原則，以及範本和 factory 模型等模式。</span><span class="sxs-lookup"><span data-stu-id="22946-111">Read and write modern C++ code (C++11 helps the most), and be familiar with basic C++ design principles and patterns like templates and the factory model.</span></span> <span data-ttu-id="22946-112">您也必須熟悉通用的 c + + 程式庫，例如標準樣板程式庫，並特別說明轉換運算子、指標類型和標準樣板程式庫資料結構 (例如 std：： vector) 。</span><span class="sxs-lookup"><span data-stu-id="22946-112">You must also be familiar with common C++ libraries like the Standard Template Library, and specifically with the casting operators, pointer types, and the standard template library data structures (such as std::vector).</span></span>
-   <span data-ttu-id="22946-113">瞭解基本幾何、三角函數和線性代數。</span><span class="sxs-lookup"><span data-stu-id="22946-113">Understand basic geometry, trigonometry, and linear algebra.</span></span> <span data-ttu-id="22946-114">您在範例中發現的大部分程式碼都假設您瞭解這些形式的數學和其常見規則。</span><span class="sxs-lookup"><span data-stu-id="22946-114">Much of the code you will find in the examples assumes you understand these forms of mathematics and their common rules.</span></span>
-   <span data-ttu-id="22946-115">熟悉 COM —特別是 [**Microsoft：： WRL：： ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart 指標) 。</span><span class="sxs-lookup"><span data-stu-id="22946-115">Have familiarity with COM—especially [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart pointer).</span></span>
-   <span data-ttu-id="22946-116">瞭解圖形和圖形技術的基礎，特別是3D 圖形。</span><span class="sxs-lookup"><span data-stu-id="22946-116">Understand the foundations of graphics and graphics technology, particularly 3D graphics.</span></span> <span data-ttu-id="22946-117">雖然 DirectX 本身有自己的術語，但它仍是根據一般3D 圖形原則的完善概念來建立。</span><span class="sxs-lookup"><span data-stu-id="22946-117">While DirectX itself has its own terminology, it still builds upon a well-established understanding of general 3D graphics principles.</span></span>
-   <span data-ttu-id="22946-118">瞭解訊息迴圈的概念，因為您將會執行接聽 Windows 作業系統的迴圈。</span><span class="sxs-lookup"><span data-stu-id="22946-118">Understand the concept of a message loop, because you'll be implementing a loop that listens to the Windows operating system.</span></span>

## <a name="and-were-off"></a><span data-ttu-id="22946-119">而我們已經關閉了！</span><span class="sxs-lookup"><span data-stu-id="22946-119">And we're off!</span></span>

<span data-ttu-id="22946-120">準備好開始了嗎？</span><span class="sxs-lookup"><span data-stu-id="22946-120">Ready to start?</span></span> <span data-ttu-id="22946-121">開始之前，讓我們先複習一下。</span><span class="sxs-lookup"><span data-stu-id="22946-121">Let's review before we head on.</span></span> <span data-ttu-id="22946-122">您已經：</span><span class="sxs-lookup"><span data-stu-id="22946-122">You have:</span></span>

-   <span data-ttu-id="22946-123">Windows 8.1 的已更新且可運作的安裝。</span><span class="sxs-lookup"><span data-stu-id="22946-123">An updated and working installation of Windows 8.1.</span></span>
-   <span data-ttu-id="22946-124">[Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs)的安裝。</span><span class="sxs-lookup"><span data-stu-id="22946-124">An installation of [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span></span>
-   <span data-ttu-id="22946-125">我位勇敢精神以及想要深入瞭解 DirectX 遊戲開發！</span><span class="sxs-lookup"><span data-stu-id="22946-125">An intrepid spirit and a desire to learn more about DirectX game development!</span></span>

## <a name="next-steps"></a><span data-ttu-id="22946-126">下一步</span><span class="sxs-lookup"><span data-stu-id="22946-126">Next steps</span></span>



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22946-127">使用 DirectX 裝置資源</span><span class="sxs-lookup"><span data-stu-id="22946-127">Work with DirectX device resources</span></span>](work-with-dxgi.md)                                           | <span data-ttu-id="22946-128">瞭解如何使用 DXGI 來建立虛擬化圖形裝置，以及建立和設定交換鏈。</span><span class="sxs-lookup"><span data-stu-id="22946-128">Learn how to use DXGI to create a virtualized graphics device, and create and configure a swap chain.</span></span>     |
| [<span data-ttu-id="22946-129">瞭解 Direct3D 11 轉譯管線</span><span class="sxs-lookup"><span data-stu-id="22946-129">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md) | <span data-ttu-id="22946-130">瞭解如何連結至 DirectX 裝置資源類別，並使用 Direct3D 圖形管線進行繪製。</span><span class="sxs-lookup"><span data-stu-id="22946-130">Learn how to hook into the DirectX device resources class, and draw using the Direct3D graphics pipeline.</span></span> |
| [<span data-ttu-id="22946-131">使用著色器和著色器資源</span><span class="sxs-lookup"><span data-stu-id="22946-131">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)               | <span data-ttu-id="22946-132">瞭解如何撰寫適用于 Direct3D 圖形管線階段的 HLSL 著色器程式。</span><span class="sxs-lookup"><span data-stu-id="22946-132">Learn how to write HLSL shader programs for Direct3D graphics pipeline stages.</span></span>                            |



 

 

 