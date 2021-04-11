---
description: 建立轉譯環境對應。
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: 'D3DXCreateRenderToEnvMap 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035352"
---
# <a name="d3dxcreaterendertoenvmap-function"></a><span data-ttu-id="82a17-103">D3DXCreateRenderToEnvMap 函式</span><span class="sxs-lookup"><span data-stu-id="82a17-103">D3DXCreateRenderToEnvMap function</span></span>

<span data-ttu-id="82a17-104">建立轉譯環境對應。</span><span class="sxs-lookup"><span data-stu-id="82a17-104">Creates a render environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a17-105">語法</span><span class="sxs-lookup"><span data-stu-id="82a17-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a><span data-ttu-id="82a17-106">參數</span><span class="sxs-lookup"><span data-stu-id="82a17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82a17-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82a17-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a17-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="82a17-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="82a17-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，也就是與呈現介面相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="82a17-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, which is the device to associate with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="82a17-110">*大小* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82a17-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a17-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82a17-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82a17-112">呈現介面的大小。</span><span class="sxs-lookup"><span data-stu-id="82a17-112">Size of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="82a17-113">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82a17-113">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a17-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82a17-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82a17-115">Mipmap 層級的數目。</span><span class="sxs-lookup"><span data-stu-id="82a17-115">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="82a17-116">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82a17-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a17-117">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="82a17-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="82a17-118">[D3DFORMAT](d3dformat.md)列舉型別的成員，其描述環境對應的像素格式。</span><span class="sxs-lookup"><span data-stu-id="82a17-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the pixel format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="82a17-119">*DepthStencil* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82a17-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a17-120">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82a17-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82a17-121">若 **為 TRUE**，表示呈現介面支援深度樣板表面。</span><span class="sxs-lookup"><span data-stu-id="82a17-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="82a17-122">否則，此成員會設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="82a17-122">Otherwise, this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="82a17-123">*DepthStencilFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82a17-123">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a17-124">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="82a17-124">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="82a17-125">如果 DepthStencil 設定為 **TRUE**，這個參數就是 [D3DFORMAT](d3dformat.md) 列舉型別的成員，它會描述環境對應的深度樣板格式。</span><span class="sxs-lookup"><span data-stu-id="82a17-125">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the depth-stencil format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="82a17-126">*ppRenderToEnvMap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82a17-126">*ppRenderToEnvMap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82a17-127">類型： **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span><span class="sxs-lookup"><span data-stu-id="82a17-127">Type: **[**LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span></span>

<span data-ttu-id="82a17-128">[**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md)介面指標的位址，表示所建立的呈現環境對應。</span><span class="sxs-lookup"><span data-stu-id="82a17-128">Address of a pointer to an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) interface that represents the created render environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82a17-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="82a17-129">Return value</span></span>

<span data-ttu-id="82a17-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82a17-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82a17-131">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="82a17-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="82a17-132">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="82a17-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="82a17-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="82a17-133">Requirements</span></span>



| <span data-ttu-id="82a17-134">需求</span><span class="sxs-lookup"><span data-stu-id="82a17-134">Requirement</span></span> | <span data-ttu-id="82a17-135">值</span><span class="sxs-lookup"><span data-stu-id="82a17-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82a17-136">標頭</span><span class="sxs-lookup"><span data-stu-id="82a17-136">Header</span></span><br/>  | <dl> <span data-ttu-id="82a17-137"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="82a17-137"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="82a17-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="82a17-138">Library</span></span><br/> | <dl> <span data-ttu-id="82a17-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="82a17-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="82a17-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82a17-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82a17-141">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="82a17-141">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
