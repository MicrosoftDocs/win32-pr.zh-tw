---
title: 'glEndList 函式 (Gl) '
description: 'GlNewList 和 glEndList 函數會建立或取代顯示清單。 |glEndList 函式 (Gl) '
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- glEndList 函式 OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f8db8c2abea44d678268f804159b60fe695f96
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106998987"
---
# <a name="glendlist-function"></a><span data-ttu-id="4825f-105">glEndList 函式</span><span class="sxs-lookup"><span data-stu-id="4825f-105">glEndList function</span></span>

<span data-ttu-id="4825f-106">[**GlNewList**](glnewlist.md)和 **glEndList** 函數會建立或取代顯示清單。</span><span class="sxs-lookup"><span data-stu-id="4825f-106">The [**glNewList**](glnewlist.md) and **glEndList** functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4825f-107">語法</span><span class="sxs-lookup"><span data-stu-id="4825f-107">Syntax</span></span>


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a><span data-ttu-id="4825f-108">參數</span><span class="sxs-lookup"><span data-stu-id="4825f-108">Parameters</span></span>

<span data-ttu-id="4825f-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="4825f-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4825f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4825f-110">Return value</span></span>

<span data-ttu-id="4825f-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4825f-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4825f-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4825f-112">Error codes</span></span>

<span data-ttu-id="4825f-113">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4825f-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4825f-114">Name</span><span class="sxs-lookup"><span data-stu-id="4825f-114">Name</span></span>                                                                                                  | <span data-ttu-id="4825f-115">意義</span><span class="sxs-lookup"><span data-stu-id="4825f-115">Meaning</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4825f-116"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="4825f-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4825f-117">呼叫 **glEndList** 時沒有先前的 **glNewList**，或在定義顯示清單時呼叫 **glNewList** 。</span><span class="sxs-lookup"><span data-stu-id="4825f-117">**glEndList** was called without a preceding **glNewList**, or if **glnewlist** was called while a display list was being defined.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4825f-118">備註</span><span class="sxs-lookup"><span data-stu-id="4825f-118">Remarks</span></span>

<span data-ttu-id="4825f-119">顯示清單是已儲存以供後續執行的 OpenGL 命令群組。</span><span class="sxs-lookup"><span data-stu-id="4825f-119">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="4825f-120">顯示清單會以 [**glNewList**](glnewlist.md)來建立。</span><span class="sxs-lookup"><span data-stu-id="4825f-120">The display lists are created with [**glNewList**](glnewlist.md).</span></span> <span data-ttu-id="4825f-121">所有後續的命令都會依發出的順序，放在顯示清單中，直到呼叫 **glEndList** 為止。</span><span class="sxs-lookup"><span data-stu-id="4825f-121">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="4825f-122">[**GlNewList**](glnewlist.md)函式有兩個參數。</span><span class="sxs-lookup"><span data-stu-id="4825f-122">The [**glNewList**](glnewlist.md) function has two parameters.</span></span> <span data-ttu-id="4825f-123">第一個參數 *list* 是一個正整數，會成為顯示清單的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="4825f-123">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="4825f-124">您可以使用 [**glGenLists**](glgenlists.md) 來建立和保留名稱，並測試 [**glIsList**](glislist.md)的唯一性。</span><span class="sxs-lookup"><span data-stu-id="4825f-124">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="4825f-125">第二個參數（ *模式*）是可採用上述兩個值之一的符號常數。</span><span class="sxs-lookup"><span data-stu-id="4825f-125">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="4825f-126">某些命令不會編譯到顯示清單中，但是會立即執行，而不論顯示清單模式為何。</span><span class="sxs-lookup"><span data-stu-id="4825f-126">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="4825f-127">這些命令有 [**glColorPointer**](glcolorpointer.md)、 [**glDeleteLists**](gldeletelists.md)、 [**glDisableClientState**](gldisableclientstate.md)、 [**glEdgeFlagPointer**](gledgeflagpointer.md)、 [**glEnableClientState**](glenableclientstate.md)、 [**glFeedbackBuffer**](glfeedbackbuffer.md)、 [**glFinish**](glfinish.md)、 [**glFlush**](glflush.md)、 [**glGenLists**](glgenlists.md)、 [**glIndexPointer**](glindexpointer.md)、 [**glInterleavedArrays**](glinterleavedarrays.md)、 [**glIsEnabled、glIsList**](glisenabled.md) [**、glNormalPointer**](glislist.md) [**、glPopClientAttrib**](glnormalpointer.md) [**、glPixelStore**](glpopclientattrib.md) [**、glPushClientAttrib**](glpixelstore-functions.md) [**、glReadPixels**](glpushclientattrib.md) [**、glRenderMode**](glreadpixels.md)、 [**glSelectBuffer、**](glselectbuffer.md)glTexCoordPointer、glVertexPointer [**、glGet、**](glrendermode.md) [**、、**](gltexcoordpointer.md) [**，以及**](glvertexpointer.md)所有 [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)常式。</span><span class="sxs-lookup"><span data-stu-id="4825f-127">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="4825f-128">同樣地，當[](glteximage1d.md)第一個引數是 GL [](glteximage2d.md) \_ proxy \_ 材質 \_ 2d 或 gl \_ proxy \_ 材質 \_ 1d 時，glTexImage2D 和 glTexImage1D 會立即執行，而不會編譯成顯示清單。</span><span class="sxs-lookup"><span data-stu-id="4825f-128">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="4825f-129">當遇到 **glEndList** 函式時，會藉由將清單與 [ [**glNewList**](glnewlist.md) ] 命令) 中指定的 [唯一名稱] (*清單* 產生關聯，來完成顯示清單定義。</span><span class="sxs-lookup"><span data-stu-id="4825f-129">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the [**glNewList**](glnewlist.md) command).</span></span> <span data-ttu-id="4825f-130">如果已有名稱 *清單* 的顯示清單，則只會在呼叫 **glEndList** 時加以取代。</span><span class="sxs-lookup"><span data-stu-id="4825f-130">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="4825f-131">[**GlCallList**](glcalllist.md)和 [**glCallLists**](glcalllists.md)函數可以輸入到顯示清單中。</span><span class="sxs-lookup"><span data-stu-id="4825f-131">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="4825f-132">**GlCallList** 或 **glCallLists** 所執行的顯示清單或清單中的命令不會包含在所建立的顯示清單中，即使清單建立模式是 GL \_ 編譯 \_ 和執行 \_ 也一樣。</span><span class="sxs-lookup"><span data-stu-id="4825f-132">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="4825f-133">下列函式會抓取 [**glNewList**](glnewlist.md)的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="4825f-133">The following function retrieves information related to [**glNewList**](glnewlist.md):</span></span>

<span data-ttu-id="4825f-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="4825f-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="4825f-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="4825f-135">Requirements</span></span>



| <span data-ttu-id="4825f-136">需求</span><span class="sxs-lookup"><span data-stu-id="4825f-136">Requirement</span></span> | <span data-ttu-id="4825f-137">值</span><span class="sxs-lookup"><span data-stu-id="4825f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4825f-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4825f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4825f-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4825f-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4825f-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4825f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4825f-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4825f-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4825f-142">標頭</span><span class="sxs-lookup"><span data-stu-id="4825f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4825f-143"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="4825f-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4825f-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="4825f-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="4825f-145"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4825f-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4825f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4825f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4825f-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4825f-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4825f-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4825f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4825f-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4825f-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4825f-150">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="4825f-150">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="4825f-151">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="4825f-151">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="4825f-152">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="4825f-152">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="4825f-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4825f-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4825f-154">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="4825f-154">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="4825f-155">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="4825f-155">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="4825f-156">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="4825f-156">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





