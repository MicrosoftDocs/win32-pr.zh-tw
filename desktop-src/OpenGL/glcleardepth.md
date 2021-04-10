---
title: 'glClearDepth 函式 (Gl) '
description: GlClearDepth 函數會指定深度緩衝區的清除值。
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- glClearDepth 函式 OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf968c7ae172bf4ce354c84b2071d62304327ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317288"
---
# <a name="glcleardepth-function"></a><span data-ttu-id="10627-104">glClearDepth 函式</span><span class="sxs-lookup"><span data-stu-id="10627-104">glClearDepth function</span></span>

<span data-ttu-id="10627-105">**GlClearDepth** 函數會指定深度緩衝區的清除值。</span><span class="sxs-lookup"><span data-stu-id="10627-105">The **glClearDepth** function specifies the clear value for the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="10627-106">語法</span><span class="sxs-lookup"><span data-stu-id="10627-106">Syntax</span></span>


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a><span data-ttu-id="10627-107">參數</span><span class="sxs-lookup"><span data-stu-id="10627-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10627-108">*深度*</span><span class="sxs-lookup"><span data-stu-id="10627-108">*depth*</span></span> 
</dt> <dd>

<span data-ttu-id="10627-109">清除深度緩衝區時所使用的深度值。</span><span class="sxs-lookup"><span data-stu-id="10627-109">The depth value used when the depth buffer is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10627-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="10627-110">Return value</span></span>

<span data-ttu-id="10627-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="10627-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10627-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="10627-112">Error codes</span></span>

<span data-ttu-id="10627-113">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="10627-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="10627-114">Name</span><span class="sxs-lookup"><span data-stu-id="10627-114">Name</span></span>                                                                                                  | <span data-ttu-id="10627-115">意義</span><span class="sxs-lookup"><span data-stu-id="10627-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="10627-116"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="10627-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="10627-117">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="10627-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="10627-118">備註</span><span class="sxs-lookup"><span data-stu-id="10627-118">Remarks</span></span>

<span data-ttu-id="10627-119">**GlClearDepth** 函數會指定 [**glClear**](glclear.md)用來清除深度緩衝區的深度值。</span><span class="sxs-lookup"><span data-stu-id="10627-119">The **glClearDepth** function specifies the depth value used by [**glClear**](glclear.md) to clear the depth buffer.</span></span> <span data-ttu-id="10627-120">**GlClearDepth** 所指定的值會壓制至範圍 \[ 0，1 \] 。</span><span class="sxs-lookup"><span data-stu-id="10627-120">Values specified by **glClearDepth** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="10627-121">下列函式會抓取 **glClearDepth** 函數的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="10627-121">The following function retrieves information related to the **glClearDepth** function:</span></span>

<span data-ttu-id="10627-122">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 深度 \_ 清除 \_ 值的 glGet</span><span class="sxs-lookup"><span data-stu-id="10627-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="10627-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="10627-123">Requirements</span></span>



| <span data-ttu-id="10627-124">需求</span><span class="sxs-lookup"><span data-stu-id="10627-124">Requirement</span></span> | <span data-ttu-id="10627-125">值</span><span class="sxs-lookup"><span data-stu-id="10627-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10627-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10627-126">Minimum supported client</span></span><br/> | <span data-ttu-id="10627-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10627-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="10627-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10627-128">Minimum supported server</span></span><br/> | <span data-ttu-id="10627-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10627-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="10627-130">標頭</span><span class="sxs-lookup"><span data-stu-id="10627-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="10627-131"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="10627-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="10627-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="10627-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="10627-133"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="10627-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="10627-134">DLL</span><span class="sxs-lookup"><span data-stu-id="10627-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10627-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10627-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10627-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10627-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10627-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="10627-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="10627-138">**glClear**</span><span class="sxs-lookup"><span data-stu-id="10627-138">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="10627-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="10627-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="10627-140">**glGet**</span><span class="sxs-lookup"><span data-stu-id="10627-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





