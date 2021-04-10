---
title: 'glClearColor 函式 (Gl) '
description: GlClearColor 函式會指定色彩緩衝區的明確值。
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- glClearColor 函式 OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686017"
---
# <a name="glclearcolor-function"></a><span data-ttu-id="0e9e8-104">glClearColor 函式</span><span class="sxs-lookup"><span data-stu-id="0e9e8-104">glClearColor function</span></span>

<span data-ttu-id="0e9e8-105">**GlClearColor** 函式會指定色彩緩衝區的明確值。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-105">The **glClearColor** function specifies clear values for the color buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9e8-106">語法</span><span class="sxs-lookup"><span data-stu-id="0e9e8-106">Syntax</span></span>


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a><span data-ttu-id="0e9e8-107">參數</span><span class="sxs-lookup"><span data-stu-id="0e9e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e9e8-108">*紅*</span><span class="sxs-lookup"><span data-stu-id="0e9e8-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9e8-109">[**GlClear**](glclear.md)用來清除色彩緩衝區的紅色值。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-109">The red value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="0e9e8-110">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="0e9e8-111">*綠色*</span><span class="sxs-lookup"><span data-stu-id="0e9e8-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9e8-112">[**GlClear**](glclear.md)用來清除色彩緩衝區的綠色值。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-112">The green value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="0e9e8-113">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="0e9e8-114">*藍色*</span><span class="sxs-lookup"><span data-stu-id="0e9e8-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9e8-115">[**GlClear**](glclear.md)用來清除色彩緩衝區的藍色值。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-115">The blue value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="0e9e8-116">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="0e9e8-117">*阿 爾 法*</span><span class="sxs-lookup"><span data-stu-id="0e9e8-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9e8-118">[**GlClear**](glclear.md)用來清除色彩緩衝區的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-118">The alpha value that [**glClear**](glclear.md) uses to clear the color buffers.</span></span> <span data-ttu-id="0e9e8-119">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e9e8-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e9e8-120">Return value</span></span>

<span data-ttu-id="0e9e8-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0e9e8-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0e9e8-122">Error codes</span></span>

<span data-ttu-id="0e9e8-123">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0e9e8-124">Name</span><span class="sxs-lookup"><span data-stu-id="0e9e8-124">Name</span></span>                                                                                                  | <span data-ttu-id="0e9e8-125">意義</span><span class="sxs-lookup"><span data-stu-id="0e9e8-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e9e8-126"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="0e9e8-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0e9e8-127">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0e9e8-128">備註</span><span class="sxs-lookup"><span data-stu-id="0e9e8-128">Remarks</span></span>

<span data-ttu-id="0e9e8-129">**GlClearColor** 函式會指定 [**glClear**](glclear.md)用來清除色彩緩衝區的紅色、綠色、藍色和 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-129">The **glClearColor** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the color buffers.</span></span> <span data-ttu-id="0e9e8-130">**GlClearColor** 所指定的值會壓制至範圍 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="0e9e8-130">Values specified by **glClearColor** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="0e9e8-131">下列函式會取出與 **glClearColor** 函數相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="0e9e8-131">The following functions retrieve information related to the **glClearColor** function:</span></span>

<span data-ttu-id="0e9e8-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ ACCUM \_ CLEAR \_ 值</span><span class="sxs-lookup"><span data-stu-id="0e9e8-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="0e9e8-133">具有引數 GL \_ 色彩 \_ 清除 \_ 值的 glGet</span><span class="sxs-lookup"><span data-stu-id="0e9e8-133">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9e8-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e9e8-134">Requirements</span></span>



| <span data-ttu-id="0e9e8-135">需求</span><span class="sxs-lookup"><span data-stu-id="0e9e8-135">Requirement</span></span> | <span data-ttu-id="0e9e8-136">值</span><span class="sxs-lookup"><span data-stu-id="0e9e8-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9e8-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e9e8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9e8-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e9e8-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0e9e8-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e9e8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9e8-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e9e8-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e9e8-141">標頭</span><span class="sxs-lookup"><span data-stu-id="0e9e8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e9e8-142"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="0e9e8-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0e9e8-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e9e8-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e9e8-144"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e9e8-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0e9e8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0e9e8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e9e8-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e9e8-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e9e8-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e9e8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9e8-148">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0e9e8-148">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0e9e8-149">**glClear**</span><span class="sxs-lookup"><span data-stu-id="0e9e8-149">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="0e9e8-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0e9e8-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0e9e8-151">**glGet**</span><span class="sxs-lookup"><span data-stu-id="0e9e8-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





