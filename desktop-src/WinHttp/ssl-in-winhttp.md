---
description: Microsoft Windows HTTP Services (WinHTTP) 支援安全通訊端層 (SSL) 包括用戶端憑證的交易。 本主題說明與 SSL 交易相關的概念，以及如何使用 WinHTTP 來處理它們。
ms.assetid: cb0a04f5-1026-4ad5-bb5b-c854064a5167
title: WinHTTP 中的 SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a041d55de85250edb1932aa3df4d114af8ef89fce6e56c3763cb235168b65be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133031"
---
# <a name="ssl-in-winhttp"></a>WinHTTP 中的 SSL

Microsoft Windows HTTP Services (WinHTTP) 支援安全通訊端層 (SSL) 包括用戶端憑證的交易。 本主題說明與 SSL 交易相關的概念，以及如何使用 WinHTTP 來處理它們。

## <a name="secure-sockets-layer"></a>安全通訊端層

SSL 是為了確保安全的 HTTP 交易而建立的標準。 SSL 提供一種機制，可在用戶端與伺服器之間的所有交易上執行最多128位加密。 它可讓用戶端透過使用伺服器憑證來確認伺服器是否屬於信任的實體。 它也可讓伺服器使用用戶端憑證來確認用戶端的身分識別。

當用戶端第一次從安全超文字傳輸通訊協定要求資源 (HTTPS) server 時，會在 SSL 交握中協商這些問題的每個問題。 基本上，用戶端和伺服器會顯示必要和慣用設定的清單。 如果可以同意並符合一組常見的需求，則會建立 SSL 連線。

WinHTTP 提供使用 SSL 的高層級介面。 雖然 SSL 信號交換和交易的詳細資料會在內部處理，但是 WinHTTP 可讓您取得加密層級、指定安全性通訊協定，以及與伺服器和用戶端憑證互動。 下列各節提供有關建立以 WinHTTP 為基礎之應用程式的詳細資料，可選擇 SSL 通訊協定版本、檢查伺服器憑證，以及選取要傳送至 HTTPS 伺服器的用戶端憑證。

## <a name="server-certificates"></a>伺服器憑證

伺服器憑證會從伺服器傳送至用戶端，讓用戶端可以取得伺服器的公開金鑰，並確保伺服器已通過憑證授權單位單位的驗證。 憑證可包含不同的資料類型。 例如，x.509 憑證包含憑證的格式、憑證的序號、用來簽署憑證的演算法、頒發證書的憑證授權單位單位名稱 (CA) 、要求憑證的機構名稱和公開金鑰，以及 CA 的簽章等的格式。

使用 (API) 的 WinHTTP 應用程式開發介面時，您可以藉由呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) 並指定 [**WinHTTP \_ 選項 \_ 安全性 \_ 憑證 \_ 結構**](option-flags.md) 旗標，來取得伺服器憑證。 伺服器憑證會以 [**WINHTTP \_ 憑證 \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) 結構傳回。 如果您想要取出憑證內容，請改為指定 [**WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 內容**](option-flags.md) 旗標。

如果伺服器憑證包含錯誤，則可在狀態回呼函數中取得錯誤的詳細資料。 [**WINHTTP \_ 回呼 \_ 狀態 \_ 安全 \_ 失敗**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback)通知指出伺服器憑證發生錯誤。 *LpvStatusInformation* 參數包含一或多個詳細的錯誤旗標。 如需詳細資訊，請參閱 [**WINHTTP \_ 狀態 \_ 回呼**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) 。

## <a name="client-certificates"></a>用戶端憑證

在 SSL 交握期間，伺服器可能需要驗證。 用戶端會藉由提供有效的用戶端憑證給伺服器來進行驗證。 WinHTTP 可讓您從本機 [*憑證存放區*](glossary.md)選取和傳送憑證。 下列各節說明使用 WinHTTP API 或 [**WinHttpRequest**](winhttprequest.md) 物件時提供用戶端憑證的程式。

### <a name="winhttp-api"></a>WinHTTP API

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)和 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)都可能無法表示要求失敗，因為 HTTPS 伺服器需要驗證。 在這些情況下，呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以傳回 \_ \_ \_ \_ \_ 所需的錯誤 WINHTTP 用戶端驗證憑證。 收到此錯誤時，請使用適當的 [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) 函數來尋找適當的憑證。 使用 [**WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容**](option-flags.md)旗標來呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) ，以指出應以下一個要求傳送此憑證。

下列程式碼範例示範如何根據主體名稱開啟 [*憑證存放區*](glossary.md) ，並在 \_ 傳回錯誤 WINHTTP \_ 用戶端 \_ 驗證憑證 \_ \_ 所需的錯誤之後，找出以主體名稱為基礎的憑證。


```C++
  if( !WinHttpReceiveResponse( hRequest, NULL ) )
  {
    if( GetLastError( ) == ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED )
    {
      //MY is the store the certificate is in.
      hMyStore = CertOpenSystemStore( 0, TEXT("MY") );
      if( hMyStore )
      {
        pCertContext = CertFindCertificateInStore( hMyStore,
             X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
             0,
             CERT_FIND_SUBJECT_STR,
             (LPVOID) szCertName, //Subject string in the certificate.
             NULL );
        if( pCertContext )
        {
          WinHttpSetOption( hRequest, 
                            WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                            (LPVOID) pCertContext, 
                            sizeof(CERT_CONTEXT) );
          CertFreeCertificateContext( pCertContext );
        }
        CertCloseStore( hMyStore, 0 );

        // NOTE: Application should now resend the request.
      }
    }
  }
```



重新傳送包含用戶端憑證的要求之前，您可以判斷您的應用程式是否可接受支援的加密層級。 呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) 並指定 [**WINHTTP \_ 選項 \_ 安全性 \_ 旗標旗標**](option-flags.md) ，以判斷所使用的加密層級。

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a>SSL 用戶端驗證的簽發者清單抓取

當 WinHttp 用戶端應用程式傳送要求至需要 SSL 用戶端驗證的安全 HTTP 伺服器時，如果應用程式未提供用戶端憑證，WinHttp 會傳回 **\_ \_ \_ \_ \_ 所需的錯誤 winHTTP 用戶端驗證** 憑證。 針對 Windows Server 2008 和 Windows Vista 上執行的電腦，WinHttp 可讓應用程式在驗證挑戰中，取得伺服器提供的憑證簽發者清單。 簽發者清單會指定伺服器授權的憑證授權單位單位清單， () Ca 以發出用戶端憑證。 應用程式會篩選簽發者清單，以取得所需的憑證。

當 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)或 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 傳回 **\_ \_ \_ \_ \_ 所需的錯誤 WinHttp 用戶端驗證** 憑證時，WinHttp 用戶端應用程式會抓取簽發者清單。 當傳回此錯誤時，應用程式會使用 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單** 選項來呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) 。 *LpBuffer* 參數必須夠大，才能包含 [SecPkgCoNtext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)結構的指標。 下列程式碼範例示範如何取出簽發者清單。


```C++
#include <windows.h>
#include <winhttp.h>
#include <schannel.h>

//...

void GetIssuerList(HINTERNET hRequest)
{
  SecPkgContext_IssuerListInfoEx* pIssuerList = NULL;
  DWORD dwBufferSize = sizeof(SecPkgContext_IssuerListInfoEx*);

  if (WinHttpQueryOption(hRequest,
           WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST,
           &pIssuerList,
           &dwBufferSize) == TRUE)
  {
    // Use the pIssuerList for cert store filtering.
    GlobalFree(pIssuerList); // Free the issuer list when done.
  }
}
```



您可以使用 [SecPkgCoNtext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) 結構 *cIssuers* 和 *aIssuers* 中的資訊來搜尋憑證，如下列程式碼範例所示。 如需詳細資訊，請參閱 [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore)。


```C++
PCERT_CONTEXT pClientCert = NULL;
PCCERT_CHAIN_CONTEXT pClientCertChain = NULL;

CERT_CHAIN_FIND_BY_ISSUER_PARA SrchCriteria;
::ZeroMemory(&SrchCriteria, sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA));
SrchCriteria.cbSize = sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA);

SrchCriteria.cIssuer = pIssuerList->cIssuers;
SrchCriteria.rgIssuer = pIssuerList->aIssuers;

pClientCertChain = CertFindChainInStore(
            hClientCertStore,
            X509_ASN_ENCODING,
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_URL_FLAG |
            // Do not perform wire download when building chains.
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_FLAG,
            // Do not search pCacheEntry->_ClientCertStore 
            // for issuer certs.
            CERT_CHAIN_FIND_BY_ISSUER,
            &SrchCriteria,
            NULL);

if (pClientCertChain)
{
    pClientCert = (PCERT_CONTEXT) pClientCertChain->rgpChain[0]->rgpElement[0]->pCertContext;

    CertDuplicateCertificateContext(pClientCert);

    CertFreeCertificateChain(pClientCertChain);

    pClientCertChain = NULL;
}
```



### <a name="optional-client-ssl-certificates"></a>選用用戶端 SSL 憑證

從 Windows Server 2008 和 Windows Vista 開始，WinHttp API 支援選用用戶端憑證。 當伺服器要求用戶端憑證、 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)或 [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 時，會傳回 **錯誤 \_ WINHTTP \_ 用戶端 \_ 驗證憑證 \_ \_ 所需** 的錯誤。 如果伺服器要求憑證，但不需要憑證，則應用程式可以指定此選項來指出它沒有憑證。 伺服器可以選擇其他驗證配置，或允許匿名存取伺服器。 應用程式會在 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)的 *lpBuffer* 參數中指定 **WINHTTP \_ NO \_ CLIENT \_ CERT \_ CONTEXT** 宏，如下列程式碼範例所示。

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

如果 **WINHTTP \_ 沒有設定 \_ 用戶端憑證 \_ \_ 內容** ，而且伺服器仍然需要用戶端憑證，則可能會傳送 403 HTTP 狀態碼。 如需詳細資訊，請參閱 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單** 選項。

### <a name="winhttprequest-object"></a>WinHttpRequest 物件

使用 [**WinHttpRequest**](winhttprequest.md)物件的 [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)方法，選取要以要求傳送至伺服器的用戶端憑證。 藉由使用 [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) 方法指定憑證選取字串來選取憑證。 憑證選取字串是由憑證位置、 [*憑證存放區*](glossary.md)和以反斜線分隔的主體名稱所組成。 下表列出此選取字串的元件。



| 元件                                                  | 描述                                                                                                                                                                                        | 可能值                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 位置                                                   | 判斷用來儲存憑證的登錄機碼。                                                                                                                               | 可能的值為「本機 \_ 電腦」，表示 [*憑證存放區*](glossary.md) 位於 **HKEY \_ 本機 \_ 電腦**<br/> 和「目前 \_ 使用者」表示 *憑證存放區* 是在非模擬的 **HKEY \_ 目前 \_ 使用者下。**<br/> 此元件會區分大小寫。 |
| [*憑證存放區*](glossary.md) | 指出包含相關憑證的 [*憑證存放區*](glossary.md) 名稱。                                                                       | 一般 [*憑證存放區*](glossary.md) 為 "MY"、"Root" 和 "TrustedPeople"。 此元件會區分大小寫。                                                                                                                                                                                          |
| 主體名稱                                               | 識別指定 [*憑證存放區*](glossary.md)中的憑證。 已選取包含此元件所指定之字串的第一個憑證。 | 主體名稱可以是任何字串。 空白字串表示應使用 [*憑證存放區*](glossary.md) 中的第一個憑證。 此元件不區分大小寫。                                                                                                                         |



 

[*憑證存放區*](glossary.md)名稱和位置是選用的元件。 但是，如果您指定 *憑證存放區*，您也必須指定該 *憑證存放區* 的位置。 預設位置是 [目前 \_ 使用者]，預設 *憑證存放區* 為 [我的]。

下列程式碼範例示範如何指定應從 **HKEY \_ 本機 \_ 電腦** 下登錄中的「個人」[*憑證存放區*](glossary.md)選擇具有「我的 Middle-Tier 憑證」主體的憑證。

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> 在某些語言中，反斜線是一個 escape 字元。 請記得修改憑證選取字串以考慮此情況。 例如，在 Microsoft JScript 中，請使用兩個連續的反斜線，而不是一個。

 

如果您未指定憑證，而 HTTPS 伺服器需要用戶端憑證，WinHTTP 會選取預設 [*憑證存放區*](glossary.md)中的第一個憑證。 如果沒有憑證存在，則會引發錯誤。 如果未接受憑證，伺服器會傳回403狀態碼，指出無法完成要求。 然後，您可以使用 [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) 選擇更適當的憑證，然後重新傳送要求。

 

