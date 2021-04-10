---
title: 'glClearStencil 函式 (Gl) '
description: GlClearStencil 函數會指定樣板緩衝區的清除值。
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- glClearStencil 函式 OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78d831540b4c7833368bbac075835faaec359695
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934512"
---
# <a name="glclearstencil-function"></a><span data-ttu-id="01f14-104">glClearStencil 函式</span><span class="sxs-lookup"><span data-stu-id="01f14-104">glClearStencil function</span></span>

<span data-ttu-id="01f14-105">**GlClearStencil** 函數會指定樣板緩衝區的清除值。</span><span class="sxs-lookup"><span data-stu-id="01f14-105">The **glClearStencil** function specifies the clear value for the stencil buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f14-106">語法</span><span class="sxs-lookup"><span data-stu-id="01f14-106">Syntax</span></span>


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a><span data-ttu-id="01f14-107">參數</span><span class="sxs-lookup"><span data-stu-id="01f14-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f14-108">*s*</span><span class="sxs-lookup"><span data-stu-id="01f14-108">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="01f14-109">清除樣板緩衝區時使用的索引。</span><span class="sxs-lookup"><span data-stu-id="01f14-109">The index used when the stencil buffer is cleared.</span></span> <span data-ttu-id="01f14-110">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="01f14-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01f14-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="01f14-111">Return value</span></span>

<span data-ttu-id="01f14-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="01f14-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01f14-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="01f14-113">Error codes</span></span>

<span data-ttu-id="01f14-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="01f14-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="01f14-115">Name</span><span class="sxs-lookup"><span data-stu-id="01f14-115">Name</span></span>                                                                                                  | <span data-ttu-id="01f14-116">意義</span><span class="sxs-lookup"><span data-stu-id="01f14-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01f14-117"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="01f14-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="01f14-118">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="01f14-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="01f14-119">備註</span><span class="sxs-lookup"><span data-stu-id="01f14-119">Remarks</span></span>

<span data-ttu-id="01f14-120">**GlClearStencil** 函數會指定 [**glClear**](glclear.md)用來清除樣板緩衝區的索引。</span><span class="sxs-lookup"><span data-stu-id="01f14-120">The **glClearStencil** function specifies the index used by [**glClear**](glclear.md) to clear the stencil buffer.</span></span> <span data-ttu-id="01f14-121">*S* 參數的遮罩是 2 <sup>m</sup> -1，其中 *m* 是樣板緩衝區中的位數。</span><span class="sxs-lookup"><span data-stu-id="01f14-121">The *s* parameter is masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in the stencil buffer.</span></span>

<span data-ttu-id="01f14-122">下列函式會取出與 **glClearStencil** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="01f14-122">The following functions retrieve information related to the **glClearStencil** function:</span></span>

<span data-ttu-id="01f14-123">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 樣板 \_ CLEAR \_ 值的 glGet</span><span class="sxs-lookup"><span data-stu-id="01f14-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

<span data-ttu-id="01f14-124">具有引數 GL \_ 樣板 \_ 位的 glGet</span><span class="sxs-lookup"><span data-stu-id="01f14-124">**glGet** with argument GL\_STENCIL\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="01f14-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="01f14-125">Requirements</span></span>



| <span data-ttu-id="01f14-126">需求</span><span class="sxs-lookup"><span data-stu-id="01f14-126">Requirement</span></span> | <span data-ttu-id="01f14-127">值</span><span class="sxs-lookup"><span data-stu-id="01f14-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01f14-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01f14-128">Minimum supported client</span></span><br/> | <span data-ttu-id="01f14-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01f14-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="01f14-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01f14-130">Minimum supported server</span></span><br/> | <span data-ttu-id="01f14-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01f14-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01f14-132">標頭</span><span class="sxs-lookup"><span data-stu-id="01f14-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="01f14-133"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="01f14-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="01f14-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="01f14-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="01f14-135"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="01f14-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="01f14-136">DLL</span><span class="sxs-lookup"><span data-stu-id="01f14-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01f14-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01f14-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01f14-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01f14-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f14-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="01f14-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="01f14-140">**glClear**</span><span class="sxs-lookup"><span data-stu-id="01f14-140">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="01f14-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="01f14-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="01f14-142">**glGet**</span><span class="sxs-lookup"><span data-stu-id="01f14-142">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





