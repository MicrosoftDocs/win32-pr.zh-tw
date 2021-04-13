---
title: 'ID3DX11EffectUnorderedAccessViewVariable SetUnorderedAccessViewArray 方法 (D3dx11effect .h) '
description: 設定未排序存取-views 的陣列。
ms.assetid: 12d0da06-990a-42b2-9566-cc5136f48781
keywords:
- SetUnorderedAccessViewArray 方法 Direct3D 11
- SetUnorderedAccessViewArray 方法 Direct3D 11，ID3DX11EffectUnorderedAccessViewVariable 介面
- ID3DX11EffectUnorderedAccessViewVariable 介面 Direct3D 11，SetUnorderedAccessViewArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053856f294906cf56acf1f38ca90663ebcc34051
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992158"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessviewarray-method"></a><span data-ttu-id="eaf49-106">ID3DX11EffectUnorderedAccessViewVariable：： SetUnorderedAccessViewArray 方法</span><span class="sxs-lookup"><span data-stu-id="eaf49-106">ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="eaf49-107">設定未排序存取-views 的陣列。</span><span class="sxs-lookup"><span data-stu-id="eaf49-107">Set an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf49-108">語法</span><span class="sxs-lookup"><span data-stu-id="eaf49-108">Syntax</span></span>


```C++
HRESULT SetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="eaf49-109">參數</span><span class="sxs-lookup"><span data-stu-id="eaf49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf49-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="eaf49-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="eaf49-111">類型： **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="eaf49-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="eaf49-112">[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="eaf49-112">An array of [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="eaf49-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="eaf49-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="eaf49-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaf49-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eaf49-115">第一個未排序存取視圖的索引。</span><span class="sxs-lookup"><span data-stu-id="eaf49-115">Index of the first unordered-access-view.</span></span>

</dd> <dt>

<span data-ttu-id="eaf49-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="eaf49-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="eaf49-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eaf49-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eaf49-118">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="eaf49-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaf49-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="eaf49-119">Return value</span></span>

<span data-ttu-id="eaf49-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eaf49-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eaf49-121">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="eaf49-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eaf49-122">備註</span><span class="sxs-lookup"><span data-stu-id="eaf49-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eaf49-123">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="eaf49-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="eaf49-124">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="eaf49-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="eaf49-125">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="eaf49-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eaf49-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaf49-126">Requirements</span></span>



| <span data-ttu-id="eaf49-127">需求</span><span class="sxs-lookup"><span data-stu-id="eaf49-127">Requirement</span></span> | <span data-ttu-id="eaf49-128">值</span><span class="sxs-lookup"><span data-stu-id="eaf49-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf49-129">標頭</span><span class="sxs-lookup"><span data-stu-id="eaf49-129">Header</span></span><br/>  | <dl> <span data-ttu-id="eaf49-130"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="eaf49-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="eaf49-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="eaf49-131">Library</span></span><br/> | <dl> <span data-ttu-id="eaf49-132"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="eaf49-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf49-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eaf49-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf49-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="eaf49-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

