---
title: 'glShadeModel 函式 (Gl) '
description: GlShadeModel 函式會選取平面或平滑陰影。
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- glShadeModel 函式 OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968550"
---
# <a name="glshademodel-function"></a><span data-ttu-id="699da-104">glShadeModel 函式</span><span class="sxs-lookup"><span data-stu-id="699da-104">glShadeModel function</span></span>

<span data-ttu-id="699da-105">**GlShadeModel** 函式會選取平面或平滑陰影。</span><span class="sxs-lookup"><span data-stu-id="699da-105">The **glShadeModel** function selects flat or smooth shading.</span></span>

## <a name="syntax"></a><span data-ttu-id="699da-106">語法</span><span class="sxs-lookup"><span data-stu-id="699da-106">Syntax</span></span>


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="699da-107">參數</span><span class="sxs-lookup"><span data-stu-id="699da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="699da-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="699da-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="699da-109">代表陰影技術的符號值。</span><span class="sxs-lookup"><span data-stu-id="699da-109">A symbolic value representing a shading technique.</span></span> <span data-ttu-id="699da-110">接受的值為 GL 一般 \_ 和 gl \_ 平滑。</span><span class="sxs-lookup"><span data-stu-id="699da-110">Accepted values are GL\_FLAT and GL\_SMOOTH.</span></span> <span data-ttu-id="699da-111">預設值為 GL \_ 平滑。</span><span class="sxs-lookup"><span data-stu-id="699da-111">The default is GL\_SMOOTH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="699da-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="699da-112">Return value</span></span>

<span data-ttu-id="699da-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="699da-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="699da-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="699da-114">Error codes</span></span>

<span data-ttu-id="699da-115">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="699da-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="699da-116">Name</span><span class="sxs-lookup"><span data-stu-id="699da-116">Name</span></span>                                                                                                  | <span data-ttu-id="699da-117">意義</span><span class="sxs-lookup"><span data-stu-id="699da-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="699da-118"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="699da-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="699da-119">*模式* 是 gl \_ GLAT 或 gl 平滑的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="699da-119">*mode* was a value other than GL\_GLAT or GL\_SMOOTH.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="699da-120"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="699da-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="699da-121">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="699da-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="699da-122">備註</span><span class="sxs-lookup"><span data-stu-id="699da-122">Remarks</span></span>

<span data-ttu-id="699da-123">OpenGL 基本型別可以是平面或平滑的陰影。</span><span class="sxs-lookup"><span data-stu-id="699da-123">OpenGL primitives can have either flat or smooth shading.</span></span> <span data-ttu-id="699da-124">平滑陰影（預設值）會使頂點的計算色彩插補，因為基本型別會進行柵格化，通常會將不同的色彩指派給每個產生的圖元片段。</span><span class="sxs-lookup"><span data-stu-id="699da-124">Smooth shading, the default, causes the computed colors of vertices to be interpolated as the primitive is rasterized, typically assigning different colors to each resulting pixel fragment.</span></span> <span data-ttu-id="699da-125">一般陰影只會選取一個頂點的計算色彩，並將其指派給所有藉由將單一基本型別來產生的圖元片段。</span><span class="sxs-lookup"><span data-stu-id="699da-125">Flat shading selects the computed color of just one vertex and assigns it to all the pixel fragments generated by rasterizing a single primitive.</span></span> <span data-ttu-id="699da-126">無論是哪一種情況，頂點的計算色彩都是光源的結果、如果已啟用光源，或是在指定頂點時的目前色彩（如果已停用光源的話）。</span><span class="sxs-lookup"><span data-stu-id="699da-126">In either case, the computed color of a vertex is the result of lighting, if lighting is enabled, or it is the current color at the time the vertex was specified, if lighting is disabled.</span></span>

<span data-ttu-id="699da-127">點的平面和平滑陰影不區分。</span><span class="sxs-lookup"><span data-stu-id="699da-127">Flat and smooth shading are indistinguishable for points.</span></span> <span data-ttu-id="699da-128">從1計算頂點和基本專案，從發出 [**glBegin**](glbegin.md) 時開始，每個平面陰影線條區段 *i* 都具有頂點 *i* + 1 的計算色彩（第二個頂點）。</span><span class="sxs-lookup"><span data-stu-id="699da-128">Counting vertices and primitives from one, starting when [**glBegin**](glbegin.md) is issued, each flat-shaded line segment *i* is given the computed color of vertex *i* + 1, its second vertex.</span></span> <span data-ttu-id="699da-129">從1開始計算，每個平面陰影多邊形都會獲得下表所列之頂點的計算色彩。</span><span class="sxs-lookup"><span data-stu-id="699da-129">Counting similarly from one, each flat-shaded polygon is given the computed color of the vertex listed in the following table.</span></span> <span data-ttu-id="699da-130">這是在所有案例中指定多邊形的最後一個頂點，但在單一多邊形中，第一個頂點指定平面陰影色彩。</span><span class="sxs-lookup"><span data-stu-id="699da-130">This is the last vertex to specify the polygon in all cases except single polygons, where the first vertex specifies the flat-shaded color.</span></span>



| <span data-ttu-id="699da-131">多邊形 i 的基本類型</span><span class="sxs-lookup"><span data-stu-id="699da-131">Primitive type of polygon i</span></span> | <span data-ttu-id="699da-132">頂點</span><span class="sxs-lookup"><span data-stu-id="699da-132">Vertex</span></span>   |
|-----------------------------|----------|
| <span data-ttu-id="699da-133">單一多邊形 (*I*= 1) </span><span class="sxs-lookup"><span data-stu-id="699da-133">Single polygon (*I*=1)</span></span>      | <span data-ttu-id="699da-134">1</span><span class="sxs-lookup"><span data-stu-id="699da-134">1</span></span>        |
| <span data-ttu-id="699da-135">三角形條紋</span><span class="sxs-lookup"><span data-stu-id="699da-135">Triangle strip</span></span>              | <span data-ttu-id="699da-136">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="699da-136">*i* + 2</span></span>  |
| <span data-ttu-id="699da-137">三角形風扇</span><span class="sxs-lookup"><span data-stu-id="699da-137">Triangle fan</span></span>                | <span data-ttu-id="699da-138">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="699da-138">*i* + 2</span></span>  |
| <span data-ttu-id="699da-139">獨立三角形</span><span class="sxs-lookup"><span data-stu-id="699da-139">Independent triangle</span></span>        | <span data-ttu-id="699da-140">3 *I*</span><span class="sxs-lookup"><span data-stu-id="699da-140">3 *I*</span></span>     |
| <span data-ttu-id="699da-141">四帶狀</span><span class="sxs-lookup"><span data-stu-id="699da-141">Quad strip</span></span>                  | <span data-ttu-id="699da-142">2 *i* + 2</span><span class="sxs-lookup"><span data-stu-id="699da-142">2 *i* + 2</span></span> |
| <span data-ttu-id="699da-143">獨立的四</span><span class="sxs-lookup"><span data-stu-id="699da-143">Independent quad</span></span>            | <span data-ttu-id="699da-144">4 *I*</span><span class="sxs-lookup"><span data-stu-id="699da-144">4 *I*</span></span>     |



 

<span data-ttu-id="699da-145">平面和平滑陰影是由 **glShadeModel** 所指定， *模式* 分別設定為 gl \_ 和 gl \_ 。</span><span class="sxs-lookup"><span data-stu-id="699da-145">Flat and smooth shading are specified by **glShadeModel** with *mode* set to GL\_FLAT and GL\_SMOOTH, respectively.</span></span>

<span data-ttu-id="699da-146">下列函式會抓取 **glShadeModel** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="699da-146">The following function retrieves information related to **glShadeModel**:</span></span>

<span data-ttu-id="699da-147">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 陰影 \_ 模型的 glGet</span><span class="sxs-lookup"><span data-stu-id="699da-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SHADE\_MODEL</span></span>

## <a name="requirements"></a><span data-ttu-id="699da-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="699da-148">Requirements</span></span>



| <span data-ttu-id="699da-149">需求</span><span class="sxs-lookup"><span data-stu-id="699da-149">Requirement</span></span> | <span data-ttu-id="699da-150">值</span><span class="sxs-lookup"><span data-stu-id="699da-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="699da-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="699da-151">Minimum supported client</span></span><br/> | <span data-ttu-id="699da-152">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="699da-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="699da-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="699da-153">Minimum supported server</span></span><br/> | <span data-ttu-id="699da-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="699da-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="699da-155">標頭</span><span class="sxs-lookup"><span data-stu-id="699da-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="699da-156"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="699da-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="699da-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="699da-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="699da-158"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="699da-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="699da-159">DLL</span><span class="sxs-lookup"><span data-stu-id="699da-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="699da-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="699da-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="699da-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="699da-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="699da-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="699da-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="699da-163">**glColor**</span><span class="sxs-lookup"><span data-stu-id="699da-163">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="699da-164">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="699da-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="699da-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="699da-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="699da-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="699da-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





