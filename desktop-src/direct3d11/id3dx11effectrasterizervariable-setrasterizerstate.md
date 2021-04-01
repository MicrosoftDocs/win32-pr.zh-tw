---
title: 'ID3DX11EffectRasterizerVariable SetRasterizerState 方法 (D3dx11effect .h) '
description: 設定轉譯器的狀態。
ms.assetid: b2cd93fb-77bb-4a39-b686-7b8f683c9172
keywords:
- SetRasterizerState 方法 Direct3D 11
- SetRasterizerState 方法 Direct3D 11，ID3DX11EffectRasterizerVariable 介面
- ID3DX11EffectRasterizerVariable 介面 Direct3D 11，SetRasterizerState 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.SetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1f44df653339f274207bfa4283fc8470c8844f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196460"
---
# <a name="id3dx11effectrasterizervariablesetrasterizerstate-method"></a><span data-ttu-id="671ed-106">ID3DX11EffectRasterizerVariable：： SetRasterizerState 方法</span><span class="sxs-lookup"><span data-stu-id="671ed-106">ID3DX11EffectRasterizerVariable::SetRasterizerState method</span></span>

<span data-ttu-id="671ed-107">設定轉譯器的狀態。</span><span class="sxs-lookup"><span data-stu-id="671ed-107">Sets the rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="671ed-108">語法</span><span class="sxs-lookup"><span data-stu-id="671ed-108">Syntax</span></span>


```C++
HRESULT SetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState *pRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="671ed-109">參數</span><span class="sxs-lookup"><span data-stu-id="671ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="671ed-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="671ed-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="671ed-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="671ed-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="671ed-112">在轉譯器介面陣列中編制索引。</span><span class="sxs-lookup"><span data-stu-id="671ed-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="671ed-113">如果只有一個轉譯器介面，請使用0。</span><span class="sxs-lookup"><span data-stu-id="671ed-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="671ed-114">*pRasterizerState*</span><span class="sxs-lookup"><span data-stu-id="671ed-114">*pRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="671ed-115">類型： **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***</span><span class="sxs-lookup"><span data-stu-id="671ed-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***</span></span>

<span data-ttu-id="671ed-116">[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="671ed-116">Pointer to an [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="671ed-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="671ed-117">Return value</span></span>

<span data-ttu-id="671ed-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="671ed-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="671ed-119">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="671ed-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="671ed-120">備註</span><span class="sxs-lookup"><span data-stu-id="671ed-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="671ed-121">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="671ed-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="671ed-122">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="671ed-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="671ed-123">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="671ed-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="671ed-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="671ed-124">Requirements</span></span>



| <span data-ttu-id="671ed-125">需求</span><span class="sxs-lookup"><span data-stu-id="671ed-125">Requirement</span></span> | <span data-ttu-id="671ed-126">值</span><span class="sxs-lookup"><span data-stu-id="671ed-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="671ed-127">標頭</span><span class="sxs-lookup"><span data-stu-id="671ed-127">Header</span></span><br/>  | <dl> <span data-ttu-id="671ed-128"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="671ed-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="671ed-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="671ed-129">Library</span></span><br/> | <dl> <span data-ttu-id="671ed-130"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="671ed-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671ed-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="671ed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671ed-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="671ed-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

