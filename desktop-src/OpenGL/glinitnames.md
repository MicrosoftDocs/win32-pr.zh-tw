---
title: 'glInitNames 函式 (Gl) '
description: GlInitNames 函式會初始化名稱堆疊。
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- glInitNames 函式 OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ebdb9d19f6c88340fd53162febe694e3566408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093892"
---
# <a name="glinitnames-function"></a><span data-ttu-id="b9b3e-104">glInitNames 函式</span><span class="sxs-lookup"><span data-stu-id="b9b3e-104">glInitNames function</span></span>

<span data-ttu-id="b9b3e-105">**GlInitNames** 函式會初始化名稱堆疊。</span><span class="sxs-lookup"><span data-stu-id="b9b3e-105">The **glInitNames** function initializes the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9b3e-106">語法</span><span class="sxs-lookup"><span data-stu-id="b9b3e-106">Syntax</span></span>


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a><span data-ttu-id="b9b3e-107">參數</span><span class="sxs-lookup"><span data-stu-id="b9b3e-107">Parameters</span></span>

<span data-ttu-id="b9b3e-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="b9b3e-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9b3e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9b3e-109">Return value</span></span>

<span data-ttu-id="b9b3e-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b9b3e-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b9b3e-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b9b3e-111">Error codes</span></span>

<span data-ttu-id="b9b3e-112">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b9b3e-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b9b3e-113">Name</span><span class="sxs-lookup"><span data-stu-id="b9b3e-113">Name</span></span>                                                                                                  | <span data-ttu-id="b9b3e-114">意義</span><span class="sxs-lookup"><span data-stu-id="b9b3e-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9b3e-115"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="b9b3e-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b9b3e-116">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="b9b3e-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b9b3e-117">備註</span><span class="sxs-lookup"><span data-stu-id="b9b3e-117">Remarks</span></span>

<span data-ttu-id="b9b3e-118">**GlInitNames** 函式會將名稱堆疊初始化為其預設空白狀態。</span><span class="sxs-lookup"><span data-stu-id="b9b3e-118">The **glInitNames** function causes the name stack to be initialized to its default empty state.</span></span> <span data-ttu-id="b9b3e-119">在選取模式期間，會使用名稱堆疊來允許唯一識別的轉譯命令集。</span><span class="sxs-lookup"><span data-stu-id="b9b3e-119">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="b9b3e-120">它包含一組排序的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="b9b3e-120">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="b9b3e-121">當轉譯模式並非 GL 選取時，名稱堆疊一律是空的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b9b3e-121">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="b9b3e-122">當轉譯模式不是 GL 時，會忽略 **glInitNames** 的呼叫 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b9b3e-122">Calls to **glInitNames** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="b9b3e-123">下列函式會取出與 **glInitNames** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="b9b3e-123">The following functions retrieve information related to **glInitNames**:</span></span>

<span data-ttu-id="b9b3e-124">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 名稱 \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="b9b3e-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="b9b3e-125">具有引數 GL \_ 最大 \_ 名稱 \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="b9b3e-125">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="b9b3e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9b3e-126">Requirements</span></span>



| <span data-ttu-id="b9b3e-127">需求</span><span class="sxs-lookup"><span data-stu-id="b9b3e-127">Requirement</span></span> | <span data-ttu-id="b9b3e-128">值</span><span class="sxs-lookup"><span data-stu-id="b9b3e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9b3e-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9b3e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b9b3e-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9b3e-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9b3e-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9b3e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b9b3e-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9b3e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9b3e-133">標頭</span><span class="sxs-lookup"><span data-stu-id="b9b3e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9b3e-134"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="b9b3e-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b9b3e-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="b9b3e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9b3e-136"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9b3e-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b9b3e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b9b3e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9b3e-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9b3e-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9b3e-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9b3e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9b3e-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b9b3e-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b9b3e-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b9b3e-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b9b3e-142">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="b9b3e-142">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="b9b3e-143">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="b9b3e-143">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="b9b3e-144">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="b9b3e-144">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="b9b3e-145">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="b9b3e-145">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





