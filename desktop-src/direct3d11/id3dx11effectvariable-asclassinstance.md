---
title: 'ID3DX11EffectVariable AsClassInstance 方法 (D3dx11effect .h) '
description: 取得類別執行個體變數。
ms.assetid: c1d4adb5-7cd2-4ba2-9a91-3d03f9596a10
keywords:
- AsClassInstance 方法 Direct3D 11
- AsClassInstance 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，AsClassInstance 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17dc9124f4b9a24ead503694c10a4a2d2205ed3b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992143"
---
# <a name="id3dx11effectvariableasclassinstance-method"></a><span data-ttu-id="4079e-106">ID3DX11EffectVariable：： AsClassInstance 方法</span><span class="sxs-lookup"><span data-stu-id="4079e-106">ID3DX11EffectVariable::AsClassInstance method</span></span>

<span data-ttu-id="4079e-107">取得類別執行個體變數。</span><span class="sxs-lookup"><span data-stu-id="4079e-107">Get a class-instance variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="4079e-108">語法</span><span class="sxs-lookup"><span data-stu-id="4079e-108">Syntax</span></span>


```C++
ID3DX11EffectClassInstanceVariable* AsClassInstance();
```



## <a name="parameters"></a><span data-ttu-id="4079e-109">參數</span><span class="sxs-lookup"><span data-stu-id="4079e-109">Parameters</span></span>

<span data-ttu-id="4079e-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4079e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4079e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4079e-111">Return value</span></span>

<span data-ttu-id="4079e-112">類型： **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="4079e-112">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="4079e-113">類別執行個體變數的指標。</span><span class="sxs-lookup"><span data-stu-id="4079e-113">A pointer to class-instance variable.</span></span> <span data-ttu-id="4079e-114">請參閱 [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)。</span><span class="sxs-lookup"><span data-stu-id="4079e-114">See [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4079e-115">備註</span><span class="sxs-lookup"><span data-stu-id="4079e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4079e-116">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="4079e-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4079e-117">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4079e-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4079e-118">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="4079e-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4079e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4079e-119">Requirements</span></span>



| <span data-ttu-id="4079e-120">需求</span><span class="sxs-lookup"><span data-stu-id="4079e-120">Requirement</span></span> | <span data-ttu-id="4079e-121">值</span><span class="sxs-lookup"><span data-stu-id="4079e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4079e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4079e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4079e-123"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="4079e-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4079e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="4079e-124">Library</span></span><br/> | <dl> <span data-ttu-id="4079e-125"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="4079e-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4079e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4079e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4079e-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="4079e-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





