---
title: 'glColor3f 函式 (Gl) '
description: '設定目前的色彩。 |glColor3f 函式 (Gl) '
ms.assetid: 3d6706f4-1028-4b23-b956-720f5611cd88
keywords:
- glColor3f 函式 OpenGL
topic_type:
- apiref
api_name:
- glColor3f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd58db9ed0111f854f5580a8865d2e919a84a959
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853931"
---
# <a name="glcolor3f-function"></a><span data-ttu-id="8b120-105">glColor3f 函式</span><span class="sxs-lookup"><span data-stu-id="8b120-105">glColor3f function</span></span>

<span data-ttu-id="8b120-106">設定目前的色彩。</span><span class="sxs-lookup"><span data-stu-id="8b120-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b120-107">語法</span><span class="sxs-lookup"><span data-stu-id="8b120-107">Syntax</span></span>


```C++
void WINAPI glColor3f(
   GLfloat red,
   GLfloat green,
   GLfloat blue
);
```



## <a name="parameters"></a><span data-ttu-id="8b120-108">參數</span><span class="sxs-lookup"><span data-stu-id="8b120-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b120-109">*紅*</span><span class="sxs-lookup"><span data-stu-id="8b120-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="8b120-110">目前色彩的新紅色值。</span><span class="sxs-lookup"><span data-stu-id="8b120-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="8b120-111">*綠色*</span><span class="sxs-lookup"><span data-stu-id="8b120-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="8b120-112">目前色彩的新綠色值。</span><span class="sxs-lookup"><span data-stu-id="8b120-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="8b120-113">*藍色*</span><span class="sxs-lookup"><span data-stu-id="8b120-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="8b120-114">目前色彩的新藍色值。</span><span class="sxs-lookup"><span data-stu-id="8b120-114">The new blue value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b120-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b120-115">Return value</span></span>

<span data-ttu-id="8b120-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8b120-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b120-117">備註</span><span class="sxs-lookup"><span data-stu-id="8b120-117">Remarks</span></span>

<span data-ttu-id="8b120-118">GL 會儲存目前的單一值色彩索引和目前的四值 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="8b120-118">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="8b120-119">**glcolor** 會設定新的四值 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="8b120-119">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="8b120-120">**glcolor** 有兩個主要變異： **glcolor3** 和 **glcolor4**。</span><span class="sxs-lookup"><span data-stu-id="8b120-120">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="8b120-121">**glcolor3** 變體會明確指定新的紅色、綠色和藍色值，並將目前的 Alpha 值設定為1.0， (以隱含的方式) 完全濃度。</span><span class="sxs-lookup"><span data-stu-id="8b120-121">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="8b120-122">**glcolor4** variant 會明確指定全部四個色彩元件。</span><span class="sxs-lookup"><span data-stu-id="8b120-122">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="8b120-123">**glcolor3b**、 **glcolor4b**、 **glcolor3s**、 **glcolor4s**、 **glcolor3i** 和 **glcolor4i** 會採用三個或四個帶正負號的位元組、短或長整數作為引數。</span><span class="sxs-lookup"><span data-stu-id="8b120-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="8b120-124">當 v 附加至名稱時，color 命令可取得此類值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="8b120-124">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="8b120-125">目前的色彩值會以浮點格式儲存，並具有未指定的尾數和指數大小。</span><span class="sxs-lookup"><span data-stu-id="8b120-125">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="8b120-126">指定時，不帶正負號的整數色彩元件會以線性方式對應至浮點值，因此最大的可表示值會對應至 1.0 (滿濃度) ，而0對應至 0.0 (零濃度) 。</span><span class="sxs-lookup"><span data-stu-id="8b120-126">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="8b120-127">經過指定時，帶正負號的整數色彩元件會以線性方式對應至浮點值，因此最大的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="8b120-127">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="8b120-128"> (請注意，此對應不會精確地將0轉換為0.0。 ) 浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="8b120-128">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="8b120-129">浮點數或帶正負號的整數值都不會在 \[ \] 目前的色彩更新之前壓制至範圍0、1。</span><span class="sxs-lookup"><span data-stu-id="8b120-129">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="8b120-130">不過，在將色彩元件插入或寫入至色彩緩衝區之前，會將色彩元件壓制至這個範圍。</span><span class="sxs-lookup"><span data-stu-id="8b120-130">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b120-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b120-131">Requirements</span></span>



| <span data-ttu-id="8b120-132">需求</span><span class="sxs-lookup"><span data-stu-id="8b120-132">Requirement</span></span> | <span data-ttu-id="8b120-133">值</span><span class="sxs-lookup"><span data-stu-id="8b120-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b120-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b120-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8b120-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b120-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8b120-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b120-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8b120-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b120-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8b120-138">標頭</span><span class="sxs-lookup"><span data-stu-id="8b120-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b120-139"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="8b120-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8b120-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="8b120-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b120-141"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b120-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8b120-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8b120-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b120-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b120-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b120-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b120-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b120-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8b120-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8b120-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8b120-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8b120-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="8b120-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="8b120-148">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="8b120-148">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





