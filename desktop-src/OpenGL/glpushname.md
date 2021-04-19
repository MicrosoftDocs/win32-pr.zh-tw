---
title: 'glPushName 函式 (Gl) '
description: 'GlPushName 和 glPopName 函式會推送並彈出名稱堆疊。 |glPushName 函式 (Gl) '
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- glPushName 函式 OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988554"
---
# <a name="glpushname-function"></a><span data-ttu-id="bc312-105">glPushName 函式</span><span class="sxs-lookup"><span data-stu-id="bc312-105">glPushName function</span></span>

<span data-ttu-id="bc312-106">**GlPushName** 和 [**glPopName**](glpopname.md)函式會推送並彈出名稱堆疊。</span><span class="sxs-lookup"><span data-stu-id="bc312-106">The **glPushName** and [**glPopName**](glpopname.md) functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc312-107">語法</span><span class="sxs-lookup"><span data-stu-id="bc312-107">Syntax</span></span>


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="bc312-108">參數</span><span class="sxs-lookup"><span data-stu-id="bc312-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc312-109">*name*</span><span class="sxs-lookup"><span data-stu-id="bc312-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="bc312-110">將推送至名稱堆疊的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc312-110">A name that will be pushed onto the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc312-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc312-111">Return value</span></span>

<span data-ttu-id="bc312-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bc312-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bc312-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bc312-113">Error codes</span></span>

<span data-ttu-id="bc312-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bc312-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bc312-115">Name</span><span class="sxs-lookup"><span data-stu-id="bc312-115">Name</span></span>                                                                                                  | <span data-ttu-id="bc312-116">意義</span><span class="sxs-lookup"><span data-stu-id="bc312-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc312-117"><dt>**GL \_ 堆疊 \_ 溢位**</dt></span><span class="sxs-lookup"><span data-stu-id="bc312-117"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="bc312-118">當目前的矩陣堆疊已滿時，就會呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="bc312-118">The function was called while the current matrix stack was full.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="bc312-119"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="bc312-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bc312-120">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="bc312-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bc312-121">備註</span><span class="sxs-lookup"><span data-stu-id="bc312-121">Remarks</span></span>

<span data-ttu-id="bc312-122">**GlPushName** 函式會將名稱推送至名稱堆疊，這一開始是空的。</span><span class="sxs-lookup"><span data-stu-id="bc312-122">The **glPushName** function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="bc312-123">[**GlPopName**](glpopname.md)函式會將一個名稱從堆疊的最上方彈出。</span><span class="sxs-lookup"><span data-stu-id="bc312-123">The [**glPopName**](glpopname.md) function pops one name off the top of the stack.</span></span> <span data-ttu-id="bc312-124">在選取模式期間，會使用名稱堆疊來允許唯一識別的轉譯命令集。</span><span class="sxs-lookup"><span data-stu-id="bc312-124">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="bc312-125">它包含一組排序的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="bc312-125">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="bc312-126">當轉譯模式並非 GL 選取時，名稱堆疊一律是空的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc312-126">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="bc312-127">當轉譯模式不是 GL 時，會忽略 **glPushName** 或 [**glPopName**](glpopname.md) 的呼叫 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc312-127">Calls to **glPushName** or [**glPopName**](glpopname.md) while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="bc312-128">下列函式會取出 **glPushName** 和 [**glPopName**](glpopname.md)的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="bc312-128">The following functions retrieve information related to **glPushName** and [**glPopName**](glpopname.md):</span></span>

<span data-ttu-id="bc312-129">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 名稱 \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="bc312-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="bc312-130">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ 名稱 \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="bc312-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="bc312-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc312-131">Requirements</span></span>



| <span data-ttu-id="bc312-132">需求</span><span class="sxs-lookup"><span data-stu-id="bc312-132">Requirement</span></span> | <span data-ttu-id="bc312-133">值</span><span class="sxs-lookup"><span data-stu-id="bc312-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc312-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc312-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bc312-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc312-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bc312-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc312-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bc312-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc312-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc312-138">標頭</span><span class="sxs-lookup"><span data-stu-id="bc312-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc312-139"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="bc312-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bc312-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="bc312-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc312-141"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc312-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bc312-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bc312-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc312-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc312-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc312-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc312-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc312-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bc312-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bc312-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bc312-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bc312-147">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="bc312-147">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="bc312-148">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="bc312-148">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="bc312-149">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="bc312-149">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="bc312-150">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="bc312-150">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





