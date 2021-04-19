---
description: 決定目前矩陣的乘積，以及由給定因素 (x、y 和 z) 所決定的計算轉譯矩陣。
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
ms.openlocfilehash: 159e1dc6b3dabeb92b32798cbe318f6c72c01d70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982050"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="50981-103">ID3DXMATRIXStack：：轉譯方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="50981-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="50981-104">決定目前矩陣的乘積，以及由給定因素 (x、y 和 z) 所決定的計算轉譯矩陣。</span><span class="sxs-lookup"><span data-stu-id="50981-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="50981-105">語法</span><span class="sxs-lookup"><span data-stu-id="50981-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="50981-106">參數</span><span class="sxs-lookup"><span data-stu-id="50981-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50981-107">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="50981-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50981-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50981-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50981-109">X 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="50981-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="50981-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50981-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50981-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50981-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50981-112">Y 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="50981-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="50981-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50981-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50981-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50981-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50981-115">Z 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="50981-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50981-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="50981-116">Return value</span></span>

<span data-ttu-id="50981-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="50981-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="50981-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="50981-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="50981-119">備註</span><span class="sxs-lookup"><span data-stu-id="50981-119">Remarks</span></span>

<span data-ttu-id="50981-120">這個方法會將目前的矩陣與計算的轉譯矩陣以右相乘 (轉換與目前的世界原點) 有關。</span><span class="sxs-lookup"><span data-stu-id="50981-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="50981-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="50981-121">Requirements</span></span>



| <span data-ttu-id="50981-122">需求</span><span class="sxs-lookup"><span data-stu-id="50981-122">Requirement</span></span> | <span data-ttu-id="50981-123">值</span><span class="sxs-lookup"><span data-stu-id="50981-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50981-124">標頭</span><span class="sxs-lookup"><span data-stu-id="50981-124">Header</span></span><br/>  | <dl> <span data-ttu-id="50981-125"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="50981-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="50981-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="50981-126">Library</span></span><br/> | <dl> <span data-ttu-id="50981-127"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="50981-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50981-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50981-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50981-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="50981-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="50981-130">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="50981-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
