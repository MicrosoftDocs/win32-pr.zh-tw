---
title: 'glPushClientAttrib 函式 (Gl) '
description: 'GlPushClientAttrib 和 glPopClientAttrib 函式會在用戶端屬性堆疊上儲存和還原用戶端狀態變數的群組。 |glPushClientAttrib 函式 (Gl) '
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- glPushClientAttrib 函式 OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944e2e4229f0d36f0009ce337fd3806020322dbf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322488"
---
# <a name="glpushclientattrib-function"></a><span data-ttu-id="aabc3-105">glPushClientAttrib 函式</span><span class="sxs-lookup"><span data-stu-id="aabc3-105">glPushClientAttrib function</span></span>

<span data-ttu-id="aabc3-106">**GlPushClientAttrib** 和 [**glPopClientAttrib**](glpopclientattrib.md)函式會在用戶端屬性堆疊上儲存和還原用戶端狀態變數的群組。</span><span class="sxs-lookup"><span data-stu-id="aabc3-106">The **glPushClientAttrib** and [**glPopClientAttrib**](glpopclientattrib.md) functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="aabc3-107">語法</span><span class="sxs-lookup"><span data-stu-id="aabc3-107">Syntax</span></span>


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="aabc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="aabc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aabc3-109">*面具*</span><span class="sxs-lookup"><span data-stu-id="aabc3-109">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="aabc3-110">表示要儲存哪些屬性的遮罩。</span><span class="sxs-lookup"><span data-stu-id="aabc3-110">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="aabc3-111">以下是符號遮罩常數及其相關聯的 OpenGL 用戶端狀態。</span><span class="sxs-lookup"><span data-stu-id="aabc3-111">The following are the symbolic mask constants and their associated OpenGL client states.</span></span>



| <span data-ttu-id="aabc3-112">值</span><span class="sxs-lookup"><span data-stu-id="aabc3-112">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="aabc3-113">意義</span><span class="sxs-lookup"><span data-stu-id="aabc3-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <span data-ttu-id="aabc3-114"><dt>**GL \_ 用戶端 \_ 圖元 \_ 存放區 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="aabc3-114"><dt>**GL\_CLIENT\_PIXEL\_STORE\_BIT**</dt></span></span> </dl>                                             | <span data-ttu-id="aabc3-115">圖元儲存模式屬性。</span><span class="sxs-lookup"><span data-stu-id="aabc3-115">Pixel storage mode attributes.</span></span><br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <span data-ttu-id="aabc3-116"><dt>**GL \_ 用戶端 \_ 頂點 \_ 陣列 \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="aabc3-116"><dt>**GL\_CLIENT\_VERTEX\_ARRAY\_BIT**</dt></span></span> </dl>                                          | <span data-ttu-id="aabc3-117">頂點陣列屬性。</span><span class="sxs-lookup"><span data-stu-id="aabc3-117">Vertex array attributes.</span></span><br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <span data-ttu-id="aabc3-118"><dt>**GL \_ 用戶端 \_ 所有的 \_ ATTRIB \_ 位**</dt></span><span class="sxs-lookup"><span data-stu-id="aabc3-118"><dt>**GL\_CLIENT\_ALL\_ATTRIB\_BITs**</dt></span></span> </dl> | <span data-ttu-id="aabc3-119">所有堆疊的用戶端狀態屬性。</span><span class="sxs-lookup"><span data-stu-id="aabc3-119">all stackable client-state attributes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aabc3-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="aabc3-120">Return value</span></span>

<span data-ttu-id="aabc3-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="aabc3-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aabc3-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="aabc3-122">Error codes</span></span>

<span data-ttu-id="aabc3-123">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aabc3-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="aabc3-124">Name</span><span class="sxs-lookup"><span data-stu-id="aabc3-124">Name</span></span>                                                                                               | <span data-ttu-id="aabc3-125">意義</span><span class="sxs-lookup"><span data-stu-id="aabc3-125">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aabc3-126"><dt>**GL \_ 堆疊 \_ 溢位**</dt></span><span class="sxs-lookup"><span data-stu-id="aabc3-126"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="aabc3-127">當用戶端屬性堆疊已滿時，就會呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="aabc3-127">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="aabc3-128">備註</span><span class="sxs-lookup"><span data-stu-id="aabc3-128">Remarks</span></span>

<span data-ttu-id="aabc3-129">**GlPushClientAttrib** 函式會使用其 mask 參數，來判斷要將哪些用戶端狀態變數群組儲存在用戶端屬性堆疊上。</span><span class="sxs-lookup"><span data-stu-id="aabc3-129">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="aabc3-130">您可以使用位 OR 運算子將已接受的符號常數聯結在一起，以設定位並建立遮罩。</span><span class="sxs-lookup"><span data-stu-id="aabc3-130">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="aabc3-131">[**GlPopClientAttrib**](glpopclientattrib.md)函式會還原上次與 **glPushclientAttrib** 儲存之用戶端狀態變數的值。</span><span class="sxs-lookup"><span data-stu-id="aabc3-131">The [**glPopClientAttrib**](glpopclientattrib.md) function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="aabc3-132">先前未儲存的用戶端狀態變數會保持不變。</span><span class="sxs-lookup"><span data-stu-id="aabc3-132">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="aabc3-133">將屬性推送至完整的用戶端屬性堆疊，或將屬性從空的堆疊中取出，會設定錯誤旗標，且不會對 OpenGL 狀態進行其他變更。</span><span class="sxs-lookup"><span data-stu-id="aabc3-133">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="aabc3-134">用戶端屬性堆疊預設為空白。</span><span class="sxs-lookup"><span data-stu-id="aabc3-134">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="aabc3-135">某些 OpenGL 用戶端狀態值無法儲存在用戶端屬性堆疊上。</span><span class="sxs-lookup"><span data-stu-id="aabc3-135">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="aabc3-136">例如，您無法在用戶端屬性堆疊上儲存選取或意見反應狀態。</span><span class="sxs-lookup"><span data-stu-id="aabc3-136">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="aabc3-137">用戶端屬性堆疊的深度至少為16。</span><span class="sxs-lookup"><span data-stu-id="aabc3-137">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="aabc3-138">**GlPushclientAttrib** 和 **glPopClientAttrib** 函式不會編譯成顯示清單，但是會立即執行。</span><span class="sxs-lookup"><span data-stu-id="aabc3-138">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="aabc3-139">**GlPushClientAttrib** 和 **glPopClientAttrib** 函式只能推送和 pop 圖元儲存模式，以及頂點陣列用戶端狀態。</span><span class="sxs-lookup"><span data-stu-id="aabc3-139">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="aabc3-140">您必須使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 來推送和保留在伺服器上的 pop 狀態。</span><span class="sxs-lookup"><span data-stu-id="aabc3-140">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="aabc3-141">**GlPushClientAttrib** 和 **glPopClientAttrib** 函式僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="aabc3-141">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="aabc3-142">下列函式會取出 **glPushClientAttrib** 和 **glPopClientAttrib** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="aabc3-142">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="aabc3-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 用戶端 ATTRIB 用戶端 \_ ATTRIB \_ 堆疊 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="aabc3-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="aabc3-144">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ 用戶端 \_ ATTRIB \_ 堆疊 \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="aabc3-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="aabc3-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="aabc3-145">Requirements</span></span>



| <span data-ttu-id="aabc3-146">需求</span><span class="sxs-lookup"><span data-stu-id="aabc3-146">Requirement</span></span> | <span data-ttu-id="aabc3-147">值</span><span class="sxs-lookup"><span data-stu-id="aabc3-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aabc3-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aabc3-148">Minimum supported client</span></span><br/> | <span data-ttu-id="aabc3-149">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aabc3-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aabc3-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aabc3-150">Minimum supported server</span></span><br/> | <span data-ttu-id="aabc3-151">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aabc3-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aabc3-152">標頭</span><span class="sxs-lookup"><span data-stu-id="aabc3-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="aabc3-153"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="aabc3-153"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="aabc3-154">程式庫</span><span class="sxs-lookup"><span data-stu-id="aabc3-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="aabc3-155"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="aabc3-155"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aabc3-156">DLL</span><span class="sxs-lookup"><span data-stu-id="aabc3-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aabc3-157"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aabc3-157"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aabc3-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aabc3-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aabc3-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="aabc3-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="aabc3-160">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="aabc3-160">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="aabc3-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="aabc3-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="aabc3-162">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="aabc3-162">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="aabc3-163">**glGet**</span><span class="sxs-lookup"><span data-stu-id="aabc3-163">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="aabc3-164">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="aabc3-164">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="aabc3-165">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="aabc3-165">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="aabc3-166">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="aabc3-166">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="aabc3-167">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="aabc3-167">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="aabc3-168">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="aabc3-168">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="aabc3-169">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="aabc3-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="aabc3-170">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="aabc3-170">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="aabc3-171">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="aabc3-171">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





