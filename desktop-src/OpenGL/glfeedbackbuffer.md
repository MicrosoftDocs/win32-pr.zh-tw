---
title: 'glFeedbackBuffer 函式 (Gl) '
description: GlFeedbackBuffer 函式會控制意見反應模式。
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- glFeedbackBuffer 函式 OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968177"
---
# <a name="glfeedbackbuffer-function"></a><span data-ttu-id="c63ed-104">glFeedbackBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="c63ed-104">glFeedbackBuffer function</span></span>

<span data-ttu-id="c63ed-105">**GlFeedbackBuffer** 函式會控制意見反應模式。</span><span class="sxs-lookup"><span data-stu-id="c63ed-105">The **glFeedbackBuffer** function controls feedback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="c63ed-106">語法</span><span class="sxs-lookup"><span data-stu-id="c63ed-106">Syntax</span></span>


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="c63ed-107">參數</span><span class="sxs-lookup"><span data-stu-id="c63ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c63ed-108">*size*</span><span class="sxs-lookup"><span data-stu-id="c63ed-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="c63ed-109">可以寫入至 *緩衝區* 的最大值數目。</span><span class="sxs-lookup"><span data-stu-id="c63ed-109">The maximum number of values that can be written into *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="c63ed-110">*type*</span><span class="sxs-lookup"><span data-stu-id="c63ed-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="c63ed-111">符號常數，描述將針對每個頂點傳回的資訊。</span><span class="sxs-lookup"><span data-stu-id="c63ed-111">A symbolic constant that describes the information that will be returned for each vertex.</span></span> <span data-ttu-id="c63ed-112">接受下列符號常數： GL \_ 2d、gl \_ 3D、gl \_ 3D \_ 色彩、gl \_ 3D \_ 色彩 \_ 材質，以及 gl \_ 4d \_ 色彩 \_ 材質。</span><span class="sxs-lookup"><span data-stu-id="c63ed-112">The following symbolic constants are accepted: GL\_2D, GL\_3D, GL\_3D\_COLOR, GL\_3D\_COLOR\_TEXTURE, and GL\_4D\_COLOR\_TEXTURE.</span></span>

</dd> <dt>

<span data-ttu-id="c63ed-113">*緩衝區*</span><span class="sxs-lookup"><span data-stu-id="c63ed-113">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="c63ed-114">傳回意見反應資料。</span><span class="sxs-lookup"><span data-stu-id="c63ed-114">Returns the feedback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c63ed-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c63ed-115">Return value</span></span>

<span data-ttu-id="c63ed-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c63ed-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c63ed-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c63ed-117">Error codes</span></span>

<span data-ttu-id="c63ed-118">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c63ed-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c63ed-119">Name</span><span class="sxs-lookup"><span data-stu-id="c63ed-119">Name</span></span>                                                                                                  | <span data-ttu-id="c63ed-120">意義</span><span class="sxs-lookup"><span data-stu-id="c63ed-120">Meaning</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c63ed-121"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="c63ed-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c63ed-122">*類型* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="c63ed-122">*type* was not an accepted value.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="c63ed-123"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="c63ed-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c63ed-124">*大小* 為負數。</span><span class="sxs-lookup"><span data-stu-id="c63ed-124">*size* was negative.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="c63ed-125"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="c63ed-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c63ed-126">當轉譯模式為 GL 意見反應時呼叫 **glFeedbackBuffer** \_ ，或 [](glrendermode.md)在 \_ 至少呼叫 **glFeedbackBuffer** 一次之前，使用引數 GL 回饋來呼叫 glRenderMode。</span><span class="sxs-lookup"><span data-stu-id="c63ed-126">**glFeedbackBuffer** was called while the render mode was GL\_FEEDBACK, or [**glRenderMode**](glrendermode.md) was called with argument GL\_FEEDBACK before **glFeedbackBuffer** was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="c63ed-127"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="c63ed-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c63ed-128">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="c63ed-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                  |



## <a name="remarks"></a><span data-ttu-id="c63ed-129">備註</span><span class="sxs-lookup"><span data-stu-id="c63ed-129">Remarks</span></span>

<span data-ttu-id="c63ed-130">**GlFeedbackBuffer** 函式會控制意見反應。</span><span class="sxs-lookup"><span data-stu-id="c63ed-130">The **glFeedbackBuffer** function controls feedback.</span></span> <span data-ttu-id="c63ed-131">意見反應（例如選取專案）是 OpenGL 模式。</span><span class="sxs-lookup"><span data-stu-id="c63ed-131">Feedback, like selection, is an OpenGL mode.</span></span> <span data-ttu-id="c63ed-132">您可以透過使用 GL 意見反應來呼叫 [**glRenderMode**](glrendermode.md) 來選取模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c63ed-132">The mode is selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="c63ed-133">當 OpenGL 處於意見反應模式時，柵格化不會產生任何圖元。</span><span class="sxs-lookup"><span data-stu-id="c63ed-133">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="c63ed-134">相反地，會將已進行柵格化之基本資訊的相關資訊，使用 OpenGL 送回至應用程式。</span><span class="sxs-lookup"><span data-stu-id="c63ed-134">Instead, information about primitives that would have been rasterized is fed back to the application using OpenGL.</span></span>

<span data-ttu-id="c63ed-135">**GlFeedbackBuffer** 函數有三個引數：</span><span class="sxs-lookup"><span data-stu-id="c63ed-135">The **glFeedbackBuffer** function has three arguments:</span></span>

-   <span data-ttu-id="c63ed-136">*緩衝區* 是指向放置意見反應資訊之浮點值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="c63ed-136">*buffer* is a pointer to an array of floating-point values into which feedback information is placed.</span></span>
-   <span data-ttu-id="c63ed-137">*大小* 指出陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="c63ed-137">*size* indicates the size of the array.</span></span>
-   <span data-ttu-id="c63ed-138">*類型* 是一個符號常數，描述針對每個頂點回送回的資訊。</span><span class="sxs-lookup"><span data-stu-id="c63ed-138">*type* is a symbolic constant describing the information that is fed back for each vertex.</span></span>

<span data-ttu-id="c63ed-139">您必須藉由呼叫 **glRenderMode** 與引數 GL 意見反應) ，在啟用意見反應模式 (之前發出 **glFeedbackBuffer** \_ 。</span><span class="sxs-lookup"><span data-stu-id="c63ed-139">You must issue **glFeedbackBuffer** before feedback mode is enabled (by calling **glRenderMode** with argument GL\_FEEDBACK).</span></span> <span data-ttu-id="c63ed-140">設定 GL \_ 意見反應但未建立意見緩衝區，或在 OpenGL 處於意見反應模式時呼叫 **glFeedbackBuffer** ，是一項錯誤。</span><span class="sxs-lookup"><span data-stu-id="c63ed-140">Setting GL\_FEEDBACK without establishing the feedback buffer, or calling **glFeedbackBuffer** while OpenGL is in feedback mode, is an error.</span></span>

<span data-ttu-id="c63ed-141">使用 GL 意見反應以外的參數值來呼叫 [**glRenderMode**](glrendermode.md) ，以將 OpenGL 從意見反應模式中取出 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c63ed-141">Take OpenGL out of feedback mode by calling [**glRenderMode**](glrendermode.md) with a parameter value other than GL\_FEEDBACK.</span></span> <span data-ttu-id="c63ed-142">當您在 OpenGL 處於意見反應模式時這麼做時， **glRenderMode** 會傳回回饋陣列中所放置的專案數目。</span><span class="sxs-lookup"><span data-stu-id="c63ed-142">When you do this while OpenGL is in feedback mode, **glRenderMode** returns the number of entries placed in the feedback array.</span></span> <span data-ttu-id="c63ed-143">傳回的值永遠不會超過 *大小*。</span><span class="sxs-lookup"><span data-stu-id="c63ed-143">The returned value never exceeds *size*.</span></span> <span data-ttu-id="c63ed-144">如果意見反應資料所需的空間超過 *緩衝區* 可用的空間， **glRenderMode** 會傳回負數值。</span><span class="sxs-lookup"><span data-stu-id="c63ed-144">If the feedback data required more room than was available in *buffer*, **glRenderMode** returns a negative value.</span></span>

<span data-ttu-id="c63ed-145">在意見反應模式中，每個要進行柵格化的基本物件都會產生一個值區塊，這些值會複製到意見陣列中。</span><span class="sxs-lookup"><span data-stu-id="c63ed-145">While in feedback mode, each primitive that would be rasterized generates a block of values that gets copied into the feedback array.</span></span> <span data-ttu-id="c63ed-146">如果這樣做會導致專案數超過最大值，則 **glFeedbackBuffer** 會部分寫入區塊，以便填滿陣列 (如果所有) 都沒有剩餘的空間，並設定溢位旗標。</span><span class="sxs-lookup"><span data-stu-id="c63ed-146">If doing so would cause the number of entries to exceed the maximum, **glFeedbackBuffer** partially writes the block so as to fill the array (if there is any room left at all), and sets an overflow flag.</span></span> <span data-ttu-id="c63ed-147">每個區塊都會以表示基本類型的程式碼開頭，後面接著描述基本頂點和相關資料的值。</span><span class="sxs-lookup"><span data-stu-id="c63ed-147">Each block begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="c63ed-148">**GlFeedbackBuffer** 函式也會寫入點陣圖和圖元矩形的專案。</span><span class="sxs-lookup"><span data-stu-id="c63ed-148">The **glFeedbackBuffer** function also writes entries for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="c63ed-149">在多邊形剔除和多邊形的 [**glPolygonMode**](glpolygonmode.md) 解釋之後發生意見反應，因此在意見緩衝區中不會傳回挑選的多邊形。</span><span class="sxs-lookup"><span data-stu-id="c63ed-149">Feedback occurs after polygon culling and [**glPolygonMode**](glpolygonmode.md) interpretation of polygons has taken place, so polygons that are culled are not returned in the feedback buffer.</span></span> <span data-ttu-id="c63ed-150">如果 OpenGL 執行會藉由執行此分解來轉譯多邊形，則會將具有三個以上邊緣的多邊形細分為三角形。</span><span class="sxs-lookup"><span data-stu-id="c63ed-150">It can also occur after polygons with more than three edges are broken up into triangles, if the OpenGL implementation renders polygons by performing this decomposition.</span></span>

<span data-ttu-id="c63ed-151">您可以使用 [**glPassThrough**](glpassthrough.md)，在意見緩衝區中插入標記。</span><span class="sxs-lookup"><span data-stu-id="c63ed-151">You can insert a marker into the feedback buffer with [**glPassThrough**](glpassthrough.md).</span></span>

<span data-ttu-id="c63ed-152">以下是寫入意見緩衝區之值區塊的文法。</span><span class="sxs-lookup"><span data-stu-id="c63ed-152">The following is the grammar for the blocks of values written into the feedback buffer.</span></span> <span data-ttu-id="c63ed-153">每個基本類型都會以唯一的識別值來表示，後面接著一些頂點。</span><span class="sxs-lookup"><span data-stu-id="c63ed-153">Each primitive is indicated with a unique identifying value followed by some number of vertices.</span></span> <span data-ttu-id="c63ed-154">多邊形專案包含一個整數值，指出接下來有多少頂點。</span><span class="sxs-lookup"><span data-stu-id="c63ed-154">Polygon entries include an integer value indicating how many vertices follow.</span></span> <span data-ttu-id="c63ed-155">頂點會以數個浮點數值的形式送回（由型別決定 *）。*</span><span class="sxs-lookup"><span data-stu-id="c63ed-155">A vertex is fed back as some number of floating-point values, as determined by *type*.</span></span> <span data-ttu-id="c63ed-156">在 RGBA 模式中，色彩會以四個值的形式送回，而在色彩索引模式中，則會以一個值</span><span class="sxs-lookup"><span data-stu-id="c63ed-156">Colors are fed back as four values in RGBA mode and one value in color-index mode.</span></span>

<span data-ttu-id="c63ed-157">feedbackList < feedbackItem feedbackList \| feedbackItem</span><span class="sxs-lookup"><span data-stu-id="c63ed-157">feedbackList <  feedbackItem feedbackList \| feedbackItem</span></span>

<span data-ttu-id="c63ed-158">feedbackItem < 點 \| lineSegment \| 多邊形 \| 點陣圖 \| pixelRectangle \| passThru</span><span class="sxs-lookup"><span data-stu-id="c63ed-158">feedbackItem <  point \| lineSegment \| polygon \| bitmap \| pixelRectangle \| passThru</span></span>

<span data-ttu-id="c63ed-159">點 < GL \_ 點 \_ 權杖頂點</span><span class="sxs-lookup"><span data-stu-id="c63ed-159">point <  GL\_POINT\_TOKEN vertex</span></span>

<span data-ttu-id="c63ed-160">lineSegment < GL \_ line \_ TOKEN 頂點頂點 \| GL \_ line \_ RESET \_ token 頂點頂點</span><span class="sxs-lookup"><span data-stu-id="c63ed-160">lineSegment <  GL\_LINE\_TOKEN vertex vertex \| GL\_LINE\_RESET\_TOKEN vertex vertex</span></span>

<span data-ttu-id="c63ed-161">多邊形 < GL \_ 多邊形 \_ TOKEN n polySpec</span><span class="sxs-lookup"><span data-stu-id="c63ed-161">polygon <  GL\_POLYGON\_TOKEN n polySpec</span></span>

<span data-ttu-id="c63ed-162">polySpec < \| polySpec 頂點頂點頂點頂點</span><span class="sxs-lookup"><span data-stu-id="c63ed-162">polySpec <  polySpec vertex \| vertex vertex vertex</span></span>

<span data-ttu-id="c63ed-163">< GL \_ 點陣圖 \_ 權杖頂點的點陣圖</span><span class="sxs-lookup"><span data-stu-id="c63ed-163">bitmap <  GL\_BITMAP\_TOKEN vertex</span></span>

<span data-ttu-id="c63ed-164">pixelRectangle < GL \_ DRAW \_ 圖元 \_ token 頂點 \| \_ 複製 \_ 圖元 \_ token 頂點</span><span class="sxs-lookup"><span data-stu-id="c63ed-164">pixelRectangle <  GL\_DRAW\_PIXEL\_TOKEN vertex \| GL\_COPY\_PIXEL\_TOKEN vertex</span></span>

<span data-ttu-id="c63ed-165">passThru < GL \_ \_ 通過 \_ 權杖值</span><span class="sxs-lookup"><span data-stu-id="c63ed-165">passThru <  GL\_PASS\_THROUGH\_TOKEN value</span></span>

<span data-ttu-id="c63ed-166">頂點 < 2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture</span><span class="sxs-lookup"><span data-stu-id="c63ed-166">vertex <  2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture</span></span>

<span data-ttu-id="c63ed-167">2d < 值值</span><span class="sxs-lookup"><span data-stu-id="c63ed-167">2d <  value value</span></span>

<span data-ttu-id="c63ed-168">3d < 值值</span><span class="sxs-lookup"><span data-stu-id="c63ed-168">3d <  value value value</span></span>

<span data-ttu-id="c63ed-169">3dColor < 值的值色彩</span><span class="sxs-lookup"><span data-stu-id="c63ed-169">3dColor <  value value value color</span></span>

<span data-ttu-id="c63ed-170">3dColorTexture < value 值 color tex</span><span class="sxs-lookup"><span data-stu-id="c63ed-170">3dColorTexture <  value value value color tex</span></span>

<span data-ttu-id="c63ed-171">4dColorTexture < value 值 color tex</span><span class="sxs-lookup"><span data-stu-id="c63ed-171">4dColorTexture <  value value value value color tex</span></span>

<span data-ttu-id="c63ed-172">< rgba 索引的色彩 \|</span><span class="sxs-lookup"><span data-stu-id="c63ed-172">color <  rgba \| index</span></span>

<span data-ttu-id="c63ed-173">rgba < 值值值</span><span class="sxs-lookup"><span data-stu-id="c63ed-173">rgba <  value value value value</span></span>

<span data-ttu-id="c63ed-174">索引 < 值</span><span class="sxs-lookup"><span data-stu-id="c63ed-174">index <  value</span></span>

<span data-ttu-id="c63ed-175">tex < value value 值</span><span class="sxs-lookup"><span data-stu-id="c63ed-175">tex <  value value value value</span></span>

<span data-ttu-id="c63ed-176">*Value* 參數是浮點數，而 *n* 是一個浮點整數，可提供多邊形中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="c63ed-176">The *value* parameter is a floating-point number, and *n* is a floating-point integer giving the number of vertices in the polygon.</span></span> <span data-ttu-id="c63ed-177">以下是符號浮點數常數： GL \_ 點 \_ 權杖、gl \_ 線路 \_ 權杖、gl \_ 行 \_ 重設 \_ 權杖、gl \_ 多邊形 \_ 權杖、GL \_ 點陣圖 \_ 權杖、gl \_ 描繪 \_ 圖元 \_ 權杖、gl \_ 複製 \_ 圖元 \_ 權杖，以及 \_ 透過權杖的 gl 傳遞 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="c63ed-177">The following are symbolic floating-point constants: GL\_POINT\_TOKEN, GL\_LINE\_TOKEN, GL\_LINE\_RESET\_TOKEN, GL\_POLYGON\_TOKEN, GL\_BITMAP\_TOKEN, GL\_DRAW\_PIXEL\_TOKEN, GL\_COPY\_PIXEL\_TOKEN, and GL\_PASS\_THROUGH\_TOKEN.</span></span> <span data-ttu-id="c63ed-178">\_ \_ \_ 每當重設 LINE stipple 模式時，就會傳回 GL 行重設權杖。</span><span class="sxs-lookup"><span data-stu-id="c63ed-178">GL\_LINE\_RESET\_TOKEN is returned whenever the line stipple pattern is reset.</span></span> <span data-ttu-id="c63ed-179">以頂點傳回的資料取決於意見反應 *類型*。</span><span class="sxs-lookup"><span data-stu-id="c63ed-179">The data returned as a vertex depends on the feedback *type*.</span></span>

<span data-ttu-id="c63ed-180">下表提供 *類型* 和每個頂點的值數目之間的對應; *k* 在色彩索引模式中為1，而在 RGBA 模式中為4。</span><span class="sxs-lookup"><span data-stu-id="c63ed-180">The following table gives the correspondence between *type* and the number of values per vertex; *k* is 1 in color-index mode and 4 in RGBA mode.</span></span>



| <span data-ttu-id="c63ed-181">類型</span><span class="sxs-lookup"><span data-stu-id="c63ed-181">Type</span></span>                   | <span data-ttu-id="c63ed-182">座標</span><span class="sxs-lookup"><span data-stu-id="c63ed-182">Coordinates</span></span>        | <span data-ttu-id="c63ed-183">Color</span><span class="sxs-lookup"><span data-stu-id="c63ed-183">Color</span></span> | <span data-ttu-id="c63ed-184">紋理</span><span class="sxs-lookup"><span data-stu-id="c63ed-184">Texture</span></span> | <span data-ttu-id="c63ed-185">總值數目</span><span class="sxs-lookup"><span data-stu-id="c63ed-185">Total number of values</span></span> |
|------------------------|--------------------|-------|---------|------------------------|
| <span data-ttu-id="c63ed-186">GL \_ 2d</span><span class="sxs-lookup"><span data-stu-id="c63ed-186">GL\_2D</span></span>                 | <span data-ttu-id="c63ed-187">*x*、 *y*</span><span class="sxs-lookup"><span data-stu-id="c63ed-187">*x*, *y*</span></span>           |       |         | <span data-ttu-id="c63ed-188">2</span><span class="sxs-lookup"><span data-stu-id="c63ed-188">2</span></span>                      |
| <span data-ttu-id="c63ed-189">GL \_ 3d</span><span class="sxs-lookup"><span data-stu-id="c63ed-189">GL\_3D</span></span>                 | <span data-ttu-id="c63ed-190">*x*、 *y*、 *z*</span><span class="sxs-lookup"><span data-stu-id="c63ed-190">*x*, *y*, *z*</span></span>      |       |         | <span data-ttu-id="c63ed-191">3</span><span class="sxs-lookup"><span data-stu-id="c63ed-191">3</span></span>                      |
| <span data-ttu-id="c63ed-192">GL \_ 3d \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="c63ed-192">GL\_3D\_COLOR</span></span>          | <span data-ttu-id="c63ed-193">*x*、 *y*、 *z*</span><span class="sxs-lookup"><span data-stu-id="c63ed-193">*x*, *y*, *z*</span></span>      | <span data-ttu-id="c63ed-194">*K*</span><span class="sxs-lookup"><span data-stu-id="c63ed-194">*k*</span></span>   |         | <span data-ttu-id="c63ed-195">3 + *k*</span><span class="sxs-lookup"><span data-stu-id="c63ed-195">3 + *k*</span></span>                |
| <span data-ttu-id="c63ed-196">GL \_ 3d \_ 色彩 \_ 材質</span><span class="sxs-lookup"><span data-stu-id="c63ed-196">GL\_3D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="c63ed-197">*x*、 *y*、 *z*、</span><span class="sxs-lookup"><span data-stu-id="c63ed-197">*x*, *y*, *z*,</span></span>     | <span data-ttu-id="c63ed-198">*K*</span><span class="sxs-lookup"><span data-stu-id="c63ed-198">*k*</span></span>   | <span data-ttu-id="c63ed-199">4</span><span class="sxs-lookup"><span data-stu-id="c63ed-199">4</span></span>       | <span data-ttu-id="c63ed-200">7 + *k*</span><span class="sxs-lookup"><span data-stu-id="c63ed-200">7 + *k*</span></span>                |
| <span data-ttu-id="c63ed-201">GL \_ 4d \_ 色彩 \_ 材質</span><span class="sxs-lookup"><span data-stu-id="c63ed-201">GL\_4D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="c63ed-202">*x*、 *y*、 *z*、 *w*</span><span class="sxs-lookup"><span data-stu-id="c63ed-202">*x*, *y*, *z*, *w*</span></span> | <span data-ttu-id="c63ed-203">*K*</span><span class="sxs-lookup"><span data-stu-id="c63ed-203">*k*</span></span>   | <span data-ttu-id="c63ed-204">4</span><span class="sxs-lookup"><span data-stu-id="c63ed-204">4</span></span>       | <span data-ttu-id="c63ed-205">8 + *k*</span><span class="sxs-lookup"><span data-stu-id="c63ed-205">8 + *k*</span></span>                |



 

<span data-ttu-id="c63ed-206">意見反應頂點座標是在視窗座標中，但 *w* 除外，其為裁剪座標。</span><span class="sxs-lookup"><span data-stu-id="c63ed-206">Feedback vertex coordinates are in window coordinates, except *w*, which is in clip coordinates.</span></span> <span data-ttu-id="c63ed-207">如果已啟用光源，則意見反應色彩會是淺色。</span><span class="sxs-lookup"><span data-stu-id="c63ed-207">Feedback colors are lighted, if lighting is enabled.</span></span> <span data-ttu-id="c63ed-208">如果已啟用材質座標產生，則會產生意見紋理座標。</span><span class="sxs-lookup"><span data-stu-id="c63ed-208">Feedback texture coordinates are generated, if texture coordinate generation is enabled.</span></span> <span data-ttu-id="c63ed-209">材質矩陣一律會轉換它們。</span><span class="sxs-lookup"><span data-stu-id="c63ed-209">They are always transformed by the texture matrix.</span></span>

<span data-ttu-id="c63ed-210">在顯示清單中使用 **glFeedbackBuffer** 函式時，不會編譯到顯示清單中，而是會立即執行。</span><span class="sxs-lookup"><span data-stu-id="c63ed-210">The **glFeedbackBuffer** function, when used in a display list, is not compiled into the display list but rather is executed immediately.</span></span>

<span data-ttu-id="c63ed-211">下列函式會抓取 **glFeedbackBuffer** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="c63ed-211">The following function retrieves information related to **glFeedbackBuffer**:</span></span>

<span data-ttu-id="c63ed-212">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 轉譯 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="c63ed-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="c63ed-213">規格需求</span><span class="sxs-lookup"><span data-stu-id="c63ed-213">Requirements</span></span>



| <span data-ttu-id="c63ed-214">需求</span><span class="sxs-lookup"><span data-stu-id="c63ed-214">Requirement</span></span> | <span data-ttu-id="c63ed-215">值</span><span class="sxs-lookup"><span data-stu-id="c63ed-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c63ed-216">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c63ed-216">Minimum supported client</span></span><br/> | <span data-ttu-id="c63ed-217">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c63ed-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c63ed-218">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c63ed-218">Minimum supported server</span></span><br/> | <span data-ttu-id="c63ed-219">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c63ed-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c63ed-220">標頭</span><span class="sxs-lookup"><span data-stu-id="c63ed-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="c63ed-221"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="c63ed-221"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c63ed-222">程式庫</span><span class="sxs-lookup"><span data-stu-id="c63ed-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="c63ed-223"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c63ed-223"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c63ed-224">DLL</span><span class="sxs-lookup"><span data-stu-id="c63ed-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c63ed-225"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c63ed-225"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c63ed-226">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c63ed-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c63ed-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c63ed-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c63ed-228">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c63ed-228">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c63ed-229">**glGet**</span><span class="sxs-lookup"><span data-stu-id="c63ed-229">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="c63ed-230">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="c63ed-230">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="c63ed-231">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="c63ed-231">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="c63ed-232">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="c63ed-232">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="c63ed-233">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="c63ed-233">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="c63ed-234">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="c63ed-234">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





