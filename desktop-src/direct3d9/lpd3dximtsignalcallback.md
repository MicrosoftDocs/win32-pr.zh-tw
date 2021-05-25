---
description: D3DXComputeIMTFromSignal 用來描述輸入網格 u、v 空間中使用者定義信號的函式原型。 函式會在提供的 u、v 座標上評估維度 uSignalDimension 的程式性信號。
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342833"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="d81d7-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="d81d7-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="d81d7-105">[**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)用來描述輸入網格 u、v 空間中使用者定義信號的函式原型。</span><span class="sxs-lookup"><span data-stu-id="d81d7-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="d81d7-106">函式會在提供的 u、v 座標上評估維度 uSignalDimension 的程式性信號。</span><span class="sxs-lookup"><span data-stu-id="d81d7-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="d81d7-107">語法</span><span class="sxs-lookup"><span data-stu-id="d81d7-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="d81d7-108">參數</span><span class="sxs-lookup"><span data-stu-id="d81d7-108">Parameters</span></span>

<span data-ttu-id="d81d7-109">\[在 \] uv-包含頂點材質座標的向量指標。</span><span class="sxs-lookup"><span data-stu-id="d81d7-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="d81d7-110">\[在 \] uPrimitiveId 中-應計算其信號之網格上的輸入三角形索引。</span><span class="sxs-lookup"><span data-stu-id="d81d7-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="d81d7-111">\[在 \] uSignalDimension 中-要儲存在信號資料陣列中的浮點數 (pfSignalOut) 。</span><span class="sxs-lookup"><span data-stu-id="d81d7-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="d81d7-112">\[在 \] pUserData 中-傳遞至 [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md)的 pUserData 指標。</span><span class="sxs-lookup"><span data-stu-id="d81d7-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="d81d7-113">\[out \] pfSignalOut-浮點數的陣列，其中包含信號資料。</span><span class="sxs-lookup"><span data-stu-id="d81d7-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="d81d7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d81d7-114">Return Value</span></span>

<span data-ttu-id="d81d7-115">必須實作為此函式，才能傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d81d7-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d81d7-116">備註</span><span class="sxs-lookup"><span data-stu-id="d81d7-116">Remarks</span></span>

<span data-ttu-id="d81d7-117">宣告回呼函數時，請務必指定 [**Windows 資料類型**](../winprog/windows-data-types.md) 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="d81d7-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="d81d7-118">否則，可能會發生堆疊溢位。</span><span class="sxs-lookup"><span data-stu-id="d81d7-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="d81d7-119">需求</span><span class="sxs-lookup"><span data-stu-id="d81d7-119">Requirement</span></span>               | <span data-ttu-id="d81d7-120">值</span><span class="sxs-lookup"><span data-stu-id="d81d7-120">Value</span></span>            |
|----------------|-------------|
| <span data-ttu-id="d81d7-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d81d7-121">Header</span></span>         | <span data-ttu-id="d81d7-122">d3dx9mesh。h</span><span class="sxs-lookup"><span data-stu-id="d81d7-122">d3dx9mesh.h</span></span> |
| <span data-ttu-id="d81d7-123">匯入程式庫</span><span class="sxs-lookup"><span data-stu-id="d81d7-123">Import Library</span></span> | <span data-ttu-id="d81d7-124">d3dx9 .lib</span><span class="sxs-lookup"><span data-stu-id="d81d7-124">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="d81d7-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="d81d7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d81d7-126">回呼函式</span><span class="sxs-lookup"><span data-stu-id="d81d7-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
