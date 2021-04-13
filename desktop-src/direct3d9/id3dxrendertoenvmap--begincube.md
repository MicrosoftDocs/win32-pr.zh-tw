---
description: 起始三次環境對應的呈現。
ms.assetid: 0f02b2e2-8132-4994-ab07-c79a1b7821dd
title: 'ID3DXRenderToEnvMap：： BeginCube 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.BeginCube
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bff6c8f3bdc49dfe0c1b677c6805cb332c05007d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322807"
---
# <a name="id3dxrendertoenvmapbegincube-method"></a><span data-ttu-id="c3afe-103">ID3DXRenderToEnvMap：： BeginCube 方法</span><span class="sxs-lookup"><span data-stu-id="c3afe-103">ID3DXRenderToEnvMap::BeginCube method</span></span>

<span data-ttu-id="c3afe-104">起始三次環境對應的呈現。</span><span class="sxs-lookup"><span data-stu-id="c3afe-104">Initiate the rendering of a cubic environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3afe-105">語法</span><span class="sxs-lookup"><span data-stu-id="c3afe-105">Syntax</span></span>


```C++
HRESULT BeginCube(
  [in] LPDIRECT3DCUBETEXTURE9 pCubeTex
);
```



## <a name="parameters"></a><span data-ttu-id="c3afe-106">參數</span><span class="sxs-lookup"><span data-stu-id="c3afe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3afe-107">*pCubeTex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3afe-107">*pCubeTex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3afe-108">類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="c3afe-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="c3afe-109">[**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)介面的指標，代表要轉譯的 cube 材質。</span><span class="sxs-lookup"><span data-stu-id="c3afe-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface that represents the cube texture to which to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3afe-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3afe-110">Return value</span></span>

<span data-ttu-id="c3afe-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3afe-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3afe-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c3afe-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c3afe-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="c3afe-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3afe-114">備註</span><span class="sxs-lookup"><span data-stu-id="c3afe-114">Remarks</span></span>

<span data-ttu-id="c3afe-115">請參閱 [**ID3DXRenderToEnvMap：：臉部**](id3dxrendertoenvmap--face.md) 以繪製6個臉部。</span><span class="sxs-lookup"><span data-stu-id="c3afe-115">See [**ID3DXRenderToEnvMap::Face**](id3dxrendertoenvmap--face.md) to draw each of the 6 faces.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3afe-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3afe-116">Requirements</span></span>



| <span data-ttu-id="c3afe-117">需求</span><span class="sxs-lookup"><span data-stu-id="c3afe-117">Requirement</span></span> | <span data-ttu-id="c3afe-118">值</span><span class="sxs-lookup"><span data-stu-id="c3afe-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3afe-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c3afe-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c3afe-120"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3afe-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c3afe-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="c3afe-121">Library</span></span><br/> | <dl> <span data-ttu-id="c3afe-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3afe-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3afe-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3afe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3afe-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="c3afe-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="c3afe-125">**ID3DXRenderToEnvMap：： End**</span><span class="sxs-lookup"><span data-stu-id="c3afe-125">**ID3DXRenderToEnvMap::End**</span></span>](id3dxrendertoenvmap--end.md)
</dt> </dl>

 

 
