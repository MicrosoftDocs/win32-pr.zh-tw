---
description: D3DXComputeIMTFromSignal 用來描述輸入網格 u、v 空間中使用者定義信號的函式原型。 函式會在提供的 u、v 座標上評估維度 uSignalDimension 的程式性信號。
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aebf9250be6fcc878d920816a81782e8ece87ec4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972294"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="087a4-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="087a4-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="087a4-105">[**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)用來描述輸入網格 u、v 空間中使用者定義信號的函式原型。</span><span class="sxs-lookup"><span data-stu-id="087a4-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="087a4-106">函式會在提供的 u、v 座標上評估維度 uSignalDimension 的程式性信號。</span><span class="sxs-lookup"><span data-stu-id="087a4-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="087a4-107">語法</span><span class="sxs-lookup"><span data-stu-id="087a4-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="087a4-108">參數</span><span class="sxs-lookup"><span data-stu-id="087a4-108">Parameters</span></span>

<span data-ttu-id="087a4-109">\[在 \] uv-包含頂點材質座標的向量指標。</span><span class="sxs-lookup"><span data-stu-id="087a4-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="087a4-110">\[在 \] uPrimitiveId 中-應計算其信號之網格上的輸入三角形索引。</span><span class="sxs-lookup"><span data-stu-id="087a4-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="087a4-111">\[在 \] uSignalDimension 中-要儲存在信號資料陣列中的浮點數 (pfSignalOut) 。</span><span class="sxs-lookup"><span data-stu-id="087a4-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="087a4-112">\[在 \] pUserData 中-傳遞至 [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)的 pUserData 指標。</span><span class="sxs-lookup"><span data-stu-id="087a4-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="087a4-113">\[out \] pfSignalOut-浮點數的陣列，其中包含信號資料。</span><span class="sxs-lookup"><span data-stu-id="087a4-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="087a4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="087a4-114">Return Value</span></span>

<span data-ttu-id="087a4-115">必須實作為此函式，才能傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="087a4-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="087a4-116">備註</span><span class="sxs-lookup"><span data-stu-id="087a4-116">Remarks</span></span>

<span data-ttu-id="087a4-117">宣告回呼函數時，請務必指定 [**Windows 資料類型**](../winprog/windows-data-types.md) 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="087a4-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="087a4-118">否則，可能會發生堆疊溢位。</span><span class="sxs-lookup"><span data-stu-id="087a4-118">Otherwise, stack overflows can occur.</span></span>



|                |             |
|----------------|-------------|
| <span data-ttu-id="087a4-119">標頭</span><span class="sxs-lookup"><span data-stu-id="087a4-119">Header</span></span>         | <span data-ttu-id="087a4-120">d3dx9mesh。h</span><span class="sxs-lookup"><span data-stu-id="087a4-120">d3dx9mesh.h</span></span> |
| <span data-ttu-id="087a4-121">匯入程式庫</span><span class="sxs-lookup"><span data-stu-id="087a4-121">Import Library</span></span> | <span data-ttu-id="087a4-122">d3dx9 .lib</span><span class="sxs-lookup"><span data-stu-id="087a4-122">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="087a4-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="087a4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="087a4-124">回呼函式</span><span class="sxs-lookup"><span data-stu-id="087a4-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
