---
title: 'ID3DX11EffectVariable AsInterface 方法 (D3dx11effect .h) '
description: 取得介面變數。
ms.assetid: 5b1e5d05-ab36-42c2-9990-154baff5e9a4
keywords:
- AsInterface 方法 Direct3D 11
- AsInterface 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，AsInterface 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsInterface
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0134aceea3202e0965bf05b709d29279be2fc29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696568"
---
# <a name="id3dx11effectvariableasinterface-method"></a><span data-ttu-id="79c77-106">ID3DX11EffectVariable：： AsInterface 方法</span><span class="sxs-lookup"><span data-stu-id="79c77-106">ID3DX11EffectVariable::AsInterface method</span></span>

<span data-ttu-id="79c77-107">取得介面變數。</span><span class="sxs-lookup"><span data-stu-id="79c77-107">Get an interface variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c77-108">語法</span><span class="sxs-lookup"><span data-stu-id="79c77-108">Syntax</span></span>


```C++
ID3DX11EffectInterfaceVariable* AsInterface();
```



## <a name="parameters"></a><span data-ttu-id="79c77-109">參數</span><span class="sxs-lookup"><span data-stu-id="79c77-109">Parameters</span></span>

<span data-ttu-id="79c77-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="79c77-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79c77-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="79c77-111">Return value</span></span>

<span data-ttu-id="79c77-112">類型： **[ **ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="79c77-112">Type: **[**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)\***</span></span>

<span data-ttu-id="79c77-113">介面變數的指標。</span><span class="sxs-lookup"><span data-stu-id="79c77-113">A pointer to an interface variable.</span></span> <span data-ttu-id="79c77-114">請參閱 [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md)。</span><span class="sxs-lookup"><span data-stu-id="79c77-114">See [**ID3DX11EffectInterfaceVariable**](id3dx11effectinterfacevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79c77-115">備註</span><span class="sxs-lookup"><span data-stu-id="79c77-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="79c77-116">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="79c77-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="79c77-117">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="79c77-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="79c77-118">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="79c77-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79c77-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="79c77-119">Requirements</span></span>



| <span data-ttu-id="79c77-120">需求</span><span class="sxs-lookup"><span data-stu-id="79c77-120">Requirement</span></span> | <span data-ttu-id="79c77-121">值</span><span class="sxs-lookup"><span data-stu-id="79c77-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c77-122">標頭</span><span class="sxs-lookup"><span data-stu-id="79c77-122">Header</span></span><br/>  | <dl> <span data-ttu-id="79c77-123"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="79c77-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="79c77-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="79c77-124">Library</span></span><br/> | <dl> <span data-ttu-id="79c77-125"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="79c77-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79c77-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79c77-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c77-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="79c77-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





