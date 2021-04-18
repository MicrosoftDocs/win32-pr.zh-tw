---
description: Microsoft Windows HTTP Services (WinHTTP) 支援安全通訊端層 (SSL) 包括用戶端憑證的交易。 本主題說明與 SSL 交易相關的概念，以及如何使用 WinHTTP 來處理它們。
ms.assetid: cb0a04f5-1026-4ad5-bb5b-c854064a5167
title: WinHTTP 中的 SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7952bb9a0227017927452502352c0354e69079c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193265"
---
# <a name="ssl-in-winhttp"></a><span data-ttu-id="7f77c-104">WinHTTP 中的 SSL</span><span class="sxs-lookup"><span data-stu-id="7f77c-104">SSL in WinHTTP</span></span>

<span data-ttu-id="7f77c-105">Microsoft Windows HTTP Services (WinHTTP) 支援安全通訊端層 (SSL) 包括用戶端憑證的交易。</span><span class="sxs-lookup"><span data-stu-id="7f77c-105">Microsoft Windows HTTP Services (WinHTTP) supports Secure Sockets Layer (SSL) transactions including client certificates.</span></span> <span data-ttu-id="7f77c-106">本主題說明與 SSL 交易相關的概念，以及如何使用 WinHTTP 來處理它們。</span><span class="sxs-lookup"><span data-stu-id="7f77c-106">This topic explains concepts involved in an SSL transaction and how they are handled using WinHTTP.</span></span>

## <a name="secure-sockets-layer"></a><span data-ttu-id="7f77c-107">安全通訊端層</span><span class="sxs-lookup"><span data-stu-id="7f77c-107">Secure Sockets Layer</span></span>

<span data-ttu-id="7f77c-108">SSL 是為了確保安全的 HTTP 交易而建立的標準。</span><span class="sxs-lookup"><span data-stu-id="7f77c-108">SSL is an established standard for ensuring secure HTTP transactions.</span></span> <span data-ttu-id="7f77c-109">SSL 提供一種機制，可在用戶端與伺服器之間的所有交易上執行最多128位加密。</span><span class="sxs-lookup"><span data-stu-id="7f77c-109">SSL provides a mechanism to perform up to 128-bit encryption on all transactions between the client and server.</span></span> <span data-ttu-id="7f77c-110">它可讓用戶端透過使用伺服器憑證來確認伺服器是否屬於信任的實體。</span><span class="sxs-lookup"><span data-stu-id="7f77c-110">It enables the client to verify that the server belongs to a trusted entity through the use of server certificates.</span></span> <span data-ttu-id="7f77c-111">它也可讓伺服器使用用戶端憑證來確認用戶端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="7f77c-111">It also enables the server to confirm the identity of the client with client certificates.</span></span>

<span data-ttu-id="7f77c-112">當用戶端第一次從安全超文字傳輸通訊協定要求資源 (HTTPS) server 時，會在 SSL 交握中協商這些問題的每個問題。</span><span class="sxs-lookup"><span data-stu-id="7f77c-112">Each of these issues encryption, server identity, and client identity are negotiated in the SSL handshake that occurs when a client first requests a resource from a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span> <span data-ttu-id="7f77c-113">基本上，用戶端和伺服器會顯示必要和慣用設定的清單。</span><span class="sxs-lookup"><span data-stu-id="7f77c-113">Essentially, the client and server each present a list of required and preferred settings.</span></span> <span data-ttu-id="7f77c-114">如果可以同意並符合一組常見的需求，則會建立 SSL 連線。</span><span class="sxs-lookup"><span data-stu-id="7f77c-114">If a common set of requirements can be agreed upon and met, an SSL connection is established.</span></span>

<span data-ttu-id="7f77c-115">WinHTTP 提供使用 SSL 的高層級介面。</span><span class="sxs-lookup"><span data-stu-id="7f77c-115">WinHTTP provides a high level interface for using SSL.</span></span> <span data-ttu-id="7f77c-116">雖然 SSL 信號交換和交易的詳細資料會在內部處理，但是 WinHTTP 可讓您取得加密層級、指定安全性通訊協定，以及與伺服器和用戶端憑證互動。</span><span class="sxs-lookup"><span data-stu-id="7f77c-116">While the details of the SSL handshake and transaction are handled internally, WinHTTP enables you to retrieve encryption levels, specify the security protocol, and interact with server and client certificates.</span></span> <span data-ttu-id="7f77c-117">下列各節提供有關建立以 WinHTTP 為基礎之應用程式的詳細資料，可選擇 SSL 通訊協定版本、檢查伺服器憑證，以及選取要傳送至 HTTPS 伺服器的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-117">The following sections provide details on creating WinHTTP based applications that elect an SSL protocol version, examine server certificates, and select client certificates to send to HTTPS servers.</span></span>

## <a name="server-certificates"></a><span data-ttu-id="7f77c-118">伺服器憑證</span><span class="sxs-lookup"><span data-stu-id="7f77c-118">Server Certificates</span></span>

<span data-ttu-id="7f77c-119">伺服器憑證會從伺服器傳送至用戶端，讓用戶端可以取得伺服器的公開金鑰，並確保伺服器已通過憑證授權單位單位的驗證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-119">Server certificates are sent from the server to the client so that the client can obtain a public key for the server and ensure that the server has been verified by a certification authority.</span></span> <span data-ttu-id="7f77c-120">憑證可包含不同的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7f77c-120">Certificates can contain different types of data.</span></span> <span data-ttu-id="7f77c-121">例如，x.509 憑證包含憑證的格式、憑證的序號、用來簽署憑證的演算法、頒發證書的憑證授權單位單位名稱 (CA) 、要求憑證的機構名稱和公開金鑰，以及 CA 的簽章等的格式。</span><span class="sxs-lookup"><span data-stu-id="7f77c-121">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the certification authority (CA) that issued the certificate, the name and public key of the entity that requests the certificate, and the CA's signature.</span></span>

<span data-ttu-id="7f77c-122">使用 (API) 的 WinHTTP 應用程式開發介面時，您可以藉由呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) 並指定 [**WinHTTP \_ 選項 \_ 安全性 \_ 憑證 \_ 結構**](option-flags.md) 旗標，來取得伺服器憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-122">When using the WinHTTP  application programming interface (API), you can retrieve a server certificate by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specifying the [**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**](option-flags.md) flag.</span></span> <span data-ttu-id="7f77c-123">伺服器憑證會以 [**WINHTTP \_ 憑證 \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) 結構傳回。</span><span class="sxs-lookup"><span data-stu-id="7f77c-123">The server certificate is returned in a [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="7f77c-124">如果您想要取出憑證內容，請改為指定 [**WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 內容**](option-flags.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="7f77c-124">If you prefer to retrieve the certificate context, specify the [**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**](option-flags.md) flag instead.</span></span>

<span data-ttu-id="7f77c-125">如果伺服器憑證包含錯誤，則可在狀態回呼函數中取得錯誤的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7f77c-125">If a server certificate contains errors, details about the error can be obtained in the status callback function.</span></span> <span data-ttu-id="7f77c-126">[**WINHTTP \_ 回呼 \_ 狀態 \_ 安全 \_ 失敗**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback)通知指出伺服器憑證發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="7f77c-126">The [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification indicates an error with a server certificate.</span></span> <span data-ttu-id="7f77c-127">*LpvStatusInformation* 參數包含一或多個詳細的錯誤旗標。</span><span class="sxs-lookup"><span data-stu-id="7f77c-127">The *lpvStatusInformation* parameter contains one or more detailed error flags.</span></span> <span data-ttu-id="7f77c-128">如需詳細資訊，請參閱 [**WINHTTP \_ 狀態 \_ 回呼**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) 。</span><span class="sxs-lookup"><span data-stu-id="7f77c-128">See [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) for more information.</span></span>

## <a name="client-certificates"></a><span data-ttu-id="7f77c-129">用戶端憑證</span><span class="sxs-lookup"><span data-stu-id="7f77c-129">Client Certificates</span></span>

<span data-ttu-id="7f77c-130">在 SSL 交握期間，伺服器可能需要驗證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-130">During the SSL handshake, the server might require authentication.</span></span> <span data-ttu-id="7f77c-131">用戶端會藉由提供有效的用戶端憑證給伺服器來進行驗證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-131">The client is authenticated by supplying a valid client certificate to the server.</span></span> <span data-ttu-id="7f77c-132">WinHTTP 可讓您從本機 [*憑證存放區*](glossary.md)選取和傳送憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-132">WinHTTP enables you to select and send a certificate from a local [*certificate store*](glossary.md).</span></span> <span data-ttu-id="7f77c-133">下列各節說明使用 WinHTTP API 或 [**WinHttpRequest**](winhttprequest.md) 物件時提供用戶端憑證的程式。</span><span class="sxs-lookup"><span data-stu-id="7f77c-133">The following sections describe the process that provides client certificates when using either the WinHTTP API or the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

### <a name="winhttp-api"></a><span data-ttu-id="7f77c-134">WinHTTP API</span><span class="sxs-lookup"><span data-stu-id="7f77c-134">WinHTTP API</span></span>

<span data-ttu-id="7f77c-135">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)和 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)都可能無法表示要求失敗，因為 HTTPS 伺服器需要驗證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-135">Both [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) and [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) can fail to indicate that a request was unsuccessful because the HTTPS server requires authentication.</span></span> <span data-ttu-id="7f77c-136">在這些情況下，呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以傳回 \_ \_ \_ \_ \_ 所需的錯誤 WINHTTP 用戶端驗證憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-136">In these cases, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to returns ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED.</span></span> <span data-ttu-id="7f77c-137">收到此錯誤時，請使用適當的 [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) 函數來尋找適當的憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-137">Upon receiving this error, use the appropriate [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) functions to find an appropriate certificate.</span></span> <span data-ttu-id="7f77c-138">使用 [**WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容**](option-flags.md)旗標來呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) ，以指出應以下一個要求傳送此憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-138">Indicate that this certificate should be sent with the next request by calling [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the [**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**](option-flags.md) flag.</span></span>

<span data-ttu-id="7f77c-139">下列程式碼範例示範如何根據主體名稱開啟 [*憑證存放區*](glossary.md) ，並在 \_ 傳回錯誤 WINHTTP \_ 用戶端 \_ 驗證憑證 \_ \_ 所需的錯誤之後，找出以主體名稱為基礎的憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-139">The following code example shows how to open a [*certificate store*](glossary.md) and locate a certificate based on subject name after the ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED error has been returned.</span></span>


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



<span data-ttu-id="7f77c-140">重新傳送包含用戶端憑證的要求之前，您可以判斷您的應用程式是否可接受支援的加密層級。</span><span class="sxs-lookup"><span data-stu-id="7f77c-140">Before resending a request that contains a client certificate, you can determine if the supported level of encryption is acceptable for your application.</span></span> <span data-ttu-id="7f77c-141">呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) 並指定 [**WINHTTP \_ 選項 \_ 安全性 \_ 旗標旗標**](option-flags.md) ，以判斷所使用的加密層級。</span><span class="sxs-lookup"><span data-stu-id="7f77c-141">Call [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specify the [**WINHTTP\_OPTION\_SECURITY\_FLAGS**](option-flags.md) flag to determine the level of encryption that is used.</span></span>

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a><span data-ttu-id="7f77c-142">SSL 用戶端驗證的簽發者清單抓取</span><span class="sxs-lookup"><span data-stu-id="7f77c-142">Issuer List Retrieval for SSL Client Authentication</span></span>

<span data-ttu-id="7f77c-143">當 WinHttp 用戶端應用程式傳送要求至需要 SSL 用戶端驗證的安全 HTTP 伺服器時，如果應用程式未提供用戶端憑證，WinHttp 會傳回 **\_ \_ \_ \_ \_ 所需的錯誤 winHTTP 用戶端驗證** 憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-143">When the WinHttp client application sends a request to a secure HTTP server that requires SSL client authentication, WinHttp returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** if the application has not supplied a client certificate.</span></span> <span data-ttu-id="7f77c-144">針對在 Windows Server 2008 和 Windows Vista 上執行的電腦，WinHttp 可讓應用程式在驗證挑戰中，取得伺服器提供的憑證簽發者清單。</span><span class="sxs-lookup"><span data-stu-id="7f77c-144">For computers running on Windows Server 2008 and Windows Vista, WinHttp enables the application to retrieve the certificate issuer list supplied by the server in the authentication challenge.</span></span> <span data-ttu-id="7f77c-145">簽發者清單會指定伺服器授權的憑證授權單位單位清單， () Ca 以發出用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-145">The Issuer List specifies a list of Certificate Authorities (CAs) that are authorized by the server to issue client certificates.</span></span> <span data-ttu-id="7f77c-146">應用程式會篩選簽發者清單，以取得所需的憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-146">The application filters the issuer list to obtain the required certificate.</span></span>

<span data-ttu-id="7f77c-147">當 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)或 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 傳回 **\_ \_ \_ \_ \_ 所需的錯誤 WinHttp 用戶端驗證** 憑證時，WinHttp 用戶端應用程式會抓取簽發者清單。</span><span class="sxs-lookup"><span data-stu-id="7f77c-147">The WinHttp client application retrieves the issuer list when [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="7f77c-148">當傳回此錯誤時，應用程式會使用 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單** 選項來呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) 。</span><span class="sxs-lookup"><span data-stu-id="7f77c-148">When this error is returned, the application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="7f77c-149">*LpBuffer* 參數必須夠大，才能包含 [SecPkgCoNtext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7f77c-149">The *lpBuffer* parameter must be large enough to contain a pointer to the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure.</span></span> <span data-ttu-id="7f77c-150">下列程式碼範例示範如何取出簽發者清單。</span><span class="sxs-lookup"><span data-stu-id="7f77c-150">The following code example shows how to retrieve the issuer list.</span></span>


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



<span data-ttu-id="7f77c-151">您可以使用 [SecPkgCoNtext \_ IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) 結構 *cIssuers* 和 *aIssuers* 中的資訊來搜尋憑證，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="7f77c-151">The information in the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure, *cIssuers* and *aIssuers*, can be used to search for the certificate as shown in the code example below.</span></span> <span data-ttu-id="7f77c-152">如需詳細資訊，請參閱 [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore)。</span><span class="sxs-lookup"><span data-stu-id="7f77c-152">For more information, see [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span></span>


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



### <a name="optional-client-ssl-certificates"></a><span data-ttu-id="7f77c-153">選用用戶端 SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="7f77c-153">Optional Client SSL Certificates</span></span>

<span data-ttu-id="7f77c-154">從 Windows Server 2008 和 Windows Vista 開始，WinHttp API 支援選用用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-154">Starting in Windows Server 2008 and Windows Vista, the WinHttp API supports optional client certificates.</span></span> <span data-ttu-id="7f77c-155">當伺服器要求用戶端憑證、 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)或 [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 時，會傳回 **錯誤 \_ WINHTTP \_ 用戶端 \_ 驗證憑證 \_ \_ 所需** 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7f77c-155">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** error.</span></span> <span data-ttu-id="7f77c-156">如果伺服器要求憑證，但不需要憑證，則應用程式可以指定此選項來指出它沒有憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-156">If the server requests the certificate, but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="7f77c-157">伺服器可以選擇其他驗證配置，或允許匿名存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="7f77c-157">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="7f77c-158">應用程式會在 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)的 *lpBuffer* 參數中指定 **WINHTTP \_ NO \_ CLIENT \_ CERT \_ CONTEXT** 宏，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="7f77c-158">The application specifies the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

<span data-ttu-id="7f77c-159">如果 **WINHTTP \_ 沒有設定 \_ 用戶端憑證 \_ \_ 內容** ，而且伺服器仍然需要用戶端憑證，則可能會傳送 403 HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="7f77c-159">If the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** is set, and the server still requires a client certificate, it may send a 403 HTTP status code.</span></span> <span data-ttu-id="7f77c-160">如需詳細資訊，請參閱 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單** 選項。</span><span class="sxs-lookup"><span data-stu-id="7f77c-160">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

### <a name="winhttprequest-object"></a><span data-ttu-id="7f77c-161">WinHttpRequest 物件</span><span class="sxs-lookup"><span data-stu-id="7f77c-161">WinHttpRequest Object</span></span>

<span data-ttu-id="7f77c-162">使用 [**WinHttpRequest**](winhttprequest.md)物件的 [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md)方法，選取要以要求傳送至伺服器的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-162">Use the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method of the [**WinHttpRequest**](winhttprequest.md) object to select client certificates to send to the server with a request.</span></span> <span data-ttu-id="7f77c-163">藉由使用 [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) 方法指定憑證選取字串來選取憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-163">Select a certificate by specifying a certificate selection string with the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method.</span></span> <span data-ttu-id="7f77c-164">憑證選取字串是由憑證位置、 [*憑證存放區*](glossary.md)和以反斜線分隔的主體名稱所組成。</span><span class="sxs-lookup"><span data-stu-id="7f77c-164">The certificate selection string consists of the certificate location, [*certificate store*](glossary.md), and subject name delimited by backslashes.</span></span> <span data-ttu-id="7f77c-165">下表列出此選取字串的元件。</span><span class="sxs-lookup"><span data-stu-id="7f77c-165">The following table lists components for this selection string.</span></span>



| <span data-ttu-id="7f77c-166">元件</span><span class="sxs-lookup"><span data-stu-id="7f77c-166">Component</span></span>                                                  | <span data-ttu-id="7f77c-167">描述</span><span class="sxs-lookup"><span data-stu-id="7f77c-167">Description</span></span>                                                                                                                                                                                        | <span data-ttu-id="7f77c-168">可能值</span><span class="sxs-lookup"><span data-stu-id="7f77c-168">Possible values</span></span>                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f77c-169">Location</span><span class="sxs-lookup"><span data-stu-id="7f77c-169">Location</span></span>                                                   | <span data-ttu-id="7f77c-170">判斷用來儲存憑證的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="7f77c-170">Determines the registry key under which the certificates are stored.</span></span>                                                                                                                               | <span data-ttu-id="7f77c-171">可能的值為「本機 \_ 電腦」，表示 [*憑證存放區*](glossary.md) 位於 **HKEY \_ 本機 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="7f77c-171">The possible values are "LOCAL\_MACHINE" to indicate that the [*certificate store*](glossary.md) is under **HKEY\_LOCAL\_MACHINE**</span></span><br/> <span data-ttu-id="7f77c-172">和「目前 \_ 使用者」表示 *憑證存放區* 是在非模擬的 **HKEY \_ 目前 \_ 使用者下。**</span><span class="sxs-lookup"><span data-stu-id="7f77c-172">and "CURRENT\_USER" to indicate that the *certificate store* is under the non-impersonated **HKEY\_CURRENT\_USER.**</span></span><br/> <span data-ttu-id="7f77c-173">此元件會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7f77c-173">This component is case-sensitive.</span></span> |
| [<span data-ttu-id="7f77c-174">*憑證存放區*</span><span class="sxs-lookup"><span data-stu-id="7f77c-174">*Certificate store*</span></span>](glossary.md) | <span data-ttu-id="7f77c-175">指出包含相關憑證的 [*憑證存放區*](glossary.md) 名稱。</span><span class="sxs-lookup"><span data-stu-id="7f77c-175">Indicates the name of the [*certificate store*](glossary.md) that contains the relevant certificate.</span></span>                                                                       | <span data-ttu-id="7f77c-176">一般 [*憑證存放區*](glossary.md) 為 "MY"、"Root" 和 "TrustedPeople"。</span><span class="sxs-lookup"><span data-stu-id="7f77c-176">Typical [*certificate stores*](glossary.md) are "MY", "Root", and "TrustedPeople".</span></span> <span data-ttu-id="7f77c-177">此元件會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7f77c-177">This component is case-sensitive.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="7f77c-178">主體名稱</span><span class="sxs-lookup"><span data-stu-id="7f77c-178">Subject name</span></span>                                               | <span data-ttu-id="7f77c-179">識別指定 [*憑證存放區*](glossary.md)中的憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-179">Identifies a certificate within the specified [*certificate store*](glossary.md).</span></span> <span data-ttu-id="7f77c-180">已選取包含此元件所指定之字串的第一個憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-180">The first certificate that contains the string specified for this component is selected.</span></span> | <span data-ttu-id="7f77c-181">主體名稱可以是任何字串。</span><span class="sxs-lookup"><span data-stu-id="7f77c-181">The subject name can be any string.</span></span> <span data-ttu-id="7f77c-182">空白字串表示應使用 [*憑證存放區*](glossary.md) 中的第一個憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-182">A blank string indicates that the first certificate in the [*certificate store*](glossary.md) should be used.</span></span> <span data-ttu-id="7f77c-183">此元件不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7f77c-183">This component is case-insensitive.</span></span>                                                                                                                         |



 

<span data-ttu-id="7f77c-184">[*憑證存放區*](glossary.md)名稱和位置是選用的元件。</span><span class="sxs-lookup"><span data-stu-id="7f77c-184">The [*certificate store*](glossary.md) name and location are optional components.</span></span> <span data-ttu-id="7f77c-185">但是，如果您指定 *憑證存放區*，您也必須指定該 *憑證存放區* 的位置。</span><span class="sxs-lookup"><span data-stu-id="7f77c-185">However, if you specify a *certificate store*, you must also specify the location of that *certificate store*.</span></span> <span data-ttu-id="7f77c-186">預設位置是 [目前 \_ 使用者]，預設 *憑證存放區* 為 [我的]。</span><span class="sxs-lookup"><span data-stu-id="7f77c-186">The default location is CURRENT\_USER and the default *certificate store* is "MY".</span></span>

<span data-ttu-id="7f77c-187">下列程式碼範例示範如何指定應從 **HKEY \_ 本機 \_ 電腦** 下登錄中的「個人」[*憑證存放區*](glossary.md)選擇具有「我的 Middle-Tier 憑證」主體的憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-187">The following code example shows how to specify that a certificate with the subject "My Middle-Tier Certificate" should be chosen from the "Personal" [*certificate store*](glossary.md) in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> <span data-ttu-id="7f77c-188">在某些語言中，反斜線是一個 escape 字元。</span><span class="sxs-lookup"><span data-stu-id="7f77c-188">In some languages the backslash is an escape character.</span></span> <span data-ttu-id="7f77c-189">請記得修改憑證選取字串以考慮此情況。</span><span class="sxs-lookup"><span data-stu-id="7f77c-189">Remember to modify the certificate selection string to account for this.</span></span> <span data-ttu-id="7f77c-190">例如，在 Microsoft JScript 中，請使用兩個連續的反斜線，而不是一個。</span><span class="sxs-lookup"><span data-stu-id="7f77c-190">For example, in Microsoft JScript, use two adjacent backslashes instead of one.</span></span>

 

<span data-ttu-id="7f77c-191">如果您未指定憑證，而 HTTPS 伺服器需要用戶端憑證，WinHTTP 會選取預設 [*憑證存放區*](glossary.md)中的第一個憑證。</span><span class="sxs-lookup"><span data-stu-id="7f77c-191">If you do not specify a certificate and an HTTPS server requires a client certificate, WinHTTP selects the first certificate in the default [*certificate store*](glossary.md).</span></span> <span data-ttu-id="7f77c-192">如果沒有憑證存在，則會引發錯誤。</span><span class="sxs-lookup"><span data-stu-id="7f77c-192">If no certificates exist, an error is raised.</span></span> <span data-ttu-id="7f77c-193">如果未接受憑證，伺服器會傳回403狀態碼，指出無法完成要求。</span><span class="sxs-lookup"><span data-stu-id="7f77c-193">If the certificate is not accepted, the server returns a 403 status code to indicate that the request cannot be fulfilled.</span></span> <span data-ttu-id="7f77c-194">然後，您可以使用 [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) 選擇更適當的憑證，然後重新傳送要求。</span><span class="sxs-lookup"><span data-stu-id="7f77c-194">You can then choose a more appropriate certificate with [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) and resend the request.</span></span>

 

