---
title: OpenGL 正確性秘訣
description: OpenGL 正確性秘訣
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL、正確性秘訣
- OpenGL、最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5294d2e989591216ea8cf66aa380933718776f2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372052"
---
# <a name="opengl-correctness-tips"></a><span data-ttu-id="df6b7-105">OpenGL 正確性秘訣</span><span class="sxs-lookup"><span data-stu-id="df6b7-105">OpenGL Correctness Tips</span></span>

<span data-ttu-id="df6b7-106">遵循下列指導方針來建立可依您預期執行的 OpenGL 應用程式：</span><span class="sxs-lookup"><span data-stu-id="df6b7-106">Follow these guidelines to create OpenGL applications that perform as you intend:</span></span>

-   <span data-ttu-id="df6b7-107">假設 OpenGL 實作為未來版本中的錯誤行為可能會變更。</span><span class="sxs-lookup"><span data-stu-id="df6b7-107">Assume error behavior on the part of an OpenGL implementation may change in a future release of OpenGL.</span></span> <span data-ttu-id="df6b7-108">OpenGL 錯誤語義在未來的修訂版本中可能會變更。</span><span class="sxs-lookup"><span data-stu-id="df6b7-108">OpenGL error semantics may change in future revisions.</span></span>
-   <span data-ttu-id="df6b7-109">使用投影矩陣將所有幾何折迭為單一平面。</span><span class="sxs-lookup"><span data-stu-id="df6b7-109">Use the projection matrix to collapse all geometry to a single plane.</span></span> <span data-ttu-id="df6b7-110">如果使用模型矩陣，則以眼睛座標運作的 OpenGL 功能 (例如光源和應用程式定義的裁剪平面) 可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="df6b7-110">If the modelview matrix is used, OpenGL features that operate in eye coordinates (such as lighting and application-defined clipping planes) might fail.</span></span>
-   <span data-ttu-id="df6b7-111">請勿對單一矩陣進行大量變更。</span><span class="sxs-lookup"><span data-stu-id="df6b7-111">Do not make extensive changes to a single matrix.</span></span> <span data-ttu-id="df6b7-112">例如，請勿以增量角度持續呼叫 [**glRotate**](glrotate.md) ，以建立旋轉的動畫。</span><span class="sxs-lookup"><span data-stu-id="df6b7-112">For example, do not animate a rotation by continually calling [**glRotate**](glrotate.md) with an incremental angle.</span></span> <span data-ttu-id="df6b7-113">相反地，請使用 [**glLoadIdentity**](glloadidentity.md) 為每個框架初始化指定的矩陣，然後使用該框架所需的完整角度來呼叫 **glRotate** 。</span><span class="sxs-lookup"><span data-stu-id="df6b7-113">Rather, use [**glLoadIdentity**](glloadidentity.md) to initialize the given matrix for each frame, and then call **glRotate** with the desired complete angle for that frame.</span></span>
-   <span data-ttu-id="df6b7-114">只有在針對符合規範的 OpenGL 執行所建立的 invariance 規則保證此行為時，才會通過轉譯資料庫的多個傳遞來產生相同的圖元片段。</span><span class="sxs-lookup"><span data-stu-id="df6b7-114">Expect multiple passes through a rendering database to generate the same pixel fragments only if this behavior is guaranteed by the invariance rules established for a compliant OpenGL implementation.</span></span> <span data-ttu-id="df6b7-115">否則，多個階段可能會產生不同的片段集。</span><span class="sxs-lookup"><span data-stu-id="df6b7-115">Otherwise, multiple passes might generate varying sets of fragments.</span></span>
-   <span data-ttu-id="df6b7-116">在定義顯示清單時，不預期會回報錯誤。</span><span class="sxs-lookup"><span data-stu-id="df6b7-116">Do not expect errors to be reported while a display list is being defined.</span></span> <span data-ttu-id="df6b7-117">只有在執行清單時，顯示清單中的命令才會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="df6b7-117">The commands within a display list generate errors only when the list is executed.</span></span>
-   <span data-ttu-id="df6b7-118">若要優化深度緩衝區的作業，請盡可能將接近的錐錐平面放在最接近的觀點。</span><span class="sxs-lookup"><span data-stu-id="df6b7-118">To optimize the operation of the depth buffer, place the near frustum plane as far from the viewpoint as possible.</span></span>
-   <span data-ttu-id="df6b7-119">呼叫 [**glFlush**](glflush.md) 來強制執行所有先前的 OpenGL 命令。</span><span class="sxs-lookup"><span data-stu-id="df6b7-119">Call [**glFlush**](glflush.md) to force execution of all previous OpenGL commands.</span></span> <span data-ttu-id="df6b7-120">請勿在 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 或 [**glIsEnabled**](glisenabled.md) 上計算，以排清轉譯資料流程。</span><span class="sxs-lookup"><span data-stu-id="df6b7-120">Do not count on [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) or [**glIsEnabled**](glisenabled.md) to flush the rendering stream.</span></span> <span data-ttu-id="df6b7-121">查詢命令會排清傳回有效資料所需的資料流程數量，但不一定會完成所有暫止的轉譯命令。</span><span class="sxs-lookup"><span data-stu-id="df6b7-121">Query commands flush as much of the stream as is required to return valid data but don't necessarily complete all pending rendering commands.</span></span>
-   <span data-ttu-id="df6b7-122">在轉譯 predithered 影像時關閉遞色 (例如， [**glCopyPixels**](glcopypixels.md) 被呼叫時) 。</span><span class="sxs-lookup"><span data-stu-id="df6b7-122">Turn off dithering when rendering predithered images (for example, when [**glCopyPixels**](glcopypixels.md) is called).</span></span>
-   <span data-ttu-id="df6b7-123">利用累積緩衝區的完整範圍。</span><span class="sxs-lookup"><span data-stu-id="df6b7-123">Make use of the full range of the accumulation buffer.</span></span> <span data-ttu-id="df6b7-124">例如，如果累積四個映射，則會在每一季累積時進行調整。</span><span class="sxs-lookup"><span data-stu-id="df6b7-124">For example, if accumulating four images, scale each by one-quarter as it is accumulated.</span></span>
-   <span data-ttu-id="df6b7-125">若要取得精確的二維柵格化，請仔細地指定要進行柵格化之基本專案的正向投射和頂點。</span><span class="sxs-lookup"><span data-stu-id="df6b7-125">To obtain exact two-dimensional rasterization, carefully specify both the orthographic projection and the vertices of the primitives that are to be rasterized.</span></span> <span data-ttu-id="df6b7-126">使用整數座標指定正射投射，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="df6b7-126">Specify the orthographic projection with integer coordinates, as shown in the following example.</span></span>

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    <span data-ttu-id="df6b7-127">參數的 *寬度* 和 *高度* 是區的維度。</span><span class="sxs-lookup"><span data-stu-id="df6b7-127">The parameters *width* and *height* are the dimensions of the viewport.</span></span> <span data-ttu-id="df6b7-128">在指定此投射矩陣的情況下，將多邊形頂點和圖元影像位置放在整數座標，以可預測的方式表示。</span><span class="sxs-lookup"><span data-stu-id="df6b7-128">Given this projection matrix, place polygon vertices and pixel image positions at integer coordinates to rasterize predictably.</span></span> <span data-ttu-id="df6b7-129">例如， [glRecti](glrect-functions.md) ( 0，0，1，1 ) 可靠地填滿了此區的左下圖元，而 [glRasterPos2i](glrasterpos-functions.md) ( 0、0 ) 可靠地將 unzoomed 影像放置在此區的左下圖元。</span><span class="sxs-lookup"><span data-stu-id="df6b7-129">For example, [glRecti](glrect-functions.md)( 0, 0, 1, 1 ) reliably fills the lower-left pixel of the viewport, and [glRasterPos2i](glrasterpos-functions.md)( 0, 0 ) reliably positions an unzoomed image at the lower-left pixel of the viewport.</span></span> <span data-ttu-id="df6b7-130">不過，點頂點、線條頂點和點陣圖位置應該放在半整數位置。</span><span class="sxs-lookup"><span data-stu-id="df6b7-130">However, point vertices, line vertices, and bitmap positions should be placed at half-integer locations.</span></span> <span data-ttu-id="df6b7-131">例如，從 (*x* (1) ，0.5) 到 (*x* (2) ) ，0.5 (將會在圖格中的最底部資料列中可靠地轉譯，而以) 0.5，0.5 ( 繪製的點會可靠地填滿與 glRecti ) 0，0，1，1相同的圖元。</span><span class="sxs-lookup"><span data-stu-id="df6b7-131">For example, a line drawn from (*x* (1) , 0.5) to (*x* (2) , 0.5) will be reliably rendered along the bottom row of pixels in the viewport, and a point drawn at (0.5, 0.5) will reliably fill the same pixel as glRecti( 0, 0, 1, 1 ).</span></span>

    <span data-ttu-id="df6b7-132">一種最佳的危害，可讓您在整數位置指定所有基本型別，同時仍然確保可預測的點陣化，也就是將 *x* 和 *y* 轉譯為0.375，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="df6b7-132">An optimum compromise that allows all primitives to be specified at integer positions, while still ensuring predictable rasterization, is to translate *x* and *y* by 0.375, as shown in the following code sample.</span></span> <span data-ttu-id="df6b7-133">這類轉譯會將多邊形和圖元影像邊緣安全地遠離圖元的中心，同時將線條頂點移至接近圖元中心。</span><span class="sxs-lookup"><span data-stu-id="df6b7-133">Such a translation keeps polygon and pixel image edges safely away from the centers of pixels, while moving line vertices close enough to the pixel centers.</span></span>

    ``` syntax
    glViewport(0, 0, width, height);
    glMatrixMode(GL_PROJECTION);
    glLoadIdentity( );
    gluOrtho2D(0, width, 0, height);
    glMatrixMode(GL_MODELVIEW);
    glLoadIdentity( );
    glTranslatef(0.375, 0.375, 0.0);
    /* render all primitives at integer positions */
    ```

-   <span data-ttu-id="df6b7-134">避免使用負 *w* 頂點座標和負 *q* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="df6b7-134">Avoid using negative *w* vertex coordinates and negative *q* texture coordinates.</span></span> <span data-ttu-id="df6b7-135">OpenGL 可能無法正確地裁剪這類座標，而且可能會在這類座標所定義的網底基本專案時產生插補錯誤。</span><span class="sxs-lookup"><span data-stu-id="df6b7-135">OpenGL might not clip such coordinates correctly and can make interpolation errors when shading primitives defined by such coordinates.</span></span>

 

 




