---
title: ID2D1Geometry 加寬方法
description: 依指定的筆觸擴大幾何，並將結果寫入至 ID2D1SimplifiedGeometrySink。
ms.assetid: c951ab85-7980-41e3-95c4-291d2fb046c8
keywords:
- 擴大方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 73a1ce3f90192f49a719a92d80f448694ce43235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000875"
---
# <a name="id2d1geometrywiden-methods"></a><span data-ttu-id="8c207-104">ID2D1Geometry：：加寬方法</span><span class="sxs-lookup"><span data-stu-id="8c207-104">ID2D1Geometry::Widen methods</span></span>

<span data-ttu-id="8c207-105">依指定的筆觸擴大幾何，並將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)。</span><span class="sxs-lookup"><span data-stu-id="8c207-105">Widens the geometry by the specified stroke and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span>

### <a name="overload-list"></a><span data-ttu-id="8c207-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="8c207-106">Overload list</span></span>



| <span data-ttu-id="8c207-107">方法</span><span class="sxs-lookup"><span data-stu-id="8c207-107">Method</span></span>                                                                                                                                                                                                          | <span data-ttu-id="8c207-108">描述</span><span class="sxs-lookup"><span data-stu-id="8c207-108">Description</span></span>                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c207-109">[**加寬 (FLOAT、ID2D1StrokeStyle \* 、D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))</span><span class="sxs-lookup"><span data-stu-id="8c207-109">[**Widen(FLOAT,ID2D1StrokeStyle\*,D2D1\_MATRIX\_3X2\_F\*,ID2D1SimplifiedGeometrySink\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))</span></span>             | <span data-ttu-id="8c207-110">依指定的筆觸擴大幾何，並在指定的矩陣轉換結果之後，將結果寫入 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ，並使用預設的容錯值壓平合併。</span><span class="sxs-lookup"><span data-stu-id="8c207-110">Widens the geometry by the specified stroke and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) after it has been transformed by the specified matrix and flattened using the default tolerance.</span></span><br/>   |
| <span data-ttu-id="8c207-111">[**加寬 (FLOAT、ID2D1StrokeStyle \* 、D2D1 \_ 矩陣 \_ 3X2 \_ F&、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))</span><span class="sxs-lookup"><span data-stu-id="8c207-111">[**Widen(FLOAT,ID2D1StrokeStyle\*,D2D1\_MATRIX\_3X2\_F&,ID2D1SimplifiedGeometrySink\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))</span></span>              | <span data-ttu-id="8c207-112">依指定的筆觸擴大幾何，並在指定的矩陣轉換結果之後，將結果寫入 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ，並使用預設的容錯值壓平合併。</span><span class="sxs-lookup"><span data-stu-id="8c207-112">Widens the geometry by the specified stroke and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) after it has been transformed by the specified matrix and flattened using the default tolerance.</span></span><br/>   |
| <span data-ttu-id="8c207-113">[**加寬 (FLOAT、ID2D1StrokeStyle \* 、D2D1 \_ 矩陣 \_ 3X2 \_ F \* 、FLOAT、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink))</span><span class="sxs-lookup"><span data-stu-id="8c207-113">[**Widen(FLOAT,ID2D1StrokeStyle\*,D2D1\_MATRIX\_3X2\_F\*,FLOAT,ID2D1SimplifiedGeometrySink\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink))</span></span> | <span data-ttu-id="8c207-114">依指定的筆觸擴大幾何，並在指定的矩陣轉換結果之後，將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ，並使用指定的容忍度壓平合併。</span><span class="sxs-lookup"><span data-stu-id="8c207-114">Widens the geometry by the specified stroke and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/> |
| <span data-ttu-id="8c207-115">[**加寬 (FLOAT、ID2D1StrokeStyle \* 、D2D1 \_ 矩陣 \_ 3X2 \_ F&、FLOAT、ID2D1SimplifiedGeometrySink \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))</span><span class="sxs-lookup"><span data-stu-id="8c207-115">[**Widen(FLOAT,ID2D1StrokeStyle\*,D2D1\_MATRIX\_3X2\_F&,FLOAT,ID2D1SimplifiedGeometrySink\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-widen(float_id2d1strokestyle_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))</span></span>  | <span data-ttu-id="8c207-116">依指定的筆觸擴大幾何，並在指定的矩陣轉換結果之後，將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) ，並使用指定的容忍度壓平合併。</span><span class="sxs-lookup"><span data-stu-id="8c207-116">Widens the geometry by the specified stroke and writes the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="8c207-117">範例</span><span class="sxs-lookup"><span data-stu-id="8c207-117">Examples</span></span>

<span data-ttu-id="8c207-118">下列程式碼範例示範如何使用 **加寬** 依指定的筆觸來加寬幾何，然後將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) 物件。</span><span class="sxs-lookup"><span data-stu-id="8c207-118">The following code example shows how to use **Widen** to widen the geometry by the specified stroke and then write the result to an [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) object.</span></span>


```C++
 ID2D1GeometrySink *pGeometrySink = NULL;
 hr = pPathGeometry->Open(&pGeometrySink);
 if (SUCCEEDED(hr))
 {
     hr = pGeometry->Widen(
             strokeWidth,
             pIStrokeStyle,
             pWorldTransform,
             pGeometrySink
             );

     if (SUCCEEDED(hr))
     {
         hr = pGeometrySink->Close();
         if (SUCCEEDED(hr))
         {
             ID2D1Mesh *pMesh = NULL;
             hr = m_pRT->CreateMesh(&pMesh);
             if (SUCCEEDED(hr))
             {
                 ID2D1TessellationSink *pSink = NULL;
                 hr = pMesh->Open(&pSink);
                 if (SUCCEEDED(hr))
                 {
                     hr = pPathGeometry->Tessellate(
                             NULL, // world transform (already handled in Widen)
                             pSink
                             );
                     if (SUCCEEDED(hr))
                     {
                         hr = pSink->Close();
                         if (SUCCEEDED(hr))
                         {
                             SafeReplace(&m_pStrokeMesh, pMesh);
                         }
                     }
                     pSink->Release();
                 }
                 pMesh->Release();
             }
         }
     }
     pGeometrySink->Release();
 }
 pPathGeometry->Release();
```



## <a name="requirements"></a><span data-ttu-id="8c207-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c207-119">Requirements</span></span>



| <span data-ttu-id="8c207-120">需求</span><span class="sxs-lookup"><span data-stu-id="8c207-120">Requirement</span></span> | <span data-ttu-id="8c207-121">值</span><span class="sxs-lookup"><span data-stu-id="8c207-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c207-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c207-122">Library</span></span><br/> | <dl> <span data-ttu-id="8c207-123"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c207-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c207-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8c207-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="8c207-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c207-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c207-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c207-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c207-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="8c207-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

