---
description: 設定每個材質的 >albedo 值，並覆寫先前的 >albedo 值。
ms.assetid: 2928c861-a07e-4099-b04f-cdfa41e70874
title: 'ID3DXPRTEngine：： SetPerTexelAlbedo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce977a1ab28477ab8e40d59d18cfbcc55f558f88
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386478"
---
# <a name="id3dxprtenginesetpertexelalbedo-method"></a><span data-ttu-id="3410d-103">ID3DXPRTEngine：： SetPerTexelAlbedo 方法</span><span class="sxs-lookup"><span data-stu-id="3410d-103">ID3DXPRTEngine::SetPerTexelAlbedo method</span></span>

<span data-ttu-id="3410d-104">設定每個材質的 >albedo 值，並覆寫先前的 >albedo 值。</span><span class="sxs-lookup"><span data-stu-id="3410d-104">Sets an albedo value for each texel, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3410d-105">語法</span><span class="sxs-lookup"><span data-stu-id="3410d-105">Syntax</span></span>


```C++
HRESULT SetPerTexelAlbedo(
  [in] LPDIRECT3DTEXTURE9        pAlbedoTexture,
  [in] UINT                      NumChannels,
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="3410d-106">參數</span><span class="sxs-lookup"><span data-stu-id="3410d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3410d-107">*pAlbedoTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3410d-107">*pAlbedoTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3410d-108">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="3410d-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="3410d-109">要在其中儲存 >albedo 值之 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 材質物件的指標。</span><span class="sxs-lookup"><span data-stu-id="3410d-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object in which to store albedo values.</span></span>

</dd> <dt>

<span data-ttu-id="3410d-110">*NumChannels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3410d-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3410d-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3410d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3410d-112">要設定的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="3410d-112">Number of color channels to set.</span></span> <span data-ttu-id="3410d-113">設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。</span><span class="sxs-lookup"><span data-stu-id="3410d-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="3410d-114">*pGH* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3410d-114">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3410d-115">類型： **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="3410d-115">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="3410d-116">[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)物件的選擇性指標。</span><span class="sxs-lookup"><span data-stu-id="3410d-116">Optional pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object.</span></span> <span data-ttu-id="3410d-117">如果未提供，就會在內部建立並終結材質裝訂邊 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="3410d-117">If not provided, a texture gutter helper object is created and destroyed internally.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3410d-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="3410d-118">Return value</span></span>

<span data-ttu-id="3410d-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3410d-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3410d-120">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3410d-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3410d-121">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLED3DERR \_ OUTOFVIDEOMEMORY、D3DERR \_ WASSTILLDRAWING、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="3410d-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLED3DERR\_OUTOFVIDEOMEMORY, D3DERR\_WASSTILLDRAWING, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3410d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3410d-122">Requirements</span></span>



| <span data-ttu-id="3410d-123">需求</span><span class="sxs-lookup"><span data-stu-id="3410d-123">Requirement</span></span> | <span data-ttu-id="3410d-124">值</span><span class="sxs-lookup"><span data-stu-id="3410d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3410d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3410d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3410d-126"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="3410d-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3410d-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="3410d-127">Library</span></span><br/> | <dl> <span data-ttu-id="3410d-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3410d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3410d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3410d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3410d-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="3410d-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
