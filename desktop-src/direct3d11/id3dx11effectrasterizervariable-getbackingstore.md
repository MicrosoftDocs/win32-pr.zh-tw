---
title: 'ID3DX11EffectRasterizerVariable GetBackingStore 方法 (D3dx11effect .h) '
description: 取得包含 rasteriser 狀態之變數的指標。
ms.assetid: aff62a6c-bdef-49ad-9492-5db0878f632e
keywords:
- GetBackingStore 方法 Direct3D 11
- GetBackingStore 方法 Direct3D 11，ID3DX11EffectRasterizerVariable 介面
- ID3DX11EffectRasterizerVariable 介面 Direct3D 11，GetBackingStore 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1941ba93b69f1d07eeebaa6c1f0c9323f5c0a49e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035408"
---
# <a name="id3dx11effectrasterizervariablegetbackingstore-method"></a><span data-ttu-id="e6373-106">ID3DX11EffectRasterizerVariable：： GetBackingStore 方法</span><span class="sxs-lookup"><span data-stu-id="e6373-106">ID3DX11EffectRasterizerVariable::GetBackingStore method</span></span>

<span data-ttu-id="e6373-107">取得包含 rasteriser 狀態之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="e6373-107">Get a pointer to a variable that contains rasteriser state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6373-108">語法</span><span class="sxs-lookup"><span data-stu-id="e6373-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT                  Index,
   D3D11_RASTERIZER_DESC *pRasterizerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="e6373-109">參數</span><span class="sxs-lookup"><span data-stu-id="e6373-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6373-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="e6373-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="e6373-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e6373-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e6373-112">Rasteriser 狀態原因陣列中的索引。</span><span class="sxs-lookup"><span data-stu-id="e6373-112">Index into an array of rasteriser-state descriptions.</span></span> <span data-ttu-id="e6373-113">如果效果中只有一個 rasteriser 變數，請使用0。</span><span class="sxs-lookup"><span data-stu-id="e6373-113">If there is only one rasteriser variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="e6373-114">*pRasterizerDesc*</span><span class="sxs-lookup"><span data-stu-id="e6373-114">*pRasterizerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="e6373-115">類型： D3D11 轉譯器 **[ **\_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***</span><span class="sxs-lookup"><span data-stu-id="e6373-115">Type: **[**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)\***</span></span>

<span data-ttu-id="e6373-116">Rasteriser 狀態原因的指標 (參閱 D3D11 轉譯器 [**\_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)) 。</span><span class="sxs-lookup"><span data-stu-id="e6373-116">A pointer to a rasteriser-state description (see [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6373-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6373-117">Return value</span></span>

<span data-ttu-id="e6373-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e6373-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e6373-119">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="e6373-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e6373-120">備註</span><span class="sxs-lookup"><span data-stu-id="e6373-120">Remarks</span></span>

<span data-ttu-id="e6373-121">效果變數會儲存在備份存放區的記憶體中;套用技術時，備份存放區中的值會複製到裝置。</span><span class="sxs-lookup"><span data-stu-id="e6373-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="e6373-122">備份存放區資料可以在必要時用來重新建立變數。</span><span class="sxs-lookup"><span data-stu-id="e6373-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="e6373-123">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="e6373-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e6373-124">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e6373-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e6373-125">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="e6373-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6373-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6373-126">Requirements</span></span>



| <span data-ttu-id="e6373-127">需求</span><span class="sxs-lookup"><span data-stu-id="e6373-127">Requirement</span></span> | <span data-ttu-id="e6373-128">值</span><span class="sxs-lookup"><span data-stu-id="e6373-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6373-129">標頭</span><span class="sxs-lookup"><span data-stu-id="e6373-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e6373-130"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6373-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e6373-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="e6373-131">Library</span></span><br/> | <dl> <span data-ttu-id="e6373-132"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="e6373-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6373-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6373-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6373-134">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="e6373-134">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

