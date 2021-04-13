---
title: IMsRdpClientTransportSettings2 GatewayPreAuthRequirement 屬性
description: 指定或抓取遠端桌面閘道 (RD 閘道) 單次密碼 (OTP) 功能是否已啟用的設定。
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- GatewayPreAuthRequirement 屬性遠端桌面服務
- GatewayPreAuthRequirement 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayPreAuthRequirement 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509351"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a><span data-ttu-id="78f0e-106">IMsRdpClientTransportSettings2：： GatewayPreAuthRequirement 屬性</span><span class="sxs-lookup"><span data-stu-id="78f0e-106">IMsRdpClientTransportSettings2::GatewayPreAuthRequirement property</span></span>

<span data-ttu-id="78f0e-107">指定或抓取遠端桌面閘道 (RD 閘道) 單次密碼 (OTP) 功能是否已啟用的設定。</span><span class="sxs-lookup"><span data-stu-id="78f0e-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature is enabled.</span></span>

<span data-ttu-id="78f0e-108">啟用 OTP 時， **GatewayPreAuthRequirement** 會嘗試使用 [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) 屬性從網際網路 COOKIE 存放區查詢 otp cookie。</span><span class="sxs-lookup"><span data-stu-id="78f0e-108">When OTP is enabled, **GatewayPreAuthRequirement** tries to query the OTP cookie from the Internet cookie store by using the [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) property.</span></span> <span data-ttu-id="78f0e-109">如果成功， **GatewayPreAuthRequirement** 會將 OTP cookie 傳送到防火牆伺服器 (例如，Microsoft Internet Security and 加速 \[ ISA \] server) 以進行預先驗證。</span><span class="sxs-lookup"><span data-stu-id="78f0e-109">If successful, **GatewayPreAuthRequirement** sends the OTP cookie to the firewall server (such as Microsoft Internet Security and Acceleration \[ISA\] server) for pre-authentication.</span></span>

<span data-ttu-id="78f0e-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="78f0e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="78f0e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="78f0e-111">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a><span data-ttu-id="78f0e-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="78f0e-112">Property value</span></span>

<span data-ttu-id="78f0e-113">如果設定為1，則會啟用 OTP 功能。</span><span class="sxs-lookup"><span data-stu-id="78f0e-113">If set to 1, the OTP feature is enabled.</span></span> <span data-ttu-id="78f0e-114">如果設定為0，則會停用 OTP 功能。</span><span class="sxs-lookup"><span data-stu-id="78f0e-114">If set to 0, the OTP feature is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78f0e-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="78f0e-115">Error codes</span></span>

<span data-ttu-id="78f0e-116">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="78f0e-116">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="78f0e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="78f0e-117">Requirements</span></span>



| <span data-ttu-id="78f0e-118">需求</span><span class="sxs-lookup"><span data-stu-id="78f0e-118">Requirement</span></span> | <span data-ttu-id="78f0e-119">值</span><span class="sxs-lookup"><span data-stu-id="78f0e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78f0e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78f0e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="78f0e-121">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="78f0e-121">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="78f0e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78f0e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="78f0e-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78f0e-123">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="78f0e-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="78f0e-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="78f0e-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78f0e-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="78f0e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="78f0e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78f0e-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78f0e-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="78f0e-128">IID</span><span class="sxs-lookup"><span data-stu-id="78f0e-128">IID</span></span><br/>                      | <span data-ttu-id="78f0e-129">IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="78f0e-129">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78f0e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78f0e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f0e-131">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="78f0e-131">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="78f0e-132">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="78f0e-132">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





