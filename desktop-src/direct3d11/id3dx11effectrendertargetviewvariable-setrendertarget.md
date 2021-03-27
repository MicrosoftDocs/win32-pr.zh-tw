---
title: 'ID3DX11EffectRenderTargetViewVariable SetRenderTarget 方法 (D3dx11effect .h) '
description: 設定呈現目標。
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- SetRenderTarget 方法 Direct3D 11
- SetRenderTarget 方法 Direct3D 11，ID3DX11EffectRenderTargetViewVariable 介面
- ID3DX11EffectRenderTargetViewVariable 介面 Direct3D 11，SetRenderTarget 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb53f0dff19fcd8990575dc9b305b0fb2f7e149b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854092"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a><span data-ttu-id="fac6c-106">ID3DX11EffectRenderTargetViewVariable：： SetRenderTarget 方法</span><span class="sxs-lookup"><span data-stu-id="fac6c-106">ID3DX11EffectRenderTargetViewVariable::SetRenderTarget method</span></span>

<span data-ttu-id="fac6c-107">設定呈現目標。</span><span class="sxs-lookup"><span data-stu-id="fac6c-107">Set a render-target.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac6c-108">語法</span><span class="sxs-lookup"><span data-stu-id="fac6c-108">Syntax</span></span>


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="fac6c-109">參數</span><span class="sxs-lookup"><span data-stu-id="fac6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac6c-110">*pResource*</span><span class="sxs-lookup"><span data-stu-id="fac6c-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="fac6c-111">類型： **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span><span class="sxs-lookup"><span data-stu-id="fac6c-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span></span>

<span data-ttu-id="fac6c-112">呈現目標視圖介面的指標。</span><span class="sxs-lookup"><span data-stu-id="fac6c-112">A pointer to a render-target-view interface.</span></span> <span data-ttu-id="fac6c-113">請參閱 [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)。</span><span class="sxs-lookup"><span data-stu-id="fac6c-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac6c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="fac6c-114">Return value</span></span>

<span data-ttu-id="fac6c-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fac6c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fac6c-116">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="fac6c-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fac6c-117">備註</span><span class="sxs-lookup"><span data-stu-id="fac6c-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fac6c-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="fac6c-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fac6c-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fac6c-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fac6c-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="fac6c-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fac6c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="fac6c-121">Requirements</span></span>



| <span data-ttu-id="fac6c-122">需求</span><span class="sxs-lookup"><span data-stu-id="fac6c-122">Requirement</span></span> | <span data-ttu-id="fac6c-123">值</span><span class="sxs-lookup"><span data-stu-id="fac6c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac6c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fac6c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fac6c-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="fac6c-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fac6c-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="fac6c-126">Library</span></span><br/> | <dl> <span data-ttu-id="fac6c-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="fac6c-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac6c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fac6c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac6c-129">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="fac6c-129">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





