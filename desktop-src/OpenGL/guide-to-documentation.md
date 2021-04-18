---
title: 檔指南
description: 在 Windows 中為 OpenGL 設定的檔包含五個元素。
ms.assetid: 1672e9a3-10f0-4ae4-a6a3-b482a3bdda10
keywords:
- Windows 上的 OpenGL，檔
- OpenGL 參考手冊
- OpenGL 程式設計指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc27d11b8d829efebf0914dbb1d67c872cf0196d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968414"
---
# <a name="guide-to-documentation"></a><span data-ttu-id="2f1b6-106">檔指南</span><span class="sxs-lookup"><span data-stu-id="2f1b6-106">Guide To Documentation</span></span>

<span data-ttu-id="2f1b6-107">在 Windows 中為 OpenGL 設定的檔包含五個元素。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-107">The documentation set for OpenGL in Windows includes five elements.</span></span>

-   <span data-ttu-id="2f1b6-108">*Opengl 參考手冊* 包含了 opengl 的運作方式，以及一組詳細的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-108">The *OpenGL Reference Manual* includes an overview of how OpenGL works and a set of detailed reference pages.</span></span> <span data-ttu-id="2f1b6-109">參考頁面涵蓋所有115相異的 OpenGL 函式，以及 OpenGL 公用程式中的43函式 (X.GLU 隊) 程式庫。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-109">The reference pages cover all the 115 distinct OpenGL functions, as well as the 43 functions in the OpenGL Utility (GLU) library.</span></span>

-   <span data-ttu-id="2f1b6-110">*Opengl 程式設計指南* 說明如何使用 OpenGL 建立圖形程式。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-110">The *OpenGL Programming Guide* explains how to create graphics programs using OpenGL.</span></span> <span data-ttu-id="2f1b6-111">其中包含下列主要主題的討論：</span><span class="sxs-lookup"><span data-stu-id="2f1b6-111">It includes discussions of the following major topics:</span></span>

    -   <span data-ttu-id="2f1b6-112">繪製幾何形狀</span><span class="sxs-lookup"><span data-stu-id="2f1b6-112">Drawing geometric shapes</span></span>
    -   <span data-ttu-id="2f1b6-113">圖元、點陣圖、字型和影像</span><span class="sxs-lookup"><span data-stu-id="2f1b6-113">Pixels, bitmaps, fonts, and images</span></span>
    -   <span data-ttu-id="2f1b6-114">視圖和矩陣轉換</span><span class="sxs-lookup"><span data-stu-id="2f1b6-114">Viewing and matrix transformations</span></span>
    -   <span data-ttu-id="2f1b6-115">材質對應</span><span class="sxs-lookup"><span data-stu-id="2f1b6-115">Texture mapping</span></span>
    -   <span data-ttu-id="2f1b6-116">顯示清單</span><span class="sxs-lookup"><span data-stu-id="2f1b6-116">Display lists</span></span>
    -   <span data-ttu-id="2f1b6-117">Advanced 複合技術</span><span class="sxs-lookup"><span data-stu-id="2f1b6-117">Advanced composite techniques</span></span>
    -   <span data-ttu-id="2f1b6-118">Color</span><span class="sxs-lookup"><span data-stu-id="2f1b6-118">Color</span></span>
    -   <span data-ttu-id="2f1b6-119">評估工具和 NURBS</span><span class="sxs-lookup"><span data-stu-id="2f1b6-119">Evaluators and NURBS</span></span>
    -   <span data-ttu-id="2f1b6-120">光源</span><span class="sxs-lookup"><span data-stu-id="2f1b6-120">Lighting</span></span>
    -   <span data-ttu-id="2f1b6-121">選取專案和意見反應</span><span class="sxs-lookup"><span data-stu-id="2f1b6-121">Selection and feedback</span></span>
    -   <span data-ttu-id="2f1b6-122">混合、消除鋸齒和霧化</span><span class="sxs-lookup"><span data-stu-id="2f1b6-122">Blending, antialiasing, and fog</span></span>
    -   <span data-ttu-id="2f1b6-123">先進的技術</span><span class="sxs-lookup"><span data-stu-id="2f1b6-123">Advanced techniques</span></span>

    <span data-ttu-id="2f1b6-124">此外，Opengl 程式 *設計指南* 包含的附錄可討論 Opengl 公用程式程式庫和 Opengl 程式設計手冊輔助程式庫。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-124">In addition, the *OpenGL Programming Guide* contains appendixes that discuss the OpenGL Utility library and the OpenGL Programming Guide Auxiliary library.</span></span>

-   <span data-ttu-id="2f1b6-125">第三個檔元素是此總覽。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-125">The third documentation element is this overview.</span></span> <span data-ttu-id="2f1b6-126">它描述 OpenGL 的 Windows 執行，並提供其元件的總覽。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-126">It describes the Windows implementation of OpenGL and provides an overview of its components.</span></span> <span data-ttu-id="2f1b6-127">它會討論轉譯內容、像素格式和緩衝區的概念;將 OpenGL 連接至 Windows 視窗系統的 WGL 函式;以及支援每個視窗像素格式的 Windows 函式，以及適用于 OpenGL 圖形視窗的視窗的雙重緩衝。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-127">It discusses the concepts of rendering contexts, pixel formats, and buffers; the WGL functions that connect OpenGL to the Windows windowing systems; and the Windows functions that support per-window pixel formats and double buffering of windows for OpenGL graphics windows.</span></span> <span data-ttu-id="2f1b6-128">WGL 函式和函式是適用于 OpenGL 的 Windows 實作為專屬的。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-128">The WGL functions and the functions are specific to the Windows implementation of OpenGL.</span></span>

-   <span data-ttu-id="2f1b6-129">第四個檔元素是 WGL 函式的參考頁面集合、剛才提及的 Windows 函式，以及 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 資料結構。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-129">The fourth documentation element is the set of reference pages for the WGL functions, the Windows functions just mentioned, and the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure.</span></span>

-   <span data-ttu-id="2f1b6-130">第五個檔元素是移植指南。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-130">The fifth documentation element is the porting guide.</span></span> <span data-ttu-id="2f1b6-131">它會討論如何將現有的 OpenGL 程式碼從其他環境移至 Windows。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-131">It discusses moving existing OpenGL code from other environments to Windows.</span></span>

<span data-ttu-id="2f1b6-132">前兩個元素是官方的 OpenGL 書籍;它們不包含在 Microsoft Windows SDK 中。</span><span class="sxs-lookup"><span data-stu-id="2f1b6-132">The first two elements are the official OpenGL books; they are not included in the Microsoft Windows SDK.</span></span>

 

 




