---
title: 'ID3DX11EffectPass GetDesc 方法 (D3dx11effect .h) '
description: 取得傳遞描述。
ms.assetid: 423766be-96b2-4038-834e-34125789e8b1
keywords:
- GetDesc 方法 Direct3D 11
- GetDesc 方法 Direct3D 11，ID3DX11EffectPass 介面
- ID3DX11EffectPass 介面 Direct3D 11，GetDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a85a8c08faa100ecb3987a1a1421613d9c448b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323075"
---
# <a name="id3dx11effectpassgetdesc-method"></a><span data-ttu-id="213f1-106">ID3DX11EffectPass：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="213f1-106">ID3DX11EffectPass::GetDesc method</span></span>

<span data-ttu-id="213f1-107">取得傳遞描述。</span><span class="sxs-lookup"><span data-stu-id="213f1-107">Get a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="213f1-108">語法</span><span class="sxs-lookup"><span data-stu-id="213f1-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_PASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="213f1-109">參數</span><span class="sxs-lookup"><span data-stu-id="213f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="213f1-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="213f1-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="213f1-111">類型： **[ **D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="213f1-111">Type: **[**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)\***</span></span>

<span data-ttu-id="213f1-112">傳遞描述的指標 (參閱 [**D3DX11 \_ pass \_ DESC**](d3dx11-pass-desc.md)) 。</span><span class="sxs-lookup"><span data-stu-id="213f1-112">A pointer to a pass description (see [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="213f1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="213f1-113">Return value</span></span>

<span data-ttu-id="213f1-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="213f1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="213f1-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="213f1-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="213f1-116">備註</span><span class="sxs-lookup"><span data-stu-id="213f1-116">Remarks</span></span>

<span data-ttu-id="213f1-117">Pass 是設定轉譯狀態和著色器的程式碼區塊， (接著設定常數緩衝區、取樣器和紋理) 。</span><span class="sxs-lookup"><span data-stu-id="213f1-117">A pass is a block of code that sets render state and shaders (which in turn sets constant buffers, samplers and textures).</span></span> <span data-ttu-id="213f1-118">效果技術包含一或多個階段。</span><span class="sxs-lookup"><span data-stu-id="213f1-118">An effect technique contains one or more passes.</span></span>

> [!Note]  
> <span data-ttu-id="213f1-119">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="213f1-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="213f1-120">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="213f1-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="213f1-121">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="213f1-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="213f1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="213f1-122">Requirements</span></span>



| <span data-ttu-id="213f1-123">需求</span><span class="sxs-lookup"><span data-stu-id="213f1-123">Requirement</span></span> | <span data-ttu-id="213f1-124">值</span><span class="sxs-lookup"><span data-stu-id="213f1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="213f1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="213f1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="213f1-126"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="213f1-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="213f1-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="213f1-127">Library</span></span><br/> | <dl> <span data-ttu-id="213f1-128"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="213f1-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="213f1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="213f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="213f1-130">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="213f1-130">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





