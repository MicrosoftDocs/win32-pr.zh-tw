---
title: 'ID3DX11EffectStringVariable GetStringArray 方法 (D3dx11effect .h) '
description: 取得字串的陣列。
ms.assetid: 2cc45b2f-1851-49d2-8844-3e249c48f327
keywords:
- GetStringArray 方法 Direct3D 11
- GetStringArray 方法 Direct3D 11，ID3DX11EffectStringVariable 介面
- ID3DX11EffectStringVariable 介面 Direct3D 11，GetStringArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetStringArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2050ebd7c9ae3735385a379e6ef7bdff0e1cfd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974469"
---
# <a name="id3dx11effectstringvariablegetstringarray-method"></a><span data-ttu-id="23ce8-106">ID3DX11EffectStringVariable：： GetStringArray 方法</span><span class="sxs-lookup"><span data-stu-id="23ce8-106">ID3DX11EffectStringVariable::GetStringArray method</span></span>

<span data-ttu-id="23ce8-107">取得字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="23ce8-107">Get an array of strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="23ce8-108">語法</span><span class="sxs-lookup"><span data-stu-id="23ce8-108">Syntax</span></span>


```C++
HRESULT GetStringArray(
   LPCSTR *ppStrings,
   UINT   Offset,
   UINT   Count
);
```



## <a name="parameters"></a><span data-ttu-id="23ce8-109">參數</span><span class="sxs-lookup"><span data-stu-id="23ce8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23ce8-110">*ppStrings*</span><span class="sxs-lookup"><span data-stu-id="23ce8-110">*ppStrings*</span></span> 
</dt> <dd>

<span data-ttu-id="23ce8-111">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="23ce8-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="23ce8-112">陣列中第一個字串的指標。</span><span class="sxs-lookup"><span data-stu-id="23ce8-112">A pointer to the first string in the array.</span></span>

</dd> <dt>

<span data-ttu-id="23ce8-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="23ce8-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="23ce8-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="23ce8-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="23ce8-115">位移 (于陣列開頭與要取得的第一個字串之間) 的字串數目。</span><span class="sxs-lookup"><span data-stu-id="23ce8-115">The offset (in number of strings) between the start of the array and the first string to get.</span></span>

</dd> <dt>

<span data-ttu-id="23ce8-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="23ce8-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="23ce8-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="23ce8-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="23ce8-118">傳回陣列中的字串數目。</span><span class="sxs-lookup"><span data-stu-id="23ce8-118">The number of strings in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23ce8-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="23ce8-119">Return value</span></span>

<span data-ttu-id="23ce8-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23ce8-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23ce8-121">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="23ce8-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23ce8-122">備註</span><span class="sxs-lookup"><span data-stu-id="23ce8-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23ce8-123">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="23ce8-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="23ce8-124">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="23ce8-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="23ce8-125">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="23ce8-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23ce8-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="23ce8-126">Requirements</span></span>



| <span data-ttu-id="23ce8-127">需求</span><span class="sxs-lookup"><span data-stu-id="23ce8-127">Requirement</span></span> | <span data-ttu-id="23ce8-128">值</span><span class="sxs-lookup"><span data-stu-id="23ce8-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23ce8-129">標頭</span><span class="sxs-lookup"><span data-stu-id="23ce8-129">Header</span></span><br/>  | <dl> <span data-ttu-id="23ce8-130"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="23ce8-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="23ce8-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="23ce8-131">Library</span></span><br/> | <dl> <span data-ttu-id="23ce8-132"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="23ce8-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ce8-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23ce8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ce8-134">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="23ce8-134">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

