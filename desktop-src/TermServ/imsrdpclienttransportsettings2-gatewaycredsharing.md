---
title: IMsRdpClientTransportSettings2 GatewayCredSharing 屬性
description: 指定或抓取遠端桌面閘道 (RD 閘道) 認證共用功能是否已啟用的設定。
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- GatewayCredSharing 屬性遠端桌面服務
- GatewayCredSharing 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayCredSharing 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464581"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a><span data-ttu-id="66966-106">IMsRdpClientTransportSettings2：： GatewayCredSharing 屬性</span><span class="sxs-lookup"><span data-stu-id="66966-106">IMsRdpClientTransportSettings2::GatewayCredSharing property</span></span>

<span data-ttu-id="66966-107">指定或抓取遠端桌面閘道 (RD 閘道) 認證共用功能是否已啟用的設定。</span><span class="sxs-lookup"><span data-stu-id="66966-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) credential sharing feature is enabled.</span></span> <span data-ttu-id="66966-108">啟用此功能時，遠端桌面 ActiveX 控制項會嘗試使用相同的認證來驗證遠端桌面工作階段主機 (RD 工作階段主機) 伺服器和 RD 閘道伺服器。</span><span class="sxs-lookup"><span data-stu-id="66966-108">When the feature is enabled, the Remote Desktop ActiveX control tries to use the same credentials to authenticate to the Remote Desktop Session Host (RD Session Host) server and to the RD Gateway server.</span></span>

<span data-ttu-id="66966-109">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="66966-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="66966-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="66966-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a><span data-ttu-id="66966-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="66966-111">Property value</span></span>

<span data-ttu-id="66966-112">如果設定為1，則會啟用認證共用。</span><span class="sxs-lookup"><span data-stu-id="66966-112">If set to one, credential sharing is enabled.</span></span> <span data-ttu-id="66966-113">如果設定為零，則會停用認證共用。</span><span class="sxs-lookup"><span data-stu-id="66966-113">If set to zero, credential sharing is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66966-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="66966-114">Error codes</span></span>

<span data-ttu-id="66966-115">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="66966-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="66966-116">備註</span><span class="sxs-lookup"><span data-stu-id="66966-116">Remarks</span></span>

<span data-ttu-id="66966-117">ActiveX 控制項會使用這個屬性來執行 RD 工作階段主機伺服器與 RD 閘道伺服器之間共用認證的單一提示。</span><span class="sxs-lookup"><span data-stu-id="66966-117">This property is used by the ActiveX control to implement a single prompt for credential sharing between the RD Session Host server and the RD Gateway server.</span></span> <span data-ttu-id="66966-118">認證共用不支援使用 [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) 或 [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)的 web 密碼共用。</span><span class="sxs-lookup"><span data-stu-id="66966-118">Credential sharing does not support web-based password sharing with [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) or [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66966-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="66966-119">Requirements</span></span>



| <span data-ttu-id="66966-120">需求</span><span class="sxs-lookup"><span data-stu-id="66966-120">Requirement</span></span> | <span data-ttu-id="66966-121">值</span><span class="sxs-lookup"><span data-stu-id="66966-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66966-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66966-122">Minimum supported client</span></span><br/> | <span data-ttu-id="66966-123">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="66966-123">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="66966-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66966-124">Minimum supported server</span></span><br/> | <span data-ttu-id="66966-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66966-125">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="66966-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="66966-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="66966-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66966-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="66966-128">DLL</span><span class="sxs-lookup"><span data-stu-id="66966-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66966-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66966-129"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="66966-130">IID</span><span class="sxs-lookup"><span data-stu-id="66966-130">IID</span></span><br/>                      | <span data-ttu-id="66966-131">IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="66966-131">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66966-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66966-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66966-133">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="66966-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="66966-134">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="66966-134">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





