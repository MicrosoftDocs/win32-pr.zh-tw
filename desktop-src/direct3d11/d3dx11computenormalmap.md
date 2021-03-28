---
title: 'D3DX11ComputeNormalMap 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 DirectXTex 程式庫 ComputeNormalMap。
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- D3DX11ComputeNormalMap 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196374"
---
# <a name="d3dx11computenormalmap-function"></a><span data-ttu-id="62a2d-105">D3DX11ComputeNormalMap 函式</span><span class="sxs-lookup"><span data-stu-id="62a2d-105">D3DX11ComputeNormalMap function</span></span>

> [!Note]  
> <span data-ttu-id="62a2d-106">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="62a2d-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="62a2d-107">我們建議您不要使用此函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 **ComputeNormalMap**。</span><span class="sxs-lookup"><span data-stu-id="62a2d-107">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **ComputeNormalMap**.</span></span>

 

<span data-ttu-id="62a2d-108">將高度地圖轉換成一般地圖。</span><span class="sxs-lookup"><span data-stu-id="62a2d-108">Converts a height map into a normal map.</span></span> <span data-ttu-id="62a2d-109">每個標準的 (x、y、z) 元件都會對應到輸出材質 (r、g、b) 通道。</span><span class="sxs-lookup"><span data-stu-id="62a2d-109">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a2d-110">語法</span><span class="sxs-lookup"><span data-stu-id="62a2d-110">Syntax</span></span>


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="62a2d-111">參數</span><span class="sxs-lookup"><span data-stu-id="62a2d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a2d-112">*pCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62a2d-112">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a2d-113">類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="62a2d-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="62a2d-114">[**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)介面的指標，代表來源的高度地圖材質。</span><span class="sxs-lookup"><span data-stu-id="62a2d-114">Pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="62a2d-115">*pSrcTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62a2d-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a2d-116">類型： **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="62a2d-116">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="62a2d-117">[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)介面的指標，代表來源的高度地圖材質。</span><span class="sxs-lookup"><span data-stu-id="62a2d-117">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="62a2d-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="62a2d-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a2d-119">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62a2d-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62a2d-120">\_控制正常對應產生的一或多個 D3DX NORMALMAP 旗標。</span><span class="sxs-lookup"><span data-stu-id="62a2d-120">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="62a2d-121">*頻道* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62a2d-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a2d-122">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62a2d-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62a2d-123">一個 D3DX \_ 通道旗標，指定高度資訊的來源。</span><span class="sxs-lookup"><span data-stu-id="62a2d-123">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="62a2d-124">*振幅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62a2d-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a2d-125">類型： **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62a2d-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62a2d-126">常數值乘數，可增加 (或減少標準對應中的值) 。</span><span class="sxs-lookup"><span data-stu-id="62a2d-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="62a2d-127">較高的值通常會使凹凸變得更明顯，較低的值通常會讓顯示的偏低。</span><span class="sxs-lookup"><span data-stu-id="62a2d-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="62a2d-128">*pDestTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62a2d-128">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62a2d-129">類型： **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="62a2d-129">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="62a2d-130">[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)介面的指標，表示目的地材質。</span><span class="sxs-lookup"><span data-stu-id="62a2d-130">Pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a2d-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="62a2d-131">Return value</span></span>

<span data-ttu-id="62a2d-132">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="62a2d-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="62a2d-133">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="62a2d-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="62a2d-134">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="62a2d-134">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="62a2d-135">備註</span><span class="sxs-lookup"><span data-stu-id="62a2d-135">Remarks</span></span>

<span data-ttu-id="62a2d-136">這個方法會使用核心大小為3x3 的中央差異來計算正常。</span><span class="sxs-lookup"><span data-stu-id="62a2d-136">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="62a2d-137">目的地中的 RGB 通道包含一般 (x、y、z) 元件的偏誤。</span><span class="sxs-lookup"><span data-stu-id="62a2d-137">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="62a2d-138">中央差異分母會硬式編碼為2.0。</span><span class="sxs-lookup"><span data-stu-id="62a2d-138">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a2d-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="62a2d-139">Requirements</span></span>



| <span data-ttu-id="62a2d-140">需求</span><span class="sxs-lookup"><span data-stu-id="62a2d-140">Requirement</span></span> | <span data-ttu-id="62a2d-141">值</span><span class="sxs-lookup"><span data-stu-id="62a2d-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62a2d-142">標頭</span><span class="sxs-lookup"><span data-stu-id="62a2d-142">Header</span></span><br/>  | <dl> <span data-ttu-id="62a2d-143"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-143"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="62a2d-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="62a2d-144">Library</span></span><br/> | <dl> <span data-ttu-id="62a2d-145"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="62a2d-145"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="62a2d-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62a2d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a2d-147">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="62a2d-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

