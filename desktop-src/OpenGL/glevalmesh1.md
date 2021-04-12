---
title: 'glEvalMesh1 函式 (Gl) '
description: 計算點或線條的一維方格。
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- glEvalMesh1 函式 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508787"
---
# <a name="glevalmesh1-function"></a><span data-ttu-id="f598b-104">glEvalMesh1 函式</span><span class="sxs-lookup"><span data-stu-id="f598b-104">glEvalMesh1 function</span></span>

<span data-ttu-id="f598b-105">計算點或線條的一維方格。</span><span class="sxs-lookup"><span data-stu-id="f598b-105">Computes a one-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="f598b-106">語法</span><span class="sxs-lookup"><span data-stu-id="f598b-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a><span data-ttu-id="f598b-107">參數</span><span class="sxs-lookup"><span data-stu-id="f598b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f598b-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="f598b-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="f598b-109">值，指定是否要計算點或線條的一維網格。</span><span class="sxs-lookup"><span data-stu-id="f598b-109">A value that specifies whether to compute a one-dimensional mesh of points or lines.</span></span> <span data-ttu-id="f598b-110">接受下列符號常數： GL \_ 點和 gl \_ 行。</span><span class="sxs-lookup"><span data-stu-id="f598b-110">The following symbolic constants are accepted: GL\_POINT and GL\_LINE.</span></span>

</dd> <dt>

<span data-ttu-id="f598b-111">*i1*</span><span class="sxs-lookup"><span data-stu-id="f598b-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="f598b-112">方格網域變數 i 的第一個整數值。</span><span class="sxs-lookup"><span data-stu-id="f598b-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="f598b-113">*i2*</span><span class="sxs-lookup"><span data-stu-id="f598b-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="f598b-114">方格網域變數 i 的最後一個整數值。</span><span class="sxs-lookup"><span data-stu-id="f598b-114">The last integer value for grid domain variable i.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f598b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f598b-115">Return value</span></span>

<span data-ttu-id="f598b-116">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f598b-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f598b-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="f598b-117">Error codes</span></span>

<span data-ttu-id="f598b-118">[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f598b-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f598b-119">Name</span><span class="sxs-lookup"><span data-stu-id="f598b-119">Name</span></span>                                                                                                  | <span data-ttu-id="f598b-120">意義</span><span class="sxs-lookup"><span data-stu-id="f598b-120">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f598b-121"><dt>**GL \_ 無效 \_ 列舉**</dt></span><span class="sxs-lookup"><span data-stu-id="f598b-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f598b-122">表示 *模式* 不是可接受的值。</span><span class="sxs-lookup"><span data-stu-id="f598b-122">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="f598b-123"><dt>**GL \_ 不正確 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="f598b-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f598b-124">呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。</span><span class="sxs-lookup"><span data-stu-id="f598b-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="f598b-125">備註</span><span class="sxs-lookup"><span data-stu-id="f598b-125">Remarks</span></span>

<span data-ttu-id="f598b-126">將 [**glMapGrid**](glmapgrid-functions.md) 和 [**glEvalMesh**](glevalmesh-functions.md) 一起使用，可有效率地產生和評估一系列平均間距的地圖定義域值。</span><span class="sxs-lookup"><span data-stu-id="f598b-126">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) together to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="f598b-127">**GlEvalMesh** 函式會逐步執行一維或二維方格的整數定義域，其範圍是 [**glMap1**](glmap1.md)和 [**glMap2**](glmap2.md)所指定之評估對應的定義域。</span><span class="sxs-lookup"><span data-stu-id="f598b-127">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="f598b-128">Mode 參數會決定產生的頂點是否以點、線條或填滿的多邊形連接。</span><span class="sxs-lookup"><span data-stu-id="f598b-128">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="f598b-129">在一維的案例中， **glEvalMesh1** 會產生網格，就像執行下列程式碼片段一樣：</span><span class="sxs-lookup"><span data-stu-id="f598b-129">In the one-dimensional case, **glEvalMesh1**, the mesh is generated as if the following code fragment were executed:</span></span>

<span data-ttu-id="f598b-130">[**glBegin**](glbegin.md) (*類型*) ;</span><span class="sxs-lookup"><span data-stu-id="f598b-130">[**glBegin**](glbegin.md)(*type*);</span></span>

<span data-ttu-id="f598b-131">針對 (i = i1;i <= i2;i + = 1) </span><span class="sxs-lookup"><span data-stu-id="f598b-131">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="f598b-132">{</span><span class="sxs-lookup"><span data-stu-id="f598b-132">{</span></span>

<span data-ttu-id="f598b-133">[**glEvalCoord1**](glevalcoord1d.md) (i？ u + u1) </span><span class="sxs-lookup"><span data-stu-id="f598b-133">[**glEvalCoord1**](glevalcoord1d.md)(i?u + u1)</span></span>

<span data-ttu-id="f598b-134">}</span><span class="sxs-lookup"><span data-stu-id="f598b-134">}</span></span>

<span data-ttu-id="f598b-135">[**glEnd**](glend.md) ( ) ;</span><span class="sxs-lookup"><span data-stu-id="f598b-135">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="f598b-136">其中</span><span class="sxs-lookup"><span data-stu-id="f598b-136">where</span></span>

<span data-ttu-id="f598b-137">？ u = (u2 u1) /n</span><span class="sxs-lookup"><span data-stu-id="f598b-137">?u = (u2 u1) / n</span></span>

<span data-ttu-id="f598b-138">和 n、u1 和 u2 是最新 [**glMapGrid1**](glmapgrid1d.md) 函式的引數。</span><span class="sxs-lookup"><span data-stu-id="f598b-138">and n, u1, and u2 are the arguments to the most recent [**glMapGrid1**](glmapgrid1d.md) function.</span></span> <span data-ttu-id="f598b-139"> \_ 如果模式為 gl 點，則類型參數為 gl 點 \_ ， \_ 如果模式為 GL 行，則為 gl 行 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f598b-139">The *type* parameter is GL\_POINTS if mode is GL\_POINT, or GL\_LINES if mode is GL\_LINE.</span></span> <span data-ttu-id="f598b-140">其中一個絕對數值需求是，如果 i = n，則計算自 i？ u + u1 的值就完全是 u2。</span><span class="sxs-lookup"><span data-stu-id="f598b-140">The one absolute numeric requirement is that if i = n, then the value computed from i?u + u1 is exactly u2.</span></span>

## <a name="requirements"></a><span data-ttu-id="f598b-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="f598b-141">Requirements</span></span>



| <span data-ttu-id="f598b-142">需求</span><span class="sxs-lookup"><span data-stu-id="f598b-142">Requirement</span></span> | <span data-ttu-id="f598b-143">值</span><span class="sxs-lookup"><span data-stu-id="f598b-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f598b-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f598b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f598b-145">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f598b-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f598b-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f598b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f598b-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f598b-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f598b-148">標頭</span><span class="sxs-lookup"><span data-stu-id="f598b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="f598b-149"><dt>Gl</dt></span><span class="sxs-lookup"><span data-stu-id="f598b-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f598b-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="f598b-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="f598b-151"><dt>Opengl32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f598b-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f598b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="f598b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f598b-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f598b-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f598b-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f598b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f598b-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f598b-155">**glBegin**</span></span>](glbegin.md)
</dt> </dl>

 

 





