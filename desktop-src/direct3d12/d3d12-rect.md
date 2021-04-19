---
title: 'D3D12_RECT (D3D12) '
description: D3D12 \_ rect 宣告為 rect。
ms.assetid: 39511ACE-7AC5-42A2-896D-7E0977A346C6
keywords:
- D3D12_RECT
topic_type:
- apiref
api_name:
- D3D12_RECT
api_location:
- D3D12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d408832e800413f94e251ee27a57e5b326378c36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997238"
---
# <a name="d3d12_rect"></a><span data-ttu-id="d04bf-104">D3D12 \_ RECT</span><span class="sxs-lookup"><span data-stu-id="d04bf-104">D3D12\_RECT</span></span>

<span data-ttu-id="d04bf-105">D3D12 \_ rect 宣告為 rect。</span><span class="sxs-lookup"><span data-stu-id="d04bf-105">D3D12\_RECT is declared as a RECT.</span></span> <span data-ttu-id="d04bf-106">如需有關此 GDI 矩形結構的詳細資訊，請參閱 [**RECT**](/previous-versions//dd162897(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="d04bf-106">For more information about this GDI rectangle structure, see [**RECT**](/previous-versions//dd162897(v=vs.85)).</span></span>

``` syntax
typedef RECT D3D12_RECT;
```

## <a name="remarks"></a><span data-ttu-id="d04bf-107">備註</span><span class="sxs-lookup"><span data-stu-id="d04bf-107">Remarks</span></span>

<span data-ttu-id="d04bf-108">下列方法會使用此結構：</span><span class="sxs-lookup"><span data-stu-id="d04bf-108">This structure is used by the following methods:</span></span>

-   [<span data-ttu-id="d04bf-109">**RSSetScissorRects**</span><span class="sxs-lookup"><span data-stu-id="d04bf-109">**RSSetScissorRects**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)
-   [<span data-ttu-id="d04bf-110">**ClearDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="d04bf-110">**ClearDepthStencilView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [<span data-ttu-id="d04bf-111">**ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="d04bf-111">**ClearRenderTargetView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [<span data-ttu-id="d04bf-112">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="d04bf-112">**ClearUnorderedAccessViewUint**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="d04bf-113">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="d04bf-113">**ClearUnorderedAccessViewFloat**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)

<span data-ttu-id="d04bf-114">此結構是 [**D3D12 \_ 捨棄 \_ 區域**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="d04bf-114">This structure is a member of the [**D3D12\_DISCARD\_REGION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_discard_region) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d04bf-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d04bf-115">Requirements</span></span>



| <span data-ttu-id="d04bf-116">需求</span><span class="sxs-lookup"><span data-stu-id="d04bf-116">Requirement</span></span> | <span data-ttu-id="d04bf-117">值</span><span class="sxs-lookup"><span data-stu-id="d04bf-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d04bf-118">標頭</span><span class="sxs-lookup"><span data-stu-id="d04bf-118">Header</span></span><br/> | <dl> <span data-ttu-id="d04bf-119"><dt>D3D12。h</dt></span><span class="sxs-lookup"><span data-stu-id="d04bf-119"><dt>D3D12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d04bf-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d04bf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d04bf-121">核心結構</span><span class="sxs-lookup"><span data-stu-id="d04bf-121">Core Structures</span></span>](direct3d-12-structures.md)
</dt> <dt>

[<span data-ttu-id="d04bf-122">**CD3DX12 \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="d04bf-122">**CD3DX12\_RECT**</span></span>](cd3dx12-rect.md)
</dt> </dl>

 

