---
description: 取得圖元著色器。
ms.assetid: 173a20a5-dda0-493f-a161-2dc2881e71f2
title: 'ID3DXBaseEffect：： GetPixelShader 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e555bac2e20ebab1cb0aec3d313cab8ad05e833e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986129"
---
# <a name="id3dxbaseeffectgetpixelshader-method"></a><span data-ttu-id="5781d-103">ID3DXBaseEffect：： GetPixelShader 方法</span><span class="sxs-lookup"><span data-stu-id="5781d-103">ID3DXBaseEffect::GetPixelShader method</span></span>

<span data-ttu-id="5781d-104">取得圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="5781d-104">Gets a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="5781d-105">語法</span><span class="sxs-lookup"><span data-stu-id="5781d-105">Syntax</span></span>


```C++
HRESULT GetPixelShader(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DPIXELSHADER9 *ppPShader
);
```



## <a name="parameters"></a><span data-ttu-id="5781d-106">參數</span><span class="sxs-lookup"><span data-stu-id="5781d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5781d-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5781d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5781d-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5781d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5781d-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5781d-109">Unique identifier.</span></span> <span data-ttu-id="5781d-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="5781d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5781d-111">*ppPShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5781d-111">*ppPShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5781d-112">類型： **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***</span><span class="sxs-lookup"><span data-stu-id="5781d-112">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)\***</span></span>

<span data-ttu-id="5781d-113">傳回圖元著色器物件。</span><span class="sxs-lookup"><span data-stu-id="5781d-113">Returns a pixel shader object.</span></span> <span data-ttu-id="5781d-114">請參閱 [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) 物件。</span><span class="sxs-lookup"><span data-stu-id="5781d-114">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5781d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5781d-115">Return value</span></span>

<span data-ttu-id="5781d-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5781d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5781d-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5781d-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5781d-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5781d-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5781d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5781d-119">Requirements</span></span>



| <span data-ttu-id="5781d-120">需求</span><span class="sxs-lookup"><span data-stu-id="5781d-120">Requirement</span></span> | <span data-ttu-id="5781d-121">值</span><span class="sxs-lookup"><span data-stu-id="5781d-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5781d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5781d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5781d-123"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="5781d-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5781d-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="5781d-124">Library</span></span><br/> | <dl> <span data-ttu-id="5781d-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5781d-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5781d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5781d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5781d-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="5781d-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
