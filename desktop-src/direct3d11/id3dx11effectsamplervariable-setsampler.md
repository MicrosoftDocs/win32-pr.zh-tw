---
title: 'ID3DX11EffectSamplerVariable SetSampler 方法 (D3dx11effect .h) '
description: 設定取樣器狀態。
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- SetSampler 方法 Direct3D 11
- SetSampler 方法 Direct3D 11，ID3DX11EffectSamplerVariable 介面
- ID3DX11EffectSamplerVariable 介面 Direct3D 11，SetSampler 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.SetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a68adef00ac980b532e2fcd877e71eb63dc470
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323056"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a><span data-ttu-id="d5858-106">ID3DX11EffectSamplerVariable：： SetSampler 方法</span><span class="sxs-lookup"><span data-stu-id="d5858-106">ID3DX11EffectSamplerVariable::SetSampler method</span></span>

<span data-ttu-id="d5858-107">設定取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="d5858-107">Set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5858-108">語法</span><span class="sxs-lookup"><span data-stu-id="d5858-108">Syntax</span></span>


```C++
HRESULT SetSampler(
   UINT               Index,
   ID3D11SamplerState *pSampler
);
```



## <a name="parameters"></a><span data-ttu-id="d5858-109">參數</span><span class="sxs-lookup"><span data-stu-id="d5858-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5858-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="d5858-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="d5858-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d5858-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d5858-112">索引至取樣器介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="d5858-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="d5858-113">如果只有一個取樣器介面，請使用0。</span><span class="sxs-lookup"><span data-stu-id="d5858-113">If there is only one sampler interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="d5858-114">*pSampler*</span><span class="sxs-lookup"><span data-stu-id="d5858-114">*pSampler*</span></span> 
</dt> <dd>

<span data-ttu-id="d5858-115">類型： **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span><span class="sxs-lookup"><span data-stu-id="d5858-115">Type: **[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span></span>

<span data-ttu-id="d5858-116">[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)介面的指標，其中包含取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="d5858-116">Pointer to an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) interface containing the sampler state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5858-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5858-117">Return value</span></span>

<span data-ttu-id="d5858-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5858-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5858-119">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="d5858-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5858-120">備註</span><span class="sxs-lookup"><span data-stu-id="d5858-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5858-121">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="d5858-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d5858-122">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d5858-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d5858-123">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="d5858-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d5858-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5858-124">Requirements</span></span>



| <span data-ttu-id="d5858-125">需求</span><span class="sxs-lookup"><span data-stu-id="d5858-125">Requirement</span></span> | <span data-ttu-id="d5858-126">值</span><span class="sxs-lookup"><span data-stu-id="d5858-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5858-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d5858-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d5858-128"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5858-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d5858-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5858-129">Library</span></span><br/> | <dl> <span data-ttu-id="d5858-130"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="d5858-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5858-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5858-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5858-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="d5858-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

