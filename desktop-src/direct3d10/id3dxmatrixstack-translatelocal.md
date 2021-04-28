---
description: ID3DXMATRIXStack：： TranslateLocal 方法 (D3DX10 .h) -決定由給定因數 (x、y 和 z) 和目前矩陣所決定的計算轉譯矩陣的乘積。
ms.assetid: 96399801-dd80-4e9a-a5c3-c5d41eb9368a
title: 'ID3DXMATRIXStack：： TranslateLocal 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80fabea58bd30b0db9b3ff41b522614007fe4b7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107746"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx10h"></a><span data-ttu-id="8fe08-103">ID3DXMATRIXStack：： TranslateLocal 方法 (D3DX10 .h) </span><span class="sxs-lookup"><span data-stu-id="8fe08-103">ID3DXMATRIXStack::TranslateLocal method (D3DX10.h)</span></span>

<span data-ttu-id="8fe08-104">決定由給定因數決定的計算轉譯矩陣的乘積 (x、y 和 z) 和目前的矩陣。</span><span class="sxs-lookup"><span data-stu-id="8fe08-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe08-105">語法</span><span class="sxs-lookup"><span data-stu-id="8fe08-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="8fe08-106">參數</span><span class="sxs-lookup"><span data-stu-id="8fe08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe08-107">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="8fe08-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe08-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fe08-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fe08-109">X 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="8fe08-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="8fe08-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fe08-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe08-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fe08-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fe08-112">Y 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="8fe08-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="8fe08-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fe08-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe08-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fe08-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fe08-115">Z 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="8fe08-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe08-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fe08-116">Return value</span></span>

<span data-ttu-id="8fe08-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8fe08-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8fe08-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="8fe08-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fe08-119">備註</span><span class="sxs-lookup"><span data-stu-id="8fe08-119">Remarks</span></span>

<span data-ttu-id="8fe08-120">這個方法會將目前的矩陣與計算的轉譯矩陣相乘 (轉換是關於物件) 的本機來源。</span><span class="sxs-lookup"><span data-stu-id="8fe08-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation(&tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="8fe08-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fe08-121">Requirements</span></span>



| <span data-ttu-id="8fe08-122">需求</span><span class="sxs-lookup"><span data-stu-id="8fe08-122">Requirement</span></span> | <span data-ttu-id="8fe08-123">值</span><span class="sxs-lookup"><span data-stu-id="8fe08-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe08-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8fe08-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8fe08-125"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="8fe08-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8fe08-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="8fe08-126">Library</span></span><br/> | <dl> <span data-ttu-id="8fe08-127"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fe08-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe08-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fe08-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe08-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="8fe08-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="8fe08-130">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="8fe08-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
