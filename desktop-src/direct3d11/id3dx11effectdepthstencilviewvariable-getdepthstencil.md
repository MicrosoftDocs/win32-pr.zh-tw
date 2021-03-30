---
title: 'ID3DX11EffectDepthStencilViewVariable GetDepthStencil 方法 (D3dx11effect .h) '
description: 取得深度樣板查看資源。
ms.assetid: 7d94d98b-7070-41ee-9a9d-fe848f8914f2
keywords:
- GetDepthStencil 方法 Direct3D 11
- GetDepthStencil 方法 Direct3D 11，ID3DX11EffectDepthStencilViewVariable 介面
- ID3DX11EffectDepthStencilViewVariable 介面 Direct3D 11，GetDepthStencil 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49206f051922982ac77265e68fa3d7b7397d1348
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974676"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencil-method"></a><span data-ttu-id="aadb7-106">ID3DX11EffectDepthStencilViewVariable：： GetDepthStencil 方法</span><span class="sxs-lookup"><span data-stu-id="aadb7-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencil method</span></span>

<span data-ttu-id="aadb7-107">取得深度樣板查看資源。</span><span class="sxs-lookup"><span data-stu-id="aadb7-107">Get a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="aadb7-108">語法</span><span class="sxs-lookup"><span data-stu-id="aadb7-108">Syntax</span></span>


```C++
HRESULT GetDepthStencil(
   ID3D11DepthStencilView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="aadb7-109">參數</span><span class="sxs-lookup"><span data-stu-id="aadb7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aadb7-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="aadb7-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="aadb7-111">類型： **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="aadb7-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="aadb7-112">深度樣板視圖介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="aadb7-112">The address of a pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="aadb7-113">請參閱 [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)。</span><span class="sxs-lookup"><span data-stu-id="aadb7-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aadb7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="aadb7-114">Return value</span></span>

<span data-ttu-id="aadb7-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aadb7-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aadb7-116">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="aadb7-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aadb7-117">備註</span><span class="sxs-lookup"><span data-stu-id="aadb7-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aadb7-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="aadb7-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="aadb7-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="aadb7-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="aadb7-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="aadb7-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aadb7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="aadb7-121">Requirements</span></span>



| <span data-ttu-id="aadb7-122">需求</span><span class="sxs-lookup"><span data-stu-id="aadb7-122">Requirement</span></span> | <span data-ttu-id="aadb7-123">值</span><span class="sxs-lookup"><span data-stu-id="aadb7-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aadb7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="aadb7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="aadb7-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="aadb7-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="aadb7-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="aadb7-126">Library</span></span><br/> | <dl> <span data-ttu-id="aadb7-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="aadb7-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aadb7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aadb7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aadb7-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="aadb7-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





