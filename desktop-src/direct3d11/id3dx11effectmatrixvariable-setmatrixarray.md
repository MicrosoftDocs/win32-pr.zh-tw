---
title: 'ID3DX11EffectMatrixVariable SetMatrixArray 方法 (D3dx11effect .h) '
description: 設定浮點數矩陣的陣列。
ms.assetid: c90d621c-7500-49c3-ab40-2d0630fc4bec
keywords:
- SetMatrixArray 方法 Direct3D 11
- SetMatrixArray 方法 Direct3D 11，ID3DX11EffectMatrixVariable 介面
- ID3DX11EffectMatrixVariable 介面 Direct3D 11，SetMatrixArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffe0f6a81e0086a9afd6da9e464f09ae577dab2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974624"
---
# <a name="id3dx11effectmatrixvariablesetmatrixarray-method"></a><span data-ttu-id="d934d-106">ID3DX11EffectMatrixVariable：： SetMatrixArray 方法</span><span class="sxs-lookup"><span data-stu-id="d934d-106">ID3DX11EffectMatrixVariable::SetMatrixArray method</span></span>

<span data-ttu-id="d934d-107">設定浮點數矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="d934d-107">Set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d934d-108">語法</span><span class="sxs-lookup"><span data-stu-id="d934d-108">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="d934d-109">參數</span><span class="sxs-lookup"><span data-stu-id="d934d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d934d-110">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="d934d-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="d934d-111">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="d934d-111">Type: **float\***</span></span>

<span data-ttu-id="d934d-112">第一個矩陣的指標。</span><span class="sxs-lookup"><span data-stu-id="d934d-112">A pointer to the first matrix.</span></span>

</dd> <dt>

<span data-ttu-id="d934d-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="d934d-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="d934d-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d934d-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d934d-115">要從陣列開頭跳過的矩陣元素數目。</span><span class="sxs-lookup"><span data-stu-id="d934d-115">The number of matrix elements to skip from the start of the array.</span></span>

</dd> <dt>

<span data-ttu-id="d934d-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="d934d-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="d934d-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d934d-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d934d-118">要設定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d934d-118">The number of elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d934d-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d934d-119">Return value</span></span>

<span data-ttu-id="d934d-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d934d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d934d-121">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="d934d-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d934d-122">備註</span><span class="sxs-lookup"><span data-stu-id="d934d-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d934d-123">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="d934d-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d934d-124">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d934d-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d934d-125">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="d934d-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d934d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d934d-126">Requirements</span></span>



| <span data-ttu-id="d934d-127">需求</span><span class="sxs-lookup"><span data-stu-id="d934d-127">Requirement</span></span> | <span data-ttu-id="d934d-128">值</span><span class="sxs-lookup"><span data-stu-id="d934d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d934d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d934d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d934d-130"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="d934d-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d934d-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="d934d-131">Library</span></span><br/> | <dl> <span data-ttu-id="d934d-132"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="d934d-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d934d-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d934d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d934d-134">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="d934d-134">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

