---
title: 'glMateriali 函式 (Gl) '
description: TheglMateriali 函數會指定光源模型的材質參數。
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- glMateriali 函式 OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc4f1bf6628f1674cf9c3534b9f0c9d028246d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968336"
---
# <a name="glmateriali-function"></a><span data-ttu-id="1f266-104">glMateriali 函式</span><span class="sxs-lookup"><span data-stu-id="1f266-104">glMateriali function</span></span>

<span data-ttu-id="1f266-105">**GlMateriali** 函數會指定光源模型的材質參數。</span><span class="sxs-lookup"><span data-stu-id="1f266-105">The **glMateriali** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f266-106">語法</span><span class="sxs-lookup"><span data-stu-id="1f266-106">Syntax</span></span>


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="1f266-107">參數</span><span class="sxs-lookup"><span data-stu-id="1f266-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f266-108">*臉*</span><span class="sxs-lookup"><span data-stu-id="1f266-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="1f266-109">正在更新的臉部或臉部。</span><span class="sxs-lookup"><span data-stu-id="1f266-109">The face or faces that are being updated.</span></span> <span data-ttu-id="1f266-110">必須是下列其中一項： GL \_ front、gl \_ BACK 或 gl \_ front 和 gl \_ 回來。</span><span class="sxs-lookup"><span data-stu-id="1f266-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="1f266-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="1f266-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="1f266-112">要更新之臉部或臉部的單一值材質參數。</span><span class="sxs-lookup"><span data-stu-id="1f266-112">The single-valued material parameter of the face or faces being updated.</span></span> <span data-ttu-id="1f266-113">必須是 GL \_ 的反光。</span><span class="sxs-lookup"><span data-stu-id="1f266-113">Must be GL\_SHININESS.</span></span>



| <span data-ttu-id="1f266-114">值</span><span class="sxs-lookup"><span data-stu-id="1f266-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="1f266-115">意義</span><span class="sxs-lookup"><span data-stu-id="1f266-115">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="1f266-116"><dt>**GL \_ 反光**</dt></span><span class="sxs-lookup"><span data-stu-id="1f266-116"><dt>**GL\_SHININESS**</dt></span></span> </dl> | <span data-ttu-id="1f266-117">*Param* 參數是單一整數，可指定材質的 RGBA 反射指數。</span><span class="sxs-lookup"><span data-stu-id="1f266-117">The *param* parameter is a single integer that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="1f266-118">整數值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="1f266-118">Integer values are mapped directly.</span></span> <span data-ttu-id="1f266-119">只 \[ 接受範圍0，128中的值 \] 。</span><span class="sxs-lookup"><span data-stu-id="1f266-119">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="1f266-120">正面和背面材質的預設反射指數為0。</span><span class="sxs-lookup"><span data-stu-id="1f266-120">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="1f266-121">*param*</span><span class="sxs-lookup"><span data-stu-id="1f266-121">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="1f266-122">將設定參數 GL 反光的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1f266-122">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f266-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f266-123">Return value</span></span>

<span data-ttu-id="1f266-124">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1f266-124">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1f266-125">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1f266-125">Error codes</span></span>

<span data-ttu-id="1f266-126">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1f266-126">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1f266-127">Name</span><span class="sxs-lookup"><span data-stu-id="1f266-127">Name</span></span>                                                                                              | <span data-ttu-id="1f266-128">意義</span><span class="sxs-lookup"><span data-stu-id="1f266-128">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f266-129"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="1f266-129"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="1f266-130">*臉部* 或 *pname* 都不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="1f266-130">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="1f266-131"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="1f266-131"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="1f266-132">\[已指定0、128範圍以外的反射指數 \] 。</span><span class="sxs-lookup"><span data-stu-id="1f266-132">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1f266-133">備註</span><span class="sxs-lookup"><span data-stu-id="1f266-133">Remarks</span></span>

<span data-ttu-id="1f266-134">**GlMateriali** 函式會將值指派給材質參數。</span><span class="sxs-lookup"><span data-stu-id="1f266-134">The **glMateriali** function assigns values to material parameters.</span></span> <span data-ttu-id="1f266-135">有兩組相符的材質參數。</span><span class="sxs-lookup"><span data-stu-id="1f266-135">There are two matched sets of material parameters.</span></span> <span data-ttu-id="1f266-136">其中一個是 *front* 的集合，用來將點、線條、點陣圖和所有多邊形 (在停用雙面光源時，) ，或只是在) 啟用雙面光源 (時的多邊形。</span><span class="sxs-lookup"><span data-stu-id="1f266-136">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="1f266-137">另一組 [ *回溯*] 則是在啟用雙面光源的情況下，用來為向下多邊形加上陰影。</span><span class="sxs-lookup"><span data-stu-id="1f266-137">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="1f266-138">如需單面和雙面光源計算的詳細資料，請參閱 [**glLightModel**](gllightmodel-functions.md) 。</span><span class="sxs-lookup"><span data-stu-id="1f266-138">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="1f266-139">**GlMateriali** 函式會採用三個引數。</span><span class="sxs-lookup"><span data-stu-id="1f266-139">The **glMateriali** function takes three arguments.</span></span> <span data-ttu-id="1f266-140">第一個是 *臉部*，指定是否 \_ 要修改 gl FRONT 教材、gl \_ 回材料，或 gl \_ 正面 \_ 和 \_ 背面材質。</span><span class="sxs-lookup"><span data-stu-id="1f266-140">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="1f266-141">第二個 *pname*，則會指定一或兩個集合中的哪一個參數將會被修改。</span><span class="sxs-lookup"><span data-stu-id="1f266-141">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="1f266-142">第三個 *參數* 會指定將指派給指定參數的值。</span><span class="sxs-lookup"><span data-stu-id="1f266-142">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="1f266-143">材質參數用於光源方程式，可選擇性地套用至每個頂點。</span><span class="sxs-lookup"><span data-stu-id="1f266-143">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="1f266-144">此方程式會在 [**glLightModel**](gllightmodel-functions.md)中討論。</span><span class="sxs-lookup"><span data-stu-id="1f266-144">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="1f266-145">您可以隨時更新材質參數。</span><span class="sxs-lookup"><span data-stu-id="1f266-145">The material parameters can be updated at any time.</span></span> <span data-ttu-id="1f266-146">尤其是，在呼叫 [**glBegin**](glbegin.md)和對應的 [**glEnd**](glend.md)呼叫之間，可以呼叫 **glMateriali** 。</span><span class="sxs-lookup"><span data-stu-id="1f266-146">In particular, **glMateriali** can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="1f266-147">不過，如果每個頂點只會變更單一材質參數，則 [**glColorMaterial**](glcolormaterial.md) 優先于 **glMateriali**。</span><span class="sxs-lookup"><span data-stu-id="1f266-147">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMateriali**.</span></span>

<span data-ttu-id="1f266-148">下列函式會抓取 **glMateriali** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="1f266-148">The following function retrieves information related to **glMateriali**:</span></span>

[<span data-ttu-id="1f266-149">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="1f266-149">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="1f266-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f266-150">Requirements</span></span>



| <span data-ttu-id="1f266-151">需求</span><span class="sxs-lookup"><span data-stu-id="1f266-151">Requirement</span></span> | <span data-ttu-id="1f266-152">值</span><span class="sxs-lookup"><span data-stu-id="1f266-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f266-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f266-153">Minimum supported client</span></span><br/> | <span data-ttu-id="1f266-154">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f266-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1f266-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f266-155">Minimum supported server</span></span><br/> | <span data-ttu-id="1f266-156">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f266-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f266-157">標頭</span><span class="sxs-lookup"><span data-stu-id="1f266-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f266-158"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="1f266-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1f266-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="1f266-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f266-160"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f266-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f266-161">DLL</span><span class="sxs-lookup"><span data-stu-id="1f266-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f266-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f266-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f266-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f266-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f266-164">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="1f266-164">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="1f266-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="1f266-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="1f266-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="1f266-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





