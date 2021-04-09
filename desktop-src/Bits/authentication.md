---
title: '驗證 (位) '
description: BITS 支援基本驗證、Passport 驗證，以及數個挑戰/回應驗證配置。
ms.assetid: cfd4aec3-79d0-4971-93f8-df797e5c0f75
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 5d970956676a3348dd4b8c4b420e044bd4714775
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103933816"
---
# <a name="authentication-bits"></a>驗證 (位) 

BITS 支援基本驗證、Passport 驗證，以及數個挑戰/回應驗證配置。 如果伺服器或 proxy 需要使用者驗證，請使用 [**IBackgroundCopyJob2：： SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 函數來指定使用者的認證。 BITS 使用 [CryptoAPI](/windows/desktop/SecCrypto/cryptography-portal) 來保護認證。

若要設定基本驗證的認證，請使用 [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 函數來指定使用者名稱和密碼。 您應僅使用基本驗證搭配受 HTTPs://保護的安全網站;否則使用者將可以看見使用者名稱和密碼。 

您可以在 URL 中內嵌使用者名稱和密碼。 這並不是很好的安全性作法，而且在 RFC 3986 (區段 3.2.1) 中已淘汰。

針對 [Passport](/windows/desktop/WinHttp/passport-authentication-in-winhttp) 驗證，BITS 僅支援明確的認證，而非與帳戶系結的隱含認證。

針對挑戰/回應驗證，BITS 會模擬使用者並使用 [Snego](../com/snego.md) 來判斷要使用的挑戰/回應驗證，例如 NTLM 或 Kerberos 通訊協定。 如需 BITS 支援的挑戰/回應配置清單，請參閱「 [**BG \_ 驗證 \_ 配置**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme)」。

如果伺服器上的虛擬目錄具有匿名驗證並啟用另一個驗證配置，且 Acl 保護虛擬目錄或下載檔案，BITS 工作可能會失敗。 例如，如果虛擬目錄已啟用匿名和整合式驗證，且檔案包含只允許 Ben 讀取檔案的 ACL，則作業會失敗並顯示「拒絕存取」。 發生這種情況是因為虛擬目錄允許匿名存取，因此 IIS 不會明確驗證 Ben (Ben 的認證不會用來存取檔案，且拒絕存取) 。

## <a name="using-implicit-credentials"></a>使用隱含認證

若要使用使用者的隱含 (登入) NTLM 或 Kerberos 驗證的認證，請 [**呼叫 IBackgroundCopyJob2：： SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials)方法，並將 [**BG \_ 基本 \_ 認證**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_basic_credentials)結構的使用者 **名稱** 和 **密碼** 成員設定為 **Null**。 如果您指定 proxy 的隱含認證，BITS 也會使用隱含的憑證來進行伺服器驗證，除非您指定明確的伺服器認證。

如需服務的詳細資訊，請參閱 [服務帳戶和 BITS](service-accounts-and-bits.md)。

您也可以變更 **LMCompatibilityLevel** 或 **UseLMCompat** 登錄值;不過，只有當您的現有應用程式無法變更為呼叫 [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 方法時，才應該變更這些值。

如果 **LMCompatibilityLevel** 登錄值為2或以上，且您未呼叫 [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 方法，則 BITS 會使用隱含認證進行驗證。 **LMCompatibilityLevel** 登錄值的完整路徑是 **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **LMCompatibilityLevel**。

請注意，變更 **LMCompatibilityLevel** 登錄值可能會影響電腦上正在執行的其他應用程式和服務。 如需使用 **LMCompatibilityLevel** 登錄值的詳細資訊，請參閱 [KB147706](https://support.microsoft.com/kb/147706)。

如果設定 **LMCompatibilityLevel** 登錄值是問題，您可以在 **HKEY \_ LOCAL \_ MACHINE**  \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **BITS** 下建立 UseLMCompat 登錄值。 登錄值為 DWORD。 下表列出 **UseLMCompat** 的可能值：

|值|描述|
|-|-|
| 0     | 只要伺服器提示您輸入 NTLM 或 Kerberos 認證，BITS 就會傳送隱含的認證。                                                                                           |
| 1     | 只有當用戶端電腦的 **LMCompatibilityLevel** 登錄值大於或等於2時，BITS 才會傳送隱含的認證。<br/>     |
| 2     | 只有當應用程式呼叫 [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 方法時，BITS 才會傳送隱含的認證。<br/> |

如果登錄值不存在，BITS 會針對 **UseLMCompat** 登錄值使用 "2" 的預設值。

## <a name="using-certificates-for-clientserver-authentication"></a>使用憑證進行用戶端/伺服器驗證

在安全的用戶端/伺服器通訊中，用戶端和伺服器可以使用數位憑證互相相互驗證。 BITS 會自動支援安全 HTTP 傳輸的憑證型伺服器驗證。 若要為用戶端憑證提供相互驗證所需的位，請呼叫 [**IBackgroundCopyJobHttpOptions：： SetClientCertificateByID**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) 或 [**IBackgroundCopyJobHttpOptions：： SetClientCertificateByName**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname) 方法。

當網站接受但不需要 SSL 用戶端憑證，而且 BITS 作業未指定用戶端憑證時，作業將會失敗，並出現錯誤 (0x80072f0c) **\_ \_ \_ \_ \_ 所需的 WINHTTP 用戶端驗證** 憑證。

## <a name="how-to-handle-authenticated-proxy-scenarios-that-require-user-specific-settings"></a>如何處理需要使用者特定設定的已驗證 proxy 案例

如果您在需要 proxy 驗證的環境中使用 BITS，但在電腦的網路網域中，以沒有可用 NTLM 或 Kerberos 認證的帳戶執行時，您必須採取額外的步驟，以使用在網域上具有認證的另一個使用者帳戶的認證來正確進行驗證。 當您的位程式碼以系統服務（如 LocalService、NetworkService 或 LocalSystem）執行時，這是常見的案例，因為這些帳戶沒有可用的 NTLM 或 Kerberos 認證。

當設定網路協助程式權杖 (BG \_ 權杖網路) 時，BITS 中使用的 proxy 偵測邏輯會執行下列動作 \_ ：

-   如果 [**IBackgroundCopyJob：： SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) 是以 **BG \_ JOB \_ PROXY \_ USAGE \_ PRECONFIG** 呼叫，則請使用作業擁有者權杖內容模擬透過 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)來讀取本機 IE PROXY 設定。 從 Windows 10 版本 1809 (10.0;組建 17763) ，此步驟會使用 helper 權杖身分識別。
-   如果 [**IBackgroundCopyJob：： SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) 是以 [ **bg \_ proxy \_ 使用 \_** 方式自動偵測] 來呼叫，或從 [ **bg \_ 作業 \_ PROXY \_ 使用 \_** 方式] PRECONFIG 案例中的 IE 設定指定 [自動偵測] 或 [自動設定 URL]，則透過 [**WinHttpGetProxyForUrl**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl)使用協助程式權杖模擬來執行自動 PROXY 偵測或 Web PROXY 自動探索通訊協定 (WPAD) 。

之後，會在整個中使用協助程式權杖模擬進行 proxy 或伺服器驗證。

從 Windows 10 版本 1809 (10.0;組建 17763) ，已簡化驗證的 proxy 案例與使用者特定的認證。

1.  呼叫 BITS 作業的 [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 方法與 **bg \_ auth \_ 配置 \_ 協商**、將使用者 *名稱* 設定為 **Null**、將 *密碼* 設定為 **null**，並將 *目標* 設定為 **BG \_ 驗證 \_ 目標 \_ PROXY**。 這會導致使用者帳戶的隱含認證用於 proxy 和伺服器的 NTLM 和 Kerberos 驗證。
2.  呼叫 [**IBackgroundCopyJob：： SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) 與 **BG \_ JOB \_ PROXY \_ USAGE \_ PRECONFIG**。
3.  [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)的 QueryInterface。
4.  模擬您要用於 NTLM/Kerberos 認證的使用者帳戶。
5.  呼叫 [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)。
6. 使用 **BG \_ TOKEN \_ NETWORK** 呼叫 [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) 。
7. 還原模擬。
8. 繼續作業設定。
9. 在作業上呼叫 [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) 。

Windows 10 版本 1809 (10.0;組建 17763) ，協助程式權杖身分識別) 的正確使用者身分 (識別用於以網路為基礎的 proxy 偵測 (WPAD) 和 proxy 驗證，但即使已設定協助程式權杖，仍會使用作業擁有者的權杖來實際偵測本機 (IE) proxy 設定。 若要解決這項缺點，您可以遵循下列步驟。

1.  模擬您要用於 NTLM/Kerberos 認證的使用者帳戶。
2.  藉由呼叫 [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)來取得使用者帳戶的 IE proxy 設定。
3.  還原模擬。
4.  呼叫 BITS 作業的 [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) 方法與 **bg \_ auth \_ 配置 \_ 協商**、將使用者 *名稱* 設定為 **Null**、將 *密碼* 設定為 **null**，並將 *目標* 設定為 **BG \_ 驗證 \_ 目標 \_ PROXY**。 這會導致使用者帳戶的隱含認證用於 proxy 和伺服器的 NTLM 和 Kerberos 驗證。
5.  如果步驟2產生任何使用者專屬的 proxy 設定 (也就是 *lpszProxy* 或 *LpszProxyBypass* 不是 **Null**) ，請手動設定對應的工作設定，並使用 [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) 搭配 **BG \_ 工作 \_ proxy \_ 使用 \_** 方式覆寫設定。
6.  如果步驟2未產生任何使用者專屬的 proxy 設定，請以 **BG \_ 作業使用方式 \_ \_ PRECONFIG** 呼叫 [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) 。
7.  [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)的 QueryInterface。
8.  再次模擬使用者帳戶。
9.  呼叫 [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)。
10. 使用 **BG \_ TOKEN \_ NETWORK** 呼叫 [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) 。
11. 還原模擬。
12. 繼續作業設定。
13. 在作業上呼叫 [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) 。
