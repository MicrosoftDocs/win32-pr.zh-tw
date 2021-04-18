---
title: 'gluBuild1DMipmaps 函式 (X.glu 隊) '
description: GluBuild1DMipmaps 函式會建立1個 mipmap。
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- gluBuild1DMipmaps 函式 OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967328"
---
# <a name="glubuild1dmipmaps-function"></a><span data-ttu-id="c7495-104">gluBuild1DMipmaps 函式</span><span class="sxs-lookup"><span data-stu-id="c7495-104">gluBuild1DMipmaps function</span></span>

<span data-ttu-id="c7495-105">**GluBuild1DMipmaps** 函式會建立1個 mipmap。</span><span class="sxs-lookup"><span data-stu-id="c7495-105">The **gluBuild1DMipmaps** function creates 1-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7495-106">語法</span><span class="sxs-lookup"><span data-stu-id="c7495-106">Syntax</span></span>


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="c7495-107">參數</span><span class="sxs-lookup"><span data-stu-id="c7495-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7495-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="c7495-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="c7495-109">目標材質。</span><span class="sxs-lookup"><span data-stu-id="c7495-109">The target texture.</span></span> <span data-ttu-id="c7495-110">必須是 GL \_ 紋理 \_ 1d。</span><span class="sxs-lookup"><span data-stu-id="c7495-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="c7495-111">*元件*</span><span class="sxs-lookup"><span data-stu-id="c7495-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="c7495-112">材質中的色彩元件數目。</span><span class="sxs-lookup"><span data-stu-id="c7495-112">The number of color components in the texture.</span></span> <span data-ttu-id="c7495-113">必須是1、2、3或4。</span><span class="sxs-lookup"><span data-stu-id="c7495-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="c7495-114">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="c7495-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="c7495-115">材質影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="c7495-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="c7495-116">*format*</span><span class="sxs-lookup"><span data-stu-id="c7495-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="c7495-117">圖元資料的格式。</span><span class="sxs-lookup"><span data-stu-id="c7495-117">The format of the pixel data.</span></span> <span data-ttu-id="c7495-118">下列值有效： GL \_ 色彩 \_ 索引、gl \_ RED、GL \_ 綠、gl \_ BLUE、gl \_ ALPHA、GL \_ RGB、GL \_ RGBA、GL \_ BGR \_ EXT、gl \_ BGRA \_ EXT、gl \_ 亮度或 gl \_ 亮度 \_ ALPHA。</span><span class="sxs-lookup"><span data-stu-id="c7495-118">The following values are valid: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="c7495-119">*type*</span><span class="sxs-lookup"><span data-stu-id="c7495-119">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="c7495-120">*資料* 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="c7495-120">The data type for *data*.</span></span> <span data-ttu-id="c7495-121">下列值有效： GL 不 \_ 帶正負號 \_ 的位元組、gl \_ 位元組、GL \_ 點陣圖、gl \_ 未簽署 \_ 短、gl \_ 簡短、GL 不 \_ 帶正負號 \_ int、gl \_ int 或 GL \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="c7495-121">The following values are valid: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="c7495-122">*data*</span><span class="sxs-lookup"><span data-stu-id="c7495-122">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="c7495-123">記憶體中影像資料的指標。</span><span class="sxs-lookup"><span data-stu-id="c7495-123">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7495-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7495-124">Return value</span></span>

<span data-ttu-id="c7495-125">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c7495-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7495-126">備註</span><span class="sxs-lookup"><span data-stu-id="c7495-126">Remarks</span></span>

<span data-ttu-id="c7495-127">**GluBuild1DMipmaps** 函式會取得輸入影像，並使用 [**gluScaleImage**](gluscaleimage.md)) 產生 (的所有 mipmap 影像，以便輸入影像可作為 mipmapped 材質影像使用。</span><span class="sxs-lookup"><span data-stu-id="c7495-127">The **gluBuild1DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so that the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="c7495-128">接著會呼叫 [**glTexImage1D**](glteximage1d.md) 函式來載入每個影像。</span><span class="sxs-lookup"><span data-stu-id="c7495-128">The [**glTexImage1D**](glteximage1d.md) function is then called to load each of the images.</span></span> <span data-ttu-id="c7495-129">如果輸入影像的寬度不是2的乘冪，則會在產生 mipmap 之前，將影像調整為最接近的兩次乘冪。</span><span class="sxs-lookup"><span data-stu-id="c7495-129">If the width of the input image is not a power of two, then the image is scaled to the nearest power of two before the mipmaps are generated.</span></span>

<span data-ttu-id="c7495-130">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="c7495-130">A return value of zero indicates success.</span></span> <span data-ttu-id="c7495-131">否則，會傳回 X.GLU 隊錯誤碼 (請參閱 [**gluErrorString**](gluerrorstring.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c7495-131">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="c7495-132">如需 *格式* 參數可接受值的描述，請參閱 **glTexImage1D**。</span><span class="sxs-lookup"><span data-stu-id="c7495-132">For a description of the acceptable values for the *format* parameter, see **glTexImage1D**.</span></span> <span data-ttu-id="c7495-133">如需 *類型* 參數可接受值的描述，請參閱 [**glDrawPixels**](gldrawpixels.md)。</span><span class="sxs-lookup"><span data-stu-id="c7495-133">For a description of the acceptable values for the *type* parameter, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7495-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7495-134">Requirements</span></span>



| <span data-ttu-id="c7495-135">需求</span><span class="sxs-lookup"><span data-stu-id="c7495-135">Requirement</span></span> | <span data-ttu-id="c7495-136">值</span><span class="sxs-lookup"><span data-stu-id="c7495-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c7495-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7495-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c7495-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7495-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c7495-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7495-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c7495-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7495-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c7495-141">標頭</span><span class="sxs-lookup"><span data-stu-id="c7495-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7495-142"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7495-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="c7495-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7495-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7495-144"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7495-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c7495-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c7495-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7495-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7495-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7495-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7495-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7495-148">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="c7495-148">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="c7495-149">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="c7495-149">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="c7495-150">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="c7495-150">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="c7495-151">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="c7495-151">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





