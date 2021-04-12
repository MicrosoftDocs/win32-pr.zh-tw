---
title: Windows 篩選平台的新功能
description: Windows 8 和 Windows Server 2012 引進了新的 Windows 篩選平台程式設計項目。
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104316927"
---
# <a name="whats-new-in-windows-filtering-platform"></a><span data-ttu-id="6c5cd-103">Windows 篩選平台的新功能</span><span class="sxs-lookup"><span data-stu-id="6c5cd-103">What's New in Windows Filtering Platform</span></span>

<span data-ttu-id="6c5cd-104">Windows 8 和 Windows Server 2012 引進了新的 Windows 篩選平台程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="6c5cd-104">Windows 8 and Windows Server 2012 introduce new Windows Filtering Platform programming elements.</span></span> <span data-ttu-id="6c5cd-105">新功能包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="6c5cd-105">New functionality includes the following:</span></span>

-   <span data-ttu-id="6c5cd-106">*第2層篩選*：提供對 L2 (MAC) 層的存取權，以允許篩選該層的流量。</span><span class="sxs-lookup"><span data-stu-id="6c5cd-106">*Layer 2 filtering*: Provides access to the L2 (MAC) layer, allowing filtering of traffic at that layer.</span></span>
-   <span data-ttu-id="6c5cd-107">*vSwitch 篩選*：允許對 vSwitch 進行檢查及/或修改的封包。</span><span class="sxs-lookup"><span data-stu-id="6c5cd-107">*vSwitch filtering*: Allows packets traversing a vSwitch to be inspected and/or modified.</span></span> <span data-ttu-id="6c5cd-108">您可以在 vSwitch 輸入和輸出中使用 WFP 篩選器或標注。</span><span class="sxs-lookup"><span data-stu-id="6c5cd-108">WFP filters or callouts can be used at the vSwitch ingress and egress.</span></span>
-   <span data-ttu-id="6c5cd-109">*應用程式容器管理*：允許存取應用程式容器和網路隔離連線問題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6c5cd-109">*App container management*: Allows access to information about app containers and network isolation connectivity issues.</span></span>
-   <span data-ttu-id="6c5cd-110">*Ipsec 更新*：延伸的 ipsec 功能，包括線上狀態監視、憑證選取和金鑰管理。</span><span class="sxs-lookup"><span data-stu-id="6c5cd-110">*IPsec updates*: Extended IPsec functionality including connection state monitoring, certificate selection, and key management.</span></span>

<span data-ttu-id="6c5cd-111">Windows 驅動程式套件也包含 [Windows 8 之 WFP 變更的](/windows-hardware/drivers/network/wfp-changes-for-windows-8)相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6c5cd-111">The Windows Driver Kit also includes information on [WFP Changes for Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).</span></span>

## <a name="windows-8-api-updates"></a><span data-ttu-id="6c5cd-112">Windows 8 API 更新</span><span class="sxs-lookup"><span data-stu-id="6c5cd-112">Windows 8 API updates</span></span>

<span data-ttu-id="6c5cd-113">已針對 Windows 8 和 Windows Server 2012 新增許多新的 Api。</span><span class="sxs-lookup"><span data-stu-id="6c5cd-113">Many new APIs have been added for Windows 8 and Windows Server 2012.</span></span>

## <a name="new-functions"></a><span data-ttu-id="6c5cd-114">新的函式</span><span class="sxs-lookup"><span data-stu-id="6c5cd-114">New functions</span></span>

-   [<span data-ttu-id="6c5cd-115">**FWPM \_ NET \_ EVENT \_ CALLBACK1**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-115">**FWPM\_NET\_EVENT\_CALLBACK1**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [<span data-ttu-id="6c5cd-116">**FwpmConnectionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-116">**FwpmConnectionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [<span data-ttu-id="6c5cd-117">**FwpmConnectionDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-117">**FwpmConnectionDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [<span data-ttu-id="6c5cd-118">**FwpmConnectionEnum0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-118">**FwpmConnectionEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [<span data-ttu-id="6c5cd-119">**FwpmConnectionGetById0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-119">**FwpmConnectionGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [<span data-ttu-id="6c5cd-120">**FwpmConnectionGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-120">**FwpmConnectionGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [<span data-ttu-id="6c5cd-121">**FwpmConnectionSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-121">**FwpmConnectionSetSecurityInfo0**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [<span data-ttu-id="6c5cd-122">**FwpmConnectionSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-122">**FwpmConnectionSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [<span data-ttu-id="6c5cd-123">**FwpmConnectionSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-123">**FwpmConnectionSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [<span data-ttu-id="6c5cd-124">**FwpmConnectionUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-124">**FwpmConnectionUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [<span data-ttu-id="6c5cd-125">**FwpmIPsecTunnelAdd2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-125">**FwpmIPsecTunnelAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [<span data-ttu-id="6c5cd-126">**FwpmNetEventEnum2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-126">**FwpmNetEventEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [<span data-ttu-id="6c5cd-127">**FwpmNetEventSubscribe1**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-127">**FwpmNetEventSubscribe1**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [<span data-ttu-id="6c5cd-128">**FwpmProviderCoNtextAdd2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-128">**FwpmProviderContextAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [<span data-ttu-id="6c5cd-129">**FwpmProviderCoNtextEnum2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-129">**FwpmProviderContextEnum2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [<span data-ttu-id="6c5cd-130">**FwpmProviderCoNtextGetById2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-130">**FwpmProviderContextGetById2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [<span data-ttu-id="6c5cd-131">**FwpmProviderCoNtextGetByKey2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-131">**FwpmProviderContextGetByKey2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [<span data-ttu-id="6c5cd-132">**FwpmvSwitchEventsGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-132">**FwpmvSwitchEventsGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [<span data-ttu-id="6c5cd-133">**FwpmvSwitchEventsSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-133">**FwpmvSwitchEventsSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [<span data-ttu-id="6c5cd-134">**FwpmvSwitchEventSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-134">**FwpmvSwitchEventSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [<span data-ttu-id="6c5cd-135">**FwpmvSwitchEventUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-135">**FwpmvSwitchEventUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [<span data-ttu-id="6c5cd-136">**IkeextSaEnum2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-136">**IkeextSaEnum2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [<span data-ttu-id="6c5cd-137">**IkeextSaGetById2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-137">**IkeextSaGetById2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [<span data-ttu-id="6c5cd-138">**IPSEC \_ 金鑰 \_ 管理員 \_ 按鍵 \_ 聽寫 \_ CHECK0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-138">**IPSEC\_KEY\_MANAGER\_KEY\_DICTATION\_CHECK0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [<span data-ttu-id="6c5cd-139">**IPSEC \_ 金鑰 \_ 管理員會 \_ 聽寫 \_ KEY0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-139">**IPSEC\_KEY\_MANAGER\_DICTATE\_KEY0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [<span data-ttu-id="6c5cd-140">**IPSEC \_ 金鑰 \_ 管理員 \_ 通知 \_ KEY0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-140">**IPSEC\_KEY\_MANAGER\_NOTIFY\_KEY0**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [<span data-ttu-id="6c5cd-141">**IPSEC \_ SA \_ 內容 \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-141">**IPSEC\_SA\_CONTEXT\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [<span data-ttu-id="6c5cd-142">**IPsecKeyManagerAddAndRegister0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-142">**IPsecKeyManagerAddAndRegister0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [<span data-ttu-id="6c5cd-143">**IPsecKeyManagerGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-143">**IPsecKeyManagerGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [<span data-ttu-id="6c5cd-144">**IPsecKeyManagerSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-144">**IPsecKeyManagerSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [<span data-ttu-id="6c5cd-145">**IPsecKeyManagersGet0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-145">**IPsecKeyManagersGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [<span data-ttu-id="6c5cd-146">**IPsecKeyManagerUnregisterAndDelete0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-146">**IPsecKeyManagerUnregisterAndDelete0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [<span data-ttu-id="6c5cd-147">**IPsecSaCoNtextSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-147">**IPsecSaContextSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [<span data-ttu-id="6c5cd-148">**IPsecSaCoNtextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-148">**IPsecSaContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [<span data-ttu-id="6c5cd-149">**IPsecSaCoNtextUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-149">**IPsecSaContextUnsubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [<span data-ttu-id="6c5cd-150">**NetworkIsolationDiagnoseConnectFailureAndGetInfo**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-150">**NetworkIsolationDiagnoseConnectFailureAndGetInfo**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [<span data-ttu-id="6c5cd-151">**NetworkIsolationEnumAppContainers**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-151">**NetworkIsolationEnumAppContainers**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [<span data-ttu-id="6c5cd-152">**NetworkIsolationEnumerateAppContainerRules**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-152">**NetworkIsolationEnumerateAppContainerRules**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [<span data-ttu-id="6c5cd-153">**NetworkIsolationFreeAppContainers**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-153">**NetworkIsolationFreeAppContainers**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [<span data-ttu-id="6c5cd-154">**NetworkIsolationGetAppContainerConfig**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-154">**NetworkIsolationGetAppContainerConfig**</span></span>](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [<span data-ttu-id="6c5cd-155">**NetworkIsolationRegisterForAppContainerChanges**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-155">**NetworkIsolationRegisterForAppContainerChanges**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [<span data-ttu-id="6c5cd-156">**NetworkIsolationSetAppContainerConfig**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-156">**NetworkIsolationSetAppContainerConfig**</span></span>](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [<span data-ttu-id="6c5cd-157">**NetworkIsolationSetupAppContainerBinaries**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-157">**NetworkIsolationSetupAppContainerBinaries**</span></span>](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [<span data-ttu-id="6c5cd-158">**PAC \_ 變更 \_ 回呼 \_ FN**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-158">**PAC\_CHANGES\_CALLBACK\_FN**</span></span>](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a><span data-ttu-id="6c5cd-159">新結構</span><span class="sxs-lookup"><span data-stu-id="6c5cd-159">New structures</span></span>

-   [<span data-ttu-id="6c5cd-160">**IKEEXT \_ 驗證 \_ METHOD2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-160">**IKEEXT\_AUTHENTICATION\_METHOD2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [<span data-ttu-id="6c5cd-161">**IKEEXT \_ CERT \_ EKUS0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-161">**IKEEXT\_CERT\_EKUS0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [<span data-ttu-id="6c5cd-162">**IKEEXT \_ CERT \_ .name0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-162">**IKEEXT\_CERT\_NAME0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [<span data-ttu-id="6c5cd-163">**IKEEXT \_ 憑證 \_ AUTHENTICATION2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-163">**IKEEXT\_CERTIFICATE\_AUTHENTICATION2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [<span data-ttu-id="6c5cd-164">**IKEEXT \_ 憑證 \_ CRITERIA0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-164">**IKEEXT\_CERTIFICATE\_CRITERIA0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [<span data-ttu-id="6c5cd-165">**IKEEXT \_ EM \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-165">**IKEEXT\_EM\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [<span data-ttu-id="6c5cd-166">**IKEEXT \_ KERBEROS \_ AUTHENTICATION1**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-166">**IKEEXT\_KERBEROS\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [<span data-ttu-id="6c5cd-167">**IKEEXT \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-167">**IKEEXT\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [<span data-ttu-id="6c5cd-168">**IPSEC \_ 金鑰 \_ MANAGER0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-168">**IPSEC\_KEY\_MANAGER0**</span></span>](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [<span data-ttu-id="6c5cd-169">**IPSEC \_ 金鑰 \_ 管理員 \_ CALLBACKS0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-169">**IPSEC\_KEY\_MANAGER\_CALLBACKS0**</span></span>](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [<span data-ttu-id="6c5cd-170">**IPSEC \_ 金鑰 \_ POLICY1**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-170">**IPSEC\_KEYING\_POLICY1**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [<span data-ttu-id="6c5cd-171">**IPSEC \_ SA \_ 內容 \_ CHANGE0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-171">**IPSEC\_SA\_CONTEXT\_CHANGE0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [<span data-ttu-id="6c5cd-172">**IPSEC \_ SA \_ 內容 \_ SUBSCRIPTION0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-172">**IPSEC\_SA\_CONTEXT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [<span data-ttu-id="6c5cd-173">**IPSEC \_ 傳輸 \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-173">**IPSEC\_TRANSPORT\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [<span data-ttu-id="6c5cd-174">**IPSEC \_ 通道 \_ ENDPOINT0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-174">**IPSEC\_TUNNEL\_ENDPOINT0**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [<span data-ttu-id="6c5cd-175">**IPSEC \_ 通道 \_ ENDPOINTS2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-175">**IPSEC\_TUNNEL\_ENDPOINTS2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [<span data-ttu-id="6c5cd-176">**IPSEC \_ 通道 \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-176">**IPSEC\_TUNNEL\_POLICY2**</span></span>](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [<span data-ttu-id="6c5cd-177">**FWPM \_ CONNECTION0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-177">**FWPM\_CONNECTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [<span data-ttu-id="6c5cd-178">**FWPM \_ 連接 \_ 列舉 \_ TEMPLATE0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-178">**FWPM\_CONNECTION\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [<span data-ttu-id="6c5cd-179">**FWPM \_ 連接 \_ SUBSCRIPTION0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-179">**FWPM\_CONNECTION\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [<span data-ttu-id="6c5cd-180">**FWPM \_ NET \_ EVENT2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-180">**FWPM\_NET\_EVENT2**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [<span data-ttu-id="6c5cd-181">**FWPM \_ NET \_ 事件 \_ 功能 \_ ALLOW0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-181">**FWPM\_NET\_EVENT\_CAPABILITY\_ALLOW0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [<span data-ttu-id="6c5cd-182">**FWPM \_ NET \_ 事件 \_ 功能 \_ DROP0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-182">**FWPM\_NET\_EVENT\_CAPABILITY\_DROP0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [<span data-ttu-id="6c5cd-183">**FWPM \_ NET \_ 事件 \_ 分類 \_ ALLOW0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-183">**FWPM\_NET\_EVENT\_CLASSIFY\_ALLOW0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [<span data-ttu-id="6c5cd-184">**FWPM \_ NET \_ 事件 \_ 分類 \_ DROP2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-184">**FWPM\_NET\_EVENT\_CLASSIFY\_DROP2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [<span data-ttu-id="6c5cd-185">**FWPM \_ NET \_ 事件 \_ 分類 \_ DROP \_ MAC0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-185">**FWPM\_NET\_EVENT\_CLASSIFY\_DROP\_MAC0**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [<span data-ttu-id="6c5cd-186">**FWPM \_ NET \_ EVENT \_ h 2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-186">**FWPM\_NET\_EVENT\_HEADER2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [<span data-ttu-id="6c5cd-187">**FWPM \_ 提供者 \_ CONTEXT2**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-187">**FWPM\_PROVIDER\_CONTEXT2**</span></span>](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [<span data-ttu-id="6c5cd-188">**FWPM \_ VSWITCH \_ EVENT0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-188">**FWPM\_VSWITCH\_EVENT0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [<span data-ttu-id="6c5cd-189">**FWPM \_ VSWITCH \_ 事件 \_ SUBSCRIPTION0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-189">**FWPM\_VSWITCH\_EVENT\_SUBSCRIPTION0**</span></span>](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a><span data-ttu-id="6c5cd-190">新的列舉類型</span><span class="sxs-lookup"><span data-stu-id="6c5cd-190">New enumerated types</span></span>

-   [<span data-ttu-id="6c5cd-191">**.FWP \_ VSWITCH \_ 網路 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-191">**FWP\_VSWITCH\_NETWORK\_TYPE**</span></span>](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [<span data-ttu-id="6c5cd-192">**FWPM \_ APPC \_ 網路 \_ 功能 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-192">**FWPM\_APPC\_NETWORK\_CAPABILITY\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [<span data-ttu-id="6c5cd-193">**FWPM \_ 連接 \_ 事件 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-193">**FWPM\_CONNECTION\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [<span data-ttu-id="6c5cd-194">**FWPM \_ VSWITCH \_ 事件 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-194">**FWPM\_VSWITCH\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [<span data-ttu-id="6c5cd-195">**IKEEXT \_ 憑證 \_ 準則 \_ 名稱 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-195">**IKEEXT\_CERT\_CRITERIA\_NAME\_TYPE**</span></span>](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [<span data-ttu-id="6c5cd-196">**IPSEC \_ SA \_ 內容 \_ 事件 \_ TYPE0**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-196">**IPSEC\_SA\_CONTEXT\_EVENT\_TYPE0**</span></span>](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a><span data-ttu-id="6c5cd-197">新的篩選層識別碼</span><span class="sxs-lookup"><span data-stu-id="6c5cd-197">New filtering layer identifiers</span></span>

[<span data-ttu-id="6c5cd-198">**篩選圖層識別碼：**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-198">**Filtering Layer Identifiers:**</span></span>](management-filtering-layer-identifiers-.md)

-   <span data-ttu-id="6c5cd-199">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="6c5cd-199">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="6c5cd-200">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="6c5cd-200">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="6c5cd-201">FWPM \_ 圖層 \_ 輸入 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="6c5cd-201">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="6c5cd-202">FWPM \_ 圖層 \_ 輸出 \_ MAC \_ 框架 \_ 原生</span><span class="sxs-lookup"><span data-stu-id="6c5cd-202">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="6c5cd-203">FWPM \_ 圖層輸入 \_ \_ VSWITCH \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="6c5cd-203">FWPM\_LAYER\_INGRESS\_VSWITCH\_ETHERNET</span></span>
-   <span data-ttu-id="6c5cd-204">FWPM \_ 圖層輸出 \_ \_ VSWITCH \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="6c5cd-204">FWPM\_LAYER\_EGRESS\_VSWITCH\_ETHERNET</span></span>
-   <span data-ttu-id="6c5cd-205">FWPM \_ 圖層輸入 \_ \_ vswitch \_ 傳輸 \_ V4/FWPM \_ 層輸入 \_ \_ vswitch \_ 傳輸 \_ V6</span><span class="sxs-lookup"><span data-stu-id="6c5cd-205">FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_INGRESS\_VSWITCH\_TRANSPORT\_V6</span></span>
-   <span data-ttu-id="6c5cd-206">FWPM \_ 層 \_ \_ 輸出 vswitch \_ 傳輸 \_ V4/FWPM \_ 層 \_ \_ 輸出 vswitch \_ 傳輸 \_ V6</span><span class="sxs-lookup"><span data-stu-id="6c5cd-206">FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V4 / FWPM\_LAYER\_EGRESS\_VSWITCH\_TRANSPORT\_V6</span></span>

## <a name="new-filtering-condition-identifiers"></a><span data-ttu-id="6c5cd-207">新的篩選準則識別碼</span><span class="sxs-lookup"><span data-stu-id="6c5cd-207">New filtering condition identifiers</span></span>

[<span data-ttu-id="6c5cd-208">**篩選準則識別碼：**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-208">**Filtering Condition Identifiers:**</span></span>](filtering-condition-identifiers-.md)

-   <span data-ttu-id="6c5cd-209">FWPM \_ 條件 \_ 介面 \_ MAC \_ 位址</span><span class="sxs-lookup"><span data-stu-id="6c5cd-209">FWPM\_CONDITION\_INTERFACE\_MAC\_ADDRESS</span></span>
-   <span data-ttu-id="6c5cd-210">FWPM \_ 條件 \_ MAC \_ 本機 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="6c5cd-210">FWPM\_CONDITION\_MAC\_LOCAL\_ADDRESS</span></span>
-   <span data-ttu-id="6c5cd-211">FWPM \_ 條件 \_ MAC \_ 遠端 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="6c5cd-211">FWPM\_CONDITION\_MAC\_REMOTE\_ADDRESS</span></span>
-   <span data-ttu-id="6c5cd-212">FWPM \_ CONDITION \_ 乙太幣 \_ TYPE</span><span class="sxs-lookup"><span data-stu-id="6c5cd-212">FWPM\_CONDITION\_ETHER\_TYPE</span></span>
-   <span data-ttu-id="6c5cd-213">FWPM \_ 條件 \_ VLAN \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="6c5cd-213">FWPM\_CONDITION\_VLAN\_ID</span></span>
-   <span data-ttu-id="6c5cd-214">FWPM \_ 條件 \_ NDIS \_ 埠</span><span class="sxs-lookup"><span data-stu-id="6c5cd-214">FWPM\_CONDITION\_NDIS\_PORT</span></span>
-   <span data-ttu-id="6c5cd-215">FWPM \_ 條件 \_ NDIS \_ 媒體 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="6c5cd-215">FWPM\_CONDITION\_NDIS\_MEDIA\_TYPE</span></span>
-   <span data-ttu-id="6c5cd-216">FWPM \_ 條件 \_ NDIS \_ 實體 \_ 媒體 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="6c5cd-216">FWPM\_CONDITION\_NDIS\_PHYSICAL\_MEDIA\_TYPE</span></span>
-   <span data-ttu-id="6c5cd-217">FWPM \_ 條件 \_ L2 \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="6c5cd-217">FWPM\_CONDITION\_L2\_FLAGS</span></span>
-   <span data-ttu-id="6c5cd-218">FWPM \_ 條件 \_ MAC \_ 本機 \_ 位址 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="6c5cd-218">FWPM\_CONDITION\_MAC\_LOCAL\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="6c5cd-219">FWPM \_ 條件 \_ MAC \_ 遠端 \_ 位址 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="6c5cd-219">FWPM\_CONDITION\_MAC\_REMOTE\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="6c5cd-220">FWPM \_ 條件 \_ ALE \_ 套件 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="6c5cd-220">FWPM\_CONDITION\_ALE\_PACKAGE\_ID</span></span>
-   <span data-ttu-id="6c5cd-221">FWPM \_ 條件 \_ MAC \_ 來源 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="6c5cd-221">FWPM\_CONDITION\_MAC\_SOURCE\_ADDRESS</span></span>
-   <span data-ttu-id="6c5cd-222">FWPM \_ 條件 \_ MAC \_ 目的地 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="6c5cd-222">FWPM\_CONDITION\_MAC\_DESTINATION\_ADDRESS</span></span>
-   <span data-ttu-id="6c5cd-223">FWPM \_ 條件 \_ MAC \_ 來源 \_ 位址 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="6c5cd-223">FWPM\_CONDITION\_MAC\_SOURCE\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="6c5cd-224">FWPM \_ 條件 \_ MAC \_ 目的地 \_ 位址 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="6c5cd-224">FWPM\_CONDITION\_MAC\_DESTINATION\_ADDRESS\_TYPE</span></span>
-   <span data-ttu-id="6c5cd-225">FWPM \_ 條件 \_ IP \_ 來源 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="6c5cd-225">FWPM\_CONDITION\_IP\_SOURCE\_PORT</span></span>
-   <span data-ttu-id="6c5cd-226">FWPM \_ 條件 \_ IP \_ 目的地 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="6c5cd-226">FWPM\_CONDITION\_IP\_DESTINATION\_PORT</span></span>
-   <span data-ttu-id="6c5cd-227">FWPM \_ 條件 \_ VSWITCH \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="6c5cd-227">FWPM\_CONDITION\_VSWITCH\_ID</span></span>
-   <span data-ttu-id="6c5cd-228">FWPM \_ 條件 \_ VSWITCH \_ 網路 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="6c5cd-228">FWPM\_CONDITION\_VSWITCH\_NETWORK\_TYPE</span></span>
-   <span data-ttu-id="6c5cd-229">FWPM \_ 條件 \_ VSWITCH \_ 來源 \_ 介面 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="6c5cd-229">FWPM\_CONDITION\_VSWITCH\_SOURCE\_INTERFACE\_ID</span></span>
-   <span data-ttu-id="6c5cd-230">FWPM \_ 條件 \_ VSWITCH \_ 目的地 \_ 介面 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="6c5cd-230">FWPM\_CONDITION\_VSWITCH\_DESTINATION\_INTERFACE\_ID</span></span>
-   <span data-ttu-id="6c5cd-231">FWPM \_ 條件 \_ VSWITCH \_ 來源 \_ VM \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="6c5cd-231">FWPM\_CONDITION\_VSWITCH\_SOURCE\_VM\_ID</span></span>
-   <span data-ttu-id="6c5cd-232">FWPM \_ 條件 \_ VSWITCH \_ 目的地 \_ VM \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="6c5cd-232">FWPM\_CONDITION\_VSWITCH\_DESTINATION\_VM\_ID</span></span>
-   <span data-ttu-id="6c5cd-233">FWPM \_ 條件 \_ VSWITCH \_ 來源 \_ 介面 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="6c5cd-233">FWPM\_CONDITION\_VSWITCH\_SOURCE\_INTERFACE\_TYPE</span></span>
-   <span data-ttu-id="6c5cd-234">FWPM \_ 條件 \_ VSWITCH \_ 租使用者 \_ 網路 \_ 識別碼</span><span class="sxs-lookup"><span data-stu-id="6c5cd-234">FWPM\_CONDITION\_VSWITCH\_TENANT\_NETWORK\_ID</span></span>

## <a name="new-filtering-condition-flags"></a><span data-ttu-id="6c5cd-235">新的篩選準則旗標</span><span class="sxs-lookup"><span data-stu-id="6c5cd-235">New filtering condition flags</span></span>

[<span data-ttu-id="6c5cd-236">**篩選準則旗標：**</span><span class="sxs-lookup"><span data-stu-id="6c5cd-236">**Filtering Condition Flags:**</span></span>](filtering-condition-flags-.md)

-   <span data-ttu-id="6c5cd-237">.FWP \_ 條件 \_ 旗標 \_ 是 \_ PROXY \_ 連接</span><span class="sxs-lookup"><span data-stu-id="6c5cd-237">FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION</span></span>
-   <span data-ttu-id="6c5cd-238">.FWP \_ 條件 \_ 旗標 \_ 是 \_ APPCONTAINER \_ 回送</span><span class="sxs-lookup"><span data-stu-id="6c5cd-238">FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK</span></span>
-   <span data-ttu-id="6c5cd-239">.FWP \_ 條件 \_ 旗標 \_ 為 \_ 非 \_ APPCONTAINER \_ 回送</span><span class="sxs-lookup"><span data-stu-id="6c5cd-239">FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK</span></span>
-   <span data-ttu-id="6c5cd-240">.FWP \_ 條件 \_ 旗標 \_ 正在接受 \_ \_ 原則 \_ 授權</span><span class="sxs-lookup"><span data-stu-id="6c5cd-240">FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE</span></span>
-   <span data-ttu-id="6c5cd-241">.FWP \_ 條件 \_ L2 \_ 是 \_ 原生 \_ 乙太網路</span><span class="sxs-lookup"><span data-stu-id="6c5cd-241">FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET</span></span>
-   <span data-ttu-id="6c5cd-242">.FWP \_ 條件 \_ L2 \_ 為 \_ WIFI</span><span class="sxs-lookup"><span data-stu-id="6c5cd-242">FWP\_CONDITION\_L2\_IS\_WIFI</span></span>
-   <span data-ttu-id="6c5cd-243">.FWP \_ 條件 \_ L2 \_ 為 \_ MOBILE \_ 寬頻</span><span class="sxs-lookup"><span data-stu-id="6c5cd-243">FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND</span></span>
-   <span data-ttu-id="6c5cd-244">.FWP \_ 條件 \_ L2 \_ 為 \_ WIFI \_ DIRECT \_ 資料</span><span class="sxs-lookup"><span data-stu-id="6c5cd-244">FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA</span></span>
-   <span data-ttu-id="6c5cd-245">\_ \_ \_ 已 VM2VM 的 .fwp 條件 L2 \_</span><span class="sxs-lookup"><span data-stu-id="6c5cd-245">FWP\_CONDITION\_L2\_IS\_VM2VM</span></span>
-   <span data-ttu-id="6c5cd-246">.FWP \_ 條件 \_ L2 \_ 是 \_ 格式不正確的封 \_ 包</span><span class="sxs-lookup"><span data-stu-id="6c5cd-246">FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET</span></span>
-   <span data-ttu-id="6c5cd-247">.FWP \_ 條件 \_ L2 \_ 是 \_ IP \_ 片段 \_ 群組</span><span class="sxs-lookup"><span data-stu-id="6c5cd-247">FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP</span></span>
-   <span data-ttu-id="6c5cd-248">\_ \_ \_ 當 \_ 連接器 \_ 存在時的 .fwp 條件 L2</span><span class="sxs-lookup"><span data-stu-id="6c5cd-248">FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT</span></span>

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a><span data-ttu-id="6c5cd-249">Windows 7 更新至 Windows 篩選平台</span><span class="sxs-lookup"><span data-stu-id="6c5cd-249">Windows 7 updates to the Windows Filtering Platform</span></span>

<span data-ttu-id="6c5cd-250">[Windows 篩選平台的新功能]()詳述了許多 windows 7 的更新。</span><span class="sxs-lookup"><span data-stu-id="6c5cd-250">The document [What's New in Windows Filtering Platform]() details many of the updates made for Windows 7.</span></span> <span data-ttu-id="6c5cd-251">您也可以在 Windows 7 上的 [WFP 變更](/windows-hardware/drivers/network/wfp-changes-for-windows-7)Windows 驅動程式套件中取得資訊。</span><span class="sxs-lookup"><span data-stu-id="6c5cd-251">Information is also available in the Windows Driver Kit on [WFP Changes for Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).</span></span>

 

 