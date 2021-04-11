---
description: 調整目前的矩陣與全球座標原點的大小。
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: 'ID3DXMATRIXStack：： Scale 方法 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5ed926a55c0dba6f74e819cd89a7fa75f6d087c4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116181"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a><span data-ttu-id="d2ace-103">ID3DXMATRIXStack：： Scale 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="d2ace-103">ID3DXMATRIXStack::Scale method (D3dx9math.h)</span></span>

<span data-ttu-id="d2ace-104">調整目前的矩陣與全球座標原點的大小。</span><span class="sxs-lookup"><span data-stu-id="d2ace-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ace-105">語法</span><span class="sxs-lookup"><span data-stu-id="d2ace-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="d2ace-106">參數</span><span class="sxs-lookup"><span data-stu-id="d2ace-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ace-107">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="d2ace-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ace-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2ace-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2ace-109">X 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="d2ace-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="d2ace-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2ace-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ace-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2ace-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2ace-112">Y 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="d2ace-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="d2ace-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2ace-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ace-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2ace-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2ace-115">Z 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="d2ace-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ace-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2ace-116">Return value</span></span>

<span data-ttu-id="d2ace-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2ace-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2ace-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d2ace-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2ace-119">備註</span><span class="sxs-lookup"><span data-stu-id="d2ace-119">Remarks</span></span>

<span data-ttu-id="d2ace-120">這個方法會將目前的矩陣與計算的刻度矩陣向右相乘。</span><span class="sxs-lookup"><span data-stu-id="d2ace-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="d2ace-121">轉換與目前的世界原點有關。</span><span class="sxs-lookup"><span data-stu-id="d2ace-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="d2ace-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2ace-122">Requirements</span></span>



| <span data-ttu-id="d2ace-123">需求</span><span class="sxs-lookup"><span data-stu-id="d2ace-123">Requirement</span></span> | <span data-ttu-id="d2ace-124">值</span><span class="sxs-lookup"><span data-stu-id="d2ace-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ace-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d2ace-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d2ace-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2ace-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d2ace-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2ace-127">Library</span></span><br/> | <dl> <span data-ttu-id="d2ace-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2ace-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2ace-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2ace-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ace-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="d2ace-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d2ace-131">**ID3DXMATRIXStack::ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="d2ace-131">**ID3DXMATRIXStack::ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
