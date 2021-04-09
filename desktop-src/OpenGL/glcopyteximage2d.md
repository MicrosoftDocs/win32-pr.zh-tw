---
title: 'glCopyTexImage2D 函式 (Gl) '
description: GlCopyTexImage2D 函式會將圖元從畫面格緩衝區複製到二維紋理影像。
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- glCopyTexImage2D 函式 OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d04a979e9bb026da904687506f3201d12c12c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843744"
---
# <a name="glcopyteximage2d-function"></a><span data-ttu-id="fdba7-104">glCopyTexImage2D 函式</span><span class="sxs-lookup"><span data-stu-id="fdba7-104">glCopyTexImage2D function</span></span>

<span data-ttu-id="fdba7-105">**GlCopyTexImage2D** 函式會將圖元從畫面格緩衝區複製到二維紋理影像。</span><span class="sxs-lookup"><span data-stu-id="fdba7-105">The **glCopyTexImage2D** function copies pixels from the framebuffer into a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdba7-106">語法</span><span class="sxs-lookup"><span data-stu-id="fdba7-106">Syntax</span></span>


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
);
```



## <a name="parameters"></a><span data-ttu-id="fdba7-107">參數</span><span class="sxs-lookup"><span data-stu-id="fdba7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdba7-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="fdba7-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="fdba7-109">將變更影像資料的目標。</span><span class="sxs-lookup"><span data-stu-id="fdba7-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="fdba7-110">必須具有值 GL \_ 紋理 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="fdba7-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-111">*level*</span><span class="sxs-lookup"><span data-stu-id="fdba7-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="fdba7-112">詳細資料層級數目。</span><span class="sxs-lookup"><span data-stu-id="fdba7-112">The level-of-detail number.</span></span> <span data-ttu-id="fdba7-113">層級0是基底映射。</span><span class="sxs-lookup"><span data-stu-id="fdba7-113">Level 0 is the base image.</span></span> <span data-ttu-id="fdba7-114">層級 *n* 是第 *n* 個 mipmap 縮減影像。</span><span class="sxs-lookup"><span data-stu-id="fdba7-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-115">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="fdba7-115">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="fdba7-116">材質資料的內部格式和解析度。</span><span class="sxs-lookup"><span data-stu-id="fdba7-116">The internal format and resolution of the texture data.</span></span> <span data-ttu-id="fdba7-117">*InternalFormat* 不接受值1、2、3和4。</span><span class="sxs-lookup"><span data-stu-id="fdba7-117">The values 1, 2, 3, and 4 are not accepted for *internalFormat*.</span></span> <span data-ttu-id="fdba7-118">參數可以採用下列其中一個符號值。</span><span class="sxs-lookup"><span data-stu-id="fdba7-118">The parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="fdba7-119">常數</span><span class="sxs-lookup"><span data-stu-id="fdba7-119">Constant</span></span>                 | <span data-ttu-id="fdba7-120">R 位</span><span class="sxs-lookup"><span data-stu-id="fdba7-120">R Bits</span></span> | <span data-ttu-id="fdba7-121">G 位</span><span class="sxs-lookup"><span data-stu-id="fdba7-121">G Bits</span></span> | <span data-ttu-id="fdba7-122">B 位</span><span class="sxs-lookup"><span data-stu-id="fdba7-122">B Bits</span></span> | <span data-ttu-id="fdba7-123">位</span><span class="sxs-lookup"><span data-stu-id="fdba7-123">A Bits</span></span> | <span data-ttu-id="fdba7-124">L 位</span><span class="sxs-lookup"><span data-stu-id="fdba7-124">L Bits</span></span> | <span data-ttu-id="fdba7-125">I 位</span><span class="sxs-lookup"><span data-stu-id="fdba7-125">I Bits</span></span> |
|--------------------------|--------|--------|--------|--------|--------|--------|
| <span data-ttu-id="fdba7-126">GL \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="fdba7-126">GL\_ALPHA</span></span>                |        |        |        |        |        |        |
| <span data-ttu-id="fdba7-127">GL \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="fdba7-127">GL\_ALPHA4</span></span>               |        |        |        | <span data-ttu-id="fdba7-128">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-128">4</span></span>      |        |        |
| <span data-ttu-id="fdba7-129">GL \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="fdba7-129">GL\_ALPHA8</span></span>               |        |        |        | <span data-ttu-id="fdba7-130">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-130">8</span></span>      |        |        |
| <span data-ttu-id="fdba7-131">GL \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="fdba7-131">GL\_ALPHA12</span></span>              |        |        |        | <span data-ttu-id="fdba7-132">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-132">12</span></span>     |        |        |
| <span data-ttu-id="fdba7-133">GL \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="fdba7-133">GL\_ALPHA16</span></span>              |        |        |        | <span data-ttu-id="fdba7-134">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-134">16</span></span>     |        |        |
| <span data-ttu-id="fdba7-135">GL \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="fdba7-135">GL\_LUMINANCE</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="fdba7-136">GL \_ LUMINANCE4</span><span class="sxs-lookup"><span data-stu-id="fdba7-136">GL\_LUMINANCE4</span></span>           |        |        |        |        | <span data-ttu-id="fdba7-137">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-137">4</span></span>      |        |
| <span data-ttu-id="fdba7-138">GL \_ LUMINANCE8</span><span class="sxs-lookup"><span data-stu-id="fdba7-138">GL\_LUMINANCE8</span></span>           |        |        |        |        | <span data-ttu-id="fdba7-139">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-139">8</span></span>      |        |
| <span data-ttu-id="fdba7-140">GL \_ LUMINANCE12</span><span class="sxs-lookup"><span data-stu-id="fdba7-140">GL\_LUMINANCE12</span></span>          |        |        |        |        | <span data-ttu-id="fdba7-141">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-141">12</span></span>     |        |
| <span data-ttu-id="fdba7-142">GL \_ LUMINANCE16</span><span class="sxs-lookup"><span data-stu-id="fdba7-142">GL\_LUMINANCE16</span></span>          |        |        |        |        | <span data-ttu-id="fdba7-143">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-143">16</span></span>     |        |
| <span data-ttu-id="fdba7-144">GL \_ 亮度 \_ ALPHA</span><span class="sxs-lookup"><span data-stu-id="fdba7-144">GL\_LUMINANCE\_ALPHA</span></span>     |        |        |        |        |        |        |
| <span data-ttu-id="fdba7-145">GL \_ LUMINANCE4 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="fdba7-145">GL\_LUMINANCE4\_ALPHA4</span></span>   |        |        |        | <span data-ttu-id="fdba7-146">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-146">4</span></span>      | <span data-ttu-id="fdba7-147">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-147">4</span></span>      |        |
| <span data-ttu-id="fdba7-148">GL \_ LUMINANCE6 \_ ALPHA2</span><span class="sxs-lookup"><span data-stu-id="fdba7-148">GL\_LUMINANCE6\_ALPHA2</span></span>   |        |        |        | <span data-ttu-id="fdba7-149">2</span><span class="sxs-lookup"><span data-stu-id="fdba7-149">2</span></span>      | <span data-ttu-id="fdba7-150">6</span><span class="sxs-lookup"><span data-stu-id="fdba7-150">6</span></span>      |        |
| <span data-ttu-id="fdba7-151">GL \_ LUMINANCE8 \_ ALPHA8</span><span class="sxs-lookup"><span data-stu-id="fdba7-151">GL\_LUMINANCE8\_ALPHA8</span></span>   |        |        |        | <span data-ttu-id="fdba7-152">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-152">8</span></span>      | <span data-ttu-id="fdba7-153">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-153">8</span></span>      |        |
| <span data-ttu-id="fdba7-154">GL \_ LUMINANCE12 \_ ALPHA4</span><span class="sxs-lookup"><span data-stu-id="fdba7-154">GL\_LUMINANCE12\_ALPHA4</span></span>  |        |        |        | <span data-ttu-id="fdba7-155">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-155">4</span></span>      | <span data-ttu-id="fdba7-156">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-156">12</span></span>     |        |
| <span data-ttu-id="fdba7-157">GL \_ LUMINANCE12 \_ ALPHA12</span><span class="sxs-lookup"><span data-stu-id="fdba7-157">GL\_LUMINANCE12\_ALPHA12</span></span> |        |        |        | <span data-ttu-id="fdba7-158">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-158">12</span></span>     | <span data-ttu-id="fdba7-159">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-159">12</span></span>     |        |
| <span data-ttu-id="fdba7-160">GL \_ LUMINANCE16 \_ ALPHA16</span><span class="sxs-lookup"><span data-stu-id="fdba7-160">GL\_LUMINANCE16\_ALPHA16</span></span> |        |        |        | <span data-ttu-id="fdba7-161">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-161">16</span></span>     | <span data-ttu-id="fdba7-162">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-162">16</span></span>     |        |
| <span data-ttu-id="fdba7-163">GL \_ 濃度</span><span class="sxs-lookup"><span data-stu-id="fdba7-163">GL\_INTENSITY</span></span>            |        |        |        |        |        |        |
| <span data-ttu-id="fdba7-164">GL \_ INTENSITY4</span><span class="sxs-lookup"><span data-stu-id="fdba7-164">GL\_INTENSITY4</span></span>           |        |        |        |        |        | <span data-ttu-id="fdba7-165">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-165">4</span></span>      |
| <span data-ttu-id="fdba7-166">GL \_ INTENSITY8</span><span class="sxs-lookup"><span data-stu-id="fdba7-166">GL\_INTENSITY8</span></span>           |        |        |        |        |        | <span data-ttu-id="fdba7-167">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-167">8</span></span>      |
| <span data-ttu-id="fdba7-168">GL \_ INTENSITY12</span><span class="sxs-lookup"><span data-stu-id="fdba7-168">GL\_INTENSITY12</span></span>          |        |        |        |        |        | <span data-ttu-id="fdba7-169">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-169">12</span></span>     |
| <span data-ttu-id="fdba7-170">GL \_ INTENSITY16</span><span class="sxs-lookup"><span data-stu-id="fdba7-170">GL\_INTENSITY16</span></span>          |        |        |        |        |        | <span data-ttu-id="fdba7-171">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-171">16</span></span>     |
| <span data-ttu-id="fdba7-172">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="fdba7-172">GL\_RGB</span></span>                  |        |        |        |        |        |        |
| <span data-ttu-id="fdba7-173">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="fdba7-173">GL\_R3\_G3\_B2</span></span>           | <span data-ttu-id="fdba7-174">3</span><span class="sxs-lookup"><span data-stu-id="fdba7-174">3</span></span>      | <span data-ttu-id="fdba7-175">3</span><span class="sxs-lookup"><span data-stu-id="fdba7-175">3</span></span>      | <span data-ttu-id="fdba7-176">2</span><span class="sxs-lookup"><span data-stu-id="fdba7-176">2</span></span>      |        |        |        |
| <span data-ttu-id="fdba7-177">GL \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="fdba7-177">GL\_RGB4</span></span>                 | <span data-ttu-id="fdba7-178">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-178">4</span></span>      | <span data-ttu-id="fdba7-179">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-179">4</span></span>      | <span data-ttu-id="fdba7-180">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-180">4</span></span>      |        |        |        |
| <span data-ttu-id="fdba7-181">GL \_ RGB5</span><span class="sxs-lookup"><span data-stu-id="fdba7-181">GL\_RGB5</span></span>                 | <span data-ttu-id="fdba7-182">5</span><span class="sxs-lookup"><span data-stu-id="fdba7-182">5</span></span>      | <span data-ttu-id="fdba7-183">5</span><span class="sxs-lookup"><span data-stu-id="fdba7-183">5</span></span>      | <span data-ttu-id="fdba7-184">5</span><span class="sxs-lookup"><span data-stu-id="fdba7-184">5</span></span>      |        |        |        |
| <span data-ttu-id="fdba7-185">GL \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="fdba7-185">GL\_RGB8</span></span>                 | <span data-ttu-id="fdba7-186">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-186">8</span></span>      | <span data-ttu-id="fdba7-187">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-187">8</span></span>      | <span data-ttu-id="fdba7-188">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-188">8</span></span>      |        |        |        |
| <span data-ttu-id="fdba7-189">GL \_ RGB10</span><span class="sxs-lookup"><span data-stu-id="fdba7-189">GL\_RGB10</span></span>                | <span data-ttu-id="fdba7-190">10</span><span class="sxs-lookup"><span data-stu-id="fdba7-190">10</span></span>     | <span data-ttu-id="fdba7-191">10</span><span class="sxs-lookup"><span data-stu-id="fdba7-191">10</span></span>     | <span data-ttu-id="fdba7-192">10</span><span class="sxs-lookup"><span data-stu-id="fdba7-192">10</span></span>     |        |        |        |
| <span data-ttu-id="fdba7-193">GL \_ RGB12</span><span class="sxs-lookup"><span data-stu-id="fdba7-193">GL\_RGB12</span></span>                | <span data-ttu-id="fdba7-194">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-194">12</span></span>     | <span data-ttu-id="fdba7-195">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-195">12</span></span>     | <span data-ttu-id="fdba7-196">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-196">12</span></span>     |        |        |        |
| <span data-ttu-id="fdba7-197">GL \_ RGB16</span><span class="sxs-lookup"><span data-stu-id="fdba7-197">GL\_RGB16</span></span>                | <span data-ttu-id="fdba7-198">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-198">16</span></span>     | <span data-ttu-id="fdba7-199">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-199">16</span></span>     | <span data-ttu-id="fdba7-200">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-200">16</span></span>     |        |        |        |
| <span data-ttu-id="fdba7-201">GL \_ RGBA</span><span class="sxs-lookup"><span data-stu-id="fdba7-201">GL\_RGBA</span></span>                 |        |        |        |        |        |        |
| <span data-ttu-id="fdba7-202">GL \_ RGBA2</span><span class="sxs-lookup"><span data-stu-id="fdba7-202">GL\_RGBA2</span></span>                | <span data-ttu-id="fdba7-203">2</span><span class="sxs-lookup"><span data-stu-id="fdba7-203">2</span></span>      | <span data-ttu-id="fdba7-204">2</span><span class="sxs-lookup"><span data-stu-id="fdba7-204">2</span></span>      | <span data-ttu-id="fdba7-205">2</span><span class="sxs-lookup"><span data-stu-id="fdba7-205">2</span></span>      | <span data-ttu-id="fdba7-206">2</span><span class="sxs-lookup"><span data-stu-id="fdba7-206">2</span></span>      |        |        |
| <span data-ttu-id="fdba7-207">GL \_ RGBA4</span><span class="sxs-lookup"><span data-stu-id="fdba7-207">GL\_RGBA4</span></span>                | <span data-ttu-id="fdba7-208">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-208">4</span></span>      | <span data-ttu-id="fdba7-209">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-209">4</span></span>      | <span data-ttu-id="fdba7-210">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-210">4</span></span>      | <span data-ttu-id="fdba7-211">4</span><span class="sxs-lookup"><span data-stu-id="fdba7-211">4</span></span>      |        |        |
| <span data-ttu-id="fdba7-212">GL \_ RGB5 \_ A1</span><span class="sxs-lookup"><span data-stu-id="fdba7-212">GL\_RGB5\_A1</span></span>             | <span data-ttu-id="fdba7-213">5</span><span class="sxs-lookup"><span data-stu-id="fdba7-213">5</span></span>      | <span data-ttu-id="fdba7-214">5</span><span class="sxs-lookup"><span data-stu-id="fdba7-214">5</span></span>      | <span data-ttu-id="fdba7-215">5</span><span class="sxs-lookup"><span data-stu-id="fdba7-215">5</span></span>      | <span data-ttu-id="fdba7-216">1</span><span class="sxs-lookup"><span data-stu-id="fdba7-216">1</span></span>      |        |        |
| <span data-ttu-id="fdba7-217">GL \_ RGBA8</span><span class="sxs-lookup"><span data-stu-id="fdba7-217">GL\_RGBA8</span></span>                | <span data-ttu-id="fdba7-218">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-218">8</span></span>      | <span data-ttu-id="fdba7-219">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-219">8</span></span>      | <span data-ttu-id="fdba7-220">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-220">8</span></span>      | <span data-ttu-id="fdba7-221">8</span><span class="sxs-lookup"><span data-stu-id="fdba7-221">8</span></span>      |        |        |
| <span data-ttu-id="fdba7-222">GL \_ RGB10 \_ A2</span><span class="sxs-lookup"><span data-stu-id="fdba7-222">GL\_RGB10\_A2</span></span>            | <span data-ttu-id="fdba7-223">10</span><span class="sxs-lookup"><span data-stu-id="fdba7-223">10</span></span>     | <span data-ttu-id="fdba7-224">10</span><span class="sxs-lookup"><span data-stu-id="fdba7-224">10</span></span>     | <span data-ttu-id="fdba7-225">10</span><span class="sxs-lookup"><span data-stu-id="fdba7-225">10</span></span>     | <span data-ttu-id="fdba7-226">2</span><span class="sxs-lookup"><span data-stu-id="fdba7-226">2</span></span>      |        |        |
| <span data-ttu-id="fdba7-227">GL \_ RGBA12</span><span class="sxs-lookup"><span data-stu-id="fdba7-227">GL\_RGBA12</span></span>               | <span data-ttu-id="fdba7-228">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-228">12</span></span>     | <span data-ttu-id="fdba7-229">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-229">12</span></span>     | <span data-ttu-id="fdba7-230">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-230">12</span></span>     | <span data-ttu-id="fdba7-231">12</span><span class="sxs-lookup"><span data-stu-id="fdba7-231">12</span></span>     |        |        |
| <span data-ttu-id="fdba7-232">GL \_ RGBA16</span><span class="sxs-lookup"><span data-stu-id="fdba7-232">GL\_RGBA16</span></span>               | <span data-ttu-id="fdba7-233">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-233">16</span></span>     | <span data-ttu-id="fdba7-234">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-234">16</span></span>     | <span data-ttu-id="fdba7-235">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-235">16</span></span>     | <span data-ttu-id="fdba7-236">16</span><span class="sxs-lookup"><span data-stu-id="fdba7-236">16</span></span>     |        |        |



 

</dd> <dt>

<span data-ttu-id="fdba7-237">*x*</span><span class="sxs-lookup"><span data-stu-id="fdba7-237">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="fdba7-238">要複製之圖元矩形區域左下角的視窗 x 平面座標。</span><span class="sxs-lookup"><span data-stu-id="fdba7-238">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-239">*y*</span><span class="sxs-lookup"><span data-stu-id="fdba7-239">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="fdba7-240">要複製之圖元矩形區域左下角的視窗 y 平面座標。</span><span class="sxs-lookup"><span data-stu-id="fdba7-240">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-241">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="fdba7-241">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="fdba7-242">材質影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="fdba7-242">The width of the texture image.</span></span> <span data-ttu-id="fdba7-243">必須為 \* 某個整數 *n* 的 2n + 2 個 *框線*。</span><span class="sxs-lookup"><span data-stu-id="fdba7-243">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-244">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="fdba7-244">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="fdba7-245">材質影像的高度。</span><span class="sxs-lookup"><span data-stu-id="fdba7-245">The height of the texture image.</span></span> <span data-ttu-id="fdba7-246">必須為 \* 某個整數 *n* 的 2n + 2 個 *框線*。</span><span class="sxs-lookup"><span data-stu-id="fdba7-246">Must be 2n + 2 \* *border* for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="fdba7-247">*邊境*</span><span class="sxs-lookup"><span data-stu-id="fdba7-247">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="fdba7-248">框線的寬度。</span><span class="sxs-lookup"><span data-stu-id="fdba7-248">The width of the border.</span></span> <span data-ttu-id="fdba7-249">必須是零或1。</span><span class="sxs-lookup"><span data-stu-id="fdba7-249">Must be either zero or 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdba7-250">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdba7-250">Return value</span></span>

<span data-ttu-id="fdba7-251">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fdba7-251">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fdba7-252">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fdba7-252">Error codes</span></span>

<span data-ttu-id="fdba7-253">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fdba7-253">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fdba7-254">Name</span><span class="sxs-lookup"><span data-stu-id="fdba7-254">Name</span></span>                                                                                                  | <span data-ttu-id="fdba7-255">意義</span><span class="sxs-lookup"><span data-stu-id="fdba7-255">Meaning</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fdba7-256"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-256"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fdba7-257">*目標* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="fdba7-257">*target* was not an accepted value.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="fdba7-258"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-258"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fdba7-259">*層級* 小於零或大於 log2 *max*，其中 *max* 是 GL \_ 最大紋理大小的傳回值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="fdba7-259">*level* was less than zero or greater than log2 *max*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                               |
| <dl> <span data-ttu-id="fdba7-260"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-260"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fdba7-261">*框線* 不是零或1。</span><span class="sxs-lookup"><span data-stu-id="fdba7-261">*border* was not zero or 1.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="fdba7-262"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-262"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fdba7-263">*寬度* 小於零、大於 2 + GL \_ 最大 \_ 紋理 \_ 大小，或 *寬度* 不能表示為 \* 某個整數 *n* 的 2n + 2 *框線*。</span><span class="sxs-lookup"><span data-stu-id="fdba7-263">*width* was less than zero, greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or *width* cannot be represented as 2n + 2 \* *border* for some integer *n*.</span></span><br/> |
| <dl> <span data-ttu-id="fdba7-264"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-264"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fdba7-265">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="fdba7-265">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="fdba7-266">備註</span><span class="sxs-lookup"><span data-stu-id="fdba7-266">Remarks</span></span>

<span data-ttu-id="fdba7-267">**GlCopyTexImage2D** 函式會使用來自目前畫面格緩衝區的圖元來定義二維紋理影像，而不是從主儲存體（例如 [**glTexImage2D**](glteximage2d.md)的情況下）。</span><span class="sxs-lookup"><span data-stu-id="fdba7-267">The **glCopyTexImage2D** function defines a two-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexImage2D**](glteximage2d.md).</span></span>

<span data-ttu-id="fdba7-268">使用以 *層級* 指定的 mipmap 層級，會將材質陣列定義為圖元的矩形，其左上角位於座標 *x* 和 *y*、寬度等於 *寬度* + (2 \* *框線*) ，以及高度等於 *高度* + (2 \* *框線*) 。</span><span class="sxs-lookup"><span data-stu-id="fdba7-268">Using the mipmap level specified with *level*, texture arrays are defined as a rectangle of pixels with the lower-left corner located at the coordinates *x* and *y*, width equal to *width* + (2 \* *border*), and a height equal to *height* + (2 \* *border*).</span></span> <span data-ttu-id="fdba7-269">材質陣列的內部格式是以 *internalFormat* 參數指定。</span><span class="sxs-lookup"><span data-stu-id="fdba7-269">The internal format of the texture array is specified with the *internalFormat* parameter.</span></span>

<span data-ttu-id="fdba7-270">**GlCopyTexImage2D** 函式會使用與 [**glCopyPixels**](glcopypixels.md)相同的方式來處理資料列中的圖元，但在最後轉換圖元之前，所有圖元元件值都會壓制至範圍 \[ 0、1， \] 並轉換成紋理陣列中儲存的材質內部格式。</span><span class="sxs-lookup"><span data-stu-id="fdba7-270">The **glCopyTexImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="fdba7-271">圖元排序是以對應于較低 *s* 和 *t* 紋理座標的較低 *x* 和 *y* 座標來決定。</span><span class="sxs-lookup"><span data-stu-id="fdba7-271">Pixel ordering is determined with lower *x* and *y* coordinates corresponding to lower *s* and *t* texture coordinates.</span></span> <span data-ttu-id="fdba7-272">如果目前畫面格緩衝區中指定資料列內的任何圖元都在與目前轉譯內容相關聯的視窗之外，則其值為未定義。</span><span class="sxs-lookup"><span data-stu-id="fdba7-272">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="fdba7-273">您不能在顯示清單中包含 **glCopyTexImage2D** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdba7-273">You cannot include calls to **glCopyTexImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="fdba7-274">**GlCopyTexImage2D** 函數僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="fdba7-274">The **glCopyTexImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="fdba7-275">紋理在色彩索引模式中沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="fdba7-275">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="fdba7-276">[**GlPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md)函式會以完全影響 [**glDrawPixels**](gldrawpixels.md)的方式來影響紋理影像。</span><span class="sxs-lookup"><span data-stu-id="fdba7-276">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="fdba7-277">下列函式會抓取 **glCopyTexImage2D** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="fdba7-277">The following function retrieves information related to **glCopyTexImage2D**:</span></span>

<span data-ttu-id="fdba7-278">[](glisenabled.md)具有引數 GL \_ 材質 \_ 2d 的 glIsEnabled</span><span class="sxs-lookup"><span data-stu-id="fdba7-278">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="fdba7-279">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdba7-279">Requirements</span></span>



| <span data-ttu-id="fdba7-280">需求</span><span class="sxs-lookup"><span data-stu-id="fdba7-280">Requirement</span></span> | <span data-ttu-id="fdba7-281">值</span><span class="sxs-lookup"><span data-stu-id="fdba7-281">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdba7-282">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdba7-282">Minimum supported client</span></span><br/> | <span data-ttu-id="fdba7-283">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-283">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fdba7-284">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdba7-284">Minimum supported server</span></span><br/> | <span data-ttu-id="fdba7-285">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fdba7-285">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fdba7-286">標頭</span><span class="sxs-lookup"><span data-stu-id="fdba7-286">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdba7-287"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-287"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fdba7-288">程式庫</span><span class="sxs-lookup"><span data-stu-id="fdba7-288">Library</span></span><br/>                  | <dl> <span data-ttu-id="fdba7-289"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-289"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fdba7-290">DLL</span><span class="sxs-lookup"><span data-stu-id="fdba7-290">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdba7-291"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdba7-291"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdba7-292">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdba7-292">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdba7-293">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fdba7-293">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fdba7-294">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="fdba7-294">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="fdba7-295">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="fdba7-295">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="fdba7-296">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fdba7-296">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fdba7-297">**glFog**</span><span class="sxs-lookup"><span data-stu-id="fdba7-297">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="fdba7-298">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="fdba7-298">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="fdba7-299">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="fdba7-299">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="fdba7-300">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="fdba7-300">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="fdba7-301">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="fdba7-301">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="fdba7-302">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="fdba7-302">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="fdba7-303">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="fdba7-303">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="fdba7-304">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="fdba7-304">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





