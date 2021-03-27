---
title: 'ID3DX11EffectBlendVariable SetBlendState 方法 (D3dx11effect .h) '
description: 設定效果的 blend 狀態。
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- SetBlendState 方法 Direct3D 11
- SetBlendState 方法 Direct3D 11，ID3DX11EffectBlendVariable 介面
- ID3DX11EffectBlendVariable 介面 Direct3D 11，SetBlendState 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce781f29c521df7b81821cb19a56e6fd3999310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696755"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a><span data-ttu-id="19505-106">ID3DX11EffectBlendVariable：： SetBlendState 方法</span><span class="sxs-lookup"><span data-stu-id="19505-106">ID3DX11EffectBlendVariable::SetBlendState method</span></span>

<span data-ttu-id="19505-107">設定效果的 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="19505-107">Sets an effect's blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="19505-108">語法</span><span class="sxs-lookup"><span data-stu-id="19505-108">Syntax</span></span>


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="19505-109">參數</span><span class="sxs-lookup"><span data-stu-id="19505-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19505-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="19505-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="19505-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="19505-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="19505-112">在 blend 狀態介面的陣列中編制索引。</span><span class="sxs-lookup"><span data-stu-id="19505-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="19505-113">如果只有一個 blend 狀態介面，請使用0。</span><span class="sxs-lookup"><span data-stu-id="19505-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="19505-114">*pBlendState*</span><span class="sxs-lookup"><span data-stu-id="19505-114">*pBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="19505-115">類型： **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span><span class="sxs-lookup"><span data-stu-id="19505-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span></span>

<span data-ttu-id="19505-116">[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)介面的指標，其中包含要設定的 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="19505-116">A pointer to an [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) interface containing the blend-state to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19505-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="19505-117">Return value</span></span>

<span data-ttu-id="19505-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19505-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19505-119">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="19505-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="19505-120">備註</span><span class="sxs-lookup"><span data-stu-id="19505-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="19505-121">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="19505-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="19505-122">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="19505-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="19505-123">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="19505-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="19505-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="19505-124">Requirements</span></span>



| <span data-ttu-id="19505-125">需求</span><span class="sxs-lookup"><span data-stu-id="19505-125">Requirement</span></span> | <span data-ttu-id="19505-126">值</span><span class="sxs-lookup"><span data-stu-id="19505-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19505-127">標頭</span><span class="sxs-lookup"><span data-stu-id="19505-127">Header</span></span><br/>  | <dl> <span data-ttu-id="19505-128"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="19505-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="19505-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="19505-129">Library</span></span><br/> | <dl> <span data-ttu-id="19505-130"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="19505-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19505-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19505-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19505-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="19505-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

