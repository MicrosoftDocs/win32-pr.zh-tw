---
description: 設定紋理。
ms.assetid: edf5bf61-508a-4417-bdf8-c36e6ba7ab30
title: 'ID3DXBaseEffect：： SetTexture 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 398dcc2f3d61ad32c08b67735a9ec7ed1a192acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985861"
---
# <a name="id3dxbaseeffectsettexture-method"></a><span data-ttu-id="be773-103">ID3DXBaseEffect：： SetTexture 方法</span><span class="sxs-lookup"><span data-stu-id="be773-103">ID3DXBaseEffect::SetTexture method</span></span>

<span data-ttu-id="be773-104">設定紋理。</span><span class="sxs-lookup"><span data-stu-id="be773-104">Sets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="be773-105">語法</span><span class="sxs-lookup"><span data-stu-id="be773-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] D3DXHANDLE             hParameter,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="be773-106">參數</span><span class="sxs-lookup"><span data-stu-id="be773-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be773-107">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be773-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be773-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="be773-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="be773-109">唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="be773-109">Unique identifier.</span></span> <span data-ttu-id="be773-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="be773-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="be773-111">*pTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be773-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be773-112">類型： **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="be773-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="be773-113">材質物件。</span><span class="sxs-lookup"><span data-stu-id="be773-113">Texture object.</span></span> <span data-ttu-id="be773-114">請參閱 [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)。</span><span class="sxs-lookup"><span data-stu-id="be773-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be773-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="be773-115">Return value</span></span>

<span data-ttu-id="be773-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be773-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be773-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="be773-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="be773-118">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="be773-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="be773-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="be773-119">Requirements</span></span>



| <span data-ttu-id="be773-120">需求</span><span class="sxs-lookup"><span data-stu-id="be773-120">Requirement</span></span> | <span data-ttu-id="be773-121">值</span><span class="sxs-lookup"><span data-stu-id="be773-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be773-122">標頭</span><span class="sxs-lookup"><span data-stu-id="be773-122">Header</span></span><br/>  | <dl> <span data-ttu-id="be773-123"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="be773-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="be773-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="be773-124">Library</span></span><br/> | <dl> <span data-ttu-id="be773-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="be773-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="be773-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be773-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be773-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="be773-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="be773-128">**GetTexture**</span><span class="sxs-lookup"><span data-stu-id="be773-128">**GetTexture**</span></span>](id3dxbaseeffect--gettexture.md)
</dt> </dl>

 

 
