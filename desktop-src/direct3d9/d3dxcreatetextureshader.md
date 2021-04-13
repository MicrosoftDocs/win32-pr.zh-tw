---
description: 從編譯的著色器建立紋理著色器物件。
ms.assetid: 3e8017f7-fe6b-4f4e-a80e-b16b16c0b348
title: 'D3DXCreateTextureShader 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c32715f1b939d30acb53b1cbe07e081d43d21823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322939"
---
# <a name="d3dxcreatetextureshader-function"></a><span data-ttu-id="2efa5-103">D3DXCreateTextureShader 函式</span><span class="sxs-lookup"><span data-stu-id="2efa5-103">D3DXCreateTextureShader function</span></span>

<span data-ttu-id="2efa5-104">從編譯的著色器建立紋理著色器物件。</span><span class="sxs-lookup"><span data-stu-id="2efa5-104">Creates a texture shader object from the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="2efa5-105">語法</span><span class="sxs-lookup"><span data-stu-id="2efa5-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureShader(
  _In_  const DWORD               *pFunction,
  _Out_       LPD3DXTEXTURESHADER *ppTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="2efa5-106">參數</span><span class="sxs-lookup"><span data-stu-id="2efa5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2efa5-107">*pFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2efa5-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2efa5-108">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2efa5-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2efa5-109">函數 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="2efa5-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="2efa5-110">*ppTextureShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2efa5-110">*ppTextureShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2efa5-111">類型： **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span><span class="sxs-lookup"><span data-stu-id="2efa5-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)\***</span></span>

<span data-ttu-id="2efa5-112">傳回 [**ID3DXTextureShader**](id3dxtextureshader.md) 物件，這個物件可以用來 Cti 使用 [**D3DXFillTextureTX**](d3dxfilltexturetx.md) 函式填滿材質的內容。</span><span class="sxs-lookup"><span data-stu-id="2efa5-112">Returns an [**ID3DXTextureShader**](id3dxtextureshader.md) object which can be used to procedurally fill the contents of a texture using the [**D3DXFillTextureTX**](d3dxfilltexturetx.md) functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2efa5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2efa5-113">Return value</span></span>

<span data-ttu-id="2efa5-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2efa5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2efa5-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2efa5-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2efa5-116">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="2efa5-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2efa5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2efa5-117">Requirements</span></span>



| <span data-ttu-id="2efa5-118">需求</span><span class="sxs-lookup"><span data-stu-id="2efa5-118">Requirement</span></span> | <span data-ttu-id="2efa5-119">值</span><span class="sxs-lookup"><span data-stu-id="2efa5-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2efa5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2efa5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2efa5-121"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="2efa5-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2efa5-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="2efa5-122">Library</span></span><br/> | <dl> <span data-ttu-id="2efa5-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2efa5-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2efa5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2efa5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2efa5-125">著色器函式</span><span class="sxs-lookup"><span data-stu-id="2efa5-125">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
