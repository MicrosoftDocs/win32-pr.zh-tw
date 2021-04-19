---
title: 'glColor4us 函式 (Gl) '
description: '設定目前的色彩。 |glColor4us 函式 (Gl) '
ms.assetid: 800ab5f7-bf42-4df6-8f3f-64df651240bd
keywords:
- glColor4us 函式 OpenGL
topic_type:
- apiref
api_name:
- glColor4us
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be59d11c944febe7149c78d0abc7444cd11d146
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986485"
---
# <a name="glcolor4us-function"></a><span data-ttu-id="02eae-105">glColor4us 函式</span><span class="sxs-lookup"><span data-stu-id="02eae-105">glColor4us function</span></span>

<span data-ttu-id="02eae-106">設定目前的色彩。</span><span class="sxs-lookup"><span data-stu-id="02eae-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="02eae-107">語法</span><span class="sxs-lookup"><span data-stu-id="02eae-107">Syntax</span></span>


```C++
void WINAPI glColor4us(
   GLushort red,
   GLushort green,
   GLushort blue,
   GLushort alpha
);
```



## <a name="parameters"></a><span data-ttu-id="02eae-108">參數</span><span class="sxs-lookup"><span data-stu-id="02eae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02eae-109">*紅*</span><span class="sxs-lookup"><span data-stu-id="02eae-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="02eae-110">目前色彩的新紅色值。</span><span class="sxs-lookup"><span data-stu-id="02eae-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="02eae-111">*綠色*</span><span class="sxs-lookup"><span data-stu-id="02eae-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="02eae-112">目前色彩的新綠色值。</span><span class="sxs-lookup"><span data-stu-id="02eae-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="02eae-113">*藍色*</span><span class="sxs-lookup"><span data-stu-id="02eae-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="02eae-114">目前色彩的新藍色值。</span><span class="sxs-lookup"><span data-stu-id="02eae-114">The new blue value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="02eae-115">*阿 爾 法*</span><span class="sxs-lookup"><span data-stu-id="02eae-115">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="02eae-116">目前色彩的新 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="02eae-116">The new alpha value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02eae-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="02eae-117">Return value</span></span>

<span data-ttu-id="02eae-118">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="02eae-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02eae-119">備註</span><span class="sxs-lookup"><span data-stu-id="02eae-119">Remarks</span></span>

<span data-ttu-id="02eae-120">GL 會儲存目前的單一值色彩索引和目前的四值 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="02eae-120">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="02eae-121">**glcolor** 會設定新的四值 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="02eae-121">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="02eae-122">**glcolor** 有兩個主要變異： **glcolor3** 和 **glcolor4**。</span><span class="sxs-lookup"><span data-stu-id="02eae-122">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="02eae-123">**glcolor3** 變體會明確指定新的紅色、綠色和藍色值，並將目前的 Alpha 值設定為1.0， (以隱含的方式) 完全濃度。</span><span class="sxs-lookup"><span data-stu-id="02eae-123">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="02eae-124">**glcolor4** variant 會明確指定全部四個色彩元件。</span><span class="sxs-lookup"><span data-stu-id="02eae-124">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="02eae-125">**glcolor3b**、 **glcolor4b**、 **glcolor3s**、 **glcolor4s**、 **glcolor3i** 和 **glcolor4i** 會採用三個或四個帶正負號的位元組、短或長整數作為引數。</span><span class="sxs-lookup"><span data-stu-id="02eae-125">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="02eae-126">當 v 附加至名稱時，color 命令可取得此類值陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="02eae-126">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="02eae-127">目前的色彩值會以浮點格式儲存，並具有未指定的尾數和指數大小。</span><span class="sxs-lookup"><span data-stu-id="02eae-127">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="02eae-128">指定時，不帶正負號的整數色彩元件會以線性方式對應至浮點值，因此最大的可表示值會對應至 1.0 (滿濃度) ，而0對應至 0.0 (零濃度) 。</span><span class="sxs-lookup"><span data-stu-id="02eae-128">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="02eae-129">經過指定時，帶正負號的整數色彩元件會以線性方式對應至浮點值，因此最大的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。</span><span class="sxs-lookup"><span data-stu-id="02eae-129">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="02eae-130"> (請注意，此對應不會精確地將0轉換為0.0。 ) 浮點值會直接對應。</span><span class="sxs-lookup"><span data-stu-id="02eae-130">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="02eae-131">浮點數或帶正負號的整數值都不會在 \[ \] 目前的色彩更新之前壓制至範圍0、1。</span><span class="sxs-lookup"><span data-stu-id="02eae-131">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="02eae-132">不過，在將色彩元件插入或寫入至色彩緩衝區之前，會將色彩元件壓制至這個範圍。</span><span class="sxs-lookup"><span data-stu-id="02eae-132">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="02eae-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="02eae-133">Requirements</span></span>



| <span data-ttu-id="02eae-134">需求</span><span class="sxs-lookup"><span data-stu-id="02eae-134">Requirement</span></span> | <span data-ttu-id="02eae-135">值</span><span class="sxs-lookup"><span data-stu-id="02eae-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02eae-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02eae-136">Minimum supported client</span></span><br/> | <span data-ttu-id="02eae-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02eae-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="02eae-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02eae-138">Minimum supported server</span></span><br/> | <span data-ttu-id="02eae-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02eae-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02eae-140">標頭</span><span class="sxs-lookup"><span data-stu-id="02eae-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="02eae-141"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="02eae-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="02eae-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="02eae-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="02eae-143"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="02eae-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="02eae-144">DLL</span><span class="sxs-lookup"><span data-stu-id="02eae-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02eae-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02eae-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02eae-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02eae-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02eae-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="02eae-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="02eae-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="02eae-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="02eae-149">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="02eae-149">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="02eae-150">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="02eae-150">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 





