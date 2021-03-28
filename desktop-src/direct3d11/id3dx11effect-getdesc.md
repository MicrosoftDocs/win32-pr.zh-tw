---
title: 'ID3DX11Effect GetDesc 方法 (D3dx11effect .h) '
description: 取得效果描述。
ms.assetid: ca684786-c813-48d1-acad-e78aafd1c0db
keywords:
- GetDesc 方法 Direct3D 11
- GetDesc 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587cde43ec2d9136bab5884691c99321d1492835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992346"
---
# <a name="id3dx11effectgetdesc-method"></a><span data-ttu-id="5e993-106">ID3DX11Effect：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="5e993-106">ID3DX11Effect::GetDesc method</span></span>

<span data-ttu-id="5e993-107">取得效果描述。</span><span class="sxs-lookup"><span data-stu-id="5e993-107">Get an effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e993-108">語法</span><span class="sxs-lookup"><span data-stu-id="5e993-108">Syntax</span></span>


```C++
HRESULT GetDesc(
   D3DX11_EFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="5e993-109">參數</span><span class="sxs-lookup"><span data-stu-id="5e993-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e993-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="5e993-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="5e993-111">類型： **[ **D3DX11 \_ 效果 \_ DESC**](d3dx11-effect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e993-111">Type: **[**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)\***</span></span>

<span data-ttu-id="5e993-112">效果描述的指標 (查看 [**D3DX11 \_ 效果 \_ DESC**](d3dx11-effect-desc.md)) 。</span><span class="sxs-lookup"><span data-stu-id="5e993-112">A pointer to an effect description (see [**D3DX11\_EFFECT\_DESC**](d3dx11-effect-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e993-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e993-113">Return value</span></span>

<span data-ttu-id="5e993-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e993-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e993-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="5e993-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e993-116">備註</span><span class="sxs-lookup"><span data-stu-id="5e993-116">Remarks</span></span>

<span data-ttu-id="5e993-117">效果描述包含效果的基本資訊，例如它所包含的技巧，以及它所需的常數緩衝區資源。</span><span class="sxs-lookup"><span data-stu-id="5e993-117">An effect description contains basic information about an effect such as the techniques it contains and the constant buffer resources it requires.</span></span>

> [!Note]  
> <span data-ttu-id="5e993-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="5e993-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="5e993-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5e993-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="5e993-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="5e993-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e993-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e993-121">Requirements</span></span>



| <span data-ttu-id="5e993-122">需求</span><span class="sxs-lookup"><span data-stu-id="5e993-122">Requirement</span></span> | <span data-ttu-id="5e993-123">值</span><span class="sxs-lookup"><span data-stu-id="5e993-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e993-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5e993-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5e993-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e993-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="5e993-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="5e993-126">Library</span></span><br/> | <dl> <span data-ttu-id="5e993-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="5e993-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e993-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e993-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e993-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="5e993-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





