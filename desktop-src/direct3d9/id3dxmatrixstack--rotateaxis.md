---
description: ID3DXMATRIXStack：： RotateAxis 方法 (D3dx9math .h) -在任意軸的周圍旋轉 (相對於全球座標空間) 。
ms.assetid: b7ae5195-a2af-429f-9a0d-51cd7e955362
title: 'ID3DXMATRIXStack：： RotateAxis 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ea62b65bca73eb3fe7b2cd962e1afd9b35d53bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093486"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx9mathh"></a><span data-ttu-id="0ab11-103">ID3DXMATRIXStack：： RotateAxis 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="0ab11-103">ID3DXMATRIXStack::RotateAxis method (D3dx9math.h)</span></span>

<span data-ttu-id="0ab11-104">繞著任意軸的 (相對於全局座標空間) 旋轉。</span><span class="sxs-lookup"><span data-stu-id="0ab11-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ab11-105">語法</span><span class="sxs-lookup"><span data-stu-id="0ab11-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="0ab11-106">參數</span><span class="sxs-lookup"><span data-stu-id="0ab11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ab11-107">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ab11-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab11-108">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0ab11-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0ab11-109">任意旋轉軸的指標。</span><span class="sxs-lookup"><span data-stu-id="0ab11-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="0ab11-110">請參閱 [**D3DXVECTOR3**](d3dxvector3.md)。</span><span class="sxs-lookup"><span data-stu-id="0ab11-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ab11-111">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ab11-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab11-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ab11-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ab11-113">任意軸的旋轉角度（以弧度為單位）。</span><span class="sxs-lookup"><span data-stu-id="0ab11-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="0ab11-114">朝原點查看任意軸時，會以逆時針測量角度。</span><span class="sxs-lookup"><span data-stu-id="0ab11-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ab11-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ab11-115">Return value</span></span>

<span data-ttu-id="0ab11-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ab11-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ab11-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0ab11-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ab11-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="0ab11-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ab11-119">備註</span><span class="sxs-lookup"><span data-stu-id="0ab11-119">Remarks</span></span>

<span data-ttu-id="0ab11-120">這個方法會使用計算的旋轉矩陣，將旋轉加入矩陣堆疊中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0ab11-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="0ab11-121">由於旋轉會靠右乘以矩陣堆疊，所以旋轉是相對於全球座標空間。</span><span class="sxs-lookup"><span data-stu-id="0ab11-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ab11-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ab11-122">Requirements</span></span>



| <span data-ttu-id="0ab11-123">需求</span><span class="sxs-lookup"><span data-stu-id="0ab11-123">Requirement</span></span> | <span data-ttu-id="0ab11-124">值</span><span class="sxs-lookup"><span data-stu-id="0ab11-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab11-125">標頭</span><span class="sxs-lookup"><span data-stu-id="0ab11-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0ab11-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ab11-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0ab11-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="0ab11-127">Library</span></span><br/> | <dl> <span data-ttu-id="0ab11-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ab11-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0ab11-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ab11-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ab11-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="0ab11-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="0ab11-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="0ab11-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="0ab11-132">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="0ab11-132">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="0ab11-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="0ab11-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="0ab11-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="0ab11-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
