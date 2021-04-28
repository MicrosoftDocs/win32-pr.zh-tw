---
description: 材質 fill 函式所使用的 LPD3DXFILL3D 函數類型。
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c711459cffa3430b31ba7c91d77cc9519e6a43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114306"
---
# <a name="lpd3dxfill3d"></a><span data-ttu-id="e9e55-103">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="e9e55-103">LPD3DXFILL3D</span></span>

<span data-ttu-id="e9e55-104">紋理填滿函數使用的函式類型。</span><span class="sxs-lookup"><span data-stu-id="e9e55-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e55-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9e55-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="e9e55-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9e55-106">Parameters</span></span>

<span data-ttu-id="e9e55-107">不悅-函數用來傳回結果的向量指標。</span><span class="sxs-lookup"><span data-stu-id="e9e55-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="e9e55-108">X、Y、Z 和 W 會分別對應至 R、G、B 和 A。</span><span class="sxs-lookup"><span data-stu-id="e9e55-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="e9e55-109">pTexCoord-向量的指標，其中包含目前正在評估之材質的座標。</span><span class="sxs-lookup"><span data-stu-id="e9e55-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="e9e55-110">材質和音量紋理的材質座標元件範圍從0到1。</span><span class="sxs-lookup"><span data-stu-id="e9e55-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="e9e55-111">Cube 紋理的材質座標元件範圍從-1 到1。</span><span class="sxs-lookup"><span data-stu-id="e9e55-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="e9e55-112">pTexelSize-包含目前材質之維度的向量指標。</span><span class="sxs-lookup"><span data-stu-id="e9e55-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="e9e55-113">.Pdata-使用者資料的指標。</span><span class="sxs-lookup"><span data-stu-id="e9e55-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9e55-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9e55-114">Return Value</span></span>

<span data-ttu-id="e9e55-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e9e55-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9e55-116">備註</span><span class="sxs-lookup"><span data-stu-id="e9e55-116">Remarks</span></span>

<span data-ttu-id="e9e55-117">宣告回呼函數時，請務必指定 [**Windows 資料類型**](../winprog/windows-data-types.md) 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="e9e55-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="e9e55-118">否則，可能會發生堆疊溢位。</span><span class="sxs-lookup"><span data-stu-id="e9e55-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="e9e55-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e9e55-119">Header</span></span>                   | <span data-ttu-id="e9e55-120">d3dx9tex。h</span><span class="sxs-lookup"><span data-stu-id="e9e55-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="e9e55-121">匯入程式庫</span><span class="sxs-lookup"><span data-stu-id="e9e55-121">Import Library</span></span>           | <span data-ttu-id="e9e55-122">d3dx9 .lib</span><span class="sxs-lookup"><span data-stu-id="e9e55-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="e9e55-123">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="e9e55-123">Minimum Operating System</span></span> | <span data-ttu-id="e9e55-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e9e55-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e9e55-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9e55-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9e55-126">回呼函式</span><span class="sxs-lookup"><span data-stu-id="e9e55-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="e9e55-127">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="e9e55-127">LPD3DXFILL2D</span></span>](lpd3dxfill2d.md)
</dt> </dl>

 

 
