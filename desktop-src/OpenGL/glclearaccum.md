---
title: 'glClearAccum 函式 (Gl) '
description: GlClearAccum 函數會指定累積緩衝區的清除值。
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- glClearAccum 函式 OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104129"
---
# <a name="glclearaccum-function"></a><span data-ttu-id="0595b-104">glClearAccum 函式</span><span class="sxs-lookup"><span data-stu-id="0595b-104">glClearAccum function</span></span>

<span data-ttu-id="0595b-105">**GlClearAccum** 函數會指定累積緩衝區的清除值。</span><span class="sxs-lookup"><span data-stu-id="0595b-105">The **glClearAccum** function specifies the clear values for the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0595b-106">語法</span><span class="sxs-lookup"><span data-stu-id="0595b-106">Syntax</span></span>


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a><span data-ttu-id="0595b-107">參數</span><span class="sxs-lookup"><span data-stu-id="0595b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0595b-108">*紅*</span><span class="sxs-lookup"><span data-stu-id="0595b-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="0595b-109">清除累積緩衝區時使用的紅色值。</span><span class="sxs-lookup"><span data-stu-id="0595b-109">The red value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="0595b-110">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="0595b-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="0595b-111">*綠色*</span><span class="sxs-lookup"><span data-stu-id="0595b-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="0595b-112">清除累積緩衝區時使用的綠色值。</span><span class="sxs-lookup"><span data-stu-id="0595b-112">The green value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="0595b-113">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="0595b-113">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="0595b-114">*藍色*</span><span class="sxs-lookup"><span data-stu-id="0595b-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="0595b-115">清除累積緩衝區時使用的藍色值。</span><span class="sxs-lookup"><span data-stu-id="0595b-115">The blue value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="0595b-116">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="0595b-116">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="0595b-117">*阿 爾 法*</span><span class="sxs-lookup"><span data-stu-id="0595b-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="0595b-118">清除累積緩衝區時使用的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="0595b-118">The alpha value used when the accumulation buffer is cleared.</span></span> <span data-ttu-id="0595b-119">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="0595b-119">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0595b-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="0595b-120">Return value</span></span>

<span data-ttu-id="0595b-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0595b-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0595b-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0595b-122">Error codes</span></span>

<span data-ttu-id="0595b-123">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0595b-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0595b-124">Name</span><span class="sxs-lookup"><span data-stu-id="0595b-124">Name</span></span>                                                                                                  | <span data-ttu-id="0595b-125">意義</span><span class="sxs-lookup"><span data-stu-id="0595b-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0595b-126"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="0595b-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0595b-127">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="0595b-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0595b-128">備註</span><span class="sxs-lookup"><span data-stu-id="0595b-128">Remarks</span></span>

<span data-ttu-id="0595b-129">**GlClearAccum** 函數會指定 [**glClear**](glclear.md)用來清除累積緩衝區的紅色、綠色、藍色和 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="0595b-129">The **glClearAccum** function specifies the red, green, blue, and alpha values used by [**glClear**](glclear.md) to clear the accumulation buffer.</span></span>

<span data-ttu-id="0595b-130">**GlClearAccum** 所指定的值會壓制至範圍 \[ 1，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="0595b-130">Values specified by **glClearAccum** are clamped to the range \[1,1\].</span></span>

<span data-ttu-id="0595b-131">下列函式會抓取 **glClearAccum** 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="0595b-131">The following function retrieves information related to **glClearAccum**:</span></span>

<span data-ttu-id="0595b-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ ACCUM \_ CLEAR \_ 值</span><span class="sxs-lookup"><span data-stu-id="0595b-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="0595b-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="0595b-133">Requirements</span></span>



| <span data-ttu-id="0595b-134">需求</span><span class="sxs-lookup"><span data-stu-id="0595b-134">Requirement</span></span> | <span data-ttu-id="0595b-135">值</span><span class="sxs-lookup"><span data-stu-id="0595b-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0595b-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0595b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0595b-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0595b-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0595b-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0595b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0595b-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0595b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0595b-140">標頭</span><span class="sxs-lookup"><span data-stu-id="0595b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0595b-141"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="0595b-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0595b-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="0595b-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="0595b-143"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0595b-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0595b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0595b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0595b-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0595b-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0595b-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0595b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0595b-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0595b-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0595b-148">**glClear**</span><span class="sxs-lookup"><span data-stu-id="0595b-148">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="0595b-149">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0595b-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0595b-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="0595b-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





