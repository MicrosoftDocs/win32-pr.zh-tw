---
title: 'ID3DX11Effect GetVariableBySemantic 方法 (D3dx11effect .h) '
description: 依語義取得變數。
ms.assetid: fe731af6-3e9b-4f3e-9761-121796ac8c48
keywords:
- GetVariableBySemantic 方法 Direct3D 11
- GetVariableBySemantic 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetVariableBySemantic 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8276b1850242bd83639883bf75fc927d8484765
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196388"
---
# <a name="id3dx11effectgetvariablebysemantic-method"></a><span data-ttu-id="104ee-106">ID3DX11Effect：： GetVariableBySemantic 方法</span><span class="sxs-lookup"><span data-stu-id="104ee-106">ID3DX11Effect::GetVariableBySemantic method</span></span>

<span data-ttu-id="104ee-107">依語義取得變數。</span><span class="sxs-lookup"><span data-stu-id="104ee-107">Get a variable by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="104ee-108">語法</span><span class="sxs-lookup"><span data-stu-id="104ee-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="104ee-109">參數</span><span class="sxs-lookup"><span data-stu-id="104ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="104ee-110">*語義*</span><span class="sxs-lookup"><span data-stu-id="104ee-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="104ee-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="104ee-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="104ee-112">語義名稱。</span><span class="sxs-lookup"><span data-stu-id="104ee-112">The semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="104ee-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="104ee-113">Return value</span></span>

<span data-ttu-id="104ee-114">類型： **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="104ee-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="104ee-115">以語義表示之效果變數的指標。</span><span class="sxs-lookup"><span data-stu-id="104ee-115">A pointer to the effect variable indicated by the Semantic.</span></span> <span data-ttu-id="104ee-116">請參閱 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="104ee-116">See [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="104ee-117">備註</span><span class="sxs-lookup"><span data-stu-id="104ee-117">Remarks</span></span>

<span data-ttu-id="104ee-118">每個效果變數都可以附加語義，也就是使用者定義的中繼資料字串。</span><span class="sxs-lookup"><span data-stu-id="104ee-118">Each effect variable can have a semantic attached, which is a user defined metadata string.</span></span> <span data-ttu-id="104ee-119">某些 [系統值的語法](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) 是保留字，會觸發管線階段內建的功能。</span><span class="sxs-lookup"><span data-stu-id="104ee-119">Some [system-value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) are reserved words that trigger built in functionality by pipeline stages.</span></span>

<span data-ttu-id="104ee-120">如果找不到變數，方法會傳回 [**效果變數介面**](id3dx11effectvariable.md) 的指標;您可以呼叫 [**ID3DX11Effect：： IsValid**](id3dx11effect-isvalid.md) 來確認語義是否存在。</span><span class="sxs-lookup"><span data-stu-id="104ee-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the semantic exists.</span></span>

> [!Note]  
> <span data-ttu-id="104ee-121">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="104ee-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="104ee-122">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="104ee-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="104ee-123">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="104ee-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="104ee-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="104ee-124">Requirements</span></span>



| <span data-ttu-id="104ee-125">需求</span><span class="sxs-lookup"><span data-stu-id="104ee-125">Requirement</span></span> | <span data-ttu-id="104ee-126">值</span><span class="sxs-lookup"><span data-stu-id="104ee-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="104ee-127">標頭</span><span class="sxs-lookup"><span data-stu-id="104ee-127">Header</span></span><br/>  | <dl> <span data-ttu-id="104ee-128"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="104ee-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="104ee-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="104ee-129">Library</span></span><br/> | <dl> <span data-ttu-id="104ee-130"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="104ee-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="104ee-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="104ee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="104ee-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="104ee-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

