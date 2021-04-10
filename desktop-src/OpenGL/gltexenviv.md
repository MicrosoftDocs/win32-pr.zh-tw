---
title: 'glTexEnviv 函式 (Gl) '
description: GlTexEnviv 函式會設定紋理環境參數。
ms.assetid: e98ce736-cc68-4687-8c1b-6b0fef7a677a
keywords:
- glTexEnviv 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexEnviv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ec232f559e8d4af10369ebe98dd0aea71e36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844388"
---
# <a name="gltexenviv-function"></a><span data-ttu-id="fe0c3-104">glTexEnviv 函式</span><span class="sxs-lookup"><span data-stu-id="fe0c3-104">glTexEnviv function</span></span>

<span data-ttu-id="fe0c3-105">**GlTexEnviv** 函式會設定紋理環境參數。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-105">The **glTexEnviv** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0c3-106">語法</span><span class="sxs-lookup"><span data-stu-id="fe0c3-106">Syntax</span></span>


```C++
void WINAPI glTexEnviv(
         GLenum target,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="fe0c3-107">參數</span><span class="sxs-lookup"><span data-stu-id="fe0c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe0c3-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="fe0c3-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0c3-109">紋理環境。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-109">A texture environment.</span></span> <span data-ttu-id="fe0c3-110">必須是 GL \_ 紋理 \_ 環境。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="fe0c3-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="fe0c3-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0c3-112">單一值紋理環境參數的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="fe0c3-113">接受的值為 GL \_ 紋理 \_ 環境 \_ 模式和 gl \_ 紋理的 \_ 環境 \_ 色彩。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-113">Accepted values are GL\_TEXTURE\_ENV\_MODE and GL\_TEXTURE\_ENV\_COLOR.</span></span>

</dd> <dt>

<span data-ttu-id="fe0c3-114">*params*</span><span class="sxs-lookup"><span data-stu-id="fe0c3-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="fe0c3-115">參數陣列的指標：單一符號常數或 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-115">A pointer to an array of parameters: either a single symbolic constant or an RGBA color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe0c3-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe0c3-116">Return value</span></span>

<span data-ttu-id="fe0c3-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fe0c3-118">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fe0c3-118">Error codes</span></span>

<span data-ttu-id="fe0c3-119">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fe0c3-120">Name</span><span class="sxs-lookup"><span data-stu-id="fe0c3-120">Name</span></span>                                                                                                  | <span data-ttu-id="fe0c3-121">意義</span><span class="sxs-lookup"><span data-stu-id="fe0c3-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe0c3-122"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c3-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fe0c3-123">*target* 或 *pname* 不是其中一個可接受的定義值，或當 *params* 應該有定義的常數值 (根據 *pname*) 的值而不是時。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="fe0c3-124"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c3-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fe0c3-125">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="fe0c3-126">備註</span><span class="sxs-lookup"><span data-stu-id="fe0c3-126">Remarks</span></span>

<span data-ttu-id="fe0c3-127">材質環境指定當片段有紋理時，材質值的轉譯方式。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="fe0c3-128">*目標* 參數必須是 GL \_ 紋理 \_ 環境。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="fe0c3-129">*Pname* 參數可以是 gl \_ 紋理 \_ 環境 \_ 模式或 gl \_ 紋理 \_ \_ 的環境色彩。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-129">The *pname* parameter can be either GL\_TEXTURE\_ENV\_MODE or GL\_TEXTURE\_ENV\_COLOR.</span></span>

<span data-ttu-id="fe0c3-130">如果 *pname* 是 GL \_ 紋理 \_ 環境 \_ 模式，則會 (*參數* ，或指向材質函數的符號名稱) 。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-130">If *pname* is GL\_TEXTURE\_ENV\_MODE, then *params* is (or points to) the symbolic name of a texture function.</span></span> <span data-ttu-id="fe0c3-131">已定義三個材質函數： GL \_ lambert、gl \_ DECAL 和 GL \_ BLEND。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-131">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="fe0c3-132">材質函式會使用適用于片段的材質影像值，在片段上作用 (查看 [**glTexParameter**](gltexparameter-functions.md)) 並產生該片段的 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-132">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="fe0c3-133">下表顯示如何為每個可選擇的材質函數產生 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-133">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="fe0c3-134">*C* 是三倍的色彩值 (RGB) ，而 *a* 是相關聯的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-134">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="fe0c3-135">從材質影像解壓縮的 RGBA 值位於 \[ 0、1的範圍內 \] 。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-135">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="fe0c3-136">注標 *f* 指的是傳入片段、紋理影像的注標 *t* 、紋理環境色彩的注標 *c* ，以及注標 *v* 表示紋理函式所產生的值。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-136">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="fe0c3-137">材質影像的每個材質元素最多可有四個元件 (查看 [**glTexImage1D**](glteximage1d.md) 和 [**glTexImage2D**](glteximage2d.md)) 。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-137">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="fe0c3-138">在一個元件的影像中，Lt 表示單一元件。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-138">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="fe0c3-139">雙元件映射使用 *L？*</span><span class="sxs-lookup"><span data-stu-id="fe0c3-139">A two-component image uses *L?*</span></span>  <span data-ttu-id="fe0c3-140">和 *答？*</span><span class="sxs-lookup"><span data-stu-id="fe0c3-140">and *A?*</span></span> <span data-ttu-id="fe0c3-141">.</span><span class="sxs-lookup"><span data-stu-id="fe0c3-141">.</span></span> <span data-ttu-id="fe0c3-142">三個元件的影像只有一個色彩值 *C？*</span><span class="sxs-lookup"><span data-stu-id="fe0c3-142">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="fe0c3-143">.</span><span class="sxs-lookup"><span data-stu-id="fe0c3-143">.</span></span> <span data-ttu-id="fe0c3-144">四個元件的影像同時具有色彩值 *C？*</span><span class="sxs-lookup"><span data-stu-id="fe0c3-144">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="fe0c3-145">和 Alpha 值 *A？*</span><span class="sxs-lookup"><span data-stu-id="fe0c3-145">and an alpha value *A?*</span></span> <span data-ttu-id="fe0c3-146">.</span><span class="sxs-lookup"><span data-stu-id="fe0c3-146">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fe0c3-147">元件數目</span><span class="sxs-lookup"><span data-stu-id="fe0c3-147">Number of components</span></span></th>
<th><span data-ttu-id="fe0c3-148">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="fe0c3-148">GL_MODULATE</span></span></th>
<th><span data-ttu-id="fe0c3-149">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="fe0c3-149">GL_DECAL</span></span></th>
<th><span data-ttu-id="fe0c3-150">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="fe0c3-150">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="fe0c3-151">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fe0c3-151">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fe0c3-152"><em>C<sub>v</sub> </em>   = <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-152"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="fe0c3-153"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-153"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="fe0c3-154">未定義 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fe0c3-154">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fe0c3-155"><em>C<sub>v</sub> </em>   = <em> (1</em> - <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-155"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="fe0c3-156"><em>) C<sub>f</sub> </em> + <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-156"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="fe0c3-157"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-157"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe0c3-158"><em>A<sub>v</sub> </em>   = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-158"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="fe0c3-159"><em>A<sub>v</sub> </em>   = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-159"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="fe0c3-160">2 $ {移除} $</span><span class="sxs-lookup"><span data-stu-id="fe0c3-160">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fe0c3-161"><em>C<sub>v</sub> </em>   = <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-161"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="fe0c3-162"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-162"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="fe0c3-163">未定義 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fe0c3-163">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fe0c3-164"><em>C<sub>v</sub> </em>   = <em> (1</em> - <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-164"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="fe0c3-165"><em>) C<sub>f</sub> </em> + <em>L？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-165"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="fe0c3-166"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-166"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe0c3-167"><em>A<sub>v</sub> </em>   = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-167"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="fe0c3-168"><em>A<sub>v</sub> </em>   = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-168"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="fe0c3-169">3 $ {移除} $</span><span class="sxs-lookup"><span data-stu-id="fe0c3-169">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fe0c3-170"><em>C<sub>v</sub> </em>   = <em>C？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-170"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="fe0c3-171"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-171"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="fe0c3-172"><em>C<sub>v</sub> </em>   = <em>C？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-172"><em>C<sub>v</sub></em>  = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="fe0c3-173">未定義 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fe0c3-173">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe0c3-174"><em>A<sub>v</sub> </em>   = <em> <sub>F</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="fe0c3-174"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="fe0c3-175"><em>A<sub>v</sub> </em>   = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-175"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="fe0c3-176">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fe0c3-176">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="fe0c3-177"><em>C<sub>v</sub> </em>   = <em>C？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-177"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="fe0c3-178"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-178"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="fe0c3-179"><em>C<sub>v</sub> </em> = (1- <em>A？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-179"><em>C<sub>v</sub></em>  = (1 - <em>A?</em></span></span> <span data-ttu-id="fe0c3-180"><em>) C<sub>f</sub> </em> + <em>A？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-180"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="fe0c3-181"><em>C？</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-181"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="fe0c3-182">未定義 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="fe0c3-182">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe0c3-183"><em>A<sub>v</sub> </em>   = <em>答：</em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-183"><em>A<sub>v</sub></em>  = <em>A?</em></span></span> <span data-ttu-id="fe0c3-184"><em><sub>F</sub></em> </span><span class="sxs-lookup"><span data-stu-id="fe0c3-184"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="fe0c3-185"><em>A<sub>v</sub> </em>   = <em> <sub>F</sub> </em></span><span class="sxs-lookup"><span data-stu-id="fe0c3-185"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="fe0c3-186">如果 pname 是 GL \_ 紋理 \_ 環境 \_ 色彩，則 *params* 是陣列的指標，該陣列包含由四個值組成的 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-186">If pname is GL\_TEXTURE\_ENV\_COLOR, *params* is a pointer to an array that holds an RGBA color consisting of four values.</span></span> <span data-ttu-id="fe0c3-187">整數色彩元件會以線性方式轉譯，因此最多正整數會對應到1.0，而最大的負整數會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-187">Integer color components are interpreted linearly such that the most positive integer maps to 1.0, and the most negative integer maps to -1.0.</span></span> <span data-ttu-id="fe0c3-188">當指定值時，這些值會壓制至範圍 \[ 0、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-188">The values are clamped to the range \[0, 1\] when they are specified.</span></span> <span data-ttu-id="fe0c3-189">*C <sub>c</sub>* 採用這四個值。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-189">*C<sub>c</sub>* takes these four values.</span></span>

<span data-ttu-id="fe0c3-190">GL \_ 紋理 \_ 環境 \_ 模式預設為 gl \_ lambert，而 gl \_ 紋理 \_ 環境 \_ 色彩預設為 (0、0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="fe0c3-190">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE and GL\_TEXTURE\_ENV\_COLOR defaults to (0, 0, 0, 0).</span></span>

<span data-ttu-id="fe0c3-191">下列函式會抓取 **glTexEnviv** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="fe0c3-191">The following function retrieves information related to **glTexEnviv**:</span></span>

[<span data-ttu-id="fe0c3-192">**glTexGetEnviv**</span><span class="sxs-lookup"><span data-stu-id="fe0c3-192">**glTexGetEnviv**</span></span>](glgettexenviv.md)

## <a name="requirements"></a><span data-ttu-id="fe0c3-193">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe0c3-193">Requirements</span></span>



| <span data-ttu-id="fe0c3-194">需求</span><span class="sxs-lookup"><span data-stu-id="fe0c3-194">Requirement</span></span> | <span data-ttu-id="fe0c3-195">值</span><span class="sxs-lookup"><span data-stu-id="fe0c3-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0c3-196">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe0c3-196">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0c3-197">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe0c3-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fe0c3-198">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe0c3-198">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0c3-199">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe0c3-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fe0c3-200">標頭</span><span class="sxs-lookup"><span data-stu-id="fe0c3-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe0c3-201"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c3-201"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fe0c3-202">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe0c3-202">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe0c3-203"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c3-203"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe0c3-204">DLL</span><span class="sxs-lookup"><span data-stu-id="fe0c3-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe0c3-205"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe0c3-205"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0c3-206">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe0c3-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0c3-207">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fe0c3-207">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fe0c3-208">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fe0c3-208">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fe0c3-209">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="fe0c3-209">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="fe0c3-210">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="fe0c3-210">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="fe0c3-211">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fe0c3-211">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





