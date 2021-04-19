---
title: 'glColor3fv 函式 (Gl) '
description: '從已存在的色彩值陣列中設定目前的色彩。 |glColor3fv 函式 (Gl) '
ms.assetid: 4ffaaa7e-4fa3-45b8-acf0-850e1e9d9a60
keywords:
- glColor3fv 函式 OpenGL
topic_type:
- apiref
api_name:
- glColor3fv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234930f573d492fe03ef39b8d3217649322095aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997362"
---
# <a name="glcolor3fv-function"></a><span data-ttu-id="988a8-105">glColor3fv 函式</span><span class="sxs-lookup"><span data-stu-id="988a8-105">glColor3fv function</span></span>

<span data-ttu-id="988a8-106">從已存在的色彩值陣列中設定目前的色彩。</span><span class="sxs-lookup"><span data-stu-id="988a8-106">Sets the current color from an already existing array of color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="988a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="988a8-107">Syntax</span></span>


```C++
void WINAPI glColor3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="988a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="988a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="988a8-109">*V*</span><span class="sxs-lookup"><span data-stu-id="988a8-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="988a8-110">陣列的指標，其中包含紅色、綠色和藍色值。</span><span class="sxs-lookup"><span data-stu-id="988a8-110">A pointer to an array that contains red, green, and blue values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="988a8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="988a8-111">Return value</span></span>

<span data-ttu-id="988a8-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="988a8-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="988a8-113">備註</span><span class="sxs-lookup"><span data-stu-id="988a8-113">Remarks</span></span>

<span data-ttu-id="988a8-114">GL 會儲存目前的單一值色彩索引和目前的四值 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="988a8-114">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="988a8-115">**glcolor** 會設定新的四值 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="988a8-115">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="988a8-116">**glcolor** 有兩個主要變異： **glcolor3** 和 **glcolor4**。</span><span class="sxs-lookup"><span data-stu-id="988a8-116">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="988a8-117">**glcolor3** 變體會明確指定新的紅色、綠色和藍色值，並將目前的 Alpha 值設定為1.0， (以隱含的方式) 完全濃度。</span><span class="sxs-lookup"><span data-stu-id="988a8-117">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="988a8-118">**glcolor4** variant 會明確指定全部四個色彩元件。</span><span class="sxs-lookup"><span data-stu-id="988a8-118">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="988a8-119">**glcolor3b**、 **glcolor4b**、 **glcolor3s**、 **glcolor4s**、 **glcolor3i** 和 **glcolor4i** 會採用三個或四個帶正負號的位元組、短或長整數作為引數。</span><span class="sxs-lookup"><span data-stu-id="988a8-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="988a8-120">當 v 附加至名稱時，color 命令可取得此類值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="988a8-120">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="988a8-121">目前的色彩值會以浮點格式儲存，並具有未指定的尾數和指數大小。</span><span class="sxs-lookup"><span data-stu-id="988a8-121">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="988a8-122">指定時，不帶正負號的整數色彩元件會以線性方式對應至浮點值，因此最大的可表示值會對應至 1.0 (滿濃度) ，而0對應至 0.0 (零濃度) 。</span><span class="sxs-lookup"><span data-stu-id="988a8-122">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="988a8-123">經過指定時，帶正負號的整數色彩元件會以線性方式對應至浮點值，因此最大的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="988a8-123">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="988a8-124"> (請注意，此對應不會精確地將0轉換為0.0。 ) 浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="988a8-124">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="988a8-125">浮點數或帶正負號的整數值都不會在 \[ \] 目前的色彩更新之前壓制至範圍0、1。</span><span class="sxs-lookup"><span data-stu-id="988a8-125">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="988a8-126">不過，在將色彩元件插入或寫入至色彩緩衝區之前，會將色彩元件壓制至這個範圍。</span><span class="sxs-lookup"><span data-stu-id="988a8-126">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="988a8-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="988a8-127">Requirements</span></span>



| <span data-ttu-id="988a8-128">需求</span><span class="sxs-lookup"><span data-stu-id="988a8-128">Requirement</span></span> | <span data-ttu-id="988a8-129">值</span><span class="sxs-lookup"><span data-stu-id="988a8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="988a8-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="988a8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="988a8-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="988a8-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="988a8-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="988a8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="988a8-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="988a8-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="988a8-134">標頭</span><span class="sxs-lookup"><span data-stu-id="988a8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="988a8-135"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="988a8-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="988a8-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="988a8-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="988a8-137"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="988a8-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="988a8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="988a8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="988a8-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="988a8-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="988a8-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="988a8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="988a8-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="988a8-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="988a8-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="988a8-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="988a8-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="988a8-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="988a8-144">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="988a8-144">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





