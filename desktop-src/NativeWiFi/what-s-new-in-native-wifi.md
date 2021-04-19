---
description: 原生 Wifi 的新功能
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: 原生 Wifi 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974584"
---
# <a name="whats-new-in-native-wifi"></a><span data-ttu-id="92f26-103">原生 Wifi 的新功能</span><span class="sxs-lookup"><span data-stu-id="92f26-103">What's New in Native Wifi</span></span>

## <a name="windows-10-version-2004"></a><span data-ttu-id="92f26-104">Windows 10 (版本 2004)</span><span class="sxs-lookup"><span data-stu-id="92f26-104">Windows 10, version 2004</span></span>

<span data-ttu-id="92f26-105">請參閱透過網站布建 [Wi-Fi 設定檔](prov-wifi-profile-via-website.md)。</span><span class="sxs-lookup"><span data-stu-id="92f26-105">See [Provision a Wi-Fi profile via a website](prov-wifi-profile-via-website.md).</span></span>

## <a name="windows-10"></a><span data-ttu-id="92f26-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="92f26-106">Windows 10</span></span>

<span data-ttu-id="92f26-107">已將對熱點2.0 的支援新增至 [WLAN \_ 設定檔架構](wlan-profileschema-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="92f26-107">Support for Hotspot 2.0 has been added to the [WLAN\_profile schema](wlan-profileschema-schema.md).</span></span> <span data-ttu-id="92f26-108">作用點2.0 可讓您使用現有的認證和服務提供者網路中的成員資格，自動連線至公用 Wi-Fi 服務。</span><span class="sxs-lookup"><span data-stu-id="92f26-108">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="92f26-109">服務提供者會指定如何使用新的架構專案來描述要使用的網路，以及如何對它們進行驗證。</span><span class="sxs-lookup"><span data-stu-id="92f26-109">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span> <span data-ttu-id="92f26-110">請參閱 [**Hotspot2**](wlan-profileschema-hotspot2-element.md) 元素檔以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="92f26-110">See the [**Hotspot2**](wlan-profileschema-hotspot2-element.md) element documentation for details.</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="92f26-111">Windows 8 與 Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92f26-111">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="92f26-112">下列功能已新增至 Windows 8 和 Windows Server 2012 上的原生 Wifi Api。</span><span class="sxs-lookup"><span data-stu-id="92f26-112">The following features have been added to the Native Wifi APIs on Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="92f26-113">Wi-Fi 直接功能，以 Wi-Fi 聯盟的 Wi-Fi 對等技術規格 v1.1 開發為基礎， (查看 [Wi-fi 同盟發佈的規格](https://www.wi-fi.org/)) 。</span><span class="sxs-lookup"><span data-stu-id="92f26-113">A Wi-Fi Direct feature based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="92f26-114">Wi-Fi 點對點技術規格的目標是要提供解決方案來 Wi-Fi 裝置到裝置的連線能力，而不需要無線存取點， (無線 AP) 設定連線或使用現有的 Wi-Fi 臨機操作 (IBSS) 機制。</span><span class="sxs-lookup"><span data-stu-id="92f26-114">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism.</span></span>

<span data-ttu-id="92f26-115">下列函數支援 Wi-Fi 直接功能。</span><span class="sxs-lookup"><span data-stu-id="92f26-115">The following functions support the Wi-Fi Direct feature.</span></span>

-   [<span data-ttu-id="92f26-116">**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="92f26-116">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [<span data-ttu-id="92f26-117">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="92f26-117">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [<span data-ttu-id="92f26-118">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="92f26-118">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [<span data-ttu-id="92f26-119">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="92f26-119">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [<span data-ttu-id="92f26-120">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="92f26-120">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [<span data-ttu-id="92f26-121">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="92f26-121">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [<span data-ttu-id="92f26-122">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="92f26-122">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [<span data-ttu-id="92f26-123">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="92f26-123">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="92f26-124">Windows 7 與 Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92f26-124">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="92f26-125">下列功能已新增至 Windows 7 和 Windows Server 2008 R2 上的原生 Wifi Api。</span><span class="sxs-lookup"><span data-stu-id="92f26-125">The following features have been added to the Native Wifi APIs on Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="92f26-126">無線裝載網路可讓單一實體的無線介面卡以用戶端的身分連線到 (AP) 的硬體存取點，同時作為軟體 AP，讓其他支援無線裝置的裝置能夠連線。</span><span class="sxs-lookup"><span data-stu-id="92f26-126">The wireless Hosted Network allows a single physical wireless adapter to connect as a client to a hardware access point (AP), while at the same time acting as a software AP allowing other wireless-capable devices to connect to it.</span></span>

<span data-ttu-id="92f26-127">下列功能支援無線裝載的網路功能。</span><span class="sxs-lookup"><span data-stu-id="92f26-127">The following functions support the wireless Hosted Network feature.</span></span>

-   [<span data-ttu-id="92f26-128">**WlanHostedNetworkForceStart**</span><span class="sxs-lookup"><span data-stu-id="92f26-128">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [<span data-ttu-id="92f26-129">**WlanHostedNetworkForceStop**</span><span class="sxs-lookup"><span data-stu-id="92f26-129">**WlanHostedNetworkForceStop**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [<span data-ttu-id="92f26-130">**WlanHostedNetworkInitSettings**</span><span class="sxs-lookup"><span data-stu-id="92f26-130">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [<span data-ttu-id="92f26-131">**WlanHostedNetworkQueryProperty**</span><span class="sxs-lookup"><span data-stu-id="92f26-131">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [<span data-ttu-id="92f26-132">**WlanHostedNetworkQuerySecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="92f26-132">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [<span data-ttu-id="92f26-133">**WlanHostedNetworkQueryStatus**</span><span class="sxs-lookup"><span data-stu-id="92f26-133">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [<span data-ttu-id="92f26-134">**WlanHostedNetworkRefreshSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="92f26-134">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [<span data-ttu-id="92f26-135">**WlanHostedNetworkSetProperty**</span><span class="sxs-lookup"><span data-stu-id="92f26-135">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [<span data-ttu-id="92f26-136">**WlanHostedNetworkSetSecondaryKey**</span><span class="sxs-lookup"><span data-stu-id="92f26-136">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [<span data-ttu-id="92f26-137">**WlanHostedNetworkStartUsing**</span><span class="sxs-lookup"><span data-stu-id="92f26-137">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [<span data-ttu-id="92f26-138">**WlanHostedNetworkStopUsing**</span><span class="sxs-lookup"><span data-stu-id="92f26-138">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [<span data-ttu-id="92f26-139">**WlanRegisterVirtualStationNotification**</span><span class="sxs-lookup"><span data-stu-id="92f26-139">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

<span data-ttu-id="92f26-140">下列可搭配無線託管網路使用的新結構。</span><span class="sxs-lookup"><span data-stu-id="92f26-140">The following new structures that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="92f26-141">**WLAN \_ 託管 \_ 網路 \_ 連線 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="92f26-141">**WLAN\_HOSTED\_NETWORK\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [<span data-ttu-id="92f26-142">**WLAN \_ HOSTED \_ NETWORK \_ 資料 \_ 對等 \_ 狀態 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="92f26-142">**WLAN\_HOSTED\_NETWORK\_DATA\_PEER\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [<span data-ttu-id="92f26-143">**WLAN \_ 託管 \_ 網路 \_ 對等 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="92f26-143">**WLAN\_HOSTED\_NETWORK\_PEER\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [<span data-ttu-id="92f26-144">**WLAN \_ HOSTED \_ NETWORK \_ 無線電 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="92f26-144">**WLAN\_HOSTED\_NETWORK\_RADIO\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [<span data-ttu-id="92f26-145">**WLAN \_ 託管 \_ 網路 \_ 安全性 \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="92f26-145">**WLAN\_HOSTED\_NETWORK\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [<span data-ttu-id="92f26-146">**WLAN \_ 託管 \_ 網路 \_ 狀態 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="92f26-146">**WLAN\_HOSTED\_NETWORK\_STATE\_CHANGE**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [<span data-ttu-id="92f26-147">**WLAN \_ 託管 \_ 網路 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="92f26-147">**WLAN\_HOSTED\_NETWORK\_STATUS**</span></span>](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

<span data-ttu-id="92f26-148">下列使用無線裝載網路的新列舉。</span><span class="sxs-lookup"><span data-stu-id="92f26-148">The following new enumerations that work with wireless Hosted Network.</span></span>

-   [<span data-ttu-id="92f26-149">**WLAN \_ 託管 \_ 網路 \_ 通知 \_ 碼**</span><span class="sxs-lookup"><span data-stu-id="92f26-149">**WLAN\_HOSTED\_NETWORK\_NOTIFICATION\_CODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [<span data-ttu-id="92f26-150">**WLAN \_ 託管 \_ 網路 \_ 操作碼**</span><span class="sxs-lookup"><span data-stu-id="92f26-150">**WLAN\_HOSTED\_NETWORK\_OPCODE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [<span data-ttu-id="92f26-151">**WLAN \_ 託管 \_ 網路 \_ 對等 \_ 驗證 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="92f26-151">**WLAN\_HOSTED\_NETWORK\_PEER\_AUTH\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [<span data-ttu-id="92f26-152">**WLAN \_ 託管 \_ 網路 \_ 原因**</span><span class="sxs-lookup"><span data-stu-id="92f26-152">**WLAN\_HOSTED\_NETWORK\_REASON**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [<span data-ttu-id="92f26-153">**WLAN \_ 託管 \_ 網路 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="92f26-153">**WLAN\_HOSTED\_NETWORK\_STATE**</span></span>](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a><span data-ttu-id="92f26-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="92f26-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92f26-155">關於無線託管網路</span><span class="sxs-lookup"><span data-stu-id="92f26-155">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="92f26-156">使用無線託管網路和網際網路連線共用</span><span class="sxs-lookup"><span data-stu-id="92f26-156">Using Wireless Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



