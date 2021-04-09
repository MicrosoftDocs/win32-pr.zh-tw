---
title: OpenGL 效能秘訣
description: OpenGL 效能秘訣
ms.assetid: f85bf725-1361-49b9-894c-c803b2dead60
keywords:
- OpenGL，效能秘訣
- OpenGL、最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e5b6fa33f8d6841d0fd47d1a655ef99facc84e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673263"
---
# <a name="opengl-performance-tips"></a><span data-ttu-id="0c88e-105">OpenGL 效能秘訣</span><span class="sxs-lookup"><span data-stu-id="0c88e-105">OpenGL Performance Tips</span></span>

<span data-ttu-id="0c88e-106">這些程式設計實務會優化應用程式的效能：</span><span class="sxs-lookup"><span data-stu-id="0c88e-106">These programming practices optimize your application's performance:</span></span>

-   <span data-ttu-id="0c88e-107">當只有單一材質屬性在每個頂點上 (快速地變動時，請使用 [**glColorMaterial**](glcolormaterial.md) ，例如) 。</span><span class="sxs-lookup"><span data-stu-id="0c88e-107">Use [**glColorMaterial**](glcolormaterial.md) when only a single material property is being varied rapidly (at each vertex, for example).</span></span> <span data-ttu-id="0c88e-108">使用 [**glMaterial**](glmaterial-functions.md) 進行不頻繁的變更，或當超過單一材質屬性時，快速地變動。</span><span class="sxs-lookup"><span data-stu-id="0c88e-108">Use [**glMaterial**](glmaterial-functions.md) for infrequent changes, or when more than a single material property is being varied rapidly.</span></span>
-   <span data-ttu-id="0c88e-109">使用 [**glLoadIdentity**](glloadidentity.md) 初始化矩陣，而不是載入您自己的身分識別矩陣複本。</span><span class="sxs-lookup"><span data-stu-id="0c88e-109">Use [**glLoadIdentity**](glloadidentity.md) to initialize a matrix, rather than loading your own copy of the identity matrix.</span></span>
-   <span data-ttu-id="0c88e-110">使用特定的矩陣呼叫（例如 [**glRotate**](glrotate.md)、 [**glTranslate**](gltranslate.md)和 [**glScale**](glscale.md)），而不是撰寫您自己的旋轉、轉譯和調整矩陣，以及呼叫 [**glMultMatrix**](glmultmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="0c88e-110">Use specific matrix calls such as [**glRotate**](glrotate.md), [**glTranslate**](gltranslate.md), and [**glScale**](glscale.md), rather than composing your own rotation, translation, and scale matrices and calling [**glMultMatrix**](glmultmatrix.md).</span></span>
-   <span data-ttu-id="0c88e-111">使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 來儲存和還原狀態值。</span><span class="sxs-lookup"><span data-stu-id="0c88e-111">Use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to save and restore state values.</span></span> <span data-ttu-id="0c88e-112">只有當您的應用程式需要其本身計算的狀態值時，才使用查詢函數。</span><span class="sxs-lookup"><span data-stu-id="0c88e-112">Use query functions only when your application requires the state values for its own computations.</span></span>
-   <span data-ttu-id="0c88e-113">使用顯示清單來封裝可能需要大量記憶體的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="0c88e-113">Use display lists to encapsulate potentially memory-intensive state changes.</span></span> <span data-ttu-id="0c88e-114">例如，請將完全指定紋理所需的所有 [**glTexImage**](glteximage1d.md) 呼叫放 (，可能) 也會將相關聯的 [**glTexParameter**](gltexparameter-functions.md)、 [**glPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md) 呼叫放入單一顯示清單中。</span><span class="sxs-lookup"><span data-stu-id="0c88e-114">For example, place all the [**glTexImage**](glteximage1d.md) calls required to completely specify a texture (and perhaps the associated [**glTexParameter**](gltexparameter-functions.md), [**glPixelStore**](glpixelstore-functions.md), and [**glPixelTransfer**](glpixeltransfer.md) calls as well) into a single display list.</span></span> <span data-ttu-id="0c88e-115">呼叫此顯示清單來選取材質。</span><span class="sxs-lookup"><span data-stu-id="0c88e-115">Call this display list to select the texture.</span></span>
-   <span data-ttu-id="0c88e-116">使用顯示清單來封裝將會重複繪製之固定物件的轉譯呼叫。</span><span class="sxs-lookup"><span data-stu-id="0c88e-116">Use display lists to encapsulate the rendering calls of rigid objects that will be drawn repeatedly.</span></span>
-   <span data-ttu-id="0c88e-117">若要將用戶端/伺服器環境中的網路頻寬降到最低，請使用評估工具甚至是簡單的介面鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="0c88e-117">To minimize network bandwidth in client/server environments, use evaluators even for simple surface tessellations.</span></span>
-   <span data-ttu-id="0c88e-118">可能的話，為了避免產生 GL 正規化的額外負荷 \_ ，請提供單位長度的法線。</span><span class="sxs-lookup"><span data-stu-id="0c88e-118">If possible, to avoid the overhead of GL\_NORMALIZE, provide unit-length normals.</span></span> <span data-ttu-id="0c88e-119">因為 [**glScale**](glscale.md) 幾乎一律需要啟用 GL 正規化 \_ ，所以請避免在執行光源時使用 **glScale** 。</span><span class="sxs-lookup"><span data-stu-id="0c88e-119">Because [**glScale**](glscale.md) almost always requires enabling GL\_NORMALIZE, avoid using **glScale** when doing lighting.</span></span>
-   <span data-ttu-id="0c88e-120">如果不需要平滑陰影，請將 [**glShadeModel**](glshademodel.md) 設定為 [一般] \_ 。</span><span class="sxs-lookup"><span data-stu-id="0c88e-120">If smooth shading isn't required, set [**glShadeModel**](glshademodel.md) to GL\_FLAT.</span></span>
-   <span data-ttu-id="0c88e-121">如果可能的話，請針對每個框架使用單一 [**glClear**](glclear.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0c88e-121">Use a single [**glClear**](glclear.md) call per frame, if possible.</span></span> <span data-ttu-id="0c88e-122">請勿使用 **glClear** 來清除緩衝區的小型子領域加寬;您只能使用它來完全或幾乎完全清除緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0c88e-122">Do not use **glClear** to clear small subregions of the buffers; use it only to clear the buffer completely or nearly completely.</span></span>
-   <span data-ttu-id="0c88e-123">若要繪製多個獨立三角形，請使用單一呼叫，而不是多個呼叫來 [**glBegin**](glbegin.md) ( GL \_ 三角形 ) 或 **glBegin** ( GL \_ 多邊形 ) 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0c88e-123">To draw multiple independent triangles, use a single call rather than multiple calls to [**glBegin**](glbegin.md) ( GL\_TRIANGLES ) or a call to **glBegin** ( GL\_POLYGON ).</span></span> <span data-ttu-id="0c88e-124">同樣：</span><span class="sxs-lookup"><span data-stu-id="0c88e-124">Similarly:</span></span>

    <span data-ttu-id="0c88e-125">若要繪製單一三角形，請使用 GL \_ 三角形，而非 gl \_ 多邊形。</span><span class="sxs-lookup"><span data-stu-id="0c88e-125">To draw a single triangle, use GL\_TRIANGLES rather than GL\_POLYGON.</span></span>

    <span data-ttu-id="0c88e-126">使用單一呼叫來 [**glBegin**](glbegin.md) ( GL \_ 四邊形 ) ，而不是重複呼叫 **glBegin** ( gl \_ 多邊形 ) 。</span><span class="sxs-lookup"><span data-stu-id="0c88e-126">Use a single call to [**glBegin**](glbegin.md) ( GL\_QUADS ) rather than calling **glBegin** ( GL\_POLYGON ) repeatedly.</span></span>

    <span data-ttu-id="0c88e-127">使用單一呼叫 [**glBegin**](glbegin.md) ( GL \_ 線 ) 來繪製多個獨立的線段，而不是多次呼叫 **glBegin** ( \_ GL 行 ) 。</span><span class="sxs-lookup"><span data-stu-id="0c88e-127">Use a single call to [**glBegin**](glbegin.md) ( GL\_LINES ) to draw multiple independent line segments, rather than calling **glBegin** ( GL\_LINES ) multiple times.</span></span>

-   <span data-ttu-id="0c88e-128">一般情況下，請使用向量形式的命令來傳遞預先計算資料，並使用純量形式的命令來傳遞計算接近呼叫時間的值。</span><span class="sxs-lookup"><span data-stu-id="0c88e-128">In general, use the vector forms of commands to pass precomputed data, and use the scalar forms of commands to pass values that are computed near call time.</span></span>
-   <span data-ttu-id="0c88e-129">避免進行多餘的模式變更，例如將色彩設定為平面陰影多邊形的每個頂點之間的相同值。</span><span class="sxs-lookup"><span data-stu-id="0c88e-129">Avoid making redundant mode changes, such as setting the color to the same value between each vertex of a flat-shaded polygon.</span></span>
-   <span data-ttu-id="0c88e-130">繪製或複製影像時，請停用柵格化和個別片段作業，以將資源優化。</span><span class="sxs-lookup"><span data-stu-id="0c88e-130">When drawing or copying images, disable rasterization and per-fragment operations, to optimize resources.</span></span> <span data-ttu-id="0c88e-131">OpenGL 可以將材質套用至圖元影像。</span><span class="sxs-lookup"><span data-stu-id="0c88e-131">OpenGL can apply textures to pixel images.</span></span>

 

 




