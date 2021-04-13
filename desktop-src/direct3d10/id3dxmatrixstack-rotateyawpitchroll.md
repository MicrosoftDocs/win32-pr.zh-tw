---
description: 繞著任意軸的 (相對於全局座標空間) 旋轉。
ms.assetid: 35e237f6-40f2-4001-adb0-f489d61f64e7
title: 'ID3DXMATRIXStack：： RotateYawPitchRoll 方法 (D3DX10 .h) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8d57af31e9944c718419a3a90863c9960d0bdb36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323375"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx10h"></a><span data-ttu-id="19cd7-103">ID3DXMATRIXStack：： RotateYawPitchRoll 方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="19cd7-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3DX10.h)</span></span>

<span data-ttu-id="19cd7-104">繞著任意軸的 (相對於全局座標空間) 旋轉。</span><span class="sxs-lookup"><span data-stu-id="19cd7-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="19cd7-105">語法</span><span class="sxs-lookup"><span data-stu-id="19cd7-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="19cd7-106">參數</span><span class="sxs-lookup"><span data-stu-id="19cd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19cd7-107">*偏擺* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19cd7-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cd7-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19cd7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19cd7-109">以弧度為單位的 y 軸偏擺。</span><span class="sxs-lookup"><span data-stu-id="19cd7-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="19cd7-110">*推銷* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19cd7-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cd7-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19cd7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19cd7-112">以弧度為單位的 X 軸左右間距。</span><span class="sxs-lookup"><span data-stu-id="19cd7-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="19cd7-113">*滾動* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19cd7-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cd7-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19cd7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19cd7-115">以弧度為單位的 Z 軸左右滾動。</span><span class="sxs-lookup"><span data-stu-id="19cd7-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19cd7-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="19cd7-116">Return value</span></span>

<span data-ttu-id="19cd7-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19cd7-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19cd7-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="19cd7-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="19cd7-119">備註</span><span class="sxs-lookup"><span data-stu-id="19cd7-119">Remarks</span></span>

<span data-ttu-id="19cd7-120">這個方法會使用計算的旋轉矩陣，將旋轉加入矩陣堆疊中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="19cd7-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="19cd7-121">由於旋轉會靠右乘以矩陣堆疊，所以旋轉是相對於全球座標空間。</span><span class="sxs-lookup"><span data-stu-id="19cd7-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="19cd7-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="19cd7-122">Requirements</span></span>



| <span data-ttu-id="19cd7-123">需求</span><span class="sxs-lookup"><span data-stu-id="19cd7-123">Requirement</span></span> | <span data-ttu-id="19cd7-124">值</span><span class="sxs-lookup"><span data-stu-id="19cd7-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19cd7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="19cd7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="19cd7-126"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="19cd7-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="19cd7-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="19cd7-127">Library</span></span><br/> | <dl> <span data-ttu-id="19cd7-128"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="19cd7-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19cd7-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19cd7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19cd7-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="19cd7-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="19cd7-131">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="19cd7-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
