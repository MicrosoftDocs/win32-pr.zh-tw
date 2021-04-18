---
title: 'ID3DX11EffectVectorVariable SetFloatVectorArray 方法 (D3dx11effect .h) '
description: 設定包含浮點數據之四個元件向量的陣列。
ms.assetid: f07edf0f-8a90-41bf-ae03-5a62a19e57e2
keywords:
- SetFloatVectorArray 方法 Direct3D 11
- SetFloatVectorArray 方法 Direct3D 11，ID3DX11EffectVectorVariable 介面
- ID3DX11EffectVectorVariable 介面 Direct3D 11，SetFloatVectorArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f8f731dd90251848095f899bdc141bbc1d6748
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974640"
---
# <a name="id3dx11effectvectorvariablesetfloatvectorarray-method"></a><span data-ttu-id="3c3a6-106">ID3DX11EffectVectorVariable：： SetFloatVectorArray 方法</span><span class="sxs-lookup"><span data-stu-id="3c3a6-106">ID3DX11EffectVectorVariable::SetFloatVectorArray method</span></span>

<span data-ttu-id="3c3a6-107">設定包含浮點數據之四個元件向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="3c3a6-107">Set an array of four-component vectors that contain floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3a6-108">語法</span><span class="sxs-lookup"><span data-stu-id="3c3a6-108">Syntax</span></span>


```C++
HRESULT SetFloatVectorArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="3c3a6-109">參數</span><span class="sxs-lookup"><span data-stu-id="3c3a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c3a6-110">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="3c3a6-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="3c3a6-111">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="3c3a6-111">Type: **float\***</span></span>

<span data-ttu-id="3c3a6-112">要設定之資料開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="3c3a6-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="3c3a6-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="3c3a6-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3c3a6-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c3a6-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c3a6-115">必須設為 0;這會保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="3c3a6-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="3c3a6-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="3c3a6-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3c3a6-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c3a6-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c3a6-118">要設定的陣列元素數目。</span><span class="sxs-lookup"><span data-stu-id="3c3a6-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c3a6-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c3a6-119">Return value</span></span>

<span data-ttu-id="3c3a6-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c3a6-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c3a6-121">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="3c3a6-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c3a6-122">備註</span><span class="sxs-lookup"><span data-stu-id="3c3a6-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3c3a6-123">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="3c3a6-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3c3a6-124">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3c3a6-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3c3a6-125">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="3c3a6-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c3a6-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c3a6-126">Requirements</span></span>



| <span data-ttu-id="3c3a6-127">需求</span><span class="sxs-lookup"><span data-stu-id="3c3a6-127">Requirement</span></span> | <span data-ttu-id="3c3a6-128">值</span><span class="sxs-lookup"><span data-stu-id="3c3a6-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3a6-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3c3a6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3c3a6-130"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c3a6-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3c3a6-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c3a6-131">Library</span></span><br/> | <dl> <span data-ttu-id="3c3a6-132"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="3c3a6-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c3a6-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c3a6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c3a6-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="3c3a6-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

