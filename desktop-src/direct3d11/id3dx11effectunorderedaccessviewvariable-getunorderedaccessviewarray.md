---
title: 'ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessViewArray 方法 (D3dx11effect .h) '
description: 取得未排序存取-views 的陣列。
ms.assetid: 38f838bb-cdcb-43c2-8b98-a188f479e93d
keywords:
- GetUnorderedAccessViewArray 方法 Direct3D 11
- GetUnorderedAccessViewArray 方法 Direct3D 11，ID3DX11EffectUnorderedAccessViewVariable 介面
- ID3DX11EffectUnorderedAccessViewVariable 介面 Direct3D 11，GetUnorderedAccessViewArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c264b5652287676d0792027f4f0ea8921bdb92f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196333"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessviewarray-method"></a><span data-ttu-id="d7518-106">ID3DX11EffectUnorderedAccessViewVariable：： GetUnorderedAccessViewArray 方法</span><span class="sxs-lookup"><span data-stu-id="d7518-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="d7518-107">取得未排序存取-views 的陣列。</span><span class="sxs-lookup"><span data-stu-id="d7518-107">Get an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7518-108">語法</span><span class="sxs-lookup"><span data-stu-id="d7518-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="d7518-109">參數</span><span class="sxs-lookup"><span data-stu-id="d7518-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7518-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="d7518-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="d7518-111">類型： **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="d7518-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="d7518-112">傳回時，將設定為 UAV 陣列的 [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) 指標指標。</span><span class="sxs-lookup"><span data-stu-id="d7518-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set to the UAV array on return.</span></span>

</dd> <dt>

<span data-ttu-id="d7518-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="d7518-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="d7518-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d7518-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d7518-115">第一個介面的索引。</span><span class="sxs-lookup"><span data-stu-id="d7518-115">Index of the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="d7518-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="d7518-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="d7518-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d7518-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d7518-118">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d7518-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7518-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7518-119">Return value</span></span>

<span data-ttu-id="d7518-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d7518-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d7518-121">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="d7518-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7518-122">備註</span><span class="sxs-lookup"><span data-stu-id="d7518-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d7518-123">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="d7518-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d7518-124">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7518-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d7518-125">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="d7518-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7518-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7518-126">Requirements</span></span>



| <span data-ttu-id="d7518-127">需求</span><span class="sxs-lookup"><span data-stu-id="d7518-127">Requirement</span></span> | <span data-ttu-id="d7518-128">值</span><span class="sxs-lookup"><span data-stu-id="d7518-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7518-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d7518-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d7518-130"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7518-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d7518-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="d7518-131">Library</span></span><br/> | <dl> <span data-ttu-id="d7518-132"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="d7518-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7518-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7518-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7518-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="d7518-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

