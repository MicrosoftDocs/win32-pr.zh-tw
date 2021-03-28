---
title: 'ID3DX11EffectVariable GetType 方法 (D3dx11effect .h) '
description: 取得型別資訊。
ms.assetid: c9ada96a-0259-48c1-b869-ba0f51bf4600
keywords:
- GetType 方法 Direct3D 11
- GetType 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，GetType 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetType
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a6a654dd815770da8913660b22215dfbecc36b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322675"
---
# <a name="id3dx11effectvariablegettype-method"></a><span data-ttu-id="f0450-106">ID3DX11EffectVariable：： GetType 方法</span><span class="sxs-lookup"><span data-stu-id="f0450-106">ID3DX11EffectVariable::GetType method</span></span>

<span data-ttu-id="f0450-107">取得型別資訊。</span><span class="sxs-lookup"><span data-stu-id="f0450-107">Get type information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0450-108">語法</span><span class="sxs-lookup"><span data-stu-id="f0450-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetType();
```



## <a name="parameters"></a><span data-ttu-id="f0450-109">參數</span><span class="sxs-lookup"><span data-stu-id="f0450-109">Parameters</span></span>

<span data-ttu-id="f0450-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f0450-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0450-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0450-111">Return value</span></span>

<span data-ttu-id="f0450-112">類型： **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0450-112">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="f0450-113">[**ID3DX11EffectType**](id3dx11effecttype.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="f0450-113">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f0450-114">備註</span><span class="sxs-lookup"><span data-stu-id="f0450-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f0450-115">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="f0450-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f0450-116">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f0450-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f0450-117">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="f0450-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0450-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0450-118">Requirements</span></span>



| <span data-ttu-id="f0450-119">需求</span><span class="sxs-lookup"><span data-stu-id="f0450-119">Requirement</span></span> | <span data-ttu-id="f0450-120">值</span><span class="sxs-lookup"><span data-stu-id="f0450-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0450-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f0450-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f0450-122"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0450-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f0450-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="f0450-123">Library</span></span><br/> | <dl> <span data-ttu-id="f0450-124"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="f0450-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0450-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0450-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0450-126">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="f0450-126">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





