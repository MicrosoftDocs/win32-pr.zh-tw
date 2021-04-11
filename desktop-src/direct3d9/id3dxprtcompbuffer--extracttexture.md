---
description: 從 ID3DXPRTCompBuffer 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 IDirect3DTexture9 物件。
ms.assetid: 2159e57d-b8e5-421f-b20a-ac58b29e3c45
title: 'ID3DXPRTCompBuffer：： ExtractTexture 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6a2200c680c19019375a5e33d2d8b675992dc38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035378"
---
# <a name="id3dxprtcompbufferextracttexture-method"></a><span data-ttu-id="74499-103">ID3DXPRTCompBuffer：： ExtractTexture 方法</span><span class="sxs-lookup"><span data-stu-id="74499-103">ID3DXPRTCompBuffer::ExtractTexture method</span></span>

<span data-ttu-id="74499-104">從 [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) 壓縮的資料緩衝區中，將每個範例主體元件分析 (PCA) 投影係數，然後將資料新增至 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 物件。</span><span class="sxs-lookup"><span data-stu-id="74499-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="74499-105">語法</span><span class="sxs-lookup"><span data-stu-id="74499-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               StartPCA,
  [in] UINT               NumPCA,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="74499-106">參數</span><span class="sxs-lookup"><span data-stu-id="74499-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74499-107">*StartPCA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74499-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74499-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74499-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74499-109">要從中解壓縮紋理資料之緩衝區係數的起始值。</span><span class="sxs-lookup"><span data-stu-id="74499-109">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="74499-110">*NumPCA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74499-110">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74499-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74499-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74499-112">要從緩衝區中解壓縮的 PCA 係數數目。</span><span class="sxs-lookup"><span data-stu-id="74499-112">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="74499-113">*pTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74499-113">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74499-114">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="74499-114">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="74499-115">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)紋理物件的指標，該物件會儲存 PCA 係數。</span><span class="sxs-lookup"><span data-stu-id="74499-115">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74499-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="74499-116">Return value</span></span>

<span data-ttu-id="74499-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74499-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74499-118">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="74499-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="74499-119">如果方法失敗，則會傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="74499-119">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="74499-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="74499-120">Requirements</span></span>



| <span data-ttu-id="74499-121">需求</span><span class="sxs-lookup"><span data-stu-id="74499-121">Requirement</span></span> | <span data-ttu-id="74499-122">值</span><span class="sxs-lookup"><span data-stu-id="74499-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74499-123">標頭</span><span class="sxs-lookup"><span data-stu-id="74499-123">Header</span></span><br/>  | <dl> <span data-ttu-id="74499-124"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="74499-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="74499-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="74499-125">Library</span></span><br/> | <dl> <span data-ttu-id="74499-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="74499-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74499-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74499-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74499-128">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="74499-128">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
