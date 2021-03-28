---
title: 'ID3DX11EffectConstantBuffer SetTextureBuffer 方法 (D3dx11effect .h) '
description: 設定材質緩衝區。
ms.assetid: b8c327e4-52ff-498e-81e9-187e58bbe5d2
keywords:
- SetTextureBuffer 方法 Direct3D 11
- SetTextureBuffer 方法 Direct3D 11，ID3DX11EffectConstantBuffer 介面
- ID3DX11EffectConstantBuffer 介面 Direct3D 11，SetTextureBuffer 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer.SetTextureBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736ec4c5f0125dfc37925d67875cf97c5441117c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974484"
---
# <a name="id3dx11effectconstantbuffersettexturebuffer-method"></a><span data-ttu-id="6add5-106">ID3DX11EffectConstantBuffer：： SetTextureBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="6add5-106">ID3DX11EffectConstantBuffer::SetTextureBuffer method</span></span>

<span data-ttu-id="6add5-107">設定材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6add5-107">Set a texture-buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6add5-108">語法</span><span class="sxs-lookup"><span data-stu-id="6add5-108">Syntax</span></span>


```C++
HRESULT SetTextureBuffer(
   ID3D11ShaderResourceView *pTextureBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="6add5-109">參數</span><span class="sxs-lookup"><span data-stu-id="6add5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6add5-110">*pTextureBuffer*</span><span class="sxs-lookup"><span data-stu-id="6add5-110">*pTextureBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="6add5-111">類型： **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="6add5-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\***</span></span>

<span data-ttu-id="6add5-112">用來存取材質緩衝區的著色器資源檢視介面指標。</span><span class="sxs-lookup"><span data-stu-id="6add5-112">A pointer to a shader-resource-view interface for accessing a texture buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6add5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6add5-113">Return value</span></span>

<span data-ttu-id="6add5-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6add5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6add5-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="6add5-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6add5-116">備註</span><span class="sxs-lookup"><span data-stu-id="6add5-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6add5-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="6add5-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6add5-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6add5-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6add5-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="6add5-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6add5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6add5-120">Requirements</span></span>



| <span data-ttu-id="6add5-121">需求</span><span class="sxs-lookup"><span data-stu-id="6add5-121">Requirement</span></span> | <span data-ttu-id="6add5-122">值</span><span class="sxs-lookup"><span data-stu-id="6add5-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6add5-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6add5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6add5-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="6add5-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6add5-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="6add5-125">Library</span></span><br/> | <dl> <span data-ttu-id="6add5-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="6add5-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6add5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6add5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6add5-128">ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="6add5-128">ID3DX11EffectConstantBuffer</span></span>](id3dx11effectconstantbuffer.md)
</dt> </dl>

 

 





