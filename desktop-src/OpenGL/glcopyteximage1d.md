---
title: 'glCopyTexImage1D 函式 (Gl) '
description: GlCopyTexImage1D 函式會將圖元從畫面格緩衝區複製到一維材質影像。
ms.assetid: 3b4d12d5-5efe-40d2-ac5f-95ea5ef243dd
keywords:
- glCopyTexImage1D 函式 OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63180386c094f0c4e4de0f1a361bc3bcb1c6e5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998017"
---
# <a name="glcopyteximage1d-function"></a><span data-ttu-id="c34ca-104">glCopyTexImage1D 函式</span><span class="sxs-lookup"><span data-stu-id="c34ca-104">glCopyTexImage1D function</span></span>

<span data-ttu-id="c34ca-105">**GlCopyTexImage1D** 函式會將圖元從畫面格緩衝區複製到一維材質影像。</span><span class="sxs-lookup"><span data-stu-id="c34ca-105">The **glCopyTexImage1D** function copies pixels from the framebuffer into a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="c34ca-106">語法</span><span class="sxs-lookup"><span data-stu-id="c34ca-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage1D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="c34ca-107">參數</span><span class="sxs-lookup"><span data-stu-id="c34ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c34ca-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="c34ca-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="c34ca-109">將變更影像資料的目標。</span><span class="sxs-lookup"><span data-stu-id="c34ca-109">The target for which the image data will be changed.</span></span> <span data-ttu-id="c34ca-110">必須具有值 GL \_ 紋理 \_ 1d。</span><span class="sxs-lookup"><span data-stu-id="c34ca-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="c34ca-111">*level*</span><span class="sxs-lookup"><span data-stu-id="c34ca-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="c34ca-112">詳細資料層級數目。</span><span class="sxs-lookup"><span data-stu-id="c34ca-112">The level-of-detail number.</span></span> <span data-ttu-id="c34ca-113">層級0是基底映射。</span><span class="sxs-lookup"><span data-stu-id="c34ca-113">Level 0 is the base image.</span></span> <span data-ttu-id="c34ca-114">層級 *n* 是第 *n* 個 mipmap 縮減影像。</span><span class="sxs-lookup"><span data-stu-id="c34ca-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="c34ca-115">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="c34ca-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c34ca-116">材質資料的內部格式和解析度。</span><span class="sxs-lookup"><span data-stu-id="c34ca-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="c34ca-117">此參數必須是下列其中一個符號值。</span><span class="sxs-lookup"><span data-stu-id="c34ca-117">This parameter must be one of the following symbolic values.</span></span>



| <span data-ttu-id="c34ca-118">常數</span><span class="sxs-lookup"><span data-stu-id="c34ca-118">Constant</span></span>                 | <span data-ttu-id="c34ca-119">R 位</span><span class="sxs-lookup"><span data-stu-id="c34ca-119">R Bits</span></span> | <span data-ttu-id="c34ca-120">G 位</span><span class="sxs-lookup"><span data-stu-id="c34ca-120">G Bits</span></span> | <span data-ttu-id="c34ca-121">B 位</span><span class="sxs-lookup"><span data-stu-id="c34ca-121">B Bits</span></span> | <span data-ttu-id="c34ca-122">位</span><span class="sxs-lookup"><span data-stu-id="c34ca-122">A Bits</span></span> | <span data-ttu-id="c34ca-123">L 位</span><span class="sxs-lookup"><span data-stu-id="c34ca-123">L Bits</span></span> | <span data-ttu-id="c34ca-124">I 位</span><span class="sxs-lookup"><span data-stu-id="c34ca-124">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="c34ca-125">GL \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="c34ca-125">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="c34ca-126">GL \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="c34ca-126">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="c34ca-127">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-127">4</span></span>      |        |        |
| <span data-ttu-id="c34ca-128">GL \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="c34ca-128">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="c34ca-129">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-129">8</span></span>      |        |        |
| <span data-ttu-id="c34ca-130">GL \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="c34ca-130">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="c34ca-131">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-131">12</span></span>     |        |        |
| <span data-ttu-id="c34ca-132">GL \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="c34ca-132">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="c34ca-133">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-133">16</span></span>     |        |        |
| <span data-ttu-id="c34ca-134">GL \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="c34ca-134">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="c34ca-135">GL \_ LUMINANCE4</span><span class="sxs-lookup"><span data-stu-id="c34ca-135">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="c34ca-136">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-136">4</span></span>      |        |
| <span data-ttu-id="c34ca-137">GL \_ LUMINANCE8</span><span class="sxs-lookup"><span data-stu-id="c34ca-137">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="c34ca-138">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-138">8</span></span>      |        |
| <span data-ttu-id="c34ca-139">GL \_ LUMINANCE12</span><span class="sxs-lookup"><span data-stu-id="c34ca-139">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="c34ca-140">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-140">12</span></span>     |        |
| <span data-ttu-id="c34ca-141">GL \_ LUMINANCE16</span><span class="sxs-lookup"><span data-stu-id="c34ca-141">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="c34ca-142">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-142">16</span></span>     |        |
| <span data-ttu-id="c34ca-143">GL \_ 亮度 \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="c34ca-143">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="c34ca-144">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="c34ca-144">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="c34ca-145">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-145">4</span></span>      | <span data-ttu-id="c34ca-146">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-146">4</span></span>      |        |
| <span data-ttu-id="c34ca-147">GL \_ LUMINANCE6 \_ ALPHA2</span><span class="sxs-lookup"><span data-stu-id="c34ca-147">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="c34ca-148">2</span><span class="sxs-lookup"><span data-stu-id="c34ca-148">2</span></span>      | <span data-ttu-id="c34ca-149">6</span><span class="sxs-lookup"><span data-stu-id="c34ca-149">6</span></span>      |        |
| <span data-ttu-id="c34ca-150">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="c34ca-150">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="c34ca-151">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-151">8</span></span>      | <span data-ttu-id="c34ca-152">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-152">8</span></span>      |        |
| <span data-ttu-id="c34ca-153">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="c34ca-153">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="c34ca-154">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-154">4</span></span>      | <span data-ttu-id="c34ca-155">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-155">12</span></span>     |        |
| <span data-ttu-id="c34ca-156">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="c34ca-156">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="c34ca-157">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-157">12</span></span>     | <span data-ttu-id="c34ca-158">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-158">12</span></span>     |        |
| <span data-ttu-id="c34ca-159">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="c34ca-159">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="c34ca-160">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-160">16</span></span>     | <span data-ttu-id="c34ca-161">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-161">16</span></span>     |        |
| <span data-ttu-id="c34ca-162">GL \_ 濃度</span><span class="sxs-lookup"><span data-stu-id="c34ca-162">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="c34ca-163">GL \_ INTENSITY4</span><span class="sxs-lookup"><span data-stu-id="c34ca-163">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="c34ca-164">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-164">4</span></span>      |
| <span data-ttu-id="c34ca-165">GL \_ INTENSITY8</span><span class="sxs-lookup"><span data-stu-id="c34ca-165">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="c34ca-166">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-166">8</span></span>      |
| <span data-ttu-id="c34ca-167">GL \_ INTENSITY12</span><span class="sxs-lookup"><span data-stu-id="c34ca-167">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="c34ca-168">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-168">12</span></span>     |
| <span data-ttu-id="c34ca-169">GL \_ INTENSITY16</span><span class="sxs-lookup"><span data-stu-id="c34ca-169">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="c34ca-170">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-170">16</span></span>     |
| <span data-ttu-id="c34ca-171">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="c34ca-171">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="c34ca-172">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="c34ca-172">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="c34ca-173">3</span><span class="sxs-lookup"><span data-stu-id="c34ca-173">3</span></span>      | <span data-ttu-id="c34ca-174">3</span><span class="sxs-lookup"><span data-stu-id="c34ca-174">3</span></span>      | <span data-ttu-id="c34ca-175">2</span><span class="sxs-lookup"><span data-stu-id="c34ca-175">2</span></span>      |        |        |        |
| <span data-ttu-id="c34ca-176">GL \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="c34ca-176">GL\_RGB4</span></span>                 | <span data-ttu-id="c34ca-177">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-177">4</span></span>      | <span data-ttu-id="c34ca-178">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-178">4</span></span>      | <span data-ttu-id="c34ca-179">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-179">4</span></span>      |        |        |        |
| <span data-ttu-id="c34ca-180">GL \_ RGB5</span><span class="sxs-lookup"><span data-stu-id="c34ca-180">GL\_RGB5</span></span>                 | <span data-ttu-id="c34ca-181">5</span><span class="sxs-lookup"><span data-stu-id="c34ca-181">5</span></span>      | <span data-ttu-id="c34ca-182">5</span><span class="sxs-lookup"><span data-stu-id="c34ca-182">5</span></span>      | <span data-ttu-id="c34ca-183">5</span><span class="sxs-lookup"><span data-stu-id="c34ca-183">5</span></span>      |        |        |        |
| <span data-ttu-id="c34ca-184">GL \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="c34ca-184">GL\_RGB8</span></span>                 | <span data-ttu-id="c34ca-185">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-185">8</span></span>      | <span data-ttu-id="c34ca-186">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-186">8</span></span>      | <span data-ttu-id="c34ca-187">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-187">8</span></span>      |        |        |        |
| <span data-ttu-id="c34ca-188">GL \_ RGB10</span><span class="sxs-lookup"><span data-stu-id="c34ca-188">GL\_RGB10</span></span>                | <span data-ttu-id="c34ca-189">10</span><span class="sxs-lookup"><span data-stu-id="c34ca-189">10</span></span>     | <span data-ttu-id="c34ca-190">10</span><span class="sxs-lookup"><span data-stu-id="c34ca-190">10</span></span>     | <span data-ttu-id="c34ca-191">10</span><span class="sxs-lookup"><span data-stu-id="c34ca-191">10</span></span>     |        |        |        |
| <span data-ttu-id="c34ca-192">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="c34ca-192">GL\_RGB12</span></span>                | <span data-ttu-id="c34ca-193">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-193">12</span></span>     | <span data-ttu-id="c34ca-194">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-194">12</span></span>     | <span data-ttu-id="c34ca-195">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-195">12</span></span>     |        |        |        |
| <span data-ttu-id="c34ca-196">GL \_ RGB16</span><span class="sxs-lookup"><span data-stu-id="c34ca-196">GL\_RGB16</span></span>                | <span data-ttu-id="c34ca-197">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-197">16</span></span>     | <span data-ttu-id="c34ca-198">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-198">16</span></span>     | <span data-ttu-id="c34ca-199">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-199">16</span></span>     |        |        |        |
| <span data-ttu-id="c34ca-200">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="c34ca-200">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="c34ca-201">GL \_ RGBA2</span><span class="sxs-lookup"><span data-stu-id="c34ca-201">GL\_RGBA2</span></span>                | <span data-ttu-id="c34ca-202">2</span><span class="sxs-lookup"><span data-stu-id="c34ca-202">2</span></span>      | <span data-ttu-id="c34ca-203">2</span><span class="sxs-lookup"><span data-stu-id="c34ca-203">2</span></span>      | <span data-ttu-id="c34ca-204">2</span><span class="sxs-lookup"><span data-stu-id="c34ca-204">2</span></span>      | <span data-ttu-id="c34ca-205">2</span><span class="sxs-lookup"><span data-stu-id="c34ca-205">2</span></span>      |        |        |
| <span data-ttu-id="c34ca-206">GL \_ RGBA4</span><span class="sxs-lookup"><span data-stu-id="c34ca-206">GL\_RGBA4</span></span>                | <span data-ttu-id="c34ca-207">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-207">4</span></span>      | <span data-ttu-id="c34ca-208">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-208">4</span></span>      | <span data-ttu-id="c34ca-209">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-209">4</span></span>      | <span data-ttu-id="c34ca-210">4</span><span class="sxs-lookup"><span data-stu-id="c34ca-210">4</span></span>      |        |        |
| <span data-ttu-id="c34ca-211">GL \_ RGB5 \_ A1</span><span class="sxs-lookup"><span data-stu-id="c34ca-211">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="c34ca-212">5</span><span class="sxs-lookup"><span data-stu-id="c34ca-212">5</span></span>      | <span data-ttu-id="c34ca-213">5</span><span class="sxs-lookup"><span data-stu-id="c34ca-213">5</span></span>      | <span data-ttu-id="c34ca-214">5</span><span class="sxs-lookup"><span data-stu-id="c34ca-214">5</span></span>      | <span data-ttu-id="c34ca-215">1</span><span class="sxs-lookup"><span data-stu-id="c34ca-215">1</span></span>      |        |        |
| <span data-ttu-id="c34ca-216">GL \_ RGBA8</span><span class="sxs-lookup"><span data-stu-id="c34ca-216">GL\_RGBA8</span></span>                | <span data-ttu-id="c34ca-217">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-217">8</span></span>      | <span data-ttu-id="c34ca-218">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-218">8</span></span>      | <span data-ttu-id="c34ca-219">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-219">8</span></span>      | <span data-ttu-id="c34ca-220">8</span><span class="sxs-lookup"><span data-stu-id="c34ca-220">8</span></span>      |        |        |
| <span data-ttu-id="c34ca-221">GL \_ RGB10 \_ A2</span><span class="sxs-lookup"><span data-stu-id="c34ca-221">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="c34ca-222">10</span><span class="sxs-lookup"><span data-stu-id="c34ca-222">10</span></span>     | <span data-ttu-id="c34ca-223">10</span><span class="sxs-lookup"><span data-stu-id="c34ca-223">10</span></span>     | <span data-ttu-id="c34ca-224">10</span><span class="sxs-lookup"><span data-stu-id="c34ca-224">10</span></span>     | <span data-ttu-id="c34ca-225">2</span><span class="sxs-lookup"><span data-stu-id="c34ca-225">2</span></span>      |        |        |
| <span data-ttu-id="c34ca-226">GL \_ RGBA12</span><span class="sxs-lookup"><span data-stu-id="c34ca-226">GL\_RGBA12</span></span>               | <span data-ttu-id="c34ca-227">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-227">12</span></span>     | <span data-ttu-id="c34ca-228">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-228">12</span></span>     | <span data-ttu-id="c34ca-229">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-229">12</span></span>     | <span data-ttu-id="c34ca-230">12</span><span class="sxs-lookup"><span data-stu-id="c34ca-230">12</span></span>     |        |        |
| <span data-ttu-id="c34ca-231">GL \_ RGBA16</span><span class="sxs-lookup"><span data-stu-id="c34ca-231">GL\_RGBA16</span></span>               | <span data-ttu-id="c34ca-232">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-232">16</span></span>     | <span data-ttu-id="c34ca-233">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-233">16</span></span>     | <span data-ttu-id="c34ca-234">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-234">16</span></span>     | <span data-ttu-id="c34ca-235">16</span><span class="sxs-lookup"><span data-stu-id="c34ca-235">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="c34ca-236">*x*</span><span class="sxs-lookup"><span data-stu-id="c34ca-236">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="c34ca-237">要複製之圖元資料列左下角的視窗 x 平面座標。</span><span class="sxs-lookup"><span data-stu-id="c34ca-237">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="c34ca-238">*y*</span><span class="sxs-lookup"><span data-stu-id="c34ca-238">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="c34ca-239">要複製之圖元資料列左下角的視窗 y 平面座標。</span><span class="sxs-lookup"><span data-stu-id="c34ca-239">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="c34ca-240">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="c34ca-240">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="c34ca-241">材質影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="c34ca-241">The width of the texture image.</span></span> <span data-ttu-id="c34ca-242">必須為零或 2n + 2 (某個整數 *n* 的 *框線*) 。</span><span class="sxs-lookup"><span data-stu-id="c34ca-242">Must be zero or 2n + 2(*border*) for some integer *n*.</span></span> <span data-ttu-id="c34ca-243">材質影像的高度為1。</span><span class="sxs-lookup"><span data-stu-id="c34ca-243">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="c34ca-244">*邊境*</span><span class="sxs-lookup"><span data-stu-id="c34ca-244">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="c34ca-245">框線的寬度。</span><span class="sxs-lookup"><span data-stu-id="c34ca-245">The width of the border.</span></span> <span data-ttu-id="c34ca-246">必須是零或1。</span><span class="sxs-lookup"><span data-stu-id="c34ca-246">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c34ca-247">傳回值</span><span class="sxs-lookup"><span data-stu-id="c34ca-247">Return value</span></span>

<span data-ttu-id="c34ca-248">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c34ca-248">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c34ca-249">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c34ca-249">Error codes</span></span>

<span data-ttu-id="c34ca-250">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c34ca-250">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c34ca-251">Name</span><span class="sxs-lookup"><span data-stu-id="c34ca-251">Name</span></span>                                                                                                  | <span data-ttu-id="c34ca-252">意義</span><span class="sxs-lookup"><span data-stu-id="c34ca-252">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c34ca-253"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="c34ca-253"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c34ca-254">*目標* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="c34ca-254">*target* was not an accepted value.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="c34ca-255"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="c34ca-255"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c34ca-256">*層級* 小於零或大於 log2 *max*，其中 *max* 是 GL \_ 最大紋理大小的傳回值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="c34ca-256">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                           |
| <dl> <span data-ttu-id="c34ca-257"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="c34ca-257"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c34ca-258">*框線* 不是零或1。</span><span class="sxs-lookup"><span data-stu-id="c34ca-258">*border* was not zero or 1.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="c34ca-259"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="c34ca-259"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c34ca-260">*寬度* 小於零、大於 2 + GL \_ 最大 \_ 紋理 \_ 大小，或 *寬度* 不能表示為某個整數 *n* 的 2n + (*框線*) 。</span><span class="sxs-lookup"><span data-stu-id="c34ca-260">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n +(*border*) for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="c34ca-261"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="c34ca-261"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c34ca-262">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="c34ca-262">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="c34ca-263">備註</span><span class="sxs-lookup"><span data-stu-id="c34ca-263">Remarks</span></span>

<span data-ttu-id="c34ca-264">**GlCopyTexImage1D** 函式會使用來自目前畫面格緩衝區的圖元來定義一維紋理影像，而不是從主儲存體定義為 [**glTexImage1D**](glteximage1d.md)的情況。</span><span class="sxs-lookup"><span data-stu-id="c34ca-264">The **glCopyTexImage1D** function defines a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage1D**](glteximage1d.md).</span></span>

<span data-ttu-id="c34ca-265">使用以 *層級* 指定的 mipmap 層級，會將材質陣列定義為與 *x* 和 *y* 所指定座標之視窗左下角對齊的圖元列，且長度等於 *width* + 2 的 \* *框線*。</span><span class="sxs-lookup"><span data-stu-id="c34ca-265">Using the mipmap level specified with *level*, texture arrays are defined as a pixel row aligned with the lower-left corner of the window at the coordinates specified by *x* and *y*, with a length equal to *width* + 2 \* *border*.</span></span> <span data-ttu-id="c34ca-266">材質陣列的內部格式是以 *internalFormat* 參數指定。</span><span class="sxs-lookup"><span data-stu-id="c34ca-266">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="c34ca-267">**GlCopyTexImage1D** 函式會使用與 [**glCopyPixels**](glcopypixels.md)相同的方式來處理資料列中的圖元，但在圖元的最後轉換之前，所有圖元元件值都會壓制至範圍 \[ 0、1， \] 並轉換為紋理陣列中儲存的材質內部格式。</span><span class="sxs-lookup"><span data-stu-id="c34ca-267">The **glCopyTexImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="c34ca-268">圖元順序是以對應于較低材質座標的較低 *x* 座標來決定。</span><span class="sxs-lookup"><span data-stu-id="c34ca-268">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="c34ca-269">如果目前畫面格緩衝區中指定資料列內的任何圖元都在與目前轉譯內容相關聯的視窗之外，則其值為未定義。</span><span class="sxs-lookup"><span data-stu-id="c34ca-269">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="c34ca-270">您不能在顯示清單中包含 **glCopyTexImage1D** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c34ca-270">You cannot include calls to **glCopyTexImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="c34ca-271">**GlCopyTexImage1D** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c34ca-271">The **glCopyTexImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="c34ca-272">紋理在色彩索引模式中沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="c34ca-272">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="c34ca-273">[**GlPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md)函式會以完全影響 [**glDrawPixels**](gldrawpixels.md)的方式來影響紋理影像。</span><span class="sxs-lookup"><span data-stu-id="c34ca-273">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="c34ca-274">下列函式會抓取 **glCopyTexImage1D** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="c34ca-274">The following function retrieves information related to **glCopyTexImage1D**:</span></span>

<span data-ttu-id="c34ca-275">[](glisenabled.md)具有引數 GL \_ 材質 \_ 1d 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="c34ca-275">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="c34ca-276">規格需求</span><span class="sxs-lookup"><span data-stu-id="c34ca-276">Requirements</span></span>



| <span data-ttu-id="c34ca-277">需求</span><span class="sxs-lookup"><span data-stu-id="c34ca-277">Requirement</span></span> | <span data-ttu-id="c34ca-278">值</span><span class="sxs-lookup"><span data-stu-id="c34ca-278">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c34ca-279">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c34ca-279">Minimum supported client</span></span><br/> | <span data-ttu-id="c34ca-280">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c34ca-280">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c34ca-281">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c34ca-281">Minimum supported server</span></span><br/> | <span data-ttu-id="c34ca-282">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c34ca-282">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c34ca-283">標頭</span><span class="sxs-lookup"><span data-stu-id="c34ca-283">Header</span></span><br/>                   | <dl> <span data-ttu-id="c34ca-284"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="c34ca-284"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c34ca-285">程式庫</span><span class="sxs-lookup"><span data-stu-id="c34ca-285">Library</span></span><br/>                  | <dl> <span data-ttu-id="c34ca-286"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c34ca-286"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c34ca-287">DLL</span><span class="sxs-lookup"><span data-stu-id="c34ca-287">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c34ca-288"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c34ca-288"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c34ca-289">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c34ca-289">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c34ca-290">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="c34ca-290">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="c34ca-291">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="c34ca-291">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="c34ca-292">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="c34ca-292">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="c34ca-293">**glFog**</span><span class="sxs-lookup"><span data-stu-id="c34ca-293">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="c34ca-294">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="c34ca-294">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="c34ca-295">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="c34ca-295">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="c34ca-296">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="c34ca-296">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="c34ca-297">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="c34ca-297">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="c34ca-298">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="c34ca-298">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="c34ca-299">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="c34ca-299">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="c34ca-300">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="c34ca-300">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





