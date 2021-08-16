---
description: 列出可與 SSPI 搭配使用的安全性封裝。
ms.assetid: f5999d41-b334-49be-8883-d9b9042d20dc
title: 使用安全性封裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9253ee2ac4cec98e3c68a1f3dab80a71b216e6235af78722864ee0e0958897c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915190"
---
# <a name="using-security-packages"></a>使用安全性封裝

[*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) 可搭配下列 [*安全性套件*](../secgloss/s-gly.md)使用：

-   [Kerberos 安全性套件](#kerberos-security-package)
-   [NTLM 安全性封裝](#ntlm-security-package)

[*Kerberos*](../secgloss/k-gly.md)和 NTLM 通訊協定會實作為作業系統提供的 Secur32.dll [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 的安全性套件。 根據預設，在系統啟動時，電腦上的 [*本機安全機構*](../secgloss/l-gly.md) 會將 KERBEROS 和 NTLM 驗證的支援載入 (LSA) 。 在 Windows 伺服器或 Windows 網域中，您可以使用這兩種套件來驗證網路登入和用戶端/伺服器連接。 使用哪一種取決於連接另一端的電腦功能。 Kerberos 通訊協定一律是慣用的（如果有的話）。

建立互動式使用者的安全性內容之後，就可以在使用者的安全性內容中執行的進程載入 Kerberos 或 NTLM 封裝的另一個實例，以支援交換、簽署、驗證、加密和解密訊息。 不過，除了 LSA 以外的任何程式都不允許存取認證快取中的 [*工作階段金鑰*](../secgloss/s-gly.md) 或票證。

系統服務和傳輸層級的應用程式會透過 SSPI 存取 SSP，以提供用來列舉系統上可用之安全性封裝的函式、選取封裝，以及使用該套件來取得已驗證的連接。

SSPI 中的方法是一般常式，開發人員可以在不知道特定 [*安全性通訊協定*](../secgloss/s-gly.md)的詳細資料的情況下使用。 例如，當用戶端/伺服器連接通過驗證時：

1.  用戶端上的應用程式會使用 SSPI 函式 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)將 [*認證*](../secgloss/c-gly.md)傳送至伺服器。
2.  連接之伺服器端上的應用程式會使用 SSPI 函式 [**AcceptSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)來回應。
3.  連接經過驗證之後，伺服器上的 LSA 會使用來自用戶端的資訊來建立 [*存取權杖*](../secgloss/a-gly.md)。
4.  伺服器接著可以呼叫 SSPI 函式 [**ImpersonateSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) ，將存取權杖附加至服務的模擬執行緒。

## <a name="kerberos-security-package"></a>Kerberos 安全性套件

Kerberos [*安全性套件*](../secgloss/s-gly.md) 是以 [*kerberos 驗證通訊協定*](../secgloss/k-gly.md)為基礎。

如果使用 Kerberos 通訊協定來驗證用戶端/伺服器連接， [**InitializeSecurityCoNtext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 會產生 GSSAPI 訊息，其中包含 \_ 來自用戶端的 KRB AP 要求 \_ 訊息。 [**AcceptSecurityCoNtext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) 接著會產生 GSSAPI 訊息，其中包含 \_ 來自伺服器的 KRB AP \_ REP 訊息。

如需在 Kerberos 通訊協定的執行幕後進行之步驟的背景資訊，請參閱 [Microsoft Kerberos](microsoft-kerberos.md)。

所有分散式服務都會使用 SSPI 來存取 Kerberos 通訊協定。 Kerberos 通訊協定用於驗證的方式部分清單包括：

-   列印多工緩衝處理器服務
-   CIFS/SMB 遠端檔案存取
-   Active Directory 的 [*LDAP*](../secgloss/l-gly.md)查詢
-   分散式檔案系統管理與參考
-   IPsec 主機對主機安全性授權單位驗證
-   網路服務品質的保留要求
-   Internet Information Services 的內部網路驗證
-   使用已驗證 RPC 的遠端伺服器或工作站管理
-   網域使用者和電腦的憑證服務 [*憑證要求*](../secgloss/c-gly.md)

## <a name="ntlm-security-package"></a>NTLM 安全性封裝

NTLM 安全性封裝是以 NTLM 驗證通訊協定為基礎。

 

 
