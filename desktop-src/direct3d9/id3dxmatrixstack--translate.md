---
description: 決定目前矩陣的乘積，以及由給定因素 (x、y 和 z) 所決定的計算轉譯矩陣。
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: 'ID3DXMATRIXStack：：轉譯方法 (D3dx9math .h) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 228b4302a512e96d5c009edcb3f0b673ee61e047
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999056"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="f4381-103">ID3DXMATRIXStack：：轉譯方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="f4381-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="f4381-104">決定目前矩陣的乘積，以及由給定因素 (x、y 和 z) 所決定的計算轉譯矩陣。</span><span class="sxs-lookup"><span data-stu-id="f4381-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4381-105">語法</span><span class="sxs-lookup"><span data-stu-id="f4381-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="f4381-106">參數</span><span class="sxs-lookup"><span data-stu-id="f4381-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4381-107">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="f4381-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4381-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4381-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4381-109">X 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="f4381-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="f4381-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4381-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4381-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4381-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4381-112">Y 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="f4381-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="f4381-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4381-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4381-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4381-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4381-115">Z 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="f4381-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4381-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4381-116">Return value</span></span>

<span data-ttu-id="f4381-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4381-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4381-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f4381-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4381-119">備註</span><span class="sxs-lookup"><span data-stu-id="f4381-119">Remarks</span></span>

<span data-ttu-id="f4381-120">這個方法會將目前的矩陣與計算的轉譯矩陣以右相乘 (轉換與目前的世界原點) 有關。</span><span class="sxs-lookup"><span data-stu-id="f4381-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="f4381-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4381-121">Requirements</span></span>



| <span data-ttu-id="f4381-122">需求</span><span class="sxs-lookup"><span data-stu-id="f4381-122">Requirement</span></span> | <span data-ttu-id="f4381-123">值</span><span class="sxs-lookup"><span data-stu-id="f4381-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4381-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f4381-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f4381-125"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4381-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f4381-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="f4381-126">Library</span></span><br/> | <dl> <span data-ttu-id="f4381-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4381-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f4381-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4381-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4381-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="f4381-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f4381-130">**ID3DXMATRIXStack::TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="f4381-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
