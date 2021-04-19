---
title: 'glPolygonMode 函式 (Gl) '
description: GlPolygonMode 函式會選取多邊形的點陣化模式。
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- glPolygonMode 函式 OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966545"
---
# <a name="glpolygonmode-function"></a><span data-ttu-id="268bc-104">glPolygonMode 函式</span><span class="sxs-lookup"><span data-stu-id="268bc-104">glPolygonMode function</span></span>

<span data-ttu-id="268bc-105">**GlPolygonMode** 函式會選取多邊形的點陣化模式。</span><span class="sxs-lookup"><span data-stu-id="268bc-105">The **glPolygonMode** function selects a polygon rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="268bc-106">語法</span><span class="sxs-lookup"><span data-stu-id="268bc-106">Syntax</span></span>


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="268bc-107">參數</span><span class="sxs-lookup"><span data-stu-id="268bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="268bc-108">*臉*</span><span class="sxs-lookup"><span data-stu-id="268bc-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="268bc-109">適用于 *模式* 的多邊形。</span><span class="sxs-lookup"><span data-stu-id="268bc-109">The polygons that *mode* applies to.</span></span> <span data-ttu-id="268bc-110">必須是上層 \_ 多邊形的 gl 正面、gl \_ 回背面的多邊形，或 \_ \_ \_ 適用于 FRONT 和 back 多邊形的 gl 正面和背面。</span><span class="sxs-lookup"><span data-stu-id="268bc-110">Must be GL\_FRONT for front-facing polygons, GL\_BACK for back-facing polygons, or GL\_FRONT\_AND\_BACK for front- and back-facing polygons.</span></span>

</dd> <dt>

<span data-ttu-id="268bc-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="268bc-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="268bc-112">多邊形將會被柵格化的方式。</span><span class="sxs-lookup"><span data-stu-id="268bc-112">The way polygons will be rasterized.</span></span> <span data-ttu-id="268bc-113">下列模式已定義，可在 *模式* 中指定。</span><span class="sxs-lookup"><span data-stu-id="268bc-113">The following modes are defined and can be specified in *mode*.</span></span> <span data-ttu-id="268bc-114">預設值為 \_ front 和 back 多邊形的 GL 填滿。</span><span class="sxs-lookup"><span data-stu-id="268bc-114">The default is GL\_FILL for both front- and back-facing polygons.</span></span>



| <span data-ttu-id="268bc-115">值</span><span class="sxs-lookup"><span data-stu-id="268bc-115">Value</span></span>                                                                                                                                          | <span data-ttu-id="268bc-116">意義</span><span class="sxs-lookup"><span data-stu-id="268bc-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <span data-ttu-id="268bc-117"><dt>**GL \_ 點**</dt></span><span class="sxs-lookup"><span data-stu-id="268bc-117"><dt>**GL\_POINT**</dt></span></span> </dl> | <span data-ttu-id="268bc-118">標示為界限邊緣開頭的多邊形頂點會繪製為點。</span><span class="sxs-lookup"><span data-stu-id="268bc-118">Polygon vertices that are marked as the start of a boundary edge are drawn as points.</span></span> <span data-ttu-id="268bc-119">點屬性（例如 GL \_ 點 \_ 大小和 gl \_ 點）會 \_ 將點的點陣化順暢地控制。</span><span class="sxs-lookup"><span data-stu-id="268bc-119">Point attributes such as GL\_POINT\_SIZE and GL\_POINT\_SMOOTH control the rasterization of the points.</span></span> <span data-ttu-id="268bc-120">GL 多邊形模式以外的多邊形點陣化屬性沒有 \_ \_ 任何作用。</span><span class="sxs-lookup"><span data-stu-id="268bc-120">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <span data-ttu-id="268bc-121"><dt>**GL \_ 線**</dt></span><span class="sxs-lookup"><span data-stu-id="268bc-121"><dt>**GL\_LINE**</dt></span></span> </dl>    | <span data-ttu-id="268bc-122">多邊形的邊界邊緣會繪製為直線線段。</span><span class="sxs-lookup"><span data-stu-id="268bc-122">Boundary edges of the polygon are drawn as line segments.</span></span> <span data-ttu-id="268bc-123">它們會被視為行 stippling 的連接線區段;在區段之間不會重設 line stipple 計數器和模式 (請參閱 [**glLineStipple**](gllinestipple.md)) 。</span><span class="sxs-lookup"><span data-stu-id="268bc-123">They are treated as connected line segments for line stippling; the line stipple counter and pattern are not reset between segments (see [**glLineStipple**](gllinestipple.md)).</span></span> <span data-ttu-id="268bc-124">生產線屬性（例如 GL \_ 線條 \_ 寬度和 gl \_ 線）會 \_ 順暢地控制線條的點陣化。</span><span class="sxs-lookup"><span data-stu-id="268bc-124">Line attributes such as GL\_LINE\_WIDTH and GL\_LINE\_SMOOTH control the rasterization of the lines.</span></span> <span data-ttu-id="268bc-125">GL 多邊形模式以外的多邊形點陣化屬性沒有 \_ \_ 任何作用。</span><span class="sxs-lookup"><span data-stu-id="268bc-125">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <span data-ttu-id="268bc-126"><dt>**GL \_ 填滿**</dt></span><span class="sxs-lookup"><span data-stu-id="268bc-126"><dt>**GL\_FILL**</dt></span></span> </dl>    | <span data-ttu-id="268bc-127">多邊形的內部會填滿。</span><span class="sxs-lookup"><span data-stu-id="268bc-127">The interior of the polygon is filled.</span></span> <span data-ttu-id="268bc-128">多邊形屬性（例如 GL \_ 多邊形 \_ STIPPLE 和 gl \_ 多邊形）會 \_ 順暢地控制多邊形的點陣化。</span><span class="sxs-lookup"><span data-stu-id="268bc-128">Polygon attributes such as GL\_POLYGON\_STIPPLE and GL\_POLYGON\_SMOOTH control the rasterization of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="268bc-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="268bc-129">Return value</span></span>

<span data-ttu-id="268bc-130">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="268bc-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="268bc-131">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="268bc-131">Error codes</span></span>

<span data-ttu-id="268bc-132">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="268bc-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="268bc-133">Name</span><span class="sxs-lookup"><span data-stu-id="268bc-133">Name</span></span>                                                                                                  | <span data-ttu-id="268bc-134">意義</span><span class="sxs-lookup"><span data-stu-id="268bc-134">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="268bc-135"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="268bc-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="268bc-136">*臉部* 或 *模式* 都不是接受的值。</span><span class="sxs-lookup"><span data-stu-id="268bc-136">Either *face* or *mode* was not an accepted value.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="268bc-137"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="268bc-137"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="268bc-138">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="268bc-138">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="268bc-139">備註</span><span class="sxs-lookup"><span data-stu-id="268bc-139">Remarks</span></span>

<span data-ttu-id="268bc-140">**GlPolygonMode** 函式會控制要進行點陣的多邊形轉譯。</span><span class="sxs-lookup"><span data-stu-id="268bc-140">The **glPolygonMode** function controls the interpretation of polygons for rasterization.</span></span> <span data-ttu-id="268bc-141">*臉部* 參數描述適用的多邊形 *模式*：正面的多邊形 (gl \_ front) 、背面的多邊形 (GL \_ 回) ，或 (gl \_ 前端 \_ 和 \_ 後端) 。</span><span class="sxs-lookup"><span data-stu-id="268bc-141">The *face* parameter describes which polygons *mode* applies to: front-facing polygons (GL\_FRONT), back-facing polygons (GL\_BACK), or both (GL\_FRONT\_AND\_BACK).</span></span> <span data-ttu-id="268bc-142">多邊形模式只會影響多邊形的最終柵格化。</span><span class="sxs-lookup"><span data-stu-id="268bc-142">The polygon mode affects only the final rasterization of polygons.</span></span> <span data-ttu-id="268bc-143">尤其是，多邊形的頂點會發亮，並且在套用這些模式之前裁剪多邊形並可能會挑選。</span><span class="sxs-lookup"><span data-stu-id="268bc-143">In particular, a polygon's vertices are lit and the polygon is clipped and possibly culled before these modes are applied.</span></span>

<span data-ttu-id="268bc-144">若要繪製具有已填滿多邊形和空心多邊形的介面，請呼叫</span><span class="sxs-lookup"><span data-stu-id="268bc-144">To draw a surface with filled back-facing polygons and outlined front-facing polygons, call</span></span>

<span data-ttu-id="268bc-145">**glPolygonMode** (gl \_ FRONT、gl \_ 行) ;</span><span class="sxs-lookup"><span data-stu-id="268bc-145">**glPolygonMode**(GL\_FRONT, GL\_LINE);</span></span>

<span data-ttu-id="268bc-146">頂點會標示為界限，或具有邊緣旗標的 nonboundary。</span><span class="sxs-lookup"><span data-stu-id="268bc-146">Vertices are marked as boundary or nonboundary with an edge flag.</span></span> <span data-ttu-id="268bc-147">邊緣旗標是在分解多邊形時由 OpenGL 在內部產生的，而且可以使用 [**glEdgeFlag**](gledgeflag-functions.md)明確設定。</span><span class="sxs-lookup"><span data-stu-id="268bc-147">Edge flags are generated internally by OpenGL when it decomposes polygons, and they can be set explicitly using [**glEdgeFlag**](gledgeflag-functions.md).</span></span>

<span data-ttu-id="268bc-148">下列函式會抓取 **glPolygonMode** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="268bc-148">The following function retrieves information related to **glPolygonMode**:</span></span>

<span data-ttu-id="268bc-149">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 多邊形 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="268bc-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="268bc-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="268bc-150">Requirements</span></span>



| <span data-ttu-id="268bc-151">需求</span><span class="sxs-lookup"><span data-stu-id="268bc-151">Requirement</span></span> | <span data-ttu-id="268bc-152">值</span><span class="sxs-lookup"><span data-stu-id="268bc-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="268bc-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="268bc-153">Minimum supported client</span></span><br/> | <span data-ttu-id="268bc-154">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="268bc-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="268bc-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="268bc-155">Minimum supported server</span></span><br/> | <span data-ttu-id="268bc-156">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="268bc-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="268bc-157">標頭</span><span class="sxs-lookup"><span data-stu-id="268bc-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="268bc-158"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="268bc-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="268bc-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="268bc-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="268bc-160"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="268bc-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="268bc-161">DLL</span><span class="sxs-lookup"><span data-stu-id="268bc-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="268bc-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="268bc-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="268bc-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="268bc-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268bc-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="268bc-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="268bc-165">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="268bc-165">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="268bc-166">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="268bc-166">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="268bc-167">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="268bc-167">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="268bc-168">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="268bc-168">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="268bc-169">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="268bc-169">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="268bc-170">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="268bc-170">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





