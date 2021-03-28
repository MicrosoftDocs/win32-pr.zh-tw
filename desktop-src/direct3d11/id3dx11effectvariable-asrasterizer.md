---
title: 'ID3DX11EffectVariable AsRasterizer 方法 (D3dx11effect .h) '
description: 取得轉譯器變數。
ms.assetid: 6a55d067-f527-4a1b-a4d4-a6d1719aebe7
keywords:
- AsRasterizer 方法 Direct3D 11
- AsRasterizer 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，AsRasterizer 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsRasterizer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbe4edc1b1195a9d449b37897f0875b1f35aae3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992396"
---
# <a name="id3dx11effectvariableasrasterizer-method"></a><span data-ttu-id="332af-106">ID3DX11EffectVariable：： AsRasterizer 方法</span><span class="sxs-lookup"><span data-stu-id="332af-106">ID3DX11EffectVariable::AsRasterizer method</span></span>

<span data-ttu-id="332af-107">取得轉譯器變數。</span><span class="sxs-lookup"><span data-stu-id="332af-107">Get a rasterizer variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="332af-108">語法</span><span class="sxs-lookup"><span data-stu-id="332af-108">Syntax</span></span>


```C++
ID3DX11EffectRasterizerVariable* AsRasterizer();
```



## <a name="parameters"></a><span data-ttu-id="332af-109">參數</span><span class="sxs-lookup"><span data-stu-id="332af-109">Parameters</span></span>

<span data-ttu-id="332af-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="332af-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="332af-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="332af-111">Return value</span></span>

<span data-ttu-id="332af-112">類型： **[ **ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="332af-112">Type: **[**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)\***</span></span>

<span data-ttu-id="332af-113">轉譯器變數的指標。</span><span class="sxs-lookup"><span data-stu-id="332af-113">A pointer to a rasterizer variable.</span></span> <span data-ttu-id="332af-114">請參閱 [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md)。</span><span class="sxs-lookup"><span data-stu-id="332af-114">See [**ID3DX11EffectRasterizerVariable**](id3dx11effectrasterizervariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="332af-115">備註</span><span class="sxs-lookup"><span data-stu-id="332af-115">Remarks</span></span>

<span data-ttu-id="332af-116">AsRasterizer 會傳回已針對轉譯器變數特製化的效果變數版本。</span><span class="sxs-lookup"><span data-stu-id="332af-116">AsRasterizer returns a version of the effect variable that has been specialized to a rasterizer variable.</span></span> <span data-ttu-id="332af-117">類似于轉換，如果效果變數不包含轉譯器資料，則此特製化會傳回不正確物件。</span><span class="sxs-lookup"><span data-stu-id="332af-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain rasterizer data.</span></span>

<span data-ttu-id="332af-118">應用程式可以藉由呼叫 [**IsValid**](id3dx11effectvariable-isvalid.md)來測試傳回的物件是否有效。</span><span class="sxs-lookup"><span data-stu-id="332af-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="332af-119">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="332af-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="332af-120">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="332af-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="332af-121">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="332af-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="332af-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="332af-122">Requirements</span></span>



| <span data-ttu-id="332af-123">需求</span><span class="sxs-lookup"><span data-stu-id="332af-123">Requirement</span></span> | <span data-ttu-id="332af-124">值</span><span class="sxs-lookup"><span data-stu-id="332af-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="332af-125">標頭</span><span class="sxs-lookup"><span data-stu-id="332af-125">Header</span></span><br/>  | <dl> <span data-ttu-id="332af-126"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="332af-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="332af-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="332af-127">Library</span></span><br/> | <dl> <span data-ttu-id="332af-128"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="332af-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="332af-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="332af-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332af-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="332af-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





