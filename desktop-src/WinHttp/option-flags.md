---
Description: WinHttpQueryOption 和 WinHttpSetOption 支援下列選項旗標。
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: '選項旗標 (WinHTTP. h) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 25049ee11c59c6b320b794c07bd65e5ec9b930c9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395413"
---
# <a name="option-flags"></a><span data-ttu-id="2407b-103">選項旗標</span><span class="sxs-lookup"><span data-stu-id="2407b-103">Option Flags</span></span>

<span data-ttu-id="2407b-104">[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)和 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)支援下列選項旗標。</span><span class="sxs-lookup"><span data-stu-id="2407b-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="2407b-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP \_ 選項有 \_ 保證 \_ 非 \_ 封鎖 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2407b-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-106">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="2407b-106">The default is FALSE.</span></span> <span data-ttu-id="2407b-107">如果設定為 TRUE，當用戶端應用程式封鎖狀態回呼時，WinHTTP 無法保證進度。</span><span class="sxs-lookup"><span data-stu-id="2407b-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="2407b-108">用戶端應用程式必須特別小心地在回呼內執行最基本的作業，而不會封鎖、儘快傳回，而且特別不能等待任何後續的 WinHTTP 呼叫。</span><span class="sxs-lookup"><span data-stu-id="2407b-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="2407b-109">如果未遵循這些指導方針，可能會對效能造成負面影響，或可能應用程式停止回應。</span><span class="sxs-lookup"><span data-stu-id="2407b-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="2407b-110">如果以指定的方式使用，此選項可能會改善效能。</span><span class="sxs-lookup"><span data-stu-id="2407b-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP \_ 選項 \_ 自動登入 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="2407b-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-112">設定不帶正負號的長整數值，指定具有下列其中一個值的 [自動登入原則](authentication-in-winhttp.md) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="2407b-113">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-113">Term</span></span> | <span data-ttu-id="2407b-114">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-114">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 高</span><span class="sxs-lookup"><span data-stu-id="2407b-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="2407b-116">未使用預設認證。</span><span class="sxs-lookup"><span data-stu-id="2407b-116">Default credentials are not used.</span></span> <span data-ttu-id="2407b-117">請注意，只有當您依實際的電腦名稱稱指定伺服器時，此旗標才會生效。</span><span class="sxs-lookup"><span data-stu-id="2407b-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="2407b-118">如果您將伺服器指定為 "localhost" 或 IP 位址，它將不會生效。</span><span class="sxs-lookup"><span data-stu-id="2407b-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="2407b-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 低</span><span class="sxs-lookup"><span data-stu-id="2407b-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="2407b-120">系統會針對所有要求執行使用預設認證的已驗證登入。</span><span class="sxs-lookup"><span data-stu-id="2407b-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="2407b-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 中</span><span class="sxs-lookup"><span data-stu-id="2407b-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="2407b-122">使用預設認證的已驗證登入只會針對近端內部網路上的要求執行。</span><span class="sxs-lookup"><span data-stu-id="2407b-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="2407b-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**WINHTTP \_ 選項 \_ 背景 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="2407b-123"><span id="WINHTTP_OPTION_BACKGROUND_CONNECTIONS"></span><span id="winhttp_option_background_connections"></span>**WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2407b-124">當您在會話控制碼上設定此選項時，必須傳遞您要開啟的連接數目。</span><span class="sxs-lookup"><span data-stu-id="2407b-124">When you set this option on a session handle, you must pass the number of connections you wish to open.</span></span> <span data-ttu-id="2407b-125">然後，在第一次傳送要求時，WinHttp 會以平行方式開啟多個連接，而不是只開啟單一連線。</span><span class="sxs-lookup"><span data-stu-id="2407b-125">Then, upon first sending a request, rather than opening only a single connection, WinHttp opens a number of connections in parallel.</span></span> <span data-ttu-id="2407b-126">這可以改善後續要求對相同目的地的效能，而不會造成連線建立的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="2407b-126">This can improve the performance of subsequent requests to the same destination, which won't have the overhead of connection establishment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP \_ 選項 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2407b-127"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-128">抓取以 [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)設定之回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="2407b-128">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="2407b-129"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-130">設定用戶端憑證內容。</span><span class="sxs-lookup"><span data-stu-id="2407b-130">Sets the client certificate context.</span></span> <span data-ttu-id="2407b-131">如果應用程式收到 [**\_ \_ \_ \_ \_ 所需的錯誤 WINHTTP 用戶端驗證**](error-messages.md)憑證，則必須先呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 來提供憑證，再重試要求。</span><span class="sxs-lookup"><span data-stu-id="2407b-131">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="2407b-132">在處理此選項的過程中，WinHttp 會在呼叫端提供的憑證內容上呼叫 [**CertDuplicateCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) ，如此一來，呼叫端就可以獨立釋放憑證內容。</span><span class="sxs-lookup"><span data-stu-id="2407b-132">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="2407b-133">應用程式不應該嘗試 \_ \_ 在已從中抓取 \_ \_ 憑證內容的憑證存放區上呼叫 [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) 時，關閉憑證存放區的憑證關閉存放區強制旗標旗標。</span><span class="sxs-lookup"><span data-stu-id="2407b-133">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="2407b-134">可能會發生存取違規。</span><span class="sxs-lookup"><span data-stu-id="2407b-134">An access violation may occur.</span></span>

<span data-ttu-id="2407b-135">當伺服器要求用戶端憑證、 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)或 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 時，會傳回 [**錯誤 \_ WINHTTP \_ 用戶端 \_ 驗證憑證 \_ \_ 所需**](error-messages.md) 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2407b-135">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="2407b-136">如果伺服器要求憑證，但不需要憑證，則應用程式可以指定此選項來指出它沒有憑證。</span><span class="sxs-lookup"><span data-stu-id="2407b-136">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="2407b-137">伺服器可以選擇其他驗證配置，或允許匿名存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="2407b-137">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="2407b-138">應用程式會在 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)的 *lpBuffer* 參數中提供 **WINHTTP \_ NO \_ CLIENT \_ CERT \_ CONTEXT** 宏，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="2407b-138">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="2407b-139">如果伺服器需要用戶端憑證，它可能會傳送 403 HTTP 狀態碼來回應。</span><span class="sxs-lookup"><span data-stu-id="2407b-139">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="2407b-140">如需詳細資訊，請參閱 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單** 選項。</span><span class="sxs-lookup"><span data-stu-id="2407b-140">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="2407b-141"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-142">當 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)或 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)的錯誤是 **\_ \_ \_ \_ \_ 需要的 WINHTTP 用戶端驗證憑證錯誤** 時，會抓取 [**SecPkgCoNtext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)結構。</span><span class="sxs-lookup"><span data-stu-id="2407b-142">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="2407b-143">結構中的簽發者清單包含伺服器 (CA) 可接受的憑證授權單位單位清單。</span><span class="sxs-lookup"><span data-stu-id="2407b-143">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="2407b-144">用戶端應用程式可以篩選 CA 清單，以取得 SSL 驗證的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="2407b-144">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="2407b-145">或者，如果伺服器要求用戶端憑證，但不需要它，則應用程式可以使用 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容** 選項來呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-145">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="2407b-146">如需詳細資訊，請參閱 **WINHTTP \_ option \_ CLIENT \_ CERT \_ CONTEXT** 選項。</span><span class="sxs-lookup"><span data-stu-id="2407b-146">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP \_ 選項 \_ 字碼頁**</span><span class="sxs-lookup"><span data-stu-id="2407b-147"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-148">設定用來處理 URL (也就是查詢字串) 的 [*字碼頁*](glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-148">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="2407b-149">預設值為 UTF8。</span><span class="sxs-lookup"><span data-stu-id="2407b-149">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP \_ 選項 \_ 設定 \_ PASSPORT \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="2407b-150"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-151">設定不帶正負號的長整數值，這個值會指定是否啟用 [WinHTTP 驗證中的 Passport 驗證](passport-authentication-in-winhttp.md) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-151">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="2407b-152">這個值可以是下列值之一：</span><span class="sxs-lookup"><span data-stu-id="2407b-152">The value can be one of the following:</span></span>

| <span data-ttu-id="2407b-153">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-153">Term</span></span> | <span data-ttu-id="2407b-154">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-154">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ 停用 \_ PASSPORT \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="2407b-155"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="2407b-156">Microsoft Passport 驗證已停用。</span><span class="sxs-lookup"><span data-stu-id="2407b-156">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="2407b-157">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="2407b-157">This is the default.</span></span> |
| <span data-ttu-id="2407b-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ 停用 \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="2407b-158"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="2407b-159">Passport keyring 已停用。</span><span class="sxs-lookup"><span data-stu-id="2407b-159">The Passport keyring is disabled.</span></span> <span data-ttu-id="2407b-160">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="2407b-160">This is the default.</span></span> |
| <span data-ttu-id="2407b-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ 啟用 \_ PASSPORT \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="2407b-161"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="2407b-162">Passport 驗證已啟用。</span><span class="sxs-lookup"><span data-stu-id="2407b-162">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="2407b-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ 啟用 \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="2407b-163"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="2407b-164">Passport keyring 已啟用。</span><span class="sxs-lookup"><span data-stu-id="2407b-164">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="2407b-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP \_ 選項 \_ 連接 \_ 重試**</span><span class="sxs-lookup"><span data-stu-id="2407b-165"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-166">設定或抓取不帶正負號的長整數值，其中包含連接到主機的 timesWinHTTP 嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="2407b-166">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="2407b-167">Microsoft Windows HTTP Services (WinHTTP) 只會在每個網際網路通訊協定 (IP) 位址嘗試一次。</span><span class="sxs-lookup"><span data-stu-id="2407b-167">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="2407b-168">例如，如果您嘗試連線到有10個 IP 位址的多重主目錄主機，而 **winHTTP \_ 選項連線 \_ \_ 重試** 設定為7，則 winHTTP 只會嘗試連線到前七個 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="2407b-168">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="2407b-169">假設有一組相同的10個 IP 位址，則當 **winHTTP \_ 選項 \_ 連接 \_ 重試** 設定為20時，winHTTP 只會嘗試10次。</span><span class="sxs-lookup"><span data-stu-id="2407b-169">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="2407b-170">如果連接嘗試在指定的嘗試次數之後仍失敗，或連接逾時之前已過期，則會取消要求。</span><span class="sxs-lookup"><span data-stu-id="2407b-170">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="2407b-171">**WINHTTP \_ 選項 \_ 連接 \_ 重試** 的預設值為五次嘗試。</span><span class="sxs-lookup"><span data-stu-id="2407b-171">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP \_ 選項 \_ 連接 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="2407b-172"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-173">設定或抓取不帶正負號的長整數值，其中包含超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2407b-173">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="2407b-174">將此選項設定為無限 (0xFFFFFFFF) 將會停用此計時器。</span><span class="sxs-lookup"><span data-stu-id="2407b-174">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="2407b-175">如果 TCP 連線要求所花費的時間超過這個超時值，就會取消要求。</span><span class="sxs-lookup"><span data-stu-id="2407b-175">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="2407b-176">預設的超時時間為60秒。</span><span class="sxs-lookup"><span data-stu-id="2407b-176">The default timeout is 60 seconds.</span></span> <span data-ttu-id="2407b-177">當您嘗試連線到單一主機 (多個 IP 位址時，) 的多重主控制項，則會有每個個別連接的時間限制。</span><span class="sxs-lookup"><span data-stu-id="2407b-177">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP \_ 選項 \_ 連接 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="2407b-178"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-179">抓取 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 傳回時產生回應之要求的來源和目的地 IP 位址和埠。</span><span class="sxs-lookup"><span data-stu-id="2407b-179">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="2407b-180">應用程式會使用 **WINHTTP \_ 選項 \_ 連接 \_ 資訊** 選項來呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) ，並在 *lpBuffer* 參數中提供 [**winHTTP \_ 連接 \_ 資訊**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)結構。</span><span class="sxs-lookup"><span data-stu-id="2407b-180">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="2407b-181">如需詳細資訊，請參閱 **WINHTTP \_ 連接 \_ 資訊**。</span><span class="sxs-lookup"><span data-stu-id="2407b-181">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="2407b-182">**Windows Server 2003 SP1 和 WINDOWS XP 含 SP2：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="2407b-182">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="2407b-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-184">針對要求所使用的基礎連接，擷取 [**TCP \_ 資訊 \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) 結構。</span><span class="sxs-lookup"><span data-stu-id="2407b-184">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="2407b-185">傳回的結構可能包含透過相同連接傳送的先前要求的統計資料。</span><span class="sxs-lookup"><span data-stu-id="2407b-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="2407b-186">**WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V1** 已取代此選項。</span><span class="sxs-lookup"><span data-stu-id="2407b-186">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="2407b-187"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-188">擷取要求所使用之基礎連接的 [**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) 結構。</span><span class="sxs-lookup"><span data-stu-id="2407b-188">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="2407b-189">傳回的結構可能包含透過相同連接傳送的先前要求的統計資料。</span><span class="sxs-lookup"><span data-stu-id="2407b-189">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP \_ 選項 \_ 內容 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="2407b-190"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-191">設定或抓取 DWORD 指標，其中包含與這個 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼相關聯之內容值的指標。 **\_**</span><span class="sxs-lookup"><span data-stu-id="2407b-191">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="2407b-192">使用儲存在緩衝區中的值，並為 **WINHTTP \_ 選項 \_ 內容 \_ 值** 選項旗標指派新值。</span><span class="sxs-lookup"><span data-stu-id="2407b-192">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP \_ 選項 \_ 解壓縮**</span><span class="sxs-lookup"><span data-stu-id="2407b-193"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-194">設定旗標的 DWORD，以判斷 WinHTTP 是否會自動以壓縮的內容編碼方式解壓縮回應主體。</span><span class="sxs-lookup"><span data-stu-id="2407b-194">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="2407b-195">WinHTTP 也會設定適當的 Accept-Encoding 標頭，覆寫呼叫端所提供的任何一個。</span><span class="sxs-lookup"><span data-stu-id="2407b-195">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="2407b-196">支援的值為：</span><span class="sxs-lookup"><span data-stu-id="2407b-196">Supported values are:</span></span>

| <span data-ttu-id="2407b-197">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-197">Term</span></span> | <span data-ttu-id="2407b-198">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-198">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP \_ 解壓縮 \_ 旗標 \_ GZIP</span><span class="sxs-lookup"><span data-stu-id="2407b-199"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="2407b-200">解壓縮內容編碼： gzip 回應。</span><span class="sxs-lookup"><span data-stu-id="2407b-200">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="2407b-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP \_ 解壓縮 \_ 旗標 \_ DEFLATE</span><span class="sxs-lookup"><span data-stu-id="2407b-201"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="2407b-202">解壓縮內容編碼： deflate 回應。</span><span class="sxs-lookup"><span data-stu-id="2407b-202">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="2407b-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP \_ 解壓縮 \_ 旗標 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="2407b-203"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="2407b-204">使用任何支援的內容編碼來將回應解壓縮。</span><span class="sxs-lookup"><span data-stu-id="2407b-204">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="2407b-205">根據預設，WinHTTP 會將壓縮的回應傳遞給未修改的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="2407b-205">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP \_ 選項 \_ 停用 \_ CERT \_ 鏈 \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="2407b-206"><span id="WINHTTP_OPTION_DISABLE_CERT_CHAIN_BUILDING"></span><span id="winhttp_option_disable_cert_chain_building"></span>**WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="2407b-207">在 WinHttp 會話控制碼上設定這個選項，可讓您啟用/停用伺服器憑證鏈是否已建立。</span><span class="sxs-lookup"><span data-stu-id="2407b-207">Setting this option on a WinHttp session handle allows you to enable/disable whether the server certificate chain is built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP \_ 選項 \_ 停用 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="2407b-208"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-209">設定不帶正負號的長整數值，指定使用下列其中一個或多個旗標停用的功能。</span><span class="sxs-lookup"><span data-stu-id="2407b-209">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="2407b-210">請注意，只有在使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立要求控制碼之後，以及使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)傳送要求之前，才應將這項功能傳遞至要求控制碼上的 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-210">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="2407b-211">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-211">Term</span></span> | <span data-ttu-id="2407b-212">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-212">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ 停用 \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="2407b-213"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="2407b-214">自動驗證已停用。</span><span class="sxs-lookup"><span data-stu-id="2407b-214">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="2407b-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ 停用 \_ COOKIE</span><span class="sxs-lookup"><span data-stu-id="2407b-215"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="2407b-216">已停用自動將 cookie 標頭新增至要求的功能。</span><span class="sxs-lookup"><span data-stu-id="2407b-216">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="2407b-217">此外，傳回的 cookie 也不會自動新增至 cookie 資料庫。</span><span class="sxs-lookup"><span data-stu-id="2407b-217">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="2407b-218">停用 cookie 可能會導致 Passport 驗證效能不佳。</span><span class="sxs-lookup"><span data-stu-id="2407b-218">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="2407b-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ 停用 \_ 保持運作 \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="2407b-219"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="2407b-220">停用連接的 keep-alive 語義。</span><span class="sxs-lookup"><span data-stu-id="2407b-220">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="2407b-221">MSN、NTLM 和其他類型的驗證都需要 keep-alive 語義。</span><span class="sxs-lookup"><span data-stu-id="2407b-221">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="2407b-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP \_ 停用重新 \_ 導向</span><span class="sxs-lookup"><span data-stu-id="2407b-222"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="2407b-223">使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)傳送要求時，自動重新導向已停用。</span><span class="sxs-lookup"><span data-stu-id="2407b-223">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="2407b-224">如果自動重新導向已停用，應用程式必須註冊回呼函式，Passport 驗證才會成功。</span><span class="sxs-lookup"><span data-stu-id="2407b-224">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="2407b-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP \_ 選項 \_ 停用 \_ 安全 \_ 通訊協定 \_ 回復**</span><span class="sxs-lookup"><span data-stu-id="2407b-225"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-226">當初始通訊協定協商失敗時，防止 WinHTTP 使用較低版本的安全性通訊協定來重試連接。</span><span class="sxs-lookup"><span data-stu-id="2407b-226">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP \_ 選項 \_ 停用 \_ 串流 \_ 佇列**</span><span class="sxs-lookup"><span data-stu-id="2407b-227"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-228">允許新的要求在達到最大並行串流限制時開啟額外的 HTTP/2 連接，而不是在現有的連接上等候下一個可用的資料流程。</span><span class="sxs-lookup"><span data-stu-id="2407b-228">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP \_ 選項 \_ 啟用 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="2407b-229"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-230">設定不帶正負號的長整數值，指定目前已啟用的功能。</span><span class="sxs-lookup"><span data-stu-id="2407b-230">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="2407b-231">可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2407b-231">Can be one of the following values.</span></span>

| <span data-ttu-id="2407b-232">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-232">Term</span></span> | <span data-ttu-id="2407b-233">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-233">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ 啟用 \_ SSL \_ 還原 \_ 模擬</span><span class="sxs-lookup"><span data-stu-id="2407b-234"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="2407b-235">如果啟用，WinHTTP 會暫時還原 SSL 憑證驗證作業期間的用戶端模擬。</span><span class="sxs-lookup"><span data-stu-id="2407b-235">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="2407b-236">此值只能在會話控制碼上進行設定。</span><span class="sxs-lookup"><span data-stu-id="2407b-236">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="2407b-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ 啟用 \_ SSL \_ 撤銷</span><span class="sxs-lookup"><span data-stu-id="2407b-237"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="2407b-238">啟用時，WinHTTP 允許 SSL 撤銷。</span><span class="sxs-lookup"><span data-stu-id="2407b-238">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="2407b-239">此值只能在要求控制碼上進行設定。</span><span class="sxs-lookup"><span data-stu-id="2407b-239">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP \_ 選項 \_ 啟用 \_ HTTP \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="2407b-240"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-241">設定可接受之 advanced HTTP 版本的 DWORD 位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="2407b-241">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="2407b-242">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="2407b-242">Possible values are:</span></span>

| <span data-ttu-id="2407b-243">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-243">Term</span></span> | <span data-ttu-id="2407b-244">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-244">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP \_ 通訊協定 \_ 旗標 \_ HTTP2 (0x1) </span><span class="sxs-lookup"><span data-stu-id="2407b-245"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="2407b-246">針對要求啟用 HTTP/2。</span><span class="sxs-lookup"><span data-stu-id="2407b-246">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="2407b-247">無 (0x0) </span><span class="sxs-lookup"><span data-stu-id="2407b-247">None (0x0)</span></span> | <span data-ttu-id="2407b-248">將要求限制為 HTTP/1.1 及更早的版本。</span><span class="sxs-lookup"><span data-stu-id="2407b-248">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="2407b-249">舊版的 HTTP (1.1 和先前的) 無法使用這個選項停用。</span><span class="sxs-lookup"><span data-stu-id="2407b-249">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="2407b-250">預設值為0x0。</span><span class="sxs-lookup"><span data-stu-id="2407b-250">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP \_ 選項 \_ ENABLE \_ HTTP2 \_ PLUS \_ CLIENT \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="2407b-251"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="2407b-252">您可以在 WinHttp 會話控制碼上設定這個選項，讓 WinHttp 在使用 HTTP/2 時，使用呼叫端提供的用戶端憑證內容。</span><span class="sxs-lookup"><span data-stu-id="2407b-252">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP \_ 選項 \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="2407b-253"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-254">設定 **布林** 值，這個值會指定目前是否已啟用追蹤。</span><span class="sxs-lookup"><span data-stu-id="2407b-254">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="2407b-255">如需 WinHTTP 中追蹤設備的詳細資訊，請參閱 [WinHTTP 追蹤設備](winhttptracecfg-exe--a-trace-configuration-tool.md)。</span><span class="sxs-lookup"><span data-stu-id="2407b-255">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="2407b-256">此選項只能在 **Null** **HINTERNET** 控制碼上進行設定。</span><span class="sxs-lookup"><span data-stu-id="2407b-256">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="2407b-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP \_ 選項 \_ 編碼 \_ 額外**</span><span class="sxs-lookup"><span data-stu-id="2407b-257"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-258">啟用路徑和查詢字串的 URL 百分比編碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-258">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="2407b-259">或者，您可以在呼叫 WinHttp 之前對編碼百分比進行編碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-259">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="2407b-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP \_ 選項 \_ 到期 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="2407b-260"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-261">此選項只能在要求控制碼上設定，而該控制碼仍在使用中 (傳送或接收) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-261">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="2407b-262">設定此選項會告知 WinHttp 在與傳入的要求控制碼相關聯的連接上停止服務要求。</span><span class="sxs-lookup"><span data-stu-id="2407b-262">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="2407b-263">當要求控制碼完成時，將會關閉此連接。</span><span class="sxs-lookup"><span data-stu-id="2407b-263">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="2407b-264">此選項不會使用任何參數。</span><span class="sxs-lookup"><span data-stu-id="2407b-264">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP \_ 選項 \_ 延伸 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="2407b-265"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-266">抓取不帶正負號的長整數值，其中包含 Microsoft Windows 通訊端錯誤碼，該錯誤碼已對應到 \_ \_ \* 此執行緒內容中最後傳回的錯誤 WINHTTP 錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2407b-266">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="2407b-267">您可以傳遞 **Null** 做為控制碼值。</span><span class="sxs-lookup"><span data-stu-id="2407b-267">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**WINHTTP \_ 選項 \_ FIRST \_ 可用 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="2407b-268"><span id="WINHTTP_OPTION_FIRST_AVAILABLE_CONNECTION"></span><span id="winhttp_option_first_available_connection"></span>**WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="2407b-269">根據預設，當 WinHttp 傳送要求時，如果沒有可用的連線來處理要求，WinHttp 將會嘗試建立新的連線，並將要求系結至這個新連接。</span><span class="sxs-lookup"><span data-stu-id="2407b-269">By default, when WinHttp sends a request, if there are no available connections to serve the request, WinHttp will attempt to establish a new connection, and the request will be bound to this new connection.</span></span> <span data-ttu-id="2407b-270">當您設定此選項時，會改為在第一個可用的連接上提供這類要求，而不一定是要建立的連接。</span><span class="sxs-lookup"><span data-stu-id="2407b-270">When you set this option, such a request will instead be served on the first connection that becomes available, and not necessarily the one being established.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP \_ 選項 \_ 全域 \_ PROXY \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="2407b-271"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-272">將 *hInternet* 函式參數設定為 **Null** 的 [**WINHTTP 認證 \_ \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2407b-272">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="2407b-273">此選項需要登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings！ShareCredsWithWinHttp**。</span><span class="sxs-lookup"><span data-stu-id="2407b-273">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="2407b-274">如果未設定此登錄機碼，WinHTTP 將會傳回錯誤： **\_ winHTTP \_ 無效 \_ 選項** 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2407b-274">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="2407b-275">依預設，此登錄機碼不存在。</span><span class="sxs-lookup"><span data-stu-id="2407b-275">This registry key is not present by default.</span></span> <span data-ttu-id="2407b-276">當設定時，WinINet 會將認證傳送至 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="2407b-276">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="2407b-277">每當 WinHttp 收到驗證挑戰，而且目前的控制碼上沒有設定任何認證時，就會使用 WinINet 提供的認證。</span><span class="sxs-lookup"><span data-stu-id="2407b-277">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="2407b-278">為了共用 proxy 認證以外的伺服器認證，使用者必須設定 **WINHTTP \_ 選項 [ \_ 使用 \_ 全域 \_ 伺服器 \_ 認證** ]。</span><span class="sxs-lookup"><span data-stu-id="2407b-278">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP \_ 選項 \_ 全域 \_ 伺服器 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="2407b-279"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-280">將 *hInternet* 函式參數設定為 **Null** 的 [**WINHTTP 認證 \_ \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2407b-280">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="2407b-281">此選項需要登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings！ShareCredsWithWinHttp**。</span><span class="sxs-lookup"><span data-stu-id="2407b-281">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="2407b-282">如果未設定此登錄機碼，WinHTTP 將會傳回錯誤： **\_ winHTTP \_ 無效 \_ 選項** 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2407b-282">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="2407b-283">依預設，此登錄機碼不存在。</span><span class="sxs-lookup"><span data-stu-id="2407b-283">This registry key is not present by default.</span></span> <span data-ttu-id="2407b-284">當設定時，WinINet 會將認證傳送至 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="2407b-284">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="2407b-285">每當 WinHttp 收到驗證挑戰，而且目前的控制碼上沒有設定任何認證時，就會使用 WinINet 提供的認證。</span><span class="sxs-lookup"><span data-stu-id="2407b-285">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="2407b-286">為了共用 proxy 認證以外的伺服器認證，使用者必須設定 **WINHTTP \_ 選項 [ \_ 使用 \_ 全域 \_ 伺服器 \_ 認證** ]。</span><span class="sxs-lookup"><span data-stu-id="2407b-286">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP \_ 選項 \_ 控制碼 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="2407b-287"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-288">抓取不帶正負號的長整數值，其中包含傳入的 [HINTERNET](hinternet-handles-in-winhttp.md) 控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="2407b-288">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="2407b-289">傳回值可以是下列其中一個：</span><span class="sxs-lookup"><span data-stu-id="2407b-289">The return value can be one of the following:</span></span>

| <span data-ttu-id="2407b-290">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-290">Term</span></span> | <span data-ttu-id="2407b-291">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-291">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP \_ 控制碼 \_ 類型 \_ 連接</span><span class="sxs-lookup"><span data-stu-id="2407b-292"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="2407b-293">控制碼是連接控制碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-293">The handle is a connection handle.</span></span> |
| <span data-ttu-id="2407b-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP \_ 控制碼 \_ 類型 \_ 要求</span><span class="sxs-lookup"><span data-stu-id="2407b-294"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="2407b-295">控制碼是要求控制碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-295">The handle is a request handle.</span></span> |
| <span data-ttu-id="2407b-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP \_ 控制碼 \_ 類型 \_ 會話</span><span class="sxs-lookup"><span data-stu-id="2407b-296"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="2407b-297">控制碼是會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-297">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="2407b-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_需要 WINHTTP 選項 \_ HTTP \_ 通訊協定 \_**</span><span class="sxs-lookup"><span data-stu-id="2407b-298"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-299">防止 **WINHTTP \_ 選項啟用 \_ \_ HTTP \_ 通訊協定** 以外的通訊協定版本使用於要求。</span><span class="sxs-lookup"><span data-stu-id="2407b-299">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**使用的 WINHTTP \_ 選項 \_ HTTP \_ 通訊協定 \_**</span><span class="sxs-lookup"><span data-stu-id="2407b-300"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-301">取得 DWORD，指出指定的要求上使用的是哪個先進的 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="2407b-301">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="2407b-302">如需可能值的清單，請參閱 **WINHTTP \_ 選項 \_ ENABLE \_ HTTP \_ PROTOCOL**。</span><span class="sxs-lookup"><span data-stu-id="2407b-302">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP \_ 選項 \_ HTTP \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="2407b-303"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-304">設定或抓取 [**HTTP \_ 版本 \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) 結構，其中包含所支援的 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="2407b-304">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="2407b-305">這是整個進程的選項;針對控制碼使用 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2407b-305">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP \_ 選項 \_ HTTP2 \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="2407b-306"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="2407b-307">您可以在會話控制碼上設定這個選項，讓 WinHttp 使用 HTTP/2 偵測框架作為 keepalive 機制。</span><span class="sxs-lookup"><span data-stu-id="2407b-307">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="2407b-308">呼叫端指定的超時時間（以毫秒為單位），且在該超時期間的連線上沒有任何活動之後，WinHttp 將開始傳送 HTTP/2 偵測畫面。</span><span class="sxs-lookup"><span data-stu-id="2407b-308">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="2407b-309">呼叫端無法設定小於5000毫秒的超時值。</span><span class="sxs-lookup"><span data-stu-id="2407b-309">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP \_ 選項 \_ HTTP2 \_ PLUS \_ 傳輸 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="2407b-310"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="2407b-311">您可以在 WinHttp 要求控制碼上設定這個選項，以控制當 HTTP/2 回應包含「傳輸編碼」標頭時，WinHttp 的行為方式。</span><span class="sxs-lookup"><span data-stu-id="2407b-311">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="2407b-312">在這種情況下，如果此選項設定為 **FALSE**，WinHttp 將會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2407b-312">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="2407b-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP \_ 選項會 \_ 離線略過憑證 \_ \_ 撤銷 \_**</span><span class="sxs-lookup"><span data-stu-id="2407b-313"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-314">允許安全連線使用無法下載憑證撤銷清單的安全性憑證。</span><span class="sxs-lookup"><span data-stu-id="2407b-314">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP \_ OPTION \_ IPV6 \_ FAST \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="2407b-315"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-316">啟用 IPv6 快速回復 (更滿意的連接 Eyeballs) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-316">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="2407b-317">這種行為與 [RFC 6555](https://tools.ietf.org/html/rfc6555) 中所述的快樂 Eyeballs 行為類似，可在 IPv6 不可靠的網路上改善連線時間。</span><span class="sxs-lookup"><span data-stu-id="2407b-317">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="2407b-318">如果為指定的主機解析 IPv6 和 IPv4 位址，WinHttp 將會先以短暫的 (300 毫秒) timeout 來連線至第一個已解析的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="2407b-318">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="2407b-319">如果連線失敗，WinHttp 將嘗試以標準超時連接到第一個已解析的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="2407b-319">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="2407b-320">第二個連接失敗時，WinHttp 會以標準超時重試第一個已解析的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="2407b-320">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="2407b-321">第三個連接失敗時，WinHttp 會還原為任何剩餘位址的預設行為，並嘗試使用標準超時連接到每一個位址，直到建立連線或未保留任何位址為止。</span><span class="sxs-lookup"><span data-stu-id="2407b-321">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP \_ 選項 \_ 為 \_ PROXY \_ CONNECT \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="2407b-322"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-323">取得是否可以取出 Proxy 傳回 Connect 回應。</span><span class="sxs-lookup"><span data-stu-id="2407b-323">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_ \_ \_ \_ 每 \_ 1 \_ 0 部 \_ 伺服器的 WINHTTP 選項 MAX CONNS**</span><span class="sxs-lookup"><span data-stu-id="2407b-324"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-325">設定或抓取不帶正負號的長整數值，其中包含每個 HTTP/1.0 伺服器允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="2407b-325">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="2407b-326">預設值為 [ **無限**]。</span><span class="sxs-lookup"><span data-stu-id="2407b-326">The default value is **INFINITE**.</span></span>

<span data-ttu-id="2407b-327">**Windows VISTA SP1 和 Windows Server 2008：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="2407b-327">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**每一伺服器的 WINHTTP \_ 選項 \_ MAX \_ CONNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2407b-328"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-329">設定或抓取不帶正負號的長整數值，其中包含每個伺服器允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="2407b-329">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="2407b-330">預設值為 [ **無限**]。</span><span class="sxs-lookup"><span data-stu-id="2407b-330">The default value is **INFINITE**.</span></span>

<span data-ttu-id="2407b-331">當此選項設定為零時，WinHTTP 會將連接數目的限制設定為2。</span><span class="sxs-lookup"><span data-stu-id="2407b-331">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 自動重新 \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="2407b-332"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-333">設定 WinHTTP 遵循的重新導向數目上限;預設值為10。</span><span class="sxs-lookup"><span data-stu-id="2407b-333">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="2407b-334">這項限制可防止未經授權的網站使 WinHTTP 用戶端在大量重新導向之後暫停。</span><span class="sxs-lookup"><span data-stu-id="2407b-334">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="2407b-335">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="2407b-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 狀態 \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="2407b-336"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-337">將最終狀態代碼傳回至 WinHTTP 用戶端之前，已忽略參考最大的資訊100-199 狀態碼回應數目。</span><span class="sxs-lookup"><span data-stu-id="2407b-337">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="2407b-338">資訊100-199 狀態碼可由伺服器在最終狀態代碼之前傳送，如需詳細資訊，請參閱 HTTP/1.1 的規格 (如需詳細資訊，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-338">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="2407b-339">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="2407b-339">The default is 10.</span></span>

<span data-ttu-id="2407b-340">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="2407b-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP \_ 選項 \_ \_ 回應 \_ 清空最 \_ 大值**</span><span class="sxs-lookup"><span data-stu-id="2407b-341"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-342">系結至從回應中清空的資料量，以重複使用連接（以位元組指定）。</span><span class="sxs-lookup"><span data-stu-id="2407b-342">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="2407b-343">預設值為1MB。</span><span class="sxs-lookup"><span data-stu-id="2407b-343">The default is 1MB.</span></span>

<span data-ttu-id="2407b-344">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="2407b-344">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP \_ 選項 \_ 的 \_ 回應 \_ 標頭 \_ 大小上限**</span><span class="sxs-lookup"><span data-stu-id="2407b-345"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-346">伺服器回應的標頭部分大小上限的系結集，以位元組為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="2407b-346">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="2407b-347">這項系結會透過傳送無限標頭資料的回應，來保護用戶端免于嘗試停止用戶端的未經授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="2407b-347">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="2407b-348">預設值是64KB。</span><span class="sxs-lookup"><span data-stu-id="2407b-348">The default value is 64KB.</span></span>

<span data-ttu-id="2407b-349">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="2407b-349">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP \_ 選項 \_ 父 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="2407b-350"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-351">捕獲此控制碼的父控制碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-351">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="2407b-352"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-353">抓取包含 Passport 登入伺服器所提供之 [*cobranding*](glossary.md) 文字的字串。</span><span class="sxs-lookup"><span data-stu-id="2407b-353">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="2407b-354">當登入伺服器以401狀態碼回應時，應立即取出此選項。</span><span class="sxs-lookup"><span data-stu-id="2407b-354">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="2407b-355">應用程式應該以位元組為單位，以位元組為單位，且足以容納傳回的字串。</span><span class="sxs-lookup"><span data-stu-id="2407b-355">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ URL**</span><span class="sxs-lookup"><span data-stu-id="2407b-356"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-357">抓取包含 Passport 登入伺服器所提供之 [*cobranding*](glossary.md) 圖形 URL 的字串。</span><span class="sxs-lookup"><span data-stu-id="2407b-357">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="2407b-358">當登入伺服器以401狀態碼回應時，應立即取出此選項。</span><span class="sxs-lookup"><span data-stu-id="2407b-358">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="2407b-359">應用程式應該以位元組為單位，以位元組為單位，且足以容納傳回的字串。</span><span class="sxs-lookup"><span data-stu-id="2407b-359">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ RETURN \_ URL**</span><span class="sxs-lookup"><span data-stu-id="2407b-360"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-361">在要求控制碼上設定唯讀選項，以抓取 Passport 傳回 URL。</span><span class="sxs-lookup"><span data-stu-id="2407b-361">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ 登出 \_**</span><span class="sxs-lookup"><span data-stu-id="2407b-362"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-363">將會話控制碼上的選項設定為登出任何 Passport 登入。</span><span class="sxs-lookup"><span data-stu-id="2407b-363">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="2407b-364">應用程式應該傳入 Passport 傳回 URL，此 URL 是以 **WINHTTP \_ 選項 \_ Passport \_ return \_ url** 抓取。</span><span class="sxs-lookup"><span data-stu-id="2407b-364">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="2407b-365">系統會清除所有與傳回 URL 相關的 cookie。</span><span class="sxs-lookup"><span data-stu-id="2407b-365">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP \_ 選項 \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="2407b-366"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-367">設定或抓取包含與要求控制碼相關聯之密碼的字串值。</span><span class="sxs-lookup"><span data-stu-id="2407b-367">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP \_ 選項 \_ PROXY**</span><span class="sxs-lookup"><span data-stu-id="2407b-368"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-369">設定或抓取 [**WINHTTP \_ PROXY \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) 結構，其中包含現有會話控制碼或要求控制碼上的 PROXY 資料。</span><span class="sxs-lookup"><span data-stu-id="2407b-369">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="2407b-370">在抓取 proxy 資料時，應用程式必須釋放此結構中所包含的 **lpszProxy** 和 **lpszProxyBypass** 字串 (如果它們是非 **Null**) 使用 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函數。</span><span class="sxs-lookup"><span data-stu-id="2407b-370">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="2407b-371">應用程式可以藉由傳遞 **Null** 控制碼 (預設 proxy) 來查詢全域 proxy 資料。</span><span class="sxs-lookup"><span data-stu-id="2407b-371">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP \_ 選項 \_ PROXY \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="2407b-372"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-373">設定或抓取包含用來存取 proxy 之密碼的字串值。</span><span class="sxs-lookup"><span data-stu-id="2407b-373">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**已 \_ 使用 WINHTTP 選項 \_ PROXY \_ SPN \_**</span><span class="sxs-lookup"><span data-stu-id="2407b-374"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-375">取得 WinHTTP 在驗證期間提供給 SSPI 的 proxy 伺服器主體名稱。</span><span class="sxs-lookup"><span data-stu-id="2407b-375">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="2407b-376">這個字串值會在驗證失敗後 usefor 傳遞至 [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-376">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP \_ 選項 \_ PROXY 使用者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="2407b-377"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-378">設定或抓取包含用來存取 proxy 之使用者名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="2407b-378">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP \_ 選項 \_ 讀取 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="2407b-379"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-380">此選項已被取代;它沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="2407b-380">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP \_ 選項 \_ 接收 \_ PROXY \_ CONNECT \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="2407b-381"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-382">設定是否可以取出 proxy 回應實體。</span><span class="sxs-lookup"><span data-stu-id="2407b-382">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="2407b-383">預設會停用這個選項。</span><span class="sxs-lookup"><span data-stu-id="2407b-383">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP \_ 選項 \_ 接收 \_ 回應 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="2407b-384"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-385">設定或抓取不帶正負號的長整數值，其中包含要等候接收要求的所有回應標頭的超時值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2407b-385">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="2407b-386">如果 WinHTTP 無法在此超時期間內接收所有標頭，則會取消要求。</span><span class="sxs-lookup"><span data-stu-id="2407b-386">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="2407b-387">預設的超時值為90秒。</span><span class="sxs-lookup"><span data-stu-id="2407b-387">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="2407b-388">只有從通訊端接收資料時，才會檢查此超時時間。</span><span class="sxs-lookup"><span data-stu-id="2407b-388">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="2407b-389">如此一來，當超時時間過期時，用戶端應用程式就不會收到通知，直到伺服器的資料抵達為止。</span><span class="sxs-lookup"><span data-stu-id="2407b-389">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="2407b-390">如果沒有資料從伺服器抵達，用戶端應用程式的超時期限和通知之間的延遲可能會與使用 [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)函數的 *dwReceiveTimeout* 參數所設定的超時值相同。</span><span class="sxs-lookup"><span data-stu-id="2407b-390">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP \_ 選項 \_ 接收 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="2407b-391"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-392">設定或抓取不帶正負號的長整數值，其中包含接收要求的部分回應或讀取某些資料的超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2407b-392">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="2407b-393">如果回應時間超過這個超時值，就會取消要求。</span><span class="sxs-lookup"><span data-stu-id="2407b-393">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="2407b-394">預設的逾時值是 30 秒。</span><span class="sxs-lookup"><span data-stu-id="2407b-394">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP \_ 選項重新 \_ 導向 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="2407b-395"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-396">設定 WinHTTP 的行為，關於處理一倍的 HTTP 重新導向狀態碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-396">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="2407b-397">您可以在會話或要求控制碼上將此選項設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="2407b-397">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="2407b-398">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-398">Term</span></span> | <span data-ttu-id="2407b-399">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-399">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP \_ 選項的重新 \_ 導向 \_ 原則 \_ 一律</span><span class="sxs-lookup"><span data-stu-id="2407b-400"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="2407b-401">所有重新導向都會自動遵循。</span><span class="sxs-lookup"><span data-stu-id="2407b-401">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="2407b-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP \_ 選項重新 \_ 導向 \_ 原則不 \_ 允許 \_ HTTPS \_ 至 \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="2407b-402"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="2407b-403">除了源自安全 (HTTPs) URL 到不安全的 (HTTP) URL 以外的所有重新導向。</span><span class="sxs-lookup"><span data-stu-id="2407b-403">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="2407b-404">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="2407b-404">This is the default setting.</span></span> |
| <span data-ttu-id="2407b-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP \_ 選項重新 \_ 導向 \_ 原則 \_ 永不</span><span class="sxs-lookup"><span data-stu-id="2407b-405"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="2407b-406">重新導向永遠不會跟著進行。</span><span class="sxs-lookup"><span data-stu-id="2407b-406">Redirects are never followed.</span></span> <span data-ttu-id="2407b-407">這會將30倍的狀態傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="2407b-407">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP \_ 選項 \_ 拒絕 \_ \_ URL 中的 USERPWD \_**</span><span class="sxs-lookup"><span data-stu-id="2407b-408"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-409">拒絕包含使用者名稱和密碼的 Url。</span><span class="sxs-lookup"><span data-stu-id="2407b-409">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="2407b-410">即使未指定使用者名稱或密碼，此選項也會拒絕包含 *username： password* 語義的 url。</span><span class="sxs-lookup"><span data-stu-id="2407b-410">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="2407b-411">例如，" u:p@hostname "、" :@hostname "、" u:@hostname " 和 " :p@hostname " 都會標示為無效。</span><span class="sxs-lookup"><span data-stu-id="2407b-411">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="2407b-412">如果將不正確 URL 傳遞至函式，則會傳回 [錯誤 \_ WINHTTP 不正確 \_ \_ url](error-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="2407b-412">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="2407b-413">根據預設，這個選項是關閉的。</span><span class="sxs-lookup"><span data-stu-id="2407b-413">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP \_ 選項 \_ 要求 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="2407b-414"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-415">此選項已被取代;它沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="2407b-415">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP \_ 選項 \_ 要求 \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="2407b-416"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-417">擷取要求的統計資料。</span><span class="sxs-lookup"><span data-stu-id="2407b-417">Retreives statistics for the request.</span></span>  <span data-ttu-id="2407b-418">如需可用的統計資料清單，請參閱 [**WINHTTP \_ 要求 \_ 統計**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)資料。</span><span class="sxs-lookup"><span data-stu-id="2407b-418">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP \_ 選項 \_ 要求 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="2407b-419"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-420">擷取要求的計時資訊。</span><span class="sxs-lookup"><span data-stu-id="2407b-420">Retreives timing information for the request.</span></span> <span data-ttu-id="2407b-421">如需可用的時間清單，請參閱 [**WINHTTP \_ 要求 \_ 時間**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)。</span><span class="sxs-lookup"><span data-stu-id="2407b-421">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP \_ 選項 \_ 需要 \_ STREAM \_ END**</span><span class="sxs-lookup"><span data-stu-id="2407b-422"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="2407b-423">此選項會告知 WinHttp 略過「內容長度」回應標頭，並繼續接收串流，直到收到 END_STREAM 旗標為止。</span><span class="sxs-lookup"><span data-stu-id="2407b-423">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP \_ 選項 \_ 解析 \_ 主機名稱**</span><span class="sxs-lookup"><span data-stu-id="2407b-424"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="2407b-425">您可以在 WinHttp 要求控制碼上設定這個選項，然後再傳送。</span><span class="sxs-lookup"><span data-stu-id="2407b-425">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="2407b-426">如果設定，WinHttp 將使用呼叫端提供的字串作為 DNS 解析的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="2407b-426">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP \_ 選項 \_ 解析 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="2407b-427"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-428">設定或抓取不帶正負號的長整數值，其中包含用來解析主機名稱的超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2407b-428">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="2407b-429">預設的超時值是 **無限** 的。</span><span class="sxs-lookup"><span data-stu-id="2407b-429">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="2407b-430">如果指定了非預設值，每個名稱解析都有一個執行緒建立的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="2407b-430">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP \_ 選項 \_ 安全 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="2407b-431"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-432">設定不帶正負號的長整數值，指定可接受哪些安全通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2407b-432">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="2407b-433">依預設，只有 SSL3 和 TLS1 會在 Windows 7 和 Windows 8 中啟用。</span><span class="sxs-lookup"><span data-stu-id="2407b-433">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="2407b-434">依預設，只有 SSL3、TLS 1.0、TLS 1.1 和 TLS 1.2 會在 Windows 8.1 和 Windows 10 中啟用。</span><span class="sxs-lookup"><span data-stu-id="2407b-434">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="2407b-435">值可以是下列一或多個值的組合。</span><span class="sxs-lookup"><span data-stu-id="2407b-435">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="2407b-436">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-436">Term</span></span> | <span data-ttu-id="2407b-437">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-437">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="2407b-438"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="2407b-439">您可以使用安全通訊端層 (SSL) 2.0、SSL 3.0 和傳輸層安全性 (TLS) 1.0 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2407b-439">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="2407b-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="2407b-440"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="2407b-441">您可以使用 SSL 2.0 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2407b-441">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="2407b-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="2407b-442"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="2407b-443">您可以使用 SSL 3.0 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2407b-443">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="2407b-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="2407b-444"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="2407b-445">您可以使用 TLS 1.0 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2407b-445">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="2407b-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="2407b-446"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="2407b-447">您可以使用 TLS 1.1 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2407b-447">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="2407b-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="2407b-448"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="2407b-449">您可以使用 TLS 1.2 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2407b-449">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="2407b-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 憑證 \_ 結構**</span><span class="sxs-lookup"><span data-stu-id="2407b-450"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-451">抓取 SSL/TLS 伺服器到 [**WINHTTP \_ 憑證 \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) 結構中的憑證。</span><span class="sxs-lookup"><span data-stu-id="2407b-451">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="2407b-452">應用程式必須使用 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)釋放 **lpszSubjectInfo** 和 **lpszIssuerInfo** 成員。</span><span class="sxs-lookup"><span data-stu-id="2407b-452">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="2407b-453"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-454">設定或抓取不帶正負號的長整數值，其中包含控制碼的安全性旗標。</span><span class="sxs-lookup"><span data-stu-id="2407b-454">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="2407b-455">它可以是下列值的組合：</span><span class="sxs-lookup"><span data-stu-id="2407b-455">It can be a combination of these values:</span></span>

| <span data-ttu-id="2407b-456">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-456">Term</span></span> | <span data-ttu-id="2407b-457">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-457">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>安全性 \_ 旗標 \_ 忽略 \_ CERT \_ CN \_ 無效</span><span class="sxs-lookup"><span data-stu-id="2407b-458"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="2407b-459">允許在憑證中使用不正確一般名稱;亦即，應用程式所指定的伺服器名稱不符合憑證中的一般名稱。</span><span class="sxs-lookup"><span data-stu-id="2407b-459">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="2407b-460">如果設定此旗標，則應用程式不會收到 **WINHTTP \_ 回呼 \_ 狀態 \_ 旗標 \_ CERT \_ CN \_ 無效** 的回呼。</span><span class="sxs-lookup"><span data-stu-id="2407b-460">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="2407b-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>安全性 \_ 旗標 \_ 忽略憑證 \_ \_ 日期 \_ 無效</span><span class="sxs-lookup"><span data-stu-id="2407b-461"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="2407b-462">允許不正確憑證日期，也就是過期或尚未有效的憑證。</span><span class="sxs-lookup"><span data-stu-id="2407b-462">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="2407b-463">如果設定此旗標，則應用程式不會收到 **WINHTTP \_ 回呼 \_ 狀態 \_ 旗標憑證 \_ \_ 日期 \_ 無效** 的回呼。</span><span class="sxs-lookup"><span data-stu-id="2407b-463">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="2407b-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>安全性 \_ 旗標 \_ 忽略 \_ 未知的 \_ CA</span><span class="sxs-lookup"><span data-stu-id="2407b-464"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="2407b-465">允許不正確憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="2407b-465">Allows an invalid certificate authority.</span></span> <span data-ttu-id="2407b-466">如果設定此旗標，則應用程式不會收到 **WINHTTP \_ 回呼 \_ 狀態 \_ 旗標 \_ 不正確 \_ CA** 回呼。</span><span class="sxs-lookup"><span data-stu-id="2407b-466">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="2407b-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>安全性 \_ 旗標 \_ 忽略憑證錯誤的 \_ \_ \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="2407b-467"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="2407b-468">允許以非伺服器憑證建立伺服器的身分識別 (例如，) 的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="2407b-468">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="2407b-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>安全性 \_ 旗標 \_ 忽略 \_ 弱 \_ 式簽章</span><span class="sxs-lookup"><span data-stu-id="2407b-469"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="2407b-470">允許忽略弱式簽章。</span><span class="sxs-lookup"><span data-stu-id="2407b-470">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="2407b-471">從 Windows 7 和 Windows Server 2008 R2 開始，每個 OS 的匯總套件更新中都有提供此旗標。</span><span class="sxs-lookup"><span data-stu-id="2407b-471">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="2407b-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>安全性 \_ 旗標 \_ 安全</span><span class="sxs-lookup"><span data-stu-id="2407b-472"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="2407b-473">使用安全傳輸。</span><span class="sxs-lookup"><span data-stu-id="2407b-473">Uses secure transfers.</span></span> <span data-ttu-id="2407b-474">這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。</span><span class="sxs-lookup"><span data-stu-id="2407b-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="2407b-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>安全性 \_ 旗標 \_ 強度 \_ 中</span><span class="sxs-lookup"><span data-stu-id="2407b-475"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="2407b-476">使用中型 (56 位) 加密。</span><span class="sxs-lookup"><span data-stu-id="2407b-476">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="2407b-477">這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。</span><span class="sxs-lookup"><span data-stu-id="2407b-477">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="2407b-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>安全性 \_ 旗標 \_ 強度 \_ 強</span><span class="sxs-lookup"><span data-stu-id="2407b-478"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="2407b-479">使用強式 (128 位) 加密。</span><span class="sxs-lookup"><span data-stu-id="2407b-479">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="2407b-480">這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。</span><span class="sxs-lookup"><span data-stu-id="2407b-480">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="2407b-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>安全性 \_ 旗標 \_ 強度 \_ 弱</span><span class="sxs-lookup"><span data-stu-id="2407b-481"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="2407b-482">使用弱式 (40 位) 加密。</span><span class="sxs-lookup"><span data-stu-id="2407b-482">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="2407b-483">這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。</span><span class="sxs-lookup"><span data-stu-id="2407b-483">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="2407b-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="2407b-484"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-485">擷取要求的 SChannel 連線和加密資訊。</span><span class="sxs-lookup"><span data-stu-id="2407b-485">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 金鑰 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="2407b-486"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-487">抓取不帶正負號的長整數值，其中包含加密金鑰的加密強度。</span><span class="sxs-lookup"><span data-stu-id="2407b-487">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="2407b-488">較大的數位表示較強的加密強度加密。</span><span class="sxs-lookup"><span data-stu-id="2407b-488">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP \_ 選項 \_ 傳送 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="2407b-489"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-490">設定或抓取不帶正負號的長整數值，其中包含要傳送要求或寫入部分資料的超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2407b-490">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="2407b-491">如果傳送要求的時間超過超時時間，則會取消傳送作業。</span><span class="sxs-lookup"><span data-stu-id="2407b-491">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="2407b-492">預設的超時時間為30秒。</span><span class="sxs-lookup"><span data-stu-id="2407b-492">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ 選項 \_ 伺服器 \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="2407b-493"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-494">取得 SecPkgCoNtext 系結 [**結構 \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) 的指標，此結構會指定 (CBT) 的通道系結 Token。</span><span class="sxs-lookup"><span data-stu-id="2407b-494">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="2407b-495">通道系結權杖是安全傳輸通道的屬性，可用來將驗證通道系結至安全傳輸通道。</span><span class="sxs-lookup"><span data-stu-id="2407b-495">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="2407b-496">只有在建立 SSL 連線之後，此選項才能取得此權杖。</span><span class="sxs-lookup"><span data-stu-id="2407b-496">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="2407b-497">傳遞此選項和 *lpBuffer* 至 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)的 **null** 值，將會傳回 \_ 錯誤 \_ 的緩衝區，以及 *lpdwBufferLength* 參數中緩衝區的必要位元組大小。</span><span class="sxs-lookup"><span data-stu-id="2407b-497">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="2407b-498">這個傳回的緩衝區大小值可以在後續的呼叫中傳遞，以查詢通道系結 Token。</span><span class="sxs-lookup"><span data-stu-id="2407b-498">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="2407b-499">\_ \_ \_ 如果您想要根據通道系結 Token 修改要求標頭，則在處理 WINHTTP 回呼狀態要求時，必須執行這些步驟。</span><span class="sxs-lookup"><span data-stu-id="2407b-499">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="2407b-500">請注意，Windows XP 和 Vista 不支援在此回呼期間修改要求標頭。</span><span class="sxs-lookup"><span data-stu-id="2407b-500">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 鏈 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="2407b-501"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-502">抓取伺服器憑證鏈內容。</span><span class="sxs-lookup"><span data-stu-id="2407b-502">Retrieves the server certification chain context.</span></span> <span data-ttu-id="2407b-503">**WINHTTP \_可以傳遞選項 \_ 伺服器憑證 \_ \_ 鏈 \_ 內容** ，以取得在協商 SSL 連線期間收到的伺服器憑證鏈的憑證 **\_ 鏈 \_ 內容** 重複指標。</span><span class="sxs-lookup"><span data-stu-id="2407b-503">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="2407b-504">用戶端必須在[](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)填入緩衝區的傳回 PCCERT \_ 內容指標上呼叫 CertFreeCertificateCoNtext。</span><span class="sxs-lookup"><span data-stu-id="2407b-504">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="2407b-505"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-506">抓取伺服器認證內容。</span><span class="sxs-lookup"><span data-stu-id="2407b-506">Retrieves the server certification context.</span></span> <span data-ttu-id="2407b-507">**WINHTTP \_您可以傳遞選項 \_ 伺服器憑證 \_ \_ 內容** ，以取得在協商 SSL 連線期間收到之伺服器憑證的憑證 [**內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) 重複指標。</span><span class="sxs-lookup"><span data-stu-id="2407b-507">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="2407b-508">用戶端必須在[](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)填入緩衝區的傳回 PCCERT \_ 內容指標上呼叫 CertFreeCertificateCoNtext。</span><span class="sxs-lookup"><span data-stu-id="2407b-508">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**已 \_ 使用 WINHTTP 選項 \_ 伺服器 \_ SPN \_**</span><span class="sxs-lookup"><span data-stu-id="2407b-509"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-510">取得 WinHTTP 在驗證期間提供給 SSPI 的伺服器伺服器主體名稱。</span><span class="sxs-lookup"><span data-stu-id="2407b-510">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="2407b-511">在驗證失敗之後，這個字串值可以傳遞給 [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-511">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP \_ 選項 \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="2407b-512"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-513">在建立 Kerberos 或協商 Kerberos 驗證的 SPN (服務主體名稱) 時，包含或移除伺服器埠號碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-513">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="2407b-514">此旗標是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="2407b-514">This flag is one of the following values:</span></span>

| <span data-ttu-id="2407b-515">詞彙</span><span class="sxs-lookup"><span data-stu-id="2407b-515">Term</span></span> | <span data-ttu-id="2407b-516">描述</span><span class="sxs-lookup"><span data-stu-id="2407b-516">Description</span></span> |
|-|-|
| <span data-ttu-id="2407b-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ 停用 \_ SPN \_ 伺服器 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="2407b-517"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="2407b-518">移除伺服器埠號碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-518">Removes the server port number.</span></span> |
| <span data-ttu-id="2407b-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ 啟用 \_ SPN \_ 伺服器 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="2407b-519"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="2407b-520">包括伺服器埠號碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-520">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="2407b-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP \_ 選項 \_ 資料流程 \_ 錯誤碼 \_**</span><span class="sxs-lookup"><span data-stu-id="2407b-521"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="2407b-522">此選項可在 WinHttp 要求控制碼上進行查詢，並會傳回由 HTTP 資料流程接收的 RST_STREAM 框架所指出的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-522">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP \_ 選項 \_ TCP \_ 快速 \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="2407b-523"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-524">啟用連接的 TCP Fast Open。</span><span class="sxs-lookup"><span data-stu-id="2407b-524">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP \_ 選項 \_ TCP \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="2407b-525"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-526">您可以在 WinHttp 會話控制碼上設定這個選項，以啟用基礎通訊端上的 TCP 保持連線行為。</span><span class="sxs-lookup"><span data-stu-id="2407b-526">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="2407b-527">接受 [**tcp \_ keepalive**](/windows/win32/winsock/sio-keepalive-vals) 結構。</span><span class="sxs-lookup"><span data-stu-id="2407b-527">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP \_ 選項 \_ TLS \_ FALSE \_ START**</span><span class="sxs-lookup"><span data-stu-id="2407b-528"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-529">啟用連接的 TLS False Start。</span><span class="sxs-lookup"><span data-stu-id="2407b-529">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP \_ 選項 \_ TLS \_ 通訊協定不 \_ 安全 \_ 的回復**</span><span class="sxs-lookup"><span data-stu-id="2407b-530"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-531">您可以在 WinHttp 會話控制碼上設定這個選項，以控制如果有較新的通訊協定版本的 TLS 交握失敗，是否允許回溯至 TLS 1.0。</span><span class="sxs-lookup"><span data-stu-id="2407b-531">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP \_ 選項 \_ UNLOAD \_ 通知 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="2407b-532"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-533">取得將在特定會話的最後一個回呼完成時設定的事件。</span><span class="sxs-lookup"><span data-stu-id="2407b-533">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="2407b-534">此旗標必須用於會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-534">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="2407b-535">事件必須等到 WinHTTP 設定後才能關閉。</span><span class="sxs-lookup"><span data-stu-id="2407b-535">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP \_ 選項 \_ UNSAFE \_ 標頭 \_ 剖析**</span><span class="sxs-lookup"><span data-stu-id="2407b-536"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-537">此選項已保留供內部使用，不應該呼叫。</span><span class="sxs-lookup"><span data-stu-id="2407b-537">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP \_ 選項 \_ 升級 \_ 至 \_ WEB \_ 通訊端**</span><span class="sxs-lookup"><span data-stu-id="2407b-538"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-539">指示堆疊使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)啟動 WebSocket 交握處理常式。</span><span class="sxs-lookup"><span data-stu-id="2407b-539">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="2407b-540">此選項不會使用任何參數。</span><span class="sxs-lookup"><span data-stu-id="2407b-540">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP \_ 選項 \_ URL**</span><span class="sxs-lookup"><span data-stu-id="2407b-541"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-542">抓取字串值，其中包含已下載資源的完整 URL。</span><span class="sxs-lookup"><span data-stu-id="2407b-542">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="2407b-543">如果原始 URL 包含任何額外的資料（例如搜尋字串或錨點），或重新導向呼叫，則傳回的 URL 會與原始的 URL 不同。</span><span class="sxs-lookup"><span data-stu-id="2407b-543">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="2407b-544">應用程式應該傳入緩衝區（以位元組為單位），這夠大，足以將傳回的 URL 保存在寬字元中。</span><span class="sxs-lookup"><span data-stu-id="2407b-544">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP \_ 選項 \_ 使用 \_ 全域 \_ 伺服器 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="2407b-545"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-546">採用 **BOOL** ，而且只能設定會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-546">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="2407b-547">它只會在設定選項之後，向下傳播至從會話控制碼建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2407b-547">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="2407b-548">若 **為 TRUE**，則此選項會導致最後使用從 WinInet 推入的全域伺服器認證。</span><span class="sxs-lookup"><span data-stu-id="2407b-548">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="2407b-549">此選項的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2407b-549">The default for this option is **FALSE**.</span></span> <span data-ttu-id="2407b-550">此選項需要登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings！ShareCredsWithWinHttp**。</span><span class="sxs-lookup"><span data-stu-id="2407b-550">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="2407b-551">依預設，此登錄機碼不存在。</span><span class="sxs-lookup"><span data-stu-id="2407b-551">This registry key is not present by default.</span></span> <span data-ttu-id="2407b-552">當設定時，WinINet 會將認證傳送至 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="2407b-552">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="2407b-553">每當 WinHttp 收到驗證挑戰，而且目前的控制碼上沒有設定任何認證時，就會使用 WinINet 提供的認證。</span><span class="sxs-lookup"><span data-stu-id="2407b-553">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP \_ 選項 \_ 使用者 \_ 代理程式**</span><span class="sxs-lookup"><span data-stu-id="2407b-554"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-555">設定或抓取 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)提供的控制碼上的 [*使用者代理程式*](glossary.md)字串，並在後續的 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)函式中使用，但前提是它不是由 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)或 **WinHttpSendRequest** 所加入的標頭所覆寫。</span><span class="sxs-lookup"><span data-stu-id="2407b-555">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="2407b-556">在抓取使用者代理程式時，應用程式應該傳入緩衝區（以位元組為單位），這夠大，足以將傳回的 URL 保存在寬字元中。</span><span class="sxs-lookup"><span data-stu-id="2407b-556">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="2407b-557">設定使用者代理程式時，緩衝區大小是字串的長度（以字元為單位），加上 **Null** 結束字元。</span><span class="sxs-lookup"><span data-stu-id="2407b-557">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP \_ 選項使用者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="2407b-558"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-559">設定或抓取包含使用者名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="2407b-559">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 關閉 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="2407b-560"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-561">設定 [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) 應該等候才能完成關閉信號交換的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2407b-561">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="2407b-562">預設值是 10 秒。</span><span class="sxs-lookup"><span data-stu-id="2407b-562">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ KEEPALIVE \_ 間隔**</span><span class="sxs-lookup"><span data-stu-id="2407b-563"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-564">設定透過連接傳送 keep-alive 封包的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="2407b-564">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="2407b-565">預設間隔為 30000 (30 秒) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-565">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="2407b-566">最小間隔為 15000 (15 秒) 。</span><span class="sxs-lookup"><span data-stu-id="2407b-566">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="2407b-567">使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 設定低於15000的值，將會傳回 **錯誤 \_ 不正確 \_ 參數**。</span><span class="sxs-lookup"><span data-stu-id="2407b-567">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="2407b-568">**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ KEEPALIVE \_ 間隔** 的預設值是從 **HKLM： \\ SOFTWARE \\ Microsoft \\ WebSocket \\ KeepaliveInterval** 進行讀取。</span><span class="sxs-lookup"><span data-stu-id="2407b-568">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="2407b-569">如果未設定值，則會使用預設值30000。</span><span class="sxs-lookup"><span data-stu-id="2407b-569">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="2407b-570">的 keepalive 間隔不能低於15000毫秒。</span><span class="sxs-lookup"><span data-stu-id="2407b-570">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 接收 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="2407b-571"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-572">設定或抓取 DWORD，以指定要用於 WebSocket 連接的接收緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="2407b-572">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 傳送 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="2407b-573"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-574">設定或抓取 DWORD，以指定要用於 WebSocket 連接的傳送緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="2407b-574">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP \_ 選項背景 \_ 工作 \_ 執行緒 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="2407b-575"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-576">設定不帶正負號的長整數值，指定執行緒集區應用於非同步完成的背景工作執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="2407b-576">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="2407b-577">此選項的預設值為零，表示工作者執行緒的數目等於系統上的 Cpu 數目。</span><span class="sxs-lookup"><span data-stu-id="2407b-577">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="2407b-578">此選項只能在發生非同步作業之前，在 **Null**  [HINTERNET](hinternet-handles-in-winhttp.md) 控制碼上設定。</span><span class="sxs-lookup"><span data-stu-id="2407b-578">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="2407b-579">此選項只能設定一次。</span><span class="sxs-lookup"><span data-stu-id="2407b-579">This option can only be set once.</span></span>

<span data-ttu-id="2407b-580">**Windows Server 2008 R2 和 windows 7：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="2407b-580">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2407b-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP \_ 選項 \_ 寫入 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="2407b-581"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2407b-582">此選項已被取代;它沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="2407b-582">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2407b-583">備註</span><span class="sxs-lookup"><span data-stu-id="2407b-583">Remarks</span></span>

<span data-ttu-id="2407b-584">下表列出選項旗標，方法是指定它們可以處理的控制碼、是否可以查詢和設定，以及使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="2407b-584">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="2407b-585">「X」表示選項旗標適用于與函式或控制碼搭配使用，而「-」指定選項旗標無效。</span><span class="sxs-lookup"><span data-stu-id="2407b-585">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="2407b-586">如果您嘗試在不支援的 Windows 版本上設定或查詢選項旗標，將會導致 **錯誤 \_ WINHTTP \_ 不正確 \_ 選項**。</span><span class="sxs-lookup"><span data-stu-id="2407b-586">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="2407b-587">選項旗標和資料類型</span><span class="sxs-lookup"><span data-stu-id="2407b-587">Option flag, and data type</span></span> | <span data-ttu-id="2407b-588">會話控制碼</span><span class="sxs-lookup"><span data-stu-id="2407b-588">Session handle</span></span> | <span data-ttu-id="2407b-589">要求控制碼</span><span class="sxs-lookup"><span data-stu-id="2407b-589">Request handle</span></span> | <span data-ttu-id="2407b-590">查詢選項</span><span class="sxs-lookup"><span data-stu-id="2407b-590">Query option</span></span> | <span data-ttu-id="2407b-591">Set 選項</span><span class="sxs-lookup"><span data-stu-id="2407b-591">Set option</span></span> | <span data-ttu-id="2407b-592">最低 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="2407b-592">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="2407b-593">WINHTTP \_ 選項有 \_ 保證 \_ 非 \_ 封鎖 \_ 回呼</span><span class="sxs-lookup"><span data-stu-id="2407b-593">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="2407b-594">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-594">**BOOL**</span></span> | <span data-ttu-id="2407b-595">X</span><span class="sxs-lookup"><span data-stu-id="2407b-595">X</span></span> | \- | \- | <span data-ttu-id="2407b-596">X</span><span class="sxs-lookup"><span data-stu-id="2407b-596">X</span></span> | \- |
| <span data-ttu-id="2407b-597">WINHTTP \_ 選項 \_ 自動登入 \_ 原則</span><span class="sxs-lookup"><span data-stu-id="2407b-597">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="2407b-598">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-598">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-599">X</span><span class="sxs-lookup"><span data-stu-id="2407b-599">X</span></span> | \- | <span data-ttu-id="2407b-600">X</span><span class="sxs-lookup"><span data-stu-id="2407b-600">X</span></span> | \- |
| <span data-ttu-id="2407b-601">WINHTTP \_ 選項 \_ 背景 \_ 連接</span><span class="sxs-lookup"><span data-stu-id="2407b-601">WINHTTP\_OPTION\_BACKGROUND\_CONNECTIONS</span></span><br/><span data-ttu-id="2407b-602">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-602">**DWORD**</span></span> | <span data-ttu-id="2407b-603">X</span><span class="sxs-lookup"><span data-stu-id="2407b-603">X</span></span> | \- | \- | <span data-ttu-id="2407b-604">X</span><span class="sxs-lookup"><span data-stu-id="2407b-604">X</span></span> | <span data-ttu-id="2407b-605">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="2407b-605">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="2407b-606">WINHTTP \_ 選項 \_ 回呼</span><span class="sxs-lookup"><span data-stu-id="2407b-606">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="2407b-607">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="2407b-607">**LPVOID**</span></span> | <span data-ttu-id="2407b-608">X</span><span class="sxs-lookup"><span data-stu-id="2407b-608">X</span></span> | <span data-ttu-id="2407b-609">X</span><span class="sxs-lookup"><span data-stu-id="2407b-609">X</span></span> | <span data-ttu-id="2407b-610">X</span><span class="sxs-lookup"><span data-stu-id="2407b-610">X</span></span> | <span data-ttu-id="2407b-611">X</span><span class="sxs-lookup"><span data-stu-id="2407b-611">X</span></span> | \- |
| <span data-ttu-id="2407b-612">WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容</span><span class="sxs-lookup"><span data-stu-id="2407b-612">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="2407b-613">**憑證 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="2407b-613">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="2407b-614">X</span><span class="sxs-lookup"><span data-stu-id="2407b-614">X</span></span> | \- | <span data-ttu-id="2407b-615">X</span><span class="sxs-lookup"><span data-stu-id="2407b-615">X</span></span> | <span data-ttu-id="2407b-616">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2407b-616">Windows Vista</span></span> |
| <span data-ttu-id="2407b-617">WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="2407b-617">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="2407b-618">**SecPkgCoNtext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="2407b-618">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="2407b-619">X</span><span class="sxs-lookup"><span data-stu-id="2407b-619">X</span></span> | <span data-ttu-id="2407b-620">X</span><span class="sxs-lookup"><span data-stu-id="2407b-620">X</span></span> | \- | <span data-ttu-id="2407b-621">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2407b-621">Windows Vista</span></span> |
| <span data-ttu-id="2407b-622">WINHTTP \_ 選項 \_ 字碼頁</span><span class="sxs-lookup"><span data-stu-id="2407b-622">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="2407b-623">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-623">**DWORD**</span></span> | <span data-ttu-id="2407b-624">X</span><span class="sxs-lookup"><span data-stu-id="2407b-624">X</span></span> | \- | \- | <span data-ttu-id="2407b-625">X</span><span class="sxs-lookup"><span data-stu-id="2407b-625">X</span></span> | \- |
| <span data-ttu-id="2407b-626">WINHTTP \_ 選項 \_ 設定 \_ PASSPORT \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="2407b-626">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="2407b-627">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-627">**DWORD**</span></span> | <span data-ttu-id="2407b-628">X</span><span class="sxs-lookup"><span data-stu-id="2407b-628">X</span></span> | \- | \- | <span data-ttu-id="2407b-629">X</span><span class="sxs-lookup"><span data-stu-id="2407b-629">X</span></span> | \- |
| <span data-ttu-id="2407b-630">WINHTTP \_ 選項 \_ 連接 \_ 重試</span><span class="sxs-lookup"><span data-stu-id="2407b-630">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="2407b-631">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-631">**DWORD**</span></span> | <span data-ttu-id="2407b-632">X</span><span class="sxs-lookup"><span data-stu-id="2407b-632">X</span></span> | <span data-ttu-id="2407b-633">X</span><span class="sxs-lookup"><span data-stu-id="2407b-633">X</span></span> | <span data-ttu-id="2407b-634">X</span><span class="sxs-lookup"><span data-stu-id="2407b-634">X</span></span> | <span data-ttu-id="2407b-635">X</span><span class="sxs-lookup"><span data-stu-id="2407b-635">X</span></span> | \- |
| <span data-ttu-id="2407b-636">WINHTTP \_ 選項 \_ 連接 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="2407b-636">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="2407b-637">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-637">**DWORD**</span></span> | <span data-ttu-id="2407b-638">X</span><span class="sxs-lookup"><span data-stu-id="2407b-638">X</span></span> | <span data-ttu-id="2407b-639">X</span><span class="sxs-lookup"><span data-stu-id="2407b-639">X</span></span> | <span data-ttu-id="2407b-640">X</span><span class="sxs-lookup"><span data-stu-id="2407b-640">X</span></span> | <span data-ttu-id="2407b-641">X</span><span class="sxs-lookup"><span data-stu-id="2407b-641">X</span></span> | \- |
| <span data-ttu-id="2407b-642">WINHTTP \_ 選項 \_ 連接 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="2407b-642">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="2407b-643">**WINHTTP \_ 連接 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="2407b-643">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="2407b-644">X</span><span class="sxs-lookup"><span data-stu-id="2407b-644">X</span></span> | <span data-ttu-id="2407b-645">X</span><span class="sxs-lookup"><span data-stu-id="2407b-645">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-646">WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V0</span><span class="sxs-lookup"><span data-stu-id="2407b-646">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="2407b-647">**TCP \_ 資訊 \_ v0**</span><span class="sxs-lookup"><span data-stu-id="2407b-647">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="2407b-648">X</span><span class="sxs-lookup"><span data-stu-id="2407b-648">X</span></span> | <span data-ttu-id="2407b-649">X</span><span class="sxs-lookup"><span data-stu-id="2407b-649">X</span></span> | \- | <span data-ttu-id="2407b-650">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="2407b-650">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="2407b-651">WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V1</span><span class="sxs-lookup"><span data-stu-id="2407b-651">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="2407b-652">**TCP \_ 資訊 \_ v1**</span><span class="sxs-lookup"><span data-stu-id="2407b-652">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="2407b-653">X</span><span class="sxs-lookup"><span data-stu-id="2407b-653">X</span></span> | <span data-ttu-id="2407b-654">X</span><span class="sxs-lookup"><span data-stu-id="2407b-654">X</span></span> | \- | <span data-ttu-id="2407b-655">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="2407b-655">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="2407b-656">WINHTTP \_ 選項 \_ 內容 \_ 值</span><span class="sxs-lookup"><span data-stu-id="2407b-656">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="2407b-657">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-657">**DWORD\_PTR**</span></span> | <span data-ttu-id="2407b-658">X</span><span class="sxs-lookup"><span data-stu-id="2407b-658">X</span></span> | <span data-ttu-id="2407b-659">X</span><span class="sxs-lookup"><span data-stu-id="2407b-659">X</span></span> | <span data-ttu-id="2407b-660">X</span><span class="sxs-lookup"><span data-stu-id="2407b-660">X</span></span> | <span data-ttu-id="2407b-661">X</span><span class="sxs-lookup"><span data-stu-id="2407b-661">X</span></span> | \- |
| <span data-ttu-id="2407b-662">WINHTTP \_ 選項 \_ 解壓縮</span><span class="sxs-lookup"><span data-stu-id="2407b-662">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="2407b-663">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-663">**DWORD**</span></span> | <span data-ttu-id="2407b-664">X</span><span class="sxs-lookup"><span data-stu-id="2407b-664">X</span></span> | <span data-ttu-id="2407b-665">X</span><span class="sxs-lookup"><span data-stu-id="2407b-665">X</span></span> | \- | <span data-ttu-id="2407b-666">X</span><span class="sxs-lookup"><span data-stu-id="2407b-666">X</span></span> | <span data-ttu-id="2407b-667">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2407b-667">Windows 8.1</span></span> |
| <span data-ttu-id="2407b-668">WINHTTP \_ 選項 \_ 停用 \_ CERT \_ 鏈 \_ 建立</span><span class="sxs-lookup"><span data-stu-id="2407b-668">WINHTTP\_OPTION\_DISABLE\_CERT\_CHAIN\_BUILDING</span></span><br/><span data-ttu-id="2407b-669">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-669">**BOOL**</span></span> | <span data-ttu-id="2407b-670">X</span><span class="sxs-lookup"><span data-stu-id="2407b-670">X</span></span> | \- | \- | <span data-ttu-id="2407b-671">X</span><span class="sxs-lookup"><span data-stu-id="2407b-671">X</span></span> | <span data-ttu-id="2407b-672">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="2407b-672">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="2407b-673">WINHTTP \_ 選項 \_ 停用 \_ 功能</span><span class="sxs-lookup"><span data-stu-id="2407b-673">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="2407b-674">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-674">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-675">X</span><span class="sxs-lookup"><span data-stu-id="2407b-675">X</span></span> | \- | <span data-ttu-id="2407b-676">X</span><span class="sxs-lookup"><span data-stu-id="2407b-676">X</span></span> | \- |
| <span data-ttu-id="2407b-677">WINHTTP \_ 選項 \_ 停用 \_ 安全 \_ 通訊協定 \_ 回復</span><span class="sxs-lookup"><span data-stu-id="2407b-677">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="2407b-678">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-678">**BOOL**</span></span> | <span data-ttu-id="2407b-679">X</span><span class="sxs-lookup"><span data-stu-id="2407b-679">X</span></span> | \- | \- | <span data-ttu-id="2407b-680">X</span><span class="sxs-lookup"><span data-stu-id="2407b-680">X</span></span> | <span data-ttu-id="2407b-681">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="2407b-681">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="2407b-682">WINHTTP \_ 選項 \_ 停用 \_ 串流 \_ 佇列</span><span class="sxs-lookup"><span data-stu-id="2407b-682">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="2407b-683">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-683">**BOOL**</span></span> | <span data-ttu-id="2407b-684">X</span><span class="sxs-lookup"><span data-stu-id="2407b-684">X</span></span> | <span data-ttu-id="2407b-685">X</span><span class="sxs-lookup"><span data-stu-id="2407b-685">X</span></span> | \- | <span data-ttu-id="2407b-686">X</span><span class="sxs-lookup"><span data-stu-id="2407b-686">X</span></span> | <span data-ttu-id="2407b-687">Windows 10 版本1809</span><span class="sxs-lookup"><span data-stu-id="2407b-687">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="2407b-688">WINHTTP \_ 選項 \_ 啟用 \_ 功能</span><span class="sxs-lookup"><span data-stu-id="2407b-688">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="2407b-689">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-689">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="2407b-690">X</span><span class="sxs-lookup"><span data-stu-id="2407b-690">X</span></span> | \- |
| <span data-ttu-id="2407b-691">WINHTTP \_ 選項 \_ 啟用 \_ HTTP \_ 通訊協定</span><span class="sxs-lookup"><span data-stu-id="2407b-691">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="2407b-692">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-692">**DWORD**</span></span> | <span data-ttu-id="2407b-693">X</span><span class="sxs-lookup"><span data-stu-id="2407b-693">X</span></span> | <span data-ttu-id="2407b-694">X</span><span class="sxs-lookup"><span data-stu-id="2407b-694">X</span></span> | \- | <span data-ttu-id="2407b-695">X</span><span class="sxs-lookup"><span data-stu-id="2407b-695">X</span></span> | <span data-ttu-id="2407b-696">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="2407b-696">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="2407b-697">WINHTTP \_ 選項 \_ ENABLE \_ HTTP2 \_ PLUS \_ CLIENT \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="2407b-697">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="2407b-698">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-698">**BOOL**</span></span> | <span data-ttu-id="2407b-699">X</span><span class="sxs-lookup"><span data-stu-id="2407b-699">X</span></span> | \- | \- | <span data-ttu-id="2407b-700">X</span><span class="sxs-lookup"><span data-stu-id="2407b-700">X</span></span> | <span data-ttu-id="2407b-701">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="2407b-701">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="2407b-702">WINHTTP \_ 選項 \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="2407b-702">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="2407b-703">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-703">**DWORD**</span></span> | \- | \- | <span data-ttu-id="2407b-704">X</span><span class="sxs-lookup"><span data-stu-id="2407b-704">X</span></span> | <span data-ttu-id="2407b-705">X</span><span class="sxs-lookup"><span data-stu-id="2407b-705">X</span></span> | \- |
| <span data-ttu-id="2407b-706">WINHTTP \_ 選項 \_ 編碼 \_ 額外</span><span class="sxs-lookup"><span data-stu-id="2407b-706">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="2407b-707">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-707">**BOOL**</span></span> | <span data-ttu-id="2407b-708">X</span><span class="sxs-lookup"><span data-stu-id="2407b-708">X</span></span> | <span data-ttu-id="2407b-709">X</span><span class="sxs-lookup"><span data-stu-id="2407b-709">X</span></span> | \- | <span data-ttu-id="2407b-710">X</span><span class="sxs-lookup"><span data-stu-id="2407b-710">X</span></span> | <span data-ttu-id="2407b-711">Windows 10 版本1803</span><span class="sxs-lookup"><span data-stu-id="2407b-711">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="2407b-712">WINHTTP \_ 選項 \_ 到期 \_ 連接</span><span class="sxs-lookup"><span data-stu-id="2407b-712">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="2407b-713">N/A</span><span class="sxs-lookup"><span data-stu-id="2407b-713">N/A</span></span> | \- | <span data-ttu-id="2407b-714">X</span><span class="sxs-lookup"><span data-stu-id="2407b-714">X</span></span> | \- | <span data-ttu-id="2407b-715">X</span><span class="sxs-lookup"><span data-stu-id="2407b-715">X</span></span> | <span data-ttu-id="2407b-716">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="2407b-716">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="2407b-717">WINHTTP \_ 選項 \_ 延伸 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="2407b-717">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="2407b-718">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-718">**DWORD**</span></span> | <span data-ttu-id="2407b-719">X</span><span class="sxs-lookup"><span data-stu-id="2407b-719">X</span></span> | <span data-ttu-id="2407b-720">X</span><span class="sxs-lookup"><span data-stu-id="2407b-720">X</span></span> | <span data-ttu-id="2407b-721">X</span><span class="sxs-lookup"><span data-stu-id="2407b-721">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-722">WINHTTP \_ 選項 \_ FIRST \_ 可用 \_ 連接</span><span class="sxs-lookup"><span data-stu-id="2407b-722">WINHTTP\_OPTION\_FIRST\_AVAILABLE\_CONNECTION</span></span><br/><span data-ttu-id="2407b-723">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-723">**BOOL**</span></span> | <span data-ttu-id="2407b-724">X</span><span class="sxs-lookup"><span data-stu-id="2407b-724">X</span></span> | \- | \- | <span data-ttu-id="2407b-725">X</span><span class="sxs-lookup"><span data-stu-id="2407b-725">X</span></span> | <span data-ttu-id="2407b-726">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="2407b-726">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="2407b-727">WINHTTP \_ 選項 \_ 全域 \_ PROXY \_ 認證</span><span class="sxs-lookup"><span data-stu-id="2407b-727">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="2407b-728">**WINHTTP \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="2407b-728">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="2407b-729">X</span><span class="sxs-lookup"><span data-stu-id="2407b-729">X</span></span> | <span data-ttu-id="2407b-730">X</span><span class="sxs-lookup"><span data-stu-id="2407b-730">X</span></span> | \- | <span data-ttu-id="2407b-731">X</span><span class="sxs-lookup"><span data-stu-id="2407b-731">X</span></span> | \- |
| <span data-ttu-id="2407b-732">WINHTTP \_ 選項 \_ 全域 \_ 伺服器 \_ 認證</span><span class="sxs-lookup"><span data-stu-id="2407b-732">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="2407b-733">**WINHTTP \_ 認證 \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="2407b-733">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="2407b-734">X</span><span class="sxs-lookup"><span data-stu-id="2407b-734">X</span></span> | <span data-ttu-id="2407b-735">X</span><span class="sxs-lookup"><span data-stu-id="2407b-735">X</span></span> | \- | <span data-ttu-id="2407b-736">X</span><span class="sxs-lookup"><span data-stu-id="2407b-736">X</span></span> | \- |
| <span data-ttu-id="2407b-737">WINHTTP \_ 選項 \_ 控制碼 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="2407b-737">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="2407b-738">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-738">**DWORD**</span></span> | <span data-ttu-id="2407b-739">X</span><span class="sxs-lookup"><span data-stu-id="2407b-739">X</span></span> | <span data-ttu-id="2407b-740">X</span><span class="sxs-lookup"><span data-stu-id="2407b-740">X</span></span> | <span data-ttu-id="2407b-741">X</span><span class="sxs-lookup"><span data-stu-id="2407b-741">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-742">\_需要 WINHTTP 選項 \_ HTTP \_ 通訊協定 \_</span><span class="sxs-lookup"><span data-stu-id="2407b-742">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="2407b-743">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-743">**BOOL**</span></span> | <span data-ttu-id="2407b-744">X</span><span class="sxs-lookup"><span data-stu-id="2407b-744">X</span></span> | <span data-ttu-id="2407b-745">X</span><span class="sxs-lookup"><span data-stu-id="2407b-745">X</span></span> | \- | <span data-ttu-id="2407b-746">X</span><span class="sxs-lookup"><span data-stu-id="2407b-746">X</span></span> | <span data-ttu-id="2407b-747">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="2407b-747">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="2407b-748">使用的 WINHTTP \_ 選項 \_ HTTP \_ 通訊協定 \_</span><span class="sxs-lookup"><span data-stu-id="2407b-748">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="2407b-749">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-749">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-750">X</span><span class="sxs-lookup"><span data-stu-id="2407b-750">X</span></span> | <span data-ttu-id="2407b-751">X</span><span class="sxs-lookup"><span data-stu-id="2407b-751">X</span></span> | \- | <span data-ttu-id="2407b-752">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="2407b-752">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="2407b-753">WINHTTP \_ 選項 \_ HTTP \_ 版本</span><span class="sxs-lookup"><span data-stu-id="2407b-753">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="2407b-754">**HTTP \_ 版本 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="2407b-754">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="2407b-755">X</span><span class="sxs-lookup"><span data-stu-id="2407b-755">X</span></span> | <span data-ttu-id="2407b-756">X</span><span class="sxs-lookup"><span data-stu-id="2407b-756">X</span></span> | <span data-ttu-id="2407b-757">X</span><span class="sxs-lookup"><span data-stu-id="2407b-757">X</span></span> | <span data-ttu-id="2407b-758">X</span><span class="sxs-lookup"><span data-stu-id="2407b-758">X</span></span> | \- |
| <span data-ttu-id="2407b-759">WINHTTP \_ 選項 \_ HTTP2 \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="2407b-759">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="2407b-760">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-760">**DWORD**</span></span> | <span data-ttu-id="2407b-761">X</span><span class="sxs-lookup"><span data-stu-id="2407b-761">X</span></span> | \- | \- | <span data-ttu-id="2407b-762">X</span><span class="sxs-lookup"><span data-stu-id="2407b-762">X</span></span> | <span data-ttu-id="2407b-763">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="2407b-763">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="2407b-764">WINHTTP \_ 選項 \_ HTTP2 \_ PLUS \_ 傳輸 \_ 編碼</span><span class="sxs-lookup"><span data-stu-id="2407b-764">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="2407b-765">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-765">**BOOL**</span></span> | <span data-ttu-id="2407b-766">X</span><span class="sxs-lookup"><span data-stu-id="2407b-766">X</span></span> | <span data-ttu-id="2407b-767">X</span><span class="sxs-lookup"><span data-stu-id="2407b-767">X</span></span> | \- | <span data-ttu-id="2407b-768">X</span><span class="sxs-lookup"><span data-stu-id="2407b-768">X</span></span> | <span data-ttu-id="2407b-769">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="2407b-769">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="2407b-770">WINHTTP \_ 選項會 \_ 離線略過憑證 \_ \_ 撤銷 \_</span><span class="sxs-lookup"><span data-stu-id="2407b-770">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="2407b-771">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-771">**BOOL**</span></span> | \- | <span data-ttu-id="2407b-772">X</span><span class="sxs-lookup"><span data-stu-id="2407b-772">X</span></span> | \- | <span data-ttu-id="2407b-773">X</span><span class="sxs-lookup"><span data-stu-id="2407b-773">X</span></span> | <span data-ttu-id="2407b-774">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="2407b-774">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="2407b-775">WINHTTP \_ OPTION \_ IPV6 \_ FAST \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="2407b-775">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="2407b-776">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-776">**BOOL**</span></span> | <span data-ttu-id="2407b-777">X</span><span class="sxs-lookup"><span data-stu-id="2407b-777">X</span></span> | \- | \- | <span data-ttu-id="2407b-778">X</span><span class="sxs-lookup"><span data-stu-id="2407b-778">X</span></span> | <span data-ttu-id="2407b-779">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="2407b-779">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="2407b-780">WINHTTP \_ 選項 \_ 為 \_ PROXY \_ CONNECT \_ 回應</span><span class="sxs-lookup"><span data-stu-id="2407b-780">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="2407b-781">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-781">**BOOL**</span></span> | <span data-ttu-id="2407b-782">X</span><span class="sxs-lookup"><span data-stu-id="2407b-782">X</span></span> | <span data-ttu-id="2407b-783">X</span><span class="sxs-lookup"><span data-stu-id="2407b-783">X</span></span> | <span data-ttu-id="2407b-784">X</span><span class="sxs-lookup"><span data-stu-id="2407b-784">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-785">\_ \_ \_ \_ 每 \_ 1 \_ 0 部 \_ 伺服器的 WINHTTP 選項 MAX CONNS</span><span class="sxs-lookup"><span data-stu-id="2407b-785">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="2407b-786">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-786">**DWORD**</span></span> | <span data-ttu-id="2407b-787">X</span><span class="sxs-lookup"><span data-stu-id="2407b-787">X</span></span> | \- | <span data-ttu-id="2407b-788">X</span><span class="sxs-lookup"><span data-stu-id="2407b-788">X</span></span> | <span data-ttu-id="2407b-789">X</span><span class="sxs-lookup"><span data-stu-id="2407b-789">X</span></span> | \- |
| <span data-ttu-id="2407b-790">每一伺服器的 WINHTTP \_ 選項 \_ MAX \_ CONNS \_ \_</span><span class="sxs-lookup"><span data-stu-id="2407b-790">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="2407b-791">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-791">**DWORD**</span></span> | <span data-ttu-id="2407b-792">X</span><span class="sxs-lookup"><span data-stu-id="2407b-792">X</span></span> | \- | <span data-ttu-id="2407b-793">X</span><span class="sxs-lookup"><span data-stu-id="2407b-793">X</span></span> | <span data-ttu-id="2407b-794">X</span><span class="sxs-lookup"><span data-stu-id="2407b-794">X</span></span> | \- |
| <span data-ttu-id="2407b-795">WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 自動重新 \_ 導向</span><span class="sxs-lookup"><span data-stu-id="2407b-795">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="2407b-796">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-796">**DWORD**</span></span> | <span data-ttu-id="2407b-797">X</span><span class="sxs-lookup"><span data-stu-id="2407b-797">X</span></span> | <span data-ttu-id="2407b-798">X</span><span class="sxs-lookup"><span data-stu-id="2407b-798">X</span></span> | <span data-ttu-id="2407b-799">X</span><span class="sxs-lookup"><span data-stu-id="2407b-799">X</span></span> | <span data-ttu-id="2407b-800">X</span><span class="sxs-lookup"><span data-stu-id="2407b-800">X</span></span> | \- |
| <span data-ttu-id="2407b-801">WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 狀態 \_ 繼續</span><span class="sxs-lookup"><span data-stu-id="2407b-801">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="2407b-802">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-802">**DWORD**</span></span> | <span data-ttu-id="2407b-803">X</span><span class="sxs-lookup"><span data-stu-id="2407b-803">X</span></span> | <span data-ttu-id="2407b-804">X</span><span class="sxs-lookup"><span data-stu-id="2407b-804">X</span></span> | <span data-ttu-id="2407b-805">X</span><span class="sxs-lookup"><span data-stu-id="2407b-805">X</span></span> | <span data-ttu-id="2407b-806">X</span><span class="sxs-lookup"><span data-stu-id="2407b-806">X</span></span> | \- |
| <span data-ttu-id="2407b-807">WINHTTP \_ 選項 \_ \_ 回應 \_ 清空最 \_ 大值</span><span class="sxs-lookup"><span data-stu-id="2407b-807">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="2407b-808">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-808">**DWORD**</span></span> | <span data-ttu-id="2407b-809">X</span><span class="sxs-lookup"><span data-stu-id="2407b-809">X</span></span> | <span data-ttu-id="2407b-810">X</span><span class="sxs-lookup"><span data-stu-id="2407b-810">X</span></span> | <span data-ttu-id="2407b-811">X</span><span class="sxs-lookup"><span data-stu-id="2407b-811">X</span></span> | <span data-ttu-id="2407b-812">X</span><span class="sxs-lookup"><span data-stu-id="2407b-812">X</span></span> | \- |
| <span data-ttu-id="2407b-813">WINHTTP \_ 選項 \_ 的 \_ 回應 \_ 標頭 \_ 大小上限</span><span class="sxs-lookup"><span data-stu-id="2407b-813">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="2407b-814">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-814">**DWORD**</span></span> | <span data-ttu-id="2407b-815">X</span><span class="sxs-lookup"><span data-stu-id="2407b-815">X</span></span> | <span data-ttu-id="2407b-816">X</span><span class="sxs-lookup"><span data-stu-id="2407b-816">X</span></span> | <span data-ttu-id="2407b-817">X</span><span class="sxs-lookup"><span data-stu-id="2407b-817">X</span></span> | <span data-ttu-id="2407b-818">X</span><span class="sxs-lookup"><span data-stu-id="2407b-818">X</span></span> | \- |
| <span data-ttu-id="2407b-819">WINHTTP \_ 選項 \_ 父 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="2407b-819">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="2407b-820">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="2407b-820">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="2407b-821">X</span><span class="sxs-lookup"><span data-stu-id="2407b-821">X</span></span> | <span data-ttu-id="2407b-822">X</span><span class="sxs-lookup"><span data-stu-id="2407b-822">X</span></span> | <span data-ttu-id="2407b-823">X</span><span class="sxs-lookup"><span data-stu-id="2407b-823">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-824">WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ 文字</span><span class="sxs-lookup"><span data-stu-id="2407b-824">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="2407b-825">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-825">**LPWSTR**</span></span> | \- | <span data-ttu-id="2407b-826">X</span><span class="sxs-lookup"><span data-stu-id="2407b-826">X</span></span> | <span data-ttu-id="2407b-827">X</span><span class="sxs-lookup"><span data-stu-id="2407b-827">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-828">WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ URL</span><span class="sxs-lookup"><span data-stu-id="2407b-828">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="2407b-829">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-829">**LPWSTR**</span></span> | \- | <span data-ttu-id="2407b-830">X</span><span class="sxs-lookup"><span data-stu-id="2407b-830">X</span></span> | <span data-ttu-id="2407b-831">X</span><span class="sxs-lookup"><span data-stu-id="2407b-831">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-832">WINHTTP \_ 選項 \_ PASSPORT \_ RETURN \_ URL</span><span class="sxs-lookup"><span data-stu-id="2407b-832">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="2407b-833">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="2407b-833">**LPVOID**</span></span> | \- | <span data-ttu-id="2407b-834">X</span><span class="sxs-lookup"><span data-stu-id="2407b-834">X</span></span> | <span data-ttu-id="2407b-835">X</span><span class="sxs-lookup"><span data-stu-id="2407b-835">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-836">WINHTTP \_ 選項 \_ PASSPORT \_ 登出 \_</span><span class="sxs-lookup"><span data-stu-id="2407b-836">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="2407b-837">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="2407b-837">**LPVOID**</span></span> | <span data-ttu-id="2407b-838">X</span><span class="sxs-lookup"><span data-stu-id="2407b-838">X</span></span> | \- | \- | <span data-ttu-id="2407b-839">X</span><span class="sxs-lookup"><span data-stu-id="2407b-839">X</span></span> | \- |
| <span data-ttu-id="2407b-840">WINHTTP \_ 選項 \_ 密碼</span><span class="sxs-lookup"><span data-stu-id="2407b-840">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="2407b-841">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-841">**LPWSTR**</span></span> | \- | <span data-ttu-id="2407b-842">X</span><span class="sxs-lookup"><span data-stu-id="2407b-842">X</span></span> | <span data-ttu-id="2407b-843">X</span><span class="sxs-lookup"><span data-stu-id="2407b-843">X</span></span> | <span data-ttu-id="2407b-844">X</span><span class="sxs-lookup"><span data-stu-id="2407b-844">X</span></span> | \- |
| <span data-ttu-id="2407b-845">WINHTTP \_ 選項 \_ PROXY</span><span class="sxs-lookup"><span data-stu-id="2407b-845">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="2407b-846">**WINHTTP \_ PROXY \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="2407b-846">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="2407b-847">X</span><span class="sxs-lookup"><span data-stu-id="2407b-847">X</span></span> | <span data-ttu-id="2407b-848">X</span><span class="sxs-lookup"><span data-stu-id="2407b-848">X</span></span> | <span data-ttu-id="2407b-849">X</span><span class="sxs-lookup"><span data-stu-id="2407b-849">X</span></span> | <span data-ttu-id="2407b-850">X</span><span class="sxs-lookup"><span data-stu-id="2407b-850">X</span></span> | \- |
| <span data-ttu-id="2407b-851">WINHTTP \_ 選項 \_ PROXY \_ 密碼</span><span class="sxs-lookup"><span data-stu-id="2407b-851">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="2407b-852">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-852">**LPWSTR**</span></span> | \- | <span data-ttu-id="2407b-853">X</span><span class="sxs-lookup"><span data-stu-id="2407b-853">X</span></span> | <span data-ttu-id="2407b-854">X</span><span class="sxs-lookup"><span data-stu-id="2407b-854">X</span></span> | <span data-ttu-id="2407b-855">X</span><span class="sxs-lookup"><span data-stu-id="2407b-855">X</span></span> | \- |
| <span data-ttu-id="2407b-856">已 \_ 使用 WINHTTP 選項 \_ PROXY \_ SPN \_</span><span class="sxs-lookup"><span data-stu-id="2407b-856">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="2407b-857">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-857">**LPWSTR**</span></span> | \- | <span data-ttu-id="2407b-858">X</span><span class="sxs-lookup"><span data-stu-id="2407b-858">X</span></span> | <span data-ttu-id="2407b-859">X</span><span class="sxs-lookup"><span data-stu-id="2407b-859">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-860">WINHTTP \_ 選項 \_ PROXY 使用者 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="2407b-860">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="2407b-861">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-861">**LPWSTR**</span></span> | \- | <span data-ttu-id="2407b-862">X</span><span class="sxs-lookup"><span data-stu-id="2407b-862">X</span></span> | <span data-ttu-id="2407b-863">X</span><span class="sxs-lookup"><span data-stu-id="2407b-863">X</span></span> | <span data-ttu-id="2407b-864">X</span><span class="sxs-lookup"><span data-stu-id="2407b-864">X</span></span> | \- |
| <span data-ttu-id="2407b-865">WINHTTP \_ 選項 \_ 讀取 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="2407b-865">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="2407b-866">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-866">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-867">X</span><span class="sxs-lookup"><span data-stu-id="2407b-867">X</span></span> | <span data-ttu-id="2407b-868">X</span><span class="sxs-lookup"><span data-stu-id="2407b-868">X</span></span> | <span data-ttu-id="2407b-869">X</span><span class="sxs-lookup"><span data-stu-id="2407b-869">X</span></span> | \- |
| <span data-ttu-id="2407b-870">WINHTTP \_ 選項 \_ 接收 \_ PROXY \_ CONNECT \_ 回應</span><span class="sxs-lookup"><span data-stu-id="2407b-870">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="2407b-871">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-871">**BOOL**</span></span> | <span data-ttu-id="2407b-872">X</span><span class="sxs-lookup"><span data-stu-id="2407b-872">X</span></span> | <span data-ttu-id="2407b-873">X</span><span class="sxs-lookup"><span data-stu-id="2407b-873">X</span></span> | \- | <span data-ttu-id="2407b-874">X</span><span class="sxs-lookup"><span data-stu-id="2407b-874">X</span></span> | \- |
| <span data-ttu-id="2407b-875">WINHTTP \_ 選項 \_ 接收 \_ 回應 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="2407b-875">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="2407b-876">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-876">**DWORD**</span></span> | <span data-ttu-id="2407b-877">X</span><span class="sxs-lookup"><span data-stu-id="2407b-877">X</span></span> | <span data-ttu-id="2407b-878">X</span><span class="sxs-lookup"><span data-stu-id="2407b-878">X</span></span> | <span data-ttu-id="2407b-879">X</span><span class="sxs-lookup"><span data-stu-id="2407b-879">X</span></span> | <span data-ttu-id="2407b-880">X</span><span class="sxs-lookup"><span data-stu-id="2407b-880">X</span></span> | \- |
| <span data-ttu-id="2407b-881">WINHTTP \_ 選項 \_ 接收 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="2407b-881">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="2407b-882">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-882">**DWORD**</span></span> | <span data-ttu-id="2407b-883">X</span><span class="sxs-lookup"><span data-stu-id="2407b-883">X</span></span> | <span data-ttu-id="2407b-884">X</span><span class="sxs-lookup"><span data-stu-id="2407b-884">X</span></span> | <span data-ttu-id="2407b-885">X</span><span class="sxs-lookup"><span data-stu-id="2407b-885">X</span></span> | <span data-ttu-id="2407b-886">X</span><span class="sxs-lookup"><span data-stu-id="2407b-886">X</span></span> | \- |
| <span data-ttu-id="2407b-887">WINHTTP \_ 選項重新 \_ 導向 \_ 原則</span><span class="sxs-lookup"><span data-stu-id="2407b-887">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="2407b-888">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-888">**DWORD**</span></span> | <span data-ttu-id="2407b-889">X</span><span class="sxs-lookup"><span data-stu-id="2407b-889">X</span></span> | <span data-ttu-id="2407b-890">X</span><span class="sxs-lookup"><span data-stu-id="2407b-890">X</span></span> | <span data-ttu-id="2407b-891">X</span><span class="sxs-lookup"><span data-stu-id="2407b-891">X</span></span> | <span data-ttu-id="2407b-892">X</span><span class="sxs-lookup"><span data-stu-id="2407b-892">X</span></span> | \- |
| <span data-ttu-id="2407b-893">WINHTTP \_ 選項 \_ 拒絕 \_ \_ URL 中的 USERPWD \_</span><span class="sxs-lookup"><span data-stu-id="2407b-893">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="2407b-894">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-894">**BOOL**</span></span> | \- | <span data-ttu-id="2407b-895">X</span><span class="sxs-lookup"><span data-stu-id="2407b-895">X</span></span> | \- | <span data-ttu-id="2407b-896">X</span><span class="sxs-lookup"><span data-stu-id="2407b-896">X</span></span> | \- |
| <span data-ttu-id="2407b-897">WINHTTP \_ 選項 \_ 要求 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="2407b-897">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="2407b-898">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-898">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-899">X</span><span class="sxs-lookup"><span data-stu-id="2407b-899">X</span></span> | <span data-ttu-id="2407b-900">X</span><span class="sxs-lookup"><span data-stu-id="2407b-900">X</span></span> | <span data-ttu-id="2407b-901">X</span><span class="sxs-lookup"><span data-stu-id="2407b-901">X</span></span> | \- |
| <span data-ttu-id="2407b-902">WINHTTP \_ 選項 \_ 要求 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="2407b-902">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="2407b-903">**WINHTTP \_ 要求 \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="2407b-903">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="2407b-904">X</span><span class="sxs-lookup"><span data-stu-id="2407b-904">X</span></span> | <span data-ttu-id="2407b-905">X</span><span class="sxs-lookup"><span data-stu-id="2407b-905">X</span></span> | \- | <span data-ttu-id="2407b-906">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="2407b-906">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="2407b-907">WINHTTP \_ 選項 \_ 要求 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="2407b-907">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="2407b-908">**WINHTTP \_ 要求 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="2407b-908">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="2407b-909">X</span><span class="sxs-lookup"><span data-stu-id="2407b-909">X</span></span> | <span data-ttu-id="2407b-910">X</span><span class="sxs-lookup"><span data-stu-id="2407b-910">X</span></span> | \- | <span data-ttu-id="2407b-911">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="2407b-911">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="2407b-912">WINHTTP \_ 選項 \_ 需要 \_ STREAM \_ END</span><span class="sxs-lookup"><span data-stu-id="2407b-912">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="2407b-913">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-913">**BOOL**</span></span> | <span data-ttu-id="2407b-914">X</span><span class="sxs-lookup"><span data-stu-id="2407b-914">X</span></span> | <span data-ttu-id="2407b-915">X</span><span class="sxs-lookup"><span data-stu-id="2407b-915">X</span></span> | \- | <span data-ttu-id="2407b-916">X</span><span class="sxs-lookup"><span data-stu-id="2407b-916">X</span></span> | <span data-ttu-id="2407b-917">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="2407b-917">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="2407b-918">WINHTTP \_ 選項 \_ 解析 \_ 主機名稱</span><span class="sxs-lookup"><span data-stu-id="2407b-918">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="2407b-919">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-919">**LPWSTR**</span></span> | \- | <span data-ttu-id="2407b-920">X</span><span class="sxs-lookup"><span data-stu-id="2407b-920">X</span></span> | \- | <span data-ttu-id="2407b-921">X</span><span class="sxs-lookup"><span data-stu-id="2407b-921">X</span></span> | <span data-ttu-id="2407b-922">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="2407b-922">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="2407b-923">WINHTTP \_ 選項 \_ 解析 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="2407b-923">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="2407b-924">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-924">**DWORD**</span></span> | <span data-ttu-id="2407b-925">X</span><span class="sxs-lookup"><span data-stu-id="2407b-925">X</span></span> | <span data-ttu-id="2407b-926">X</span><span class="sxs-lookup"><span data-stu-id="2407b-926">X</span></span> | <span data-ttu-id="2407b-927">X</span><span class="sxs-lookup"><span data-stu-id="2407b-927">X</span></span> | <span data-ttu-id="2407b-928">X</span><span class="sxs-lookup"><span data-stu-id="2407b-928">X</span></span> | \- |
| <span data-ttu-id="2407b-929">WINHTTP \_ 選項 \_ 安全 \_ 通訊協定</span><span class="sxs-lookup"><span data-stu-id="2407b-929">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="2407b-930">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-930">**DWORD**</span></span> | <span data-ttu-id="2407b-931">X</span><span class="sxs-lookup"><span data-stu-id="2407b-931">X</span></span> | \- | \- | <span data-ttu-id="2407b-932">X</span><span class="sxs-lookup"><span data-stu-id="2407b-932">X</span></span> | \- |
| <span data-ttu-id="2407b-933">WINHTTP \_ 選項 \_ 安全性 \_ 憑證 \_ 結構</span><span class="sxs-lookup"><span data-stu-id="2407b-933">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="2407b-934">**WINHTTP \_ 憑證 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="2407b-934">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="2407b-935">X</span><span class="sxs-lookup"><span data-stu-id="2407b-935">X</span></span> | <span data-ttu-id="2407b-936">X</span><span class="sxs-lookup"><span data-stu-id="2407b-936">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-937">WINHTTP \_ 選項 \_ 安全性 \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="2407b-937">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="2407b-938">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-938">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-939">X</span><span class="sxs-lookup"><span data-stu-id="2407b-939">X</span></span> | <span data-ttu-id="2407b-940">X</span><span class="sxs-lookup"><span data-stu-id="2407b-940">X</span></span> | <span data-ttu-id="2407b-941">X</span><span class="sxs-lookup"><span data-stu-id="2407b-941">X</span></span> | \- |
| <span data-ttu-id="2407b-942">WINHTTP \_ 選項 \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="2407b-942">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="2407b-943">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="2407b-943">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="2407b-944">X</span><span class="sxs-lookup"><span data-stu-id="2407b-944">X</span></span> | <span data-ttu-id="2407b-945">X</span><span class="sxs-lookup"><span data-stu-id="2407b-945">X</span></span> | \- | <span data-ttu-id="2407b-946">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="2407b-946">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="2407b-947">WINHTTP \_ 選項 \_ 安全性 \_ 金鑰 \_ 位</span><span class="sxs-lookup"><span data-stu-id="2407b-947">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="2407b-948">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-948">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-949">X</span><span class="sxs-lookup"><span data-stu-id="2407b-949">X</span></span> | <span data-ttu-id="2407b-950">X</span><span class="sxs-lookup"><span data-stu-id="2407b-950">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-951">WINHTTP \_ 選項 \_ 傳送 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="2407b-951">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="2407b-952">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-952">**DWORD**</span></span> | <span data-ttu-id="2407b-953">X</span><span class="sxs-lookup"><span data-stu-id="2407b-953">X</span></span> | <span data-ttu-id="2407b-954">X</span><span class="sxs-lookup"><span data-stu-id="2407b-954">X</span></span> | <span data-ttu-id="2407b-955">X</span><span class="sxs-lookup"><span data-stu-id="2407b-955">X</span></span> | <span data-ttu-id="2407b-956">X</span><span class="sxs-lookup"><span data-stu-id="2407b-956">X</span></span> | \- |
| <span data-ttu-id="2407b-957">WINHTTP \_ 選項 \_ 伺服器 \_ CBT</span><span class="sxs-lookup"><span data-stu-id="2407b-957">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="2407b-958">[**SecPkgCoNtext \_ 系結**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="2407b-958">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="2407b-959">X</span><span class="sxs-lookup"><span data-stu-id="2407b-959">X</span></span> | <span data-ttu-id="2407b-960">X</span><span class="sxs-lookup"><span data-stu-id="2407b-960">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-961">WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 鏈 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="2407b-961">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="2407b-962">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="2407b-962">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="2407b-963">X</span><span class="sxs-lookup"><span data-stu-id="2407b-963">X</span></span> | <span data-ttu-id="2407b-964">X</span><span class="sxs-lookup"><span data-stu-id="2407b-964">X</span></span> | \- | <span data-ttu-id="2407b-965">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="2407b-965">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="2407b-966">WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="2407b-966">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="2407b-967">**憑證內容**</span><span class="sxs-lookup"><span data-stu-id="2407b-967">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="2407b-968">X</span><span class="sxs-lookup"><span data-stu-id="2407b-968">X</span></span> | <span data-ttu-id="2407b-969">X</span><span class="sxs-lookup"><span data-stu-id="2407b-969">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-970">已 \_ 使用 WINHTTP 選項 \_ 伺服器 \_ SPN \_</span><span class="sxs-lookup"><span data-stu-id="2407b-970">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="2407b-971">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-971">**LPWSTR**</span></span> | \- | <span data-ttu-id="2407b-972">X</span><span class="sxs-lookup"><span data-stu-id="2407b-972">X</span></span> | <span data-ttu-id="2407b-973">X</span><span class="sxs-lookup"><span data-stu-id="2407b-973">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-974">WINHTTP \_ 選項 \_ SPN</span><span class="sxs-lookup"><span data-stu-id="2407b-974">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="2407b-975">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-975">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-976">X</span><span class="sxs-lookup"><span data-stu-id="2407b-976">X</span></span> | \- | <span data-ttu-id="2407b-977">X</span><span class="sxs-lookup"><span data-stu-id="2407b-977">X</span></span> | \- |
| <span data-ttu-id="2407b-978">WINHTTP \_ 選項 \_ 資料流程 \_ 錯誤碼 \_</span><span class="sxs-lookup"><span data-stu-id="2407b-978">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="2407b-979">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-979">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-980">X</span><span class="sxs-lookup"><span data-stu-id="2407b-980">X</span></span> | <span data-ttu-id="2407b-981">X</span><span class="sxs-lookup"><span data-stu-id="2407b-981">X</span></span> | \- | <span data-ttu-id="2407b-982">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="2407b-982">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="2407b-983">WINHTTP \_ 選項 \_ TCP \_ 快速 \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="2407b-983">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="2407b-984">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-984">**BOOL**</span></span> | <span data-ttu-id="2407b-985">X</span><span class="sxs-lookup"><span data-stu-id="2407b-985">X</span></span> | \- | \- | <span data-ttu-id="2407b-986">X</span><span class="sxs-lookup"><span data-stu-id="2407b-986">X</span></span> | <span data-ttu-id="2407b-987">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="2407b-987">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="2407b-988">WINHTTP \_ 選項 \_ TCP \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="2407b-988">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="2407b-989">**tcp \_ keepalive**</span><span class="sxs-lookup"><span data-stu-id="2407b-989">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="2407b-990">X</span><span class="sxs-lookup"><span data-stu-id="2407b-990">X</span></span> | \- | \- | <span data-ttu-id="2407b-991">X</span><span class="sxs-lookup"><span data-stu-id="2407b-991">X</span></span> | <span data-ttu-id="2407b-992">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="2407b-992">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="2407b-993">WINHTTP \_ 選項 \_ TLS \_ FALSE \_ START</span><span class="sxs-lookup"><span data-stu-id="2407b-993">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="2407b-994">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-994">**BOOL**</span></span> | <span data-ttu-id="2407b-995">X</span><span class="sxs-lookup"><span data-stu-id="2407b-995">X</span></span> | \- | \- | <span data-ttu-id="2407b-996">X</span><span class="sxs-lookup"><span data-stu-id="2407b-996">X</span></span> | <span data-ttu-id="2407b-997">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="2407b-997">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="2407b-998">WINHTTP \_ 選項 \_ TLS \_ 通訊協定不 \_ 安全 \_ 的回復</span><span class="sxs-lookup"><span data-stu-id="2407b-998">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="2407b-999">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-999">**BOOL**</span></span> | <span data-ttu-id="2407b-1000">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1000">X</span></span> | \- | \- | <span data-ttu-id="2407b-1001">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1001">X</span></span> | <span data-ttu-id="2407b-1002">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="2407b-1002">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="2407b-1003">WINHTTP \_ 選項 \_ UNLOAD \_ 通知 \_ 事件</span><span class="sxs-lookup"><span data-stu-id="2407b-1003">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="2407b-1004">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="2407b-1004">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="2407b-1005">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1005">X</span></span> | \- | \- | <span data-ttu-id="2407b-1006">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1006">X</span></span> | \- |
| <span data-ttu-id="2407b-1007">WINHTTP \_ 選項 \_ UNSAFE \_ 標頭 \_ 剖析</span><span class="sxs-lookup"><span data-stu-id="2407b-1007">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="2407b-1008">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-1008">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-1009">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1009">X</span></span> | \- | <span data-ttu-id="2407b-1010">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1010">X</span></span> | \- |
| <span data-ttu-id="2407b-1011">WINHTTP \_ 選項 \_ 升級 \_ 至 \_ WEB \_ 通訊端</span><span class="sxs-lookup"><span data-stu-id="2407b-1011">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="2407b-1012">N/A</span><span class="sxs-lookup"><span data-stu-id="2407b-1012">N/A</span></span> | \- | <span data-ttu-id="2407b-1013">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1013">X</span></span> | \- | <span data-ttu-id="2407b-1014">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1014">X</span></span> | \- |
| <span data-ttu-id="2407b-1015">WINHTTP \_ 選項 \_ URL</span><span class="sxs-lookup"><span data-stu-id="2407b-1015">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="2407b-1016">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-1016">**LPWSTR**</span></span> | \- | <span data-ttu-id="2407b-1017">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1017">X</span></span> | <span data-ttu-id="2407b-1018">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1018">X</span></span> | \- | \- |
| <span data-ttu-id="2407b-1019">WINHTTP \_ 選項 \_ 使用 \_ 全域 \_ 伺服器 \_ 認證</span><span class="sxs-lookup"><span data-stu-id="2407b-1019">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="2407b-1020">**Bool**</span><span class="sxs-lookup"><span data-stu-id="2407b-1020">**BOOL**</span></span> | <span data-ttu-id="2407b-1021">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1021">X</span></span> | <span data-ttu-id="2407b-1022">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1022">X</span></span> | \- | <span data-ttu-id="2407b-1023">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1023">X</span></span> | \- |
| <span data-ttu-id="2407b-1024">WINHTTP \_ 選項 \_ 使用者 \_ 代理程式</span><span class="sxs-lookup"><span data-stu-id="2407b-1024">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="2407b-1025">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-1025">**LPWSTR**</span></span> | <span data-ttu-id="2407b-1026">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1026">X</span></span> | \- | <span data-ttu-id="2407b-1027">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1027">X</span></span> | <span data-ttu-id="2407b-1028">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1028">X</span></span> | \- |
| <span data-ttu-id="2407b-1029">WINHTTP \_ 選項使用者 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="2407b-1029">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="2407b-1030">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="2407b-1030">**LPWSTR**</span></span> | \- | <span data-ttu-id="2407b-1031">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1031">X</span></span> | <span data-ttu-id="2407b-1032">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1032">X</span></span> | <span data-ttu-id="2407b-1033">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1033">X</span></span> | \- |
| <span data-ttu-id="2407b-1034">WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 關閉 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="2407b-1034">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="2407b-1035">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-1035">**DWORD**</span></span> | \- | \- | <span data-ttu-id="2407b-1036">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1036">X</span></span> | <span data-ttu-id="2407b-1037">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1037">X</span></span> | \- |
| <span data-ttu-id="2407b-1038">WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ KEEPALIVE \_ 間隔</span><span class="sxs-lookup"><span data-stu-id="2407b-1038">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="2407b-1039">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-1039">**DWORD**</span></span> | \- | \- | <span data-ttu-id="2407b-1040">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1040">X</span></span> | <span data-ttu-id="2407b-1041">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1041">X</span></span> | \- |
| <span data-ttu-id="2407b-1042">WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 接收 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="2407b-1042">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="2407b-1043">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-1043">**DWORD**</span></span> | <span data-ttu-id="2407b-1044">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1044">X</span></span> | <span data-ttu-id="2407b-1045">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1045">X</span></span> | <span data-ttu-id="2407b-1046">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1046">X</span></span> | <span data-ttu-id="2407b-1047">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1047">X</span></span> | <span data-ttu-id="2407b-1048">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2407b-1048">Windows 8.1</span></span> |
| <span data-ttu-id="2407b-1049">WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 傳送 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="2407b-1049">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="2407b-1050">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-1050">**DWORD**</span></span> | <span data-ttu-id="2407b-1051">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1051">X</span></span> | <span data-ttu-id="2407b-1052">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1052">X</span></span> | <span data-ttu-id="2407b-1053">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1053">X</span></span> | <span data-ttu-id="2407b-1054">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1054">X</span></span> | <span data-ttu-id="2407b-1055">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2407b-1055">Windows 8.1</span></span> |
| <span data-ttu-id="2407b-1056">WINHTTP \_ 選項背景 \_ 工作 \_ 執行緒 \_ 計數</span><span class="sxs-lookup"><span data-stu-id="2407b-1056">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="2407b-1057">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-1057">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="2407b-1058">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1058">X</span></span> | \- |
| <span data-ttu-id="2407b-1059">WINHTTP \_ 選項 \_ 寫入 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="2407b-1059">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="2407b-1060">**Dword**</span><span class="sxs-lookup"><span data-stu-id="2407b-1060">**DWORD**</span></span> | \- | <span data-ttu-id="2407b-1061">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1061">X</span></span> | <span data-ttu-id="2407b-1062">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1062">X</span></span> | <span data-ttu-id="2407b-1063">X</span><span class="sxs-lookup"><span data-stu-id="2407b-1063">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="2407b-1064">針對 Windows XP 和 Windows 2000，請參閱 [執行時間需求](winhttp-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="2407b-1064">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2407b-1065">規格需求</span><span class="sxs-lookup"><span data-stu-id="2407b-1065">Requirements</span></span>

| <span data-ttu-id="2407b-1066">需求</span><span class="sxs-lookup"><span data-stu-id="2407b-1066">Requirement</span></span> | <span data-ttu-id="2407b-1067">值</span><span class="sxs-lookup"><span data-stu-id="2407b-1067">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2407b-1068">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2407b-1068">Minimum supported client</span></span> | <span data-ttu-id="2407b-1069">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2407b-1069">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="2407b-1070">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2407b-1070">Minimum supported server</span></span> | <span data-ttu-id="2407b-1071">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="2407b-1071">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="2407b-1072">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2407b-1072">Redistributable</span></span>          | <span data-ttu-id="2407b-1073">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="2407b-1073">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="2407b-1074">標頭</span><span class="sxs-lookup"><span data-stu-id="2407b-1074">Header</span></span>                   | <span data-ttu-id="2407b-1075">WinHTTP. h</span><span class="sxs-lookup"><span data-stu-id="2407b-1075">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="2407b-1076">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2407b-1076">See also</span></span>

[<span data-ttu-id="2407b-1077">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="2407b-1077">WinHTTP Versions</span></span>](winhttp-versions.md)
