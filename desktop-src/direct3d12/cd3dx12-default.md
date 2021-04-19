---
title: 'CD3DX12_DEFAULT 結構 (D3dx12 .h) '
description: 將 D3D12 \_ 預設值傳遞至每個 helper 結構的函式。 此結構只是用來做為在其他 helper 結構上設定預設參數的機制。
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- CD3DX12_DEFAULT 結構
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975655"
---
# <a name="cd3dx12_default-structure"></a><span data-ttu-id="50832-105">CD3DX12 \_ 預設結構</span><span class="sxs-lookup"><span data-stu-id="50832-105">CD3DX12\_DEFAULT structure</span></span>

<span data-ttu-id="50832-106">將 D3D12 \_ 預設值傳遞至每個 helper 結構的函式。</span><span class="sxs-lookup"><span data-stu-id="50832-106">Passes D3D12\_DEFAULT into a constructor for each helper structure.</span></span> <span data-ttu-id="50832-107">此結構只是用來做為在其他 helper 結構上設定預設參數的機制。</span><span class="sxs-lookup"><span data-stu-id="50832-107">This structure is simply used as a mechanism to set default parameters on the other helper structures.</span></span>

## <a name="remarks"></a><span data-ttu-id="50832-108">備註</span><span class="sxs-lookup"><span data-stu-id="50832-108">Remarks</span></span>

<span data-ttu-id="50832-109">此結構的宣告方式如下：</span><span class="sxs-lookup"><span data-stu-id="50832-109">This struct is declared as follows:</span></span>

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

<span data-ttu-id="50832-110">將 D3D12 \_ 預設值傳遞至每個 helper 結構的函式。</span><span class="sxs-lookup"><span data-stu-id="50832-110">Passes D3D12\_DEFAULT into a constructor for each helper struct.</span></span> <span data-ttu-id="50832-111">例如，下列的函式會在 d3dx12 中宣告：</span><span class="sxs-lookup"><span data-stu-id="50832-111">For example, the following constructor is declared in d3dx12.h:</span></span>

<span data-ttu-id="50832-112">CD3DX12 \_ CPU \_ 描述項 \_ 控制碼 (CD3DX12 \_ 預設) {ptr = 0;}</span><span class="sxs-lookup"><span data-stu-id="50832-112">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT) { ptr = 0; }</span></span>

## <a name="requirements"></a><span data-ttu-id="50832-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="50832-113">Requirements</span></span>



| <span data-ttu-id="50832-114">需求</span><span class="sxs-lookup"><span data-stu-id="50832-114">Requirement</span></span> | <span data-ttu-id="50832-115">值</span><span class="sxs-lookup"><span data-stu-id="50832-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="50832-116">標頭</span><span class="sxs-lookup"><span data-stu-id="50832-116">Header</span></span><br/> | <dl> <span data-ttu-id="50832-117"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="50832-117"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50832-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50832-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50832-119">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="50832-119">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





