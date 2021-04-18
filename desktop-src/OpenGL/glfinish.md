---
title: 'glFinish 函式 (Gl) '
description: GlFinish 函式會封鎖，直到所有 OpenGL 執行完成為止。
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
keywords:
- glFinish 函式 OpenGL
topic_type:
- apiref
api_name:
- glFinish
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731ffc91dbb8d31137a792b59d3ebc36bb4d5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509451"
---
# <a name="glfinish-function"></a><span data-ttu-id="5f925-104">glFinish 函式</span><span class="sxs-lookup"><span data-stu-id="5f925-104">glFinish function</span></span>

<span data-ttu-id="5f925-105">**GlFinish** 函式會封鎖，直到所有 OpenGL 執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="5f925-105">The **glFinish** function blocks until all OpenGL execution is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f925-106">語法</span><span class="sxs-lookup"><span data-stu-id="5f925-106">Syntax</span></span>


```C++
void WINAPI glFinish(void);
```



## <a name="parameters"></a><span data-ttu-id="5f925-107">參數</span><span class="sxs-lookup"><span data-stu-id="5f925-107">Parameters</span></span>

<span data-ttu-id="5f925-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="5f925-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f925-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f925-109">Return value</span></span>

<span data-ttu-id="5f925-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5f925-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5f925-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5f925-111">Error codes</span></span>

<span data-ttu-id="5f925-112">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5f925-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5f925-113">Name</span><span class="sxs-lookup"><span data-stu-id="5f925-113">Name</span></span>                                                                                                  | <span data-ttu-id="5f925-114">意義</span><span class="sxs-lookup"><span data-stu-id="5f925-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f925-115"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="5f925-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5f925-116">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="5f925-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5f925-117">備註</span><span class="sxs-lookup"><span data-stu-id="5f925-117">Remarks</span></span>

<span data-ttu-id="5f925-118">**GlFinish** 函式必須等到所有先前呼叫之 OpenGL 函式的效果都完成後，才會傳回。</span><span class="sxs-lookup"><span data-stu-id="5f925-118">The **glFinish** function does not return until the effects of all previously called OpenGL functions are complete.</span></span> <span data-ttu-id="5f925-119">這類效果包括所有 OpenGL 狀態的變更、連接狀態的所有變更，以及畫面格緩衝區內容的所有變更。</span><span class="sxs-lookup"><span data-stu-id="5f925-119">Such effects include all changes to the OpenGL state, all changes to the connection state, and all changes to the framebuffer contents.</span></span>

<span data-ttu-id="5f925-120">**GlFinish** 函式需要伺服器的來回行程。</span><span class="sxs-lookup"><span data-stu-id="5f925-120">The **glFinish** function requires a round trip to the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f925-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f925-121">Requirements</span></span>



| <span data-ttu-id="5f925-122">需求</span><span class="sxs-lookup"><span data-stu-id="5f925-122">Requirement</span></span> | <span data-ttu-id="5f925-123">值</span><span class="sxs-lookup"><span data-stu-id="5f925-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f925-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f925-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5f925-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f925-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5f925-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5f925-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5f925-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5f925-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f925-128">標頭</span><span class="sxs-lookup"><span data-stu-id="5f925-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f925-129"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="5f925-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5f925-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="5f925-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f925-131"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f925-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f925-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5f925-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f925-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f925-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f925-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f925-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f925-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5f925-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5f925-136">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5f925-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5f925-137">**glFlush**</span><span class="sxs-lookup"><span data-stu-id="5f925-137">**glFlush**</span></span>](glflush.md)
</dt> </dl>

 

 





