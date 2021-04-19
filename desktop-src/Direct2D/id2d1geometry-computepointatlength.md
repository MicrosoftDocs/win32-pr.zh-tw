---
title: ID2D1Geometry ComputePointAtLength 方法
description: 沿著指定的距離，以 \ 160; geometry 計算點和正切向量。
ms.assetid: b76aa3db-2967-4baa-a449-f664b080fb74
keywords:
- ComputePointAtLength 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5b49be0b5a17dd828c9bd86ca41b4a3ff115f47a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991034"
---
# <a name="id2d1geometrycomputepointatlength-methods"></a><span data-ttu-id="d2ef3-104">ID2D1Geometry：： ComputePointAtLength 方法</span><span class="sxs-lookup"><span data-stu-id="d2ef3-104">ID2D1Geometry::ComputePointAtLength methods</span></span>

<span data-ttu-id="d2ef3-105">計算沿著幾何之指定距離的點和正切向量。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-105">Calculates the point and tangent vector at the specified distance along the geometry.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d2ef3-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="d2ef3-106">Overload list</span></span>



| <span data-ttu-id="d2ef3-107">方法</span><span class="sxs-lookup"><span data-stu-id="d2ef3-107">Method</span></span>                                                                                                                                                                                                        | <span data-ttu-id="d2ef3-108">描述</span><span class="sxs-lookup"><span data-stu-id="d2ef3-108">Description</span></span>                                                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ef3-109">[**ComputePointAtLength (浮點數、D2D1 \_ 矩陣 \_ 3X2 \_ F&、D2D1 \_ 點 \_ 2f \* 、D2D1 \_ 點 \_ 2f \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f__d2d1_point_2f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="d2ef3-109">[**ComputePointAtLength(FLOAT,D2D1\_MATRIX\_3X2\_F&,D2D1\_POINT\_2F\*,D2D1\_POINT\_2F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f__d2d1_point_2f_d2d1_point_2f))</span></span>              | <span data-ttu-id="d2ef3-110">依指定的矩陣轉換之後，以指定的距離計算點和正切向量，並使用預設的容錯值壓平合併。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-110">Calculates the point and tangent vector at the specified distance along the geometry after it has been transformed by the specified matrix and flattened using the default tolerance.</span></span><br/>   |
| <span data-ttu-id="d2ef3-111">[**ComputePointAtLength (FLOAT、D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、D2D1 \_ 點 \_ 2f \* 、D2D1 \_ POINT \_ 2f \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_d2d1_point_2f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="d2ef3-111">[**ComputePointAtLength(FLOAT,D2D1\_MATRIX\_3X2\_F\*,D2D1\_POINT\_2F\*,D2D1\_POINT\_2F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_d2d1_point_2f_d2d1_point_2f))</span></span>             | <span data-ttu-id="d2ef3-112">依指定的矩陣轉換之後，以指定的距離計算點和正切向量，並使用預設的容錯值壓平合併。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-112">Calculates the point and tangent vector at the specified distance along the geometry after it has been transformed by the specified matrix and flattened using the default tolerance.</span></span><br/>   |
| <span data-ttu-id="d2ef3-113">[**ComputePointAtLength (FLOAT、D2D1 \_ 矩陣 \_ 3X2 \_ F&、FLOAT、D2D1 \_ POINT \_ 2f \* 、D2D1 \_ POINT \_ 2f \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink))</span><span class="sxs-lookup"><span data-stu-id="d2ef3-113">[**ComputePointAtLength(FLOAT,D2D1\_MATRIX\_3X2\_F&,FLOAT,D2D1\_POINT\_2F\*,D2D1\_POINT\_2F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink))</span></span>  | <span data-ttu-id="d2ef3-114">依指定的矩陣轉換之後，在幾何的指定距離上計算點和正切向量，並使用指定的容錯值進行壓平合併。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-114">Calculates the point and tangent vector at the specified distance along the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/> |
| <span data-ttu-id="d2ef3-115">[**ComputePointAtLength (FLOAT、D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、FLOAT、D2D1 \_ POINT \_ 2f \* 、D2D1 \_ POINT \_ 2f \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_float_d2d1_point_2f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="d2ef3-115">[**ComputePointAtLength(FLOAT,D2D1\_MATRIX\_3X2\_F\*,FLOAT,D2D1\_POINT\_2F\*,D2D1\_POINT\_2F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_float_d2d1_point_2f_d2d1_point_2f))</span></span> | <span data-ttu-id="d2ef3-116">依指定的矩陣轉換之後，在幾何的指定距離上計算點和正切向量，並使用指定的容錯值進行壓平合併。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-116">Calculates the point and tangent vector at the specified distance along the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="d2ef3-117">範例</span><span class="sxs-lookup"><span data-stu-id="d2ef3-117">Examples</span></span>

<span data-ttu-id="d2ef3-118">下列程式碼範例示範如何使用 **ComputePointAtLength** ，在幾何的指定距離計算點和正切向量。</span><span class="sxs-lookup"><span data-stu-id="d2ef3-118">The following code example shows how to use **ComputePointAtLength** to calculate the point and tangent vector at the specified distance along the geometry.</span></span>


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;
```




```C++
// Ask the geometry to give us the point that corresponds with the
// length at the current time.
hr = m_pPathGeometry->ComputePointAtLength(
    length, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="requirements"></a><span data-ttu-id="d2ef3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2ef3-119">Requirements</span></span>



| <span data-ttu-id="d2ef3-120">需求</span><span class="sxs-lookup"><span data-stu-id="d2ef3-120">Requirement</span></span> | <span data-ttu-id="d2ef3-121">值</span><span class="sxs-lookup"><span data-stu-id="d2ef3-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ef3-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2ef3-122">Library</span></span><br/> | <dl> <span data-ttu-id="d2ef3-123"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2ef3-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="d2ef3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d2ef3-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="d2ef3-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2ef3-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2ef3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2ef3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ef3-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="d2ef3-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

