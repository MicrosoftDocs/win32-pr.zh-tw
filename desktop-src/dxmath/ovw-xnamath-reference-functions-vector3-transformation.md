---
title: DirectXMath 3D 向量轉換函式
description: 列出3D 向量轉換函式。
ms.assetid: 148972da-e460-63b9-6b01-10201f63d157
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a592071970d69d7ef4b4db42960335c5fc771ac3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996642"
---
# <a name="directxmath-3d-vector-transformation-functions"></a><span data-ttu-id="134f5-103">DirectXMath 3D 向量轉換函式</span><span class="sxs-lookup"><span data-stu-id="134f5-103">DirectXMath 3D vector transformation functions</span></span>

<span data-ttu-id="134f5-104">列出3D 向量轉換函式。</span><span class="sxs-lookup"><span data-stu-id="134f5-104">Lists the 3D vector transformation functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="134f5-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="134f5-105">In this section</span></span>



| <span data-ttu-id="134f5-106">主題</span><span class="sxs-lookup"><span data-stu-id="134f5-106">Topic</span></span>                                                                               | <span data-ttu-id="134f5-107">描述</span><span class="sxs-lookup"><span data-stu-id="134f5-107">Description</span></span>                                                                                                                                      |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="134f5-108">**XMVector3InverseRotate**</span><span class="sxs-lookup"><span data-stu-id="134f5-108">**XMVector3InverseRotate**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3inverserotate)<br/>                 | <span data-ttu-id="134f5-109">使用四元數的反向旋轉3D 向量。</span><span class="sxs-lookup"><span data-stu-id="134f5-109">Rotates a 3D vector using the inverse of a quaternion.</span></span><br/>                                                                                |
| [<span data-ttu-id="134f5-110">**XMVector3Project**</span><span class="sxs-lookup"><span data-stu-id="134f5-110">**XMVector3Project**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3project)<br/>                             | <span data-ttu-id="134f5-111">將物件空間中的3D 向量投影至螢幕空間。</span><span class="sxs-lookup"><span data-stu-id="134f5-111">Project a 3D vector from object space into screen space.</span></span><br/>                                                                              |
| [<span data-ttu-id="134f5-112">**XMVector3ProjectStream**</span><span class="sxs-lookup"><span data-stu-id="134f5-112">**XMVector3ProjectStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3projectstream)<br/>                 | <span data-ttu-id="134f5-113">將3D 向量的資料流程從物件空間投射到螢幕空間。</span><span class="sxs-lookup"><span data-stu-id="134f5-113">Projects a stream of 3D vectors from object space into screen space.</span></span><br/>                                                                  |
| [<span data-ttu-id="134f5-114">**XMVector3Rotate**</span><span class="sxs-lookup"><span data-stu-id="134f5-114">**XMVector3Rotate**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3rotate)<br/>                               | <span data-ttu-id="134f5-115">使用四元數旋轉3D 向量。</span><span class="sxs-lookup"><span data-stu-id="134f5-115">Rotates a 3D vector using a quaternion.</span></span><br/>                                                                                               |
| [<span data-ttu-id="134f5-116">**XMVector3Transform**</span><span class="sxs-lookup"><span data-stu-id="134f5-116">**XMVector3Transform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transform)<br/>                         | <span data-ttu-id="134f5-117">依矩陣轉換3D 向量。</span><span class="sxs-lookup"><span data-stu-id="134f5-117">Transforms a 3D vector by a matrix.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="134f5-118">**XMVector3TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="134f5-118">**XMVector3TransformCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoord)<br/>               | <span data-ttu-id="134f5-119">依指定的矩陣轉換3D 向量，將結果投射回 w = 1。</span><span class="sxs-lookup"><span data-stu-id="134f5-119">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span><br/>                                                      |
| [<span data-ttu-id="134f5-120">**XMVector3TransformCoordStream**</span><span class="sxs-lookup"><span data-stu-id="134f5-120">**XMVector3TransformCoordStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoordstream)<br/>   | <span data-ttu-id="134f5-121">依指定的矩陣轉換3D 向量的資料流程，投射產生的向量，使其 w 座標等於1.0。</span><span class="sxs-lookup"><span data-stu-id="134f5-121">Transforms a stream of 3D vectors by a given matrix, projecting the resulting vectors such that their w coordinates are equal to 1.0.</span></span><br/> |
| [<span data-ttu-id="134f5-122">**XMVector3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="134f5-122">**XMVector3TransformNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormal)<br/>             | <span data-ttu-id="134f5-123">依指定的矩陣轉換一般的3D 向量。</span><span class="sxs-lookup"><span data-stu-id="134f5-123">Transforms the 3D vector normal by the given matrix.</span></span><br/>                                                                                  |
| [<span data-ttu-id="134f5-124">**XMVector3TransformNormalStream**</span><span class="sxs-lookup"><span data-stu-id="134f5-124">**XMVector3TransformNormalStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormalstream)<br/> | <span data-ttu-id="134f5-125">依指定的矩陣轉換3D 一般向量的資料流程。</span><span class="sxs-lookup"><span data-stu-id="134f5-125">Transforms a stream of 3D normal vectors by a given matrix.</span></span><br/>                                                                           |
| [<span data-ttu-id="134f5-126">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="134f5-126">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)<br/>             | <span data-ttu-id="134f5-127">依指定的矩陣轉換3D 向量的資料流程。</span><span class="sxs-lookup"><span data-stu-id="134f5-127">Transforms a stream of 3D vectors by a given matrix.</span></span><br/>                                                                                  |
| [<span data-ttu-id="134f5-128">**XMVector3Unproject**</span><span class="sxs-lookup"><span data-stu-id="134f5-128">**XMVector3Unproject**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3unproject)<br/>                         | <span data-ttu-id="134f5-129">從螢幕空間將3D 向量投射到物件空間。</span><span class="sxs-lookup"><span data-stu-id="134f5-129">Projects a 3D vector from screen space into object space.</span></span><br/>                                                                             |
| [<span data-ttu-id="134f5-130">**XMVector3UnprojectStream**</span><span class="sxs-lookup"><span data-stu-id="134f5-130">**XMVector3UnprojectStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3unprojectstream)<br/>             | <span data-ttu-id="134f5-131">將3D 向量的資料流程從螢幕空間轉換成物件空間。</span><span class="sxs-lookup"><span data-stu-id="134f5-131">Transforms a stream of 3D vectors from screen space to object space.</span></span><br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="134f5-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="134f5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="134f5-133">DirectXMath 程式庫3D 向量函數</span><span class="sxs-lookup"><span data-stu-id="134f5-133">DirectXMath Library 3D Vector Functions</span></span>](ovw-xnamath-reference-functions-vector3.md)
</dt> </dl>

 

 
