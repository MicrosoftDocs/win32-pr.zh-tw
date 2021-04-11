---
title: 'glBegin 函式 (Gl) '
description: 'GlBegin 和 glend 函式會分隔基本或類似基本類型群組的頂點。 |glBegin 函式 (Gl) '
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- glBegin 函式 OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945920"
---
# <a name="glbegin-function"></a><span data-ttu-id="0f474-105">glBegin 函式</span><span class="sxs-lookup"><span data-stu-id="0f474-105">glBegin function</span></span>

<span data-ttu-id="0f474-106">**GlBegin** 和 [**glend**](glend.md)函式會分隔基本或類似基本類型群組的頂點。</span><span class="sxs-lookup"><span data-stu-id="0f474-106">The **glBegin** and [**glend**](glend.md) functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f474-107">語法</span><span class="sxs-lookup"><span data-stu-id="0f474-107">Syntax</span></span>


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="0f474-108">參數</span><span class="sxs-lookup"><span data-stu-id="0f474-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f474-109">*mode*</span><span class="sxs-lookup"><span data-stu-id="0f474-109">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="0f474-110">將從 **glBegin** 和後續 [**glend**](glend.md)之間顯示的頂點建立的基本或基本。</span><span class="sxs-lookup"><span data-stu-id="0f474-110">The primitive or primitives that will be created from vertices presented between **glBegin** and the subsequent [**glend**](glend.md).</span></span> <span data-ttu-id="0f474-111">以下是接受的符號常數及其意義：</span><span class="sxs-lookup"><span data-stu-id="0f474-111">The following are accepted symbolic constants and their meanings:</span></span>



| <span data-ttu-id="0f474-112">值</span><span class="sxs-lookup"><span data-stu-id="0f474-112">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="0f474-113">意義</span><span class="sxs-lookup"><span data-stu-id="0f474-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <span data-ttu-id="0f474-114"><dt>**GL \_ 點**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-114"><dt>**GL\_POINTS**</dt></span></span> </dl>                          | <span data-ttu-id="0f474-115">將每個頂點視為單一點。</span><span class="sxs-lookup"><span data-stu-id="0f474-115">Treats each vertex as a single point.</span></span> <span data-ttu-id="0f474-116">頂點 *n* 定義點 *n*。</span><span class="sxs-lookup"><span data-stu-id="0f474-116">Vertex *n* defines point *n*.</span></span> <span data-ttu-id="0f474-117">會繪製 *N* 個點。</span><span class="sxs-lookup"><span data-stu-id="0f474-117">*N* points are drawn.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <span data-ttu-id="0f474-118"><dt>**GL \_ 行**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-118"><dt>**GL\_LINES**</dt></span></span> </dl>                             | <span data-ttu-id="0f474-119">將每一對頂點視為獨立的線段。</span><span class="sxs-lookup"><span data-stu-id="0f474-119">Treats each pair of vertices as an independent line segment.</span></span> <span data-ttu-id="0f474-120">頂點 *2n-1* 和 *2n* 定義第 *n* 行。</span><span class="sxs-lookup"><span data-stu-id="0f474-120">Vertices *2n - 1* and *2n* define line *n*.</span></span> <span data-ttu-id="0f474-121">會繪製 *N/2* 行。</span><span class="sxs-lookup"><span data-stu-id="0f474-121">*N/2* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <span data-ttu-id="0f474-122"><dt>**GL \_ 行 \_ 帶**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-122"><dt>**GL\_LINE\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="0f474-123">從第一個頂點到最後一個頂點，繪製一組連接的線段。</span><span class="sxs-lookup"><span data-stu-id="0f474-123">Draws a connected group of line segments from the first vertex to the last.</span></span> <span data-ttu-id="0f474-124">頂點 *n* 和 *n + 1* 定義行 *n*。</span><span class="sxs-lookup"><span data-stu-id="0f474-124">Vertices *n* and *n+1* define line *n*.</span></span> <span data-ttu-id="0f474-125">會繪製 *n-1* 行。</span><span class="sxs-lookup"><span data-stu-id="0f474-125">*N - 1* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <span data-ttu-id="0f474-126"><dt>**GL \_ 線路 \_ 迴圈**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-126"><dt>**GL\_LINE\_LOOP**</dt></span></span> </dl>                | <span data-ttu-id="0f474-127">繪製從第一個頂點到最後一個頂點的已連接線段群組，然後回到第一個頂點。</span><span class="sxs-lookup"><span data-stu-id="0f474-127">Draws a connected group of line segments from the first vertex to the last, then back to the first.</span></span> <span data-ttu-id="0f474-128">頂點 *n* 和 *n + 1* 定義行 *n*。</span><span class="sxs-lookup"><span data-stu-id="0f474-128">Vertices *n* and *n + 1* define line *n*.</span></span> <span data-ttu-id="0f474-129">但是，最後一行是由頂點 *N* 和 *1* 所定義。</span><span class="sxs-lookup"><span data-stu-id="0f474-129">The last line, however, is defined by vertices *N* and *1*.</span></span> <span data-ttu-id="0f474-130">會繪製 *N* 行。</span><span class="sxs-lookup"><span data-stu-id="0f474-130">*N* lines are drawn.</span></span><br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <span data-ttu-id="0f474-131"><dt>**GL \_ 三角形**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-131"><dt>**GL\_TRIANGLES**</dt></span></span> </dl>                 | <span data-ttu-id="0f474-132">將每個三個頂點視為獨立的三角形。</span><span class="sxs-lookup"><span data-stu-id="0f474-132">Treats each triplet of vertices as an independent triangle.</span></span> <span data-ttu-id="0f474-133">頂點 *3n-2*、 *3n-1* 和 *3n* 定義三角形 *n*。</span><span class="sxs-lookup"><span data-stu-id="0f474-133">Vertices *3n - 2*, *3n - 1*, and *3n* define triangle *n*.</span></span> <span data-ttu-id="0f474-134">會繪製 *N/3* 個三角形。</span><span class="sxs-lookup"><span data-stu-id="0f474-134">*N/3* triangles are drawn.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <span data-ttu-id="0f474-135"><dt>**GL \_ 三角形 \_ 條紋**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-135"><dt>**GL\_TRIANGLE\_STRIP**</dt></span></span> </dl> | <span data-ttu-id="0f474-136">繪製一組已連接的三角形。</span><span class="sxs-lookup"><span data-stu-id="0f474-136">Draws a connected group of triangles.</span></span> <span data-ttu-id="0f474-137">針對前兩個頂點之後所呈現的每個頂點，各定義一個三角形。</span><span class="sxs-lookup"><span data-stu-id="0f474-137">One triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="0f474-138">若是奇數 *n*、頂點 *n*、 *n + 1* 和 *n + 2* ，請定義三角形 *n*。</span><span class="sxs-lookup"><span data-stu-id="0f474-138">For odd *n*, vertices *n*, *n + 1*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="0f474-139">針對偶數 *，* 頂點 *n + 1*、 *n* 和 *n + 2* 定義三角形 *n*。</span><span class="sxs-lookup"><span data-stu-id="0f474-139">For even *n*, vertices *n + 1*, *n*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="0f474-140">會繪製 *N-2* 個三角形。</span><span class="sxs-lookup"><span data-stu-id="0f474-140">*N - 2* triangles are drawn.</span></span><br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <span data-ttu-id="0f474-141"><dt>**GL \_ 三角形 \_ 風扇**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-141"><dt>**GL\_TRIANGLE\_FAN**</dt></span></span> </dl>       | <span data-ttu-id="0f474-142">繪製一組已連接的三角形。</span><span class="sxs-lookup"><span data-stu-id="0f474-142">Draws a connected group of triangles.</span></span> <span data-ttu-id="0f474-143">針對前兩個頂點之後所呈現的每個頂點，各定義一個三角形。</span><span class="sxs-lookup"><span data-stu-id="0f474-143">one triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="0f474-144">頂點 *1*、 *n + 1*、 *n + 2* 定義三角形 *n*。</span><span class="sxs-lookup"><span data-stu-id="0f474-144">Vertices *1*, *n + 1*, *n + 2* define triangle *n*.</span></span> <span data-ttu-id="0f474-145">會繪製 *N-2* 個三角形。</span><span class="sxs-lookup"><span data-stu-id="0f474-145">*N - 2* triangles are drawn.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <span data-ttu-id="0f474-146"><dt>**GL \_ 四邊形**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-146"><dt>**GL\_QUADS**</dt></span></span> </dl>                             | <span data-ttu-id="0f474-147">將四個頂點的每個群組視為獨立四邊形。</span><span class="sxs-lookup"><span data-stu-id="0f474-147">Treats each group of four vertices as an independent quadrilateral.</span></span> <span data-ttu-id="0f474-148">頂點 *4n-3*、 *4n-2*、 *4n-1* 和 *4n* 定義四邊形 *n*。</span><span class="sxs-lookup"><span data-stu-id="0f474-148">Vertices *4n - 3*, *4n - 2*, *4n - 1*, and *4n* define quadrilateral *n*.</span></span> <span data-ttu-id="0f474-149">會繪製 *N/4* quadrilaterals。</span><span class="sxs-lookup"><span data-stu-id="0f474-149">*N/4* quadrilaterals are drawn.</span></span><br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <span data-ttu-id="0f474-150"><dt>**GL \_ 四 \_ 條**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-150"><dt>**GL\_QUAD\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="0f474-151">繪製連接的 quadrilaterals 群組。</span><span class="sxs-lookup"><span data-stu-id="0f474-151">Draws a connected group of quadrilaterals.</span></span> <span data-ttu-id="0f474-152">針對第一組之後所顯示的每一對頂點，定義一個四邊形。</span><span class="sxs-lookup"><span data-stu-id="0f474-152">One quadrilateral is defined for each pair of vertices presented after the first pair.</span></span> <span data-ttu-id="0f474-153">頂點 *2n-1*、 *2n*、 *2n + 2* 和 *2n + 1* 定義四邊形 *n*。</span><span class="sxs-lookup"><span data-stu-id="0f474-153">Vertices *2n - 1*, *2n*, *2n + 2*, and *2n + 1* define quadrilateral *n*.</span></span> <span data-ttu-id="0f474-154">會繪製 *N/2-1* 個 quadrilaterals。</span><span class="sxs-lookup"><span data-stu-id="0f474-154">*N/2 - 1* quadrilaterals are drawn.</span></span> <span data-ttu-id="0f474-155">請注意，用來從資料四邊形中建立頂點的順序，與獨立資料所使用的順序不同。</span><span class="sxs-lookup"><span data-stu-id="0f474-155">Note that the order in which vertices are used to construct a quadrilateral from strip data is different from that used with independent data.</span></span><br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <span data-ttu-id="0f474-156"><dt>**GL \_ 多邊形**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-156"><dt>**GL\_POLYGON**</dt></span></span> </dl>                       | <span data-ttu-id="0f474-157">繪製單一的凸邊。</span><span class="sxs-lookup"><span data-stu-id="0f474-157">Draws a single, convex polygon.</span></span> <span data-ttu-id="0f474-158">頂點 *1* 到 *N* 定義了這個多邊形。</span><span class="sxs-lookup"><span data-stu-id="0f474-158">Vertices *1* through *N* define this polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f474-159">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f474-159">Return value</span></span>

<span data-ttu-id="0f474-160">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0f474-160">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0f474-161">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0f474-161">Error codes</span></span>

<span data-ttu-id="0f474-162">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0f474-162">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0f474-163">Name</span><span class="sxs-lookup"><span data-stu-id="0f474-163">Name</span></span>                                                                                                  | <span data-ttu-id="0f474-164">意義</span><span class="sxs-lookup"><span data-stu-id="0f474-164">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f474-165"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-165"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="0f474-166">*模式* 已設定為不接受的值。</span><span class="sxs-lookup"><span data-stu-id="0f474-166">*mode* was set to an unaccepted value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="0f474-167"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-167"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0f474-168">[GlVertex](glvertex-functions.md)、 [glColor](glcolor-functions.md)、 [glIndex](glindex-functions.md)、 [glNormal](glnormal-functions.md)、 [glTexCoord](gltexcoord-functions.md)、 [glEvalCoord](glevalcoord-functions.md)、 [glEvalPoint](glevalpoint.md)、 [glMaterial](glmaterial-functions.md)、 [glEdgeFlag](gledgeflag-functions.md)、 [**glCallList**](glcalllist.md)或 [**glCallLists**](glcalllists.md)以外的函式會在 **glBegin** 與對應的 [**glend**](glend.md)之間呼叫。</span><span class="sxs-lookup"><span data-stu-id="0f474-168">A function other than [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md), or [**glCallLists**](glcalllists.md) was called between **glBegin** and the corresponding [**glend**](glend.md).</span></span> <span data-ttu-id="0f474-169">函數 **glend** 是在呼叫對應的 **glBegin** 之前呼叫，或在 **glBegin** / **glend** 序列內呼叫 glBegin。</span><span class="sxs-lookup"><span data-stu-id="0f474-169">The function **glend** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glend** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="0f474-170">備註</span><span class="sxs-lookup"><span data-stu-id="0f474-170">Remarks</span></span>

<span data-ttu-id="0f474-171">**GlBegin** 和 [**glend**](glend.md)函式會分隔定義基本或類似基本類型群組的頂點。</span><span class="sxs-lookup"><span data-stu-id="0f474-171">The **glBegin** and [**glend**](glend.md) functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="0f474-172">**GlBegin** 函式會接受單一引數，以指定頂點所組成的10個基本類型。</span><span class="sxs-lookup"><span data-stu-id="0f474-172">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="0f474-173">從1開始，將 *n* 做為整數計數，而 *n* 則是指定的頂點總數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0f474-173">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="0f474-174">您只能在 **glBegin** 與 [**Glend**](glend.md)之間使用 OpenGL 函數的子集。</span><span class="sxs-lookup"><span data-stu-id="0f474-174">You can use only a subset of OpenGL functions between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="0f474-175">您可以使用的函數如下：</span><span class="sxs-lookup"><span data-stu-id="0f474-175">The functions you can use are:</span></span>

    [<span data-ttu-id="0f474-176">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="0f474-176">**glVertex**</span></span>](glvertex-functions.md)

     

    [<span data-ttu-id="0f474-177">**glColor**</span><span class="sxs-lookup"><span data-stu-id="0f474-177">**glColor**</span></span>](glcolor-functions.md)

     

    [<span data-ttu-id="0f474-178">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="0f474-178">**glIndex**</span></span>](glindex-functions.md)

     

    [<span data-ttu-id="0f474-179">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="0f474-179">**glNormal**</span></span>](glnormal-functions.md)

     

    [<span data-ttu-id="0f474-180">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="0f474-180">**glTexCoord**</span></span>](gltexcoord-functions.md)

     

    [<span data-ttu-id="0f474-181">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="0f474-181">**glEvalCoord**</span></span>](glevalcoord-functions.md)

     

    [<span data-ttu-id="0f474-182">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="0f474-182">**glEvalPoint**</span></span>](glevalpoint.md)

     

    [<span data-ttu-id="0f474-183">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="0f474-183">**glMaterial**</span></span>](glmaterial-functions.md)

     

    [<span data-ttu-id="0f474-184">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="0f474-184">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="0f474-185">您也可以使用 [**glCallList**](glcalllist.md) 或 [**glCallLists**](glcalllists.md) 來執行只包含上述函式的顯示清單。</span><span class="sxs-lookup"><span data-stu-id="0f474-185">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="0f474-186">如果在 **glBegin** 和 [**glend**](glend.md)之間呼叫任何其他 OpenGL 函數，則會設定錯誤旗標，並忽略函式。</span><span class="sxs-lookup"><span data-stu-id="0f474-186">If any other OpenGL function is called between **glBegin** and [**glend**](glend.md), the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="0f474-187">無論在 **glBegin** 中為 *模式* 選擇的值為何，您可以在 **glBegin** 和 [**glend**](glend.md)之間定義的頂點數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="0f474-187">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="0f474-188">未完整指定的線條、三角形、quadrilaterals 和多邊形都不會繪製。</span><span class="sxs-lookup"><span data-stu-id="0f474-188">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="0f474-189">當提供的頂點太少以指定單一基本或指定了不正確的頂點倍數時，不完整的規格結果。</span><span class="sxs-lookup"><span data-stu-id="0f474-189">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="0f474-190">忽略不完整的基本類型;繪製完整的基本專案。</span><span class="sxs-lookup"><span data-stu-id="0f474-190">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="0f474-191">每個基本類型頂點的最小規格為：</span><span class="sxs-lookup"><span data-stu-id="0f474-191">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="0f474-192">頂點的最小數目</span><span class="sxs-lookup"><span data-stu-id="0f474-192">Minimum number of vertices</span></span> | <span data-ttu-id="0f474-193">基本類型</span><span class="sxs-lookup"><span data-stu-id="0f474-193">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="0f474-194">1</span><span class="sxs-lookup"><span data-stu-id="0f474-194">1</span></span>                          | <span data-ttu-id="0f474-195">點</span><span class="sxs-lookup"><span data-stu-id="0f474-195">point</span></span>             |
    | <span data-ttu-id="0f474-196">2</span><span class="sxs-lookup"><span data-stu-id="0f474-196">2</span></span>                          | <span data-ttu-id="0f474-197">line</span><span class="sxs-lookup"><span data-stu-id="0f474-197">line</span></span>              |
    | <span data-ttu-id="0f474-198">3</span><span class="sxs-lookup"><span data-stu-id="0f474-198">3</span></span>                          | <span data-ttu-id="0f474-199">三角形</span><span class="sxs-lookup"><span data-stu-id="0f474-199">triangle</span></span>          |
    | <span data-ttu-id="0f474-200">4</span><span class="sxs-lookup"><span data-stu-id="0f474-200">4</span></span>                          | <span data-ttu-id="0f474-201">四邊形</span><span class="sxs-lookup"><span data-stu-id="0f474-201">quadrilateral</span></span>     |
    | <span data-ttu-id="0f474-202">3</span><span class="sxs-lookup"><span data-stu-id="0f474-202">3</span></span>                          | <span data-ttu-id="0f474-203">多邊形</span><span class="sxs-lookup"><span data-stu-id="0f474-203">polygon</span></span>           |

    

     

-   <span data-ttu-id="0f474-204">需要特定多個頂點的模式為 GL \_ 行 (2) 、gl \_ 三角形 (3) 、gl \_ 四邊形 (4) 和 GL 四 \_ \_ 個 () 。</span><span class="sxs-lookup"><span data-stu-id="0f474-204">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f474-205">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f474-205">Requirements</span></span>



| <span data-ttu-id="0f474-206">需求</span><span class="sxs-lookup"><span data-stu-id="0f474-206">Requirement</span></span> | <span data-ttu-id="0f474-207">值</span><span class="sxs-lookup"><span data-stu-id="0f474-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f474-208">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f474-208">Minimum supported client</span></span><br/> | <span data-ttu-id="0f474-209">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f474-209">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0f474-210">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f474-210">Minimum supported server</span></span><br/> | <span data-ttu-id="0f474-211">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f474-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0f474-212">標頭</span><span class="sxs-lookup"><span data-stu-id="0f474-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f474-213"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-213"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0f474-214">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f474-214">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f474-215"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-215"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0f474-216">DLL</span><span class="sxs-lookup"><span data-stu-id="0f474-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f474-217"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f474-217"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f474-218">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f474-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f474-219">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="0f474-219">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="0f474-220">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="0f474-220">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="0f474-221">**glColor**</span><span class="sxs-lookup"><span data-stu-id="0f474-221">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="0f474-222">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="0f474-222">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="0f474-223">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0f474-223">**glEnd**</span></span>](/windows/desktop/OpenGL/glend)
</dt> <dt>

[<span data-ttu-id="0f474-224">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="0f474-224">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="0f474-225">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="0f474-225">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="0f474-226">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="0f474-226">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="0f474-227">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="0f474-227">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="0f474-228">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="0f474-228">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="0f474-229">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="0f474-229">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="0f474-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="0f474-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

