---
title: 'glLoadName 函式 (Gl) '
description: GlLoadName 函式會將名稱載入至名稱堆疊。
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- glLoadName 函式 OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb47a0389cda13523104ee429bca46838970e15a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106410"
---
# <a name="glloadname-function"></a><span data-ttu-id="b45e8-104">glLoadName 函式</span><span class="sxs-lookup"><span data-stu-id="b45e8-104">glLoadName function</span></span>

<span data-ttu-id="b45e8-105">**GlLoadName** 函式會將名稱載入至名稱堆疊。</span><span class="sxs-lookup"><span data-stu-id="b45e8-105">The **glLoadName** function loads a name onto the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="b45e8-106">語法</span><span class="sxs-lookup"><span data-stu-id="b45e8-106">Syntax</span></span>


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="b45e8-107">參數</span><span class="sxs-lookup"><span data-stu-id="b45e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b45e8-108">*name*</span><span class="sxs-lookup"><span data-stu-id="b45e8-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="b45e8-109">將取代名稱堆疊頂端值的名稱。</span><span class="sxs-lookup"><span data-stu-id="b45e8-109">A name that will replace the top value on the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b45e8-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b45e8-110">Return value</span></span>

<span data-ttu-id="b45e8-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b45e8-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b45e8-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b45e8-112">Error codes</span></span>

<span data-ttu-id="b45e8-113">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b45e8-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b45e8-114">Name</span><span class="sxs-lookup"><span data-stu-id="b45e8-114">Name</span></span>                                                                                                  | <span data-ttu-id="b45e8-115">意義</span><span class="sxs-lookup"><span data-stu-id="b45e8-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b45e8-116"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="b45e8-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b45e8-117">當名稱堆疊為空白時，就會呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="b45e8-117">The function was called while the name stack was empty.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="b45e8-118"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="b45e8-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b45e8-119">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="b45e8-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b45e8-120">備註</span><span class="sxs-lookup"><span data-stu-id="b45e8-120">Remarks</span></span>

<span data-ttu-id="b45e8-121">**GlLoadName** 函式會導致 *名稱* 取代名稱堆疊頂端的值，這一開始是空的。</span><span class="sxs-lookup"><span data-stu-id="b45e8-121">The **glLoadName** function causes *name* to replace the value on the top of the name stack, which is initially empty.</span></span> <span data-ttu-id="b45e8-122">在選取模式期間，會使用名稱堆疊來允許唯一識別的轉譯命令集。</span><span class="sxs-lookup"><span data-stu-id="b45e8-122">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="b45e8-123">它包含一組排序的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="b45e8-123">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="b45e8-124">當轉譯模式並非 GL 選取時，名稱堆疊一律是空的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b45e8-124">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="b45e8-125">當轉譯模式不是 GL 時，會忽略 **glLoadName** 的呼叫 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b45e8-125">Calls to **glLoadName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="b45e8-126">下列函式會取出與 **glLoadName** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="b45e8-126">The following functions retrieve information related to **glLoadName**:</span></span>

<span data-ttu-id="b45e8-127">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 名稱 \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="b45e8-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="b45e8-128">具有引數 GL \_ 最大 \_ 名稱 \_ STACK \_ 深度的 glGet</span><span class="sxs-lookup"><span data-stu-id="b45e8-128">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="b45e8-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b45e8-129">Requirements</span></span>



| <span data-ttu-id="b45e8-130">需求</span><span class="sxs-lookup"><span data-stu-id="b45e8-130">Requirement</span></span> | <span data-ttu-id="b45e8-131">值</span><span class="sxs-lookup"><span data-stu-id="b45e8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b45e8-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b45e8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b45e8-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b45e8-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b45e8-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b45e8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b45e8-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b45e8-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b45e8-136">標頭</span><span class="sxs-lookup"><span data-stu-id="b45e8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b45e8-137"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="b45e8-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b45e8-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="b45e8-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="b45e8-139"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b45e8-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b45e8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b45e8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b45e8-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b45e8-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b45e8-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b45e8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b45e8-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b45e8-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b45e8-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b45e8-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b45e8-145">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="b45e8-145">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="b45e8-146">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="b45e8-146">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="b45e8-147">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="b45e8-147">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="b45e8-148">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="b45e8-148">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





