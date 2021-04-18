---
title: 'glBlendFunc 函式 (Gl) '
description: GlBlendFunc 函數會指定圖元算術。
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- glBlendFunc 函式 OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965728"
---
# <a name="glblendfunc-function"></a><span data-ttu-id="10e3a-104">glBlendFunc 函式</span><span class="sxs-lookup"><span data-stu-id="10e3a-104">glBlendFunc function</span></span>

<span data-ttu-id="10e3a-105">**GlBlendFunc** 函數會指定圖元算術。</span><span class="sxs-lookup"><span data-stu-id="10e3a-105">The **glBlendFunc** function specifies pixel arithmetic.</span></span>

## <a name="syntax"></a><span data-ttu-id="10e3a-106">語法</span><span class="sxs-lookup"><span data-stu-id="10e3a-106">Syntax</span></span>


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a><span data-ttu-id="10e3a-107">參數</span><span class="sxs-lookup"><span data-stu-id="10e3a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e3a-108">*sfactor*</span><span class="sxs-lookup"><span data-stu-id="10e3a-108">*sfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="10e3a-109">指定如何計算紅色、綠色、藍色和 Alpha 來源混合因數。</span><span class="sxs-lookup"><span data-stu-id="10e3a-109">Specifies how the red, green, blue, and alpha source-blending factors are computed.</span></span> <span data-ttu-id="10e3a-110">接受九個符號常數： GL \_ 零、gl \_ 1、GL \_ DST \_ 色彩、gl \_ 1 \_ 減去 \_ DST \_ 色彩、gl \_ 來源 \_ Alpha、GL \_ 1 \_ 減去 \_ SRC \_ Alpha、gl \_ DST \_ Alpha、gl \_ 1 \_ 減去 \_ dst \_ Alpha，以及 GL \_ SRC \_ Alpha \_ 飽和。</span><span class="sxs-lookup"><span data-stu-id="10e3a-110">Nine symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_DST\_COLOR, GL\_ONE\_MINUS\_DST\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, GL\_ONE\_MINUS\_DST\_ALPHA, and GL\_SRC\_ALPHA\_SATURATE.</span></span>

</dd> <dt>

<span data-ttu-id="10e3a-111">*dfactor*</span><span class="sxs-lookup"><span data-stu-id="10e3a-111">*dfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="10e3a-112">指定如何計算紅色、綠色、藍色和 Alpha 目的地混合因數。</span><span class="sxs-lookup"><span data-stu-id="10e3a-112">Specifies how the red, green, blue, and alpha destination-blending factors are computed.</span></span> <span data-ttu-id="10e3a-113">接受八個符號常數： GL \_ 零、gl \_ 1、gl \_ SRC \_ 色彩、gl \_ 1 \_ 減去 \_ SRC \_ 色彩、gl \_ src \_ Alpha、gl \_ \_ 減去 \_ src \_ Alpha、gl \_ DST \_ Alpha 和 gl \_ 1 \_ 減去 \_ DST \_ Alpha。</span><span class="sxs-lookup"><span data-stu-id="10e3a-113">Eight symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_SRC\_COLOR, GL\_ONE\_MINUS\_SRC\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, and GL\_ONE\_MINUS\_DST\_ALPHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10e3a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="10e3a-114">Return value</span></span>

<span data-ttu-id="10e3a-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="10e3a-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10e3a-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="10e3a-116">Error codes</span></span>

<span data-ttu-id="10e3a-117">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="10e3a-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="10e3a-118">Name</span><span class="sxs-lookup"><span data-stu-id="10e3a-118">Name</span></span>                                                                                                  | <span data-ttu-id="10e3a-119">意義</span><span class="sxs-lookup"><span data-stu-id="10e3a-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="10e3a-120"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="10e3a-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="10e3a-121">*Sfactor* 或 *dfactor* 都不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="10e3a-121">Either *sfactor* or *dfactor* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="10e3a-122"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="10e3a-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="10e3a-123">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="10e3a-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="10e3a-124">備註</span><span class="sxs-lookup"><span data-stu-id="10e3a-124">Remarks</span></span>

<span data-ttu-id="10e3a-125">在 RGB 模式中，可以使用混合傳入 (來源) RGBA 值的函式，以及已在目的地值) 的 (畫面格緩衝區中的 RGBA 值來繪製圖元。</span><span class="sxs-lookup"><span data-stu-id="10e3a-125">In RGB mode, pixels can be drawn using a function that blends the incoming (source) RGBA values with the RGBA values that are already in the framebuffer (the destination values).</span></span> <span data-ttu-id="10e3a-126">依預設，會停用混色。</span><span class="sxs-lookup"><span data-stu-id="10e3a-126">By default, blending is disabled.</span></span> <span data-ttu-id="10e3a-127">使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 搭配 GL \_ BLEND 引數來啟用和停用混合。</span><span class="sxs-lookup"><span data-stu-id="10e3a-127">Use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the GL\_BLEND argument to enable and disable blending.</span></span>

<span data-ttu-id="10e3a-128">啟用時， **glBlendFunc** 會定義混合的運算。</span><span class="sxs-lookup"><span data-stu-id="10e3a-128">When enabled, **glBlendFunc** defines the operation of blending.</span></span> <span data-ttu-id="10e3a-129">*Sfactor* 參數會指定使用九種方法來調整來源色彩元件的大小。</span><span class="sxs-lookup"><span data-stu-id="10e3a-129">The *sfactor* parameter specifies which of nine methods is used to scale the source color components.</span></span> <span data-ttu-id="10e3a-130">*Dfactor* 參數會指定用來調整目的地色彩元件的八種方法。</span><span class="sxs-lookup"><span data-stu-id="10e3a-130">The *dfactor* parameter specifies which of eight methods is used to scale the destination color components.</span></span> <span data-ttu-id="10e3a-131">下表說明了11種可能的方法。</span><span class="sxs-lookup"><span data-stu-id="10e3a-131">The eleven possible methods are described in the following table.</span></span> <span data-ttu-id="10e3a-132">每個方法都會定義四個縮放因數，分別用於紅色、綠色、藍色和 Alpha。</span><span class="sxs-lookup"><span data-stu-id="10e3a-132">Each method defines four scale factors one each for red, green, blue, and alpha.</span></span>

<span data-ttu-id="10e3a-133">在資料表和後續的方商中，來源和目的地色彩元件稱為 (*R*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-133">In the table and in subsequent equations, source and destination color components are referred to as (*R*?</span></span> <span data-ttu-id="10e3a-134">， *G*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-134">, *G*?</span></span> <span data-ttu-id="10e3a-135">， *B*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-135">, *B*?</span></span> <span data-ttu-id="10e3a-136">， *答*：</span><span class="sxs-lookup"><span data-stu-id="10e3a-136">, *A*?</span></span> <span data-ttu-id="10e3a-137">) 和 (*R*<sub>d</sub> 、 *G*<sub>d</sub> 、 *B*<sub>d</sub> 、 \*\* <sub>d</sub> ) 。</span><span class="sxs-lookup"><span data-stu-id="10e3a-137">) and (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span></span> <span data-ttu-id="10e3a-138">其可理解的整數值介於零和 (*k*<sub>r</sub> 、 *k*<sub>G</sub> 、 *k*<sub>r</sub> 、 *k*<sub>A</sub> ) ，其中</span><span class="sxs-lookup"><span data-stu-id="10e3a-138">They are understood to have integer values between zero and (*k*<sub>R</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), where</span></span>

<span data-ttu-id="10e3a-139">*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1</span><span class="sxs-lookup"><span data-stu-id="10e3a-139">*k*<sub>R</sub> = 2 <sup>m</sup>*R* - 1</span></span>

<span data-ttu-id="10e3a-140">*k*<sub>g</sub> = 2 <sup>m</sup>*g* -1</span><span class="sxs-lookup"><span data-stu-id="10e3a-140">*k*<sub>G</sub> = 2 <sup>m</sup>*G* - 1</span></span>

<span data-ttu-id="10e3a-141">*k*<sub>b</sub> = 2 <sup>m</sup>*b* -1</span><span class="sxs-lookup"><span data-stu-id="10e3a-141">*k*<sub>B</sub> = 2 <sup>m</sup>*B* - 1</span></span>

<span data-ttu-id="10e3a-142">*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1</span><span class="sxs-lookup"><span data-stu-id="10e3a-142">*k*<sub>A</sub> = 2 <sup>m</sup>*A* - 1</span></span>

<span data-ttu-id="10e3a-143">和 (*m*<sub>R</sub> 、 *m*<sub>G</sub> 、 *m*<sub>B</sub> 、 *m*<sub>A</sub> ) 是紅色、綠色、藍色和 Alpha bitplanes 的數目。</span><span class="sxs-lookup"><span data-stu-id="10e3a-143">and (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) is the number of red, green, blue, and alpha bitplanes.</span></span>

<span data-ttu-id="10e3a-144">來源和目的縮放比例稱為 (*s*<sub>r</sub> 、 *s*<sub>G</sub> 、 *s*<sub>B</sub> 、 *s*<sub>) 和</sub> (*d*<sub>r</sub> 、 *d*<sub>G</sub> 、 *d*<sub>B</sub> 、 *d*<sub>A</sub> ) 。</span><span class="sxs-lookup"><span data-stu-id="10e3a-144">Source and destination scale factors are referred to as (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) and (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ).</span></span> <span data-ttu-id="10e3a-145">表格中描述的比例因素（表示 (*f*<sub>R</sub> 、 *f*<sub>G</sub> 、 *f*<sub>B</sub> 、 *f*<sub>A</sub> ) ）代表來源或目的地因素。</span><span class="sxs-lookup"><span data-stu-id="10e3a-145">The scale factors described in the table, denoted (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), represent either source or destination factors.</span></span> <span data-ttu-id="10e3a-146">所有比例因素的範圍為 \[ 0、1 \] 。</span><span class="sxs-lookup"><span data-stu-id="10e3a-146">All scale factors have range \[0,1\].</span></span>



| <span data-ttu-id="10e3a-147">參數</span><span class="sxs-lookup"><span data-stu-id="10e3a-147">Parameter</span></span>                  | <span data-ttu-id="10e3a-148"> (*f*<sub>R</sub>  、 *f*<sub>G</sub>  、 *f*<sub>B</sub>  、 *f*<sub>A</sub>  ) </span><span class="sxs-lookup"><span data-stu-id="10e3a-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span></span>                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10e3a-149">GL \_ 零</span><span class="sxs-lookup"><span data-stu-id="10e3a-149">GL\_ZERO</span></span>                   | <span data-ttu-id="10e3a-150">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="10e3a-150">(0,0,0,0)</span></span>                                                                                                                                                    |
| <span data-ttu-id="10e3a-151">GL \_ 1</span><span class="sxs-lookup"><span data-stu-id="10e3a-151">GL\_ONE</span></span>                    | <span data-ttu-id="10e3a-152"> (1，1，1，1) </span><span class="sxs-lookup"><span data-stu-id="10e3a-152">(1,1,1,1)</span></span>                                                                                                                                                    |
| <span data-ttu-id="10e3a-153">GL \_ SRC \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="10e3a-153">GL\_SRC\_COLOR</span></span>             | <span data-ttu-id="10e3a-154"> (*R*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-154">(*R*?</span></span><span data-ttu-id="10e3a-155"> / *k*<sub>R</sub> 、 *G*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-155"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="10e3a-156"> / *k*<sub>G</sub> 、 *B*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-156"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="10e3a-157"> / *k*<sub>B</sub> ， *A*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-157"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="10e3a-158"> / *k*<sub>)</sub></span><span class="sxs-lookup"><span data-stu-id="10e3a-158"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="10e3a-159">GL \_ 1 \_ 減去 \_ SRC \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="10e3a-159">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="10e3a-160"> (1，1，1，1)  (*R*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-160">(1,1,1,1) - (*R*?</span></span><span data-ttu-id="10e3a-161"> / *k*<sub>R</sub> 、 *G*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-161"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="10e3a-162"> / *k*<sub>G</sub> 、 *B*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-162"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="10e3a-163"> / *k*<sub>B</sub> ， *A*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-163"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="10e3a-164"> / *k*<sub>)</sub></span><span class="sxs-lookup"><span data-stu-id="10e3a-164"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="10e3a-165">GL \_ DST \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="10e3a-165">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="10e3a-166"> (*r*<sub>d</sub>  /  *k*<sub>R</sub> 、 *g*<sub>d</sub>  /  *k*<sub>G</sub> 、 *B*<sub>d</sub>  /  *k*<sub>B</sub> 、 *a*<sub>d</sub>  /  *k*<sub>a</sub> ) </span><span class="sxs-lookup"><span data-stu-id="10e3a-166">(*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="10e3a-167">GL \_ 1 \_ 減去 \_ DST \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="10e3a-167">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="10e3a-168"> (1，1，1，1)  (*R*<sub>d</sub>  /  *k*<sub>r</sub> 、 *G*<sub>d</sub>  /  *k*<sub>G</sub> 、 *B*<sub>d</sub>  /  *k*<sub>b</sub> 、\ \** <sub>d</sub>  /  *k*<sub>a</sub> ) </span><span class="sxs-lookup"><span data-stu-id="10e3a-168">(1,1,1,1) - (*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="10e3a-169">GL \_ SRC \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="10e3a-169">GL\_SRC\_ALPHA</span></span>             | <span data-ttu-id="10e3a-170"> (*嗎*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-170">(*A*?</span></span><span data-ttu-id="10e3a-171"> / *k*<sub>a</sub> ， *答*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-171"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="10e3a-172"> / *k*<sub>a</sub> ， *答*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-172"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="10e3a-173"> / *k*<sub>a</sub> ， *答*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-173"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="10e3a-174"> / *k*<sub>)</sub></span><span class="sxs-lookup"><span data-stu-id="10e3a-174"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="10e3a-175">GL \_ 1 \_ 減去 \_ SRC \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="10e3a-175">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> | <span data-ttu-id="10e3a-176"> (1，1，1，1)  (*A*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-176">(1,1,1,1) - (*A*?</span></span><span data-ttu-id="10e3a-177"> / *k*<sub>a</sub> ， *答*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-177"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="10e3a-178"> / *k*<sub>a</sub> ， *答*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-178"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="10e3a-179"> / *k*<sub>a</sub> ， *答*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-179"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="10e3a-180"> / *k*<sub>)</sub></span><span class="sxs-lookup"><span data-stu-id="10e3a-180"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="10e3a-181">GL \_ DST \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="10e3a-181">GL\_DST\_ALPHA</span></span>             | <span data-ttu-id="10e3a-182"> \(\** <sub>d</sub>  /  *k*<sub>a</sub> 、 *a*<sub>d</sub>  /  *k*<sub>a</sub> 、\ \** <sub>d</sub>  /  *k*<sub>a</sub> 、 *a*<sub>d</sub>  /  *k*<sub>a</sub> ) </span><span class="sxs-lookup"><span data-stu-id="10e3a-182">(*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="10e3a-183">GL \_ 1 \_ 減去 \_ DST \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="10e3a-183">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> | <span data-ttu-id="10e3a-184"> (1，1，1，1)  (*A*<sub>d</sub>  /  *k*<sub>a</sub> 、 *a*<sub>d</sub>k a、d  /   <sub></sub>  <sub></sub>  /  *k*<sub>a</sub> 、 *a*<sub>d</sub>  /  *k*<sub>a</sub> ) </span><span class="sxs-lookup"><span data-stu-id="10e3a-184">(1,1,1,1) - (*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="10e3a-185">GL \_ SRC \_ ALPHA \_ 飽和</span><span class="sxs-lookup"><span data-stu-id="10e3a-185">GL\_SRC\_ALPHA\_SATURATE</span></span>   | <span data-ttu-id="10e3a-186"> (*i、i、i、* 1) </span><span class="sxs-lookup"><span data-stu-id="10e3a-186">(*i,i,i,* 1)</span></span>                                                                                                                                                 |



 

<span data-ttu-id="10e3a-187">在表格中，</span><span class="sxs-lookup"><span data-stu-id="10e3a-187">In the table,</span></span>

<span data-ttu-id="10e3a-188">*i* = 最小 (*A*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-188">*i* = min (*A*?</span></span> <span data-ttu-id="10e3a-189">， *k*<sub>a</sub>   -  *a*<sub>d</sub> ) / *k*<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="10e3a-189">, *k*<sub>A</sub>  - *A*<sub>d</sub> ) / *k*<sub>A</sub></span></span>

<span data-ttu-id="10e3a-190">若要在以 RGBA 模式繪製時判斷圖元的混合 RGBA 值，系統會使用下列方程式：</span><span class="sxs-lookup"><span data-stu-id="10e3a-190">To determine the blended RGBA values of a pixel when drawing in RGBA mode, the system uses the following equations:</span></span>

<span data-ttu-id="10e3a-191">*R* (*d*) = min ( *k*<sub>r</sub> 、 *r*？*s*<sub>r</sub>  +  *r*<sub>d</sub> \*\* <sub>r</sub> ) </span><span class="sxs-lookup"><span data-stu-id="10e3a-191">*R* (*d*) = min( *k*<sub>R</sub> , *R*? *s*<sub>R</sub> + *R*<sub>d</sub> *d*<sub>R</sub> )</span></span>

<span data-ttu-id="10e3a-192">*G* (*d*) = min ( *k*<sub>g g</sub> *？\*\*s*<sub>g</sub>  +  *g*<sub>d</sub> *d*<sub>g</sub> ) </span><span class="sxs-lookup"><span data-stu-id="10e3a-192">*G* (*d*) = min( *k*<sub>G</sub> , *G*? *s*<sub>G</sub> + *G*<sub>d</sub> *d*<sub>G</sub>  )</span></span>

<span data-ttu-id="10e3a-193">*B* (*d*) = min ( *k*<sub>b</sub> *，b*？*s*<sub>b</sub>  +  *b*<sub>d</sub> *d*<sub>b</sub> ) </span><span class="sxs-lookup"><span data-stu-id="10e3a-193">*B* (*d*) = min( *k*<sub>B</sub> *, B*? *s*<sub>B</sub> + *B*<sub>d</sub> *d*<sub>B</sub>  )</span></span>

<span data-ttu-id="10e3a-194">*(* *d*) = min ( *k*<sub>a</sub> *？\*\*s*<sub>a a</sub>  +  *a*<sub>d</sub> *a* <sub></sub> ) </span><span class="sxs-lookup"><span data-stu-id="10e3a-194">*A* (*d*) = min( *k*<sub>A</sub> , *A*? *s*<sub>A</sub> + *A*<sub>d</sub> *d*<sub>A</sub>  )</span></span>

<span data-ttu-id="10e3a-195">儘管上述方程式有明顯的精確度，但不會完全指定混合算術，因為混合的運算會以不精確的整數色彩值來運作。</span><span class="sxs-lookup"><span data-stu-id="10e3a-195">Despite the apparent precision of the above equations, blending arithmetic is not exactly specified, because blending operates with imprecise integer color values.</span></span> <span data-ttu-id="10e3a-196">不過，應該等於1的 blend 因數保證不會修改其被乘數，而 blend 因數等於零則會將其被乘數減少為零。</span><span class="sxs-lookup"><span data-stu-id="10e3a-196">However, a blend factor that should be equal to one is guaranteed not to modify its multiplicand, and a blend factor equal to zero reduces its multiplicand to zero.</span></span> <span data-ttu-id="10e3a-197">因此，例如，當 *sfactor* 為 gl \_ src Alpha 時 \_ ， *dfactor* 是 gl \_ 1 \_ 減去 \_ SRC \_ ALPHA，而 *A*？等於 *k*<sub>A</sub>，則方程式會減少為簡單的取代：</span><span class="sxs-lookup"><span data-stu-id="10e3a-197">Thus, for example, when *sfactor* is GL\_SRC\_ALPHA, *dfactor* is GL\_ONE\_MINUS\_SRC\_ALPHA, and *A*? is equal to *k*<sub>A</sub>, the equations reduce to simple replacement:</span></span>

<span data-ttu-id="10e3a-198">*R*<sub>d</sub>  =  *r*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-198">*R*<sub>d</sub> = *R*?</span></span>

<span data-ttu-id="10e3a-199">*G*<sub>d</sub>  =  *g*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-199">*G*<sub>d</sub> = *G*?</span></span>

<span data-ttu-id="10e3a-200">B <sub>d</sub>  =  *b*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-200">B <sub>d</sub> = *B*?</span></span>

<span data-ttu-id="10e3a-201">*A*<sub>d</sub>  =  *a*？</span><span class="sxs-lookup"><span data-stu-id="10e3a-201">*A*<sub>d</sub> = *A*?</span></span>

## <a name="examples"></a><span data-ttu-id="10e3a-202">範例</span><span class="sxs-lookup"><span data-stu-id="10e3a-202">Examples</span></span>

<span data-ttu-id="10e3a-203">透明度最適合使用 **glBlendFunc** (GL \_ SRC \_ Alpha、gl \_ 1 \_ 減去 \_ SRC \_ Alpha) ，基本專案從最遠到最接近。</span><span class="sxs-lookup"><span data-stu-id="10e3a-203">Transparency is best implemented using **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) with primitives sorted from farthest to nearest.</span></span> <span data-ttu-id="10e3a-204">請注意，這個透明度計算不需要在畫面格緩衝區中出現 Alpha bitplanes。</span><span class="sxs-lookup"><span data-stu-id="10e3a-204">Note that this transparency calculation does not require the presence of alpha bitplanes in the framebuffer.</span></span>

<span data-ttu-id="10e3a-205">您也可以使用 **glBlendFunc** (GL \_ SRC \_ Alpha、gl \_ 1 \_ 減去 \_ SRC \_ Alpha) ，以任意順序呈現反鋸齒的點和線條。</span><span class="sxs-lookup"><span data-stu-id="10e3a-205">You can also use **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) for rendering antialiased points and lines in arbitrary order.</span></span>

<span data-ttu-id="10e3a-206">若要將多邊形消除鋸齒優化，請使用 **glBlendFunc** (GL \_ SRC \_ \_ \_) ALPHA</span><span class="sxs-lookup"><span data-stu-id="10e3a-206">To optimize polygon antialiasing, use **glBlendFunc**(GL\_SRC\_ALPHA\_SATURATE, GL\_ONE) with polygons sorted from nearest to farthest.</span></span> <span data-ttu-id="10e3a-207"> (查看 \_ glEnable 中的 GL 多邊形 \_ 平滑[](glenable.md)引數，以取得有關多邊形消除鋸齒的資訊 ) 。必須要有這個 blend 函式的 bitplanes 目的地 Alpha，才能正常運作，請儲存累積的涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="10e3a-207">(See the GL\_POLYGON\_SMOOTH argument in [**glEnable**](glenable.md) for information on polygon antialiasing.) Destination alpha bitplanes, which must be present for this blend function to operate correctly, store the accumulated coverage.</span></span>

<span data-ttu-id="10e3a-208">傳入的 (來源) Alpha 是一種材質不透明度，範圍從 1.0 (*K*<sub>) ，</sub> 代表完整的不透明度，到 0.0 (0) ，代表完整的透明度。</span><span class="sxs-lookup"><span data-stu-id="10e3a-208">Incoming (source) alpha is a material opacity, ranging from 1.0 (*K*<sub>A</sub> ), representing complete opacity, to 0.0 (0), representing complete transparency.</span></span>

<span data-ttu-id="10e3a-209">當您為繪圖啟用一個以上的色彩緩衝區時，每個啟用的緩衝區都會個別混合，而緩衝區的內容會用於目的地色彩。</span><span class="sxs-lookup"><span data-stu-id="10e3a-209">When you enable more than one color buffer for drawing, each enabled buffer is blended separately, and the contents of the buffer is used for destination color.</span></span> <span data-ttu-id="10e3a-210"> (參閱 [**glDrawBuffer**](gldrawbuffer.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="10e3a-210">(See [**glDrawBuffer**](gldrawbuffer.md).)</span></span>

<span data-ttu-id="10e3a-211">混色只會影響 RGBA 轉譯。</span><span class="sxs-lookup"><span data-stu-id="10e3a-211">Blending affects only RGBA rendering.</span></span> <span data-ttu-id="10e3a-212">色彩索引轉譯器會忽略它。</span><span class="sxs-lookup"><span data-stu-id="10e3a-212">It is ignored by color-index renderers.</span></span>

<span data-ttu-id="10e3a-213">下列函式會取出與 **glBlendFunc** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="10e3a-213">The following functions retrieve information related to **glBlendFunc**:</span></span>

<span data-ttu-id="10e3a-214">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ BLEND \_ SRC 的 glGet</span><span class="sxs-lookup"><span data-stu-id="10e3a-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_SRC</span></span>

<span data-ttu-id="10e3a-215">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ BLEND \_ DST 的 glGet</span><span class="sxs-lookup"><span data-stu-id="10e3a-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_DST</span></span>

<span data-ttu-id="10e3a-216">[](glisenabled.md)具有引數 GL \_ BLEND 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="10e3a-216">[**glIsEnabled**](glisenabled.md) with argument GL\_BLEND</span></span>

## <a name="requirements"></a><span data-ttu-id="10e3a-217">規格需求</span><span class="sxs-lookup"><span data-stu-id="10e3a-217">Requirements</span></span>



| <span data-ttu-id="10e3a-218">需求</span><span class="sxs-lookup"><span data-stu-id="10e3a-218">Requirement</span></span> | <span data-ttu-id="10e3a-219">值</span><span class="sxs-lookup"><span data-stu-id="10e3a-219">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10e3a-220">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10e3a-220">Minimum supported client</span></span><br/> | <span data-ttu-id="10e3a-221">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10e3a-221">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="10e3a-222">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10e3a-222">Minimum supported server</span></span><br/> | <span data-ttu-id="10e3a-223">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10e3a-223">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="10e3a-224">標頭</span><span class="sxs-lookup"><span data-stu-id="10e3a-224">Header</span></span><br/>                   | <dl> <span data-ttu-id="10e3a-225"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="10e3a-225"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="10e3a-226">程式庫</span><span class="sxs-lookup"><span data-stu-id="10e3a-226">Library</span></span><br/>                  | <dl> <span data-ttu-id="10e3a-227"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="10e3a-227"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="10e3a-228">DLL</span><span class="sxs-lookup"><span data-stu-id="10e3a-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10e3a-229"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10e3a-229"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10e3a-230">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10e3a-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10e3a-231">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="10e3a-231">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="10e3a-232">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="10e3a-232">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="10e3a-233">**glClear**</span><span class="sxs-lookup"><span data-stu-id="10e3a-233">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="10e3a-234">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="10e3a-234">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="10e3a-235">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="10e3a-235">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="10e3a-236">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="10e3a-236">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="10e3a-237">**glGet**</span><span class="sxs-lookup"><span data-stu-id="10e3a-237">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="10e3a-238">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="10e3a-238">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="10e3a-239">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="10e3a-239">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="10e3a-240">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="10e3a-240">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





