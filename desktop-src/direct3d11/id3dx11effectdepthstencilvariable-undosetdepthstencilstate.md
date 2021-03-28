---
title: 'ID3DX11EffectDepthStencilVariable UndoSetDepthStencilState 方法 (D3dx11effect .h) '
description: 還原先前設定的深度樣板狀態。
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- UndoSetDepthStencilState 方法 Direct3D 11
- UndoSetDepthStencilState 方法 Direct3D 11，ID3DX11EffectDepthStencilVariable 介面
- ID3DX11EffectDepthStencilVariable 介面 Direct3D 11，UndoSetDepthStencilState 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd44d486d2613406617f0534046c54818267dd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992351"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a><span data-ttu-id="19b79-106">ID3DX11EffectDepthStencilVariable：： UndoSetDepthStencilState 方法</span><span class="sxs-lookup"><span data-stu-id="19b79-106">ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState method</span></span>

<span data-ttu-id="19b79-107">還原先前設定的深度樣板狀態。</span><span class="sxs-lookup"><span data-stu-id="19b79-107">Reverts a previously set depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b79-108">語法</span><span class="sxs-lookup"><span data-stu-id="19b79-108">Syntax</span></span>


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="19b79-109">參數</span><span class="sxs-lookup"><span data-stu-id="19b79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19b79-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="19b79-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="19b79-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="19b79-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="19b79-112">索引至深度樣板介面的陣列。</span><span class="sxs-lookup"><span data-stu-id="19b79-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="19b79-113">如果只有一個深度樣板介面，請使用0。</span><span class="sxs-lookup"><span data-stu-id="19b79-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19b79-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="19b79-114">Return value</span></span>

<span data-ttu-id="19b79-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19b79-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19b79-116">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="19b79-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="19b79-117">備註</span><span class="sxs-lookup"><span data-stu-id="19b79-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="19b79-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="19b79-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="19b79-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="19b79-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="19b79-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="19b79-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="19b79-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="19b79-121">Requirements</span></span>



| <span data-ttu-id="19b79-122">需求</span><span class="sxs-lookup"><span data-stu-id="19b79-122">Requirement</span></span> | <span data-ttu-id="19b79-123">值</span><span class="sxs-lookup"><span data-stu-id="19b79-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19b79-124">標頭</span><span class="sxs-lookup"><span data-stu-id="19b79-124">Header</span></span><br/>  | <dl> <span data-ttu-id="19b79-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="19b79-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="19b79-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="19b79-126">Library</span></span><br/> | <dl> <span data-ttu-id="19b79-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="19b79-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19b79-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19b79-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19b79-129">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="19b79-129">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

