---
title: 'glGetColorTableParameterfvEXT 函式 (Gl) '
description: 'GlGetColorTableParameterfvEXT 和 glGetColorTableParameterivEXT 函數會從色彩資料表取得調色板參數。 |glGetColorTableParameterfvEXT 函式 (Gl) '
ms.assetid: e78051aa-4233-413c-8838-0741b54eab0e
keywords:
- glGetColorTableParameterfvEXT 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterfvEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533ca0c847548fa1de4518079ca6e49d15b6830f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104386388"
---
# <a name="glgetcolortableparameterfvext-function"></a><span data-ttu-id="ec5b7-105">glGetColorTableParameterfvEXT 函式</span><span class="sxs-lookup"><span data-stu-id="ec5b7-105">glGetColorTableParameterfvEXT function</span></span>

<span data-ttu-id="ec5b7-106">**GlGetColorTableParameterfvEXT** 和 [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)函數會從色彩資料表取得調色板參數。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-106">The **glGetColorTableParameterfvEXT** and [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) functions get palette parameters from color tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec5b7-107">語法</span><span class="sxs-lookup"><span data-stu-id="ec5b7-107">Syntax</span></span>


```C++
void WINAPI glGetColorTableParameterfvEXT(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="ec5b7-108">參數</span><span class="sxs-lookup"><span data-stu-id="ec5b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec5b7-109">*目標*</span><span class="sxs-lookup"><span data-stu-id="ec5b7-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5b7-110">您要取得參數資料之調色板的目標紋理。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-110">The target texture of the palette for which you want parameter data.</span></span> <span data-ttu-id="ec5b7-111">必須是材質 \_ 1d、材質 \_ 2D、proxy \_ 材質 \_ 1d 或 proxy \_ 材質 \_ 2d。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-111">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="ec5b7-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="ec5b7-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5b7-113">*參數* 所指向之調色板參數資料類型的符號常數。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-113">A symbolic constant for the type of palette parameter data pointed to by *params*.</span></span>

<span data-ttu-id="ec5b7-114">以下是接受的符號常數及其意義。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-114">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="ec5b7-115">值</span><span class="sxs-lookup"><span data-stu-id="ec5b7-115">Value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="ec5b7-116">意義</span><span class="sxs-lookup"><span data-stu-id="ec5b7-116">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <span data-ttu-id="ec5b7-117"><dt>**GL \_ 色彩 \_ 表 \_ 格式 \_ EXT**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5b7-117"><dt>**GL\_COLOR\_TABLE\_FORMAT\_EXT**</dt></span></span> </dl>              | <span data-ttu-id="ec5b7-118">傳回最新的 [**glColorTableEXT**](glcolortableext.md) 呼叫所指定的內部格式或預設值。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-118">Return the internal format specified by the most recent call to [**glColorTableEXT**](glcolortableext.md) or the default value.</span></span><br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <span data-ttu-id="ec5b7-119"><dt>**GL \_ 色彩 \_ 資料表 \_ 寬度 \_ EXT**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5b7-119"><dt>**GL\_COLOR\_TABLE\_WIDTH\_EXT**</dt></span></span> </dl>                 | <span data-ttu-id="ec5b7-120">傳回目前調色板的寬度。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-120">Return the width of the current palette.</span></span><br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <span data-ttu-id="ec5b7-121"><dt>**GL \_ 色彩 \_ 表 \_ 紅色 \_ 大小 \_ EXT**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5b7-121"><dt>**GL\_COLOR\_TABLE\_RED\_SIZE\_EXT**</dt></span></span> </dl>       | <span data-ttu-id="ec5b7-122">傳回在內部用來儲存調色板資料之紅色元件的實際大小。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-122">Return the actual size used internally to store the red component of the palette data.</span></span><br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <span data-ttu-id="ec5b7-123"><dt>**GL \_ 色彩 \_ 表 \_ 綠色 \_ 大小 \_ EXT**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5b7-123"><dt>**GL\_COLOR\_TABLE\_GREEN\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="ec5b7-124">傳回在內部用來儲存調色板資料之綠色元件的實際大小。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-124">Return the actual size used internally to store the green component of the palette data.</span></span><br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <span data-ttu-id="ec5b7-125"><dt>**GL \_ 色彩 \_ 表 \_ 藍色 \_ 大小 \_ EXT**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5b7-125"><dt>**GL\_COLOR\_TABLE\_BLUE\_SIZE\_EXT**</dt></span></span> </dl>    | <span data-ttu-id="ec5b7-126">傳回在內部用來儲存調色板資料藍色元件的實際大小。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-126">Return the actual size used internally to store the blue component of the palette data.</span></span><br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <span data-ttu-id="ec5b7-127"><dt>**GL \_ 色彩 \_ 表 \_ ALPHA \_ 大小 \_ EXT**</dt></span><span class="sxs-lookup"><span data-stu-id="ec5b7-127"><dt>**GL\_COLOR\_TABLE\_ALPHA\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="ec5b7-128">傳回在內部用來儲存調色板資料 Alpha 元件的實際大小。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-128">Return the actual size used internally to store the alpha component of the palette data.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="ec5b7-129">*params*</span><span class="sxs-lookup"><span data-stu-id="ec5b7-129">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5b7-130">指向 *pname* 參數所指定的色彩資料表參數資料。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-130">Points to the color table parameter data specified by the *pname* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec5b7-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec5b7-131">Return value</span></span>

<span data-ttu-id="ec5b7-132">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-132">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec5b7-133">備註</span><span class="sxs-lookup"><span data-stu-id="ec5b7-133">Remarks</span></span>

<span data-ttu-id="ec5b7-134">您可以使用 **glGetColorTableParameterivEXT** 和 **glGetColorTableParameterfvEXT** 函式，從以 [**glColorTableEXT**](glcolortableext.md) 為目標材質調色板設定的色彩資料表中取出特定的參數資料。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-134">You use the **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** functions to retrieve specific parameter data from color tables set with [**glColorTableEXT**](glcolortableext.md) for targeted texture palettes.</span></span> <span data-ttu-id="ec5b7-135">此外，您也可以使用這些函數來判斷 **glGetColorTableEXT** 傳回的色彩資料表專案數目。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-135">Also you can use these functions to determine the number of color table entries that **glGetColorTableEXT** returns.</span></span>

<span data-ttu-id="ec5b7-136">當 *目標* 參數為 GL \_ proxy \_ 材質 \_ 1d 或 GL \_ proxy \_ 材質 \_ 2d，且執行不支援針對 *格式* 或 *寬度* 指定的值時， **glColorTableEXT** 可能無法建立要求的色彩表。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-136">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="ec5b7-137">在此情況下，color 資料表是空的，而且所有取出的參數都是零。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-137">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="ec5b7-138">您可以藉由使用 proxy 目標呼叫 **glColorTableEXT** ，然後呼叫 **glGetColorTableParameterivEXT** 或 **glGetColorTableParameterfvEXT** 來判斷 width 參數是否符合 **GlColorTableEXT** 所設定的，來判斷 OpenGL 是否支援特定的色彩表格式和大小。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-138">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling **glGetColorTableParameterivEXT** or **glGetColorTableParameterfvEXT** to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="ec5b7-139">如果取出的寬度為零，則 **glColorTable** 的色彩表格要求會失敗。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-139">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="ec5b7-140">如果取出的寬度不是零，您可以使用紋理1d 或材質2d 的真實目標來呼叫 **glColorTable** ， \_ \_ 以設定色彩表。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-140">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

<span data-ttu-id="ec5b7-141">**GlGetColorTableParameterivEXT** 和 **glGetColorTableParameterfvEXT** 函式是延伸函式，這些函式不是標準 OpenGL 程式庫的一部分，而是 GL \_ EXT \_ 材質擴充功能的一部分 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-141">The **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** functions are extension functions that are not part of the standard OpenGL library but are part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="ec5b7-142">若要檢查 OpenGL 的執行是否支援 **glGetColorTableParameterivEXT** 和 **glGetColorTableParameterfvEXT**，請) **(** GL 延伸模組呼叫 [**glGetString**](glgetstring.md) \_ \*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-142">To check whether your implementation of OpenGL supports **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT**, call [**glGetString**](glgetstring.md)**(** GL\_EXTENSIONS **)**.</span></span> <span data-ttu-id="ec5b7-143">如果它傳回 GL \_ EXT \_ \_ （調色板）材質，則支援 **glGetColorTableParameterivEXT** 和 **glGetColorTableParameterfvEXT** 。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-143">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** are supported.</span></span> <span data-ttu-id="ec5b7-144">若要取得擴充函數的函式位址，請呼叫 [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)。</span><span class="sxs-lookup"><span data-stu-id="ec5b7-144">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec5b7-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec5b7-145">Requirements</span></span>



| <span data-ttu-id="ec5b7-146">需求</span><span class="sxs-lookup"><span data-stu-id="ec5b7-146">Requirement</span></span> | <span data-ttu-id="ec5b7-147">值</span><span class="sxs-lookup"><span data-stu-id="ec5b7-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="ec5b7-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec5b7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ec5b7-149">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec5b7-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="ec5b7-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec5b7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ec5b7-151">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec5b7-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ec5b7-152">標頭</span><span class="sxs-lookup"><span data-stu-id="ec5b7-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec5b7-153"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="ec5b7-153"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec5b7-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec5b7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5b7-155">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="ec5b7-155">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="ec5b7-156">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="ec5b7-156">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="ec5b7-157">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="ec5b7-157">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="ec5b7-158">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="ec5b7-158">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="ec5b7-159">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="ec5b7-159">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





