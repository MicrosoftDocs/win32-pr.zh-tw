---
description: 材質 fill 函式所使用的 LPD3DXFILL2D 函數類型。
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c341ccfcbcc566d65e7139813c676e2286e25cf
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342843"
---
# <a name="lpd3dxfill2d"></a><span data-ttu-id="d2eb5-103">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="d2eb5-103">LPD3DXFILL2D</span></span>

<span data-ttu-id="d2eb5-104">紋理填滿函數使用的函式類型。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2eb5-105">語法</span><span class="sxs-lookup"><span data-stu-id="d2eb5-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="d2eb5-106">參數</span><span class="sxs-lookup"><span data-stu-id="d2eb5-106">Parameters</span></span>

<span data-ttu-id="d2eb5-107">不悅-函數用來傳回結果的向量指標。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="d2eb5-108">X、Y、Z 和 W 會分別對應至 R、G、B 和 A。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="d2eb5-109">pTexCoord-向量的指標，其中包含目前正在評估之材質的座標。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="d2eb5-110">材質和音量紋理的材質座標元件範圍從0到1。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="d2eb5-111">Cube 紋理的材質座標元件範圍從-1 到1。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="d2eb5-112">pTexelSize-包含目前材質之維度的向量指標。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="d2eb5-113">.Pdata-使用者資料的指標。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2eb5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2eb5-114">Return Value</span></span>

<span data-ttu-id="d2eb5-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2eb5-116">備註</span><span class="sxs-lookup"><span data-stu-id="d2eb5-116">Remarks</span></span>

<span data-ttu-id="d2eb5-117">宣告回呼函數時，請務必指定 [**Windows 資料類型**](../winprog/windows-data-types.md) 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="d2eb5-118">否則，可能會發生堆疊溢位。</span><span class="sxs-lookup"><span data-stu-id="d2eb5-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="d2eb5-119">需求</span><span class="sxs-lookup"><span data-stu-id="d2eb5-119">Requirement</span></span>                         | <span data-ttu-id="d2eb5-120">值</span><span class="sxs-lookup"><span data-stu-id="d2eb5-120">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="d2eb5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d2eb5-121">Header</span></span>                   | <span data-ttu-id="d2eb5-122">d3dx9tex。h</span><span class="sxs-lookup"><span data-stu-id="d2eb5-122">d3dx9tex.h</span></span> |
| <span data-ttu-id="d2eb5-123">匯入程式庫</span><span class="sxs-lookup"><span data-stu-id="d2eb5-123">Import Library</span></span>           | <span data-ttu-id="d2eb5-124">d3dx9 .lib</span><span class="sxs-lookup"><span data-stu-id="d2eb5-124">d3dx9.lib</span></span>  |
| <span data-ttu-id="d2eb5-125">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="d2eb5-125">Minimum Operating System</span></span> | <span data-ttu-id="d2eb5-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d2eb5-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d2eb5-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2eb5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2eb5-128">回呼函式</span><span class="sxs-lookup"><span data-stu-id="d2eb5-128">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="d2eb5-129">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="d2eb5-129">LPD3DXFILL3D</span></span>](lpd3dxfill3d.md)
</dt> </dl>

 

 
