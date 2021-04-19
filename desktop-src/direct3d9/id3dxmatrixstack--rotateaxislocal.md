---
description: 在任意軸周圍) 旋轉 (相對於物件的區域座標空間。
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: 'ID3DXMATRIXStack：： RotateAxisLocal 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8488f6314eb926495baa2e42df9ea01616131507
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981817"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a><span data-ttu-id="86b68-103">ID3DXMATRIXStack：： RotateAxisLocal 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="86b68-103">ID3DXMATRIXStack::RotateAxisLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="86b68-104">在任意軸周圍) 旋轉 (相對於物件的區域座標空間。</span><span class="sxs-lookup"><span data-stu-id="86b68-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="86b68-105">語法</span><span class="sxs-lookup"><span data-stu-id="86b68-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="86b68-106">參數</span><span class="sxs-lookup"><span data-stu-id="86b68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86b68-107">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86b68-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86b68-108">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="86b68-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="86b68-109">任意旋轉軸的指標。</span><span class="sxs-lookup"><span data-stu-id="86b68-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="86b68-110">請參閱 [**D3DXVECTOR3**](d3dxvector3.md)。</span><span class="sxs-lookup"><span data-stu-id="86b68-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="86b68-111">*角度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="86b68-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86b68-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86b68-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="86b68-113">任意軸的旋轉角度（以弧度為單位）。</span><span class="sxs-lookup"><span data-stu-id="86b68-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="86b68-114">朝原點查看任意軸時，會以逆時針測量角度。</span><span class="sxs-lookup"><span data-stu-id="86b68-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86b68-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="86b68-115">Return value</span></span>

<span data-ttu-id="86b68-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86b68-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86b68-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="86b68-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="86b68-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="86b68-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="86b68-119">備註</span><span class="sxs-lookup"><span data-stu-id="86b68-119">Remarks</span></span>

<span data-ttu-id="86b68-120">這個方法會使用計算的旋轉矩陣，將旋轉加入矩陣堆疊中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="86b68-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="86b68-121">由於旋轉會靠左乘以矩陣堆疊，所以旋轉是相對於物件的本機座標空間。</span><span class="sxs-lookup"><span data-stu-id="86b68-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="86b68-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="86b68-122">Requirements</span></span>



| <span data-ttu-id="86b68-123">需求</span><span class="sxs-lookup"><span data-stu-id="86b68-123">Requirement</span></span> | <span data-ttu-id="86b68-124">值</span><span class="sxs-lookup"><span data-stu-id="86b68-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86b68-125">標頭</span><span class="sxs-lookup"><span data-stu-id="86b68-125">Header</span></span><br/>  | <dl> <span data-ttu-id="86b68-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="86b68-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="86b68-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="86b68-127">Library</span></span><br/> | <dl> <span data-ttu-id="86b68-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="86b68-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="86b68-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86b68-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b68-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="86b68-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="86b68-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="86b68-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="86b68-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="86b68-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="86b68-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="86b68-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="86b68-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="86b68-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
