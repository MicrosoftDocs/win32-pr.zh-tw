---
title: 'ID3DX11EffectSamplerVariable UndoSetSampler 方法 (D3dx11effect .h) '
description: 還原先前設定的取樣器狀態。
ms.assetid: bb837b12-d6c3-47e9-a0a1-0bfcfe0f3e4e
keywords:
- UndoSetSampler 方法 Direct3D 11
- UndoSetSampler 方法 Direct3D 11，ID3DX11EffectSamplerVariable 介面
- ID3DX11EffectSamplerVariable 介面 Direct3D 11，UndoSetSampler 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.UndoSetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e89d72130e92a477b3824f8e5f8fc935e99bd5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323280"
---
# <a name="id3dx11effectsamplervariableundosetsampler-method"></a><span data-ttu-id="f623e-106">ID3DX11EffectSamplerVariable：： UndoSetSampler 方法</span><span class="sxs-lookup"><span data-stu-id="f623e-106">ID3DX11EffectSamplerVariable::UndoSetSampler method</span></span>

<span data-ttu-id="f623e-107">還原先前設定的取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="f623e-107">Revert a previously set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f623e-108">語法</span><span class="sxs-lookup"><span data-stu-id="f623e-108">Syntax</span></span>


```C++
HRESULT UndoSetSampler(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="f623e-109">參數</span><span class="sxs-lookup"><span data-stu-id="f623e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f623e-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="f623e-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="f623e-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f623e-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f623e-112">索引至取樣器介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="f623e-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="f623e-113">如果只有一個取樣器介面，請使用0。</span><span class="sxs-lookup"><span data-stu-id="f623e-113">If there is only one sampler interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f623e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f623e-114">Return value</span></span>

<span data-ttu-id="f623e-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f623e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f623e-116">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="f623e-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f623e-117">備註</span><span class="sxs-lookup"><span data-stu-id="f623e-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f623e-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="f623e-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f623e-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f623e-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f623e-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="f623e-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f623e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f623e-121">Requirements</span></span>



| <span data-ttu-id="f623e-122">需求</span><span class="sxs-lookup"><span data-stu-id="f623e-122">Requirement</span></span> | <span data-ttu-id="f623e-123">值</span><span class="sxs-lookup"><span data-stu-id="f623e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f623e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f623e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f623e-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="f623e-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f623e-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="f623e-126">Library</span></span><br/> | <dl> <span data-ttu-id="f623e-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="f623e-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f623e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f623e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f623e-129">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="f623e-129">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

