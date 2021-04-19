---
description: 繞著任意軸的 (相對於全局座標空間) 旋轉。
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: 'ID3DXMATRIXStack：： RotateYawPitchRoll 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5020cb6ff3af41b9ef32ef77bb71607f6cd5ea6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000225"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a><span data-ttu-id="2e34b-103">ID3DXMATRIXStack：： RotateYawPitchRoll 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="2e34b-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3dx9math.h)</span></span>

<span data-ttu-id="2e34b-104">繞著任意軸的 (相對於全局座標空間) 旋轉。</span><span class="sxs-lookup"><span data-stu-id="2e34b-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e34b-105">語法</span><span class="sxs-lookup"><span data-stu-id="2e34b-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="2e34b-106">參數</span><span class="sxs-lookup"><span data-stu-id="2e34b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e34b-107">*偏擺* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e34b-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e34b-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e34b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e34b-109">以弧度為單位的 y 軸偏擺。</span><span class="sxs-lookup"><span data-stu-id="2e34b-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2e34b-110">*推銷* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e34b-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e34b-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e34b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e34b-112">以弧度為單位的 X 軸左右間距。</span><span class="sxs-lookup"><span data-stu-id="2e34b-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2e34b-113">*滾動* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e34b-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e34b-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e34b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e34b-115">以弧度為單位的 Z 軸左右滾動。</span><span class="sxs-lookup"><span data-stu-id="2e34b-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e34b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e34b-116">Return value</span></span>

<span data-ttu-id="2e34b-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e34b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e34b-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2e34b-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e34b-119">備註</span><span class="sxs-lookup"><span data-stu-id="2e34b-119">Remarks</span></span>

<span data-ttu-id="2e34b-120">這個方法會使用計算的旋轉矩陣，將旋轉加入矩陣堆疊中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2e34b-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="2e34b-121">由於旋轉會靠右乘以矩陣堆疊，所以旋轉是相對於全球座標空間。</span><span class="sxs-lookup"><span data-stu-id="2e34b-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e34b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e34b-122">Requirements</span></span>



| <span data-ttu-id="2e34b-123">需求</span><span class="sxs-lookup"><span data-stu-id="2e34b-123">Requirement</span></span> | <span data-ttu-id="2e34b-124">值</span><span class="sxs-lookup"><span data-stu-id="2e34b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e34b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2e34b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2e34b-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e34b-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2e34b-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="2e34b-127">Library</span></span><br/> | <dl> <span data-ttu-id="2e34b-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e34b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e34b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e34b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e34b-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="2e34b-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2e34b-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="2e34b-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="2e34b-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="2e34b-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="2e34b-133">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="2e34b-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="2e34b-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="2e34b-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
