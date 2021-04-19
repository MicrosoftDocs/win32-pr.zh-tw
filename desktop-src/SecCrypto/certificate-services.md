---
description: 憑證服務是在 Windows server 作業系統上執行的服務，會接收透過傳輸（例如 RPC 或 HTTP）的新數位憑證要求。
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: 憑證服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a3f25972f98a79a208719eb2bcb08de07d7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998521"
---
# <a name="certificate-services"></a>憑證服務

[*憑證服務*](../secgloss/c-gly.md)是在 Windows server 作業系統上執行的服務，會接收透過傳輸（例如 RPC 或 HTTP）的新數位憑證要求。 它會根據自訂或網站特定原則來檢查每個要求、設定要發行之憑證的選擇性屬性，以及頒發證書。 憑證服務可讓系統管理員將專案新增至 (CRL) 的 [*憑證撤銷清單*](../secgloss/c-gly.md) ，以及定期發佈已簽署的 crl。

憑證服務包含可程式化的介面，可用於建立其他傳輸、原則和憑證屬性與格式的支援。

在 Windows Server 2003 中，您可以按一下 [**新增或移除程式**]，然後按一下 [**新增/移除 Windows 元件**] 以安裝或卸載憑證服務，從 **主控台** 安裝憑證服務2.0。

下列各節將詳細說明憑證服務概念。 內容旨在協助您開發會與憑證服務互動的應用程式。



| Content                                                                                                                                                           | 區段                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| 憑證服務功能的描述                                                                                                               | [憑證服務功能](certificate-services-features.md)         |
| 憑證服務架構的總覽                                                                                                                     | [憑證服務架構](certificate-services-architecture.md) |
| 憑證、憑證主體和主體公開金鑰之間的關聯性[ ](../secgloss/p-gly.md) | [憑證和公開金鑰](certificates-and-public-keys.md)           |
| 憑證要求屬性的相關資訊                                                                                                              | [憑證要求指導方針](certificate-request-guidelines.md)       |
| 憑證服務處理憑證方式的詳細資料                                                                                                 | [關於憑證](about-certificates.md)                               |
| [*憑證授權單位*](../secgloss/c-gly.md)單位更新程式的描述        | [憑證授權單位單位更新](certification-authority-renewal.md)     |



 

另外也包含下列其他有用的主題。



| Content                                                                                                                                             | 區段                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| 憑證註冊控制項的相關檔，提供用來建立憑證要求的服務，包括智慧卡使用者的要求。 | [憑證註冊控制項](certificate-enrollment-control.md) |
| Microsoft 密碼編譯應用程式開發介面的檔，可提供密碼編譯式安全性服務。                | [密碼編譯基本概念](cryptography-essentials.md)               |
| 智慧卡上的檔，提供用於開發和使用智慧卡系統的服務。                                                   | [智慧卡](../secauthn/smart-card-authentication.md)                     |
| 憑證和憑證要求的名稱屬性。                                                                                           | [名稱屬性](name-properties.md)                               |
| [*X.509*](../secgloss/x-gly.md)憑證屬性的清單和描述。                                  | [憑證屬性](certificate-properties.md)                 |



 

 

 
