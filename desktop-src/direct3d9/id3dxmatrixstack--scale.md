---
description: ID3DXMATRIXStack：： Scale 方法 (D3dx9math) -調整目前有關全局座標原點的矩陣。
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
ms.openlocfilehash: 6d877fccf5bfebfdc1f9cf3943c4334e5b8c7fff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093366"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a><span data-ttu-id="52781-103">ID3DXMATRIXStack：： Scale 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="52781-103">ID3DXMATRIXStack::Scale method (D3dx9math.h)</span></span>

<span data-ttu-id="52781-104">調整目前的矩陣與全球座標原點的大小。</span><span class="sxs-lookup"><span data-stu-id="52781-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="52781-105">語法</span><span class="sxs-lookup"><span data-stu-id="52781-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="52781-106">參數</span><span class="sxs-lookup"><span data-stu-id="52781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52781-107">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="52781-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52781-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52781-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52781-109">X 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="52781-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="52781-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52781-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52781-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52781-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52781-112">Y 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="52781-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="52781-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52781-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52781-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52781-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52781-115">Z 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="52781-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52781-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="52781-116">Return value</span></span>

<span data-ttu-id="52781-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52781-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52781-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="52781-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="52781-119">備註</span><span class="sxs-lookup"><span data-stu-id="52781-119">Remarks</span></span>

<span data-ttu-id="52781-120">這個方法會將目前的矩陣與計算的刻度矩陣向右相乘。</span><span class="sxs-lookup"><span data-stu-id="52781-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="52781-121">轉換與目前的世界原點有關。</span><span class="sxs-lookup"><span data-stu-id="52781-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="52781-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="52781-122">Requirements</span></span>



| <span data-ttu-id="52781-123">需求</span><span class="sxs-lookup"><span data-stu-id="52781-123">Requirement</span></span> | <span data-ttu-id="52781-124">值</span><span class="sxs-lookup"><span data-stu-id="52781-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52781-125">標頭</span><span class="sxs-lookup"><span data-stu-id="52781-125">Header</span></span><br/>  | <dl> <span data-ttu-id="52781-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="52781-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="52781-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="52781-127">Library</span></span><br/> | <dl> <span data-ttu-id="52781-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="52781-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52781-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52781-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52781-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="52781-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="52781-131">**ID3DXMATRIXStack::ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="52781-131">**ID3DXMATRIXStack::ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
