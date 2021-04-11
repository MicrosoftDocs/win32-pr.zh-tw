---
description: 調整目前有關物件原點的矩陣。
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: 'ID3DXMATRIXStack：： ScaleLocal 方法 (D3dx9math .h) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05b188e3f1b0322225584bc0ef7c194c52ef949f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196205"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a><span data-ttu-id="9fc0a-103">ID3DXMATRIXStack：： ScaleLocal 方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="9fc0a-103">ID3DXMATRIXStack::ScaleLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="9fc0a-104">調整目前有關物件原點的矩陣。</span><span class="sxs-lookup"><span data-stu-id="9fc0a-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc0a-105">語法</span><span class="sxs-lookup"><span data-stu-id="9fc0a-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="9fc0a-106">參數</span><span class="sxs-lookup"><span data-stu-id="9fc0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc0a-107">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="9fc0a-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc0a-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fc0a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fc0a-109">X 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="9fc0a-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="9fc0a-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fc0a-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc0a-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fc0a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fc0a-112">Y 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="9fc0a-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="9fc0a-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fc0a-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc0a-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fc0a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fc0a-115">Z 方向的縮放比例元件。</span><span class="sxs-lookup"><span data-stu-id="9fc0a-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc0a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fc0a-116">Return value</span></span>

<span data-ttu-id="9fc0a-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9fc0a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9fc0a-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9fc0a-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc0a-119">備註</span><span class="sxs-lookup"><span data-stu-id="9fc0a-119">Remarks</span></span>

<span data-ttu-id="9fc0a-120">這個方法會將目前的矩陣與計算的刻度矩陣相乘。</span><span class="sxs-lookup"><span data-stu-id="9fc0a-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="9fc0a-121">轉換是關於物件的本機來源。</span><span class="sxs-lookup"><span data-stu-id="9fc0a-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="9fc0a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fc0a-122">Requirements</span></span>



| <span data-ttu-id="9fc0a-123">需求</span><span class="sxs-lookup"><span data-stu-id="9fc0a-123">Requirement</span></span> | <span data-ttu-id="9fc0a-124">值</span><span class="sxs-lookup"><span data-stu-id="9fc0a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc0a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9fc0a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9fc0a-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9fc0a-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9fc0a-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="9fc0a-127">Library</span></span><br/> | <dl> <span data-ttu-id="9fc0a-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fc0a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9fc0a-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fc0a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc0a-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="9fc0a-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="9fc0a-131">**ID3DXMATRIXStack：： Scale**</span><span class="sxs-lookup"><span data-stu-id="9fc0a-131">**ID3DXMATRIXStack::Scale**</span></span>](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
