---
title: 'glFlush 函式 (Gl) '
description: GlFlush 函式會在有限的時間內強制執行 OpenGL 函數。
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- glFlush 函式 OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686615"
---
# <a name="glflush-function"></a><span data-ttu-id="e9bce-104">glFlush 函式</span><span class="sxs-lookup"><span data-stu-id="e9bce-104">glFlush function</span></span>

<span data-ttu-id="e9bce-105">**GlFlush** 函式會在有限的時間內強制執行 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="e9bce-105">The **glFlush** function forces execution of OpenGL functions in finite time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9bce-106">語法</span><span class="sxs-lookup"><span data-stu-id="e9bce-106">Syntax</span></span>


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a><span data-ttu-id="e9bce-107">參數</span><span class="sxs-lookup"><span data-stu-id="e9bce-107">Parameters</span></span>

<span data-ttu-id="e9bce-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="e9bce-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9bce-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9bce-109">Return value</span></span>

<span data-ttu-id="e9bce-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e9bce-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e9bce-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e9bce-111">Error codes</span></span>

<span data-ttu-id="e9bce-112">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e9bce-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e9bce-113">Name</span><span class="sxs-lookup"><span data-stu-id="e9bce-113">Name</span></span>                                                                                                  | <span data-ttu-id="e9bce-114">意義</span><span class="sxs-lookup"><span data-stu-id="e9bce-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9bce-115"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="e9bce-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e9bce-116">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="e9bce-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e9bce-117">備註</span><span class="sxs-lookup"><span data-stu-id="e9bce-117">Remarks</span></span>

<span data-ttu-id="e9bce-118">許多不同位置中的不同 OpenGL 執行緩衝區命令，包括網路緩衝區和圖形加速器本身。</span><span class="sxs-lookup"><span data-stu-id="e9bce-118">Different OpenGL implementations buffer commands in several different locations, including network buffers and the graphics accelerator itself.</span></span> <span data-ttu-id="e9bce-119">**GlFlush** 函式會清空所有這些緩衝區，使所有發出的命令都能以實際轉譯引擎接受的速度快速執行。</span><span class="sxs-lookup"><span data-stu-id="e9bce-119">The **glFlush** function empties all these buffers, causing all issued commands to be executed as quickly as they are accepted by the actual rendering engine.</span></span> <span data-ttu-id="e9bce-120">雖然這項執行可能不會在任何特定時間內完成，但會在有限的時間內完成。</span><span class="sxs-lookup"><span data-stu-id="e9bce-120">Though this execution may not be completed in any particular time period, it does complete in a finite amount of time.</span></span>

<span data-ttu-id="e9bce-121">因為任何 OpenGL 程式可能會在網路上執行，或在緩衝命令的加速器上執行，所以請務必在要求所有先前發出的命令都已完成的程式中呼叫 **glFlush** 。</span><span class="sxs-lookup"><span data-stu-id="e9bce-121">Because any OpenGL program might be executed over a network, or on an accelerator that buffers commands, be sure to call **glFlush** in any programs requiring that all of their previously issued commands have been completed.</span></span> <span data-ttu-id="e9bce-122">例如，在等候相依于所產生影像的使用者輸入之前，請先呼叫 **glFlush** 。</span><span class="sxs-lookup"><span data-stu-id="e9bce-122">For example, call **glFlush** before waiting for user input that depends on the generated image.</span></span>

<span data-ttu-id="e9bce-123">**GlFlush** 函式可以隨時返回。</span><span class="sxs-lookup"><span data-stu-id="e9bce-123">The **glFlush** function can return at any time.</span></span> <span data-ttu-id="e9bce-124">它不會等到所有先前發行的 OpenGL 函式執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="e9bce-124">It does not wait until the execution of all previously issued OpenGL functions is complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9bce-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9bce-125">Requirements</span></span>



| <span data-ttu-id="e9bce-126">需求</span><span class="sxs-lookup"><span data-stu-id="e9bce-126">Requirement</span></span> | <span data-ttu-id="e9bce-127">值</span><span class="sxs-lookup"><span data-stu-id="e9bce-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bce-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9bce-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e9bce-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9bce-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e9bce-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9bce-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e9bce-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9bce-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9bce-132">標頭</span><span class="sxs-lookup"><span data-stu-id="e9bce-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9bce-133"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="e9bce-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e9bce-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9bce-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9bce-135"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9bce-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e9bce-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e9bce-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9bce-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9bce-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9bce-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9bce-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9bce-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e9bce-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e9bce-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e9bce-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e9bce-141">**glFinish**</span><span class="sxs-lookup"><span data-stu-id="e9bce-141">**glFinish**</span></span>](glfinish.md)
</dt> </dl>

 

 





