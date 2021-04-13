---
description: 起始球形環境對應的呈現。
ms.assetid: b0634120-f5ad-48b3-979a-30b0a53d22a2
title: 'ID3DXRenderToEnvMap：： BeginSphere 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginSphere
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 872aa06734ae818ef248b03fbc14dcd1c33fe815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322804"
---
# <a name="id3dxrendertoenvmapbeginsphere-method"></a><span data-ttu-id="c1758-103">ID3DXRenderToEnvMap：： BeginSphere 方法</span><span class="sxs-lookup"><span data-stu-id="c1758-103">ID3DXRenderToEnvMap::BeginSphere method</span></span>

<span data-ttu-id="c1758-104">起始球形環境對應的呈現。</span><span class="sxs-lookup"><span data-stu-id="c1758-104">Initiate the rendering of a spherical environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1758-105">語法</span><span class="sxs-lookup"><span data-stu-id="c1758-105">Syntax</span></span>


```C++
HRESULT BeginSphere(
  [in] LPDIRECT3DTEXTURE9 pTex
);
```



## <a name="parameters"></a><span data-ttu-id="c1758-106">參數</span><span class="sxs-lookup"><span data-stu-id="c1758-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1758-107">*pTex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1758-107">*pTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1758-108">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c1758-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c1758-109">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面的指標，該介面表示要呈現的材質。</span><span class="sxs-lookup"><span data-stu-id="c1758-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1758-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1758-110">Return value</span></span>

<span data-ttu-id="c1758-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1758-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1758-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c1758-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c1758-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="c1758-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.E\_FAIL</span></span>

## <a name="remarks"></a><span data-ttu-id="c1758-114">備註</span><span class="sxs-lookup"><span data-stu-id="c1758-114">Remarks</span></span>

<span data-ttu-id="c1758-115">請參閱 [**ID3DXRenderToEnvMap：：臉部**](id3dxrendertoenvmap--face.md) 以繪製臉部。</span><span class="sxs-lookup"><span data-stu-id="c1758-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw the face.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1758-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1758-116">Requirements</span></span>



| <span data-ttu-id="c1758-117">需求</span><span class="sxs-lookup"><span data-stu-id="c1758-117">Requirement</span></span> | <span data-ttu-id="c1758-118">值</span><span class="sxs-lookup"><span data-stu-id="c1758-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1758-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c1758-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c1758-120"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1758-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c1758-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1758-121">Library</span></span><br/> | <dl> <span data-ttu-id="c1758-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1758-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1758-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1758-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1758-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="c1758-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="c1758-125">**ID3DXRenderToEnvMap：： End**</span><span class="sxs-lookup"><span data-stu-id="c1758-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
