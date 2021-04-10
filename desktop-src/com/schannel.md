---
title: Schannel
description: 安全通道 (Schannel) 安全性套件，其驗證服務識別碼為 RPC \_ C \_ 驗證 GSS 安全通道 \_ \_ ，支援下列以公開金鑰為基礎的通訊協定： SSL (安全通訊端層) 2.0 和3.0 版、傳輸層安全性 (TLS) 1.0 和私用通訊技術 (PCT) 1.0。 TLS 1.0 是一種標準化、稍微修改的 SSL 3.0 版本，由網際網路工程任務推動小組 (IETF) 在檔 RFC 2246 中的1月1999日。 由於 TLS 已標準化，因此我們鼓勵開發人員使用 TLS，而不是使用 SSL。 PCT 是為了提供回溯相容性而包含，不應該用於新的開發。 使用安全通道安全性套件時，DCOM 會根據用戶端和伺服器的功能，自動協調最佳的通訊協定。
ms.assetid: 03a5f987-f668-4f19-9b58-d62711f58734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc9f82a05d1542e7585426128f10cdf452d31d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316570"
---
# <a name="schannel"></a>Schannel

安全通道 (Schannel) 安全性封裝，其驗證服務識別碼為 RPC \_ C \_ 驗證 GSS 安全通道 \_ \_ ，支援下列以公開金鑰為基礎的通訊協定： SSL (安全通訊端層) 2.0 和3.0 版、傳輸層安全性 (TLS) 1.0 和私用通訊技術 (PCT) 1.0。 TLS 1.0 是一種標準化、稍微修改的 SSL 3.0 版本，由網際網路工程任務推動小組 (IETF) 在檔 [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt)中的1月1999日。 由於 TLS 已標準化，因此我們鼓勵開發人員使用 TLS，而不是使用 SSL。 PCT 是為了提供回溯相容性而包含，不應該用於新的開發。 使用安全通道安全性套件時，DCOM 會根據用戶端和伺服器的功能，自動協調最佳的通訊協定。

下列主題簡要說明 TLS 通訊協定以及它與 DCOM 的搭配運作方式。

-   [使用 TLS 的時機](#when-to-use-tls)
-   [TLS 如何運作的簡短總覽](#brief-overview-of-how-tls-works)
-   [X.509 憑證](#x509-certificates)
    -   [用戶端憑證](#client-certificates)
-   [使用 COM 中的 TLS](#using-tls-in-com)
    -   [伺服器如何設定安全性綜合](#how-a-server-sets-the-security-blanket)
    -   [用戶端如何設定安全性的總](#how-a-client-sets-the-security-blanket)
    -   [用戶端如何變更安全性的總](#how-a-client-changes-the-security-blanket)
    -   [範例：用戶端變更安全性的總](#example-client-changes-the-security-blanket)
-   [相關主題](#related-topics)

> [!Note]  
> 在這些章節中，TLS 通訊協定的所有相關資訊也適用于 SSL 和 PCT 通訊協定。

 

## <a name="when-to-use-tls"></a>使用 TLS 的時機

當伺服器需要向匿名用戶端證明其身分識別時，TLS 是唯一可用的安全性選項。 這對於想要參與電子商務的網站來說特別重要，因為它可協助保護機密資訊的傳輸，例如信用卡號碼。 TLS 可確保電子商務客戶可以確定其執行業務的人員，因為它們會獲得伺服器身分識別的證明。 它也讓電子商務伺服器的效率不需要自行驗證其每個客戶的身分識別。

TLS 要求所有伺服器向用戶端證明其身分識別。 此外，TLS 提供讓用戶端向伺服器證明其身分識別的選項。 此相互驗證有助於限制大型公司內部網路中特定網頁的存取。

TLS 支援最強的驗證層級，並提供開放的架構，可讓加密強度隨著時間增加，以跟上技術創新。 對於傳輸中資料所需的最高層級安全性環境而言，TLS 是最好的選擇。

## <a name="brief-overview-of-how-tls-works"></a>TLS 如何運作的簡短總覽

TLS 是建立在公開金鑰基礎結構 (PKI) ，其使用公開/私密金鑰組來啟用資料加密和建立資料完整性，並使用 x.509 憑證進行驗證。

許多安全性通訊協定（例如 Kerberos v5 通訊協定）相依于單一金鑰來加密和解密資料。 因此，這類通訊協定取決於加密金鑰的安全交換;在 Kerberos 通訊協定中，這是透過從金鑰發佈中心 (KDC) 取得的票證來完成。 如此一來，使用 Kerberos 通訊協定的每個人都必須向 KDC 註冊，這對電子商務 web 伺服器來說是一項不實際的限制，旨在吸引全球數百萬名客戶。 因此，TLS 會依賴 PKI，這會使用兩個金鑰來進行資料 encryptionâ。」當其中一個索引鍵加密資料時，只有配對的另一個索引鍵可以解密。 這項設計的主要優點是可以執行加密，而不需要安全地交換加密金鑰。

PKI 使用的技巧是，其中一個金鑰會保留為私用，而且僅適用于它所註冊的主體，而另一個金鑰則公開給任何人存取。 如果有人想要將私用訊息傳送給金鑰組的擁有者，可以使用公開金鑰來加密訊息，而只有私密金鑰可以用來解密訊息。

金鑰組也用來驗證所傳送資料的完整性。 若要這樣做，金鑰組的擁有者可以在傳送數位簽章之前，先將數位簽章附加至資料。 建立數位簽章牽涉到計算資料的雜湊，並使用私密金鑰來加密雜湊。 使用公開金鑰解密數位簽章的任何人都可以確保數位簽章只能來自擁有私密金鑰的人員。 此外，收件者也可以使用與寄件者相同的演算法來計算資料的雜湊，而且如果匯出的雜湊符合數位簽章中傳送的雜湊，則收件者可以確定資料經過數位簽署之後不會修改。

使用 PKI 進行大量資料加密的其中一個缺點是其效能相對較慢。 由於涉及大量的數學運算，使用與金鑰組相依的非對稱式加密來加密和解密資料的速度，最高可達1000倍，但使用只依賴單一金鑰的對稱式加密和解密。 因此，TLS 只會使用 PKI 來產生數位簽章，以及協調用戶端和伺服器將用來進行大量資料加密和解密的會話特定單一金鑰。 TLS 支援各種不同的單一金鑰組稱式加密，未來可能會新增額外的密碼。

如需 TLS 交握通訊協定的詳細資訊，請參閱 [Tls 交握通訊協定](/windows/desktop/SecAuthN/tls-handshake-protocol)。

如需 TLS 通訊協定背後密碼編譯的詳細資訊，請參閱 [密碼編譯基本](/windows/desktop/SecCrypto/cryptography-essentials)資訊。

## <a name="x509-certificates"></a>X.509 憑證

PKI 必須處理的重大問題，就是能夠信任所使用公開金鑰的真實性。 當您使用發行給公司的公開金鑰，而該公司想要與公司合作時，您會想要確定金鑰實際上屬於公司，而不是想要探索您的信用卡號碼的竊賊。

為了保證持有金鑰組之主體的身分識別，主體是由憑證授權單位單位 (CA) 發出的 x.509 憑證。 此憑證包含可識別主體的資訊、包含主體的公開金鑰，且由 CA 進行數位簽署。 此數位簽章表示 CA 認為憑證中包含的公開金鑰確實屬於憑證所識別的主體。

那麼，您該如何信任 CA 呢？ 因為 CA 本身會保存由較高層級 CA 簽署的 x.509 憑證。 這一鏈的憑證簽章會繼續進行，直到到達根 CA，也就是簽署本身憑證的 CA。 如果您信任憑證根 CA 的完整性，您應該能夠信任憑證本身的真實性。 因此，挑選您願意信任的根 Ca 是系統管理員的重要責任。

### <a name="client-certificates"></a>用戶端憑證

當安全性傳輸層通訊協定第一次出現時，其主要目的是保證用戶端連線至真實的伺服器，並在傳輸時保護資料的隱私權。 不過，SSL 3.0 和 TLS 1.0 也支援在通訊協定交握期間傳輸用戶端的憑證。 這項選用功能可啟用用戶端和伺服器的相互驗證。

您應該在應用程式的內容中，決定是否要使用用戶端憑證。 如果主要需求是驗證服務器，就不需要用戶端憑證。 但是，如果用戶端驗證是必要的，則可以使用用戶端的憑證，而不是依賴應用程式內的自訂驗證。 使用用戶端憑證優於自訂驗證，因為它會為使用者提供單一登入案例。

## <a name="using-tls-in-com"></a>使用 COM 中的 TLS

TLS 僅支援模擬 (RPC \_ C \_ IMP \_ 層級模擬 \_) 的模擬層級。 如果 COM 將 TLS 協商為 proxy 上的驗證服務，則不論進程預設值為何，COM 都會將模擬等級設定為模擬。 為了讓模擬在 TLS 中正常運作，用戶端必須提供 x.509 憑證給伺服器，且伺服器必須將該憑證對應到伺服器上的特定使用者帳戶。 如需詳細資訊，請參閱將 [憑證對應至使用者帳戶的逐步指南](https://www.microsoft.com/isapi/redir.dll?prd=windows2000&sbp=technicallibrary&ar=security&sba=mappingcertificates)。

TLS 不支援 [掩蓋](cloaking.md)。 如果在 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 或 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) 呼叫中指定了遮蓋旗標和 TLS，將會 \_ 傳回 E INVALIDARG。

當驗證層級設定為 [無] 時，TLS 無法運作。 用戶端與伺服器之間的交握會檢查每個設定的驗證層級，並為連線選擇較高的安全性設定。

您可以藉由呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 和 [**COSETPROXYBLANKET**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)來設定 TLS 的安全性參數。 下列各節說明進行這些呼叫時所牽涉到的細微差異。

### <a name="how-a-server-sets-the-security-blanket"></a>伺服器如何設定安全性綜合

如果伺服器想要使用 TLS，它必須 \_ \_ \_ 在 CoInitializeSecurity 的 asAuthSvc 參數中指定 Schannel (RPC C 驗證 GSS \_ Schannel) 作為驗證服務。 [](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 為了防止用戶端使用較不安全的驗證服務連接到伺服器，伺服器在呼叫 **CoInitializeSecurity** 時，只能將 Schannel 指定為驗證服務。 伺服器在呼叫 **CoInitializeSecurity** 之後，就無法變更安全性的總。

若要使用 TLS，當伺服器呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時，應該指定下列參數：

-   *pVoid* 應該是 [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) 物件的指標或 [**安全 \_ 描述項**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)的指標。 它不能是 **Null** 或 AppID 的指標。
-   *cAuthSvc* 不可為0或-1。 當 *cAuthSvc* 為-1 時，COM 伺服器絕不會選擇 Schannel。
-   *asAuthSvc* 必須將 Schannel 指定為可能的驗證服務。 這是藉由為 [**唯一 \_ 驗證 \_ 清單**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list)的 Schannel 成員設定下列 [**唯一 \_ 驗證 \_ 服務**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)參數來完成的：
    -   *dwAuthnSvc* 必須是 RPC \_ C \_ 驗證 \_ GSS \_ SCHANNEL。
    -   *dwAuthzSvc* 應為「RPC \_ C \_ 授權無」 \_ 。 目前會忽略它。
    -   *pPrincipalName* 必須是指向憑證 [**\_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)的指標，轉換成 OLECHAR 的指標，代表伺服器的 x.509 憑證。
-   *dwAuthnLevel* 指出將從用戶端接收成功連線的最小驗證等級。 不可為 RPC \_ C \_ 驗證 \_ 層級 \_ 無。
-   *dwCapabilities* 不應 \_ 設定 EOAC APPID 旗標。 \_ \_ 如果 *pVoid* 指向 [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol)物件，則應設定 EOAC 存取控制旗標; *pVoid* 指向安全描述項時，不應設定此旗標 \_ 。 如需其他可能設定的旗標，請參閱 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)。

如需使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的詳細資訊，請參閱使用 [CoInitializeSecurity 設定 Processwide 安全性](setting-processwide-security-with-coinitializesecurity.md)。

### <a name="how-a-client-sets-the-security-blanket"></a>用戶端如何設定安全性的總

如果用戶端想要使用 TLS，它必須在 \_ \_ \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的 *pAuthList* 參數中，于其驗證服務清單中指定 schannel (RPC C 驗證 GSS Schannel) 。 如果在呼叫 **CoInitializeSecurity** 時未將 schannel 指定為可能的驗證服務，則在稍後呼叫 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) (或 [**IClientSecurity：：) SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) 時，如果嘗試將 schannel 指定為驗證服務，將會失敗。

當用戶端呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時，應該指定下列參數：

-   *dwAuthnLevel* 指定用戶端想要使用的預設驗證層級。 不可為 RPC \_ C \_ 驗證 \_ 層級 \_ 無。
-   *dwImpLevel* 必須是 RPC \_ C \_ IMP \_ 層級模擬 \_ 。
-   *pAuthList* 必須以下列 [**唯一的 \_ 驗證 \_ 資訊**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) 參數作為清單的成員：
    -   *dwAuthnSvc* 必須是 RPC \_ C \_ 驗證 \_ GSS \_ SCHANNEL。
    -   *dwAuthzSvc* 必須是 RPC \_ C \_ 授權 \_ 無。
    -   *pAuthInfo* 是指向憑證 [**\_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)的指標，轉換為 void 的指標，代表用戶端的 x.509 憑證。 如果用戶端沒有憑證，或不想將其憑證出示給伺服器， *pAuthInfo* 必須是 **Null** ，且伺服器會嘗試匿名連接。
-   *dwCapabilities* 是一組表示額外用戶端功能的旗標。 如需應設定哪些旗標的詳細資訊，請參閱 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 。

如需使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的詳細資訊，請參閱使用 [CoInitializeSecurity 設定 Processwide 安全性](setting-processwide-security-with-coinitializesecurity.md)。

### <a name="how-a-client-changes-the-security-blanket"></a>用戶端如何變更安全性的總

如果用戶端想要使用 TLS，但在呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)之後變更安全性階層，則必須呼叫 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) 或 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) ，並以與 **CoInitializeSecurity** 呼叫中使用的參數類似，但有下列差異：

-   *pServerPrincName* 以 msstd 或 fullsic 格式表示伺服器的主體名稱。 如需這些格式的詳細資訊，請參閱 [主體名稱](/windows/desktop/Rpc/principal-names)。 如果用戶端有伺服器的 x.509 憑證，它可以藉由呼叫 [**RpcCertGeneratePrincipalName**](/windows/desktop/api/rpcssl/nf-rpcssl-rpccertgenerateprincipalname)來尋找主體名稱。
-   *pAuthInfo* 是一種指向憑證 [**\_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)的指標，轉換為 RPC AUTH 身分 \_ \_ 識別控制碼的指標 \_ ，代表用戶端的 x.509 憑證。 如果用戶端沒有憑證，或不想將其憑證出示給伺服器， *pAuthInfo* 必須是 **Null** ，且伺服器會嘗試匿名連接。
-   *dwCapabilities* 包含表示額外用戶端功能的旗標。 只有四個旗標可以用來變更安全性的總設定： EOAC \_ 預設值、EOAC \_ 相互 \_ 驗證、EOAC \_ 任何 \_ 授權單位 (此旗標已淘汰) ，而且 EOAC \_ 設為 \_ FULLSIC。 如需詳細資訊，請參閱 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)。

如需使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)的詳細資訊，請參閱在 [介面 Proxy 層級設定安全性](setting-security-at-the-interface-proxy-level.md)。

### <a name="example-client-changes-the-security-blanket"></a>範例：用戶端變更安全性的總

下列範例會示範用戶端如何變更安全性，以容納來自伺服器的要求，以提供其 x.509 憑證給用戶端。 為了簡潔起見，已省略錯誤處理常式代碼。


```C++
void ClientChangesSecurity ()
{
  HCRYPTPROV                   provider           = 0;
  HCERTSTORE                   cert_store         = NULL;
  PCCERT_CONTEXT               client_cert        = NULL;
  PCCERT_CONTEXT               server_cert        = NULL;
  WCHAR                        *server_princ_name = NULL;
  ISecret                      *pSecret           = NULL;
  MULTI_QI                     server_instance;
  COSERVERINFO                 server_machine;
  SOLE_AUTHENTICATION_LIST     auth_list;
  SOLE_AUTHENTICATION_INFO     auth_info[1];



  // Specify all the authentication info. 
  // The client is willing to connect using SChannel,
  //   with no client certificate.
  auth_list.cAuthInfo     = 1;
  auth_list.aAuthInfo     = auth_info;
  auth_info[0].dwAuthnSvc = RPC_C_AUTHN_GSS_SCHANNEL;
  auth_info[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
  auth_info[0].pAuthInfo  = NULL;  // No certificate

  // Initialize client security with no client certificate.
  CoInitializeSecurity( NULL, -1, NULL, NULL,
                        RPC_C_AUTHN_LEVEL_PKT,
                        RPC_C_IMP_LEVEL_IMPERSONATE, &auth_list,
                        EOAC_NONE, NULL );
  
  // Specify info for the proxy.
  server_instance = {&IID_ISecret, NULL, S_OK};
  server_machine  = {0, L"ServerMachineName", NULL, 0};
  
  // Create a proxy.
  CoCreateInstanceEx( CLSID_Secret, NULL, CLSCTX_REMOTE_SERVER, 
                      &server_machine, 1, &server_instance);
  pSecret = (ISecret *) server_instance.pItf;

  //** The client obtained the server's certificate during the handshake.
  //** The server requests a certificate from the client.

  // Get the default certificate provider.
  CryptAcquireContext( &provider, NULL, NULL, PROV_RSA_SCHANNEL, 0 );

  // Open the certificate store.
  cert_store = CertOpenSystemStore( provider, L"my" );

  // Find the client's certificate.
  client_cert = 
    CertFindCertificateInStore( cert_store,
                                X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
                                0,
                                CERT_FIND_SUBJECT_STR,
                                L"ClientName",  // Use the principal name
                                NULL );

  // Find the fullsic principal name of the server.
  RpcCertGeneratePrincipalName( server_cert, RPC_C_FULL_CERT_CHAIN, 
                                &server_princ_name );

  // Change the client's security: 
  // Increase the authentication level and attach a certificate.
  CoSetProxyBlanket( pSecret, RPC_C_AUTHN_GSS_SCHANNEL,
                     RPC_C_AUTHZ_NONE,
                     server_princ_name, RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
                     RPC_C_IMP_LEVEL_IMPERSONATE, 
                     (RPC_AUTH_IDENTITY_HANDLE *) client_cert,
                     EOAC_NONE );

  cleanup:
  if (server_princ_name != NULL)
    RpcStringFree( &server_princ_name );
  if (client_cert != NULL)
    CertFreeCertificateContext(client_cert);
  if (server_cert != NULL)
    CertFreeCertificateContext(server_cert);
  if (cert_store != NULL)
    CertCloseStore( cert_store, CERT_CLOSE_STORE_CHECK_FLAG );
  if (provider != 0 )
    CryptReleaseContext( provider, 0 );
  if (pSecret != NULL)
    pSecret->Release();
  CoUninitialize();
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 和安全性封裝](com-and-security-packages.md)
</dt> </dl>

 

 