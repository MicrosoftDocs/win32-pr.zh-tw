---
description: ID3DXMATRIXStack：：：：轉譯方法 (D3DX10) -決定目前矩陣的乘積，以及由指定因數 (x、y 和 z) 所決定的計算轉譯矩陣。
ms.assetid: d6e347a5-bb66-451d-b66e-49ea8eff70b3
title: 'ID3DXMATRIXStack：：轉譯方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 41e84b62c077da03806a5e781498c05ee3c8ee67
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107766"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="5893e-103">ID3DXMATRIXStack：：轉譯方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="5893e-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="5893e-104">決定目前矩陣的乘積，以及由給定因素 (x、y 和 z) 所決定的計算轉譯矩陣。</span><span class="sxs-lookup"><span data-stu-id="5893e-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="5893e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5893e-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="5893e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5893e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5893e-107">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="5893e-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5893e-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5893e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5893e-109">X 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="5893e-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="5893e-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5893e-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5893e-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5893e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5893e-112">Y 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="5893e-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="5893e-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5893e-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5893e-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5893e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5893e-115">Z 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="5893e-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5893e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5893e-116">Return value</span></span>

<span data-ttu-id="5893e-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5893e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5893e-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5893e-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5893e-119">備註</span><span class="sxs-lookup"><span data-stu-id="5893e-119">Remarks</span></span>

<span data-ttu-id="5893e-120">這個方法會將目前的矩陣與計算的轉譯矩陣以右相乘 (轉換與目前的世界原點) 有關。</span><span class="sxs-lookup"><span data-stu-id="5893e-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="5893e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5893e-121">Requirements</span></span>



| <span data-ttu-id="5893e-122">需求</span><span class="sxs-lookup"><span data-stu-id="5893e-122">Requirement</span></span> | <span data-ttu-id="5893e-123">值</span><span class="sxs-lookup"><span data-stu-id="5893e-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5893e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5893e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5893e-125"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="5893e-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5893e-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="5893e-126">Library</span></span><br/> | <dl> <span data-ttu-id="5893e-127"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5893e-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5893e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5893e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5893e-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="5893e-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5893e-130">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="5893e-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
