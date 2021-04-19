---
title: 'glPopName 函式 (Gl) '
description: 'GlPushName 和 glPopName 函式會推送並彈出名稱堆疊。 |glPopName 函式 (Gl) '
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- glPopName 函式 OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 830c4937b30cca64de3063b42ad16dd3adc87c89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106982845"
---
# <a name="glpopname-function"></a><span data-ttu-id="6b6f4-105">glPopName 函式</span><span class="sxs-lookup"><span data-stu-id="6b6f4-105">glPopName function</span></span>

<span data-ttu-id="6b6f4-106">[**GlPushName**](glpushname.md)和 **glPopName** 函式會推送並彈出名稱堆疊。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-106">The [**glPushName**](glpushname.md) and **glPopName** functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b6f4-107">語法</span><span class="sxs-lookup"><span data-stu-id="6b6f4-107">Syntax</span></span>


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a><span data-ttu-id="6b6f4-108">參數</span><span class="sxs-lookup"><span data-stu-id="6b6f4-108">Parameters</span></span>

<span data-ttu-id="6b6f4-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b6f4-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b6f4-110">Return value</span></span>

<span data-ttu-id="6b6f4-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b6f4-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="6b6f4-112">Error codes</span></span>

<span data-ttu-id="6b6f4-113">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6b6f4-114">Name</span><span class="sxs-lookup"><span data-stu-id="6b6f4-114">Name</span></span>                                                                                                  | <span data-ttu-id="6b6f4-115">意義</span><span class="sxs-lookup"><span data-stu-id="6b6f4-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b6f4-116"><dt>**GL \_ 堆疊 \_ 下溢**</dt></span><span class="sxs-lookup"><span data-stu-id="6b6f4-116"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="6b6f4-117">當目前的矩陣堆疊只包含單一矩陣時，會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-117">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="6b6f4-118"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="6b6f4-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6b6f4-119">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6b6f4-120">備註</span><span class="sxs-lookup"><span data-stu-id="6b6f4-120">Remarks</span></span>

<span data-ttu-id="6b6f4-121">[**GlPushName**](glpushname.md)函式會將名稱推送至名稱堆疊，這一開始是空的。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-121">The [**glPushName**](glpushname.md) function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="6b6f4-122">**GlPopName** 函式會將一個名稱從堆疊的最上方彈出。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-122">The **glPopName** function pops one name off the top of the stack.</span></span> <span data-ttu-id="6b6f4-123">在選取模式期間，會使用名稱堆疊來允許唯一識別的轉譯命令集。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-123">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="6b6f4-124">它包含一組排序的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-124">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="6b6f4-125">當轉譯模式並非 GL 選取時，名稱堆疊一律是空的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-125">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="6b6f4-126">當轉譯模式不是 GL 時，會忽略 [**glPushName**](glpushname.md) 或 **glPopName** 的呼叫 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6b6f4-126">Calls to [**glPushName**](glpushname.md) or **glPopName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="6b6f4-127">下列函式會取出 [**glPushName**](glpushname.md) 和 **glPopName** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="6b6f4-127">The following functions retrieve information related to [**glPushName**](glpushname.md) and **glPopName**:</span></span>

<span data-ttu-id="6b6f4-128">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 名稱 \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="6b6f4-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="6b6f4-129">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ 名稱 \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="6b6f4-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="6b6f4-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b6f4-130">Requirements</span></span>



| <span data-ttu-id="6b6f4-131">需求</span><span class="sxs-lookup"><span data-stu-id="6b6f4-131">Requirement</span></span> | <span data-ttu-id="6b6f4-132">值</span><span class="sxs-lookup"><span data-stu-id="6b6f4-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b6f4-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b6f4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6b6f4-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b6f4-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6b6f4-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b6f4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6b6f4-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b6f4-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b6f4-137">標頭</span><span class="sxs-lookup"><span data-stu-id="6b6f4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b6f4-138"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="6b6f4-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6b6f4-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="6b6f4-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b6f4-140"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b6f4-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b6f4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6b6f4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b6f4-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b6f4-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b6f4-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b6f4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b6f4-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6b6f4-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6b6f4-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6b6f4-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6b6f4-146">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="6b6f4-146">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="6b6f4-147">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="6b6f4-147">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="6b6f4-148">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="6b6f4-148">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="6b6f4-149">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="6b6f4-149">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





