---
title: ID2D1Geometry ComputeArea 方法
description: 計算幾何的區域。
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- ComputeArea 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997750"
---
# <a name="id2d1geometrycomputearea-methods"></a><span data-ttu-id="87d2a-104">ID2D1Geometry：： ComputeArea 方法</span><span class="sxs-lookup"><span data-stu-id="87d2a-104">ID2D1Geometry::ComputeArea methods</span></span>

<span data-ttu-id="87d2a-105">計算幾何的區域。</span><span class="sxs-lookup"><span data-stu-id="87d2a-105">Computes the area of the geometry.</span></span>

### <a name="overload-list"></a><span data-ttu-id="87d2a-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="87d2a-106">Overload list</span></span>



| <span data-ttu-id="87d2a-107">方法</span><span class="sxs-lookup"><span data-stu-id="87d2a-107">Method</span></span>                                                                                                                      | <span data-ttu-id="87d2a-108">描述</span><span class="sxs-lookup"><span data-stu-id="87d2a-108">Description</span></span>                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87d2a-109">[**ComputeArea (D2D1 \_ 矩陣 \_ 3X2 \_ F&，FLOAT \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span><span class="sxs-lookup"><span data-stu-id="87d2a-109">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span></span>              | <span data-ttu-id="87d2a-110">當指定的矩陣轉換之後，並使用預設容錯壓平合併時，計算幾何的區域。</span><span class="sxs-lookup"><span data-stu-id="87d2a-110">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the default tolerance.</span></span><br/>    |
| <span data-ttu-id="87d2a-111">[**ComputeArea (D2D1 \_ 矩陣 \_ 3X2 \_ F \* ，FLOAT \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="87d2a-111">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span>             | <span data-ttu-id="87d2a-112">使用預設容錯值，在指定的矩陣轉換並壓平合併之後，計算幾何的區域。</span><span class="sxs-lookup"><span data-stu-id="87d2a-112">Computes the area of the geometry after it has been transformed by the specified matrix and flattened by using the default tolerance.</span></span><br/> |
| <span data-ttu-id="87d2a-113">[**ComputeArea (D2D1 \_ 矩陣 \_ 3X2 \_ F&，float，float \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span><span class="sxs-lookup"><span data-stu-id="87d2a-113">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span></span>  | <span data-ttu-id="87d2a-114">當指定的矩陣轉換之後，以及使用指定的容錯壓平合併時，計算幾何的區域。</span><span class="sxs-lookup"><span data-stu-id="87d2a-114">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |
| <span data-ttu-id="87d2a-115">[**ComputeArea (D2D1 \_ 矩陣 \_ 3X2 \_ F \* ，float，float \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="87d2a-115">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span> | <span data-ttu-id="87d2a-116">當指定的矩陣轉換之後，以及使用指定的容錯壓平合併時，計算幾何的區域。</span><span class="sxs-lookup"><span data-stu-id="87d2a-116">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="87d2a-117">範例</span><span class="sxs-lookup"><span data-stu-id="87d2a-117">Examples</span></span>

<span data-ttu-id="87d2a-118">下列程式碼範例會使用 **ComputeArea** 來計算指定之圓形的區域 (**m \_ pCircleGeometry1**) 。</span><span class="sxs-lookup"><span data-stu-id="87d2a-118">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



## <a name="requirements"></a><span data-ttu-id="87d2a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="87d2a-119">Requirements</span></span>



| <span data-ttu-id="87d2a-120">需求</span><span class="sxs-lookup"><span data-stu-id="87d2a-120">Requirement</span></span> | <span data-ttu-id="87d2a-121">值</span><span class="sxs-lookup"><span data-stu-id="87d2a-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="87d2a-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="87d2a-122">Library</span></span><br/> | <dl> <span data-ttu-id="87d2a-123"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="87d2a-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="87d2a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="87d2a-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="87d2a-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87d2a-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87d2a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="87d2a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d2a-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="87d2a-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

