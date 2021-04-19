---
title: DXCore 介面卡屬性 GUID
description: 下列 adapter 屬性 Guid 是在中宣告 `dxcore_interface.h` ，而且會與 [IDXCoreAdapterFactory：： CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) 和 [IDXCoreAdapter：： IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) 方法搭配使用。
keywords:
- DXCore，adapter 屬性，Guid
topic_type:
- apiref
api_name:
- DXCore adapter attribute GUIDs
api_location:
- dxcore_interface.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a532552f144dfc21aa5d6a368aecd915d30b40c8
ms.sourcegitcommit: 8737f32d64e5f01c1d38aab92736e4088d6c446e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/31/2021
ms.locfileid: "106976306"
---
# <a name="dxcore-adapter-attribute-guids"></a><span data-ttu-id="53b59-104">DXCore 介面卡屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="53b59-104">DXCore adapter attribute GUIDs</span></span>

<span data-ttu-id="53b59-105">下列 adapter 屬性 Guid 是在中宣告 `dxcore_interface.h` ，而且會與 [IDXCoreAdapterFactory：： CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) 和 [IDXCoreAdapter：： IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) 方法搭配使用。</span><span class="sxs-lookup"><span data-stu-id="53b59-105">The following adapter attribute GUIDs are declared in `dxcore_interface.h`, and are used with the [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) and [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) methods.</span></span> <span data-ttu-id="53b59-106">針對任何指定的介面卡，可能會套用一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="53b59-106">For any given adapter, one or more of the attributes could apply.</span></span>

| <span data-ttu-id="53b59-107">GUID</span><span class="sxs-lookup"><span data-stu-id="53b59-107">GUID</span></span> | <span data-ttu-id="53b59-108">值</span><span class="sxs-lookup"><span data-stu-id="53b59-108">Value</span></span> |
|-|-|
| <span data-ttu-id="53b59-109">`DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`.</span><span class="sxs-lookup"><span data-stu-id="53b59-109">`DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`.</span></span> <span data-ttu-id="53b59-110">指定支援與 [Direct3D 11](/windows/win32/direct3d11) 圖形 api 搭配使用的介面卡。</span><span class="sxs-lookup"><span data-stu-id="53b59-110">Specifies an adapter that supports being used with the [Direct3D 11](/windows/win32/direct3d11) graphics APIs.</span></span> <span data-ttu-id="53b59-111">不保證特定功能，也不保證其目前設定中的作業系統支援這些 Api。</span><span class="sxs-lookup"><span data-stu-id="53b59-111">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="53b59-112">0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b</span><span class="sxs-lookup"><span data-stu-id="53b59-112">0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b</span></span> |
| <span data-ttu-id="53b59-113">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`.</span><span class="sxs-lookup"><span data-stu-id="53b59-113">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`.</span></span> <span data-ttu-id="53b59-114">指定支援與 [Direct3D 12](/windows/win32/direct3d12) 圖形 api 搭配使用的介面卡。</span><span class="sxs-lookup"><span data-stu-id="53b59-114">Specifies an adapter that supports being used with the [Direct3D 12](/windows/win32/direct3d12) graphics APIs.</span></span> <span data-ttu-id="53b59-115">不保證特定功能，也不保證其目前設定中的作業系統支援這些 Api。</span><span class="sxs-lookup"><span data-stu-id="53b59-115">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="53b59-116">0x0c9ece4d、0x2f6e、0x4f01、0x8c、0x96、0xe8、0x9e、0x33、0x1b、0x47、0xb1</span><span class="sxs-lookup"><span data-stu-id="53b59-116">0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xe8, 0x9e, 0x33, 0x1b, 0x47, 0xb1</span></span> |
| <span data-ttu-id="53b59-117">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`.</span><span class="sxs-lookup"><span data-stu-id="53b59-117">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`.</span></span> <span data-ttu-id="53b59-118">指定支援與 [Direct3D 12 核心](../direct3d12/core-feature-levels.md) 計算 api 搭配使用的介面卡。</span><span class="sxs-lookup"><span data-stu-id="53b59-118">Specifies an adapter that supports being used with the [Direct3D 12 Core](../direct3d12/core-feature-levels.md) compute APIs.</span></span> <span data-ttu-id="53b59-119">不保證特定功能，也不保證其目前設定中的作業系統支援這些 Api。</span><span class="sxs-lookup"><span data-stu-id="53b59-119">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="53b59-120">0x248e2800、0xa793、0x4724、0xab、0xaa、0x23、0xa6<、0xde、0x1b、0xe0、0x90</span><span class="sxs-lookup"><span data-stu-id="53b59-120">0x248e2800, 0xa793, 0x4724, 0xab, 0xaa, 0x23, 0xa6, 0xde, 0x1b, 0xe0, 0x90</span></span> |

## <a name="requirements"></a><span data-ttu-id="53b59-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="53b59-121">Requirements</span></span>

| <span data-ttu-id="53b59-122">需求</span><span class="sxs-lookup"><span data-stu-id="53b59-122">Requirement</span></span> | <span data-ttu-id="53b59-123">值</span><span class="sxs-lookup"><span data-stu-id="53b59-123">Value</span></span> |
|-|-|
| <span data-ttu-id="53b59-124">標頭</span><span class="sxs-lookup"><span data-stu-id="53b59-124">Header</span></span> | <span data-ttu-id="53b59-125">dxcore_interface。h</span><span class="sxs-lookup"><span data-stu-id="53b59-125">dxcore_interface.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="53b59-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53b59-126">See also</span></span>

* [<span data-ttu-id="53b59-127">IDXCoreAdapterFactory::CreateAdapterList</span><span class="sxs-lookup"><span data-stu-id="53b59-127">IDXCoreAdapterFactory::CreateAdapterList</span></span>](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [<span data-ttu-id="53b59-128">IDXCoreAdapter::IsAttributeSupported</span><span class="sxs-lookup"><span data-stu-id="53b59-128">IDXCoreAdapter::IsAttributeSupported</span></span>](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [<span data-ttu-id="53b59-129">DXCore 參考</span><span class="sxs-lookup"><span data-stu-id="53b59-129">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="53b59-130">使用 DXCore 來列舉介面卡</span><span class="sxs-lookup"><span data-stu-id="53b59-130">Using DXCore to enumerate adapters</span></span>](./dxcore-enum-adapters.md)
* [<span data-ttu-id="53b59-131">Direct3D 12 圖形</span><span class="sxs-lookup"><span data-stu-id="53b59-131">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)
