---
title: 元件
description: 單元
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- Windows 上的 OpenGL、元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969059"
---
# <a name="components"></a><span data-ttu-id="45e07-104">單元</span><span class="sxs-lookup"><span data-stu-id="45e07-104">Components</span></span>

<span data-ttu-id="45e07-105">Microsoft 在 Windows 中執行 OpenGL 的功能包括下列元件：</span><span class="sxs-lookup"><span data-stu-id="45e07-105">Microsoft's implementation of OpenGL in Windows includes the following components:</span></span>

-   <span data-ttu-id="45e07-106">目前的 OpenGL 命令的完整集合</span><span class="sxs-lookup"><span data-stu-id="45e07-106">The full set of current OpenGL commands</span></span>

    <span data-ttu-id="45e07-107">OpenGL 包含3D 圖形作業的核心功能程式庫。</span><span class="sxs-lookup"><span data-stu-id="45e07-107">OpenGL contains a library of core functions for 3-D graphics operations.</span></span> <span data-ttu-id="45e07-108">這些基本函式是用來管理物件圖形描述、矩陣轉換、光源、著色、材質、剪切、點陣圖、霧化和消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="45e07-108">These basic functions are used to manage object shape description, matrix transformation, lighting, coloring, texture, clipping, bitmaps, fog, and antialiasing.</span></span> <span data-ttu-id="45e07-109">這些核心函數的名稱具有 "gl" 前置詞。</span><span class="sxs-lookup"><span data-stu-id="45e07-109">The names for these core functions have a "gl" prefix.</span></span>

    <span data-ttu-id="45e07-110">許多 OpenGL 命令都有數種變化，其參數的數目和類型不同。</span><span class="sxs-lookup"><span data-stu-id="45e07-110">Many of the OpenGL commands have several variants, which differ in the number and type of their parameters.</span></span> <span data-ttu-id="45e07-111">計算所有的變異數，有300個以上的 OpenGL 命令。</span><span class="sxs-lookup"><span data-stu-id="45e07-111">Counting all the variants, there are more than 300 OpenGL commands.</span></span>

-   <span data-ttu-id="45e07-112">OpenGL 公用程式 (X.GLU 隊) 程式庫</span><span class="sxs-lookup"><span data-stu-id="45e07-112">The OpenGL Utility (GLU) library</span></span>

    <span data-ttu-id="45e07-113">這是輔助函式的程式庫，能補充核心 OpenGL 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="45e07-113">This library of auxiliary functions complements the core OpenGL functions.</span></span> <span data-ttu-id="45e07-114">這些命令會管理材質支援、座標轉換、多邊形鑲嵌、呈現球體、圓柱和磁片、NURBS (非統一的有理 B 曲線) 曲線和表面，以及錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="45e07-114">The commands manage texture support, coordinate transformation, polygon tessellation, rendering spheres, cylinders and disks, NURBS (Non-Uniform Rational B-Spline) curves and surfaces, and error handling.</span></span>

-   <span data-ttu-id="45e07-115">OpenGL 程式設計指南輔助程式庫</span><span class="sxs-lookup"><span data-stu-id="45e07-115">The OpenGL Programming Guide Auxiliary library</span></span>

    <span data-ttu-id="45e07-116">這是與平臺無關的簡易函式程式庫，可用於管理 windows、處理輸入事件、繪製傳統立體物件、管理背景進程，以及執行程式。</span><span class="sxs-lookup"><span data-stu-id="45e07-116">This is a simple, platform-independent library of functions for managing windows, handling input events, drawing classic 3-D objects, managing a background process, and running a program.</span></span> <span data-ttu-id="45e07-117">視窗管理和輸入常式提供基本層級的功能，可讓您快速開始在 OpenGL 中進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="45e07-117">The window management and input routines provide a base level of functionality with which you can quickly get started programming in OpenGL.</span></span>

    <span data-ttu-id="45e07-118">不過，請勿在生產應用程式中使用它們。</span><span class="sxs-lookup"><span data-stu-id="45e07-118">Do not use them, however, in a production application.</span></span> <span data-ttu-id="45e07-119">以下是此警告的一些原因：</span><span class="sxs-lookup"><span data-stu-id="45e07-119">Here are some reasons for this warning:</span></span>

    -   <span data-ttu-id="45e07-120">訊息迴圈是在程式庫程式碼中。</span><span class="sxs-lookup"><span data-stu-id="45e07-120">The message loop is in the library code.</span></span>
    -   <span data-ttu-id="45e07-121">沒有任何方法可新增其他 WM 訊息的處理常式 \* 。</span><span class="sxs-lookup"><span data-stu-id="45e07-121">There is no way to add handlers for additional WM\* messages.</span></span>
    -   <span data-ttu-id="45e07-122">邏輯調色板的支援很少。</span><span class="sxs-lookup"><span data-stu-id="45e07-122">There is very little support for logical palettes.</span></span>

    <span data-ttu-id="45e07-123">此程式庫會在 *OpenGL 程式設計指南* 中說明和使用。</span><span class="sxs-lookup"><span data-stu-id="45e07-123">The library is described and used in the *OpenGL Programming Guide*.</span></span>

-   <span data-ttu-id="45e07-124">WGL 函式</span><span class="sxs-lookup"><span data-stu-id="45e07-124">The WGL functions</span></span>

    <span data-ttu-id="45e07-125">這組函式會將 OpenGL 連接至 Windows 視窗化系統。</span><span class="sxs-lookup"><span data-stu-id="45e07-125">This set of functions connects OpenGL to the Windows windowing system.</span></span> <span data-ttu-id="45e07-126">這些函式會管理轉譯內容、顯示清單、擴充功能和字型點陣圖。</span><span class="sxs-lookup"><span data-stu-id="45e07-126">The functions manage rendering contexts, display lists, extension functions, and font bitmaps.</span></span> <span data-ttu-id="45e07-127">WGL 函式類似于將 OpenGL 連接至 X 視窗系統的 GLX 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="45e07-127">The WGL functions are analogous to the GLX extensions that connect OpenGL to the X Window System.</span></span> <span data-ttu-id="45e07-128">這些函數的名稱具有 "wgl" 前置詞。</span><span class="sxs-lookup"><span data-stu-id="45e07-128">The names for these functions have a "wgl" prefix.</span></span>

-   <span data-ttu-id="45e07-129">適用于像素格式和雙重緩衝的新 Windows 函數</span><span class="sxs-lookup"><span data-stu-id="45e07-129">New Windows functions for pixel formats and double buffering</span></span>

    <span data-ttu-id="45e07-130">這些函式支援每個視窗的像素格式和雙重緩衝 (，以) windows 的平滑影像變更。</span><span class="sxs-lookup"><span data-stu-id="45e07-130">These functions support per-window pixel formats and double buffering (for smooth image changes) of windows.</span></span> <span data-ttu-id="45e07-131">這些新功能只適用于 OpenGL 圖形視窗。</span><span class="sxs-lookup"><span data-stu-id="45e07-131">These new functions apply only to OpenGL graphics windows.</span></span>

 

 




