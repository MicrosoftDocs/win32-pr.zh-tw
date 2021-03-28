---
title: 'ID3DX11EffectBlendVariable UndoSetBlendState 方法 (D3dx11effect .h) '
description: 還原先前設定的 blend 狀態。
ms.assetid: 375c225b-558f-4ad0-81e7-62eff3e28cf1
keywords:
- UndoSetBlendState 方法 Direct3D 11
- UndoSetBlendState 方法 Direct3D 11，ID3DX11EffectBlendVariable 介面
- ID3DX11EffectBlendVariable 介面 Direct3D 11，UndoSetBlendState 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.UndoSetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e117eafa9b6379b2240cf491809c58d8600d840f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992323"
---
# <a name="id3dx11effectblendvariableundosetblendstate-method"></a><span data-ttu-id="51e56-106">ID3DX11EffectBlendVariable：： UndoSetBlendState 方法</span><span class="sxs-lookup"><span data-stu-id="51e56-106">ID3DX11EffectBlendVariable::UndoSetBlendState method</span></span>

<span data-ttu-id="51e56-107">還原先前設定的 blend 狀態。</span><span class="sxs-lookup"><span data-stu-id="51e56-107">Reverts a previously set blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e56-108">語法</span><span class="sxs-lookup"><span data-stu-id="51e56-108">Syntax</span></span>


```C++
HRESULT UndoSetBlendState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="51e56-109">參數</span><span class="sxs-lookup"><span data-stu-id="51e56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e56-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="51e56-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="51e56-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="51e56-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="51e56-112">在 blend 狀態介面的陣列中編制索引。</span><span class="sxs-lookup"><span data-stu-id="51e56-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="51e56-113">如果只有一個 blend 狀態介面，請使用0。</span><span class="sxs-lookup"><span data-stu-id="51e56-113">If there is only one blend-state interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e56-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="51e56-114">Return value</span></span>

<span data-ttu-id="51e56-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="51e56-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="51e56-116">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="51e56-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="51e56-117">備註</span><span class="sxs-lookup"><span data-stu-id="51e56-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="51e56-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="51e56-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="51e56-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="51e56-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="51e56-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="51e56-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51e56-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="51e56-121">Requirements</span></span>



| <span data-ttu-id="51e56-122">需求</span><span class="sxs-lookup"><span data-stu-id="51e56-122">Requirement</span></span> | <span data-ttu-id="51e56-123">值</span><span class="sxs-lookup"><span data-stu-id="51e56-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e56-124">標頭</span><span class="sxs-lookup"><span data-stu-id="51e56-124">Header</span></span><br/>  | <dl> <span data-ttu-id="51e56-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="51e56-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="51e56-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="51e56-126">Library</span></span><br/> | <dl> <span data-ttu-id="51e56-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="51e56-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51e56-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51e56-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e56-129">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="51e56-129">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

