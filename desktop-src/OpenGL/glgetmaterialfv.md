---
title: 'glGetMaterialfv 函式 (Gl) '
description: 'GlGetMaterialfv 和 glGetMaterialiv 函數會傳回材質參數。 |glGetMaterialfv 函式 (Gl) '
ms.assetid: b61dbe0c-5cc2-4397-9d7c-b99507a9f037
keywords:
- glGetMaterialfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce33ee1f88d492f67cf3ebb93c575f8f36d1ffa0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321988"
---
# <a name="glgetmaterialfv-function"></a><span data-ttu-id="435dd-105">glGetMaterialfv 函式</span><span class="sxs-lookup"><span data-stu-id="435dd-105">glGetMaterialfv function</span></span>

<span data-ttu-id="435dd-106">**GlGetMaterialfv** 和 [**glGetMaterialiv**](glgetmaterialiv.md)函數會傳回材質參數。</span><span class="sxs-lookup"><span data-stu-id="435dd-106">The **glGetMaterialfv** and [**glGetMaterialiv**](glgetmaterialiv.md) functions return material parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="435dd-107">語法</span><span class="sxs-lookup"><span data-stu-id="435dd-107">Syntax</span></span>


```C++
void WINAPI glGetMaterialfv(
   GLenum  face,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="435dd-108">參數</span><span class="sxs-lookup"><span data-stu-id="435dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="435dd-109">*臉*</span><span class="sxs-lookup"><span data-stu-id="435dd-109">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="435dd-110">指定要查詢的兩個材質中的哪一個。</span><span class="sxs-lookup"><span data-stu-id="435dd-110">Specifies which of the two materials is being queried.</span></span> <span data-ttu-id="435dd-111">\_已接受 GL 前或 gl \_ 回，分別代表 front 和 BACK 教材。</span><span class="sxs-lookup"><span data-stu-id="435dd-111">GL\_FRONT or GL\_BACK are accepted, representing the front and back materials, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="435dd-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="435dd-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="435dd-113">要傳回的材質參數。</span><span class="sxs-lookup"><span data-stu-id="435dd-113">The material parameter to return.</span></span> <span data-ttu-id="435dd-114">接受下列值。</span><span class="sxs-lookup"><span data-stu-id="435dd-114">The following values are accepted.</span></span>



| <span data-ttu-id="435dd-115">值</span><span class="sxs-lookup"><span data-stu-id="435dd-115">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="435dd-116">意義</span><span class="sxs-lookup"><span data-stu-id="435dd-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="435dd-117"><dt>**GL \_ 環境**</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-117"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                    | <span data-ttu-id="435dd-118">*Params* 參數會傳回四個整數或浮點值，代表材質的環境反射率。</span><span class="sxs-lookup"><span data-stu-id="435dd-118">The *params* parameter returns four integer or floating-point values representing the ambient reflectance of the material.</span></span> <span data-ttu-id="435dd-119">在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。</span><span class="sxs-lookup"><span data-stu-id="435dd-119">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="435dd-120">如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。</span><span class="sxs-lookup"><span data-stu-id="435dd-120">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="435dd-121"><dt>**GL \_ 擴散**</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-121"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                    | <span data-ttu-id="435dd-122">*Params* 參數會傳回四個整數或浮點值，代表材質的擴散反射率。</span><span class="sxs-lookup"><span data-stu-id="435dd-122">The *params* parameter returns four integer or floating-point values representing the diffuse reflectance of the material.</span></span> <span data-ttu-id="435dd-123">在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。</span><span class="sxs-lookup"><span data-stu-id="435dd-123">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="435dd-124">如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。</span><span class="sxs-lookup"><span data-stu-id="435dd-124">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="435dd-125"><dt>**GL \_ 反射**</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-125"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                 | <span data-ttu-id="435dd-126">*Params* 參數會傳回四個整數或浮點值，代表材質的反射反射率。</span><span class="sxs-lookup"><span data-stu-id="435dd-126">The *params* parameter returns four integer or floating-point values representing the specular reflectance of the material.</span></span> <span data-ttu-id="435dd-127">在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。</span><span class="sxs-lookup"><span data-stu-id="435dd-127">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="435dd-128">如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。</span><span class="sxs-lookup"><span data-stu-id="435dd-128">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="435dd-129"><dt>**GL \_ 排放**</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-129"><dt>**GL\_EMISSION**</dt></span></span> </dl>                 | <span data-ttu-id="435dd-130">*Params* 參數會傳回四個整數或浮點值，代表所發出之材質的亮度。</span><span class="sxs-lookup"><span data-stu-id="435dd-130">The *params* parameter returns four integer or floating-point values representing the emitted light intensity of the material.</span></span> <span data-ttu-id="435dd-131">在要求時，整數值會以線性方式從內部浮點表示對應，因此，1.0 對應到最大的可表示整數值，而-1.0 則對應至最大的可表示整數值。</span><span class="sxs-lookup"><span data-stu-id="435dd-131">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="435dd-132">如果內部值超出範圍 \[ -1、1 \] ，則對應的整數傳回值為未定義。</span><span class="sxs-lookup"><span data-stu-id="435dd-132">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="435dd-133"><dt>**GL \_ 反光**</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-133"><dt>**GL\_SHININESS**</dt></span></span> </dl>              | <span data-ttu-id="435dd-134">*Params* 參數會傳回代表材質反射指數的一個整數或浮點值。</span><span class="sxs-lookup"><span data-stu-id="435dd-134">The *params* parameter returns one integer or floating-point value representing the specular exponent of the material.</span></span> <span data-ttu-id="435dd-135">在要求時，整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。</span><span class="sxs-lookup"><span data-stu-id="435dd-135">Integer values, when requested, are computed by rounding the internal floating-point value to the nearest integer value.</span></span><br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="435dd-136"><dt>**GL \_ 色彩 \_ 索引**</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-136"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl> | <span data-ttu-id="435dd-137">*Params* 參數會傳回三個整數或浮點值，代表材質的環境、擴散和反射索引。</span><span class="sxs-lookup"><span data-stu-id="435dd-137">The *params* parameter returns three integer or floating-point values representing the ambient, diffuse, and specular indexes of the material.</span></span> <span data-ttu-id="435dd-138">這些索引只能用於色彩索引光源。</span><span class="sxs-lookup"><span data-stu-id="435dd-138">Use these indexes only for color-index lighting.</span></span> <span data-ttu-id="435dd-139"> (其他參數都只用于 RGBA 光源。在要求時，) 整數值會藉由將內部浮點值四捨五入為最接近的整數值來計算。</span><span class="sxs-lookup"><span data-stu-id="435dd-139">(The other parameters are all used only for RGBA lighting.) Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                            |



 

</dd> <dt>

<span data-ttu-id="435dd-140">*params*</span><span class="sxs-lookup"><span data-stu-id="435dd-140">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="435dd-141">傳回要求的資料。</span><span class="sxs-lookup"><span data-stu-id="435dd-141">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="435dd-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="435dd-142">Return value</span></span>

<span data-ttu-id="435dd-143">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="435dd-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="435dd-144">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="435dd-144">Error codes</span></span>

<span data-ttu-id="435dd-145">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="435dd-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="435dd-146">Name</span><span class="sxs-lookup"><span data-stu-id="435dd-146">Name</span></span>                                                                                                  | <span data-ttu-id="435dd-147">意義</span><span class="sxs-lookup"><span data-stu-id="435dd-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="435dd-148"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="435dd-149">*目標* 或 *查詢* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="435dd-149">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="435dd-150"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="435dd-151">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="435dd-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="435dd-152">備註</span><span class="sxs-lookup"><span data-stu-id="435dd-152">Remarks</span></span>

<span data-ttu-id="435dd-153">**GlGetMaterial** 函式會以 *params* *傳回材質的* 參數 *pname* 值或值。</span><span class="sxs-lookup"><span data-stu-id="435dd-153">The **glGetMaterial** function returns in *params* the value or values of parameter *pname* of material *face*.</span></span>

<span data-ttu-id="435dd-154">如果產生錯誤，則不會對 *參數* 的內容進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="435dd-154">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="435dd-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="435dd-155">Requirements</span></span>



| <span data-ttu-id="435dd-156">需求</span><span class="sxs-lookup"><span data-stu-id="435dd-156">Requirement</span></span> | <span data-ttu-id="435dd-157">值</span><span class="sxs-lookup"><span data-stu-id="435dd-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="435dd-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="435dd-158">Minimum supported client</span></span><br/> | <span data-ttu-id="435dd-159">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="435dd-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="435dd-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="435dd-160">Minimum supported server</span></span><br/> | <span data-ttu-id="435dd-161">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="435dd-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="435dd-162">標頭</span><span class="sxs-lookup"><span data-stu-id="435dd-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="435dd-163"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="435dd-164">程式庫</span><span class="sxs-lookup"><span data-stu-id="435dd-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="435dd-165"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="435dd-166">DLL</span><span class="sxs-lookup"><span data-stu-id="435dd-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="435dd-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="435dd-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="435dd-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="435dd-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="435dd-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="435dd-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="435dd-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="435dd-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="435dd-171">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="435dd-171">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





