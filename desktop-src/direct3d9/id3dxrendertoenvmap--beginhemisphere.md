---
description: 起始 hemispheric 環境對應的呈現。
ms.assetid: 1150aad9-dd8c-4943-afaf-90794faaaf70
title: 'ID3DXRenderToEnvMap：： BeginHemisphere 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginHemisphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96eb4bbf4cfc6cac952368337456b946f64cf711
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196229"
---
# <a name="id3dxrendertoenvmapbeginhemisphere-method"></a><span data-ttu-id="44620-103">ID3DXRenderToEnvMap：： BeginHemisphere 方法</span><span class="sxs-lookup"><span data-stu-id="44620-103">ID3DXRenderToEnvMap::BeginHemisphere method</span></span>

<span data-ttu-id="44620-104">起始 hemispheric 環境對應的呈現。</span><span class="sxs-lookup"><span data-stu-id="44620-104">Initiate the rendering of a hemispheric environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="44620-105">語法</span><span class="sxs-lookup"><span data-stu-id="44620-105">Syntax</span></span>


```C++
HRESULT BeginHemisphere(
  [in] LPDIRECT3DTEXTURE9 pTexZPos,
  [in] LPDIRECT3DTEXTURE9 pTexZNeg
);
```



## <a name="parameters"></a><span data-ttu-id="44620-106">參數</span><span class="sxs-lookup"><span data-stu-id="44620-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44620-107">*pTexZPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44620-107">*pTexZPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44620-108">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="44620-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="44620-109">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面的指標，代表正面材質呈現介面。</span><span class="sxs-lookup"><span data-stu-id="44620-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the positive texture render surface.</span></span>

</dd> <dt>

<span data-ttu-id="44620-110">*pTexZNeg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44620-110">*pTexZNeg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44620-111">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="44620-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="44620-112">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面的指標，代表負材質呈現介面。</span><span class="sxs-lookup"><span data-stu-id="44620-112">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the negative texture render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44620-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="44620-113">Return value</span></span>

<span data-ttu-id="44620-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44620-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44620-115">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="44620-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="44620-116">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="44620-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="44620-117">備註</span><span class="sxs-lookup"><span data-stu-id="44620-117">Remarks</span></span>

<span data-ttu-id="44620-118">請參閱 [**ID3DXRenderToEnvMap：：臉部**](id3dxrendertoenvmap--face.md) 以繪製臉部。</span><span class="sxs-lookup"><span data-stu-id="44620-118">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="44620-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="44620-119">Requirements</span></span>



| <span data-ttu-id="44620-120">需求</span><span class="sxs-lookup"><span data-stu-id="44620-120">Requirement</span></span> | <span data-ttu-id="44620-121">值</span><span class="sxs-lookup"><span data-stu-id="44620-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44620-122">標頭</span><span class="sxs-lookup"><span data-stu-id="44620-122">Header</span></span><br/>  | <dl> <span data-ttu-id="44620-123"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="44620-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="44620-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="44620-124">Library</span></span><br/> | <dl> <span data-ttu-id="44620-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="44620-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="44620-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44620-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44620-127">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="44620-127">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="44620-128">**ID3DXRenderToEnvMap：： End**</span><span class="sxs-lookup"><span data-stu-id="44620-128">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
