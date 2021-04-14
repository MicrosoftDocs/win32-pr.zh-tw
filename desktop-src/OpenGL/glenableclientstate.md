---
title: 'glEnableClientState 函式 (Gl) '
description: 'GlEnableClientState 和 glDisableClientState 函數會分別啟用和停用陣列。 |glEnableClientState 函式 (Gl) '
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- glEnableClientState 函式 OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e333a51d4c1fe0a5ff11c717790e03aa6d054a09
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322304"
---
# <a name="glenableclientstate-function"></a><span data-ttu-id="995e1-105">glEnableClientState 函式</span><span class="sxs-lookup"><span data-stu-id="995e1-105">glEnableClientState function</span></span>

<span data-ttu-id="995e1-106">**GlEnableClientState** 和 [**glDisableClientState**](gldisableclientstate.md)函數會分別啟用和停用陣列。</span><span class="sxs-lookup"><span data-stu-id="995e1-106">The **glEnableClientState** and [**glDisableClientState**](gldisableclientstate.md) functions enable and disable arrays respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="995e1-107">語法</span><span class="sxs-lookup"><span data-stu-id="995e1-107">Syntax</span></span>


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a><span data-ttu-id="995e1-108">參數</span><span class="sxs-lookup"><span data-stu-id="995e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="995e1-109">*array*</span><span class="sxs-lookup"><span data-stu-id="995e1-109">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="995e1-110">您要啟用或停用之陣列的符號常數。</span><span class="sxs-lookup"><span data-stu-id="995e1-110">A symbolic constant for the array you want to enable or disable.</span></span> <span data-ttu-id="995e1-111">此參數可以採用下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="995e1-111">This parameter can assume one of the following values.</span></span>



| <span data-ttu-id="995e1-112">值</span><span class="sxs-lookup"><span data-stu-id="995e1-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="995e1-113">意義</span><span class="sxs-lookup"><span data-stu-id="995e1-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <span data-ttu-id="995e1-114"><dt>**GL \_ 色彩 \_ 陣列**</dt></span><span class="sxs-lookup"><span data-stu-id="995e1-114"><dt>**GL\_COLOR\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="995e1-115">如果啟用，請使用色彩陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="995e1-115">If enabled, use color arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="995e1-116">另請參閱 [**glColorPointer**](glcolorpointer.md)。</span><span class="sxs-lookup"><span data-stu-id="995e1-116">See also [**glColorPointer**](glcolorpointer.md).</span></span><br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <span data-ttu-id="995e1-117"><dt>**GL \_ EDGE \_ 旗標 \_ 陣列**</dt></span><span class="sxs-lookup"><span data-stu-id="995e1-117"><dt>**GL\_EDGE\_FLAG\_ARRAY**</dt></span></span> </dl>             | <span data-ttu-id="995e1-118">如果啟用，請使用邊緣旗標陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="995e1-118">If enabled, use edge flag arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="995e1-119">另請參閱 [**glEdgeFlagPointer**](gledgeflagpointer.md)。</span><span class="sxs-lookup"><span data-stu-id="995e1-119">See also [**glEdgeFlagPointer**](gledgeflagpointer.md).</span></span><br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <span data-ttu-id="995e1-120"><dt>**GL \_ 索引 \_ 陣列**</dt></span><span class="sxs-lookup"><span data-stu-id="995e1-120"><dt>**GL\_INDEX\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="995e1-121">如果啟用，請使用索引陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="995e1-121">If enabled, use index arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="995e1-122">另請參閱 [**glIndexPointer**](glindexpointer.md)。</span><span class="sxs-lookup"><span data-stu-id="995e1-122">See also [**glIndexPointer**](glindexpointer.md).</span></span><br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <span data-ttu-id="995e1-123"><dt>**GL \_ 標準 \_ 陣列**</dt></span><span class="sxs-lookup"><span data-stu-id="995e1-123"><dt>**GL\_NORMAL\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="995e1-124">如果啟用，請使用一般陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="995e1-124">If enabled, use normal arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="995e1-125">另請參閱 [**glNormalPointer**](glnormalpointer.md)。</span><span class="sxs-lookup"><span data-stu-id="995e1-125">See also [**glNormalPointer**](glnormalpointer.md).</span></span><br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <span data-ttu-id="995e1-126"><dt>**GL \_ 紋理 \_ COORD \_ 陣列**</dt></span><span class="sxs-lookup"><span data-stu-id="995e1-126"><dt>**GL\_TEXTURE\_COORD\_ARRAY**</dt></span></span> </dl> | <span data-ttu-id="995e1-127">若已啟用，請使用紋理座標陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="995e1-127">If enabled, use texture coordinate arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="995e1-128">另請參閱 [**glTexCoordPointer**](gltexcoordpointer.md)。</span><span class="sxs-lookup"><span data-stu-id="995e1-128">See also [**glTexCoordPointer**](gltexcoordpointer.md).</span></span><br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <span data-ttu-id="995e1-129"><dt>**GL \_ 頂點 \_ 陣列**</dt></span><span class="sxs-lookup"><span data-stu-id="995e1-129"><dt>**GL\_VERTEX\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="995e1-130">如果啟用，請使用頂點陣列搭配 [**glArrayElement**](glarrayelement.md)、 [**glDrawElements**](gldrawelements.md)或 [**glDrawArrays**](gldrawarrays.md)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="995e1-130">If enabled, use vertex arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="995e1-131">另請參閱 [**glVertexPointer**](glvertexpointer.md)。</span><span class="sxs-lookup"><span data-stu-id="995e1-131">See also [**glVertexPointer**](glvertexpointer.md).</span></span><br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="995e1-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="995e1-132">Return value</span></span>

<span data-ttu-id="995e1-133">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="995e1-133">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="995e1-134">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="995e1-134">Error codes</span></span>

<span data-ttu-id="995e1-135">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="995e1-135">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="995e1-136">Name</span><span class="sxs-lookup"><span data-stu-id="995e1-136">Name</span></span>                                                                                             | <span data-ttu-id="995e1-137">意義</span><span class="sxs-lookup"><span data-stu-id="995e1-137">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="995e1-138"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="995e1-138"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="995e1-139">*陣列* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="995e1-139">*array* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="995e1-140">備註</span><span class="sxs-lookup"><span data-stu-id="995e1-140">Remarks</span></span>

<span data-ttu-id="995e1-141">**GlEnableClientState** 和 **glDisableClientState** 函式會啟用和停用各種個別的陣列。</span><span class="sxs-lookup"><span data-stu-id="995e1-141">The **glEnableClientState** and **glDisableClientState** functions enable and disable various individual arrays.</span></span> <span data-ttu-id="995e1-142">使用 [**glIsEnabled**](glisenabled.md) 或 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 來判斷任何功能目前的設定。</span><span class="sxs-lookup"><span data-stu-id="995e1-142">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="995e1-143">在對 [**glBegin**](glbegin.md)的呼叫和 [**glEnd**](glend.md)的對應呼叫之間呼叫 **glEnableClientState** 和 **glDisableClientState** 可能會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="995e1-143">Calling **glEnableClientState** and **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) can cause an error.</span></span> <span data-ttu-id="995e1-144">如果未產生任何錯誤，則行為是未定義的。</span><span class="sxs-lookup"><span data-stu-id="995e1-144">If no error is generated, the behavior is undefined.</span></span>

> [!Note]  
> <span data-ttu-id="995e1-145">**GlEnableClientState** 和 **glDisableClientState** 函式僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="995e1-145">The **glEnableClientState** and **glDisableClientState** functions are only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="995e1-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="995e1-146">Requirements</span></span>



| <span data-ttu-id="995e1-147">需求</span><span class="sxs-lookup"><span data-stu-id="995e1-147">Requirement</span></span> | <span data-ttu-id="995e1-148">值</span><span class="sxs-lookup"><span data-stu-id="995e1-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="995e1-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="995e1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="995e1-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="995e1-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="995e1-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="995e1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="995e1-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="995e1-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="995e1-153">標頭</span><span class="sxs-lookup"><span data-stu-id="995e1-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="995e1-154"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="995e1-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="995e1-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="995e1-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="995e1-156"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="995e1-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="995e1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="995e1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="995e1-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="995e1-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="995e1-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="995e1-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="995e1-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="995e1-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="995e1-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="995e1-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="995e1-162">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="995e1-162">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="995e1-163">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="995e1-163">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="995e1-164">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="995e1-164">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="995e1-165">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="995e1-165">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="995e1-166">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="995e1-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="995e1-167">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="995e1-167">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="995e1-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="995e1-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="995e1-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="995e1-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="995e1-170">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="995e1-170">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="995e1-171">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="995e1-171">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="995e1-172">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="995e1-172">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="995e1-173">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="995e1-173">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="995e1-174">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="995e1-174">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





