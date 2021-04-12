---
description: 從緩衝區的色頻中，將係數資料從指定的係數範圍中解壓縮，並將資料加入至 IDirect3DTexture9 物件。
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'ID3DXPRTBuffer：： ExtractTexture 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ea6cfdc8fb6ec83f847ccf37d06972974ea4de8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946148"
---
# <a name="id3dxprtbufferextracttexture-method"></a><span data-ttu-id="2f0cc-103">ID3DXPRTBuffer：： ExtractTexture 方法</span><span class="sxs-lookup"><span data-stu-id="2f0cc-103">ID3DXPRTBuffer::ExtractTexture method</span></span>

<span data-ttu-id="2f0cc-104">從緩衝區的色頻中，將係數資料從指定的係數範圍中解壓縮，並將資料加入至 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 物件。</span><span class="sxs-lookup"><span data-stu-id="2f0cc-104">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f0cc-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f0cc-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="2f0cc-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f0cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f0cc-107">*頻道* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f0cc-107">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f0cc-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f0cc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f0cc-109">用來將材質資料解壓縮的緩衝區色彩通道。</span><span class="sxs-lookup"><span data-stu-id="2f0cc-109">Buffer color channel from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="2f0cc-110">*StartCoefficient* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f0cc-110">*StartCoefficient* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f0cc-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f0cc-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f0cc-112">要從中解壓縮紋理資料之緩衝區係數的起始值。</span><span class="sxs-lookup"><span data-stu-id="2f0cc-112">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="2f0cc-113">*NumCoefficients* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f0cc-113">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f0cc-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f0cc-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f0cc-115">從 StartCoefficient 開始解壓縮紋理資料的純量值。</span><span class="sxs-lookup"><span data-stu-id="2f0cc-115">Number of scalars, beginning at StartCoefficient, from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="2f0cc-116">*pTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f0cc-116">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f0cc-117">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="2f0cc-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="2f0cc-118">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)紋理物件的指標，該物件會儲存係數。</span><span class="sxs-lookup"><span data-stu-id="2f0cc-118">Pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f0cc-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f0cc-119">Return value</span></span>

<span data-ttu-id="2f0cc-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f0cc-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f0cc-121">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2f0cc-121">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2f0cc-122">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="2f0cc-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f0cc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f0cc-123">Requirements</span></span>



| <span data-ttu-id="2f0cc-124">需求</span><span class="sxs-lookup"><span data-stu-id="2f0cc-124">Requirement</span></span> | <span data-ttu-id="2f0cc-125">值</span><span class="sxs-lookup"><span data-stu-id="2f0cc-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f0cc-126">標頭</span><span class="sxs-lookup"><span data-stu-id="2f0cc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2f0cc-127"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f0cc-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2f0cc-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="2f0cc-128">Library</span></span><br/> | <dl> <span data-ttu-id="2f0cc-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f0cc-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f0cc-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f0cc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f0cc-131">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="2f0cc-131">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
