---
title: IMsRdpClientTransportSettings2 GatewayPreAuthServerAddr 屬性
description: 指定或抓取預先驗證服務器的網址，此位址用於遠端桌面閘道 (RD 閘道) 單次密碼 (OTP) 功能。
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- GatewayPreAuthServerAddr 屬性遠端桌面服務
- GatewayPreAuthServerAddr 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayPreAuthServerAddr 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384165"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a><span data-ttu-id="363fd-106">IMsRdpClientTransportSettings2：： GatewayPreAuthServerAddr 屬性</span><span class="sxs-lookup"><span data-stu-id="363fd-106">IMsRdpClientTransportSettings2::GatewayPreAuthServerAddr property</span></span>

<span data-ttu-id="363fd-107">指定或抓取預先驗證服務器的網址，此位址用於遠端桌面閘道 (RD 閘道) 單次密碼 (OTP) 功能。</span><span class="sxs-lookup"><span data-stu-id="363fd-107">Specifies or retrieves the web address of the pre-authentication server, which is used for the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature.</span></span>

<span data-ttu-id="363fd-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="363fd-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="363fd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="363fd-109">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="363fd-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="363fd-110">Property value</span></span>

<span data-ttu-id="363fd-111">預先驗證服務器的網址：例如，Microsoft Internet Security and 加速 (ISA) server 的網址。</span><span class="sxs-lookup"><span data-stu-id="363fd-111">The web address of the pre-authentication server; for example, the web address of the Microsoft Internet Security and Acceleration (ISA) server.</span></span> <span data-ttu-id="363fd-112">使用「HTTPs://*主機名稱*」的格式來指定網址。*DomainName*.Com/*>websitename*"或" HTTPs://*HostName*。*DomainName*.Com/*>websitename*"。</span><span class="sxs-lookup"><span data-stu-id="363fd-112">Specify the web address by using the format "https://*HostName*.*DomainName*.com/*WebsiteName*" or "https://*HostName*.*DomainName*.com/*WebsiteName*".</span></span>

## <a name="error-codes"></a><span data-ttu-id="363fd-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="363fd-113">Error codes</span></span>

<span data-ttu-id="363fd-114">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="363fd-114">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="363fd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="363fd-115">Requirements</span></span>



| <span data-ttu-id="363fd-116">需求</span><span class="sxs-lookup"><span data-stu-id="363fd-116">Requirement</span></span> | <span data-ttu-id="363fd-117">值</span><span class="sxs-lookup"><span data-stu-id="363fd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="363fd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="363fd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="363fd-119">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="363fd-119">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="363fd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="363fd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="363fd-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="363fd-121">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="363fd-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="363fd-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="363fd-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="363fd-123"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="363fd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="363fd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="363fd-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="363fd-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="363fd-126">IID</span><span class="sxs-lookup"><span data-stu-id="363fd-126">IID</span></span><br/>                      | <span data-ttu-id="363fd-127">IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="363fd-127">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="363fd-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="363fd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363fd-129">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="363fd-129">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="363fd-130">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="363fd-130">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





