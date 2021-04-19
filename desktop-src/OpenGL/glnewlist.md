---
title: 'glNewList 函式 (Gl) '
description: 'GlNewList 和 glEndList 函數會建立或取代顯示清單。 |glNewList 函式 (Gl) '
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- glNewList 函式 OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106985521"
---
# <a name="glnewlist-function"></a><span data-ttu-id="00ea8-105">glNewList 函式</span><span class="sxs-lookup"><span data-stu-id="00ea8-105">glNewList function</span></span>

<span data-ttu-id="00ea8-106">**GlNewList** 和 [**glEndList**](glendlist.md)函數會建立或取代顯示清單。</span><span class="sxs-lookup"><span data-stu-id="00ea8-106">The **glNewList** and [**glEndList**](glendlist.md) functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ea8-107">語法</span><span class="sxs-lookup"><span data-stu-id="00ea8-107">Syntax</span></span>


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="00ea8-108">參數</span><span class="sxs-lookup"><span data-stu-id="00ea8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ea8-109">*list*</span><span class="sxs-lookup"><span data-stu-id="00ea8-109">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="00ea8-110">顯示清單名稱。</span><span class="sxs-lookup"><span data-stu-id="00ea8-110">The display list name.</span></span>

</dd> <dt>

<span data-ttu-id="00ea8-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="00ea8-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="00ea8-112">編譯模式。</span><span class="sxs-lookup"><span data-stu-id="00ea8-112">The compilation mode.</span></span> <span data-ttu-id="00ea8-113">接受下列值。</span><span class="sxs-lookup"><span data-stu-id="00ea8-113">The following values are accepted.</span></span>



| <span data-ttu-id="00ea8-114">值</span><span class="sxs-lookup"><span data-stu-id="00ea8-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="00ea8-115">意義</span><span class="sxs-lookup"><span data-stu-id="00ea8-115">Meaning</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <span data-ttu-id="00ea8-116"><dt>**GL \_ 編譯**</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-116"><dt>**GL\_COMPILE**</dt></span></span> </dl>                                       | <span data-ttu-id="00ea8-117">命令只會進行編譯。</span><span class="sxs-lookup"><span data-stu-id="00ea8-117">Commands are merely compiled.</span></span><br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <span data-ttu-id="00ea8-118"><dt>**GL \_ 編譯 \_ 和 \_ 執行**</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-118"><dt>**GL\_COMPILE\_AND\_EXECUTE**</dt></span></span> </dl> | <span data-ttu-id="00ea8-119">命令會在編譯到顯示清單中時執行。</span><span class="sxs-lookup"><span data-stu-id="00ea8-119">Commands are executed as they are compiled into the display list.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00ea8-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="00ea8-120">Return value</span></span>

<span data-ttu-id="00ea8-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="00ea8-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="00ea8-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="00ea8-122">Error codes</span></span>

<span data-ttu-id="00ea8-123">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="00ea8-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="00ea8-124">Name</span><span class="sxs-lookup"><span data-stu-id="00ea8-124">Name</span></span>                                                                                                  | <span data-ttu-id="00ea8-125">意義</span><span class="sxs-lookup"><span data-stu-id="00ea8-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00ea8-126"><dt>**GL \_ 無效 \_ 值**</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="00ea8-127">*清單* 為零。</span><span class="sxs-lookup"><span data-stu-id="00ea8-127">*list* was zero.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="00ea8-128"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="00ea8-129">*模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="00ea8-129">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="00ea8-130"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="00ea8-131">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="00ea8-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="00ea8-132">備註</span><span class="sxs-lookup"><span data-stu-id="00ea8-132">Remarks</span></span>

<span data-ttu-id="00ea8-133">顯示清單是已儲存以供後續執行的 OpenGL 命令群組。</span><span class="sxs-lookup"><span data-stu-id="00ea8-133">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="00ea8-134">顯示清單會以 **glNewList** 來建立。</span><span class="sxs-lookup"><span data-stu-id="00ea8-134">The display lists are created with **glNewList**.</span></span> <span data-ttu-id="00ea8-135">所有後續的命令都會依發出的順序，放在顯示清單中，直到呼叫 **glEndList** 為止。</span><span class="sxs-lookup"><span data-stu-id="00ea8-135">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="00ea8-136">**GlNewList** 函式有兩個參數。</span><span class="sxs-lookup"><span data-stu-id="00ea8-136">The **glNewList** function has two parameters.</span></span> <span data-ttu-id="00ea8-137">第一個參數 *list* 是一個正整數，會成為顯示清單的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="00ea8-137">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="00ea8-138">您可以使用 [**glGenLists**](glgenlists.md) 來建立和保留名稱，並測試 [**glIsList**](glislist.md)的唯一性。</span><span class="sxs-lookup"><span data-stu-id="00ea8-138">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="00ea8-139">第二個參數（ *模式*）是可採用上述兩個值之一的符號常數。</span><span class="sxs-lookup"><span data-stu-id="00ea8-139">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="00ea8-140">某些命令不會編譯到顯示清單中，但是會立即執行，而不論顯示清單模式為何。</span><span class="sxs-lookup"><span data-stu-id="00ea8-140">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="00ea8-141">這些命令有 [**glColorPointer**](glcolorpointer.md)、 [**glDeleteLists**](gldeletelists.md)、 [**glDisableClientState**](gldisableclientstate.md)、 [**glEdgeFlagPointer**](gledgeflagpointer.md)、 [**glEnableClientState**](glenableclientstate.md)、 [**glFeedbackBuffer**](glfeedbackbuffer.md)、 [**glFinish**](glfinish.md)、 [**glFlush**](glflush.md)、 [**glGenLists**](glgenlists.md)、 [**glIndexPointer**](glindexpointer.md)、 [**glInterleavedArrays**](glinterleavedarrays.md)、 [**glIsEnabled、glIsList**](glisenabled.md) [**、glNormalPointer**](glislist.md) [**、glPopClientAttrib**](glnormalpointer.md) [**、glPixelStore**](glpopclientattrib.md) [**、glPushClientAttrib**](glpixelstore-functions.md) [**、glReadPixels**](glpushclientattrib.md) [**、glRenderMode**](glreadpixels.md)、 [**glSelectBuffer、**](glselectbuffer.md)glTexCoordPointer、glVertexPointer [**、glGet、**](glrendermode.md) [**、、**](gltexcoordpointer.md) [**，以及**](glvertexpointer.md)所有 [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)常式。</span><span class="sxs-lookup"><span data-stu-id="00ea8-141">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="00ea8-142">同樣地，當[](glteximage1d.md)第一個引數是 GL [](glteximage2d.md) \_ proxy \_ 材質 \_ 2d 或 gl \_ proxy \_ 材質 \_ 1d 時，glTexImage2D 和 glTexImage1D 會立即執行，而不會編譯成顯示清單。</span><span class="sxs-lookup"><span data-stu-id="00ea8-142">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="00ea8-143">當遇到 **glEndList** 函式時，會藉由將清單與 [ **glNewList** ] 命令) 中指定的 [唯一名稱] (*清單* 產生關聯，來完成顯示清單定義。</span><span class="sxs-lookup"><span data-stu-id="00ea8-143">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the **glNewList** command).</span></span> <span data-ttu-id="00ea8-144">如果已有名稱 *清單* 的顯示清單，則只會在呼叫 **glEndList** 時加以取代。</span><span class="sxs-lookup"><span data-stu-id="00ea8-144">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="00ea8-145">[**GlCallList**](glcalllist.md)和 [**glCallLists**](glcalllists.md)函數可以輸入到顯示清單中。</span><span class="sxs-lookup"><span data-stu-id="00ea8-145">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="00ea8-146">**GlCallList** 或 **glCallLists** 所執行的顯示清單或清單中的命令不會包含在所建立的顯示清單中，即使清單建立模式是 GL \_ 編譯 \_ 和執行 \_ 也一樣。</span><span class="sxs-lookup"><span data-stu-id="00ea8-146">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="00ea8-147">下列函式會抓取 **glNewList** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="00ea8-147">The following function retrieves information related to **glNewList**:</span></span>

<span data-ttu-id="00ea8-148">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="00ea8-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="00ea8-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="00ea8-149">Requirements</span></span>



| <span data-ttu-id="00ea8-150">需求</span><span class="sxs-lookup"><span data-stu-id="00ea8-150">Requirement</span></span> | <span data-ttu-id="00ea8-151">值</span><span class="sxs-lookup"><span data-stu-id="00ea8-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00ea8-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00ea8-152">Minimum supported client</span></span><br/> | <span data-ttu-id="00ea8-153">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00ea8-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="00ea8-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00ea8-154">Minimum supported server</span></span><br/> | <span data-ttu-id="00ea8-155">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00ea8-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="00ea8-156">標頭</span><span class="sxs-lookup"><span data-stu-id="00ea8-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="00ea8-157"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="00ea8-158">程式庫</span><span class="sxs-lookup"><span data-stu-id="00ea8-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="00ea8-159"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="00ea8-160">DLL</span><span class="sxs-lookup"><span data-stu-id="00ea8-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00ea8-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00ea8-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00ea8-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00ea8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ea8-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="00ea8-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="00ea8-164">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="00ea8-164">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="00ea8-165">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="00ea8-165">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="00ea8-166">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="00ea8-166">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="00ea8-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="00ea8-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="00ea8-168">**glEndList**</span><span class="sxs-lookup"><span data-stu-id="00ea8-168">**glEndList**</span></span>](glendlist.md)
</dt> <dt>

[<span data-ttu-id="00ea8-169">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="00ea8-169">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="00ea8-170">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="00ea8-170">**glIsList**</span></span>](glislist.md)
</dt> </dl>

 

 





