---
description: 使用 Windows api 和服務來開發更安全的桌面應用程式。
ms.assetid: 1d078a53-250e-4f40-8a3b-83396f2201fc
title: 安全性及身分識別
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: ff19c113340af314177b821bfd8294036d752d90218a5255eb6a429e9b6312ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226333"
---
# <a name="security-and-identity"></a>安全性及身分識別

使用 Windows api 和服務來開發更安全的桌面應用程式。 這些 Api 提供：

- 驗證
- 授權
- 密碼編譯
- 目錄、身分識別和存取服務
- 家長監護
- 版權管理

本節也提供最佳作法和其他安全性文章。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
| ----- | ----------- |
| [反惡意程式碼掃描介面](./amsi/antimalware-scan-interface-portal.md) | 反惡意程式碼掃描介面 (AMSI) 是一種泛型介面標準，可讓應用程式和服務與任何存在於電腦上的反惡意程式碼產品整合。 它可為使用者及其資料、應用程式和工作負載提供增強的惡意程式碼防護。 |
| [驗證](./secauthn/authentication-portal.md) | 驗證是系統用來驗證使用者登入資訊的程式。 使用者的名稱和密碼會與授權清單相比較，如果系統偵測到相符項，則會將存取權授與給該使用者的許可權清單中指定的範圍。 |
| [授權](./secauthz/authorization-portal.md) | 授權是授與個人使用系統及其儲存資料的許可權。 授權通常是由系統管理員設定，並由電腦根據某種形式的使用者識別碼（例如代碼號碼或密碼）進行驗證。 |
| [安全性 Api 的最佳作法](./secbp/best-practices-for-the-security-apis.md) | 提供開發更安全應用程式的最佳做法。 |
| [憑證註冊 API](./seccertenroll/certenroll-portal.md) | 憑證註冊 API 可以用來建立用戶端應用程式，以要求憑證並安裝憑證回應。 |
| [控制流程防護 (CFG) ](./secbp/control-flow-guard.md) | Control Flow Guard (CFG) 是一種高度優化的平臺安全性功能，其建立是為了對抗記憶體損毀弱點。 |
| [碼編譯](./seccrypto/cryptography-portal.md) | 密碼編譯是使用程式碼來轉換資料，如此一來，只有特定的收件者才能夠使用金鑰來讀取它。 CryptoAPI 讓使用者可以在安全的環境中建立及交換檔和其他資料，尤其是透過非安全的媒體（例如網際網路）。 |
| [密碼編譯 API：新一代](./seccng/cng-portal.md) | 密碼編譯 API：新一代 (CNG) 可讓使用者在安全的環境中建立及交換檔和其他資料，尤其是透過非安全的媒體（例如網際網路）。 |
| [動態存取控制開發人員擴充性](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) | 動態存取控制 (DAC) 案例（如 Windows Server 2012 所提供）具有各種開發人員擴充性點，可為應用程式開發加入自訂潛力。 |
| [目錄、身分識別和 Access Services](./srvnodes/directory--identity--and-access-services.md) | 網路系統管理員可以使用目錄服務來自動化一般管理工作，例如新增使用者和群組、管理印表機，以及設定網路資源的許可權。<br/> 獨立軟體廠商和使用者開發人員可以使用目錄服務來目錄啟用其產品和應用程式。 服務可以在目錄中發佈自己，用戶端可以使用目錄來尋找服務，而且兩者都可以使用目錄來尋找和操作其他物件。<br/> Forefront Identity Manager (FIM) 提供整合式且全方位的解決方案，可用於管理使用者身分識別的整個生命週期及其相關聯的認證。<br/> 身分識別生命週期管理員 (ILM) 可讓 IT 組織透過在整個異類企業中提供使用者身分識別的單一觀點，以及透過自動化一般工作，來降低管理身分識別和存取生命週期的成本。<br/> Active Directory 同盟服務 (AD FS) 在安全性與企業界限之間安全地共用數位身分識別和權利，藉以啟用同盟身分識別和存取管理。 |
| [可延伸的驗證通訊協定](./eap/extensible-authentication-protocol-reference.md) | 可延伸的驗證通訊協定 (EAP) 是數個系統元件所支援的標準。 EAP 對於保護無線 (802.1 X) 和有線區域網路、撥號和虛擬私人網路 (Vpn) 的安全性非常重要。 |
| [可延伸的驗證通訊協定主機](./eaphost/about-eap-host.md) | EAPHost 是一種 Microsoft Windows 網路元件，提供可延伸的驗證通訊協定 (EAP) 基礎結構，以驗證 "要求者" 通訊協定的執行，例如 802.1 x 和點對點 (PPP) 。 |
| [MS-CHAP 密碼管理 API](/previous-versions/windows/desktop/mschap/portal) | 您可以使用 MS-CHAP 密碼管理 API 來建立應用程式，以變更遠端工作站上網路使用者的密碼。 |
| [網路存取保護](./nap/network-access-protection-start-page.md) | 網路存取保護 (NAP) 是一組作業系統元件，可提供保護私人網路存取的平臺。 NAP 平臺提供了一種整合方式，可評估網路用戶端的系統健全狀況狀態，嘗試連線到網路或在網路上通訊，以及限制網路用戶端的存取，直到達到健康原則需求為止。 |
| [網路原則伺服器](./nps/portal.md) | 網路原則伺服器 (NPS) 是 Microsoft 對遠端驗證撥入使用者服務 (RADIUS) 伺服器和 proxy 的實施。 這是網際網路驗證服務 (IAS) 的後續版本。 |
| [家長監護](./parcon/parental-controls-portal.md) | Windows 的家長監護技術旨在協助用心家長或監護人，以確保能以年齡或成熟度等級來存取其保護下的適當教材。 除了內建功能以外，它還提供了可擴充的基礎結構。 |
| [Rights Management](./srvnodes/rights-management.md) | 現在提供三代的 Rights Management SDK，以及 Microsoft 針對所有支援的作業系統提供的 RMS 程式碼範例和開發人員工具的全面藍圖;Android、iOS/OS X、Windows Phone 和 Windows Desktop。 |
| [SDL) 的安全性開發生命週期 (-流程指引](/previous-versions/windows/desktop/cc307891(v=msdn.10)) | Microsoft 安全性開發週期 (SDL) 是領先業界的軟體安全性保證程式。 從2004開始，SDL 一直都是 Microsoft 的計畫和強制性原則，在 Microsoft 軟體和文化中的安全性與隱私權方面都扮演了重要的角色。 SDL 結合了整體與實用的方法，在開發過程中的初期和整個階段都有安全性和隱私權。 |
| [安全性管理](./secmgmt/management-portal.md) | 安全性管理技術可以用來管理本地安全機構 (LSA) 原則和密碼篩選原則、查詢來自外部來源的程式能力，以及擴充安全性設定工具功能的服務附件。 |
| [安全性 WMI 提供者](./secprov/secprov-portal.md) | 安全性 wmi 提供者可讓系統管理員和程式設計人員使用) Windows Management Instrumentation WMI (，設定 BitLocker 磁碟機加密 (的) 和可信賴平臺模組 (TPM) 。 |
| [安全性詞彙](./secgloss/security-glossary.md) | 提供安全性條款的詞彙。 |
| [TPM 基本服務](./tbs/tpm-base-services-portal.md) | 信賴平臺模組 (TPM) 基礎服務 (TB) 功能會跨應用程式集中進行 TPM 存取。 [TB] 功能使用由呼叫應用程式以合作排程 TPM 存取所指定的優先順序。 |
| [Windows 生物特徵辨識架構 API](./secbiomet/biometric-service-api-portal.md) | 您可以使用 Windows 生物特徵辨識架構 API 來建立用戶端應用程式，以安全地捕捉、儲存和比較使用者生物特徵辨識資訊。 |
| [安全性技術文章](https://msdn.microsoft.com/library/hh322936.aspx) | 關於安全性和密碼編譯的文章。 |



 

 

 