---
description: ID3DXBaseMesh：:D rawSubset 方法-繪製網格的子集。
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: 'ID3DXBaseMesh：:D rawSubset 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.DrawSubset
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 252c9b9921c7eafd8f0c2a54cfa14a85e91b8f7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115466"
---
# <a name="id3dxbasemeshdrawsubset-method"></a><span data-ttu-id="767d7-103">ID3DXBaseMesh：:D rawSubset 方法</span><span class="sxs-lookup"><span data-stu-id="767d7-103">ID3DXBaseMesh::DrawSubset method</span></span>

<span data-ttu-id="767d7-104">繪製網格的子集。</span><span class="sxs-lookup"><span data-stu-id="767d7-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="767d7-105">語法</span><span class="sxs-lookup"><span data-stu-id="767d7-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="767d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="767d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="767d7-107">*AttribId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="767d7-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="767d7-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="767d7-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="767d7-109">DWORD，指定要繪製的網格子集。</span><span class="sxs-lookup"><span data-stu-id="767d7-109">DWORD that specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="767d7-110">此值可用來區分網格中的臉部，以屬於一或多個屬性群組。</span><span class="sxs-lookup"><span data-stu-id="767d7-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="767d7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="767d7-111">Return value</span></span>

<span data-ttu-id="767d7-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="767d7-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="767d7-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="767d7-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="767d7-114">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="767d7-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="767d7-115">備註</span><span class="sxs-lookup"><span data-stu-id="767d7-115">Remarks</span></span>

<span data-ttu-id="767d7-116">AttribId 所指定的子集將由 [**IDirect3DDevice9：:D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) 方法，使用 D3DPT TRIANGLELIST 基本型別轉譯 \_ ，因此索引緩衝區必須正確地初始化。</span><span class="sxs-lookup"><span data-stu-id="767d7-116">The subset that is specified by AttribId will be rendered by the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method, using the D3DPT\_TRIANGLELIST primitive type, so an index buffer must be properly initialized.</span></span>

<span data-ttu-id="767d7-117">屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。</span><span class="sxs-lookup"><span data-stu-id="767d7-117">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="767d7-118">此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時 (*AttribId*) 繪製指定的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="767d7-118">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (*AttribId*) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="767d7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="767d7-119">Requirements</span></span>



| <span data-ttu-id="767d7-120">需求</span><span class="sxs-lookup"><span data-stu-id="767d7-120">Requirement</span></span> | <span data-ttu-id="767d7-121">值</span><span class="sxs-lookup"><span data-stu-id="767d7-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="767d7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="767d7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="767d7-123"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="767d7-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="767d7-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="767d7-124">Library</span></span><br/> | <dl> <span data-ttu-id="767d7-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="767d7-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="767d7-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="767d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="767d7-127">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="767d7-127">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
