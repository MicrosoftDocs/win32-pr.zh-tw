---
title: OpenGL 簡介
description: OpenGL 簡介
ms.assetid: 8fe214a9-f071-470b-ac72-182a7bd54fbd
keywords:
- OpenGL，簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cece636e51348288e587116bf13f95696b93ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932081"
---
# <a name="introduction-to-opengl"></a><span data-ttu-id="7a283-104">OpenGL 簡介</span><span class="sxs-lookup"><span data-stu-id="7a283-104">Introduction to OpenGL</span></span>

<span data-ttu-id="7a283-105">OpenGL 的主要目的是將兩個和三維的物件轉譯成畫面格緩衝區，作為圖形硬體的軟體介面。</span><span class="sxs-lookup"><span data-stu-id="7a283-105">As a software interface for graphics hardware, the main purpose of OpenGL is to render two- and three-dimensional objects into a framebuffer.</span></span> <span data-ttu-id="7a283-106">這些物件會描述為頂點 (的序列，以定義) 影像的幾何物件) 或圖元 (。</span><span class="sxs-lookup"><span data-stu-id="7a283-106">These objects are described as sequences of vertices (that define geometric objects) or pixels (that define images).</span></span> <span data-ttu-id="7a283-107">OpenGL 會對此資料執行數個處理常式，將其轉換成圖元以形成畫面格緩衝區中最後所需的影像。</span><span class="sxs-lookup"><span data-stu-id="7a283-107">OpenGL performs several processes on this data to convert it to pixels to form the final desired image in the framebuffer.</span></span>

<span data-ttu-id="7a283-108">下列主題提供 OpenGL 運作方式的全球觀點：</span><span class="sxs-lookup"><span data-stu-id="7a283-108">The following topics present a global view of how OpenGL works:</span></span>

-   <span data-ttu-id="7a283-109">基本[和命令](primitives-and-commands.md)討論點、線段和多邊形作為繪圖的基本單位;以及命令的處理。</span><span class="sxs-lookup"><span data-stu-id="7a283-109">[Primitives and Commands](primitives-and-commands.md) discusses points, line segments, and polygons as the basic units of drawing; and the processing of commands.</span></span>
-   <span data-ttu-id="7a283-110">[Opengl 圖形控制項](opengl-graphic-control.md) 描述 opengl 控制項和它未控制哪些圖形作業。</span><span class="sxs-lookup"><span data-stu-id="7a283-110">[OpenGL Graphic Control](opengl-graphic-control.md) describes which graphic operations OpenGL controls and which it does not control.</span></span>
-   <span data-ttu-id="7a283-111">[執行模型](execution-model.md) 會討論用來解讀 OpenGL 命令的用戶端/伺服器模型。</span><span class="sxs-lookup"><span data-stu-id="7a283-111">[Execution Model](execution-model.md) discusses the client/server model for interpreting OpenGL commands.</span></span>
-   <span data-ttu-id="7a283-112">[基本 opengl](basic-opengl-operation.md) 作業提供有關 OpenGL 如何處理資料以在畫面格緩衝區中產生對應影像的高階描述。</span><span class="sxs-lookup"><span data-stu-id="7a283-112">[Basic OpenGL Operation](basic-opengl-operation.md) gives a high-level description of how OpenGL processes data to produce a corresponding image in the framebuffer.</span></span>
-   <span data-ttu-id="7a283-113">[Opengl 函數名稱](opengl-function-names.md) 會描述 opengl 中使用的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="7a283-113">[OpenGL Function Names](opengl-function-names.md) describes the naming conventions used in OpenGL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a283-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a283-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a283-115">OpenGL 處理管線</span><span class="sxs-lookup"><span data-stu-id="7a283-115">OpenGL Processing Pipeline</span></span>](opengl-processing-pipeline.md)
</dt> <dt>

[<span data-ttu-id="7a283-116">使用評估工具</span><span class="sxs-lookup"><span data-stu-id="7a283-116">Using Evaluators</span></span>](using-evaluators.md)
</dt> <dt>

[<span data-ttu-id="7a283-117">執行選取專案和意見反應</span><span class="sxs-lookup"><span data-stu-id="7a283-117">Performing Selection and Feedback</span></span>](performing-selection-and-feedback.md)
</dt> <dt>

[<span data-ttu-id="7a283-118">使用顯示清單</span><span class="sxs-lookup"><span data-stu-id="7a283-118">Using Display Lists</span></span>](using-display-lists.md)
</dt> <dt>

[<span data-ttu-id="7a283-119">管理模式和執行</span><span class="sxs-lookup"><span data-stu-id="7a283-119">Managing Modes and Execution</span></span>](managing-modes-and-execution.md)
</dt> <dt>

[<span data-ttu-id="7a283-120">取得狀態資訊</span><span class="sxs-lookup"><span data-stu-id="7a283-120">Obtaining State Information</span></span>](obtaining-state-information.md)
</dt> <dt>

[<span data-ttu-id="7a283-121">OpenGL 公用程式庫</span><span class="sxs-lookup"><span data-stu-id="7a283-121">OpenGL Utility Library</span></span>](opengl-utility-library.md)
</dt> </dl>

 

 




