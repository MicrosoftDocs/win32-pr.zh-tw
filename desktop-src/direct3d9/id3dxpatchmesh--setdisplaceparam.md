---
description: 設定網狀幾何置換參數。
ms.assetid: 4c78e5b3-fb63-4341-a811-5531cf9564e7
title: 'ID3DXPatchMesh：： SetDisplaceParam 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.SetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1d59791859e0330415512db1551709729455d0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988197"
---
# <a name="id3dxpatchmeshsetdisplaceparam-method"></a><span data-ttu-id="6eeb5-103">ID3DXPatchMesh：： SetDisplaceParam 方法</span><span class="sxs-lookup"><span data-stu-id="6eeb5-103">ID3DXPatchMesh::SetDisplaceParam method</span></span>

<span data-ttu-id="6eeb5-104">設定網狀幾何置換參數。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-104">Sets mesh geometry displacement parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eeb5-105">語法</span><span class="sxs-lookup"><span data-stu-id="6eeb5-105">Syntax</span></span>


```C++
HRESULT SetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 Texture,
  [in] D3DTEXTUREFILTERTYPE   MinFilter,
  [in] D3DTEXTUREFILTERTYPE   MagFilter,
  [in] D3DTEXTUREFILTERTYPE   MipFilter,
  [in] D3DTEXTUREADDRESS      Wrap,
  [in] DWORD                  dwLODBias
);
```



## <a name="parameters"></a><span data-ttu-id="6eeb5-106">參數</span><span class="sxs-lookup"><span data-stu-id="6eeb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eeb5-107">*材質* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6eeb5-107">*Texture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb5-108">類型： **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="6eeb5-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="6eeb5-109">包含置換資料的材質。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-109">Texture containing the displacement data.</span></span>

</dd> <dt>

<span data-ttu-id="6eeb5-110">*MinFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6eeb5-110">*MinFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb5-111">類型： **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="6eeb5-111">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="6eeb5-112">縮制層級。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-112">Minification level.</span></span> <span data-ttu-id="6eeb5-113">如需詳細資訊，請參閱 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-113">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="6eeb5-114">*MagFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6eeb5-114">*MagFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb5-115">類型： **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="6eeb5-115">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="6eeb5-116">放大層級。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-116">Magnification level.</span></span> <span data-ttu-id="6eeb5-117">如需詳細資訊，請參閱 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-117">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="6eeb5-118">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6eeb5-118">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb5-119">類型： **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span><span class="sxs-lookup"><span data-stu-id="6eeb5-119">Type: **[**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**</span></span>

<span data-ttu-id="6eeb5-120">Mip 篩選層級。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-120">Mip filter level.</span></span> <span data-ttu-id="6eeb5-121">如需詳細資訊，請參閱 [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-121">For more information, see [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span>

</dd> <dt>

<span data-ttu-id="6eeb5-122">*換行* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6eeb5-122">*Wrap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb5-123">類型： **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**</span><span class="sxs-lookup"><span data-stu-id="6eeb5-123">Type: **[**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**</span></span>

<span data-ttu-id="6eeb5-124">材質位址換行模式。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-124">Texture address wrap mode.</span></span> <span data-ttu-id="6eeb5-125">如需詳細資訊，請參閱 [ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)</span><span class="sxs-lookup"><span data-stu-id="6eeb5-125">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md)</span></span>

</dd> <dt>

<span data-ttu-id="6eeb5-126">*dwLODBias* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6eeb5-126">*dwLODBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeb5-127">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6eeb5-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6eeb5-128">詳細資料偏差值的層級。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-128">Level of detail bias value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eeb5-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="6eeb5-129">Return value</span></span>

<span data-ttu-id="6eeb5-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6eeb5-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6eeb5-131">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-131">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6eeb5-132">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eeb5-133">備註</span><span class="sxs-lookup"><span data-stu-id="6eeb5-133">Remarks</span></span>

<span data-ttu-id="6eeb5-134">置換地圖只能是2D 紋理。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-134">Displacement maps can only be 2D textures.</span></span> <span data-ttu-id="6eeb5-135">Nonadaptive 鑲嵌會忽略 mipmap。</span><span class="sxs-lookup"><span data-stu-id="6eeb5-135">Mipmapping is ignored for nonadaptive tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eeb5-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="6eeb5-136">Requirements</span></span>



| <span data-ttu-id="6eeb5-137">需求</span><span class="sxs-lookup"><span data-stu-id="6eeb5-137">Requirement</span></span> | <span data-ttu-id="6eeb5-138">值</span><span class="sxs-lookup"><span data-stu-id="6eeb5-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6eeb5-139">標頭</span><span class="sxs-lookup"><span data-stu-id="6eeb5-139">Header</span></span><br/>  | <dl> <span data-ttu-id="6eeb5-140"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6eeb5-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6eeb5-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="6eeb5-141">Library</span></span><br/> | <dl> <span data-ttu-id="6eeb5-142"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6eeb5-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6eeb5-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6eeb5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eeb5-144">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="6eeb5-144">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
