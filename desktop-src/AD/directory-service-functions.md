---
title: '目錄服務函式 (AD DS) '
description: 目錄服務函式提供一個公用程式，可在 Windows NT 或 Windows 2000 網域中找出 (DC) 的網域控制站。
ms.assetid: 7b519c81-5a6c-470a-a525-1894efd53305
ms.tgt_platform: multiple
keywords:
- 目錄服務功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b071128806926e07cf61d62e53b823d8e7e1ac
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "104022933"
---
# <a name="directory-service-functions-ad-ds"></a><span data-ttu-id="6db4e-104">目錄服務函式 (AD DS) </span><span class="sxs-lookup"><span data-stu-id="6db4e-104">Directory Service Functions (AD DS)</span></span>

<span data-ttu-id="6db4e-105">目錄服務函式提供一個公用程式，可在 Windows NT 或 Windows 2000 網域中找出 (DC) 的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="6db4e-105">The directory service functions provide a utility for locating a domain controller (DC) in a Windows NT or Windows 2000 domain.</span></span> <span data-ttu-id="6db4e-106">架構會與用戶端以及所有版本的 Windows NT 和 Windows 2000 中的伺服器互動。</span><span class="sxs-lookup"><span data-stu-id="6db4e-106">The architecture interacts with clients as well as servers in all versions of Windows NT and Windows 2000.</span></span> <span data-ttu-id="6db4e-107">下列功能可讓開發人員使用目錄服務中的網域控制站和網域成員資格：</span><span class="sxs-lookup"><span data-stu-id="6db4e-107">The following functions enable developers to work with the domain controller and domain membership in the directory service:</span></span>

-   [<span data-ttu-id="6db4e-108">**DsAddressToSiteNames**</span><span class="sxs-lookup"><span data-stu-id="6db4e-108">**DsAddressToSiteNames**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesa)
-   [<span data-ttu-id="6db4e-109">**DsAddressToSiteNamesEx**</span><span class="sxs-lookup"><span data-stu-id="6db4e-109">**DsAddressToSiteNamesEx**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesexa)
-   [<span data-ttu-id="6db4e-110">**DsDeregisterDnsHostRecords**</span><span class="sxs-lookup"><span data-stu-id="6db4e-110">**DsDeregisterDnsHostRecords**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsderegisterdnshostrecordsa)
-   [<span data-ttu-id="6db4e-111">**DsEnumerateDomainTrusts**</span><span class="sxs-lookup"><span data-stu-id="6db4e-111">**DsEnumerateDomainTrusts**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa)
-   [<span data-ttu-id="6db4e-112">**DsGetDcClose**</span><span class="sxs-lookup"><span data-stu-id="6db4e-112">**DsGetDcClose**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)
-   [<span data-ttu-id="6db4e-113">**DsGetDcName**</span><span class="sxs-lookup"><span data-stu-id="6db4e-113">**DsGetDcName**</span></span>](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)
-   [<span data-ttu-id="6db4e-114">**DsGetDcNext**</span><span class="sxs-lookup"><span data-stu-id="6db4e-114">**DsGetDcNext**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)
-   [<span data-ttu-id="6db4e-115">**DsGetDcOpen**</span><span class="sxs-lookup"><span data-stu-id="6db4e-115">**DsGetDcOpen**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)
-   [<span data-ttu-id="6db4e-116">**DsGetDcSiteCoverage**</span><span class="sxs-lookup"><span data-stu-id="6db4e-116">**DsGetDcSiteCoverage**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcsitecoveragea)
-   [<span data-ttu-id="6db4e-117">**DsGetForestTrustInformationW**</span><span class="sxs-lookup"><span data-stu-id="6db4e-117">**DsGetForestTrustInformationW**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetforesttrustinformationw)
-   [<span data-ttu-id="6db4e-118">**DsGetSiteName**</span><span class="sxs-lookup"><span data-stu-id="6db4e-118">**DsGetSiteName**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea)
-   [<span data-ttu-id="6db4e-119">**DsMergeForestTrustInformationW**</span><span class="sxs-lookup"><span data-stu-id="6db4e-119">**DsMergeForestTrustInformationW**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsmergeforesttrustinformationw)
-   [<span data-ttu-id="6db4e-120">**DsRoleFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="6db4e-120">**DsRoleFreeMemory**</span></span>](/windows/desktop/api/Dsrole/nf-dsrole-dsrolefreememory)
-   [<span data-ttu-id="6db4e-121">**DsRoleGetPrimaryDomainInformation**</span><span class="sxs-lookup"><span data-stu-id="6db4e-121">**DsRoleGetPrimaryDomainInformation**</span></span>](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation)
-   [<span data-ttu-id="6db4e-122">**DsValidateSubnetName**</span><span class="sxs-lookup"><span data-stu-id="6db4e-122">**DsValidateSubnetName**</span></span>](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)

<span data-ttu-id="6db4e-123">DC 定位器（ [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)）是由 Netlogon 服務所執行。</span><span class="sxs-lookup"><span data-stu-id="6db4e-123">The DC locator, [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea), is implemented by the Netlogon service.</span></span> <span data-ttu-id="6db4e-124">每個 DC 都會使用傳輸特定的機制（例如，在 WINS 中），在 DNS 伺服器上註冊其 DNS 名稱及其 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="6db4e-124">Each DC registers its DNS name on the DNS server and its NetBIOS name using a transport-specific mechanism, for example, in WINS.</span></span> <span data-ttu-id="6db4e-125">DC 定位器會查閱名稱，然後將資料包傳送到註冊此名稱的 DC，或進行 ping。</span><span class="sxs-lookup"><span data-stu-id="6db4e-125">The DC locator looks up the name, then sends a datagram to, or pings, the DC that registered the name.</span></span> <span data-ttu-id="6db4e-126">針對 NetBIOS 功能變數名稱，資料包是一封郵筒訊息。</span><span class="sxs-lookup"><span data-stu-id="6db4e-126">For NetBIOS domain names, the datagram is a mailslot message.</span></span> <span data-ttu-id="6db4e-127">針對 DNS 功能變數名稱，資料包是 LDAP UDP 搜尋。</span><span class="sxs-lookup"><span data-stu-id="6db4e-127">For DNS domain names, the datagram is an LDAP UDP search.</span></span> <span data-ttu-id="6db4e-128">每個這類 DC 都會回應，指出目前正在運作。</span><span class="sxs-lookup"><span data-stu-id="6db4e-128">Each such DC responds indicating that it is currently operational.</span></span> <span data-ttu-id="6db4e-129">第一個要回應的 DC 會傳回給呼叫者。</span><span class="sxs-lookup"><span data-stu-id="6db4e-129">The first DC to respond is returned to the caller.</span></span>

<span data-ttu-id="6db4e-130">傳回的 DC 會快取，因此後續呼叫端不需要重複上述演算法，也不需要讓所有呼叫端都使用相同的 DC。</span><span class="sxs-lookup"><span data-stu-id="6db4e-130">The returned DC is cached, so that subsequent callers need not repeat the preceding algorithm, and to encourage all callers to use that same DC.</span></span> <span data-ttu-id="6db4e-131">這可確保單一用戶端的 DC 內容具有一致的觀點。</span><span class="sxs-lookup"><span data-stu-id="6db4e-131">This ensures that a single client has a consistent view of the contents of the DC.</span></span>

<span data-ttu-id="6db4e-132">依 DNS 功能變數名稱搜尋 DC 時，DC 定位器會嘗試在「最接近」的網站中找到 DC。</span><span class="sxs-lookup"><span data-stu-id="6db4e-132">When searching for a DC by DNS domain name, the DC locator attempts to find a DC in the "closest" site.</span></span> <span data-ttu-id="6db4e-133">每個 DC 都會註冊額外的 DNS 記錄，指出 DC 所在的網站，以及 DC 包含的網站。</span><span class="sxs-lookup"><span data-stu-id="6db4e-133">Each DC registers additional DNS records indicating what site that the DC is in and what sites the DC includes.</span></span> <span data-ttu-id="6db4e-134">DC 定位程式會先搜尋此網站專屬的 DNS 記錄，再搜尋非網站專屬的 DNS 記錄，藉此在該網站中偏好 DC。</span><span class="sxs-lookup"><span data-stu-id="6db4e-134">The DC locator first searches for this site-specific DNS record before searching for the DNS record that is not site-specific, thus preferring a DC in that site.</span></span> <span data-ttu-id="6db4e-135">當 DC 定位器將資料包傳送至 DC 時，DC 會在 DS 的設定/網站/子網容器中查閱用戶端的 IP 位址，以尋找子網物件。</span><span class="sxs-lookup"><span data-stu-id="6db4e-135">When the DC locator sends a datagram to the DC, the DC looks up the IP address of the client in the Configuration/Sites/Subnet container of the DS to find a subnet object.</span></span> <span data-ttu-id="6db4e-136">子網物件的 **siteObject** 屬性會定義包含用戶端的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="6db4e-136">The **siteObject** property of the subnet object defines the name of the site that contains the client.</span></span> <span data-ttu-id="6db4e-137">DC 會以包含用戶端的網站名稱回應 ping，以及此 DC 是否涵蓋該網站的指標。</span><span class="sxs-lookup"><span data-stu-id="6db4e-137">The DC responds to the ping with the name of the site that contains the client, along with an indicator of whether this DC covers that site.</span></span> <span data-ttu-id="6db4e-138">如果 DC 未包含該網站，而且 DC 定位器尚未嘗試在該網站中找到 DC，DC 定位器就會再次嘗試在網站中尋找 DC。</span><span class="sxs-lookup"><span data-stu-id="6db4e-138">If the DC does not include that site and the DC locator has not yet attempted to find a DC in that site, the DC locator tries again to find a DC in the site.</span></span>

<span data-ttu-id="6db4e-139">若要尋找包含用戶端的網站名稱，請使用 [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea) 函數。</span><span class="sxs-lookup"><span data-stu-id="6db4e-139">To find the name of the site containing the client, use the [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea) function.</span></span> <span data-ttu-id="6db4e-140">設定/網站/子網容器中的物件名稱必須是有效的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="6db4e-140">The names of the objects in the Configuration/Sites/Subnet container must be valid subnet names.</span></span> <span data-ttu-id="6db4e-141">[**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)函數會指出指定的子網名稱是否有效。</span><span class="sxs-lookup"><span data-stu-id="6db4e-141">The [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea) function indicates whether a specified subnet name is valid.</span></span>

 

 




