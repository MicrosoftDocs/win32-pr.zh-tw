---
title: IMsRdpClientTransportSettings4 介面
description: 定義遠端桌面閘道 (RD 閘道) server 的其他屬性。 |IMsRdpClientTransportSettings4 介面
ms.assetid: 8b079d38-f6bc-465b-9af8-414e618f2820
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings4 介面遠端桌面服務
- IMsRdpClientTransportSettings4 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 902f04641165c5444d1a763ff9381dc9d339e924
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104514405"
---
# <a name="imsrdpclienttransportsettings4-interface"></a><span data-ttu-id="7949a-106">IMsRdpClientTransportSettings4 介面</span><span class="sxs-lookup"><span data-stu-id="7949a-106">IMsRdpClientTransportSettings4 interface</span></span>

<span data-ttu-id="7949a-107">定義遠端桌面閘道 (RD 閘道) server 的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="7949a-107">Defines additional properties for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="7949a-108">成員</span><span class="sxs-lookup"><span data-stu-id="7949a-108">Members</span></span>

<span data-ttu-id="7949a-109">**IMsRdpClientTransportSettings4** 介面繼承自 [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)。</span><span class="sxs-lookup"><span data-stu-id="7949a-109">The **IMsRdpClientTransportSettings4** interface inherits from [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md).</span></span> <span data-ttu-id="7949a-110">**IMsRdpClientTransportSettings4** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7949a-110">**IMsRdpClientTransportSettings4** also has these types of members:</span></span>

-   [<span data-ttu-id="7949a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="7949a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7949a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7949a-112">Properties</span></span>

<span data-ttu-id="7949a-113">**IMsRdpClientTransportSettings4** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7949a-113">The **IMsRdpClientTransportSettings4** interface has these properties.</span></span>



| <span data-ttu-id="7949a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="7949a-114">Property</span></span>                                                                                       | <span data-ttu-id="7949a-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="7949a-115">Access type</span></span>           | <span data-ttu-id="7949a-116">Description</span><span class="sxs-lookup"><span data-stu-id="7949a-116">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------|
| [<span data-ttu-id="7949a-117">**GatewayBrokeringType**</span><span class="sxs-lookup"><span data-stu-id="7949a-117">**GatewayBrokeringType**</span></span>](imsrdpclienttransportsettings4-gatewaybrokeringtype.md)<br/> | <span data-ttu-id="7949a-118">唯寫</span><span class="sxs-lookup"><span data-stu-id="7949a-118">Write-only</span></span><br/> | <span data-ttu-id="7949a-119">取得和設定閘道代理類型。</span><span class="sxs-lookup"><span data-stu-id="7949a-119">Gets and sets the gateway brokering type.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7949a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="7949a-120">Requirements</span></span>



| <span data-ttu-id="7949a-121">需求</span><span class="sxs-lookup"><span data-stu-id="7949a-121">Requirement</span></span> | <span data-ttu-id="7949a-122">值</span><span class="sxs-lookup"><span data-stu-id="7949a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7949a-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7949a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7949a-124">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7949a-124">Windows 8.1</span></span><br/>                                                                            |
| <span data-ttu-id="7949a-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7949a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7949a-126">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7949a-126">Windows Server 2012 R2</span></span><br/>                                                                 |
| <span data-ttu-id="7949a-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="7949a-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="7949a-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7949a-128"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="7949a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7949a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7949a-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7949a-130"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="7949a-131">IID</span><span class="sxs-lookup"><span data-stu-id="7949a-131">IID</span></span><br/>                      | <span data-ttu-id="7949a-132">IID \_ IMsRdpClientTransportSettings4 定義為011C3236-4D81-4515-9143-067AB630D299</span><span class="sxs-lookup"><span data-stu-id="7949a-132">IID\_IMsRdpClientTransportSettings4 is defined as 011C3236-4D81-4515-9143-067AB630D299</span></span><br/> |



 

 





