---
title: 'ID3DX11EffectDepthStencilVariable GetDepthStencilState 方法 (D3dx11effect .h) '
description: 取得深度樣板介面的指標。
ms.assetid: 3e8f7fc6-960c-45f5-9276-9aa2a5e7a6c9
keywords:
- GetDepthStencilState 方法 Direct3D 11
- GetDepthStencilState 方法 Direct3D 11，ID3DX11EffectDepthStencilVariable 介面
- ID3DX11EffectDepthStencilVariable 介面 Direct3D 11，GetDepthStencilState 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9276c7a126d5441361a4d449c4ee2ece70d995
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974681"
---
# <a name="id3dx11effectdepthstencilvariablegetdepthstencilstate-method"></a><span data-ttu-id="5da0e-106">ID3DX11EffectDepthStencilVariable：： GetDepthStencilState 方法</span><span class="sxs-lookup"><span data-stu-id="5da0e-106">ID3DX11EffectDepthStencilVariable::GetDepthStencilState method</span></span>

<span data-ttu-id="5da0e-107">取得深度樣板介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5da0e-107">Get a pointer to a depth-stencil interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da0e-108">語法</span><span class="sxs-lookup"><span data-stu-id="5da0e-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState **ppDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="5da0e-109">參數</span><span class="sxs-lookup"><span data-stu-id="5da0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5da0e-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="5da0e-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="5da0e-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5da0e-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5da0e-112">索引至深度樣板介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="5da0e-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="5da0e-113">如果只有一個深度樣板介面，請使用0。</span><span class="sxs-lookup"><span data-stu-id="5da0e-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="5da0e-114">*ppDepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="5da0e-114">*ppDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="5da0e-115">類型： **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="5da0e-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span></span>

<span data-ttu-id="5da0e-116">Blend 狀態介面指標的位址 (參閱 [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)) 。</span><span class="sxs-lookup"><span data-stu-id="5da0e-116">The address of a pointer to a blend-state interface (see [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5da0e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5da0e-117">Return value</span></span>

<span data-ttu-id="5da0e-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5da0e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5da0e-119">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="5da0e-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5da0e-120">備註</span><span class="sxs-lookup"><span data-stu-id="5da0e-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5da0e-121">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="5da0e-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5da0e-122">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5da0e-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5da0e-123">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="5da0e-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5da0e-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5da0e-124">Requirements</span></span>



| <span data-ttu-id="5da0e-125">需求</span><span class="sxs-lookup"><span data-stu-id="5da0e-125">Requirement</span></span> | <span data-ttu-id="5da0e-126">值</span><span class="sxs-lookup"><span data-stu-id="5da0e-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5da0e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5da0e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5da0e-128"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="5da0e-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5da0e-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="5da0e-129">Library</span></span><br/> | <dl> <span data-ttu-id="5da0e-130"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="5da0e-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5da0e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5da0e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da0e-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="5da0e-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

