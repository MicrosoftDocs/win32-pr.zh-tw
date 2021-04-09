---
title: 'glLightModelf 函式 (Gl) '
description: GlLightModelf 函式會設定光源模型參數。
ms.assetid: 7002c157-514e-4102-93f7-21a0df97a5c2
keywords:
- glLightModelf 函式 OpenGL
topic_type:
- apiref
api_name:
- glLightModelf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2c17f7dc82080544a9055805cf62726227c200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024618"
---
# <a name="gllightmodelf-function"></a><span data-ttu-id="9c50e-104">glLightModelf 函式</span><span class="sxs-lookup"><span data-stu-id="9c50e-104">glLightModelf function</span></span>

<span data-ttu-id="9c50e-105">**GlLightModelf** 函式會設定光源模型參數。</span><span class="sxs-lookup"><span data-stu-id="9c50e-105">The **glLightModelf** function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c50e-106">語法</span><span class="sxs-lookup"><span data-stu-id="9c50e-106">Syntax</span></span>


```C++
void WINAPI glLightModelf(
   GLenum  pname,
   GLfloat *param
);
```



## <a name="parameters"></a><span data-ttu-id="9c50e-107">參數</span><span class="sxs-lookup"><span data-stu-id="9c50e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c50e-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="9c50e-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="9c50e-109">單一值光源模型參數。</span><span class="sxs-lookup"><span data-stu-id="9c50e-109">A single-valued lighting model parameter.</span></span> <span data-ttu-id="9c50e-110">接受下列值。</span><span class="sxs-lookup"><span data-stu-id="9c50e-110">The following values are accepted.</span></span>



| <span data-ttu-id="9c50e-111">值</span><span class="sxs-lookup"><span data-stu-id="9c50e-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="9c50e-112">意義</span><span class="sxs-lookup"><span data-stu-id="9c50e-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="9c50e-113"><dt>**GL \_ 光 \_ 模型 \_ 本機 \_ 檢視器**</dt></span><span class="sxs-lookup"><span data-stu-id="9c50e-113"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="9c50e-114">*Param* 參數是單一浮點值，可指定反射反射角度的計算方式。</span><span class="sxs-lookup"><span data-stu-id="9c50e-114">The *param* parameter is a single floating-point value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="9c50e-115">如果 *param* 為 0 (或 0.0) ，反射反映角度會讓視圖方向與-Z 軸的方向平行，並在-*z* 軸的方向中，不論頂點的位置是以眼睛座標為單位。</span><span class="sxs-lookup"><span data-stu-id="9c50e-115">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="9c50e-116">否則，就會從眼睛座標系統的原點計算反射反射。</span><span class="sxs-lookup"><span data-stu-id="9c50e-116">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="9c50e-117">預設值是 0。</span><span class="sxs-lookup"><span data-stu-id="9c50e-117">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="9c50e-118"><dt>**GL \_ 燈 \_ 模型 \_ 二 \_ 邊**</dt></span><span class="sxs-lookup"><span data-stu-id="9c50e-118"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="9c50e-119">*Param* 參數是單一浮點值，可指定多邊形是否已完成單面或雙面光源計算。</span><span class="sxs-lookup"><span data-stu-id="9c50e-119">The *param* parameter is a single floating-point value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="9c50e-120">它不會影響點、線條或點陣圖的光源計算。</span><span class="sxs-lookup"><span data-stu-id="9c50e-120">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="9c50e-121">如果 *param* 為 0 (或 0.0) ，則會指定單面光源，而且只會在光源方程式中使用 front 材質參數。</span><span class="sxs-lookup"><span data-stu-id="9c50e-121">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="9c50e-122">否則，就會指定雙面光源。</span><span class="sxs-lookup"><span data-stu-id="9c50e-122">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="9c50e-123">在這種情況下，會使用後端材質參數將背面的多邊形頂點燈亮，並在評估光源之前，先將其法線反轉。</span><span class="sxs-lookup"><span data-stu-id="9c50e-123">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="9c50e-124">正面多邊形的頂點一律會使用 front 材質參數，而不會變更其法線。</span><span class="sxs-lookup"><span data-stu-id="9c50e-124">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="9c50e-125">預設值是 0。</span><span class="sxs-lookup"><span data-stu-id="9c50e-125">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9c50e-126">*param*</span><span class="sxs-lookup"><span data-stu-id="9c50e-126">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="9c50e-127">將設定 *參數* 的值。</span><span class="sxs-lookup"><span data-stu-id="9c50e-127">The value to which *param* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c50e-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c50e-128">Return value</span></span>

<span data-ttu-id="9c50e-129">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9c50e-129">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9c50e-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9c50e-130">Error codes</span></span>

<span data-ttu-id="9c50e-131">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9c50e-131">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9c50e-132">Name</span><span class="sxs-lookup"><span data-stu-id="9c50e-132">Name</span></span>                                                                                                  | <span data-ttu-id="9c50e-133">意義</span><span class="sxs-lookup"><span data-stu-id="9c50e-133">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c50e-134"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="9c50e-134"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9c50e-135">*pname* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="9c50e-135">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="9c50e-136"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="9c50e-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9c50e-137">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="9c50e-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9c50e-138">備註</span><span class="sxs-lookup"><span data-stu-id="9c50e-138">Remarks</span></span>

<span data-ttu-id="9c50e-139">**GlLightModelf** 函數會設定光源模型參數。</span><span class="sxs-lookup"><span data-stu-id="9c50e-139">The **glLightModelf** function sets lighting model parameter.</span></span> <span data-ttu-id="9c50e-140">*Pname* 參數會為參數命名，而 *param* 會提供新值。個別光源參數的值或值。</span><span class="sxs-lookup"><span data-stu-id="9c50e-140">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="9c50e-141">在 RGBA 模式中，頂點的燈光色彩是材質排放強度的總和、材質環境反射率的乘積以及光線模型的全場景環境濃度，以及每個已啟用光源的比重。</span><span class="sxs-lookup"><span data-stu-id="9c50e-141">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="9c50e-142">每個燈光來源都有三個詞彙的總和：環境、擴散和反射。</span><span class="sxs-lookup"><span data-stu-id="9c50e-142">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="9c50e-143">環境光源的比重是材質環境反射率和光線環境濃度的乘積。</span><span class="sxs-lookup"><span data-stu-id="9c50e-143">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="9c50e-144">擴散光源的比重是材質的材質反射率、光線的擴散濃度，以及頂點的標準向量（從頂點到光源）的點乘積乘積。</span><span class="sxs-lookup"><span data-stu-id="9c50e-144">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="9c50e-145">反射光源的比重是材質反射反射率的乘積、光線的反射濃度，以及正規化頂點對眼睛和頂點對光線向量的點乘積，並提升為材質的反光能力。</span><span class="sxs-lookup"><span data-stu-id="9c50e-145">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="9c50e-146">所有三個光源的貢獻都會根據從頂點到光源的距離，以及光源方向、分佈指數和分佈截止角度，平均衰減。</span><span class="sxs-lookup"><span data-stu-id="9c50e-146">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="9c50e-147">如果所有的點乘積都評估為負值，則會以零取代。</span><span class="sxs-lookup"><span data-stu-id="9c50e-147">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="9c50e-148">產生之淺色色彩的 Alpha 元件會設定為材質漫射反射率的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="9c50e-148">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="9c50e-149">在色彩索引模式中，頂點的淺色索引值範圍從環境到使用 GL 色彩索引傳遞給 [**glMaterial**](glmaterial-functions.md) 的反射值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="9c50e-149">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="9c50e-150">擴散和反射係數，以 ( .30、59、.11) 加權的色彩、材質的反光、以及與 RGBA 案例相同的反映和衰減方程式來計算，以判斷產生的索引在環境上的程度。</span><span class="sxs-lookup"><span data-stu-id="9c50e-150">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="9c50e-151">下列函式會取出與 **glLightModelf** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="9c50e-151">The following functions retrieve information related to the **glLightModelf** function:</span></span>

<span data-ttu-id="9c50e-152">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 光 \_ 模型 \_ 本機 \_ 檢視器的 glGet</span><span class="sxs-lookup"><span data-stu-id="9c50e-152">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="9c50e-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 淺色 \_ 模型 \_ 二 \_ 邊</span><span class="sxs-lookup"><span data-stu-id="9c50e-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="9c50e-154">[](glisenabled.md)具有引數 GL \_ 光源的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="9c50e-154">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="9c50e-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c50e-155">Requirements</span></span>



| <span data-ttu-id="9c50e-156">需求</span><span class="sxs-lookup"><span data-stu-id="9c50e-156">Requirement</span></span> | <span data-ttu-id="9c50e-157">值</span><span class="sxs-lookup"><span data-stu-id="9c50e-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c50e-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c50e-158">Minimum supported client</span></span><br/> | <span data-ttu-id="9c50e-159">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c50e-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9c50e-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c50e-160">Minimum supported server</span></span><br/> | <span data-ttu-id="9c50e-161">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c50e-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9c50e-162">標頭</span><span class="sxs-lookup"><span data-stu-id="9c50e-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c50e-163"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="9c50e-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9c50e-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="9c50e-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c50e-165"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c50e-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9c50e-166">DLL</span><span class="sxs-lookup"><span data-stu-id="9c50e-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c50e-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c50e-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c50e-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c50e-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c50e-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9c50e-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9c50e-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9c50e-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9c50e-171">**glLight**</span><span class="sxs-lookup"><span data-stu-id="9c50e-171">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="9c50e-172">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="9c50e-172">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





