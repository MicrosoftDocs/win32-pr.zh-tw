---
title: IMsRdpClientTransportSettings 介面
description: 管理遠端桌面閘道 (RD 閘道) server 的用戶端傳輸設定。 |IMsRdpClientTransportSettings 介面
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- IMsRdpClientTransportSettings 介面遠端桌面服務
- IMsRdpClientTransportSettings 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec240d008ef2f9469fb67f4041cfb33c08383079
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974791"
---
# <a name="imsrdpclienttransportsettings-interface"></a><span data-ttu-id="58343-106">IMsRdpClientTransportSettings 介面</span><span class="sxs-lookup"><span data-stu-id="58343-106">IMsRdpClientTransportSettings interface</span></span>

<span data-ttu-id="58343-107">管理遠端桌面閘道 (RD 閘道) server 的用戶端傳輸設定。</span><span class="sxs-lookup"><span data-stu-id="58343-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="58343-108">成員</span><span class="sxs-lookup"><span data-stu-id="58343-108">Members</span></span>

<span data-ttu-id="58343-109">**IMsRdpClientTransportSettings** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="58343-109">The **IMsRdpClientTransportSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="58343-110">**IMsRdpClientTransportSettings** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="58343-110">**IMsRdpClientTransportSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="58343-111">屬性</span><span class="sxs-lookup"><span data-stu-id="58343-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58343-112">屬性</span><span class="sxs-lookup"><span data-stu-id="58343-112">Properties</span></span>

<span data-ttu-id="58343-113">**IMsRdpClientTransportSettings** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="58343-113">The **IMsRdpClientTransportSettings** interface has these properties.</span></span>



| <span data-ttu-id="58343-114">屬性</span><span class="sxs-lookup"><span data-stu-id="58343-114">Property</span></span>                                                                                                          | <span data-ttu-id="58343-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="58343-115">Access type</span></span>           | <span data-ttu-id="58343-116">Description</span><span class="sxs-lookup"><span data-stu-id="58343-116">Description</span></span>                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [<span data-ttu-id="58343-117">**GatewayCredsSource**</span><span class="sxs-lookup"><span data-stu-id="58343-117">**GatewayCredsSource**</span></span>](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | <span data-ttu-id="58343-118">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="58343-118">Read/write</span></span><br/> | <span data-ttu-id="58343-119">RD 閘道伺服器驗證方法。</span><span class="sxs-lookup"><span data-stu-id="58343-119">The RD Gateway server authentication method.</span></span><br/>     |
| [<span data-ttu-id="58343-120">**GatewayDefaultUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="58343-120">**GatewayDefaultUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | <span data-ttu-id="58343-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="58343-121">Read-only</span></span><br/>  | <span data-ttu-id="58343-122">預設的 RD 閘道使用方法。</span><span class="sxs-lookup"><span data-stu-id="58343-122">The default RD Gateway usage method.</span></span><br/>             |
| [<span data-ttu-id="58343-123">**GatewayHostname**</span><span class="sxs-lookup"><span data-stu-id="58343-123">**GatewayHostname**</span></span>](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | <span data-ttu-id="58343-124">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="58343-124">Read/write</span></span><br/> | <span data-ttu-id="58343-125">RD 閘道伺服器的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="58343-125">Host name of the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="58343-126">**GatewayIsSupported**</span><span class="sxs-lookup"><span data-stu-id="58343-126">**GatewayIsSupported**</span></span>](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | <span data-ttu-id="58343-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="58343-127">Read-only</span></span><br/>  | <span data-ttu-id="58343-128">指出是否支援 RD 閘道。</span><span class="sxs-lookup"><span data-stu-id="58343-128">Indicates whether RD Gateway is supported.</span></span><br/>       |
| [<span data-ttu-id="58343-129">**GatewayProfileUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="58343-129">**GatewayProfileUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | <span data-ttu-id="58343-130">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="58343-130">Read/write</span></span><br/> | <span data-ttu-id="58343-131">RD 閘道設定檔使用方法。</span><span class="sxs-lookup"><span data-stu-id="58343-131">The RD Gateway profile usage method.</span></span><br/>             |
| [<span data-ttu-id="58343-132">**GatewayUsageMethod**</span><span class="sxs-lookup"><span data-stu-id="58343-132">**GatewayUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | <span data-ttu-id="58343-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="58343-133">Read/write</span></span><br/> | <span data-ttu-id="58343-134">RD 閘道伺服器使用方法。</span><span class="sxs-lookup"><span data-stu-id="58343-134">The RD Gateway server usage method.</span></span><br/>              |
| [<span data-ttu-id="58343-135">**GatewayUserSelectedCredsSource**</span><span class="sxs-lookup"><span data-stu-id="58343-135">**GatewayUserSelectedCredsSource**</span></span>](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | <span data-ttu-id="58343-136">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="58343-136">Read/write</span></span><br/> | <span data-ttu-id="58343-137">使用者指定的 RD 閘道認證來源。</span><span class="sxs-lookup"><span data-stu-id="58343-137">The user-specified RD Gateway credential source.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="58343-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="58343-138">Requirements</span></span>



| <span data-ttu-id="58343-139">需求</span><span class="sxs-lookup"><span data-stu-id="58343-139">Requirement</span></span> | <span data-ttu-id="58343-140">值</span><span class="sxs-lookup"><span data-stu-id="58343-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58343-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58343-141">Minimum supported client</span></span><br/> | <span data-ttu-id="58343-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58343-142">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="58343-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58343-143">Minimum supported server</span></span><br/> | <span data-ttu-id="58343-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58343-144">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="58343-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="58343-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="58343-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58343-146"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="58343-147">DLL</span><span class="sxs-lookup"><span data-stu-id="58343-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58343-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58343-148"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="58343-149">IID</span><span class="sxs-lookup"><span data-stu-id="58343-149">IID</span></span><br/>                      | <span data-ttu-id="58343-150">IID \_ IMsRdpClientTransportSettings 定義為720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="58343-150">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58343-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58343-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58343-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="58343-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="58343-153">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="58343-153">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="58343-154">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="58343-154">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

