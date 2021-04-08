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
# <a name="directory-service-functions-ad-ds"></a>目錄服務函式 (AD DS) 

目錄服務函式提供一個公用程式，可在 Windows NT 或 Windows 2000 網域中找出 (DC) 的網域控制站。 架構會與用戶端以及所有版本的 Windows NT 和 Windows 2000 中的伺服器互動。 下列功能可讓開發人員使用目錄服務中的網域控制站和網域成員資格：

-   [**DsAddressToSiteNames**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesa)
-   [**DsAddressToSiteNamesEx**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesexa)
-   [**DsDeregisterDnsHostRecords**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsderegisterdnshostrecordsa)
-   [**DsEnumerateDomainTrusts**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa)
-   [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)
-   [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)
-   [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)
-   [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)
-   [**DsGetDcSiteCoverage**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcsitecoveragea)
-   [**DsGetForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetforesttrustinformationw)
-   [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea)
-   [**DsMergeForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsmergeforesttrustinformationw)
-   [**DsRoleFreeMemory**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolefreememory)
-   [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation)
-   [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)

DC 定位器（ [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)）是由 Netlogon 服務所執行。 每個 DC 都會使用傳輸特定的機制（例如，在 WINS 中），在 DNS 伺服器上註冊其 DNS 名稱及其 NetBIOS 名稱。 DC 定位器會查閱名稱，然後將資料包傳送到註冊此名稱的 DC，或進行 ping。 針對 NetBIOS 功能變數名稱，資料包是一封郵筒訊息。 針對 DNS 功能變數名稱，資料包是 LDAP UDP 搜尋。 每個這類 DC 都會回應，指出目前正在運作。 第一個要回應的 DC 會傳回給呼叫者。

傳回的 DC 會快取，因此後續呼叫端不需要重複上述演算法，也不需要讓所有呼叫端都使用相同的 DC。 這可確保單一用戶端的 DC 內容具有一致的觀點。

依 DNS 功能變數名稱搜尋 DC 時，DC 定位器會嘗試在「最接近」的網站中找到 DC。 每個 DC 都會註冊額外的 DNS 記錄，指出 DC 所在的網站，以及 DC 包含的網站。 DC 定位程式會先搜尋此網站專屬的 DNS 記錄，再搜尋非網站專屬的 DNS 記錄，藉此在該網站中偏好 DC。 當 DC 定位器將資料包傳送至 DC 時，DC 會在 DS 的設定/網站/子網容器中查閱用戶端的 IP 位址，以尋找子網物件。 子網物件的 **siteObject** 屬性會定義包含用戶端的網站名稱。 DC 會以包含用戶端的網站名稱回應 ping，以及此 DC 是否涵蓋該網站的指標。 如果 DC 未包含該網站，而且 DC 定位器尚未嘗試在該網站中找到 DC，DC 定位器就會再次嘗試在網站中尋找 DC。

若要尋找包含用戶端的網站名稱，請使用 [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea) 函數。 設定/網站/子網容器中的物件名稱必須是有效的子網名稱。 [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)函數會指出指定的子網名稱是否有效。

 

 




