---
title: 'ID3DX11EffectInterfaceVariable SetClassInstance 方法 (D3dx11effect .h) '
description: 設定類別實例。
ms.assetid: fc71a0d2-054a-48ed-86a5-54cf0017062a
keywords:
- SetClassInstance 方法 Direct3D 11
- SetClassInstance 方法 Direct3D 11，ID3DX11EffectInterfaceVariable 介面
- ID3DX11EffectInterfaceVariable 介面 Direct3D 11，SetClassInstance 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectInterfaceVariable.SetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03d319d55b073393ff511b2e072aa07c244e5a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974560"
---
# <a name="id3dx11effectinterfacevariablesetclassinstance-method"></a><span data-ttu-id="e09b8-106">ID3DX11EffectInterfaceVariable：： SetClassInstance 方法</span><span class="sxs-lookup"><span data-stu-id="e09b8-106">ID3DX11EffectInterfaceVariable::SetClassInstance method</span></span>

<span data-ttu-id="e09b8-107">設定類別實例。</span><span class="sxs-lookup"><span data-stu-id="e09b8-107">Sets a class instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="e09b8-108">語法</span><span class="sxs-lookup"><span data-stu-id="e09b8-108">Syntax</span></span>


```C++
HRESULT SetClassInstance(
   ID3DX11EffectClassInstanceVariable *pEffectClassInstance
);
```



## <a name="parameters"></a><span data-ttu-id="e09b8-109">參數</span><span class="sxs-lookup"><span data-stu-id="e09b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e09b8-110">*pEffectClassInstance*</span><span class="sxs-lookup"><span data-stu-id="e09b8-110">*pEffectClassInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e09b8-111">類型： **[ **ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="e09b8-111">Type: **[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)\***</span></span>

<span data-ttu-id="e09b8-112">[**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e09b8-112">Pointer to an [**ID3DX11EffectClassInstanceVariable**](id3dx11effectclassinstancevariable.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e09b8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e09b8-113">Return value</span></span>

<span data-ttu-id="e09b8-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e09b8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e09b8-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="e09b8-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e09b8-116">備註</span><span class="sxs-lookup"><span data-stu-id="e09b8-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e09b8-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="e09b8-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e09b8-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e09b8-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e09b8-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="e09b8-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e09b8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e09b8-120">Requirements</span></span>



| <span data-ttu-id="e09b8-121">需求</span><span class="sxs-lookup"><span data-stu-id="e09b8-121">Requirement</span></span> | <span data-ttu-id="e09b8-122">值</span><span class="sxs-lookup"><span data-stu-id="e09b8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e09b8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e09b8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e09b8-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e09b8-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e09b8-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="e09b8-125">Library</span></span><br/> | <dl> <span data-ttu-id="e09b8-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="e09b8-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e09b8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e09b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e09b8-128">ID3DX11EffectInterfaceVariable</span><span class="sxs-lookup"><span data-stu-id="e09b8-128">ID3DX11EffectInterfaceVariable</span></span>](id3dx11effectinterfacevariable.md)
</dt> </dl>

 

 





