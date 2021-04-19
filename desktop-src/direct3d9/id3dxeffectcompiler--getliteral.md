---
description: 取得參數的常值狀態。 常值參數的值不會在效果的存留期間變更。
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: 'ID3DXEffectCompiler：： GetLiteral 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c16e3798ab66a34e12812a3560572c45b9206b30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986081"
---
# <a name="id3dxeffectcompilergetliteral-method"></a><span data-ttu-id="21baa-104">ID3DXEffectCompiler：： GetLiteral 方法</span><span class="sxs-lookup"><span data-stu-id="21baa-104">ID3DXEffectCompiler::GetLiteral method</span></span>

<span data-ttu-id="21baa-105">取得參數的常值狀態。</span><span class="sxs-lookup"><span data-stu-id="21baa-105">Gets a literal status of a parameter.</span></span> <span data-ttu-id="21baa-106">常值參數的值不會在效果的存留期間變更。</span><span class="sxs-lookup"><span data-stu-id="21baa-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="21baa-107">語法</span><span class="sxs-lookup"><span data-stu-id="21baa-107">Syntax</span></span>


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="21baa-108">參數</span><span class="sxs-lookup"><span data-stu-id="21baa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21baa-109">*hParameter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21baa-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21baa-110">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="21baa-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="21baa-111">參數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="21baa-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="21baa-112">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="21baa-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="21baa-113">*pLiteral* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="21baa-113">*pLiteral* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21baa-114">類型： **[ **BOOL**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="21baa-114">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="21baa-115">如果參數是常值，則傳回 True，否則傳回 False。</span><span class="sxs-lookup"><span data-stu-id="21baa-115">Returns True if the parameter is a literal, and False otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21baa-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="21baa-116">Return value</span></span>

<span data-ttu-id="21baa-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21baa-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21baa-118">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="21baa-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21baa-119">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="21baa-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="21baa-120">備註</span><span class="sxs-lookup"><span data-stu-id="21baa-120">Remarks</span></span>

<span data-ttu-id="21baa-121">這種方法只會變更參數是否為常值。</span><span class="sxs-lookup"><span data-stu-id="21baa-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="21baa-122">若要變更參數的值，請使用 [**ID3DXBaseEffect：： SetBool**](id3dxbaseeffect--setbool.md) 或 [**ID3DXBaseEffect：： SetValue**](id3dxbaseeffect--setvalue.md)之類的方法。</span><span class="sxs-lookup"><span data-stu-id="21baa-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21baa-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="21baa-123">Requirements</span></span>



| <span data-ttu-id="21baa-124">需求</span><span class="sxs-lookup"><span data-stu-id="21baa-124">Requirement</span></span> | <span data-ttu-id="21baa-125">值</span><span class="sxs-lookup"><span data-stu-id="21baa-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21baa-126">標頭</span><span class="sxs-lookup"><span data-stu-id="21baa-126">Header</span></span><br/>  | <dl> <span data-ttu-id="21baa-127"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="21baa-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="21baa-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="21baa-128">Library</span></span><br/> | <dl> <span data-ttu-id="21baa-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="21baa-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="21baa-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21baa-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21baa-131">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="21baa-131">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="21baa-132"> (Direct3D 9) 的使用方式和常值 </span><span class="sxs-lookup"><span data-stu-id="21baa-132">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="21baa-133">**ID3DXEffectCompiler::SetLiteral**</span><span class="sxs-lookup"><span data-stu-id="21baa-133">**ID3DXEffectCompiler::SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
