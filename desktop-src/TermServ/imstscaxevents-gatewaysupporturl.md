---
title: IMsRdpClientTransportSettings2 GatewaySupportUrl 屬性
description: 指定或抓取網站的網址，該網站提供此遠端桌面閘道 (RD 閘道) server 的技術支援。
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- GatewaySupportUrl 屬性遠端桌面服務
- GatewaySupportUrl 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewaySupportUrl 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4212dd03d5fb217753e14c2869973bda87476367
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384162"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a><span data-ttu-id="5937e-106">IMsRdpClientTransportSettings2：： GatewaySupportUrl 屬性</span><span class="sxs-lookup"><span data-stu-id="5937e-106">IMsRdpClientTransportSettings2::GatewaySupportUrl property</span></span>

<span data-ttu-id="5937e-107">指定或抓取網站的網址，該網站提供此遠端桌面閘道 (RD 閘道) server 的技術支援。</span><span class="sxs-lookup"><span data-stu-id="5937e-107">Specifies or retrieves the web address of the site that provides technical support for this Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="5937e-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5937e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5937e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5937e-109">Syntax</span></span>


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a><span data-ttu-id="5937e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="5937e-110">Property value</span></span>

<span data-ttu-id="5937e-111">指定或抓取提供此 RD 閘道 server 技術支援的網站網址。</span><span class="sxs-lookup"><span data-stu-id="5937e-111">Specifies or retrieves the web address of the site that provides technical support for this RD Gateway server.</span></span>

## <a name="requirements"></a><span data-ttu-id="5937e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5937e-112">Requirements</span></span>



| <span data-ttu-id="5937e-113">需求</span><span class="sxs-lookup"><span data-stu-id="5937e-113">Requirement</span></span> | <span data-ttu-id="5937e-114">值</span><span class="sxs-lookup"><span data-stu-id="5937e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5937e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5937e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5937e-116">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="5937e-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="5937e-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5937e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5937e-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5937e-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="5937e-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5937e-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="5937e-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5937e-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="5937e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5937e-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5937e-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5937e-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="5937e-123">IID</span><span class="sxs-lookup"><span data-stu-id="5937e-123">IID</span></span><br/>                      | <span data-ttu-id="5937e-124">IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="5937e-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5937e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5937e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5937e-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="5937e-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="5937e-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="5937e-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





