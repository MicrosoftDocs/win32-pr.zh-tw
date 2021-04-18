---
title: 'glMaterialiv 函式 (Gl) '
description: GlMaterialiv 函數會指定光源模型的材質參數。
ms.assetid: 9d045202-e565-4cf7-946a-60299e1bc1b1
keywords:
- glMaterialfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95f12a5d34357a3436ffd6725ad2f1d56901e700
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384466"
---
# <a name="glmaterialiv-function"></a><span data-ttu-id="4cb68-104">glMaterialiv 函式</span><span class="sxs-lookup"><span data-stu-id="4cb68-104">glMaterialiv function</span></span>

<span data-ttu-id="4cb68-105">**GlMaterialiv** 函數會指定光源模型的材質參數。</span><span class="sxs-lookup"><span data-stu-id="4cb68-105">The **glMaterialiv** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb68-106">語法</span><span class="sxs-lookup"><span data-stu-id="4cb68-106">Syntax</span></span>


```C++
void WINAPI glMaterialfv(
         GLenum face,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="4cb68-107">參數</span><span class="sxs-lookup"><span data-stu-id="4cb68-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb68-108">*臉*</span><span class="sxs-lookup"><span data-stu-id="4cb68-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="4cb68-109">正在更新的臉部或臉部。</span><span class="sxs-lookup"><span data-stu-id="4cb68-109">The face or faces that are being updated.</span></span> <span data-ttu-id="4cb68-110">必須是下列其中一項： GL \_ front、gl \_ BACK 或 gl \_ front 和 gl \_ 回來。</span><span class="sxs-lookup"><span data-stu-id="4cb68-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="4cb68-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="4cb68-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="4cb68-112">要更新之臉部或臉部的材質參數。</span><span class="sxs-lookup"><span data-stu-id="4cb68-112">The material parameter of the face or faces being updated.</span></span> <span data-ttu-id="4cb68-113">您可以使用 [**glMaterialiv**](glmaterialfv.md)來指定參數，並以光源方程式進行解讀，如下所示。</span><span class="sxs-lookup"><span data-stu-id="4cb68-113">The parameters that can be specified using [**glMaterialiv**](glmaterialfv.md), and their interpretations by the lighting equation, are as follows.</span></span>



| <span data-ttu-id="4cb68-114">值</span><span class="sxs-lookup"><span data-stu-id="4cb68-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="4cb68-115">意義</span><span class="sxs-lookup"><span data-stu-id="4cb68-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="4cb68-116"><dt>**GL \_ 環境**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-116"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                                       | <span data-ttu-id="4cb68-117">Params 參數包含四個整數值，可指定材質的環境 RGBA 反射率。</span><span class="sxs-lookup"><span data-stu-id="4cb68-117">The params parameter contains four integer values that specify the ambient RGBA reflectance of the material.</span></span> <span data-ttu-id="4cb68-118">整數值會以線性方式對應，因此最正面的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="4cb68-118">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="4cb68-119">浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="4cb68-119">Floating-point values are mapped directly.</span></span> <span data-ttu-id="4cb68-120">整數和浮點值都不是壓制。</span><span class="sxs-lookup"><span data-stu-id="4cb68-120">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="4cb68-121">適用于 front 和後端材質的預設環境反射率是 (0.2、0.2、0.2、1.0) 。</span><span class="sxs-lookup"><span data-stu-id="4cb68-121">The default ambient reflectance for both front-facing and back-facing materials is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="4cb68-122"><dt>**GL \_ 擴散**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-122"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="4cb68-123">Params 參數包含四個整數值，可指定材質的擴散 RGBA 反射率。</span><span class="sxs-lookup"><span data-stu-id="4cb68-123">The params parameter contains four integer values that specify the diffuse RGBA reflectance of the material.</span></span> <span data-ttu-id="4cb68-124">整數值會以線性方式對應，因此最正面的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="4cb68-124">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="4cb68-125">浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="4cb68-125">Floating-point values are mapped directly.</span></span> <span data-ttu-id="4cb68-126">整數和浮點值都不是壓制。</span><span class="sxs-lookup"><span data-stu-id="4cb68-126">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="4cb68-127">適用于 front 和後端材質的預設擴散反射率是 (0.8、0.8、0.8、1.0) 。</span><span class="sxs-lookup"><span data-stu-id="4cb68-127">The default diffuse reflectance for both front-facing and back-facing materials is (0.8, 0.8, 0.8, 1.0).</span></span> <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="4cb68-128"><dt>**GL \_ 反射**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-128"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                                    | <span data-ttu-id="4cb68-129">Params 參數包含四個整數值，可指定材質的反射 RGBA 反射率。</span><span class="sxs-lookup"><span data-stu-id="4cb68-129">The params parameter contains four integer values that specify the specular RGBA reflectance of the material.</span></span> <span data-ttu-id="4cb68-130">整數值會以線性方式對應，因此最正面的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="4cb68-130">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="4cb68-131">浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="4cb68-131">Floating-point values are mapped directly.</span></span> <span data-ttu-id="4cb68-132">整數和浮點值都不是壓制。</span><span class="sxs-lookup"><span data-stu-id="4cb68-132">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="4cb68-133">適用于 front 和後端材質的預設反射反射率是 (0.0、0.0、0.0、1.0) 。</span><span class="sxs-lookup"><span data-stu-id="4cb68-133">The default specular reflectance for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="4cb68-134"><dt>**GL \_ 排放**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-134"><dt>**GL\_EMISSION**</dt></span></span> </dl>                                    | <span data-ttu-id="4cb68-135">Params 參數包含四個整數值，可指定針對材質發出的 RGBA 濃度。</span><span class="sxs-lookup"><span data-stu-id="4cb68-135">The params parameter contains four integer values that specify the RGBA emitted light intensity of the material.</span></span> <span data-ttu-id="4cb68-136">整數值會以線性方式對應，因此最正面的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="4cb68-136">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="4cb68-137">浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="4cb68-137">Floating-point values are mapped directly.</span></span> <span data-ttu-id="4cb68-138">整數和浮點值都不是壓制。</span><span class="sxs-lookup"><span data-stu-id="4cb68-138">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="4cb68-139">正面和後端材質的預設發射濃度是 (0.0、0.0、0.0、1.0) 。</span><span class="sxs-lookup"><span data-stu-id="4cb68-139">The default emission intensity for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="4cb68-140"><dt>**GL \_ 反光**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-140"><dt>**GL\_SHININESS**</dt></span></span> </dl>                                 | <span data-ttu-id="4cb68-141">*Param* 參數是單一整數，可指定材質的 RGBA 反射指數。</span><span class="sxs-lookup"><span data-stu-id="4cb68-141">The *param* parameter is a single integer that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="4cb68-142">整數值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="4cb68-142">Integer values are mapped directly.</span></span> <span data-ttu-id="4cb68-143">只 \[ 接受範圍0，128中的值 \] 。</span><span class="sxs-lookup"><span data-stu-id="4cb68-143">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="4cb68-144">正面和背面材質的預設反射指數為0。</span><span class="sxs-lookup"><span data-stu-id="4cb68-144">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/>                                                                                                                                                                                                     |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <span data-ttu-id="4cb68-145"><dt>**GL \_ 環境 \_ 和 \_ 擴散**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-145"><dt>**GL\_AMBIENT\_AND\_DIFFUSE**</dt></span></span> </dl> | <span data-ttu-id="4cb68-146">相當於使用相同的參數值呼叫 [**glMaterial**](glmaterial-functions.md) 兩次，一次使用 gl \_ 環境，一次使用 gl \_ 擴散。</span><span class="sxs-lookup"><span data-stu-id="4cb68-146">Equivalent to calling [**glMaterial**](glmaterial-functions.md) twice with the same parameter values, once with GL\_AMBIENT and once with GL\_DIFFUSE.</span></span> <br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="4cb68-147"><dt>**GL \_ 色彩 \_ 索引**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-147"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl>                    | <span data-ttu-id="4cb68-148">Params 參數包含三個整數值，可指定環境、擴散和反射光源的色彩索引。</span><span class="sxs-lookup"><span data-stu-id="4cb68-148">The params parameter contains three integer values specifying the color indexes for ambient, diffuse, and specular lighting.</span></span> <span data-ttu-id="4cb68-149">這三個值，以及 GL \_ 反光，是色彩索引模式光源方程式所使用的唯一材質值。</span><span class="sxs-lookup"><span data-stu-id="4cb68-149">These three values, and GL\_SHININESS, are the only material values used by the color-index mode lighting equation.</span></span> <span data-ttu-id="4cb68-150">如需色彩索引光源的討論，請參閱 [**glLightModel**](gllightmodel-functions.md) 。</span><span class="sxs-lookup"><span data-stu-id="4cb68-150">Refer to [**glLightModel**](gllightmodel-functions.md) for a discussion of color-index lighting.</span></span><br/>                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="4cb68-151">*params*</span><span class="sxs-lookup"><span data-stu-id="4cb68-151">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="4cb68-152">將設定參數 GL 反光的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4cb68-152">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb68-153">傳回值</span><span class="sxs-lookup"><span data-stu-id="4cb68-153">Return value</span></span>

<span data-ttu-id="4cb68-154">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4cb68-154">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4cb68-155">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4cb68-155">Error codes</span></span>

<span data-ttu-id="4cb68-156">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4cb68-156">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4cb68-157">Name</span><span class="sxs-lookup"><span data-stu-id="4cb68-157">Name</span></span>                                                                                              | <span data-ttu-id="4cb68-158">意義</span><span class="sxs-lookup"><span data-stu-id="4cb68-158">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4cb68-159"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-159"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="4cb68-160">*臉部* 或 *pname* 都不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="4cb68-160">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="4cb68-161"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-161"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="4cb68-162">\[已指定0、128範圍以外的反射指數 \] 。</span><span class="sxs-lookup"><span data-stu-id="4cb68-162">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4cb68-163">備註</span><span class="sxs-lookup"><span data-stu-id="4cb68-163">Remarks</span></span>

<span data-ttu-id="4cb68-164">[**GlMaterialiv**](glmaterialf.md)函式會將值指派給材質參數。</span><span class="sxs-lookup"><span data-stu-id="4cb68-164">The [**glMaterialiv**](glmaterialf.md) function assigns values to material parameters.</span></span> <span data-ttu-id="4cb68-165">有兩組相符的材質參數。</span><span class="sxs-lookup"><span data-stu-id="4cb68-165">There are two matched sets of material parameters.</span></span> <span data-ttu-id="4cb68-166">其中一個是 *front* 的集合，用來將點、線條、點陣圖和所有多邊形 (在停用雙面光源時，) ，或只是在) 啟用雙面光源 (時的多邊形。</span><span class="sxs-lookup"><span data-stu-id="4cb68-166">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="4cb68-167">另一組 [ *回溯*] 則是在啟用雙面光源的情況下，用來為向下多邊形加上陰影。</span><span class="sxs-lookup"><span data-stu-id="4cb68-167">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="4cb68-168">如需單面和雙面光源計算的詳細資料，請參閱 [**glLightModel**](gllightmodel-functions.md) 。</span><span class="sxs-lookup"><span data-stu-id="4cb68-168">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="4cb68-169">[**GlMaterialiv**](glmaterialf.md)函式會採用三個引數。</span><span class="sxs-lookup"><span data-stu-id="4cb68-169">The [**glMaterialiv**](glmaterialf.md) function takes three arguments.</span></span> <span data-ttu-id="4cb68-170">第一個是 *臉部*，指定是否 \_ 要修改 gl FRONT 教材、gl \_ 回材料，或 gl \_ 正面 \_ 和 \_ 背面材質。</span><span class="sxs-lookup"><span data-stu-id="4cb68-170">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="4cb68-171">第二個 *pname*，則會指定一或兩個集合中的哪一個參數將會被修改。</span><span class="sxs-lookup"><span data-stu-id="4cb68-171">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="4cb68-172">第三個 *參數* 會指定將指派給指定參數的值。</span><span class="sxs-lookup"><span data-stu-id="4cb68-172">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="4cb68-173">材質參數用於光源方程式，可選擇性地套用至每個頂點。</span><span class="sxs-lookup"><span data-stu-id="4cb68-173">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="4cb68-174">此方程式會在 [**glLightModel**](gllightmodel-functions.md)中討論。</span><span class="sxs-lookup"><span data-stu-id="4cb68-174">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="4cb68-175">您可以隨時更新材質參數。</span><span class="sxs-lookup"><span data-stu-id="4cb68-175">The material parameters can be updated at any time.</span></span> <span data-ttu-id="4cb68-176">尤其是，在呼叫 [**glBegin**](glbegin.md)和對應的 [**glEnd**](glend.md)呼叫之間，可以呼叫 [**glMaterialiv**](glmaterialf.md) 。</span><span class="sxs-lookup"><span data-stu-id="4cb68-176">In particular, [**glMaterialiv**](glmaterialf.md) can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="4cb68-177">不過，如果每個頂點只會變更單一材質參數，則 [**glColorMaterial**](glcolormaterial.md) 優先于 **glMaterialiv**。</span><span class="sxs-lookup"><span data-stu-id="4cb68-177">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMaterialiv**.</span></span>

<span data-ttu-id="4cb68-178">下列函式會抓取 [**glMaterialiv**](glmaterialf.md)的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="4cb68-178">The following function retrieves information related to [**glMaterialiv**](glmaterialf.md):</span></span>

[<span data-ttu-id="4cb68-179">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="4cb68-179">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="4cb68-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cb68-180">Requirements</span></span>



| <span data-ttu-id="4cb68-181">需求</span><span class="sxs-lookup"><span data-stu-id="4cb68-181">Requirement</span></span> | <span data-ttu-id="4cb68-182">值</span><span class="sxs-lookup"><span data-stu-id="4cb68-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb68-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4cb68-183">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb68-184">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cb68-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4cb68-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4cb68-185">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb68-186">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cb68-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4cb68-187">標頭</span><span class="sxs-lookup"><span data-stu-id="4cb68-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cb68-188"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-188"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4cb68-189">程式庫</span><span class="sxs-lookup"><span data-stu-id="4cb68-189">Library</span></span><br/>                  | <dl> <span data-ttu-id="4cb68-190"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-190"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4cb68-191">DLL</span><span class="sxs-lookup"><span data-stu-id="4cb68-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cb68-192"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cb68-192"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cb68-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cb68-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb68-194">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="4cb68-194">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="4cb68-195">**glLight**</span><span class="sxs-lookup"><span data-stu-id="4cb68-195">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="4cb68-196">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="4cb68-196">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





