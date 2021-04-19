---
description: 使用左手座標系統來建立線條。
ms.assetid: 0d2ef331-9edf-4b0a-ace4-ecb8bb2f7352
title: 'D3DXCreateLine 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cf7d75ca63d64be39733b36a1b7d7a1b464238e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985873"
---
# <a name="d3dxcreateline-function"></a><span data-ttu-id="c551a-103">D3DXCreateLine 函式</span><span class="sxs-lookup"><span data-stu-id="c551a-103">D3DXCreateLine function</span></span>

<span data-ttu-id="c551a-104">使用左手座標系統來建立線條。</span><span class="sxs-lookup"><span data-stu-id="c551a-104">Uses a left-handed coordinate system to create a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="c551a-105">語法</span><span class="sxs-lookup"><span data-stu-id="c551a-105">Syntax</span></span>


```C++
HRESULT D3DXCreateLine(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXLINE        *ppLine
);
```



## <a name="parameters"></a><span data-ttu-id="c551a-106">參數</span><span class="sxs-lookup"><span data-stu-id="c551a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c551a-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c551a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c551a-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c551a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c551a-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與所建立之 box 網格相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="c551a-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c551a-110">*ppLine* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c551a-110">*ppLine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c551a-111">類型： **[ **LPD3DXLINE**](id3dxline.md)\***</span><span class="sxs-lookup"><span data-stu-id="c551a-111">Type: **[**LPD3DXLINE**](id3dxline.md)\***</span></span>

<span data-ttu-id="c551a-112">[**ID3DXLine**](id3dxline.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c551a-112">Pointer to an [**ID3DXLine**](id3dxline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c551a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c551a-113">Return value</span></span>

<span data-ttu-id="c551a-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c551a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c551a-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c551a-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c551a-116">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="c551a-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c551a-117">備註</span><span class="sxs-lookup"><span data-stu-id="c551a-117">Remarks</span></span>

<span data-ttu-id="c551a-118">此函式會使用 D3DXMESH \_ MANAGED 建立選項建立網格，並 [D3DFVF \_ XYZ \| D3DFVF \_ 標準](d3dfvf.md) 的彈性頂點格式 (FVF) 。</span><span class="sxs-lookup"><span data-stu-id="c551a-118">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) Flexible Vertex Format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="c551a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c551a-119">Requirements</span></span>



| <span data-ttu-id="c551a-120">需求</span><span class="sxs-lookup"><span data-stu-id="c551a-120">Requirement</span></span> | <span data-ttu-id="c551a-121">值</span><span class="sxs-lookup"><span data-stu-id="c551a-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c551a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c551a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c551a-123"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="c551a-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c551a-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="c551a-124">Library</span></span><br/> | <dl> <span data-ttu-id="c551a-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c551a-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c551a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c551a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c551a-127">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="c551a-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
