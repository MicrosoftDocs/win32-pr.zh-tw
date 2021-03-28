---
title: 'ID3DX11EffectRasterizerVariable GetRasterizerState 方法 (D3dx11effect .h) '
description: 取得轉譯器介面的指標。
ms.assetid: 4b8515e0-b79a-4572-9142-07c50a8839b8
keywords:
- GetRasterizerState 方法 Direct3D 11
- GetRasterizerState 方法 Direct3D 11，ID3DX11EffectRasterizerVariable 介面
- ID3DX11EffectRasterizerVariable 介面 Direct3D 11，GetRasterizerState 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972140a8f74a3e5a6728429faddacc253aaa6c9d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974727"
---
# <a name="id3dx11effectrasterizervariablegetrasterizerstate-method"></a><span data-ttu-id="0032b-106">ID3DX11EffectRasterizerVariable：： GetRasterizerState 方法</span><span class="sxs-lookup"><span data-stu-id="0032b-106">ID3DX11EffectRasterizerVariable::GetRasterizerState method</span></span>

<span data-ttu-id="0032b-107">取得轉譯器介面的指標。</span><span class="sxs-lookup"><span data-stu-id="0032b-107">Get a pointer to a rasterizer interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0032b-108">語法</span><span class="sxs-lookup"><span data-stu-id="0032b-108">Syntax</span></span>


```C++
HRESULT GetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState **ppRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="0032b-109">參數</span><span class="sxs-lookup"><span data-stu-id="0032b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0032b-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="0032b-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="0032b-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0032b-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0032b-112">在轉譯器介面陣列中編制索引。</span><span class="sxs-lookup"><span data-stu-id="0032b-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="0032b-113">如果只有一個轉譯器介面，請使用0。</span><span class="sxs-lookup"><span data-stu-id="0032b-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="0032b-114">*ppRasterizerState*</span><span class="sxs-lookup"><span data-stu-id="0032b-114">*ppRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="0032b-115">類型： **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="0032b-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\*\***</span></span>

<span data-ttu-id="0032b-116">轉譯器介面指標的位址 (參閱 [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)) 。</span><span class="sxs-lookup"><span data-stu-id="0032b-116">The address of a pointer to a rasterizer interface (see [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0032b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0032b-117">Return value</span></span>

<span data-ttu-id="0032b-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0032b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0032b-119">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="0032b-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0032b-120">備註</span><span class="sxs-lookup"><span data-stu-id="0032b-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0032b-121">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="0032b-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0032b-122">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0032b-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0032b-123">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="0032b-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0032b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="0032b-124">Requirements</span></span>



| <span data-ttu-id="0032b-125">需求</span><span class="sxs-lookup"><span data-stu-id="0032b-125">Requirement</span></span> | <span data-ttu-id="0032b-126">值</span><span class="sxs-lookup"><span data-stu-id="0032b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0032b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0032b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0032b-128"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="0032b-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0032b-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="0032b-129">Library</span></span><br/> | <dl> <span data-ttu-id="0032b-130"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="0032b-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0032b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0032b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0032b-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="0032b-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

