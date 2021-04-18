---
title: 'ID3DX11EffectPass ComputeStateBlockMask 方法 (D3dx11effect .h) '
description: 產生遮罩以允許/防止狀態變更。
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- ComputeStateBlockMask 方法 Direct3D 11
- ComputeStateBlockMask 方法 Direct3D 11，ID3DX11EffectPass 介面
- ID3DX11EffectPass 介面 Direct3D 11，ComputeStateBlockMask 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc5cb32ce9e9644d7d5b62868bfa99f150cc94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974620"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a><span data-ttu-id="30f68-106">ID3DX11EffectPass：： ComputeStateBlockMask 方法</span><span class="sxs-lookup"><span data-stu-id="30f68-106">ID3DX11EffectPass::ComputeStateBlockMask method</span></span>

<span data-ttu-id="30f68-107">產生遮罩以允許/防止狀態變更。</span><span class="sxs-lookup"><span data-stu-id="30f68-107">Generate a mask for allowing/preventing state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f68-108">語法</span><span class="sxs-lookup"><span data-stu-id="30f68-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="30f68-109">參數</span><span class="sxs-lookup"><span data-stu-id="30f68-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f68-110">*pStateBlockMask*</span><span class="sxs-lookup"><span data-stu-id="30f68-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="30f68-111">類型： **[ **D3DX11 \_ 狀態 \_ 區塊 \_ 遮罩**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="30f68-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="30f68-112">狀態欄塊遮罩的指標 (參閱 [**D3DX11 \_ 狀態 \_ 區塊 \_ 遮罩**](d3dx11-state-block-mask.md)) 。</span><span class="sxs-lookup"><span data-stu-id="30f68-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f68-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="30f68-113">Return value</span></span>

<span data-ttu-id="30f68-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30f68-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30f68-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="30f68-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30f68-116">備註</span><span class="sxs-lookup"><span data-stu-id="30f68-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30f68-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="30f68-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="30f68-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="30f68-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="30f68-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="30f68-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30f68-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="30f68-120">Requirements</span></span>



| <span data-ttu-id="30f68-121">需求</span><span class="sxs-lookup"><span data-stu-id="30f68-121">Requirement</span></span> | <span data-ttu-id="30f68-122">值</span><span class="sxs-lookup"><span data-stu-id="30f68-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30f68-123">標頭</span><span class="sxs-lookup"><span data-stu-id="30f68-123">Header</span></span><br/>  | <dl> <span data-ttu-id="30f68-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="30f68-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="30f68-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="30f68-125">Library</span></span><br/> | <dl> <span data-ttu-id="30f68-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="30f68-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f68-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30f68-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f68-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="30f68-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





