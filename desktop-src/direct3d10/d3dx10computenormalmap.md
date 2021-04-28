---
description: D3DX10ComputeNormalMap 函式-將高度地圖轉換成一般地圖。 每個標準的 (x、y、z) 元件都會對應到輸出材質 (r、g、b) 通道。
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: 'D3DX10ComputeNormalMap 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 173a8e0c1b3130a399152187eb52288a0306051c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105316"
---
# <a name="d3dx10computenormalmap-function"></a><span data-ttu-id="83bb6-104">D3DX10ComputeNormalMap 函式</span><span class="sxs-lookup"><span data-stu-id="83bb6-104">D3DX10ComputeNormalMap function</span></span>

<span data-ttu-id="83bb6-105">將高度地圖轉換成一般地圖。</span><span class="sxs-lookup"><span data-stu-id="83bb6-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="83bb6-106">每個標準的 (x、y、z) 元件都會對應到輸出材質 (r、g、b) 通道。</span><span class="sxs-lookup"><span data-stu-id="83bb6-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="83bb6-107">語法</span><span class="sxs-lookup"><span data-stu-id="83bb6-107">Syntax</span></span>


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="83bb6-108">參數</span><span class="sxs-lookup"><span data-stu-id="83bb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83bb6-109">*pSrcTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83bb6-109">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bb6-110">類型： **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="83bb6-110">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="83bb6-111">ID3D10Texture2D 介面的指標，代表來源的高度地圖材質。</span><span class="sxs-lookup"><span data-stu-id="83bb6-111">Pointer to an ID3D10Texture2D interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="83bb6-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="83bb6-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bb6-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83bb6-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83bb6-114">\_控制正常對應產生的一或多個 D3DX NORMALMAP 旗標。</span><span class="sxs-lookup"><span data-stu-id="83bb6-114">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="83bb6-115">*頻道* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83bb6-115">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bb6-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83bb6-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83bb6-117">一個 D3DX \_ 通道旗標，指定高度資訊的來源。</span><span class="sxs-lookup"><span data-stu-id="83bb6-117">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="83bb6-118">*振幅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83bb6-118">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bb6-119">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83bb6-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83bb6-120">常數值乘數，可增加 (或減少標準對應中的值) 。</span><span class="sxs-lookup"><span data-stu-id="83bb6-120">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="83bb6-121">較高的值通常會使凹凸變得更明顯，較低的值通常會讓顯示的偏低。</span><span class="sxs-lookup"><span data-stu-id="83bb6-121">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="83bb6-122">*pDestTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83bb6-122">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bb6-123">類型： **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="83bb6-123">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="83bb6-124">ID3D10Texture2D 介面的指標，表示目的地材質。</span><span class="sxs-lookup"><span data-stu-id="83bb6-124">Pointer to an ID3D10Texture2D interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83bb6-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="83bb6-125">Return value</span></span>

<span data-ttu-id="83bb6-126">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83bb6-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83bb6-127">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="83bb6-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83bb6-128">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="83bb6-128">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="83bb6-129">備註</span><span class="sxs-lookup"><span data-stu-id="83bb6-129">Remarks</span></span>

<span data-ttu-id="83bb6-130">這個方法會使用核心大小為3x3 的中央差異來計算正常。</span><span class="sxs-lookup"><span data-stu-id="83bb6-130">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="83bb6-131">目的地中的 RGB 通道包含一般 (x、y、z) 元件的偏誤。</span><span class="sxs-lookup"><span data-stu-id="83bb6-131">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="83bb6-132">中央差異分母會硬式編碼為2.0。</span><span class="sxs-lookup"><span data-stu-id="83bb6-132">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="83bb6-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="83bb6-133">Requirements</span></span>



| <span data-ttu-id="83bb6-134">需求</span><span class="sxs-lookup"><span data-stu-id="83bb6-134">Requirement</span></span> | <span data-ttu-id="83bb6-135">值</span><span class="sxs-lookup"><span data-stu-id="83bb6-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83bb6-136">標頭</span><span class="sxs-lookup"><span data-stu-id="83bb6-136">Header</span></span><br/>  | <dl> <span data-ttu-id="83bb6-137"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="83bb6-137"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="83bb6-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="83bb6-138">Library</span></span><br/> | <dl> <span data-ttu-id="83bb6-139"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="83bb6-139"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="83bb6-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83bb6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83bb6-141">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="83bb6-141">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
