---
description: 切換參數的常值狀態。 常值參數的值不會在效果的存留期間變更。
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'ID3DXEffectCompiler：： SetLiteral 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322719"
---
# <a name="id3dxeffectcompilersetliteral-method"></a><span data-ttu-id="e42f6-104">ID3DXEffectCompiler：： SetLiteral 方法</span><span class="sxs-lookup"><span data-stu-id="e42f6-104">ID3DXEffectCompiler::SetLiteral method</span></span>

<span data-ttu-id="e42f6-105">切換參數的常值狀態。</span><span class="sxs-lookup"><span data-stu-id="e42f6-105">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="e42f6-106">常值參數的值不會在效果的存留期間變更。</span><span class="sxs-lookup"><span data-stu-id="e42f6-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="e42f6-107">語法</span><span class="sxs-lookup"><span data-stu-id="e42f6-107">Syntax</span></span>


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a><span data-ttu-id="e42f6-108">參數</span><span class="sxs-lookup"><span data-stu-id="e42f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e42f6-109">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e42f6-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e42f6-110">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e42f6-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e42f6-111">參數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="e42f6-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="e42f6-112">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="e42f6-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="e42f6-113">*常* \[ 值在\]</span><span class="sxs-lookup"><span data-stu-id="e42f6-113">*Literal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e42f6-114">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e42f6-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e42f6-115">如果設定為 **TRUE** ，則將參數設為常值，如果參數可以在著色器存留期間變更值，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="e42f6-115">Set to **TRUE** to make the parameter a literal, and **FALSE** if the parameter can change value during the shader lifetime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e42f6-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e42f6-116">Return value</span></span>

<span data-ttu-id="e42f6-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e42f6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e42f6-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e42f6-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e42f6-119">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="e42f6-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e42f6-120">備註</span><span class="sxs-lookup"><span data-stu-id="e42f6-120">Remarks</span></span>

<span data-ttu-id="e42f6-121">這種方法只會變更參數是否為常值。</span><span class="sxs-lookup"><span data-stu-id="e42f6-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="e42f6-122">若要變更參數的值，請使用 [**ID3DXBaseEffect：： SetBool**](id3dxbaseeffect--setbool.md) 或 [**ID3DXBaseEffect：： SetValue**](id3dxbaseeffect--setvalue.md)之類的方法。</span><span class="sxs-lookup"><span data-stu-id="e42f6-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

<span data-ttu-id="e42f6-123">在編譯效果之前，必須先呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="e42f6-123">This function must be called before the effect is compiled.</span></span> <span data-ttu-id="e42f6-124">以下是一個使用此函數的範例：</span><span class="sxs-lookup"><span data-stu-id="e42f6-124">Here is an example of how one might use this function:</span></span>


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a><span data-ttu-id="e42f6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e42f6-125">Requirements</span></span>



| <span data-ttu-id="e42f6-126">需求</span><span class="sxs-lookup"><span data-stu-id="e42f6-126">Requirement</span></span> | <span data-ttu-id="e42f6-127">值</span><span class="sxs-lookup"><span data-stu-id="e42f6-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e42f6-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e42f6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e42f6-129"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="e42f6-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e42f6-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="e42f6-130">Library</span></span><br/> | <dl> <span data-ttu-id="e42f6-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e42f6-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e42f6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e42f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e42f6-133">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="e42f6-133">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="e42f6-134"> (Direct3D 9) 的使用方式和常值 </span><span class="sxs-lookup"><span data-stu-id="e42f6-134">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="e42f6-135">**ID3DXEffectCompiler::GetLiteral**</span><span class="sxs-lookup"><span data-stu-id="e42f6-135">**ID3DXEffectCompiler::GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
