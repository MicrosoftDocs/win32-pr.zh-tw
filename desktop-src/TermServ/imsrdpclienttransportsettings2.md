---
title: IMsRdpClientTransportSettings2 介面
description: 管理遠端桌面閘道 (RD 閘道) server 的用戶端傳輸設定。 |IMsRdpClientTransportSettings2 介面
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings2 介面遠端桌面服務
- IMsRdpClientTransportSettings2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106975620"
---
# <a name="imsrdpclienttransportsettings2-interface"></a><span data-ttu-id="13f1f-106">IMsRdpClientTransportSettings2 介面</span><span class="sxs-lookup"><span data-stu-id="13f1f-106">IMsRdpClientTransportSettings2 interface</span></span>

<span data-ttu-id="13f1f-107">管理遠端桌面閘道 (RD 閘道) server 的用戶端傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="13f1f-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="13f1f-108">成員</span><span class="sxs-lookup"><span data-stu-id="13f1f-108">Members</span></span>

<span data-ttu-id="13f1f-109">**IMsRdpClientTransportSettings2** 介面繼承自 [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)。</span><span class="sxs-lookup"><span data-stu-id="13f1f-109">The **IMsRdpClientTransportSettings2** interface inherits from [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span></span> <span data-ttu-id="13f1f-110">**IMsRdpClientTransportSettings2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="13f1f-110">**IMsRdpClientTransportSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="13f1f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="13f1f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13f1f-112">屬性</span><span class="sxs-lookup"><span data-stu-id="13f1f-112">Properties</span></span>

<span data-ttu-id="13f1f-113">**IMsRdpClientTransportSettings2** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="13f1f-113">The **IMsRdpClientTransportSettings2** interface has these properties.</span></span>



| <span data-ttu-id="13f1f-114">屬性</span><span class="sxs-lookup"><span data-stu-id="13f1f-114">Property</span></span>                                                                                                    | <span data-ttu-id="13f1f-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="13f1f-115">Access type</span></span>           | <span data-ttu-id="13f1f-116">Description</span><span class="sxs-lookup"><span data-stu-id="13f1f-116">Description</span></span>                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13f1f-117">**GatewayCredSharing**</span><span class="sxs-lookup"><span data-stu-id="13f1f-117">**GatewayCredSharing**</span></span>](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | <span data-ttu-id="13f1f-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13f1f-118">Read/write</span></span><br/> | <span data-ttu-id="13f1f-119">指出是否已啟用 RD 閘道的單一登入功能。</span><span class="sxs-lookup"><span data-stu-id="13f1f-119">Indicates whether the single sign-on feature for RD Gateway is enabled.</span></span><br/>                |
| [<span data-ttu-id="13f1f-120">**GatewayDomain**</span><span class="sxs-lookup"><span data-stu-id="13f1f-120">**GatewayDomain**</span></span>](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | <span data-ttu-id="13f1f-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13f1f-121">Read/write</span></span><br/> | <span data-ttu-id="13f1f-122">使用者為了連接到 RD 閘道伺服器所提供的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="13f1f-122">The domain name that a user provides to connect to the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="13f1f-123">**GatewayEncryptedOtpCookie**</span><span class="sxs-lookup"><span data-stu-id="13f1f-123">**GatewayEncryptedOtpCookie**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | <span data-ttu-id="13f1f-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13f1f-124">Read/write</span></span><br/> | <span data-ttu-id="13f1f-125">加密的 OTP cookie。</span><span class="sxs-lookup"><span data-stu-id="13f1f-125">The encrypted OTP cookie.</span></span><br/>                                                              |
| [<span data-ttu-id="13f1f-126">**GatewayEncryptedOtpCookieSize**</span><span class="sxs-lookup"><span data-stu-id="13f1f-126">**GatewayEncryptedOtpCookieSize**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | <span data-ttu-id="13f1f-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13f1f-127">Read/write</span></span><br/> | <span data-ttu-id="13f1f-128">加密 OTP cookie 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="13f1f-128">The size, in bytes, of the encrypted OTP cookie.</span></span><br/>                                       |
| [<span data-ttu-id="13f1f-129">**GatewayPassword**</span><span class="sxs-lookup"><span data-stu-id="13f1f-129">**GatewayPassword**</span></span>](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | <span data-ttu-id="13f1f-130">唯寫</span><span class="sxs-lookup"><span data-stu-id="13f1f-130">Write-only</span></span><br/> | <span data-ttu-id="13f1f-131">使用者為了連接到 RD 閘道伺服器所提供的密碼。</span><span class="sxs-lookup"><span data-stu-id="13f1f-131">The password that a user provides to connect to the RD Gateway server.</span></span><br/>                 |
| [<span data-ttu-id="13f1f-132">**GatewayPreAuthRequirement**</span><span class="sxs-lookup"><span data-stu-id="13f1f-132">**GatewayPreAuthRequirement**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | <span data-ttu-id="13f1f-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13f1f-133">Read/write</span></span><br/> | <span data-ttu-id="13f1f-134">指出是否已啟用 RD 閘道一次性密碼 (OTP) 功能。</span><span class="sxs-lookup"><span data-stu-id="13f1f-134">Indicates whether the RD Gateway one-time password (OTP) feature is enabled.</span></span><br/>           |
| [<span data-ttu-id="13f1f-135">**GatewayPreAuthServerAddr**</span><span class="sxs-lookup"><span data-stu-id="13f1f-135">**GatewayPreAuthServerAddr**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | <span data-ttu-id="13f1f-136">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13f1f-136">Read/write</span></span><br/> | <span data-ttu-id="13f1f-137">預先驗證服務器的網路位址。</span><span class="sxs-lookup"><span data-stu-id="13f1f-137">The web address of the pre-authentication server.</span></span><br/>                                      |
| [<span data-ttu-id="13f1f-138">**GatewaySupportUrl**</span><span class="sxs-lookup"><span data-stu-id="13f1f-138">**GatewaySupportUrl**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | <span data-ttu-id="13f1f-139">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13f1f-139">Read/write</span></span><br/> | <span data-ttu-id="13f1f-140">提供 RD 閘道 server 技術支援的網站網址。</span><span class="sxs-lookup"><span data-stu-id="13f1f-140">The web address of the site that provides technical support for the RD Gateway server.</span></span><br/> |
| [<span data-ttu-id="13f1f-141">**GatewayUsername**</span><span class="sxs-lookup"><span data-stu-id="13f1f-141">**GatewayUsername**</span></span>](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | <span data-ttu-id="13f1f-142">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13f1f-142">Read/write</span></span><br/> | <span data-ttu-id="13f1f-143">使用者為了連接到 RD 閘道伺服器所提供的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="13f1f-143">The user name that a user provides to connect to the RD Gateway server.</span></span><br/>                |



 

## <a name="requirements"></a><span data-ttu-id="13f1f-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="13f1f-144">Requirements</span></span>



| <span data-ttu-id="13f1f-145">需求</span><span class="sxs-lookup"><span data-stu-id="13f1f-145">Requirement</span></span> | <span data-ttu-id="13f1f-146">值</span><span class="sxs-lookup"><span data-stu-id="13f1f-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f1f-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13f1f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="13f1f-148">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="13f1f-148">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="13f1f-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13f1f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="13f1f-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13f1f-150">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="13f1f-151">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="13f1f-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="13f1f-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13f1f-152"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="13f1f-153">DLL</span><span class="sxs-lookup"><span data-stu-id="13f1f-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13f1f-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13f1f-154"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="13f1f-155">IID</span><span class="sxs-lookup"><span data-stu-id="13f1f-155">IID</span></span><br/>                      | <span data-ttu-id="13f1f-156">IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="13f1f-156">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="13f1f-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13f1f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f1f-158">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="13f1f-158">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





