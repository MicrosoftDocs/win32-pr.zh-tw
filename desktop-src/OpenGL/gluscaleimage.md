---
title: 'gluScaleImage 函式 (X.glu 隊) '
description: GluScaleImage 函式會將影像調整為任意大小。
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- gluScaleImage 函式 OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383837"
---
# <a name="gluscaleimage-function"></a><span data-ttu-id="17bfb-104">gluScaleImage 函式</span><span class="sxs-lookup"><span data-stu-id="17bfb-104">gluScaleImage function</span></span>

<span data-ttu-id="17bfb-105">**GluScaleImage** 函式會將影像調整為任意大小。</span><span class="sxs-lookup"><span data-stu-id="17bfb-105">The **gluScaleImage** function scales an image to an arbitrary size.</span></span>

## <a name="syntax"></a><span data-ttu-id="17bfb-106">語法</span><span class="sxs-lookup"><span data-stu-id="17bfb-106">Syntax</span></span>


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a><span data-ttu-id="17bfb-107">參數</span><span class="sxs-lookup"><span data-stu-id="17bfb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17bfb-108">*format*</span><span class="sxs-lookup"><span data-stu-id="17bfb-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="17bfb-109">圖元資料的格式。</span><span class="sxs-lookup"><span data-stu-id="17bfb-109">The format of the pixel data.</span></span> <span data-ttu-id="17bfb-110">下列符號值有效： GL \_ 色彩 \_ 索引、gl 樣板 \_ \_ 索引、GL \_ 深度 \_ 元件、GL \_ RED、gl \_ 綠、gl \_ BLUE、GL \_ ALPHA、GL \_ RGB、GL \_ RGBA、GL \_ BGR \_ EXT、gl \_ BGRA \_ EXT、gl \_ 亮度，以及 gl \_ 亮度 \_ ALPHA。</span><span class="sxs-lookup"><span data-stu-id="17bfb-110">The following symbolic values are valid: GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, GL\_DEPTH\_COMPONENT, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="17bfb-111">*widthin*</span><span class="sxs-lookup"><span data-stu-id="17bfb-111">*widthin*</span></span> 
</dt> <dd>

<span data-ttu-id="17bfb-112">調整的來源影像寬度。</span><span class="sxs-lookup"><span data-stu-id="17bfb-112">The width of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="17bfb-113">*heightin*</span><span class="sxs-lookup"><span data-stu-id="17bfb-113">*heightin*</span></span> 
</dt> <dd>

<span data-ttu-id="17bfb-114">調整的來源影像高度。</span><span class="sxs-lookup"><span data-stu-id="17bfb-114">The height of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="17bfb-115">*typein*</span><span class="sxs-lookup"><span data-stu-id="17bfb-115">*typein*</span></span> 
</dt> <dd>

<span data-ttu-id="17bfb-116">*描述* 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="17bfb-116">The data type for *datain*.</span></span> <span data-ttu-id="17bfb-117">必須是下列其中一項： GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、GL \_ 點陣圖、gl 不 \_ 帶正負號 \_ 的 short、gl \_ short、GL 不 \_ 帶正負號 \_ int、gl \_ int 或 gl \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="17bfb-117">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="17bfb-118">*描述*</span><span class="sxs-lookup"><span data-stu-id="17bfb-118">*datain*</span></span> 
</dt> <dd>

<span data-ttu-id="17bfb-119">來源影像的指標。</span><span class="sxs-lookup"><span data-stu-id="17bfb-119">A pointer to the source image.</span></span>

</dd> <dt>

<span data-ttu-id="17bfb-120">*widthout*</span><span class="sxs-lookup"><span data-stu-id="17bfb-120">*widthout*</span></span> 
</dt> <dd>

<span data-ttu-id="17bfb-121">目的地影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="17bfb-121">The width of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="17bfb-122">*heightout*</span><span class="sxs-lookup"><span data-stu-id="17bfb-122">*heightout*</span></span> 
</dt> <dd>

<span data-ttu-id="17bfb-123">目的地影像的高度。</span><span class="sxs-lookup"><span data-stu-id="17bfb-123">The height of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="17bfb-124">*typeout*</span><span class="sxs-lookup"><span data-stu-id="17bfb-124">*typeout*</span></span> 
</dt> <dd>

<span data-ttu-id="17bfb-125">*Dataout* 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="17bfb-125">The data type for *dataout*.</span></span> <span data-ttu-id="17bfb-126">必須是下列其中一項： GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、GL \_ 點陣圖、gl 不 \_ 帶正負號 \_ 的 short、gl \_ short、GL 不 \_ 帶正負號 \_ int、gl \_ int 或 gl \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="17bfb-126">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="17bfb-127">*dataout*</span><span class="sxs-lookup"><span data-stu-id="17bfb-127">*dataout*</span></span> 
</dt> <dd>

<span data-ttu-id="17bfb-128">目的地影像的指標。</span><span class="sxs-lookup"><span data-stu-id="17bfb-128">A pointer to the destination image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17bfb-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="17bfb-129">Return value</span></span>

<span data-ttu-id="17bfb-130">如果此函式成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="17bfb-130">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="17bfb-131">如果函式失敗，則傳回值為 X.GLU 隊錯誤碼 (查看 [**gluErrorString**](gluerrorstring.md)) 。</span><span class="sxs-lookup"><span data-stu-id="17bfb-131">If the function fails, the return value is a GLU error code (see [**gluErrorString**](gluerrorstring.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="17bfb-132">備註</span><span class="sxs-lookup"><span data-stu-id="17bfb-132">Remarks</span></span>

<span data-ttu-id="17bfb-133">**GluScaleImage** 函式會使用適當的圖元存放區模式來調整圖元影像，以將資料從來源影像解壓縮，並將資料封裝到目的地影像。</span><span class="sxs-lookup"><span data-stu-id="17bfb-133">The **gluScaleImage** function scales a pixel image using the appropriate pixel store modes to unpack data from the source image and pack data into the destination image.</span></span>

<span data-ttu-id="17bfb-134">壓縮影像時， **gluScaleImage** 會使用 box 篩選器來取樣來源影像，並建立目的地影像的圖元。</span><span class="sxs-lookup"><span data-stu-id="17bfb-134">When shrinking an image, **gluScaleImage** uses a box filter to sample the source image and create pixels for the destination image.</span></span> <span data-ttu-id="17bfb-135">放大影像時，來源影像的圖元會以線性方式插入，以建立目的映射。</span><span class="sxs-lookup"><span data-stu-id="17bfb-135">When magnifying an image, the pixels from the source image are linearly interpolated to create the destination image.</span></span>

<span data-ttu-id="17bfb-136">如需 *format*、 *typein* 和 *typeout* 參數可接受值的描述，請參閱 [**glReadPixels**](glreadpixels.md)。</span><span class="sxs-lookup"><span data-stu-id="17bfb-136">For a description of the acceptable values for the *format*, *typein*, and *typeout* parameters, see [**glReadPixels**](glreadpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17bfb-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="17bfb-137">Requirements</span></span>



| <span data-ttu-id="17bfb-138">需求</span><span class="sxs-lookup"><span data-stu-id="17bfb-138">Requirement</span></span> | <span data-ttu-id="17bfb-139">值</span><span class="sxs-lookup"><span data-stu-id="17bfb-139">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17bfb-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17bfb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="17bfb-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17bfb-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="17bfb-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17bfb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="17bfb-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17bfb-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="17bfb-144">標頭</span><span class="sxs-lookup"><span data-stu-id="17bfb-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="17bfb-145"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="17bfb-145"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="17bfb-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="17bfb-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="17bfb-147"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="17bfb-147"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="17bfb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="17bfb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17bfb-149"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17bfb-149"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17bfb-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17bfb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17bfb-151">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="17bfb-151">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="17bfb-152">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="17bfb-152">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="17bfb-153">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="17bfb-153">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="17bfb-154">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="17bfb-154">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="17bfb-155">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="17bfb-155">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> </dl>

 

 





