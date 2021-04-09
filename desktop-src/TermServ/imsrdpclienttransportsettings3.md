---
title: IMsRdpClientTransportSettings3 介面
description: 定義遠端桌面閘道 (RD 閘道) server 的其他屬性。 |IMsRdpClientTransportSettings3 介面
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings3 介面遠端桌面服務
- IMsRdpClientTransportSettings3 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7498db4b39a4ad0e89761cbec439895e4e9a152
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853639"
---
# <a name="imsrdpclienttransportsettings3-interface"></a><span data-ttu-id="6441a-106">IMsRdpClientTransportSettings3 介面</span><span class="sxs-lookup"><span data-stu-id="6441a-106">IMsRdpClientTransportSettings3 interface</span></span>

<span data-ttu-id="6441a-107">定義遠端桌面閘道 (RD 閘道) server 的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="6441a-107">Defines additional properties for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="6441a-108">成員</span><span class="sxs-lookup"><span data-stu-id="6441a-108">Members</span></span>

<span data-ttu-id="6441a-109">**IMsRdpClientTransportSettings3** 介面繼承自 [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)。</span><span class="sxs-lookup"><span data-stu-id="6441a-109">The **IMsRdpClientTransportSettings3** interface inherits from [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span></span> <span data-ttu-id="6441a-110">**IMsRdpClientTransportSettings3** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6441a-110">**IMsRdpClientTransportSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="6441a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6441a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6441a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="6441a-112">Properties</span></span>

<span data-ttu-id="6441a-113">**IMsRdpClientTransportSettings3** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6441a-113">The **IMsRdpClientTransportSettings3** interface has these properties.</span></span>



| <span data-ttu-id="6441a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="6441a-114">Property</span></span>                                                                                                           | <span data-ttu-id="6441a-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="6441a-115">Access type</span></span>           | <span data-ttu-id="6441a-116">Description</span><span class="sxs-lookup"><span data-stu-id="6441a-116">Description</span></span>                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6441a-117">**GatewayAuthCookieServerAddr**</span><span class="sxs-lookup"><span data-stu-id="6441a-117">**GatewayAuthCookieServerAddr**</span></span>](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | <span data-ttu-id="6441a-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6441a-118">Read/write</span></span><br/> | <span data-ttu-id="6441a-119">以 cookie 為基礎的驗證的伺服器位址。</span><span class="sxs-lookup"><span data-stu-id="6441a-119">The server address for cookie-based authentication.</span></span><br/>                                                                                       |
| [<span data-ttu-id="6441a-120">**GatewayAuthLoginPage**</span><span class="sxs-lookup"><span data-stu-id="6441a-120">**GatewayAuthLoginPage**</span></span>](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | <span data-ttu-id="6441a-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6441a-121">Read/write</span></span><br/> | <span data-ttu-id="6441a-122">用來驗證使用者的登入網頁位址。</span><span class="sxs-lookup"><span data-stu-id="6441a-122">The address of the login webpage to use to authenticate a user.</span></span><br/>                                                                           |
| [<span data-ttu-id="6441a-123">**GatewayCredSourceCookie**</span><span class="sxs-lookup"><span data-stu-id="6441a-123">**GatewayCredSourceCookie**</span></span>](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | <span data-ttu-id="6441a-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6441a-124">Read/write</span></span><br/> | <span data-ttu-id="6441a-125">指定認證來源是否以 cookie 為基礎。</span><span class="sxs-lookup"><span data-stu-id="6441a-125">Specifies if the credential source is cookie based.</span></span><br/>                                                                                       |
| [<span data-ttu-id="6441a-126">**GatewayEncryptedAuthCookie**</span><span class="sxs-lookup"><span data-stu-id="6441a-126">**GatewayEncryptedAuthCookie**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | <span data-ttu-id="6441a-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6441a-127">Read/write</span></span><br/> | <span data-ttu-id="6441a-128">加密的驗證 cookie。</span><span class="sxs-lookup"><span data-stu-id="6441a-128">The encrypted authentication cookie.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="6441a-129">**GatewayEncryptedAuthCookieSize**</span><span class="sxs-lookup"><span data-stu-id="6441a-129">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | <span data-ttu-id="6441a-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6441a-130">Read/write</span></span><br/> | <span data-ttu-id="6441a-131">[**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)屬性的大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6441a-131">The size, in characters, of the [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6441a-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="6441a-132">Requirements</span></span>



| <span data-ttu-id="6441a-133">需求</span><span class="sxs-lookup"><span data-stu-id="6441a-133">Requirement</span></span> | <span data-ttu-id="6441a-134">值</span><span class="sxs-lookup"><span data-stu-id="6441a-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6441a-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6441a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6441a-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6441a-136">Windows 7</span></span><br/>                                                                              |
| <span data-ttu-id="6441a-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6441a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6441a-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6441a-138">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="6441a-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6441a-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="6441a-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6441a-140"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="6441a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6441a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6441a-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6441a-142"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="6441a-143">IID</span><span class="sxs-lookup"><span data-stu-id="6441a-143">IID</span></span><br/>                      | <span data-ttu-id="6441a-144">IID \_ IMsRdpClientTransportSettings3 定義為3D5B21AC-748D-41DE-8F30-E15169586BD4</span><span class="sxs-lookup"><span data-stu-id="6441a-144">IID\_IMsRdpClientTransportSettings3 is defined as 3D5B21AC-748D-41DE-8F30-E15169586BD4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6441a-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6441a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6441a-146">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="6441a-146">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





