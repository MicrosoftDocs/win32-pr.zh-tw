---
description: ID3DXMATRIXStack：：：：轉譯方法 (D3dx9math) -決定目前矩陣的乘積，以及由指定因數 (x、y 和 z) 所決定的計算轉譯矩陣。
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
ms.openlocfilehash: 7fadad95e8e72691a0e030ed89eedc745de2be43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093336"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="389f0-103">ID3DXMATRIXStack：：轉譯方法 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="389f0-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="389f0-104">決定目前矩陣的乘積，以及由給定因素 (x、y 和 z) 所決定的計算轉譯矩陣。</span><span class="sxs-lookup"><span data-stu-id="389f0-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="389f0-105">語法</span><span class="sxs-lookup"><span data-stu-id="389f0-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="389f0-106">參數</span><span class="sxs-lookup"><span data-stu-id="389f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="389f0-107">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="389f0-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="389f0-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="389f0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="389f0-109">X 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="389f0-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="389f0-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="389f0-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="389f0-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="389f0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="389f0-112">Y 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="389f0-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="389f0-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="389f0-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="389f0-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="389f0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="389f0-115">Z 方向的平移因數。</span><span class="sxs-lookup"><span data-stu-id="389f0-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="389f0-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="389f0-116">Return value</span></span>

<span data-ttu-id="389f0-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="389f0-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="389f0-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="389f0-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="389f0-119">備註</span><span class="sxs-lookup"><span data-stu-id="389f0-119">Remarks</span></span>

<span data-ttu-id="389f0-120">這個方法會將目前的矩陣與計算的轉譯矩陣以右相乘 (轉換與目前的世界原點) 有關。</span><span class="sxs-lookup"><span data-stu-id="389f0-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="389f0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="389f0-121">Requirements</span></span>



| <span data-ttu-id="389f0-122">需求</span><span class="sxs-lookup"><span data-stu-id="389f0-122">Requirement</span></span> | <span data-ttu-id="389f0-123">值</span><span class="sxs-lookup"><span data-stu-id="389f0-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="389f0-124">標頭</span><span class="sxs-lookup"><span data-stu-id="389f0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="389f0-125"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="389f0-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="389f0-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="389f0-126">Library</span></span><br/> | <dl> <span data-ttu-id="389f0-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="389f0-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="389f0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="389f0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="389f0-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="389f0-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="389f0-130">**ID3DXMATRIXStack::TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="389f0-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
