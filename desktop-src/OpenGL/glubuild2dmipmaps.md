---
title: 'gluBuild2DMipmaps 函式 (X.glu 隊) '
description: GluBuild2DMipmaps 函式會建立 2D mipmap。
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- gluBuild2DMipmaps 函式 OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934077"
---
# <a name="glubuild2dmipmaps-function"></a><span data-ttu-id="6903d-104">gluBuild2DMipmaps 函式</span><span class="sxs-lookup"><span data-stu-id="6903d-104">gluBuild2DMipmaps function</span></span>

<span data-ttu-id="6903d-105">**GluBuild2DMipmaps** 函式會建立 2d mipmap。</span><span class="sxs-lookup"><span data-stu-id="6903d-105">The **gluBuild2DMipmaps** function creates 2-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="6903d-106">語法</span><span class="sxs-lookup"><span data-stu-id="6903d-106">Syntax</span></span>


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="6903d-107">參數</span><span class="sxs-lookup"><span data-stu-id="6903d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6903d-108">*目標*</span><span class="sxs-lookup"><span data-stu-id="6903d-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="6903d-109">目標材質。</span><span class="sxs-lookup"><span data-stu-id="6903d-109">The target texture.</span></span> <span data-ttu-id="6903d-110">必須是 GL \_ 紋理 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="6903d-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="6903d-111">*元件*</span><span class="sxs-lookup"><span data-stu-id="6903d-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="6903d-112">材質中的色彩元件數目。</span><span class="sxs-lookup"><span data-stu-id="6903d-112">The number of color components in the texture.</span></span> <span data-ttu-id="6903d-113">必須是1、2、3或4。</span><span class="sxs-lookup"><span data-stu-id="6903d-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="6903d-114">*width* (寬度)</span><span class="sxs-lookup"><span data-stu-id="6903d-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="6903d-115">材質影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="6903d-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="6903d-116">*height* (高度)</span><span class="sxs-lookup"><span data-stu-id="6903d-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="6903d-117">材質影像的高度。</span><span class="sxs-lookup"><span data-stu-id="6903d-117">The height of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="6903d-118">*format*</span><span class="sxs-lookup"><span data-stu-id="6903d-118">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="6903d-119">圖元資料的格式。</span><span class="sxs-lookup"><span data-stu-id="6903d-119">The format of the pixel data.</span></span> <span data-ttu-id="6903d-120">必須是下列其中一項： GL \_ 色彩 \_ 索引、gl \_ RED、GL \_ 綠、gl \_ BLUE、gl \_ ALPHA、GL \_ RGB、GL \_ RGBA、GL \_ BGR \_ EXT、gl \_ BGRA \_ EXT、gl \_ 亮度或 GL \_ 亮度 \_ ALPHA。</span><span class="sxs-lookup"><span data-stu-id="6903d-120">Must be one of the following: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="6903d-121">*type*</span><span class="sxs-lookup"><span data-stu-id="6903d-121">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="6903d-122">*資料* 的資料類型。</span><span class="sxs-lookup"><span data-stu-id="6903d-122">The data type for *data*.</span></span> <span data-ttu-id="6903d-123">必須是下列其中一項： GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、GL \_ 點陣圖、gl 不 \_ 帶正負號 \_ 的 short、gl \_ short、GL 不 \_ 帶正負號 \_ int、gl \_ int 或 gl \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="6903d-123">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="6903d-124">*data*</span><span class="sxs-lookup"><span data-stu-id="6903d-124">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="6903d-125">記憶體中影像資料的指標。</span><span class="sxs-lookup"><span data-stu-id="6903d-125">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6903d-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="6903d-126">Return value</span></span>

<span data-ttu-id="6903d-127">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6903d-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6903d-128">備註</span><span class="sxs-lookup"><span data-stu-id="6903d-128">Remarks</span></span>

<span data-ttu-id="6903d-129">**GluBuild2DMipmaps** 函式會取得輸入影像，並使用 [**gluScaleImage**](gluscaleimage.md)) 來產生所有的 Mipmap (影像，以便輸入影像可作為 mipmapped 材質影像。</span><span class="sxs-lookup"><span data-stu-id="6903d-129">The **gluBuild2DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="6903d-130">若要載入每個影像，請呼叫 [**glTexImage2D**](glteximage2d.md)。</span><span class="sxs-lookup"><span data-stu-id="6903d-130">To load each of the images, call [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="6903d-131">如果輸入影像的尺寸不是二的乘冪，則會調整影像大小，使寬度和高度在 mipmap 產生之前都是兩個的乘冪。</span><span class="sxs-lookup"><span data-stu-id="6903d-131">If the dimensions of the input image are not powers of two, then the image is scaled so that both the width and height are powers of two before the mipmaps are generated.</span></span>

<span data-ttu-id="6903d-132">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="6903d-132">A return value of zero indicates success.</span></span> <span data-ttu-id="6903d-133">否則，會傳回 X.GLU 隊錯誤碼 (請參閱 [**gluErrorString**](gluerrorstring.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6903d-133">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="6903d-134">如需 *格式* 參數可接受值的描述，請參閱 **glTexImage2D**。</span><span class="sxs-lookup"><span data-stu-id="6903d-134">For a description of the acceptable values for the *format* parameter, see **glTexImage2D**.</span></span> <span data-ttu-id="6903d-135">如需 *類型* 可接受值的描述，請參閱 [**glDrawPixels**](gldrawpixels.md)。</span><span class="sxs-lookup"><span data-stu-id="6903d-135">For a description of the acceptable values for *type*, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6903d-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="6903d-136">Requirements</span></span>



| <span data-ttu-id="6903d-137">需求</span><span class="sxs-lookup"><span data-stu-id="6903d-137">Requirement</span></span> | <span data-ttu-id="6903d-138">值</span><span class="sxs-lookup"><span data-stu-id="6903d-138">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6903d-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6903d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6903d-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6903d-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6903d-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6903d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6903d-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6903d-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6903d-143">標頭</span><span class="sxs-lookup"><span data-stu-id="6903d-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="6903d-144"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="6903d-144"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="6903d-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="6903d-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="6903d-146"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6903d-146"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6903d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="6903d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6903d-148"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6903d-148"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6903d-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6903d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6903d-150">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="6903d-150">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="6903d-151">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="6903d-151">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="6903d-152">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="6903d-152">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="6903d-153">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="6903d-153">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 





