---
title: SSL 憑證
description: 安全通訊端層 (SSL) 已成為保護網際網路連線的標準，可用來防止網路遭到竊聽。 SSL 通訊協定可讓用戶端和伺服器彼此驗證並協商加密演算法。
ms.assetid: 2b78f609-473f-467b-8bf4-709b790bca53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15e4e6f2b0fe9e3bb058ba506f8a36728540443
ms.sourcegitcommit: be2b23d847b9717224c5f31816594c8abda388a7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2020
ms.locfileid: "106965226"
---
# <a name="ssl-certificates"></a><span data-ttu-id="3f659-104">SSL 憑證</span><span class="sxs-lookup"><span data-stu-id="3f659-104">SSL Certificates</span></span>

<span data-ttu-id="3f659-105">安全通訊端層 (SSL) （也稱為傳輸層安全性 (TLS) ）已成為保護網際網路連線的標準，可用來防止網路遭到竊聽。</span><span class="sxs-lookup"><span data-stu-id="3f659-105">Secure Sockets Layer (SSL), also known as Transport Layer Security (TLS), has become a standard for securing Internet connections and is used to prevent eavesdropping on the network.</span></span> <span data-ttu-id="3f659-106">SSL/TLS 通訊協定可讓用戶端和伺服器彼此驗證並協商加密演算法。</span><span class="sxs-lookup"><span data-stu-id="3f659-106">The SSL/TLS protocol allows a client and server to authenticate each other and negotiate encryption algorithms.</span></span>

<span data-ttu-id="3f659-107">SSL 會使用加密金鑰和加密演算法來保護 HTTP 連接。</span><span class="sxs-lookup"><span data-stu-id="3f659-107">SSL uses an encryption key and an encryption algorithm to secure the HTTP connection.</span></span> <span data-ttu-id="3f659-108">加密金鑰包含在用戶端和伺服器所使用的 SSL 憑證中。</span><span class="sxs-lookup"><span data-stu-id="3f659-108">The encryption keys are contained in SSL certificates used by both the client and the server.</span></span> <span data-ttu-id="3f659-109">憑證通常是 x.509 ([RFC 2459](https://www.ietf.org/rfc/rfc2459.txt)) 檔。</span><span class="sxs-lookup"><span data-stu-id="3f659-109">The certificate is typically an X.509 ([RFC 2459](https://www.ietf.org/rfc/rfc2459.txt)) document.</span></span> <span data-ttu-id="3f659-110">伺服器會提供會話的 SSL 憑證，並在交握階段將憑證傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="3f659-110">The server provides the SSL certificate for the session and sends the certificate to the client in the handshake phase.</span></span> <span data-ttu-id="3f659-111">用戶端只會在伺服器將要求傳送至憑證的用戶端時，才會將其憑證傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="3f659-111">The client sends its certificate to the server only if the server sends a request to the client for a certificate.</span></span> <span data-ttu-id="3f659-112">因此，用戶端一律會驗證服務器，但是伺服器也可以選擇是否要驗證用戶端。</span><span class="sxs-lookup"><span data-stu-id="3f659-112">Thus the client always authenticates the server but the server has the option whether or not to authenticate the client.</span></span>

<span data-ttu-id="3f659-113">伺服器憑證必須儲存在 HTTP 伺服器 API 的本機持續性儲存體中，以在每次建立安全連線時使用。</span><span class="sxs-lookup"><span data-stu-id="3f659-113">Server certificates must be stored in the HTTP Server API's local persistent storage, for use each time a secure connection is created.</span></span> <span data-ttu-id="3f659-114">每個憑證存放區專案也包含伺服器的 IP 位址和埠、用來簽署訊息的憑證雜湊 () 和應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f659-114">Each certificate store entry also contains the IP Address and port of the server, the certificate hash (used for signing the messages) and the application ID.</span></span> <span data-ttu-id="3f659-115">應用程式識別碼是用來識別擁有憑證的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3f659-115">The application ID is used to identify the application that owns the certificate.</span></span>

<span data-ttu-id="3f659-116">系統管理員可以使用設定 Api 來儲存 SSL 伺服器憑證資訊。</span><span class="sxs-lookup"><span data-stu-id="3f659-116">System administrators can store SSL server certificate information with the configuration APIs.</span></span> <span data-ttu-id="3f659-117">系統管理工具會呼叫 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) 函數，並指定服務設定參數的 HttpServiceConfigSSLCertInfo 值，以設定 SSL 憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="3f659-117">An administrative tool calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function and specifies HttpServiceConfigSSLCertInfo value for the service configuration parameter to set information for an SSL certificate.</span></span> <span data-ttu-id="3f659-118">電腦上的每個 IP 位址和通訊埠都只能設定一個伺服器憑證。</span><span class="sxs-lookup"><span data-stu-id="3f659-118">Only one server certificate can be configured for each IP Address and port pair on the machine.</span></span> <span data-ttu-id="3f659-119">HTTP 伺服器 API 也提供 [**查詢**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) 和 [**刪除**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) 函數，以存取或刪除現有的憑證。</span><span class="sxs-lookup"><span data-stu-id="3f659-119">The HTTP Server API also provides [**query**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) and [**delete**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) functions to access or delete existing certificates.</span></span>

 

 




