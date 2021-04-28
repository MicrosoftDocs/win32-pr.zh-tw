---
description: ID3DXMATRIXStack：： ScaleLocal 方法 (D3DX10. h) -調整目前有關物件原點的矩陣。
ms.assetid: 748fce3a-a33c-4975-bbf0-dd3167a036f1
title: 'ID3DXMATRIXStack：： ScaleLocal 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3961db0794703e3974dbd92d8eae8293173c2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107776"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx10h"></a><span data-ttu-id="6b011-103">ID3DXMATRIXStack：： ScaleLocal 方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="6b011-103">ID3DXMATRIXStack::ScaleLocal method (D3DX10.h)</span></span>

<span data-ttu-id="6b011-104">調整目前有關物件原點的矩陣。</span><span class="sxs-lookup"><span data-stu-id="6b011-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b011-105">語法</span><span class="sxs-lookup"><span data-stu-id="6b011-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="6b011-106">參數</span><span class="sxs-lookup"><span data-stu-id="6b011-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b011-107">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="6b011-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b011-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b011-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b011-109">X 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="6b011-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="6b011-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b011-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b011-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b011-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b011-112">Y 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="6b011-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="6b011-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b011-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b011-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b011-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b011-115">Z 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="6b011-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b011-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b011-116">Return value</span></span>

<span data-ttu-id="6b011-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b011-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b011-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6b011-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b011-119">備註</span><span class="sxs-lookup"><span data-stu-id="6b011-119">Remarks</span></span>

<span data-ttu-id="6b011-120">這個方法會將目前的矩陣與計算的刻度矩陣相乘。</span><span class="sxs-lookup"><span data-stu-id="6b011-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="6b011-121">轉換是關於物件的本機來源。</span><span class="sxs-lookup"><span data-stu-id="6b011-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="6b011-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b011-122">Requirements</span></span>



| <span data-ttu-id="6b011-123">需求</span><span class="sxs-lookup"><span data-stu-id="6b011-123">Requirement</span></span> | <span data-ttu-id="6b011-124">值</span><span class="sxs-lookup"><span data-stu-id="6b011-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b011-125">標頭</span><span class="sxs-lookup"><span data-stu-id="6b011-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6b011-126"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b011-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b011-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="6b011-127">Library</span></span><br/> | <dl> <span data-ttu-id="6b011-128"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b011-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b011-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b011-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b011-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="6b011-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="6b011-131">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="6b011-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
