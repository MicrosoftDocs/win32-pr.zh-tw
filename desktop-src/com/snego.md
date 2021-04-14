---
title: Snego
description: Snego （其驗證服務識別碼為 RPC \_ C \_ 驗證 \_ GSS \_ NEGOTIATE）實際上不提供驗證服務本身。
ms.assetid: 2087a84c-d302-4511-9f02-2d20ee9e0d8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676b6428d6b7e79893214c2d234dcfc43992e190
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382934"
---
# <a name="snego"></a><span data-ttu-id="a9967-103">Snego</span><span class="sxs-lookup"><span data-stu-id="a9967-103">Snego</span></span>

<span data-ttu-id="a9967-104">Snego （其驗證服務識別碼為 RPC \_ C \_ 驗證 \_ GSS \_ NEGOTIATE）實際上不提供驗證服務本身。</span><span class="sxs-lookup"><span data-stu-id="a9967-104">Snego, whose authentication service identifier is RPC\_C\_AUTHN\_GSS\_NEGOTIATE, does not actually provide authentication services itself.</span></span> <span data-ttu-id="a9967-105">相反地，它會取得驗證服務清單，並協調將在用戶端和伺服器之間運作的服務。</span><span class="sxs-lookup"><span data-stu-id="a9967-105">Instead, it takes a list of authentication services and negotiates a service that will work between the client and server.</span></span> <span data-ttu-id="a9967-106">驗證參數不會由 Snego 使用，但會傳遞至所選擇的驗證服務，這會執行實際的驗證。</span><span class="sxs-lookup"><span data-stu-id="a9967-106">The authentication parameters are not used by Snego but are passed to the chosen authentication service, which does the actual authentication.</span></span> <span data-ttu-id="a9967-107">Snego 是由網際網路工程任務推動 (小組所標準化，在1998年12月日的檔 [RFC 2478](https://www.ietf.org/rfc/rfc2478.txt)中) 。</span><span class="sxs-lookup"><span data-stu-id="a9967-107">Snego was standardized by the Internet Engineering Task Force (IETF) in December 1998, in document [RFC 2478](https://www.ietf.org/rfc/rfc2478.txt).</span></span>

<span data-ttu-id="a9967-108">當您不知道遠端電腦可以提供哪些驗證服務時，Snego 會很有用。</span><span class="sxs-lookup"><span data-stu-id="a9967-108">Snego is useful when you don't know what authentication services the remote computer can provide.</span></span>

<span data-ttu-id="a9967-109">若要使用 Snego，用戶端和伺服器都必須指定 Snego 作為驗證服務。</span><span class="sxs-lookup"><span data-stu-id="a9967-109">To use Snego, both the client and the server must specify Snego as the authentication service.</span></span> <span data-ttu-id="a9967-110">伺服器 \_ \_ \_ \_ 會在傳遞至 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的 *asAuthSvc* 陣列參數中，將 RPC C 驗證 GSS NEGOTIATE 指定為其中一個 [**唯一 \_ 驗證 \_ 服務**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)結構的 **dwAuthnSvc** 成員。</span><span class="sxs-lookup"><span data-stu-id="a9967-110">The server specifies RPC\_C\_AUTHN\_GSS\_NEGOTIATE as the **dwAuthnSvc** member of one of the [**SOLE\_AUTHENTICATION\_SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) structures in the *asAuthSvc* array parameter that is passed to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="a9967-111">用戶端可以藉由呼叫 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) 並傳遞 RPC \_ C \_ 驗證 \_ GSS \_ NEGOTIATE 作為 *dwAuthnSvc* 參數來指定 Snego。</span><span class="sxs-lookup"><span data-stu-id="a9967-111">The client can specify Snego by calling [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) and passing RPC\_C\_AUTHN\_GSS\_NEGOTIATE as the *dwAuthnSvc* parameter.</span></span> <span data-ttu-id="a9967-112">用戶端也應針對在 **CoSetProxyBlanket** 的呼叫中傳遞給 *PAuthInfo* 參數的 [**SEC 的 \_ WINNT \_ AUTH \_ IDENTITY \_ EX**](/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa)結構的 **PackageList** 成員，提供授權的可能驗證服務清單。</span><span class="sxs-lookup"><span data-stu-id="a9967-112">The client should also provide a list of possible authentication services for Snego through the **PackageList** member of the [**SEC\_WINNT\_AUTH\_IDENTITY\_EX**](/windows/desktop/api/sspi/ns-sspi-_sec_winnt_auth_identity_exa) structure that is passed to the *pAuthInfo* parameter in the call to **CoSetProxyBlanket**.</span></span> <span data-ttu-id="a9967-113">如果 *pAuthInfo* 為 **Null**，則 Snego 會從電腦上安裝的安全性套件中撰寫驗證服務清單。</span><span class="sxs-lookup"><span data-stu-id="a9967-113">If *pAuthInfo* is **NULL**, Snego composes a list of authentication services from the security packages installed on the computer.</span></span> <span data-ttu-id="a9967-114">接著，Snego 會將驗證服務清單傳送到伺服器、將清單與伺服器的可用驗證服務進行比較，並挑選要用於連線的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="a9967-114">Then Snego sends the list of authentication services to the server, compares the list to the server's available authentication services, and picks an authentication service to use for the connection.</span></span>

> [!Note]  
> <span data-ttu-id="a9967-115">安全通道不能在使用 Snego 的驗證服務清單上。</span><span class="sxs-lookup"><span data-stu-id="a9967-115">Schannel cannot be on the list of authentication services that Snego uses.</span></span>

 

<span data-ttu-id="a9967-116">用戶端也可以在呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時指定 Snego。</span><span class="sxs-lookup"><span data-stu-id="a9967-116">Clients can also specify Snego when they call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="a9967-117">[**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)的 *dwAuthnSvc* 和 *pAuthInfo* 參數會成為 [**唯一 \_ 驗證 \_ 資訊**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)結構的成員，此結構會透過其 *pAuthList* 參數傳遞至 **CoInitializeSecurity** 。</span><span class="sxs-lookup"><span data-stu-id="a9967-117">The *dwAuthnSvc* and *pAuthInfo* parameters of [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) become members of a [**SOLE\_AUTHENTICATION\_INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) structure that is passed to **CoInitializeSecurity** through its *pAuthList* parameter.</span></span> <span data-ttu-id="a9967-118">這些成員值的詳細資料與上一段所述的值相同。</span><span class="sxs-lookup"><span data-stu-id="a9967-118">The details of the values of those members are the same as described in the preceding paragraph.</span></span>

<span data-ttu-id="a9967-119">如果使用了 Snego，則對 [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) 或 [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) 的呼叫會將 snego 傳回為驗證服務，而不是使用 snego 挑選來建立連接的實際驗證服務。</span><span class="sxs-lookup"><span data-stu-id="a9967-119">If Snego is used, calls to [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket) or [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) will return Snego as the authentication service, rather than the actual authentication service that Snego picked for establishing the connection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9967-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9967-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9967-121">COM 和安全性封裝</span><span class="sxs-lookup"><span data-stu-id="a9967-121">COM and Security Packages</span></span>](com-and-security-packages.md)
</dt> </dl>

 

 