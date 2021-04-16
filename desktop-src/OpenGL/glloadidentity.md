---
title: 'glLoadIdentity 函式 (Gl) '
description: GlLoadIdentity 函式會將目前的矩陣取代為識別矩陣。
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- glLoadIdentity 函式 OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a2afde8ae06602933d6790c4fce33e9130a78cb
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "104552634"
---
# <a name="glloadidentity-function"></a><span data-ttu-id="e60c8-104">glLoadIdentity 函式</span><span class="sxs-lookup"><span data-stu-id="e60c8-104">glLoadIdentity function</span></span>

<span data-ttu-id="e60c8-105">**GlLoadIdentity** 函式會將目前的矩陣取代為識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="e60c8-105">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e60c8-106">語法</span><span class="sxs-lookup"><span data-stu-id="e60c8-106">Syntax</span></span>


```C++
void WINAPI glLoadIdentity(void);
```



## <a name="parameters"></a><span data-ttu-id="e60c8-107">參數</span><span class="sxs-lookup"><span data-stu-id="e60c8-107">Parameters</span></span>

<span data-ttu-id="e60c8-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="e60c8-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e60c8-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e60c8-109">Return value</span></span>

<span data-ttu-id="e60c8-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e60c8-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e60c8-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e60c8-111">Error codes</span></span>

<span data-ttu-id="e60c8-112">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e60c8-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e60c8-113">Name</span><span class="sxs-lookup"><span data-stu-id="e60c8-113">Name</span></span>                                                                                                  | <span data-ttu-id="e60c8-114">意義</span><span class="sxs-lookup"><span data-stu-id="e60c8-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e60c8-115"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="e60c8-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e60c8-116">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="e60c8-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e60c8-117">備註</span><span class="sxs-lookup"><span data-stu-id="e60c8-117">Remarks</span></span>

<span data-ttu-id="e60c8-118">**GlLoadIdentity** 函式會將目前的矩陣取代為識別矩陣。</span><span class="sxs-lookup"><span data-stu-id="e60c8-118">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span> <span data-ttu-id="e60c8-119">在語義上相當於使用下列識別矩陣來呼叫 [**glLoadMatrix**](glloadmatrix.md) 。</span><span class="sxs-lookup"><span data-stu-id="e60c8-119">It is semantically equivalent to calling [**glLoadMatrix**](glloadmatrix.md) with the following identity matrix.</span></span>

![顯示 glLoadIdentity 呼叫之身分識別矩陣的圖表。](images/load01.png)

<span data-ttu-id="e60c8-121">不過，在某些情況下，這會更有效率。</span><span class="sxs-lookup"><span data-stu-id="e60c8-121">However, in some cases, it is more efficient.</span></span>

<span data-ttu-id="e60c8-122">下列函式會取出與 **glLoadIdentity** 相關的資訊：</span><span class="sxs-lookup"><span data-stu-id="e60c8-122">The following functions retrieve information related to **glLoadIdentity**:</span></span>

<span data-ttu-id="e60c8-123">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet</span><span class="sxs-lookup"><span data-stu-id="e60c8-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="e60c8-124">具有引數 GL \_ 模型 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="e60c8-124">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="e60c8-125">具有引數 GL \_ 投射 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="e60c8-125">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="e60c8-126">具有引數 GL \_ 材質 \_ 矩陣的 glGet</span><span class="sxs-lookup"><span data-stu-id="e60c8-126">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="e60c8-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="e60c8-127">Requirements</span></span>



| <span data-ttu-id="e60c8-128">需求</span><span class="sxs-lookup"><span data-stu-id="e60c8-128">Requirement</span></span> | <span data-ttu-id="e60c8-129">值</span><span class="sxs-lookup"><span data-stu-id="e60c8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e60c8-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e60c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e60c8-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e60c8-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e60c8-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e60c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e60c8-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e60c8-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e60c8-134">標頭</span><span class="sxs-lookup"><span data-stu-id="e60c8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e60c8-135"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="e60c8-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e60c8-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="e60c8-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="e60c8-137"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e60c8-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e60c8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e60c8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e60c8-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e60c8-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e60c8-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e60c8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e60c8-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e60c8-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e60c8-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e60c8-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e60c8-143">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="e60c8-143">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="e60c8-144">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="e60c8-144">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="e60c8-145">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="e60c8-145">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="e60c8-146">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="e60c8-146">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





