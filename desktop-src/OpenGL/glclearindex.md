---
title: 'glClearIndex 函式 (Gl) '
description: GlClearIndex 函數會指定色彩索引緩衝區的清除值。
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- glClearIndex 函式 OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465657"
---
# <a name="glclearindex-function"></a><span data-ttu-id="7aea6-104">glClearIndex 函式</span><span class="sxs-lookup"><span data-stu-id="7aea6-104">glClearIndex function</span></span>

<span data-ttu-id="7aea6-105">**GlClearIndex** 函數會指定色彩索引緩衝區的清除值。</span><span class="sxs-lookup"><span data-stu-id="7aea6-105">The **glClearIndex** function specifies the clear value for the color-index buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aea6-106">語法</span><span class="sxs-lookup"><span data-stu-id="7aea6-106">Syntax</span></span>


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a><span data-ttu-id="7aea6-107">參數</span><span class="sxs-lookup"><span data-stu-id="7aea6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aea6-108">*c*</span><span class="sxs-lookup"><span data-stu-id="7aea6-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="7aea6-109">清除色彩索引緩衝區時使用的索引。</span><span class="sxs-lookup"><span data-stu-id="7aea6-109">The index used when the color-index buffers are cleared.</span></span> <span data-ttu-id="7aea6-110">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="7aea6-110">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aea6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7aea6-111">Return value</span></span>

<span data-ttu-id="7aea6-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7aea6-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7aea6-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7aea6-113">Error codes</span></span>

<span data-ttu-id="7aea6-114">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7aea6-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7aea6-115">Name</span><span class="sxs-lookup"><span data-stu-id="7aea6-115">Name</span></span>                                                                                                  | <span data-ttu-id="7aea6-116">意義</span><span class="sxs-lookup"><span data-stu-id="7aea6-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7aea6-117"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="7aea6-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7aea6-118">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="7aea6-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7aea6-119">備註</span><span class="sxs-lookup"><span data-stu-id="7aea6-119">Remarks</span></span>

<span data-ttu-id="7aea6-120">**GlClearIndex** 函數會指定 [**glClear**](glclear.md)用來清除色彩索引緩衝區的索引。</span><span class="sxs-lookup"><span data-stu-id="7aea6-120">The **glClearIndex** function specifies the index used by [**glClear**](glclear.md) to clear the color-index buffers.</span></span> <span data-ttu-id="7aea6-121">*C* 參數不是壓制。</span><span class="sxs-lookup"><span data-stu-id="7aea6-121">The *c* parameter is not clamped.</span></span> <span data-ttu-id="7aea6-122">相反地， *c* 會轉換成具有二進位點右邊未指定精確度的固定點值。</span><span class="sxs-lookup"><span data-stu-id="7aea6-122">Rather, *c* is converted to a fixed-point value with unspecified precision to the right of the binary point.</span></span> <span data-ttu-id="7aea6-123">然後，此值的整數部分會以 2 <sup>m</sup>  -1 遮罩，其中 *m* 是儲存在畫面格緩衝區中之色彩索引的位數。</span><span class="sxs-lookup"><span data-stu-id="7aea6-123">The integer part of this value is then masked with 2 <sup>m</sup>  - 1, where *m* is the number of bits in a color index stored in the framebuffer.</span></span>

<span data-ttu-id="7aea6-124">下列函式會取出與 **glClearIndex** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="7aea6-124">The following functions retrieve information related to **glClearIndex**:</span></span>

<span data-ttu-id="7aea6-125">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 索引 \_ 清除 \_ 值的 glGet</span><span class="sxs-lookup"><span data-stu-id="7aea6-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="7aea6-126">具有引數 GL \_ 索引 \_ 位的 glGet</span><span class="sxs-lookup"><span data-stu-id="7aea6-126">**glGet** with argument GL\_INDEX\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="7aea6-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="7aea6-127">Requirements</span></span>



| <span data-ttu-id="7aea6-128">需求</span><span class="sxs-lookup"><span data-stu-id="7aea6-128">Requirement</span></span> | <span data-ttu-id="7aea6-129">值</span><span class="sxs-lookup"><span data-stu-id="7aea6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7aea6-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7aea6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7aea6-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7aea6-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7aea6-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7aea6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7aea6-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7aea6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7aea6-134">標頭</span><span class="sxs-lookup"><span data-stu-id="7aea6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aea6-135"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="7aea6-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7aea6-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="7aea6-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="7aea6-137"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7aea6-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7aea6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7aea6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aea6-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aea6-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aea6-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7aea6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aea6-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7aea6-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7aea6-142">**glClear**</span><span class="sxs-lookup"><span data-stu-id="7aea6-142">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="7aea6-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7aea6-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7aea6-144">**glGet**</span><span class="sxs-lookup"><span data-stu-id="7aea6-144">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





