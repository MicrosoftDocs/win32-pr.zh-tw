---
title: 'glPopClientAttrib 函式 (Gl) '
description: 'GlPushClientAttrib 和 glPopClientAttrib 函式會在用戶端屬性堆疊上儲存和還原用戶端狀態變數的群組。 |glPopClientAttrib 函式 (Gl) '
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- glPopClientAttrib 函式 OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322316"
---
# <a name="glpopclientattrib-function"></a><span data-ttu-id="35c0e-105">glPopClientAttrib 函式</span><span class="sxs-lookup"><span data-stu-id="35c0e-105">glPopClientAttrib function</span></span>

<span data-ttu-id="35c0e-106">[**GlPushClientAttrib**](glpushclientattrib.md)和 **glPopClientAttrib** 函式會在用戶端屬性堆疊上儲存和還原用戶端狀態變數的群組。</span><span class="sxs-lookup"><span data-stu-id="35c0e-106">The [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c0e-107">語法</span><span class="sxs-lookup"><span data-stu-id="35c0e-107">Syntax</span></span>


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="35c0e-108">參數</span><span class="sxs-lookup"><span data-stu-id="35c0e-108">Parameters</span></span>

<span data-ttu-id="35c0e-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="35c0e-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35c0e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="35c0e-110">Return value</span></span>

<span data-ttu-id="35c0e-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="35c0e-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="35c0e-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="35c0e-112">Error codes</span></span>

<span data-ttu-id="35c0e-113">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="35c0e-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="35c0e-114">Name</span><span class="sxs-lookup"><span data-stu-id="35c0e-114">Name</span></span>                                                                                               | <span data-ttu-id="35c0e-115">意義</span><span class="sxs-lookup"><span data-stu-id="35c0e-115">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35c0e-116"><dt>**GL \_ 堆疊 \_ 溢位**</dt></span><span class="sxs-lookup"><span data-stu-id="35c0e-116"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="35c0e-117">當用戶端屬性堆疊已滿時，就會呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="35c0e-117">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="35c0e-118">備註</span><span class="sxs-lookup"><span data-stu-id="35c0e-118">Remarks</span></span>

<span data-ttu-id="35c0e-119">**GlPushClientAttrib** 函式會使用其 mask 參數，來判斷要將哪些用戶端狀態變數群組儲存在用戶端屬性堆疊上。</span><span class="sxs-lookup"><span data-stu-id="35c0e-119">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="35c0e-120">您可以使用位 OR 運算子將已接受的符號常數聯結在一起，以設定位並建立遮罩。</span><span class="sxs-lookup"><span data-stu-id="35c0e-120">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="35c0e-121">**GlPopClientAttrib** 函式會還原上次與 **glPushclientAttrib** 儲存之用戶端狀態變數的值。</span><span class="sxs-lookup"><span data-stu-id="35c0e-121">The **glPopClientAttrib** function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="35c0e-122">先前未儲存的用戶端狀態變數會保持不變。</span><span class="sxs-lookup"><span data-stu-id="35c0e-122">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="35c0e-123">將屬性推送至完整的用戶端屬性堆疊，或將屬性從空的堆疊中取出，會設定錯誤旗標，且不會對 OpenGL 狀態進行其他變更。</span><span class="sxs-lookup"><span data-stu-id="35c0e-123">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="35c0e-124">用戶端屬性堆疊預設為空白。</span><span class="sxs-lookup"><span data-stu-id="35c0e-124">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="35c0e-125">某些 OpenGL 用戶端狀態值無法儲存在用戶端屬性堆疊上。</span><span class="sxs-lookup"><span data-stu-id="35c0e-125">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="35c0e-126">例如，您無法在用戶端屬性堆疊上儲存選取或意見反應狀態。</span><span class="sxs-lookup"><span data-stu-id="35c0e-126">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="35c0e-127">用戶端屬性堆疊的深度至少為16。</span><span class="sxs-lookup"><span data-stu-id="35c0e-127">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="35c0e-128">**GlPushclientAttrib** 和 **glPopClientAttrib** 函式不會編譯成顯示清單，但是會立即執行。</span><span class="sxs-lookup"><span data-stu-id="35c0e-128">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="35c0e-129">**GlPushClientAttrib** 和 **glPopClientAttrib** 函式只能推送和 pop 圖元儲存模式，以及頂點陣列用戶端狀態。</span><span class="sxs-lookup"><span data-stu-id="35c0e-129">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="35c0e-130">您必須使用 [**glPushAttrib**](glpushattrib.md) 和 [**glPopAttrib**](glpopattrib.md) 來推送和保留在伺服器上的 pop 狀態。</span><span class="sxs-lookup"><span data-stu-id="35c0e-130">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="35c0e-131">**GlPushClientAttrib** 和 **glPopClientAttrib** 函式僅適用于 OpenGL 1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="35c0e-131">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="35c0e-132">下列函式會取出 **glPushClientAttrib** 和 **glPopClientAttrib** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="35c0e-132">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="35c0e-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 用戶端 ATTRIB 用戶端 \_ ATTRIB \_ 堆疊 \_ 深度</span><span class="sxs-lookup"><span data-stu-id="35c0e-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="35c0e-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ 用戶端 \_ ATTRIB \_ 堆疊 \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="35c0e-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="35c0e-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="35c0e-135">Requirements</span></span>



| <span data-ttu-id="35c0e-136">需求</span><span class="sxs-lookup"><span data-stu-id="35c0e-136">Requirement</span></span> | <span data-ttu-id="35c0e-137">值</span><span class="sxs-lookup"><span data-stu-id="35c0e-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35c0e-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35c0e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="35c0e-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35c0e-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="35c0e-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35c0e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="35c0e-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35c0e-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35c0e-142">標頭</span><span class="sxs-lookup"><span data-stu-id="35c0e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="35c0e-143"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="35c0e-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="35c0e-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="35c0e-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="35c0e-145"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="35c0e-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="35c0e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="35c0e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35c0e-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35c0e-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35c0e-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35c0e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c0e-149">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="35c0e-149">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="35c0e-150">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="35c0e-150">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="35c0e-151">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="35c0e-151">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="35c0e-152">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="35c0e-152">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="35c0e-153">**glGet**</span><span class="sxs-lookup"><span data-stu-id="35c0e-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="35c0e-154">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="35c0e-154">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="35c0e-155">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="35c0e-155">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="35c0e-156">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="35c0e-156">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="35c0e-157">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="35c0e-157">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="35c0e-158">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="35c0e-158">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="35c0e-159">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="35c0e-159">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="35c0e-160">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="35c0e-160">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="35c0e-161">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="35c0e-161">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





