---
title: 'glDisable 函式 (Gl) '
description: 'GlEnable 和 glDisable 函數會啟用或停用 OpenGL 功能。 |glDisable 函式 (Gl) '
ms.assetid: 094f730e-5e2b-485e-8d9d-fee2902d3d5f
keywords:
- glDisable 函式 OpenGL
topic_type:
- apiref
api_name:
- glDisable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff5c12e53eb060777f75ad537bed265401a7a26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981979"
---
# <a name="gldisable-function"></a><span data-ttu-id="f8ddd-105">glDisable 函式</span><span class="sxs-lookup"><span data-stu-id="f8ddd-105">glDisable function</span></span>

<span data-ttu-id="f8ddd-106">[**GlEnable**](glenable.md)和 **glDisable** 函數會啟用或停用 OpenGL 功能。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-106">The [**glEnable**](glenable.md) and **glDisable** functions enable or disable OpenGL capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ddd-107">語法</span><span class="sxs-lookup"><span data-stu-id="f8ddd-107">Syntax</span></span>


```C++
void WINAPI glDisable(
   GLenum cap
);
```



## <a name="parameters"></a><span data-ttu-id="f8ddd-108">參數</span><span class="sxs-lookup"><span data-stu-id="f8ddd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ddd-109">*帽*</span><span class="sxs-lookup"><span data-stu-id="f8ddd-109">*cap*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ddd-110">表示 OpenGL 功能的符號常數。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-110">A symbolic constant indicating an OpenGL capability.</span></span>

<span data-ttu-id="f8ddd-111">如需值 *上限* 的討論，請參閱下列備註一節。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-111">For discussion of the values *cap* can take, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ddd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8ddd-112">Return value</span></span>

<span data-ttu-id="f8ddd-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f8ddd-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f8ddd-114">Error codes</span></span>

<span data-ttu-id="f8ddd-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f8ddd-116">Name</span><span class="sxs-lookup"><span data-stu-id="f8ddd-116">Name</span></span>                                                                                                  | <span data-ttu-id="f8ddd-117">意義</span><span class="sxs-lookup"><span data-stu-id="f8ddd-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8ddd-118"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ddd-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f8ddd-119">*上限* 不是先前 [備註] 區段中所列的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-119">*cap* was not one of the values listed in the preceding Remarks section.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="f8ddd-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ddd-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f8ddd-121">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f8ddd-122">備註</span><span class="sxs-lookup"><span data-stu-id="f8ddd-122">Remarks</span></span>

<span data-ttu-id="f8ddd-123">[**GlEnable**](glenable.md)和 **glDisable** 函式會啟用和停用各種 OpenGL 圖形功能。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-123">The [**glEnable**](glenable.md) and **glDisable** functions enable and disable various OpenGL graphics capabilities.</span></span> <span data-ttu-id="f8ddd-124">使用 [**glIsEnabled**](glisenabled.md) 或 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 來判斷任何功能目前的設定。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-124">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="f8ddd-125">[**GlEnable**](glenable.md)和 **glDisable** 都採用單一引數（ *cap*），其可採用下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="f8ddd-125">Both [**glEnable**](glenable.md) and **glDisable** take a single argument, *cap*, which can assume one of the following values:</span></span>



| <span data-ttu-id="f8ddd-126">值</span><span class="sxs-lookup"><span data-stu-id="f8ddd-126">Value</span></span>                       | <span data-ttu-id="f8ddd-127">意義</span><span class="sxs-lookup"><span data-stu-id="f8ddd-127">Meaning</span></span>                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ddd-128">GL \_ ALPHA \_ 測試</span><span class="sxs-lookup"><span data-stu-id="f8ddd-128">GL\_ALPHA\_TEST</span></span>             | <span data-ttu-id="f8ddd-129">啟用時，請進行 Alpha 測試。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-129">If enabled, do alpha testing.</span></span> <span data-ttu-id="f8ddd-130">請參閱 [**glAlphaFunc**](glalphafunc.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-130">See [**glAlphaFunc**](glalphafunc.md).</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="f8ddd-131">GL \_ 自動 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="f8ddd-131">GL\_AUTO\_NORMAL</span></span>            | <span data-ttu-id="f8ddd-132">若已啟用，則當 GL \_ List.map2 \_ 頂點 \_ 3 或 gl \_ list.map2 \_ 頂點 \_ 4 產生頂點時，計算介面標準向量會 analytically。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-132">If enabled, compute surface normal vectors analytically when either GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4 has generated vertices.</span></span> <span data-ttu-id="f8ddd-133">請參閱 [**glMap2**](glmap2.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-133">See [**glMap2**](glmap2.md).</span></span>                                                                                        |
| <span data-ttu-id="f8ddd-134">GL \_ BLEND</span><span class="sxs-lookup"><span data-stu-id="f8ddd-134">GL\_BLEND</span></span>                   | <span data-ttu-id="f8ddd-135">若已啟用，請將內送 RGBA 色彩值與色彩緩衝區中的值混合。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-135">If enabled, blend the incoming RGBA color values with the values in the color buffers.</span></span> <span data-ttu-id="f8ddd-136">請參閱 [**glBlendFunc**](glblendfunc.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-136">See [**glBlendFunc**](glblendfunc.md).</span></span>                                                                                                                              |
| <span data-ttu-id="f8ddd-137">GL \_ 剪輯 \_ 平面 *i*</span><span class="sxs-lookup"><span data-stu-id="f8ddd-137">GL\_CLIP\_PLANE *i*</span></span>          | <span data-ttu-id="f8ddd-138">若已啟用，則會根據使用者 *定義的裁剪平面來* 裁剪幾何。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-138">If enabled, clip geometry against user-defined clipping plane *i*.</span></span> <span data-ttu-id="f8ddd-139">請參閱 [**glClipPlane**](glclipplane.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-139">See [**glClipPlane**](glclipplane.md).</span></span>                                                                                                                                                  |
| <span data-ttu-id="f8ddd-140">GL \_ 色彩 \_ 邏輯 \_ OP</span><span class="sxs-lookup"><span data-stu-id="f8ddd-140">GL\_COLOR\_LOGIC\_OP</span></span>        | <span data-ttu-id="f8ddd-141">啟用時，將目前的邏輯作業套用至傳入的 RGBA 色彩和色彩緩衝區值。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-141">If enabled, apply the current logical operation to the incoming RGBA color and color buffer values.</span></span> <span data-ttu-id="f8ddd-142">請參閱 [**glLogicOp**](gllogicop.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-142">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                     |
| <span data-ttu-id="f8ddd-143">GL \_ 色彩 \_ 材質</span><span class="sxs-lookup"><span data-stu-id="f8ddd-143">GL\_COLOR\_MATERIAL</span></span>         | <span data-ttu-id="f8ddd-144">啟用時，有一或多個材質參數可追蹤目前的色彩。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-144">If enabled, have one or more material parameters track the current color.</span></span> <span data-ttu-id="f8ddd-145">請參閱 [**glColorMaterial**](glcolormaterial.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-145">See [**glColorMaterial**](glcolormaterial.md).</span></span>                                                                                                                                   |
| <span data-ttu-id="f8ddd-146">GL \_ 精選 \_ 臉部</span><span class="sxs-lookup"><span data-stu-id="f8ddd-146">GL\_CULL\_FACE</span></span>              | <span data-ttu-id="f8ddd-147">若已啟用，則根據視窗座標中的纏繞來挑選多邊形。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-147">If enabled, cull polygons based on their winding in window coordinates.</span></span> <span data-ttu-id="f8ddd-148">請參閱 [**glCullFace**](glcullface.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-148">See [**glCullFace**](glcullface.md).</span></span>                                                                                                                                               |
| <span data-ttu-id="f8ddd-149">GL \_ 深度 \_ 測試</span><span class="sxs-lookup"><span data-stu-id="f8ddd-149">GL\_DEPTH\_TEST</span></span>             | <span data-ttu-id="f8ddd-150">如果啟用，請進行深度比較，並更新深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-150">If enabled, do depth comparisons and update the depth buffer.</span></span> <span data-ttu-id="f8ddd-151">請參閱 [**glDepthFunc**](gldepthfunc.md) 和 [**glDepthRange**](gldepthrange.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-151">See [**glDepthFunc**](gldepthfunc.md) and [**glDepthRange**](gldepthrange.md).</span></span>                                                                                                              |
| <span data-ttu-id="f8ddd-152">GL \_ 遞色</span><span class="sxs-lookup"><span data-stu-id="f8ddd-152">GL\_DITHER</span></span>                  | <span data-ttu-id="f8ddd-153">若已啟用，則會先將色彩元件或索引寫入色彩緩衝區，然後再將其寫入。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-153">If enabled, dither color components or indexes before they are written to the color buffer.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="f8ddd-154">GL \_ 霧化</span><span class="sxs-lookup"><span data-stu-id="f8ddd-154">GL\_FOG</span></span>                     | <span data-ttu-id="f8ddd-155">若已啟用，請將 [霧化色彩] 混合成紋理後色彩。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-155">If enabled, blend a fog color into the post-texturing color.</span></span> <span data-ttu-id="f8ddd-156">請參閱 [**glFog**](glfog.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-156">See [**glFog**](glfog.md).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="f8ddd-157">GL \_ 索引 \_ 邏輯 \_ OP</span><span class="sxs-lookup"><span data-stu-id="f8ddd-157">GL\_INDEX\_LOGIC\_OP</span></span>        | <span data-ttu-id="f8ddd-158">若已啟用，請將目前的邏輯運算套用至傳入索引和色彩緩衝區索引。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-158">If enabled, apply the current logical operation to the incoming index and color buffer indices.</span></span> <span data-ttu-id="f8ddd-159">請參閱 [**glLogicOp**](gllogicop.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-159">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                         |
| <span data-ttu-id="f8ddd-160">GL \_ 燈</span><span class="sxs-lookup"><span data-stu-id="f8ddd-160">GL\_LIGHT *i*</span></span>                | <span data-ttu-id="f8ddd-161">若已啟用，請在光源方程式的評估中包含淺 *i* 。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-161">If enabled, include light *i* in the evaluation of the lighting equation.</span></span> <span data-ttu-id="f8ddd-162">請參閱 [**glLightModel**](gllightmodel-functions.md) 和 [**glLight**](gllight-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-162">See [**glLightModel**](gllightmodel-functions.md) and [**glLight**](gllight-functions.md).</span></span>                                                                                      |
| <span data-ttu-id="f8ddd-163">GL \_ 照明</span><span class="sxs-lookup"><span data-stu-id="f8ddd-163">GL\_LIGHTING</span></span>                | <span data-ttu-id="f8ddd-164">若已啟用，請使用目前的光源參數來計算頂點色彩或索引。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-164">If enabled, use the current lighting parameters to compute the vertex color or index.</span></span> <span data-ttu-id="f8ddd-165">如果停用，請將目前的色彩或索引與每個頂點產生關聯。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-165">If disabled, associate the current color or index with each vertex.</span></span> <span data-ttu-id="f8ddd-166">請參閱 [**glMaterial**](glmaterial-functions.md)、 **glLightModel** 和 **glLight**。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-166">See [**glMaterial**](glmaterial-functions.md), **glLightModel**, and **glLight**.</span></span>                |
| <span data-ttu-id="f8ddd-167">GL \_ 行 \_ 平滑</span><span class="sxs-lookup"><span data-stu-id="f8ddd-167">GL\_LINE\_SMOOTH</span></span>            | <span data-ttu-id="f8ddd-168">若已啟用，請使用正確的篩選繪製行。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-168">If enabled, draw lines with correct filtering.</span></span> <span data-ttu-id="f8ddd-169">如果停用，則繪製別名行。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-169">If disabled, draw aliased lines.</span></span> <span data-ttu-id="f8ddd-170">請參閱 [**glLineWidth**](gllinewidth.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-170">See [**glLineWidth**](gllinewidth.md).</span></span>                                                                                                                                     |
| <span data-ttu-id="f8ddd-171">GL \_ 線 \_ STIPPLE</span><span class="sxs-lookup"><span data-stu-id="f8ddd-171">GL\_LINE\_STIPPLE</span></span>           | <span data-ttu-id="f8ddd-172">若已啟用，則會在繪製線條時使用目前的行 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-172">If enabled, use the current line stipple pattern when drawing lines.</span></span> <span data-ttu-id="f8ddd-173">請參閱 [**glLineStipple**](gllinestipple.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-173">See [**glLineStipple**](gllinestipple.md).</span></span>                                                                                                                                            |
| <span data-ttu-id="f8ddd-174">GL \_ 邏輯 \_ OP</span><span class="sxs-lookup"><span data-stu-id="f8ddd-174">GL\_LOGIC\_OP</span></span>               | <span data-ttu-id="f8ddd-175">啟用時，將目前選取的邏輯作業套用至內送和色彩緩衝區索引。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-175">If enabled, apply the currently selected logical operation to the incoming and color-buffer indexes.</span></span> <span data-ttu-id="f8ddd-176">請參閱 [**glLogicOp**](gllogicop.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-176">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                    |
| <span data-ttu-id="f8ddd-177">GL \_ MAP1 \_ 色彩 \_ 4</span><span class="sxs-lookup"><span data-stu-id="f8ddd-177">GL\_MAP1\_COLOR\_4</span></span>          | <span data-ttu-id="f8ddd-178">如果啟用， [**glEvalCoord1**](glevalcoord-functions.md)、 [**glEvalMesh1**](glevalmesh-functions.md)和 [**GLEVALPOINT1**](glevalpoint.md) 的呼叫會產生 RGBA 值。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-178">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="f8ddd-179">另請參閱 [**glMap1**](glmap1.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-179">See also [**glMap1**](glmap1.md).</span></span>                                           |
| <span data-ttu-id="f8ddd-180">GL \_ MAP1 \_ 索引</span><span class="sxs-lookup"><span data-stu-id="f8ddd-180">GL\_MAP1\_INDEX</span></span>             | <span data-ttu-id="f8ddd-181">如果啟用，呼叫 **glEvalCoord1**、 **glEvalMesh1** 和 **glEvalPoint1** 會產生色彩索引。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-181">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate color indexes.</span></span> <span data-ttu-id="f8ddd-182">另請參閱 **glMap1**。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-182">See also **glMap1**.</span></span>                                                                                                                                   |
| <span data-ttu-id="f8ddd-183">GL \_ MAP1 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="f8ddd-183">GL\_MAP1\_NORMAL</span></span>            | <span data-ttu-id="f8ddd-184">如果啟用， [**glEvalCoord1**](glevalcoord-functions.md)、 [**glEvalMesh1**](glevalmesh-functions.md)和 [**glEvalPoint1**](glevalpoint.md) 的呼叫會產生法線。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-184">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="f8ddd-185">另請參閱 [**glMap1**](glmap1.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-185">See also [**glMap1**](glmap1.md).</span></span>                                               |
| <span data-ttu-id="f8ddd-186">GL \_ MAP1 \_ 材質 \_ COORD \_ 1</span><span class="sxs-lookup"><span data-stu-id="f8ddd-186">GL\_MAP1\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="f8ddd-187">如果啟用， **glEvalCoord1**、 **glEvalMesh1** 和 **glEvalPoint1** 的呼叫會產生 *s* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-187">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s* texture coordinates.</span></span> <span data-ttu-id="f8ddd-188">另請參閱 **glMap1**。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-188">See also **glMap1**.</span></span>                                                                                                                         |
| <span data-ttu-id="f8ddd-189">GL \_ MAP1 \_ 材質 \_ COORD \_ 2</span><span class="sxs-lookup"><span data-stu-id="f8ddd-189">GL\_MAP1\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="f8ddd-190">如果啟用，呼叫 [**glEvalCoord1**](glevalcoord-functions.md)、 [**glEvalMesh1**](glevalmesh-functions.md)和 [**glEvalPoint1**](glevalpoint.md) 會產生 *s* 和 *t* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-190">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="f8ddd-191">另請參閱 [**glMap1**](glmap1.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-191">See also [**glMap1**](glmap1.md).</span></span>                       |
| <span data-ttu-id="f8ddd-192">GL \_ MAP1 \_ 材質 \_ COORD \_ 3</span><span class="sxs-lookup"><span data-stu-id="f8ddd-192">GL\_MAP1\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="f8ddd-193">如果啟用， **glEvalCoord1**、 **glEvalMesh1** 和 **glEvalPoint1** 的呼叫會產生 *s*、 *t* 和 *r* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-193">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="f8ddd-194">另請參閱 **glMap1**。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-194">See also **glMap1**.</span></span>                                                                                                           |
| <span data-ttu-id="f8ddd-195">GL \_ MAP1 \_ 材質 \_ COORD \_ 4</span><span class="sxs-lookup"><span data-stu-id="f8ddd-195">GL\_MAP1\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="f8ddd-196">如果啟用， [glEvalCoord1](glevalcoord-functions.md)、 [glEvalMesh1](glevalmesh-functions.md)和 [**glEvalPoint1**](glevalpoint.md) 的呼叫會產生 *s*、 *t*、 *r* 和 *q* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-196">If enabled, calls to [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="f8ddd-197">另請參閱 [**glMap1**](glmap1.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-197">See also [**glMap1**](glmap1.md).</span></span>                    |
| <span data-ttu-id="f8ddd-198">GL \_ MAP1 \_ 頂點 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f8ddd-198">GL\_MAP1\_VERTEX\_3</span></span>         | <span data-ttu-id="f8ddd-199">如果啟用， **glEvalCoord1**、 **glEvalMesh1** 和 **glEvalPoint1** 的呼叫會產生 *x*、 *y* 和 *z* 頂點座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-199">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="f8ddd-200">另請參閱 **glMap1**。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-200">See also **glMap1**.</span></span>                                                                                                            |
| <span data-ttu-id="f8ddd-201">GL \_ MAP1 \_ 頂點 \_ 4</span><span class="sxs-lookup"><span data-stu-id="f8ddd-201">GL\_MAP1\_VERTEX\_4</span></span>         | <span data-ttu-id="f8ddd-202">如果啟用， [**glEvalCoord1**](glevalcoord-functions.md)、 [**glEvalMesh1**](glevalmesh-functions.md)和 [**glEvalPoint1**](glevalpoint.md) 的呼叫會產生同質 *x*、 *y*、 *z* 和 *w* 頂點座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-202">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="f8ddd-203">另請參閱 [**glMap1**](glmap1.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-203">See also [**glMap1**](glmap1.md).</span></span> |
| <span data-ttu-id="f8ddd-204">GL \_ List.map2 \_ 色彩 \_ 4</span><span class="sxs-lookup"><span data-stu-id="f8ddd-204">GL\_MAP2\_COLOR\_4</span></span>          | <span data-ttu-id="f8ddd-205">如果啟用， [**glEvalCoord2**](glevalcoord-functions.md)、 [**glEvalMesh2**](glevalmesh-functions.md)和 [**GLEVALPOINT2**](glevalpoint.md) 的呼叫會產生 RGBA 值。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-205">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="f8ddd-206">另請參閱 [**glMap2**](glmap2.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-206">See also [**glMap2**](glmap2.md).</span></span>                                           |
| <span data-ttu-id="f8ddd-207">GL \_ List.map2 \_ 索引</span><span class="sxs-lookup"><span data-stu-id="f8ddd-207">GL\_MAP2\_INDEX</span></span>             | <span data-ttu-id="f8ddd-208">如果啟用，呼叫 **glEvalCoord2**、 **glEvalMesh2** 和 **glEvalPoint2** 會產生色彩索引。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-208">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate color indexes.</span></span> <span data-ttu-id="f8ddd-209">另請參閱 **glMap2**。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-209">See also **glMap2**.</span></span>                                                                                                                                   |
| <span data-ttu-id="f8ddd-210">GL \_ List.map2 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="f8ddd-210">GL\_MAP2\_NORMAL</span></span>            | <span data-ttu-id="f8ddd-211">如果啟用， [**glEvalCoord2**](glevalcoord-functions.md)、 [**glEvalMesh2**](glevalmesh-functions.md)和 [**glEvalPoint2**](glevalpoint.md) 的呼叫會產生法線。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-211">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="f8ddd-212">另請參閱 [**glMap2**](glmap2.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-212">See also [**glMap2**](glmap2.md).</span></span>                                               |
| <span data-ttu-id="f8ddd-213">GL \_ List.map2 \_ 材質 \_ COORD \_ 1</span><span class="sxs-lookup"><span data-stu-id="f8ddd-213">GL\_MAP2\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="f8ddd-214">如果啟用， **glEvalCoord2**、 **glEvalMesh2** 和 **glEvalPoint2** 的呼叫會產生 *s* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-214">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s* texture coordinates.</span></span> <span data-ttu-id="f8ddd-215">另請參閱 **glMap2**。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-215">See also **glMap2**.</span></span>                                                                                                                         |
| <span data-ttu-id="f8ddd-216">GL \_ List.map2 \_ 材質 \_ COORD \_ 2</span><span class="sxs-lookup"><span data-stu-id="f8ddd-216">GL\_MAP2\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="f8ddd-217">如果啟用，呼叫 [**glEvalCoord2**](glevalcoord-functions.md)、 [**glEvalMesh2**](glevalmesh-functions.md)和 [**glEvalPoint2**](glevalpoint.md) 會產生 *s* 和 *t* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-217">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="f8ddd-218">另請參閱 [**glMap2**](glmap2.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-218">See also [**glMap2**](glmap2.md).</span></span>                       |
| <span data-ttu-id="f8ddd-219">GL \_ List.map2 \_ 材質 \_ COORD \_ 3</span><span class="sxs-lookup"><span data-stu-id="f8ddd-219">GL\_MAP2\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="f8ddd-220">如果啟用， **glEvalCoord2**、 **glEvalMesh2** 和 **glEvalPoint2** 的呼叫會產生 *s*、 *t* 和 *r* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-220">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="f8ddd-221">另請參閱 **glMap2**。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-221">See also **glMap2**.</span></span>                                                                                                           |
| <span data-ttu-id="f8ddd-222">GL \_ List.map2 \_ 材質 \_ COORD \_ 4</span><span class="sxs-lookup"><span data-stu-id="f8ddd-222">GL\_MAP2\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="f8ddd-223">如果啟用， [**glEvalCoord2**](glevalcoord-functions.md)、 [**glEvalMesh2**](glevalmesh-functions.md)和 [**glEvalPoint2**](glevalpoint.md) 的呼叫會產生 *s*、 *t*、 *r* 和 *q* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-223">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="f8ddd-224">另請參閱 [**glMap2**](glmap2.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-224">See also [**glMap2**](glmap2.md).</span></span>            |
| <span data-ttu-id="f8ddd-225">GL \_ List.map2 \_ 頂點 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f8ddd-225">GL\_MAP2\_VERTEX\_3</span></span>         | <span data-ttu-id="f8ddd-226">如果啟用， **glEvalCoord2**、 **glEvalMesh2** 和 **glEvalPoint2** 的呼叫會產生 *x*、 *y* 和 *z* 頂點座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-226">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="f8ddd-227">另請參閱 **glMap2**。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-227">See also **glMap2**.</span></span>                                                                                                            |
| <span data-ttu-id="f8ddd-228">GL \_ List.map2 \_ 頂點 \_ 4</span><span class="sxs-lookup"><span data-stu-id="f8ddd-228">GL\_MAP2\_VERTEX\_4</span></span>         | <span data-ttu-id="f8ddd-229">如果啟用， [**glEvalCoord2**](glevalcoord-functions.md)、 [**glEvalMesh2**](glevalmesh-functions.md)和 [**glEvalPoint2**](glevalpoint.md) 的呼叫會產生同質 *x*、 *y*、 *z* 和 *w* 頂點座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-229">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="f8ddd-230">另請參閱 [**glMap2**](glmap2.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-230">See also [**glMap2**](glmap2.md).</span></span> |
| <span data-ttu-id="f8ddd-231">GL \_ 標準化</span><span class="sxs-lookup"><span data-stu-id="f8ddd-231">GL\_NORMALIZE</span></span>               | <span data-ttu-id="f8ddd-232">啟用時，以 **glNormal** 指定的一般向量會在轉換之後調整為單位長度。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-232">If enabled, normal vectors specified with **glNormal** are scaled to unit length after transformation.</span></span> <span data-ttu-id="f8ddd-233">請參閱 [**glNormal**](glnormal-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-233">See [**glNormal**](glnormal-functions.md).</span></span>                                                                                                          |
| <span data-ttu-id="f8ddd-234">GL \_ 點 \_ 平滑</span><span class="sxs-lookup"><span data-stu-id="f8ddd-234">GL\_POINT\_SMOOTH</span></span>           | <span data-ttu-id="f8ddd-235">若已啟用，請使用適當的篩選繪製點。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-235">If enabled, draw points with proper filtering.</span></span> <span data-ttu-id="f8ddd-236">如果已停用，請繪製別名點。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-236">If disabled, draw aliased points.</span></span> <span data-ttu-id="f8ddd-237">請參閱 [**glPointSize**](glpointsize.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-237">See [**glPointSize**](glpointsize.md).</span></span>                                                                                                                                    |
| <span data-ttu-id="f8ddd-238">GL \_ 多邊形 \_ 位移 \_ 填滿</span><span class="sxs-lookup"><span data-stu-id="f8ddd-238">GL\_POLYGON\_OFFSET\_FILL</span></span>   | <span data-ttu-id="f8ddd-239">如果啟用，而且多邊形是以 GL \_ 填滿模式轉譯，則在執行深度比較之前，會先將位移新增至多邊形片段的深度值。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-239">If enabled, and if the polygon is rendered in GL\_FILL mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="f8ddd-240">請參閱 [**glPolygonOffset**](glpolygonoffset.md)**。**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-240">See [**glPolygonOffset**](glpolygonoffset.md)**.**</span></span>                                      |
| <span data-ttu-id="f8ddd-241">GL \_ 多邊形 \_ 位移 \_ 線</span><span class="sxs-lookup"><span data-stu-id="f8ddd-241">GL\_POLYGON\_OFFSET\_LINE</span></span>   | <span data-ttu-id="f8ddd-242">如果啟用，而且多邊形是以 GL \_ 線模式轉譯，則在執行深度比較之前，會先將位移新增至多邊形片段的深度值。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-242">If enabled, and if the polygon is rendered in GL\_LINE mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="f8ddd-243">請參閱 **glPolygonOffset**。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-243">See **glPolygonOffset**.</span></span>                                                                 |
| <span data-ttu-id="f8ddd-244">GL \_ 多邊形 \_ 位移 \_ 點</span><span class="sxs-lookup"><span data-stu-id="f8ddd-244">GL\_POLYGON\_OFFSET\_POINT</span></span>  | <span data-ttu-id="f8ddd-245">如果啟用，則在執行深度比較之前，會將位移加入多邊形片段的深度值，如果多邊形是以 GL \_ 點模式轉譯。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-245">If enabled, an offset is added to depth values of a polygon's fragments before the depth comparison is performed, if the polygon is rendered in GL\_POINT mode.</span></span> <span data-ttu-id="f8ddd-246">請參閱 [**glPolygonOffset**](glpolygonoffset.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-246">See [**glPolygonOffset**](glpolygonoffset.md).</span></span>                                             |
| <span data-ttu-id="f8ddd-247">GL \_ 多邊形 \_ 平滑</span><span class="sxs-lookup"><span data-stu-id="f8ddd-247">GL\_POLYGON\_SMOOTH</span></span>         | <span data-ttu-id="f8ddd-248">如果啟用，則繪製具有適當篩選的多邊形。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-248">If enabled, draw polygons with proper filtering.</span></span> <span data-ttu-id="f8ddd-249">如果停用，則繪製別名的多邊形。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-249">If disabled, draw aliased polygons.</span></span> <span data-ttu-id="f8ddd-250">請參閱 [**glPolygonMode**](glpolygonmode.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-250">See [**glPolygonMode**](glpolygonmode.md).</span></span>                                                                                                                            |
| <span data-ttu-id="f8ddd-251">GL \_ 多邊形 \_ STIPPLE</span><span class="sxs-lookup"><span data-stu-id="f8ddd-251">GL\_POLYGON\_STIPPLE</span></span>        | <span data-ttu-id="f8ddd-252">若已啟用，則在轉譯多邊形時使用目前的多邊形 stipple 模式。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-252">If enabled, use the current polygon stipple pattern when rendering polygons.</span></span> <span data-ttu-id="f8ddd-253">請參閱 [**glPolygonStipple**](glpolygonstipple.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-253">See [**glPolygonStipple**](glpolygonstipple.md).</span></span>                                                                                                                              |
| <span data-ttu-id="f8ddd-254">GL \_ 剪式 \_ 測試</span><span class="sxs-lookup"><span data-stu-id="f8ddd-254">GL\_SCISSOR\_TEST</span></span>           | <span data-ttu-id="f8ddd-255">如果已啟用，則捨棄剪式矩形外部的片段。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-255">If enabled, discard fragments that are outside the scissor rectangle.</span></span> <span data-ttu-id="f8ddd-256">請參閱 [**glScissor**](glscissor.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-256">See [**glScissor**](glscissor.md).</span></span>                                                                                                                                                   |
| <span data-ttu-id="f8ddd-257">GL \_ 樣板 \_ 測試</span><span class="sxs-lookup"><span data-stu-id="f8ddd-257">GL\_STENCIL\_TEST</span></span>           | <span data-ttu-id="f8ddd-258">若已啟用，請進行樣板測試並更新樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-258">If enabled, do stencil testing and update the stencil buffer.</span></span> <span data-ttu-id="f8ddd-259">請參閱 [**glStencilFunc**](glstencilfunc.md) 和 [**glStencilOp**](glstencilop.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-259">See [**glStencilFunc**](glstencilfunc.md) and [**glStencilOp**](glstencilop.md).</span></span>                                                                                                            |
| <span data-ttu-id="f8ddd-260">GL \_ 材質 \_ 1d</span><span class="sxs-lookup"><span data-stu-id="f8ddd-260">GL\_TEXTURE\_1D</span></span>             | <span data-ttu-id="f8ddd-261">如果啟用，則會 (執行一維紋理，除非同時啟用了二維紋理) 。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-261">If enabled, one-dimensional texturing is performed (unless two-dimensional texturing is also enabled).</span></span> <span data-ttu-id="f8ddd-262">請參閱 [**glTexImage1D**](glteximage1d.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-262">See [**glTexImage1D**](glteximage1d.md).</span></span>                                                                                                            |
| <span data-ttu-id="f8ddd-263">GL \_ 材質 \_ 2d</span><span class="sxs-lookup"><span data-stu-id="f8ddd-263">GL\_TEXTURE\_2D</span></span>             | <span data-ttu-id="f8ddd-264">如果啟用，則會執行二維紋理。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-264">If enabled, two-dimensional texturing is performed.</span></span> <span data-ttu-id="f8ddd-265">請參閱 [**glTexImage2D**](glteximage2d.md)。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-265">See [**glTexImage2D**](glteximage2d.md).</span></span>                                                                                                                                                               |
| <span data-ttu-id="f8ddd-266">GL \_ 材質 \_ GEN \_ Q</span><span class="sxs-lookup"><span data-stu-id="f8ddd-266">GL\_TEXTURE\_GEN\_Q</span></span>         | <span data-ttu-id="f8ddd-267">如果啟用，則會使用以 [**glTexGen**](gltexgen-functions.md)定義的材質產生函數來計算 *q* 紋理座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-267">If enabled, the *q* texture coordinate is computed using the texture-generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="f8ddd-268">否則，會使用目前的 *q* 紋理座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-268">Otherwise, the current *q* texture coordinate is used.</span></span>                                                        |
| <span data-ttu-id="f8ddd-269">GL \_ 材質 \_ GEN \_ R</span><span class="sxs-lookup"><span data-stu-id="f8ddd-269">GL\_TEXTURE\_GEN\_R</span></span>         | <span data-ttu-id="f8ddd-270">啟用時，會使用以 [**glTexGen**](gltexgen-functions.md)定義的材質產生函數來計算 *r* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-270">If enabled, the *r* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="f8ddd-271">如果停用，則會使用目前的 *r* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-271">If disabled, the current *r* texture coordinate is used.</span></span>                                                      |
| <span data-ttu-id="f8ddd-272">GL \_ 材質 \_ GEN \_ S</span><span class="sxs-lookup"><span data-stu-id="f8ddd-272">GL\_TEXTURE\_GEN\_S</span></span>         | <span data-ttu-id="f8ddd-273">若已啟用，則會使用以 **glTexGen** 定義的材質產生函數來計算 *s* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-273">If enabled, the *s* texture coordinate is computed using the texture generation function defined with **glTexGen**.</span></span> <span data-ttu-id="f8ddd-274">如果停用，則會 *使用目前的* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-274">If disabled, the current *s* texture coordinate is used.</span></span>                                                                                |
| <span data-ttu-id="f8ddd-275">GL \_ 材質 \_ GEN \_ T</span><span class="sxs-lookup"><span data-stu-id="f8ddd-275">GL\_TEXTURE\_GEN\_T</span></span>         | <span data-ttu-id="f8ddd-276">若已啟用，則會使用以 [**glTexGen**](gltexgen-functions.md)定義的材質產生函數來計算 *t* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-276">If enabled, the *t* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="f8ddd-277">如果停用，則會使用目前的 *t* 材質座標。</span><span class="sxs-lookup"><span data-stu-id="f8ddd-277">If disabled, the current *t* texture coordinate is used.</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="f8ddd-278">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8ddd-278">Requirements</span></span>



| <span data-ttu-id="f8ddd-279">需求</span><span class="sxs-lookup"><span data-stu-id="f8ddd-279">Requirement</span></span> | <span data-ttu-id="f8ddd-280">值</span><span class="sxs-lookup"><span data-stu-id="f8ddd-280">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ddd-281">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8ddd-281">Minimum supported client</span></span><br/> | <span data-ttu-id="f8ddd-282">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8ddd-282">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f8ddd-283">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8ddd-283">Minimum supported server</span></span><br/> | <span data-ttu-id="f8ddd-284">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8ddd-284">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f8ddd-285">標頭</span><span class="sxs-lookup"><span data-stu-id="f8ddd-285">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8ddd-286"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="f8ddd-286"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f8ddd-287">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8ddd-287">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8ddd-288"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8ddd-288"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f8ddd-289">DLL</span><span class="sxs-lookup"><span data-stu-id="f8ddd-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8ddd-290"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8ddd-290"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8ddd-291">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8ddd-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ddd-292">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-292">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-293">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-293">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-294">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-294">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-295">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-295">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-296">**glClipPlane**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-296">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-297">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-297">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-298">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-298">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-299">**glCullFace**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-299">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-300">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-300">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-301">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-301">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-302">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-302">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-303">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-303">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-304">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-304">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-305">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-305">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-306">**glEvalCoord1**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-306">**glEvalCoord1**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-307">**glEvalMesh1**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-307">**glEvalMesh1**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-308">**glEvalPoint1**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-308">**glEvalPoint1**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-309">**glFog**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-309">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-310">**glGet**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-310">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-311">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-311">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-312">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-312">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-313">**glLight**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-313">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-314">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-314">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-315">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-315">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-316">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-316">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-317">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-317">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-318">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-318">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-319">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-319">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-320">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-320">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-321">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-321">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-322">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-322">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-323">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-323">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-324">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-324">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-325">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-325">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-326">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-326">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-327">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-327">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-328">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-328">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-329">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-329">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-330">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-330">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-331">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-331">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="f8ddd-332">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="f8ddd-332">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





