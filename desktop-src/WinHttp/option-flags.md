---
Description: WinHttpQueryOption 和 WinHttpSetOption 支援下列選項旗標。
ms.assetid: 2d0441f4-ddba-4f2a-8861-8803cad6f1ac
title: '選項旗標 (WinHTTP. h) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 02/25/2020
ms.openlocfilehash: 91a9506225c53893990d4dcdc534293daa6c8e00
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262060"
---
# <a name="option-flags"></a><span data-ttu-id="7d023-103">選項旗標</span><span class="sxs-lookup"><span data-stu-id="7d023-103">Option Flags</span></span>

<span data-ttu-id="7d023-104">[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)和 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)支援下列選項旗標。</span><span class="sxs-lookup"><span data-stu-id="7d023-104">The following option flags are supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span>

<dl> <dt>

<span data-ttu-id="7d023-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP \_ 選項有 \_ 保證 \_ 非 \_ 封鎖 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="7d023-105"><span id="WINHTTP_OPTION_ASSURED_NON_BLOCKING_CALLBACKS"></span><span id="winhttp_option_assured_non_blocking_callbacks"></span>**WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-106">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="7d023-106">The default is FALSE.</span></span> <span data-ttu-id="7d023-107">如果設定為 TRUE，當用戶端應用程式封鎖狀態回呼時，WinHTTP 無法保證進度。</span><span class="sxs-lookup"><span data-stu-id="7d023-107">If set to TRUE, WinHTTP does not guarantee progress if status callbacks are blocked by the client application.</span></span>

<span data-ttu-id="7d023-108">用戶端應用程式必須特別小心地在回呼內執行最基本的作業，而不會封鎖、儘快傳回，而且特別不能等待任何後續的 WinHTTP 呼叫。</span><span class="sxs-lookup"><span data-stu-id="7d023-108">The client application must take special care to perform minimal operations within the callback without blocking, returning as quickly as possible, and in particular must not wait for any subsequent WinHTTP calls.</span></span> <span data-ttu-id="7d023-109">如果未遵循這些指導方針，可能會對效能造成負面影響，或可能應用程式停止回應。</span><span class="sxs-lookup"><span data-stu-id="7d023-109">If it does not follow these guidelines, there is likely to be a negative performance impact or a potential application hang.</span></span> <span data-ttu-id="7d023-110">如果以指定的方式使用，此選項可能會改善效能。</span><span class="sxs-lookup"><span data-stu-id="7d023-110">If used in the prescribed manner, this option may improve performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP \_ 選項 \_ 自動登入 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="7d023-111"><span id="WINHTTP_OPTION_AUTOLOGON_POLICY"></span><span id="winhttp_option_autologon_policy"></span>**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-112">設定不帶正負號的長整數值，指定具有下列其中一個值的 [自動登入原則](authentication-in-winhttp.md) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-112">Sets an unsigned long integer value that specifies the [Automatic Logon Policy](authentication-in-winhttp.md) with one of the following values.</span></span>

| <span data-ttu-id="7d023-113">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-113">Term</span></span> | <span data-ttu-id="7d023-114">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-114">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 高</span><span class="sxs-lookup"><span data-stu-id="7d023-115"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_HIGH"></span><span id="winhttp_autologon_security_level_high"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH</span></span> | <span data-ttu-id="7d023-116">未使用預設認證。</span><span class="sxs-lookup"><span data-stu-id="7d023-116">Default credentials are not used.</span></span> <span data-ttu-id="7d023-117">請注意，只有當您依實際的電腦名稱稱指定伺服器時，此旗標才會生效。</span><span class="sxs-lookup"><span data-stu-id="7d023-117">Note that this flag takes effect only if you specify the server by the actual machine name.</span></span> <span data-ttu-id="7d023-118">如果您將伺服器指定為 "localhost" 或 IP 位址，它將不會生效。</span><span class="sxs-lookup"><span data-stu-id="7d023-118">It will not take effect, if you specify the server by "localhost" or IP address.</span></span> |
| <span data-ttu-id="7d023-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 低</span><span class="sxs-lookup"><span data-stu-id="7d023-119"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_LOW"></span><span id="winhttp_autologon_security_level_low"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW</span></span> | <span data-ttu-id="7d023-120">系統會針對所有要求執行使用預設認證的已驗證登入。</span><span class="sxs-lookup"><span data-stu-id="7d023-120">An authenticated log on using the default credentials is performed for all requests.</span></span> |
| <span data-ttu-id="7d023-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP \_ 自動登入 \_ 安全性 \_ 等級 \_ 中</span><span class="sxs-lookup"><span data-stu-id="7d023-121"><span id="WINHTTP_AUTOLOGON_SECURITY_LEVEL_MEDIUM"></span><span id="winhttp_autologon_security_level_medium"></span>WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM</span></span> | <span data-ttu-id="7d023-122">使用預設認證的已驗證登入只會針對近端內部網路上的要求執行。</span><span class="sxs-lookup"><span data-stu-id="7d023-122">An authenticated log on using the default credentials is performed only for requests on the local Intranet.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7d023-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP \_ 選項 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="7d023-123"><span id="WINHTTP_OPTION_CALLBACK"></span><span id="winhttp_option_callback"></span>**WINHTTP\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-124">抓取以 [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)設定之回呼函數的指標。</span><span class="sxs-lookup"><span data-stu-id="7d023-124">Retrieves the pointer to the callback function set with [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="7d023-125"><span id="WINHTTP_OPTION_CLIENT_CERT_CONTEXT"></span><span id="winhttp_option_client_cert_context"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-126">設定用戶端憑證內容。</span><span class="sxs-lookup"><span data-stu-id="7d023-126">Sets the client certificate context.</span></span> <span data-ttu-id="7d023-127">如果應用程式收到 [**\_ \_ \_ \_ \_ 所需的錯誤 WINHTTP 用戶端驗證**](error-messages.md)憑證，則必須先呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 來提供憑證，再重試要求。</span><span class="sxs-lookup"><span data-stu-id="7d023-127">If an application receives [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md), it must call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="7d023-128">在處理此選項的過程中，WinHttp 會在呼叫端提供的憑證內容上呼叫 [**CertDuplicateCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) ，如此一來，呼叫端就可以獨立釋放憑證內容。</span><span class="sxs-lookup"><span data-stu-id="7d023-128">As a part of processing this option, WinHttp calls [**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) on the caller-provided certificate context so that the certificate context can be independently released by the caller.</span></span>

> [!Note]
> <span data-ttu-id="7d023-129">應用程式不應該嘗試 \_ \_ 在已從中抓取 \_ \_ 憑證內容的憑證存放區上呼叫 [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) 時，關閉憑證存放區的憑證關閉存放區強制旗標旗標。</span><span class="sxs-lookup"><span data-stu-id="7d023-129">The application should not attempt to close the certificate store with the CERT\_CLOSE\_STORE\_FORCE\_FLAG flag in the call to [**CertCloseStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore) on the certificate store from which the certificate context was retrieved.</span></span> <span data-ttu-id="7d023-130">可能會發生存取違規。</span><span class="sxs-lookup"><span data-stu-id="7d023-130">An access violation may occur.</span></span>

<span data-ttu-id="7d023-131">當伺服器要求用戶端憑證、 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)或 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 時，會傳回 [**錯誤 \_ WINHTTP \_ 用戶端 \_ 驗證憑證 \_ \_ 所需**](error-messages.md) 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d023-131">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an [**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**](error-messages.md) error.</span></span> <span data-ttu-id="7d023-132">如果伺服器要求憑證，但不需要憑證，則應用程式可以指定此選項來指出它沒有憑證。</span><span class="sxs-lookup"><span data-stu-id="7d023-132">If the server requests the certificate but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="7d023-133">伺服器可以選擇其他驗證配置，或允許匿名存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="7d023-133">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="7d023-134">應用程式會在 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)的 *lpBuffer* 參數中提供 **WINHTTP \_ NO \_ CLIENT \_ CERT \_ CONTEXT** 宏，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="7d023-134">The application provides the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption(hRequest,
                             WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                             WINHTTP_NO_CLIENT_CERT_CONTEXT,
                             0);
```

<span data-ttu-id="7d023-135">如果伺服器需要用戶端憑證，它可能會傳送 403 HTTP 狀態碼來回應。</span><span class="sxs-lookup"><span data-stu-id="7d023-135">If the server requires a client certificate, it may send a 403 HTTP status code in response.</span></span> <span data-ttu-id="7d023-136">如需詳細資訊，請參閱 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單** 選項。</span><span class="sxs-lookup"><span data-stu-id="7d023-136">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="7d023-137"><span id="WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST"></span><span id="winhttp_option_client_cert_issuer_list"></span>**WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-138">當 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)或 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)的錯誤是 **\_ \_ \_ \_ \_ 需要的 WINHTTP 用戶端驗證憑證錯誤** 時，會抓取 [**SecPkgCoNtext \_ IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex)結構。</span><span class="sxs-lookup"><span data-stu-id="7d023-138">Retrieves a [**SecPkgContext\_IssuerListInfoEx**](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure when the error from [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) is **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="7d023-139">結構中的簽發者清單包含伺服器 (CA) 可接受的憑證授權單位單位清單。</span><span class="sxs-lookup"><span data-stu-id="7d023-139">The issuer list in the structure contains a list of acceptable Certificate Authorities (CA) from the server.</span></span> <span data-ttu-id="7d023-140">用戶端應用程式可以篩選 CA 清單，以取得 SSL 驗證的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="7d023-140">The client application can filter the CA list to retrieve the client certificate for SSL authentication.</span></span>

<span data-ttu-id="7d023-141">或者，如果伺服器要求用戶端憑證，但不需要它，則應用程式可以使用 **WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容** 選項來呼叫 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-141">Alternately, if the server requests the client certificate, but does not require it, the application can call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="7d023-142">如需詳細資訊，請參閱 **WINHTTP \_ option \_ CLIENT \_ CERT \_ CONTEXT** 選項。</span><span class="sxs-lookup"><span data-stu-id="7d023-142">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP \_ 選項 \_ 字碼頁**</span><span class="sxs-lookup"><span data-stu-id="7d023-143"><span id="WINHTTP_OPTION_CODEPAGE"></span><span id="winhttp_option_codepage"></span>**WINHTTP\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-144">設定用來處理 URL (也就是查詢字串) 的 [*字碼頁*](glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-144">Sets the [*code page*](glossary.md) that is used to process the URL (that is, query string).</span></span> <span data-ttu-id="7d023-145">預設值為 UTF8。</span><span class="sxs-lookup"><span data-stu-id="7d023-145">The default is UTF8.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP \_ 選項 \_ 設定 \_ PASSPORT \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="7d023-146"><span id="WINHTTP_OPTION_CONFIGURE_PASSPORT_AUTH"></span><span id="winhttp_option_configure_passport_auth"></span>**WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-147">設定不帶正負號的長整數值，這個值會指定是否啟用 [WinHTTP 驗證中的 Passport 驗證](passport-authentication-in-winhttp.md) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-147">Sets an unsigned long integer value that specifies whether [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md) authentication is enabled.</span></span> <span data-ttu-id="7d023-148">這個值可以是下列值之一：</span><span class="sxs-lookup"><span data-stu-id="7d023-148">The value can be one of the following:</span></span>

| <span data-ttu-id="7d023-149">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-149">Term</span></span> | <span data-ttu-id="7d023-150">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-150">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP \_ 停用 \_ PASSPORT \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="7d023-151"><span id="WINHTTP_DISABLE_PASSPORT_AUTH"></span><span id="winhttp_disable_passport_auth"></span>WINHTTP\_DISABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="7d023-152">Microsoft Passport 驗證已停用。</span><span class="sxs-lookup"><span data-stu-id="7d023-152">Microsoft Passport authentication is disabled.</span></span> <span data-ttu-id="7d023-153">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="7d023-153">This is the default.</span></span> |
| <span data-ttu-id="7d023-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP \_ 停用 \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="7d023-154"><span id="WINHTTP_DISABLE_PASSPORT_KEYRING"></span><span id="winhttp_disable_passport_keyring"></span>WINHTTP\_DISABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="7d023-155">Passport keyring 已停用。</span><span class="sxs-lookup"><span data-stu-id="7d023-155">The Passport keyring is disabled.</span></span> <span data-ttu-id="7d023-156">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="7d023-156">This is the default.</span></span> |
| <span data-ttu-id="7d023-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP \_ 啟用 \_ PASSPORT \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="7d023-157"><span id="WINHTTP_ENABLE_PASSPORT_AUTH"></span><span id="winhttp_enable_passport_auth"></span>WINHTTP\_ENABLE\_PASSPORT\_AUTH</span></span> | <span data-ttu-id="7d023-158">Passport 驗證已啟用。</span><span class="sxs-lookup"><span data-stu-id="7d023-158">Passport authentication is enabled.</span></span> |
| <span data-ttu-id="7d023-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP \_ 啟用 \_ PASSPORT \_ KEYRING</span><span class="sxs-lookup"><span data-stu-id="7d023-159"><span id="WINHTTP_ENABLE_PASSPORT_KEYRING"></span><span id="winhttp_enable_passport_keyring"></span>WINHTTP\_ENABLE\_PASSPORT\_KEYRING</span></span> | <span data-ttu-id="7d023-160">Passport keyring 已啟用。</span><span class="sxs-lookup"><span data-stu-id="7d023-160">The Passport keyring is enabled.</span></span> |

</dl> </dd> <dt>

<span data-ttu-id="7d023-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP \_ 選項 \_ 連接 \_ 重試**</span><span class="sxs-lookup"><span data-stu-id="7d023-161"><span id="WINHTTP_OPTION_CONNECT_RETRIES"></span><span id="winhttp_option_connect_retries"></span>**WINHTTP\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-162">設定或抓取不帶正負號的長整數值，其中包含連接到主機的 timesWinHTTP 嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="7d023-162">Sets or retrieves an unsigned long integer value that contains the number of timesWinHTTP attempts to connect to a host.</span></span> <span data-ttu-id="7d023-163">Microsoft Windows HTTP Services (WinHTTP) 只會在每個網際網路通訊協定 (IP) 位址嘗試一次。</span><span class="sxs-lookup"><span data-stu-id="7d023-163">Microsoft Windows HTTP Services (WinHTTP) only attempts once per Internet Protocol (IP) address.</span></span> <span data-ttu-id="7d023-164">例如，如果您嘗試連線到有10個 IP 位址的多重主目錄主機，而 **winHTTP \_ 選項連線 \_ \_ 重試** 設定為7，則 winHTTP 只會嘗試連線到前七個 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="7d023-164">For example, if you attempt to connect to a multihomed host that has 10 IP addresses and **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 7, then WinHTTP only attempts to connect to the first seven IP address.</span></span> <span data-ttu-id="7d023-165">假設有一組相同的10個 IP 位址，則當 **winHTTP \_ 選項 \_ 連接 \_ 重試** 設定為20時，winHTTP 只會嘗試10次。</span><span class="sxs-lookup"><span data-stu-id="7d023-165">Given the same set of 10 IP addresses, if **WINHTTP\_OPTION\_CONNECT\_RETRIES** is set to 20, WinHTTP attempts each of the 10 only once.</span></span> <span data-ttu-id="7d023-166">如果連接嘗試在指定的嘗試次數之後仍失敗，或連接逾時之前已過期，則會取消要求。</span><span class="sxs-lookup"><span data-stu-id="7d023-166">If a connection attempt still fails after the specified number of attempts, or if the connect timeout expired before then, the request is canceled.</span></span> <span data-ttu-id="7d023-167">**WINHTTP \_ 選項 \_ 連接 \_ 重試** 的預設值為五次嘗試。</span><span class="sxs-lookup"><span data-stu-id="7d023-167">The default value for **WINHTTP\_OPTION\_CONNECT\_RETRIES** is five attempts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP \_ 選項 \_ 連接 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="7d023-168"><span id="WINHTTP_OPTION_CONNECT_TIMEOUT"></span><span id="winhttp_option_connect_timeout"></span>**WINHTTP\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-169">設定或抓取不帶正負號的長整數值，其中包含超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d023-169">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds.</span></span> <span data-ttu-id="7d023-170">將此選項設定為無限 (0xFFFFFFFF) 將會停用此計時器。</span><span class="sxs-lookup"><span data-stu-id="7d023-170">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="7d023-171">如果 TCP 連線要求所花費的時間超過這個超時值，就會取消要求。</span><span class="sxs-lookup"><span data-stu-id="7d023-171">If a TCP connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="7d023-172">預設的超時時間為60秒。</span><span class="sxs-lookup"><span data-stu-id="7d023-172">The default timeout is 60 seconds.</span></span> <span data-ttu-id="7d023-173">當您嘗試連線到單一主機 (多個 IP 位址時，) 的多重主控制項，則會有每個個別連接的時間限制。</span><span class="sxs-lookup"><span data-stu-id="7d023-173">When you are attempting to connect to multiple IP addresses for a single host (a multihomed host), the timeout limit is for each individual connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP \_ 選項 \_ 連接 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="7d023-174"><span id="WINHTTP_OPTION_CONNECTION_INFO"></span><span id="winhttp_option_connection_info"></span>**WINHTTP\_OPTION\_CONNECTION\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-175">抓取 [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) 傳回時產生回應之要求的來源和目的地 IP 位址和埠。</span><span class="sxs-lookup"><span data-stu-id="7d023-175">Retrieves the source and destination IP address, and port of the request that generated the response when [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns.</span></span> <span data-ttu-id="7d023-176">應用程式會使用 **WINHTTP \_ 選項 \_ 連接 \_ 資訊** 選項來呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) ，並在 *lpBuffer* 參數中提供 [**winHTTP \_ 連接 \_ 資訊**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)結構。</span><span class="sxs-lookup"><span data-stu-id="7d023-176">The application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CONNECTION\_INFO** option, and provides the [**WINHTTP\_CONNECTION\_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) structure in the *lpBuffer* parameter.</span></span> <span data-ttu-id="7d023-177">如需詳細資訊，請參閱 **WINHTTP \_ 連接 \_ 資訊**。</span><span class="sxs-lookup"><span data-stu-id="7d023-177">For more information, see **WINHTTP\_CONNECTION\_INFO**.</span></span>

<span data-ttu-id="7d023-178">**Windows Server 2003 SP1 和 WINDOWS XP 含 SP2：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7d023-178">**Windows Server 2003 with SP1 and Windows XP with SP2:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V0**</span><span class="sxs-lookup"><span data-stu-id="7d023-179"><span id="WINHTTP_OPTION_CONNECTION_STATS_V0"></span><span id="winhttp_option_connection_stats_v0"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V0**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-180">針對要求所使用的基礎連接，擷取 [**TCP \_ 資訊 \_ v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) 結構。</span><span class="sxs-lookup"><span data-stu-id="7d023-180">Retreives the [**TCP\_INFO\_v0**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="7d023-181">傳回的結構可能包含透過相同連接傳送的先前要求的統計資料。</span><span class="sxs-lookup"><span data-stu-id="7d023-181">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>

> [!Note]
> <span data-ttu-id="7d023-182">**WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V1** 已取代此選項。</span><span class="sxs-lookup"><span data-stu-id="7d023-182">This option has been superseded by **WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V1**</span><span class="sxs-lookup"><span data-stu-id="7d023-183"><span id="WINHTTP_OPTION_CONNECTION_STATS_V1"></span><span id="winhttp_option_connection_stats_v1"></span>**WINHTTP\_OPTION\_CONNECTION\_STATS\_V1**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-184">擷取要求所使用之基礎連接的 [**TCP \_ INFO \_ v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) 結構。</span><span class="sxs-lookup"><span data-stu-id="7d023-184">Retreives the [**TCP\_INFO\_v1**](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) struct for the underlying connection used by the request.</span></span> <span data-ttu-id="7d023-185">傳回的結構可能包含透過相同連接傳送的先前要求的統計資料。</span><span class="sxs-lookup"><span data-stu-id="7d023-185">The returned struct may contain statistics from prior requests sent over the same connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP \_ 選項 \_ 內容 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="7d023-186"><span id="WINHTTP_OPTION_CONTEXT_VALUE"></span><span id="winhttp_option_context_value"></span>**WINHTTP\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-187">設定或抓取 DWORD 指標，其中包含與這個 [HINTERNET](hinternet-handles-in-winhttp.md)控制碼相關聯之內容值的指標。 **\_**</span><span class="sxs-lookup"><span data-stu-id="7d023-187">Sets or retrieves a **DWORD\_PTR** that contains a pointer to the context value associated with this [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span> <span data-ttu-id="7d023-188">使用儲存在緩衝區中的值，並為 **WINHTTP \_ 選項 \_ 內容 \_ 值** 選項旗標指派新值。</span><span class="sxs-lookup"><span data-stu-id="7d023-188">The value stored in the buffer is used and the **WINHTTP\_OPTION\_CONTEXT\_VALUE** option flag is assigned a new value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP \_ 選項 \_ 解壓縮**</span><span class="sxs-lookup"><span data-stu-id="7d023-189"><span id="WINHTTP_OPTION_DECOMPRESSION"></span><span id="winhttp_option_decompression"></span>**WINHTTP\_OPTION\_DECOMPRESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-190">設定旗標的 DWORD，以判斷 WinHTTP 是否會自動以壓縮的內容編碼方式解壓縮回應主體。</span><span class="sxs-lookup"><span data-stu-id="7d023-190">Sets a DWORD of flags which determine whether WinHTTP will automatically decompress response bodies with compressed Content-Encodings.</span></span> <span data-ttu-id="7d023-191">WinHTTP 也會設定適當的 Accept-Encoding 標頭，覆寫呼叫端所提供的任何一個。</span><span class="sxs-lookup"><span data-stu-id="7d023-191">WinHTTP will also set an appropriate Accept-Encoding header, overriding any supplied by the caller.</span></span> <span data-ttu-id="7d023-192">支援的值為：</span><span class="sxs-lookup"><span data-stu-id="7d023-192">Supported values are:</span></span>

| <span data-ttu-id="7d023-193">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-193">Term</span></span> | <span data-ttu-id="7d023-194">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-194">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP \_ 解壓縮 \_ 旗標 \_ GZIP</span><span class="sxs-lookup"><span data-stu-id="7d023-195"><span id="WINHTTP_DECOMPRESSION_FLAG_GZIP"></span><span id="winhttp_decompression_flag_gzip"></span>WINHTTP\_DECOMPRESSION\_FLAG\_GZIP</span></span> | <span data-ttu-id="7d023-196">解壓縮內容編碼： gzip 回應。</span><span class="sxs-lookup"><span data-stu-id="7d023-196">Decompress Content-Encoding: gzip responses.</span></span> |
| <span data-ttu-id="7d023-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP \_ 解壓縮 \_ 旗標 \_ DEFLATE</span><span class="sxs-lookup"><span data-stu-id="7d023-197"><span id="WINHTTP_DECOMPRESSION_FLAG_DEFLATE"></span><span id="winhttp_decompression_flag_deflate"></span>WINHTTP\_DECOMPRESSION\_FLAG\_DEFLATE</span></span> | <span data-ttu-id="7d023-198">解壓縮內容編碼： deflate 回應。</span><span class="sxs-lookup"><span data-stu-id="7d023-198">Decompress Content-Encoding: deflate responses.</span></span> |
| <span data-ttu-id="7d023-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP \_ 解壓縮 \_ 旗標 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="7d023-199"><span id="WINHTTP_DECOMPRESSION_FLAG_ALL"></span><span id="winhttp_decompression_flag_all"></span>WINHTTP\_DECOMPRESSION\_FLAG\_ALL</span></span> | <span data-ttu-id="7d023-200">使用任何支援的內容編碼來將回應解壓縮。</span><span class="sxs-lookup"><span data-stu-id="7d023-200">Decompress responses with any supported Content-Encoding.</span></span> |

<span data-ttu-id="7d023-201">根據預設，WinHTTP 會將壓縮的回應傳遞給未修改的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="7d023-201">By default, WinHTTP will deliver compressed responses to the caller unmodified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP \_ 選項 \_ 停用 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="7d023-202"><span id="WINHTTP_OPTION_DISABLE_FEATURE"></span><span id="winhttp_option_disable_feature"></span>**WINHTTP\_OPTION\_DISABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-203">設定不帶正負號的長整數值，指定使用下列其中一個或多個旗標停用的功能。</span><span class="sxs-lookup"><span data-stu-id="7d023-203">Sets an unsigned long integer value that specifies which features are disabled with one or more of the following flags.</span></span> <span data-ttu-id="7d023-204">請注意，只有在使用 [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)建立要求控制碼之後，以及使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)傳送要求之前，才應將這項功能傳遞至要求控制碼上的 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-204">Be aware that this feature should only be passed to [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) on request handles after the request handle is created with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), and before the request is sent with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

| <span data-ttu-id="7d023-205">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-205">Term</span></span> | <span data-ttu-id="7d023-206">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-206">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP \_ 停用 \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="7d023-207"><span id="WINHTTP_DISABLE_AUTHENTICATION"></span><span id="winhttp_disable_authentication"></span>WINHTTP\_DISABLE\_AUTHENTICATION</span></span> | <span data-ttu-id="7d023-208">自動驗證已停用。</span><span class="sxs-lookup"><span data-stu-id="7d023-208">Automatic authentication is disabled.</span></span> |
| <span data-ttu-id="7d023-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP \_ 停用 \_ COOKIE</span><span class="sxs-lookup"><span data-stu-id="7d023-209"><span id="WINHTTP_DISABLE_COOKIES"></span><span id="winhttp_disable_cookies"></span>WINHTTP\_DISABLE\_COOKIES</span></span> | <span data-ttu-id="7d023-210">已停用自動將 cookie 標頭新增至要求的功能。</span><span class="sxs-lookup"><span data-stu-id="7d023-210">Automatic addition of cookie headers to requests is disabled.</span></span> <span data-ttu-id="7d023-211">此外，傳回的 cookie 也不會自動新增至 cookie 資料庫。</span><span class="sxs-lookup"><span data-stu-id="7d023-211">Also, returned cookies are not automatically added to the cookie database.</span></span> <span data-ttu-id="7d023-212">停用 cookie 可能會導致 Passport 驗證效能不佳。</span><span class="sxs-lookup"><span data-stu-id="7d023-212">Disabling cookies can result in poor performance for Passport authentication.</span></span> |
| <span data-ttu-id="7d023-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP \_ 停用 \_ 保持運作 \_ 狀態</span><span class="sxs-lookup"><span data-stu-id="7d023-213"><span id="WINHTTP_DISABLE_KEEP_ALIVE"></span><span id="winhttp_disable_keep_alive"></span>WINHTTP\_DISABLE\_KEEP\_ALIVE</span></span> | <span data-ttu-id="7d023-214">停用連接的 keep-alive 語義。</span><span class="sxs-lookup"><span data-stu-id="7d023-214">Disables keep-alive semantics for the connection.</span></span> <span data-ttu-id="7d023-215">MSN、NTLM 和其他類型的驗證都需要 keep-alive 語義。</span><span class="sxs-lookup"><span data-stu-id="7d023-215">Keep-alive semantics are required for MSN, NTLM, and other types of authentication.</span></span> |
| <span data-ttu-id="7d023-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP \_ 停用重新 \_ 導向</span><span class="sxs-lookup"><span data-stu-id="7d023-216"><span id="WINHTTP_DISABLE_REDIRECTS"></span><span id="winhttp_disable_redirects"></span>WINHTTP\_DISABLE\_REDIRECTS</span></span> | <span data-ttu-id="7d023-217">使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)傳送要求時，自動重新導向已停用。</span><span class="sxs-lookup"><span data-stu-id="7d023-217">Automatic redirection is disabled when sending requests with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="7d023-218">如果自動重新導向已停用，應用程式必須註冊回呼函式，Passport 驗證才會成功。</span><span class="sxs-lookup"><span data-stu-id="7d023-218">If automatic redirection is disabled, an application must register a callback function in order for Passport authentication to succeed.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7d023-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP \_ 選項 \_ 停用 \_ 安全 \_ 通訊協定 \_ 回復**</span><span class="sxs-lookup"><span data-stu-id="7d023-219"><span id="WINHTTP_OPTION_DISABLE_SECURE_PROTOCOL_FALLBACK"></span><span id="winhttp_option_disable_secure_protocol_fallback"></span>**WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-220">當初始通訊協定協商失敗時，防止 WinHTTP 使用較低版本的安全性通訊協定來重試連接。</span><span class="sxs-lookup"><span data-stu-id="7d023-220">Prevents WinHTTP from retrying a connection with a lower version of the security protocol when the initial protocol negotiation fails.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP \_ 選項 \_ 停用 \_ 串流 \_ 佇列**</span><span class="sxs-lookup"><span data-stu-id="7d023-221"><span id="WINHTTP_OPTION_DISABLE_STREAM_QUEUE"></span><span id="winhttp_option_disable_stream_queue"></span>**WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-222">允許新的要求在達到最大並行串流限制時開啟額外的 HTTP/2 連接，而不是在現有的連接上等候下一個可用的資料流程。</span><span class="sxs-lookup"><span data-stu-id="7d023-222">Allows new requests to open an additional HTTP/2 connection when the maximum concurrent stream limit is reached, rather than waiting for the next available stream on an existing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP \_ 選項 \_ 啟用 \_ 功能**</span><span class="sxs-lookup"><span data-stu-id="7d023-223"><span id="WINHTTP_OPTION_ENABLE_FEATURE"></span><span id="winhttp_option_enable_feature"></span>**WINHTTP\_OPTION\_ENABLE\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-224">設定不帶正負號的長整數值，指定目前已啟用的功能。</span><span class="sxs-lookup"><span data-stu-id="7d023-224">Sets an unsigned long integer value that specifies the features currently enabled.</span></span> <span data-ttu-id="7d023-225">可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7d023-225">Can be one of the following values.</span></span>

| <span data-ttu-id="7d023-226">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-226">Term</span></span> | <span data-ttu-id="7d023-227">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-227">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP \_ 啟用 \_ SSL \_ 還原 \_ 模擬</span><span class="sxs-lookup"><span data-stu-id="7d023-228"><span id="WINHTTP_ENABLE_SSL_REVERT_IMPERSONATION"></span><span id="winhttp_enable_ssl_revert_impersonation"></span>WINHTTP\_ENABLE\_SSL\_REVERT\_IMPERSONATION</span></span> | <span data-ttu-id="7d023-229">如果啟用，WinHTTP 會暫時還原 SSL 憑證驗證作業期間的用戶端模擬。</span><span class="sxs-lookup"><span data-stu-id="7d023-229">If enabled, WinHTTP temporarily reverts client impersonation for the duration of SSL certificate authentication operations.</span></span> <span data-ttu-id="7d023-230">此值只能在會話控制碼上進行設定。</span><span class="sxs-lookup"><span data-stu-id="7d023-230">This value can be set only on the session handle.</span></span> |
| <span data-ttu-id="7d023-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP \_ 啟用 \_ SSL \_ 撤銷</span><span class="sxs-lookup"><span data-stu-id="7d023-231"><span id="WINHTTP_ENABLE_SSL_REVOCATION"></span><span id="winhttp_enable_ssl_revocation"></span>WINHTTP\_ENABLE\_SSL\_REVOCATION</span></span> | <span data-ttu-id="7d023-232">啟用時，WinHTTP 允許 SSL 撤銷。</span><span class="sxs-lookup"><span data-stu-id="7d023-232">If enabled, WinHTTP allows SSL revocation.</span></span> <span data-ttu-id="7d023-233">此值只能在要求控制碼上進行設定。</span><span class="sxs-lookup"><span data-stu-id="7d023-233">This value can be set only on the request handle.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP \_ 選項 \_ 啟用 \_ HTTP \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="7d023-234"><span id="WINHTTP_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="winhttp_option_enable_http_protocol"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-235">設定可接受之 advanced HTTP 版本的 DWORD 位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="7d023-235">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="7d023-236">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="7d023-236">Possible values are:</span></span>

| <span data-ttu-id="7d023-237">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-237">Term</span></span> | <span data-ttu-id="7d023-238">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-238">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP \_ 通訊協定 \_ 旗標 \_ HTTP2 (0x1) </span><span class="sxs-lookup"><span data-stu-id="7d023-239"><span id="WINHTTP_PROTOCOL_FLAG_HTTP2"></span><span id="winhttp_protocol_flag_http2"></span>WINHTTP\_PROTOCOL\_FLAG\_HTTP2 (0x1)</span></span> | <span data-ttu-id="7d023-240">針對要求啟用 HTTP/2。</span><span class="sxs-lookup"><span data-stu-id="7d023-240">Enables HTTP/2 for the request.</span></span> |
| <span data-ttu-id="7d023-241">無 (0x0) </span><span class="sxs-lookup"><span data-stu-id="7d023-241">None (0x0)</span></span> | <span data-ttu-id="7d023-242">將要求限制為 HTTP/1.1 及更早的版本。</span><span class="sxs-lookup"><span data-stu-id="7d023-242">Restricts the request to HTTP/1.1 and prior.</span></span> |

<span data-ttu-id="7d023-243">舊版的 HTTP (1.1 和先前的) 無法使用這個選項停用。</span><span class="sxs-lookup"><span data-stu-id="7d023-243">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="7d023-244">預設值為0x0。</span><span class="sxs-lookup"><span data-stu-id="7d023-244">The default is 0x0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-245"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP \_ 選項 \_ ENABLE \_ HTTP2 \_ PLUS \_ CLIENT \_ CERT**</span><span class="sxs-lookup"><span data-stu-id="7d023-245"><span id="WINHTTP_OPTION_ENABLE_HTTP2_PLUS_CLIENT_CERT"></span><span id="winhttp_option_enable_http2_plus_client_cert"></span>**WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7d023-246">您可以在 WinHttp 會話控制碼上設定這個選項，讓 WinHttp 在使用 HTTP/2 時，使用呼叫端提供的用戶端憑證內容。</span><span class="sxs-lookup"><span data-stu-id="7d023-246">This option can be set on a WinHttp session handle to allow WinHttp to use the caller-provided client certificate context when HTTP/2 is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-247"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP \_ 選項 \_ ENABLETRACING**</span><span class="sxs-lookup"><span data-stu-id="7d023-247"><span id="WINHTTP_OPTION_ENABLETRACING"></span><span id="winhttp_option_enabletracing"></span>**WINHTTP\_OPTION\_ENABLETRACING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-248">設定 **布林** 值，這個值會指定目前是否已啟用追蹤。</span><span class="sxs-lookup"><span data-stu-id="7d023-248">Sets a **BOOL** value that specifies whether tracing is currently enabled.</span></span> <span data-ttu-id="7d023-249">如需 WinHTTP 中追蹤設備的詳細資訊，請參閱 [WinHTTP 追蹤設備](winhttptracecfg-exe--a-trace-configuration-tool.md)。</span><span class="sxs-lookup"><span data-stu-id="7d023-249">For more information about the trace facility in WinHTTP, see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span> <span data-ttu-id="7d023-250">此選項只能在 **Null** **HINTERNET** 控制碼上進行設定。</span><span class="sxs-lookup"><span data-stu-id="7d023-250">This option can only be set on a **NULL** **HINTERNET** handle.</span></span>


</dt> </dl> </dd>

<dt>

<span data-ttu-id="7d023-251"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP \_ 選項 \_ 編碼 \_ 額外**</span><span class="sxs-lookup"><span data-stu-id="7d023-251"><span id="WINHTTP_OPTION_ENCODE_EXTRA"></span><span id="winhttp_option_encode_extra"></span>**WINHTTP\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-252">啟用路徑和查詢字串的 URL 百分比編碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-252">Enables URL percent encoding for path and query string.</span></span>

<span data-ttu-id="7d023-253">或者，您可以在呼叫 WinHttp 之前對編碼百分比進行編碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-253">Alternatively, you can percent encode before calling WinHttp.</span></span>

</dt> </dl> </dd>

<dt>

<span data-ttu-id="7d023-254"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP \_ 選項 \_ 到期 \_ 連接**</span><span class="sxs-lookup"><span data-stu-id="7d023-254"><span id="WINHTTP_OPTION_EXPIRE_CONNECTION"></span><span id="winhttp_option_expire_connection"></span>**WINHTTP\_OPTION\_EXPIRE\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-255">此選項只能在要求控制碼上設定，而該控制碼仍在使用中 (傳送或接收) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-255">This option can only be set on a request handle which is still active (sending or receiving).</span></span> <span data-ttu-id="7d023-256">設定此選項會告知 WinHttp 在與傳入的要求控制碼相關聯的連接上停止服務要求。</span><span class="sxs-lookup"><span data-stu-id="7d023-256">Setting this option will tell WinHttp to stop serving requests on the connection associated with the request handle passed in.</span></span> <span data-ttu-id="7d023-257">當要求控制碼完成時，將會關閉此連接。</span><span class="sxs-lookup"><span data-stu-id="7d023-257">The connection will be closed after the request handle this option is called with is completed.</span></span> <span data-ttu-id="7d023-258">此選項不會使用任何參數。</span><span class="sxs-lookup"><span data-stu-id="7d023-258">This option does not take any parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-259"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP \_ 選項 \_ 延伸 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="7d023-259"><span id="WINHTTP_OPTION_EXTENDED_ERROR"></span><span id="winhttp_option_extended_error"></span>**WINHTTP\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-260">抓取不帶正負號的長整數值，其中包含 Microsoft Windows 通訊端錯誤碼，該錯誤碼已對應到 \_ \_ \* 此執行緒內容中最後傳回的錯誤 WINHTTP 錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="7d023-260">Retrieves an unsigned long integer value that contains a Microsoft Windows Sockets error code that was mapped to the ERROR\_WINHTTP\_\* error messages last returned in this thread context.</span></span> <span data-ttu-id="7d023-261">您可以傳遞 **Null** 做為控制碼值。</span><span class="sxs-lookup"><span data-stu-id="7d023-261">You can pass **NULL** as the handle value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-262"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP \_ 選項 \_ 全域 \_ PROXY \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="7d023-262"><span id="WINHTTP_OPTION_GLOBAL_PROXY_CREDS"></span><span id="winhttp_option_global_proxy_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-263">將 *hInternet* 函式參數設定為 **Null** 的 [**WINHTTP 認證 \_ \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7d023-263">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="7d023-264">此選項需要登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings！ShareCredsWithWinHttp**。</span><span class="sxs-lookup"><span data-stu-id="7d023-264">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="7d023-265">如果未設定此登錄機碼，WinHTTP 將會傳回錯誤： **\_ winHTTP \_ 無效 \_ 選項** 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d023-265">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="7d023-266">依預設，此登錄機碼不存在。</span><span class="sxs-lookup"><span data-stu-id="7d023-266">This registry key is not present by default.</span></span> <span data-ttu-id="7d023-267">當設定時，WinINet 會將認證傳送至 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="7d023-267">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="7d023-268">每當 WinHttp 收到驗證挑戰，而且目前的控制碼上沒有設定任何認證時，就會使用 WinINet 提供的認證。</span><span class="sxs-lookup"><span data-stu-id="7d023-268">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="7d023-269">為了共用 proxy 認證以外的伺服器認證，使用者必須設定 **WINHTTP \_ 選項 [ \_ 使用 \_ 全域 \_ 伺服器 \_ 認證** ]。</span><span class="sxs-lookup"><span data-stu-id="7d023-269">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-270"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP \_ 選項 \_ 全域 \_ 伺服器 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="7d023-270"><span id="WINHTTP_OPTION_GLOBAL_SERVER_CREDS"></span><span id="winhttp_option_global_server_creds"></span>**WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-271">將 *hInternet* 函式參數設定為 **Null** 的 [**WINHTTP 認證 \_ \_ EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7d023-271">Takes a pointer to a [**WINHTTP\_CREDS\_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) structure with the *hInternet* function parameter set to **NULL**.</span></span> <span data-ttu-id="7d023-272">此選項需要登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings！ShareCredsWithWinHttp**。</span><span class="sxs-lookup"><span data-stu-id="7d023-272">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="7d023-273">如果未設定此登錄機碼，WinHTTP 將會傳回錯誤： **\_ winHTTP \_ 無效 \_ 選項** 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d023-273">If this registry key is not set WinHTTP will return error **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span> <span data-ttu-id="7d023-274">依預設，此登錄機碼不存在。</span><span class="sxs-lookup"><span data-stu-id="7d023-274">This registry key is not present by default.</span></span> <span data-ttu-id="7d023-275">當設定時，WinINet 會將認證傳送至 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="7d023-275">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="7d023-276">每當 WinHttp 收到驗證挑戰，而且目前的控制碼上沒有設定任何認證時，就會使用 WinINet 提供的認證。</span><span class="sxs-lookup"><span data-stu-id="7d023-276">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span> <span data-ttu-id="7d023-277">為了共用 proxy 認證以外的伺服器認證，使用者必須設定 **WINHTTP \_ 選項 [ \_ 使用 \_ 全域 \_ 伺服器 \_ 認證** ]。</span><span class="sxs-lookup"><span data-stu-id="7d023-277">In order to share server credentials in addition to proxy credentials, users needs to set **WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS** .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-278"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP \_ 選項 \_ 控制碼 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="7d023-278"><span id="WINHTTP_OPTION_HANDLE_TYPE"></span><span id="winhttp_option_handle_type"></span>**WINHTTP\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-279">抓取不帶正負號的長整數值，其中包含傳入的 [HINTERNET](hinternet-handles-in-winhttp.md) 控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="7d023-279">Retrieves an unsigned long integer value that contains the type of the [HINTERNET](hinternet-handles-in-winhttp.md) handle passed in.</span></span> <span data-ttu-id="7d023-280">傳回值可以是下列其中一個：</span><span class="sxs-lookup"><span data-stu-id="7d023-280">The return value can be one of the following:</span></span>

| <span data-ttu-id="7d023-281">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-281">Term</span></span> | <span data-ttu-id="7d023-282">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-282">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-283"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP \_ 控制碼 \_ 類型 \_ 連接</span><span class="sxs-lookup"><span data-stu-id="7d023-283"><span id="WINHTTP_HANDLE_TYPE_CONNECT"></span><span id="winhttp_handle_type_connect"></span>WINHTTP\_HANDLE\_TYPE\_CONNECT</span></span> | <span data-ttu-id="7d023-284">控制碼是連接控制碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-284">The handle is a connection handle.</span></span> |
| <span data-ttu-id="7d023-285"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP \_ 控制碼 \_ 類型 \_ 要求</span><span class="sxs-lookup"><span data-stu-id="7d023-285"><span id="WINHTTP_HANDLE_TYPE_REQUEST"></span><span id="winhttp_handle_type_request"></span>WINHTTP\_HANDLE\_TYPE\_REQUEST</span></span> | <span data-ttu-id="7d023-286">控制碼是要求控制碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-286">The handle is a request handle.</span></span> |
| <span data-ttu-id="7d023-287"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP \_ 控制碼 \_ 類型 \_ 會話</span><span class="sxs-lookup"><span data-stu-id="7d023-287"><span id="WINHTTP_HANDLE_TYPE_SESSION"></span><span id="winhttp_handle_type_session"></span>WINHTTP\_HANDLE\_TYPE\_SESSION</span></span> | <span data-ttu-id="7d023-288">控制碼是會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-288">The handle is a session handle.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7d023-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**\_需要 WINHTTP 選項 \_ HTTP \_ 通訊協定 \_**</span><span class="sxs-lookup"><span data-stu-id="7d023-289"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_REQUIRED"></span><span id="winhttp_option_http_protocol_required"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-290">防止 **WINHTTP \_ 選項啟用 \_ \_ HTTP \_ 通訊協定** 以外的通訊協定版本使用於要求。</span><span class="sxs-lookup"><span data-stu-id="7d023-290">Prevents protocol versions other than those enabled by **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL** from being used for the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-291"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**使用的 WINHTTP \_ 選項 \_ HTTP \_ 通訊協定 \_**</span><span class="sxs-lookup"><span data-stu-id="7d023-291"><span id="WINHTTP_OPTION_HTTP_PROTOCOL_USED"></span><span id="winhttp_option_http_protocol_used"></span>**WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-292">取得 DWORD，指出指定的要求上使用的是哪個先進的 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="7d023-292">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="7d023-293">如需可能值的清單，請參閱 **WINHTTP \_ 選項 \_ ENABLE \_ HTTP \_ PROTOCOL**。</span><span class="sxs-lookup"><span data-stu-id="7d023-293">For a list of possible values, see **WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL**.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-294"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP \_ 選項 \_ HTTP \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="7d023-294"><span id="WINHTTP_OPTION_HTTP_VERSION"></span><span id="winhttp_option_http_version"></span>**WINHTTP\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-295">設定或抓取 [**HTTP \_ 版本 \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) 結構，其中包含所支援的 HTTP 版本。</span><span class="sxs-lookup"><span data-stu-id="7d023-295">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info) structure that contains the HTTP version being supported.</span></span> <span data-ttu-id="7d023-296">這是整個進程的選項;針對控制碼使用 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="7d023-296">This is a process-wide option; use **NULL** for the handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-297"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP \_ 選項 \_ HTTP2 \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="7d023-297"><span id="WINHTTP_OPTION_HTTP2_KEEPALIVE"></span><span id="winhttp_option_http2_keepalive"></span>**WINHTTP\_OPTION\_HTTP2\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7d023-298">您可以在會話控制碼上設定這個選項，讓 WinHttp 使用 HTTP/2 偵測框架作為 keepalive 機制。</span><span class="sxs-lookup"><span data-stu-id="7d023-298">This option can be set on a session handle to have WinHttp use HTTP/2 PING frames as a keepalive mechanism.</span></span> <span data-ttu-id="7d023-299">呼叫端指定的超時時間（以毫秒為單位），且在該超時期間的連線上沒有任何活動之後，WinHttp 將開始傳送 HTTP/2 偵測畫面。</span><span class="sxs-lookup"><span data-stu-id="7d023-299">Callers specify a timeout in milliseconds, and after there is no activity on a connection for that timeout period, WinHttp will begin to send HTTP/2 PING frames.</span></span> <span data-ttu-id="7d023-300">呼叫端無法設定小於5000毫秒的超時值。</span><span class="sxs-lookup"><span data-stu-id="7d023-300">Callers cannot set a timeout value less than 5000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-301"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP \_ 選項 \_ HTTP2 \_ PLUS \_ 傳輸 \_ 編碼**</span><span class="sxs-lookup"><span data-stu-id="7d023-301"><span id="WINHTTP_OPTION_HTTP2_PLUS_TRANSFER_ENCODING"></span><span id="winhttp_option_http2_plus_transfer_encoding"></span>**WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7d023-302">您可以在 WinHttp 要求控制碼上設定這個選項，以控制當 HTTP/2 回應包含「傳輸編碼」標頭時，WinHttp 的行為方式。</span><span class="sxs-lookup"><span data-stu-id="7d023-302">This option can be set on a WinHttp request handle to control how WinHttp behaves when an HTTP/2 response contains a "Transfer-Encoding" header.</span></span> <span data-ttu-id="7d023-303">在這種情況下，如果此選項設定為 **FALSE**，WinHttp 將會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7d023-303">In such a case, WinHttp will return an error if this option is set to **FALSE**.</span></span>


</dt> </dl> </dd> <dt>


<span data-ttu-id="7d023-304"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP \_ 選項會 \_ 離線略過憑證 \_ \_ 撤銷 \_**</span><span class="sxs-lookup"><span data-stu-id="7d023-304"><span id="WINHTTP_OPTION_IGNORE_CERT_REVOCATION_OFFLINE"></span><span id="winhttp_option_ignore_cert_revocation_offline"></span>**WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-305">允許安全連線使用無法下載憑證撤銷清單的安全性憑證。</span><span class="sxs-lookup"><span data-stu-id="7d023-305">Allows secure connections to use security certificates for which the certificate revocation list could not be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-306"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP \_ OPTION \_ IPV6 \_ FAST \_ FALLBACK**</span><span class="sxs-lookup"><span data-stu-id="7d023-306"><span id="WINHTTP_OPTION_IPV6_FAST_FALLBACK"></span><span id="winhttp_option_ipv6_fast_fallback"></span>**WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-307">啟用 IPv6 快速回復 (更滿意的連接 Eyeballs) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-307">Enables IPv6 fast fallback (Happier Eyeballs) for the connection.</span></span> <span data-ttu-id="7d023-308">這種行為與 [RFC 6555](https://tools.ietf.org/html/rfc6555) 中所述的快樂 Eyeballs 行為類似，可在 IPv6 不可靠的網路上改善連線時間。</span><span class="sxs-lookup"><span data-stu-id="7d023-308">This behavior is similar to the Happy Eyeballs behavior described in [RFC 6555](https://tools.ietf.org/html/rfc6555) for improving connection times on networks where IPv6 is unreliable.</span></span>
- <span data-ttu-id="7d023-309">如果為指定的主機解析 IPv6 和 IPv4 位址，WinHttp 將會先以短暫的 (300 毫秒) timeout 來連線至第一個已解析的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="7d023-309">If both IPv6 and IPv4 addresses are resolved for a given host, WinHttp will begin by connecting to the first resolved IPv6 address with a short (300ms) timeout.</span></span>
- <span data-ttu-id="7d023-310">如果連線失敗，WinHttp 將嘗試以標準超時連接到第一個已解析的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="7d023-310">Should that connection fail, WinHttp will attempt to connect to the first resolved IPv4 address with the standard timeout.</span></span>
- <span data-ttu-id="7d023-311">第二個連接失敗時，WinHttp 會以標準超時重試第一個已解析的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="7d023-311">Should the second connection fail, WinHttp will retry the first resolved IPv6 address with the standard timeout.</span></span>
- <span data-ttu-id="7d023-312">第三個連接失敗時，WinHttp 會還原為任何剩餘位址的預設行為，並嘗試使用標準超時連接到每一個位址，直到建立連線或未保留任何位址為止。</span><span class="sxs-lookup"><span data-stu-id="7d023-312">Should the third connection fail, WinHttp will revert to the default behavior for any remaining addresses, attempting a connection to each one with the standard timeout until a connection is made or no addresses remain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-313"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP \_ 選項 \_ 為 \_ PROXY \_ CONNECT \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="7d023-313"><span id="WINHTTP_OPTION_IS_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_is_proxy_connect_response"></span>**WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-314">取得是否可以取出 Proxy 傳回 Connect 回應。</span><span class="sxs-lookup"><span data-stu-id="7d023-314">Gets whether or not a Proxy Return Connect Response can be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-315"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**\_ \_ \_ \_ 每 \_ 1 \_ 0 部 \_ 伺服器的 WINHTTP 選項 MAX CONNS**</span><span class="sxs-lookup"><span data-stu-id="7d023-315"><span id="WINHTTP_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="winhttp_option_max_conns_per_1_0_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-316">設定或抓取不帶正負號的長整數值，其中包含每個 HTTP/1.0 伺服器允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="7d023-316">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="7d023-317">預設值為 [ **無限**]。</span><span class="sxs-lookup"><span data-stu-id="7d023-317">The default value is **INFINITE**.</span></span>

<span data-ttu-id="7d023-318">**Windows VISTA SP1 和 Windows Server 2008：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7d023-318">**Windows Vista with SP1 and Windows Server 2008:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-319"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**每一伺服器的 WINHTTP \_ 選項 \_ MAX \_ CONNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7d023-319"><span id="WINHTTP_OPTION_MAX_CONNS_PER_SERVER"></span><span id="winhttp_option_max_conns_per_server"></span>**WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-320">設定或抓取不帶正負號的長整數值，其中包含每個伺服器允許的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="7d023-320">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="7d023-321">預設值為 [ **無限**]。</span><span class="sxs-lookup"><span data-stu-id="7d023-321">The default value is **INFINITE**.</span></span>

<span data-ttu-id="7d023-322">當此選項設定為零時，WinHTTP 會將連接數目的限制設定為2。</span><span class="sxs-lookup"><span data-stu-id="7d023-322">When this option is set to zero, WinHTTP sets the limit on the number of connections to 2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-323"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 自動重新 \_ 導向**</span><span class="sxs-lookup"><span data-stu-id="7d023-323"><span id="WINHTTP_OPTION_MAX_HTTP_AUTOMATIC_REDIRECTS"></span><span id="winhttp_option_max_http_automatic_redirects"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-324">設定 WinHTTP 遵循的重新導向數目上限;預設值為10。</span><span class="sxs-lookup"><span data-stu-id="7d023-324">Sets the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="7d023-325">這項限制可防止未經授權的網站使 WinHTTP 用戶端在大量重新導向之後暫停。</span><span class="sxs-lookup"><span data-stu-id="7d023-325">This limit prevents unauthorized sites from making the WinHTTP client pause following a large number of redirects.</span></span>

<span data-ttu-id="7d023-326">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7d023-326">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-327"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 狀態 \_ 繼續**</span><span class="sxs-lookup"><span data-stu-id="7d023-327"><span id="WINHTTP_OPTION_MAX_HTTP_STATUS_CONTINUE"></span><span id="winhttp_option_max_http_status_continue"></span>**WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-328">將最終狀態代碼傳回至 WinHTTP 用戶端之前，已忽略參考最大的資訊100-199 狀態碼回應數目。</span><span class="sxs-lookup"><span data-stu-id="7d023-328">The maximum number of Informational 100-199 status code responses ignored before returning the final status code to the WinHTTP client.</span></span> <span data-ttu-id="7d023-329">資訊100-199 狀態碼可由伺服器在最終狀態代碼之前傳送，如需詳細資訊，請參閱 HTTP/1.1 的規格 (如需詳細資訊，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-329">Informational 100-199 status codes can be sent by the server before the final status code, and are described in the specification for HTTP/1.1 (for more information, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)).</span></span> <span data-ttu-id="7d023-330">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="7d023-330">The default is 10.</span></span>

<span data-ttu-id="7d023-331">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7d023-331">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-332"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP \_ 選項 \_ \_ 回應 \_ 清空最 \_ 大值**</span><span class="sxs-lookup"><span data-stu-id="7d023-332"><span id="WINHTTP_OPTION_MAX_RESPONSE_DRAIN_SIZE"></span><span id="winhttp_option_max_response_drain_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-333">系結至從回應中清空的資料量，以重複使用連接（以位元組指定）。</span><span class="sxs-lookup"><span data-stu-id="7d023-333">A bound on the amount of data drained from responses in order to reuse a connection, specified in bytes.</span></span> <span data-ttu-id="7d023-334">預設值為1MB。</span><span class="sxs-lookup"><span data-stu-id="7d023-334">The default is 1MB.</span></span>

<span data-ttu-id="7d023-335">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7d023-335">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-336"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP \_ 選項 \_ 的 \_ 回應 \_ 標頭 \_ 大小上限**</span><span class="sxs-lookup"><span data-stu-id="7d023-336"><span id="WINHTTP_OPTION_MAX_RESPONSE_HEADER_SIZE"></span><span id="winhttp_option_max_response_header_size"></span>**WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-337">伺服器回應的標頭部分大小上限的系結集，以位元組為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="7d023-337">A bound set on the maximum size of the header portion of the server response, specified in bytes.</span></span> <span data-ttu-id="7d023-338">這項系結會透過傳送無限標頭資料的回應，來保護用戶端免于嘗試停止用戶端的未經授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="7d023-338">This bound protects the client from an unauthorized server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="7d023-339">預設值是64KB。</span><span class="sxs-lookup"><span data-stu-id="7d023-339">The default value is 64KB.</span></span>

<span data-ttu-id="7d023-340">**WINDOWS XP 加裝 SP1 和 windows 2000 SP3：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7d023-340">**Windows XP with SP1 and Windows 2000 with SP3:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-341"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP \_ 選項 \_ 父 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="7d023-341"><span id="WINHTTP_OPTION_PARENT_HANDLE"></span><span id="winhttp_option_parent_handle"></span>**WINHTTP\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-342">捕獲此控制碼的父控制碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-342">Retrieves the parent handle to this handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-343"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ 文字**</span><span class="sxs-lookup"><span data-stu-id="7d023-343"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_TEXT"></span><span id="winhttp_option_passport_cobranding_text"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-344">抓取包含 Passport 登入伺服器所提供之 [*cobranding*](glossary.md) 文字的字串。</span><span class="sxs-lookup"><span data-stu-id="7d023-344">Retrieves a string that contains the [*cobranding*](glossary.md) text provided by the Passport logon server.</span></span> <span data-ttu-id="7d023-345">當登入伺服器以401狀態碼回應時，應立即取出此選項。</span><span class="sxs-lookup"><span data-stu-id="7d023-345">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="7d023-346">應用程式應該以位元組為單位，以位元組為單位，且足以容納傳回的字串。</span><span class="sxs-lookup"><span data-stu-id="7d023-346">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-347"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ URL**</span><span class="sxs-lookup"><span data-stu-id="7d023-347"><span id="WINHTTP_OPTION_PASSPORT_COBRANDING_URL"></span><span id="winhttp_option_passport_cobranding_url"></span>**WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-348">抓取包含 Passport 登入伺服器所提供之 [*cobranding*](glossary.md) 圖形 URL 的字串。</span><span class="sxs-lookup"><span data-stu-id="7d023-348">Retrieves a string that contains a URL for a [*cobranding*](glossary.md) graphic provided by the Passport logon server.</span></span> <span data-ttu-id="7d023-349">當登入伺服器以401狀態碼回應時，應立即取出此選項。</span><span class="sxs-lookup"><span data-stu-id="7d023-349">This option should be retrieved immediately after the logon server responds with a 401 status code.</span></span> <span data-ttu-id="7d023-350">應用程式應該以位元組為單位，以位元組為單位，且足以容納傳回的字串。</span><span class="sxs-lookup"><span data-stu-id="7d023-350">An application should pass in a buffer size, in bytes, that is big enough to hold the returned string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-351"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ RETURN \_ URL**</span><span class="sxs-lookup"><span data-stu-id="7d023-351"><span id="WINHTTP_OPTION_PASSPORT_RETURN_URL"></span><span id="winhttp_option_passport_return_url"></span>**WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-352">在要求控制碼上設定唯讀選項，以抓取 Passport 傳回 URL。</span><span class="sxs-lookup"><span data-stu-id="7d023-352">Sets a read-only option on a request handle that retrieves the Passport return URL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-353"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP \_ 選項 \_ PASSPORT \_ 登出 \_**</span><span class="sxs-lookup"><span data-stu-id="7d023-353"><span id="WINHTTP_OPTION_PASSPORT_SIGN_OUT"></span><span id="winhttp_option_passport_sign_out"></span>**WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-354">將會話控制碼上的選項設定為登出任何 Passport 登入。</span><span class="sxs-lookup"><span data-stu-id="7d023-354">Sets the option on a session handle to sign out of any Passport logins.</span></span> <span data-ttu-id="7d023-355">應用程式應該傳入 Passport 傳回 URL，此 URL 是以 **WINHTTP \_ 選項 \_ Passport \_ return \_ url** 抓取。</span><span class="sxs-lookup"><span data-stu-id="7d023-355">An application should pass in the Passport return URL that was retrieved with **WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL**.</span></span> <span data-ttu-id="7d023-356">系統會清除所有與傳回 URL 相關的 cookie。</span><span class="sxs-lookup"><span data-stu-id="7d023-356">All cookies related to the return URL are cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-357"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP \_ 選項 \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="7d023-357"><span id="WINHTTP_OPTION_PASSWORD"></span><span id="winhttp_option_password"></span>**WINHTTP\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-358">設定或抓取包含與要求控制碼相關聯之密碼的字串值。</span><span class="sxs-lookup"><span data-stu-id="7d023-358">Sets or retrieves a string value that contains the password associated with a request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-359"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP \_ 選項 \_ PROXY**</span><span class="sxs-lookup"><span data-stu-id="7d023-359"><span id="WINHTTP_OPTION_PROXY"></span><span id="winhttp_option_proxy"></span>**WINHTTP\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-360">設定或抓取 [**WINHTTP \_ PROXY \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) 結構，其中包含現有會話控制碼或要求控制碼上的 PROXY 資料。</span><span class="sxs-lookup"><span data-stu-id="7d023-360">Sets or retrieves an [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure that contains the proxy data on an existing session handle or request handle.</span></span> <span data-ttu-id="7d023-361">在抓取 proxy 資料時，應用程式必須釋放此結構中所包含的 **lpszProxy** 和 **lpszProxyBypass** 字串 (如果它們是非 **Null**) 使用 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函數。</span><span class="sxs-lookup"><span data-stu-id="7d023-361">When retrieving proxy data, an application must free the **lpszProxy** and **lpszProxyBypass** strings contained in this structure (if they are non-**NULL**) using the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="7d023-362">應用程式可以藉由傳遞 **Null** 控制碼 (預設 proxy) 來查詢全域 proxy 資料。</span><span class="sxs-lookup"><span data-stu-id="7d023-362">An application can query for the global proxy data (the default proxy) by passing a **NULL** handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-363"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP \_ 選項 \_ PROXY \_ 密碼**</span><span class="sxs-lookup"><span data-stu-id="7d023-363"><span id="WINHTTP_OPTION_PROXY_PASSWORD"></span><span id="winhttp_option_proxy_password"></span>**WINHTTP\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-364">設定或抓取包含用來存取 proxy 之密碼的字串值。</span><span class="sxs-lookup"><span data-stu-id="7d023-364">Sets or retrieves a string value that contains the password used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-365"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**已 \_ 使用 WINHTTP 選項 \_ PROXY \_ SPN \_**</span><span class="sxs-lookup"><span data-stu-id="7d023-365"><span id="WINHTTP_OPTION_PROXY_SPN_USED"></span><span id="winhttp_option_proxy_spn_used"></span>**WINHTTP\_OPTION\_PROXY\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-366">取得 WinHTTP 在驗證期間提供給 SSPI 的 proxy 伺服器主體名稱。</span><span class="sxs-lookup"><span data-stu-id="7d023-366">Gets the proxy Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="7d023-367">這個字串值會在驗證失敗後 usefor 傳遞至 [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-367">This string value is usefor passing to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-368"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP \_ 選項 \_ PROXY 使用者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="7d023-368"><span id="WINHTTP_OPTION_PROXY_USERNAME"></span><span id="winhttp_option_proxy_username"></span>**WINHTTP\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-369">設定或抓取包含用來存取 proxy 之使用者名稱的字串值。</span><span class="sxs-lookup"><span data-stu-id="7d023-369">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-370"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP \_ 選項 \_ 讀取 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="7d023-370"><span id="WINHTTP_OPTION_READ_BUFFER_SIZE"></span><span id="winhttp_option_read_buffer_size"></span>**WINHTTP\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-371">此選項已被取代;它沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="7d023-371">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-372"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP \_ 選項 \_ 接收 \_ PROXY \_ CONNECT \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="7d023-372"><span id="WINHTTP_OPTION_RECEIVE_PROXY_CONNECT_RESPONSE"></span><span id="winhttp_option_receive_proxy_connect_response"></span>**WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-373">設定是否可以取出 proxy 回應實體。</span><span class="sxs-lookup"><span data-stu-id="7d023-373">Sets whether or not the proxy response entity can be retrieved.</span></span> <span data-ttu-id="7d023-374">預設會停用這個選項。</span><span class="sxs-lookup"><span data-stu-id="7d023-374">This option is disabled by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-375"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP \_ 選項 \_ 接收 \_ 回應 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="7d023-375"><span id="WINHTTP_OPTION_RECEIVE_RESPONSE_TIMEOUT"></span><span id="winhttp_option_receive_response_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-376">設定或抓取不帶正負號的長整數值，其中包含要等候接收要求的所有回應標頭的超時值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d023-376">Sets or retrieves an unsigned long integer value that contains the timeout value, in milliseconds, to wait to receive all response headers to a request.</span></span> <span data-ttu-id="7d023-377">如果 WinHTTP 無法在此超時期間內接收所有標頭，則會取消要求。</span><span class="sxs-lookup"><span data-stu-id="7d023-377">If WinHTTP fails to receive all the headers within this timeout period, the request is canceled.</span></span> <span data-ttu-id="7d023-378">預設的超時值為90秒。</span><span class="sxs-lookup"><span data-stu-id="7d023-378">The default timeout value is 90 seconds.</span></span>

<span data-ttu-id="7d023-379">只有從通訊端接收資料時，才會檢查此超時時間。</span><span class="sxs-lookup"><span data-stu-id="7d023-379">This timeout is checked only when data is received from the socket.</span></span> <span data-ttu-id="7d023-380">如此一來，當超時時間過期時，用戶端應用程式就不會收到通知，直到伺服器的資料抵達為止。</span><span class="sxs-lookup"><span data-stu-id="7d023-380">As a result, when the timeout expires the client application is not notified until more data arrives from the server.</span></span> <span data-ttu-id="7d023-381">如果沒有資料從伺服器抵達，用戶端應用程式的超時期限和通知之間的延遲可能會與使用 [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)函數的 *dwReceiveTimeout* 參數所設定的超時值相同。</span><span class="sxs-lookup"><span data-stu-id="7d023-381">If no data arrives from the server, the delay between the timeout expiration and notification of the client application could be as large as the timeout value set using the *dwReceiveTimeout* parameter of the [**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-382"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP \_ 選項 \_ 接收 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="7d023-382"><span id="WINHTTP_OPTION_RECEIVE_TIMEOUT"></span><span id="winhttp_option_receive_timeout"></span>**WINHTTP\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-383">設定或抓取不帶正負號的長整數值，其中包含接收要求的部分回應或讀取某些資料的超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d023-383">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a partial response to a request or read some data.</span></span> <span data-ttu-id="7d023-384">如果回應時間超過這個超時值，就會取消要求。</span><span class="sxs-lookup"><span data-stu-id="7d023-384">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="7d023-385">預設的逾時值是 30 秒。</span><span class="sxs-lookup"><span data-stu-id="7d023-385">The default timeout value is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-386"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP \_ 選項重新 \_ 導向 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="7d023-386"><span id="WINHTTP_OPTION_REDIRECT_POLICY"></span><span id="winhttp_option_redirect_policy"></span>**WINHTTP\_OPTION\_REDIRECT\_POLICY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-387">設定 WinHTTP 的行為，關於處理一倍的 HTTP 重新導向狀態碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-387">Sets the behavior of WinHTTP regarding the handling of a 30x HTTP redirect status code.</span></span> <span data-ttu-id="7d023-388">您可以在會話或要求控制碼上將此選項設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="7d023-388">This option can be set on a session or request handle to one of the following values:</span></span>

| <span data-ttu-id="7d023-389">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-389">Term</span></span> | <span data-ttu-id="7d023-390">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-390">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-391"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP \_ 選項的重新 \_ 導向 \_ 原則 \_ 一律</span><span class="sxs-lookup"><span data-stu-id="7d023-391"><span id="WINHTTP_OPTION_REDIRECT_POLICY_ALWAYS"></span><span id="winhttp_option_redirect_policy_always"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_ALWAYS</span></span> | <span data-ttu-id="7d023-392">所有重新導向都會自動遵循。</span><span class="sxs-lookup"><span data-stu-id="7d023-392">All redirects are followed automatically.</span></span> |
| <span data-ttu-id="7d023-393"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP \_ 選項重新 \_ 導向 \_ 原則不 \_ 允許 \_ HTTPS \_ 至 \_ HTTP</span><span class="sxs-lookup"><span data-stu-id="7d023-393"><span id="WINHTTP_OPTION_REDIRECT_POLICY_DISALLOW_HTTPS_TO_HTTP"></span><span id="winhttp_option_redirect_policy_disallow_https_to_http"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_DISALLOW\_HTTPS\_TO\_HTTP</span></span> | <span data-ttu-id="7d023-394">除了源自安全 (HTTPs) URL 到不安全的 (HTTP) URL 以外的所有重新導向。</span><span class="sxs-lookup"><span data-stu-id="7d023-394">All redirects are followed, except those that originate from a secure (https) URL to an unsecure (http) URL.</span></span> <span data-ttu-id="7d023-395">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="7d023-395">This is the default setting.</span></span> |
| <span data-ttu-id="7d023-396"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP \_ 選項重新 \_ 導向 \_ 原則 \_ 永不</span><span class="sxs-lookup"><span data-stu-id="7d023-396"><span id="WINHTTP_OPTION_REDIRECT_POLICY_NEVER"></span><span id="winhttp_option_redirect_policy_never"></span>WINHTTP\_OPTION\_REDIRECT\_POLICY\_NEVER</span></span> | <span data-ttu-id="7d023-397">重新導向永遠不會跟著進行。</span><span class="sxs-lookup"><span data-stu-id="7d023-397">Redirects are never followed.</span></span> <span data-ttu-id="7d023-398">這會將30倍的狀態傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="7d023-398">The 30x status is returned to the application.</span></span> |


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-399"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP \_ 選項 \_ 拒絕 \_ \_ URL 中的 USERPWD \_**</span><span class="sxs-lookup"><span data-stu-id="7d023-399"><span id="WINHTTP_OPTION_REJECT_USERPWD_IN_URL"></span><span id="winhttp_option_reject_userpwd_in_url"></span>**WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-400">拒絕包含使用者名稱和密碼的 Url。</span><span class="sxs-lookup"><span data-stu-id="7d023-400">Rejects URLs that contain a username and password.</span></span> <span data-ttu-id="7d023-401">即使未指定使用者名稱或密碼，此選項也會拒絕包含 *username： password* 語義的 url。</span><span class="sxs-lookup"><span data-stu-id="7d023-401">This option also rejects URLs that contain *username:password* semantics, even if no username or password is specified.</span></span> <span data-ttu-id="7d023-402">例如，" u:p@hostname "、" :@hostname "、" u:@hostname " 和 " :p@hostname " 都會標示為無效。</span><span class="sxs-lookup"><span data-stu-id="7d023-402">For example, "u:p@hostname", ":@hostname", "u:@hostname", and ":p@hostname" would all be flagged as invalid.</span></span> <span data-ttu-id="7d023-403">如果將不正確 URL 傳遞至函式，則會傳回 [錯誤 \_ WINHTTP 不正確 \_ \_ url](error-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="7d023-403">If an invalid URL is passed to the function, it returns [ERROR\_WINHTTP\_INVALID\_URL](error-messages.md).</span></span> <span data-ttu-id="7d023-404">根據預設，這個選項是關閉的。</span><span class="sxs-lookup"><span data-stu-id="7d023-404">This option is turned off by default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-405"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP \_ 選項 \_ 要求 \_ 優先順序**</span><span class="sxs-lookup"><span data-stu-id="7d023-405"><span id="WINHTTP_OPTION_REQUEST_PRIORITY"></span><span id="winhttp_option_request_priority"></span>**WINHTTP\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-406">此選項已被取代;它沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="7d023-406">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-407"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP \_ 選項 \_ 要求 \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="7d023-407"><span id="WINHTTP_OPTION_REQUEST_STATS"></span><span id="winhttp_option_request_stats"></span>**WINHTTP\_OPTION\_REQUEST\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-408">擷取要求的統計資料。</span><span class="sxs-lookup"><span data-stu-id="7d023-408">Retreives statistics for the request.</span></span>  <span data-ttu-id="7d023-409">如需可用的統計資料清單，請參閱 [**WINHTTP \_ 要求 \_ 統計**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)資料。</span><span class="sxs-lookup"><span data-stu-id="7d023-409">For a list of the available statistics, see [**WINHTTP\_REQUEST\_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-410"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP \_ 選項 \_ 要求 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="7d023-410"><span id="WINHTTP_OPTION_REQUEST_TIMES"></span><span id="winhttp_option_request_times"></span>**WINHTTP\_OPTION\_REQUEST\_TIMES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-411">擷取要求的計時資訊。</span><span class="sxs-lookup"><span data-stu-id="7d023-411">Retreives timing information for the request.</span></span> <span data-ttu-id="7d023-412">如需可用的時間清單，請參閱 [**WINHTTP \_ 要求 \_ 時間**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)。</span><span class="sxs-lookup"><span data-stu-id="7d023-412">For a list of the available timings, see [**WINHTTP\_REQUEST\_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-413"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP \_ 選項 \_ 需要 \_ STREAM \_ END**</span><span class="sxs-lookup"><span data-stu-id="7d023-413"><span id="WINHTTP_OPTION_REQUIRE_STREAM_END"></span><span id="winhttp_option_require_stream_end"></span>**WINHTTP\_OPTION\_REQUIRE\_STREAM\_END**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7d023-414">此選項會告知 WinHttp 略過「內容長度」回應標頭，並繼續接收串流，直到收到 END_STREAM 旗標為止。</span><span class="sxs-lookup"><span data-stu-id="7d023-414">This option tells WinHttp to ignore "Content-Length" response headers, and continue receiving on a stream until the END_STREAM flag is received.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-415"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP \_ 選項 \_ 解析 \_ 主機名稱**</span><span class="sxs-lookup"><span data-stu-id="7d023-415"><span id="WINHTTP_OPTION_RESOLUTION_HOSTNAME"></span><span id="winhttp_option_resolution_hostname"></span>**WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7d023-416">您可以在 WinHttp 要求控制碼上設定這個選項，然後再傳送。</span><span class="sxs-lookup"><span data-stu-id="7d023-416">This option can be set on a WinHttp request handle before it has been sent.</span></span> <span data-ttu-id="7d023-417">如果設定，WinHttp 將使用呼叫端提供的字串作為 DNS 解析的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="7d023-417">If set, WinHttp will use the caller-provided string as the hostname for DNS resolution.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-418"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP \_ 選項 \_ 解析 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="7d023-418"><span id="WINHTTP_OPTION_RESOLVE_TIMEOUT"></span><span id="winhttp_option_resolve_timeout"></span>**WINHTTP\_OPTION\_RESOLVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-419">設定或抓取不帶正負號的長整數值，其中包含用來解析主機名稱的超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d023-419">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to resolve a host name.</span></span> <span data-ttu-id="7d023-420">預設的超時值是 **無限** 的。</span><span class="sxs-lookup"><span data-stu-id="7d023-420">The default timeout value is **INFINITE**.</span></span> <span data-ttu-id="7d023-421">如果指定了非預設值，每個名稱解析都有一個執行緒建立的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="7d023-421">If a non-default value is specified, there is an overhead of one thread-creation per name resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-422"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP \_ 選項 \_ 安全 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="7d023-422"><span id="WINHTTP_OPTION_SECURE_PROTOCOLS"></span><span id="winhttp_option_secure_protocols"></span>**WINHTTP\_OPTION\_SECURE\_PROTOCOLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-423">設定不帶正負號的長整數值，指定可接受哪些安全通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7d023-423">Sets an unsigned long integer value that specifies which secure protocols are acceptable.</span></span> <span data-ttu-id="7d023-424">依預設，只有 SSL3 和 TLS1 會在 Windows 7 和 Windows 8 中啟用。</span><span class="sxs-lookup"><span data-stu-id="7d023-424">By default only SSL3 and TLS1 are enabled in Windows 7 and Windows 8.</span></span> <span data-ttu-id="7d023-425">依預設，只有 SSL3、TLS 1.0、TLS 1.1 和 TLS 1.2 會在 Windows 8.1 和 Windows 10 中啟用。</span><span class="sxs-lookup"><span data-stu-id="7d023-425">By default only SSL3, TLS1.0, TLS1.1, and TLS1.2 are enabled in Windows 8.1 and Windows 10.</span></span> <span data-ttu-id="7d023-426">值可以是下列一或多個值的組合。</span><span class="sxs-lookup"><span data-stu-id="7d023-426">The value can be a combination of one or more of the following values.</span></span>

| <span data-ttu-id="7d023-427">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-427">Term</span></span> | <span data-ttu-id="7d023-428">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-428">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-429"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="7d023-429"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_ALL"></span><span id="winhttp_flag_secure_protocol_all"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_ALL</span></span> | <span data-ttu-id="7d023-430">您可以使用安全通訊端層 (SSL) 2.0、SSL 3.0 和傳輸層安全性 (TLS) 1.0 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7d023-430">The Secure Sockets Layer (SSL) 2.0, SSL 3.0, and Transport Layer Security (TLS) 1.0 protocols can be used.</span></span> |
| <span data-ttu-id="7d023-431"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ SSL2</span><span class="sxs-lookup"><span data-stu-id="7d023-431"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL2"></span><span id="winhttp_flag_secure_protocol_ssl2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL2</span></span> | <span data-ttu-id="7d023-432">您可以使用 SSL 2.0 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7d023-432">The SSL 2.0 protocol can be used.</span></span> |
| <span data-ttu-id="7d023-433"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="7d023-433"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_SSL3"></span><span id="winhttp_flag_secure_protocol_ssl3"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_SSL3</span></span> | <span data-ttu-id="7d023-434">您可以使用 SSL 3.0 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7d023-434">The SSL 3.0 protocol can be used.</span></span> |
| <span data-ttu-id="7d023-435"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ TLS1</span><span class="sxs-lookup"><span data-stu-id="7d023-435"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1"></span><span id="winhttp_flag_secure_protocol_tls1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1</span></span> | <span data-ttu-id="7d023-436">您可以使用 TLS 1.0 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7d023-436">The TLS 1.0 protocol can be used.</span></span> |
| <span data-ttu-id="7d023-437"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ TLS1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="7d023-437"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_1"></span><span id="winhttp_flag_secure_protocol_tls1_1"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_1</span></span> | <span data-ttu-id="7d023-438">您可以使用 TLS 1.1 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7d023-438">The TLS 1.1 protocol can be used.</span></span> |
| <span data-ttu-id="7d023-439"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP \_ 旗標 \_ 安全 \_ 通訊協定 \_ TLS1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="7d023-439"><span id="WINHTTP_FLAG_SECURE_PROTOCOL_TLS1_2"></span><span id="winhttp_flag_secure_protocol_tls1_2"></span>WINHTTP\_FLAG\_SECURE\_PROTOCOL\_TLS1\_2</span></span> | <span data-ttu-id="7d023-440">您可以使用 TLS 1.2 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7d023-440">The TLS 1.2 protocol can be used.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7d023-441"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 憑證 \_ 結構**</span><span class="sxs-lookup"><span data-stu-id="7d023-441"><span id="WINHTTP_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="winhttp_option_security_certificate_struct"></span>**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-442">抓取 SSL/TLS 伺服器到 [**WINHTTP \_ 憑證 \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) 結構中的憑證。</span><span class="sxs-lookup"><span data-stu-id="7d023-442">Retrieves the certificate for a SSL/TLS server into the [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="7d023-443">應用程式必須使用 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree)釋放 **lpszSubjectInfo** 和 **lpszIssuerInfo** 成員。</span><span class="sxs-lookup"><span data-stu-id="7d023-443">The application must free the **lpszSubjectInfo** and **lpszIssuerInfo** members with [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-444"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="7d023-444"><span id="WINHTTP_OPTION_SECURITY_FLAGS"></span><span id="winhttp_option_security_flags"></span>**WINHTTP\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-445">設定或抓取不帶正負號的長整數值，其中包含控制碼的安全性旗標。</span><span class="sxs-lookup"><span data-stu-id="7d023-445">Sets or retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="7d023-446">它可以是下列值的組合：</span><span class="sxs-lookup"><span data-stu-id="7d023-446">It can be a combination of these values:</span></span>

| <span data-ttu-id="7d023-447">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-447">Term</span></span> | <span data-ttu-id="7d023-448">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-448">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-449"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>安全性 \_ 旗標 \_ 忽略 \_ CERT \_ CN \_ 無效</span><span class="sxs-lookup"><span data-stu-id="7d023-449"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span> |<span data-ttu-id="7d023-450">允許在憑證中使用不正確一般名稱;亦即，應用程式所指定的伺服器名稱不符合憑證中的一般名稱。</span><span class="sxs-lookup"><span data-stu-id="7d023-450">Allows an invalid common name in a certificate; that is, the server name specified by the application does not match the common name in the certificate.</span></span> <span data-ttu-id="7d023-451">如果設定此旗標，則應用程式不會收到 **WINHTTP \_ 回呼 \_ 狀態 \_ 旗標 \_ CERT \_ CN \_ 無效** 的回呼。</span><span class="sxs-lookup"><span data-stu-id="7d023-451">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_CN\_INVALID** callback.</span></span> |
| <span data-ttu-id="7d023-452"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>安全性 \_ 旗標 \_ 忽略憑證 \_ \_ 日期 \_ 無效</span><span class="sxs-lookup"><span data-stu-id="7d023-452"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span> |<span data-ttu-id="7d023-453">允許不正確憑證日期，也就是過期或尚未有效的憑證。</span><span class="sxs-lookup"><span data-stu-id="7d023-453">Allows an invalid certificate date, that is, an expired or not-yet-effective certificate.</span></span> <span data-ttu-id="7d023-454">如果設定此旗標，則應用程式不會收到 **WINHTTP \_ 回呼 \_ 狀態 \_ 旗標憑證 \_ \_ 日期 \_ 無效** 的回呼。</span><span class="sxs-lookup"><span data-stu-id="7d023-454">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_CERT\_DATE\_INVALID** callback.</span></span> |
| <span data-ttu-id="7d023-455"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>安全性 \_ 旗標 \_ 忽略 \_ 未知的 \_ CA</span><span class="sxs-lookup"><span data-stu-id="7d023-455"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span> | <span data-ttu-id="7d023-456">允許不正確憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="7d023-456">Allows an invalid certificate authority.</span></span> <span data-ttu-id="7d023-457">如果設定此旗標，則應用程式不會收到 **WINHTTP \_ 回呼 \_ 狀態 \_ 旗標 \_ 不正確 \_ CA** 回呼。</span><span class="sxs-lookup"><span data-stu-id="7d023-457">If this flag is set, the application does not receive a **WINHTTP\_CALLBACK\_STATUS\_FLAG\_INVALID\_CA** callback.</span></span> |
| <span data-ttu-id="7d023-458"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>安全性 \_ 旗標 \_ 忽略憑證錯誤的 \_ \_ \_ 使用方式</span><span class="sxs-lookup"><span data-stu-id="7d023-458"><span id="SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE"></span><span id="security_flag_ignore_cert_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_CERT\_WRONG\_USAGE</span></span> | <span data-ttu-id="7d023-459">允許以非伺服器憑證建立伺服器的身分識別 (例如，) 的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="7d023-459">Allows the identity of a server to be established with a non-server certificate (for example, a client certificate).</span></span> |
| <span data-ttu-id="7d023-460"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>安全性 \_ 旗標 \_ 忽略 \_ 弱 \_ 式簽章</span><span class="sxs-lookup"><span data-stu-id="7d023-460"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span> | <span data-ttu-id="7d023-461">允許忽略弱式簽章。</span><span class="sxs-lookup"><span data-stu-id="7d023-461">Allows a weak signature to be ignored.</span></span><br/><span data-ttu-id="7d023-462">從 Windows 7 和 Windows Server 2008 R2 開始，每個 OS 的匯總套件更新中都有提供此旗標。</span><span class="sxs-lookup"><span data-stu-id="7d023-462">This flag is available in the rollup update for each OS starting with Windows 7 and Windows Server 2008 R2.</span></span> |
| <span data-ttu-id="7d023-463"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>安全性 \_ 旗標 \_ 安全</span><span class="sxs-lookup"><span data-stu-id="7d023-463"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span> | <span data-ttu-id="7d023-464">使用安全傳輸。</span><span class="sxs-lookup"><span data-stu-id="7d023-464">Uses secure transfers.</span></span> <span data-ttu-id="7d023-465">這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。</span><span class="sxs-lookup"><span data-stu-id="7d023-465">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="7d023-466"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>安全性 \_ 旗標 \_ 強度 \_ 中</span><span class="sxs-lookup"><span data-stu-id="7d023-466"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span> | <span data-ttu-id="7d023-467">使用中型 (56 位) 加密。</span><span class="sxs-lookup"><span data-stu-id="7d023-467">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="7d023-468">這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。</span><span class="sxs-lookup"><span data-stu-id="7d023-468">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="7d023-469"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>安全性 \_ 旗標 \_ 強度 \_ 強</span><span class="sxs-lookup"><span data-stu-id="7d023-469"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span> | <span data-ttu-id="7d023-470">使用強式 (128 位) 加密。</span><span class="sxs-lookup"><span data-stu-id="7d023-470">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="7d023-471">這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。</span><span class="sxs-lookup"><span data-stu-id="7d023-471">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |
| <span data-ttu-id="7d023-472"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>安全性 \_ 旗標 \_ 強度 \_ 弱</span><span class="sxs-lookup"><span data-stu-id="7d023-472"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span> | <span data-ttu-id="7d023-473">使用弱式 (40 位) 加密。</span><span class="sxs-lookup"><span data-stu-id="7d023-473">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="7d023-474">這只會在呼叫 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)時傳回。</span><span class="sxs-lookup"><span data-stu-id="7d023-474">This is only returned in a call to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption).</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7d023-475"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="7d023-475"><span id="WINHTTP_OPTION_SECURITY_INFO"></span><span id="winhttp_option_security_info"></span>**WINHTTP\_OPTION\_SECURITY\_INFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-476">擷取要求的 SChannel 連線和加密資訊。</span><span class="sxs-lookup"><span data-stu-id="7d023-476">Retreives the SChannel connection and cipher information for a request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-477"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP \_ 選項 \_ 安全性 \_ 金鑰 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="7d023-477"><span id="WINHTTP_OPTION_SECURITY_KEY_BITNESS"></span><span id="winhttp_option_security_key_bitness"></span>**WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-478">抓取不帶正負號的長整數值，其中包含加密金鑰的加密強度。</span><span class="sxs-lookup"><span data-stu-id="7d023-478">Retrieves an unsigned long integer value that contains the cipher strength of the encryption key.</span></span> <span data-ttu-id="7d023-479">較大的數位表示較強的加密強度加密。</span><span class="sxs-lookup"><span data-stu-id="7d023-479">A larger number indicates stronger cipher strength encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-480"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP \_ 選項 \_ 傳送 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="7d023-480"><span id="WINHTTP_OPTION_SEND_TIMEOUT"></span><span id="winhttp_option_send_timeout"></span>**WINHTTP\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-481">設定或抓取不帶正負號的長整數值，其中包含要傳送要求或寫入部分資料的超時時間值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d023-481">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to send a request or write some data.</span></span> <span data-ttu-id="7d023-482">如果傳送要求的時間超過超時時間，則會取消傳送作業。</span><span class="sxs-lookup"><span data-stu-id="7d023-482">If sending the request takes longer than the timeout, the send operation is canceled.</span></span> <span data-ttu-id="7d023-483">預設的超時時間為30秒。</span><span class="sxs-lookup"><span data-stu-id="7d023-483">The default timeout is 30 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-484"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP \_ 選項 \_ 伺服器 \_ CBT**</span><span class="sxs-lookup"><span data-stu-id="7d023-484"><span id="WINHTTP_OPTION_SERVER_CBT"></span><span id="winhttp_option_server_cbt"></span>**WINHTTP\_OPTION\_SERVER\_CBT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-485">取得 SecPkgCoNtext 系結 [**結構 \_**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) 的指標，此結構會指定 (CBT) 的通道系結 Token。</span><span class="sxs-lookup"><span data-stu-id="7d023-485">Gets a pointer to [**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings) structure that specifies a Channel Binding Token (CBT).</span></span>

<span data-ttu-id="7d023-486">通道系結權杖是安全傳輸通道的屬性，可用來將驗證通道系結至安全傳輸通道。</span><span class="sxs-lookup"><span data-stu-id="7d023-486">A Channel Binding Token is a property of a secure transport channel and is used to bind an authentication channel to the secure transport channel.</span></span> <span data-ttu-id="7d023-487">只有在建立 SSL 連線之後，此選項才能取得此權杖。</span><span class="sxs-lookup"><span data-stu-id="7d023-487">This token can only be obtained by this option after an SSL connection has been established.</span></span>

> [!Note]
> <span data-ttu-id="7d023-488">傳遞此選項和 *lpBuffer* 至 [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)的 **null** 值，將會傳回 \_ 錯誤 \_ 的緩衝區，以及 *lpdwBufferLength* 參數中緩衝區的必要位元組大小。</span><span class="sxs-lookup"><span data-stu-id="7d023-488">Passing this option and a **null** value for *lpBuffer* to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) will return ERROR\_INSUFFICIENT\_BUFFER and the required byte size for the buffer in the *lpdwBufferLength* parameter.</span></span> <span data-ttu-id="7d023-489">這個傳回的緩衝區大小值可以在後續的呼叫中傳遞，以查詢通道系結 Token。</span><span class="sxs-lookup"><span data-stu-id="7d023-489">This returned buffer size value can be passed in a subsequent call to query for the Channel Binding Token.</span></span> <span data-ttu-id="7d023-490">\_ \_ \_ 如果您想要根據通道系結 Token 修改要求標頭，則在處理 WINHTTP 回呼狀態要求時，必須執行這些步驟。</span><span class="sxs-lookup"><span data-stu-id="7d023-490">These steps are necessary when handling WINHTTP\_CALLBACK\_STATUS\_REQUEST if you want to modify request headers based on the Channel Binding Token.</span></span> <span data-ttu-id="7d023-491">請注意，Windows XP 和 Vista 不支援在此回呼期間修改要求標頭。</span><span class="sxs-lookup"><span data-stu-id="7d023-491">Note that Windows XP and Vista do not support modifying request headers during this callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-492"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 鏈 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="7d023-492"><span id="WINHTTP_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="winhttp_option_server_cert_chain_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-493">抓取伺服器憑證鏈內容。</span><span class="sxs-lookup"><span data-stu-id="7d023-493">Retrieves the server certification chain context.</span></span> <span data-ttu-id="7d023-494">**WINHTTP \_可以傳遞選項 \_ 伺服器憑證 \_ \_ 鏈 \_ 內容** ，以取得在協商 SSL 連線期間收到的伺服器憑證鏈的憑證 **\_ 鏈 \_ 內容** 重複指標。</span><span class="sxs-lookup"><span data-stu-id="7d023-494">**WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT** can be passed to obtain a duplicated pointer to the **CERT\_CHAIN\_CONTEXT** for a server certificate chain received during a negotiated SSL connection.</span></span> <span data-ttu-id="7d023-495">用戶端必須在[](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)填入緩衝區的傳回 PCCERT \_ 內容指標上呼叫 CertFreeCertificateCoNtext。</span><span class="sxs-lookup"><span data-stu-id="7d023-495">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-496"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="7d023-496"><span id="WINHTTP_OPTION_SERVER_CERT_CONTEXT"></span><span id="winhttp_option_server_cert_context"></span>**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-497">抓取伺服器認證內容。</span><span class="sxs-lookup"><span data-stu-id="7d023-497">Retrieves the server certification context.</span></span> <span data-ttu-id="7d023-498">**WINHTTP \_您可以傳遞選項 \_ 伺服器憑證 \_ \_ 內容** ，以取得在協商 SSL 連線期間收到之伺服器憑證的憑證 [**內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) 重複指標。</span><span class="sxs-lookup"><span data-stu-id="7d023-498">**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT** can be passed to obtain a duplicated pointer to the [**CERT CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) for a server certificate received during a negotiated SSL connection.</span></span> <span data-ttu-id="7d023-499">用戶端必須在[](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)填入緩衝區的傳回 PCCERT \_ 內容指標上呼叫 CertFreeCertificateCoNtext。</span><span class="sxs-lookup"><span data-stu-id="7d023-499">The client must call [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) on the returned PCCERT\_CONTEXT pointer that is filled into the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-500"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**已 \_ 使用 WINHTTP 選項 \_ 伺服器 \_ SPN \_**</span><span class="sxs-lookup"><span data-stu-id="7d023-500"><span id="WINHTTP_OPTION_SERVER_SPN_USED"></span><span id="winhttp_option_server_spn_used"></span>**WINHTTP\_OPTION\_SERVER\_SPN\_USED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-501">取得 WinHTTP 在驗證期間提供給 SSPI 的伺服器伺服器主體名稱。</span><span class="sxs-lookup"><span data-stu-id="7d023-501">Gets the server Server Principal Name that WinHTTP supplied to SSPI during authentication.</span></span> <span data-ttu-id="7d023-502">在驗證失敗之後，這個字串值可以傳遞給 [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-502">This string value can be passed to [**SspiPromptForCredentials**](/windows/desktop/api/sspi/nf-sspi-sspipromptforcredentialsa) after an authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-503"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP \_ 選項 \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="7d023-503"><span id="WINHTTP_OPTION_SPN"></span><span id="winhttp_option_spn"></span>**WINHTTP\_OPTION\_SPN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-504">在建立 Kerberos 或協商 Kerberos 驗證的 SPN (服務主體名稱) 時，包含或移除伺服器埠號碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-504">Includes or removes the server port number when the SPN (service principal name) is built for Kerberos or Negotiate Kerberos authentication.</span></span> <span data-ttu-id="7d023-505">此旗標是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="7d023-505">This flag is one of the following values:</span></span>

| <span data-ttu-id="7d023-506">詞彙</span><span class="sxs-lookup"><span data-stu-id="7d023-506">Term</span></span> | <span data-ttu-id="7d023-507">描述</span><span class="sxs-lookup"><span data-stu-id="7d023-507">Description</span></span> |
|-|-|
| <span data-ttu-id="7d023-508"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP \_ 停用 \_ SPN \_ 伺服器 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="7d023-508"><span id="WINHTTP_DISABLE_SPN_SERVER_PORT"></span><span id="winhttp_disable_spn_server_port"></span>WINHTTP\_DISABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="7d023-509">移除伺服器埠號碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-509">Removes the server port number.</span></span> |
| <span data-ttu-id="7d023-510"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP \_ 啟用 \_ SPN \_ 伺服器 \_ 埠</span><span class="sxs-lookup"><span data-stu-id="7d023-510"><span id="WINHTTP_ENABLE_SPN_SERVER_PORT"></span><span id="winhttp_enable_spn_server_port"></span>WINHTTP\_ENABLE\_SPN\_SERVER\_PORT</span></span> | <span data-ttu-id="7d023-511">包括伺服器埠號碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-511">Includes the server port number.</span></span> |


</dl> </dd> <dt>

<span data-ttu-id="7d023-512"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP \_ 選項 \_ 資料流程 \_ 錯誤碼 \_**</span><span class="sxs-lookup"><span data-stu-id="7d023-512"><span id="WINHTTP_OPTION_STREAM_ERROR_CODE"></span><span id="winhttp_option_stream_error_code"></span>**WINHTTP\_OPTION\_STREAM\_ERROR\_CODE**</span></span>
</dt> <dd> <dl> <dt>


<span data-ttu-id="7d023-513">此選項可在 WinHttp 要求控制碼上進行查詢，並會傳回由 HTTP 資料流程接收的 RST_STREAM 框架所指出的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-513">This option can be queried on a WinHttp request handle, and will return the error code indicated by a RST_STREAM frame received on an HTTP stream.</span></span>



</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-514"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP \_ 選項 \_ TCP \_ 快速 \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="7d023-514"><span id="WINHTTP_OPTION_TCP_FAST_OPEN"></span><span id="winhttp_option_tcp_fast_open"></span>**WINHTTP\_OPTION\_TCP\_FAST\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-515">啟用連接的 TCP Fast Open。</span><span class="sxs-lookup"><span data-stu-id="7d023-515">Enables TCP Fast Open for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-516"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP \_ 選項 \_ TCP \_ KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="7d023-516"><span id="WINHTTP_OPTION_TCP_KEEPALIVE"></span><span id="winhttp_option_tcp_keepalive"></span>**WINHTTP\_OPTION\_TCP\_KEEPALIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-517">您可以在 WinHttp 會話控制碼上設定這個選項，以啟用基礎通訊端上的 TCP 保持連線行為。</span><span class="sxs-lookup"><span data-stu-id="7d023-517">This option can be set on a WinHttp session handle to enable TCP keep-alive behavior on the underlying socket.</span></span> <span data-ttu-id="7d023-518">接受 [**tcp \_ keepalive**](/windows/win32/winsock/sio-keepalive-vals) 結構。</span><span class="sxs-lookup"><span data-stu-id="7d023-518">Takes a [**tcp\_keepalive**](/windows/win32/winsock/sio-keepalive-vals) struct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-519"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP \_ 選項 \_ TLS \_ FALSE \_ START**</span><span class="sxs-lookup"><span data-stu-id="7d023-519"><span id="WINHTTP_OPTION_TLS_FALSE_START"></span><span id="winhttp_option_tls_false_start"></span>**WINHTTP\_OPTION\_TLS\_FALSE\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-520">啟用連接的 TLS False Start。</span><span class="sxs-lookup"><span data-stu-id="7d023-520">Enables TLS False Start for the connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-521"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP \_ 選項 \_ TLS \_ 通訊協定不 \_ 安全 \_ 的回復**</span><span class="sxs-lookup"><span data-stu-id="7d023-521"><span id="WINHTTP_OPTION_TLS_PROTOCOL_INSECURE_FALLBACK"></span><span id="winhttp_option_tls_protocol_insecure_fallback"></span>**WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-522">您可以在 WinHttp 會話控制碼上設定這個選項，以控制如果有較新的通訊協定版本的 TLS 交握失敗，是否允許回溯至 TLS 1.0。</span><span class="sxs-lookup"><span data-stu-id="7d023-522">This option can be set on a WinHttp session handle to control whether fallback to TLS 1.0 is allowed if there is a TLS handshake failure with a newer protocol version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-523"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP \_ 選項 \_ UNLOAD \_ 通知 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="7d023-523"><span id="WINHTTP_OPTION_UNLOAD_NOTIFY_EVENT"></span><span id="winhttp_option_unload_notify_event"></span>**WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-524">取得將在特定會話的最後一個回呼完成時設定的事件。</span><span class="sxs-lookup"><span data-stu-id="7d023-524">Takes an event that will be set when the last callback has completed for a particular session.</span></span> <span data-ttu-id="7d023-525">此旗標必須用於會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-525">This flag must be must be used on a session handle.</span></span> <span data-ttu-id="7d023-526">事件必須等到 WinHTTP 設定後才能關閉。</span><span class="sxs-lookup"><span data-stu-id="7d023-526">The event cannot be closed until after it has been set by WinHTTP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-527"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP \_ 選項 \_ UNSAFE \_ 標頭 \_ 剖析**</span><span class="sxs-lookup"><span data-stu-id="7d023-527"><span id="WINHTTP_OPTION_UNSAFE_HEADER_PARSING"></span><span id="winhttp_option_unsafe_header_parsing"></span>**WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-528">此選項已保留供內部使用，不應該呼叫。</span><span class="sxs-lookup"><span data-stu-id="7d023-528">This option is reserved for internal use and should not be called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-529"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP \_ 選項 \_ 升級 \_ 至 \_ WEB \_ 通訊端**</span><span class="sxs-lookup"><span data-stu-id="7d023-529"><span id="WINHTTP_OPTION_UPGRADE_TO_WEB_SOCKET"></span><span id="winhttp_option_upgrade_to_web_socket"></span>**WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-530">指示堆疊使用 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)啟動 WebSocket 交握處理常式。</span><span class="sxs-lookup"><span data-stu-id="7d023-530">Instructs the stack to start a WebSocket handshake process with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="7d023-531">此選項不會使用任何參數。</span><span class="sxs-lookup"><span data-stu-id="7d023-531">This option takes no parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-532"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP \_ 選項 \_ URL**</span><span class="sxs-lookup"><span data-stu-id="7d023-532"><span id="WINHTTP_OPTION_URL"></span><span id="winhttp_option_url"></span>**WINHTTP\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-533">抓取字串值，其中包含已下載資源的完整 URL。</span><span class="sxs-lookup"><span data-stu-id="7d023-533">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="7d023-534">如果原始 URL 包含任何額外的資料（例如搜尋字串或錨點），或重新導向呼叫，則傳回的 URL 會與原始的 URL 不同。</span><span class="sxs-lookup"><span data-stu-id="7d023-534">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="7d023-535">應用程式應該傳入緩衝區（以位元組為單位），這夠大，足以將傳回的 URL 保存在寬字元中。</span><span class="sxs-lookup"><span data-stu-id="7d023-535">The application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-536"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP \_ 選項 \_ 使用 \_ 全域 \_ 伺服器 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="7d023-536"><span id="WINHTTP_OPTION_USE_GLOBAL_SERVER_CREDENTIALS"></span><span id="winhttp_option_use_global_server_credentials"></span>**WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-537">採用 **BOOL** ，而且只能設定會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-537">Takes a **BOOL** and can be set only a session handle.</span></span> <span data-ttu-id="7d023-538">它只會在設定選項之後，向下傳播至從會話控制碼建立的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7d023-538">It will only propagate down to handles created from the session handle after the option has been set.</span></span> <span data-ttu-id="7d023-539">若 **為 TRUE**，則此選項會導致最後使用從 WinInet 推入的全域伺服器認證。</span><span class="sxs-lookup"><span data-stu-id="7d023-539">If **TRUE**, this option causes as a last resort the use of global server credentials that were pushed down from WinInet.</span></span> <span data-ttu-id="7d023-540">此選項的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7d023-540">The default for this option is **FALSE**.</span></span> <span data-ttu-id="7d023-541">此選項需要登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings！ShareCredsWithWinHttp**。</span><span class="sxs-lookup"><span data-stu-id="7d023-541">This option requires registry key **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Internet Settings!ShareCredsWithWinHttp**.</span></span> <span data-ttu-id="7d023-542">依預設，此登錄機碼不存在。</span><span class="sxs-lookup"><span data-stu-id="7d023-542">This registry key is not present by default.</span></span> <span data-ttu-id="7d023-543">當設定時，WinINet 會將認證傳送至 WinHTTP。</span><span class="sxs-lookup"><span data-stu-id="7d023-543">When it is set, WinINet will send credentials down to WinHTTP.</span></span> <span data-ttu-id="7d023-544">每當 WinHttp 收到驗證挑戰，而且目前的控制碼上沒有設定任何認證時，就會使用 WinINet 提供的認證。</span><span class="sxs-lookup"><span data-stu-id="7d023-544">Whenever WinHttp gets an authentication challenge and if there are no credentials set on the current handle, it will use the credentials provided by WinINet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-545"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP \_ 選項 \_ 使用者 \_ 代理程式**</span><span class="sxs-lookup"><span data-stu-id="7d023-545"><span id="WINHTTP_OPTION_USER_AGENT"></span><span id="winhttp_option_user_agent"></span>**WINHTTP\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-546">設定或抓取 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)提供的控制碼上的 [*使用者代理程式*](glossary.md)字串，並在後續的 [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)函式中使用，但前提是它不是由 [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)或 **WinHttpSendRequest** 所加入的標頭所覆寫。</span><span class="sxs-lookup"><span data-stu-id="7d023-546">Sets or retrieves the [*user agent*](glossary.md) string on handles supplied by [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) and used in subsequent [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) functions, as long as it is not overridden by a header added by [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) or **WinHttpSendRequest**.</span></span> <span data-ttu-id="7d023-547">在抓取使用者代理程式時，應用程式應該傳入緩衝區（以位元組為單位），這夠大，足以將傳回的 URL 保存在寬字元中。</span><span class="sxs-lookup"><span data-stu-id="7d023-547">When retrieving a user agent, the application should pass in a buffer, sized in bytes, that is big enough to hold the returned URL in wide char.</span></span> <span data-ttu-id="7d023-548">設定使用者代理程式時，緩衝區大小是字串的長度（以字元為單位），加上 **Null** 結束字元。</span><span class="sxs-lookup"><span data-stu-id="7d023-548">When setting the user agent, the buffer size is the length of the string, in characters, plus the **NULL** terminator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-549"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP \_ 選項使用者 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="7d023-549"><span id="WINHTTP_OPTION_USERNAME"></span><span id="winhttp_option_username"></span>**WINHTTP\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-550">設定或抓取包含使用者名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="7d023-550">Sets or retrieves a string that contains the user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-551"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 關閉 \_ 超時**</span><span class="sxs-lookup"><span data-stu-id="7d023-551"><span id="WINHTTP_OPTION_WEB_SOCKET_CLOSE_TIMEOUT"></span><span id="winhttp_option_web_socket_close_timeout"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-552">設定 [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) 應該等候才能完成關閉信號交換的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d023-552">Sets the time, in milliseconds, that [**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose) should wait to complete the close handshake.</span></span> <span data-ttu-id="7d023-553">預設值是 10 秒。</span><span class="sxs-lookup"><span data-stu-id="7d023-553">The default is 10 seconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-554"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ KEEPALIVE \_ 間隔**</span><span class="sxs-lookup"><span data-stu-id="7d023-554"><span id="WINHTTP_OPTION_WEB_SOCKET_KEEPALIVE_INTERVAL"></span><span id="winhttp_option_web_socket_keepalive_interval"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-555">設定透過連接傳送 keep-alive 封包的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d023-555">Sets the interval, in milliseconds, to send a keep-alive packet over the connection.</span></span> <span data-ttu-id="7d023-556">預設間隔為 30000 (30 秒) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-556">The default interval is 30000 (30 seconds).</span></span> <span data-ttu-id="7d023-557">最小間隔為 15000 (15 秒) 。</span><span class="sxs-lookup"><span data-stu-id="7d023-557">The minimum interval is 15000 (15 seconds).</span></span> <span data-ttu-id="7d023-558">使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 設定低於15000的值，將會傳回 **錯誤 \_ 不正確 \_ 參數**。</span><span class="sxs-lookup"><span data-stu-id="7d023-558">Using [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) to set a value lower than 15000 will return with **ERROR\_INVALID\_PARAMETER**.</span></span>

> [!Note]
> <span data-ttu-id="7d023-559">**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ KEEPALIVE \_ 間隔** 的預設值是從 **HKLM： \\ SOFTWARE \\ Microsoft \\ WebSocket \\ KeepaliveInterval** 進行讀取。</span><span class="sxs-lookup"><span data-stu-id="7d023-559">The default value for **WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL** is read from **HKLM:\\SOFTWARE\\Microsoft\\WebSocket\\KeepaliveInterval**.</span></span> <span data-ttu-id="7d023-560">如果未設定值，則會使用預設值30000。</span><span class="sxs-lookup"><span data-stu-id="7d023-560">If a value is not set, the default value of 30000 will be used.</span></span> <span data-ttu-id="7d023-561">的 keepalive 間隔不能低於15000毫秒。</span><span class="sxs-lookup"><span data-stu-id="7d023-561">It is not possible to have a lower keepalive interval than 15000 milliseconds.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-562"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 接收 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="7d023-562"><span id="WINHTTP_OPTION_WEB_SOCKET_RECEIVE_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_receive_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-563">設定或抓取 DWORD，以指定要用於 WebSocket 連接的接收緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="7d023-563">Sets or retrieves a DWORD which specifies the receive buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-564"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 傳送 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="7d023-564"><span id="WINHTTP_OPTION_WEB_SOCKET_SEND_BUFFER_SIZE"></span><span id="winhttp_option_web_socket_send_buffer_size"></span>**WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-565">設定或抓取 DWORD，以指定要用於 WebSocket 連接的傳送緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="7d023-565">Sets or retrieves a DWORD which specifies the send buffer size to be used on WebSocket connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-566"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP \_ 選項背景 \_ 工作 \_ 執行緒 \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="7d023-566"><span id="WINHTTP_OPTION_WORKER_THREAD_COUNT"></span><span id="winhttp_option_worker_thread_count"></span>**WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-567">設定不帶正負號的長整數值，指定執行緒集區應用於非同步完成的背景工作執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="7d023-567">Sets an unsigned long integer value that specifies the number of worker threads the thread pool should use for asynchronous completions.</span></span> <span data-ttu-id="7d023-568">此選項的預設值為零，表示工作者執行緒的數目等於系統上的 Cpu 數目。</span><span class="sxs-lookup"><span data-stu-id="7d023-568">The default value of this option is zero, which specifies that the number of worker threads is equal to the number of CPUs on the system.</span></span> <span data-ttu-id="7d023-569">此選項只能在發生非同步作業之前，在 **Null**  [HINTERNET](hinternet-handles-in-winhttp.md) 控制碼上設定。</span><span class="sxs-lookup"><span data-stu-id="7d023-569">This option can only be set on a **NULL**  [HINTERNET](hinternet-handles-in-winhttp.md) handle before an asynchronous operation has occurred.</span></span> <span data-ttu-id="7d023-570">此選項只能設定一次。</span><span class="sxs-lookup"><span data-stu-id="7d023-570">This option can only be set once.</span></span>

<span data-ttu-id="7d023-571">**Windows Server 2008 R2 和 windows 7：** 此旗標已淘汰。</span><span class="sxs-lookup"><span data-stu-id="7d023-571">**Windows Server 2008 R2 and Windows 7:** This flag is obsolete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d023-572"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP \_ 選項 \_ 寫入 \_ 緩衝區 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="7d023-572"><span id="WINHTTP_OPTION_WRITE_BUFFER_SIZE"></span><span id="winhttp_option_write_buffer_size"></span>**WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7d023-573">此選項已被取代;它沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="7d023-573">This option has been deprecated; it has no effect.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d023-574">備註</span><span class="sxs-lookup"><span data-stu-id="7d023-574">Remarks</span></span>

<span data-ttu-id="7d023-575">下表列出選項旗標，方法是指定它們可以處理的控制碼、是否可以查詢和設定，以及使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7d023-575">The following table lists the option flags by specifying which handles they can act upon, whether they can be queried and set, and the data type used.</span></span> <span data-ttu-id="7d023-576">「X」表示選項旗標適用于與函式或控制碼搭配使用，而「-」指定選項旗標無效。</span><span class="sxs-lookup"><span data-stu-id="7d023-576">An "X" indicates that the option flag is valid for use with the function or handle, while a "-" specifies that the option flag is invalid.</span></span>

<span data-ttu-id="7d023-577">如果您嘗試在不支援的 Windows 版本上設定或查詢選項旗標，將會導致 **錯誤 \_ WINHTTP \_ 不正確 \_ 選項**。</span><span class="sxs-lookup"><span data-stu-id="7d023-577">Attempting to set or query an option flag on a Windows version where it is not supported will result in **ERROR\_WINHTTP\_INVALID\_OPTION**.</span></span>

| <span data-ttu-id="7d023-578">選項旗標和資料類型</span><span class="sxs-lookup"><span data-stu-id="7d023-578">Option flag, and data type</span></span> | <span data-ttu-id="7d023-579">會話控制碼</span><span class="sxs-lookup"><span data-stu-id="7d023-579">Session handle</span></span> | <span data-ttu-id="7d023-580">要求控制碼</span><span class="sxs-lookup"><span data-stu-id="7d023-580">Request handle</span></span> | <span data-ttu-id="7d023-581">查詢選項</span><span class="sxs-lookup"><span data-stu-id="7d023-581">Query option</span></span> | <span data-ttu-id="7d023-582">Set 選項</span><span class="sxs-lookup"><span data-stu-id="7d023-582">Set option</span></span> | <span data-ttu-id="7d023-583">最低 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="7d023-583">Minimum Windows Version</span></span> |
|-|-|-|-|-|-|
| <span data-ttu-id="7d023-584">WINHTTP \_ 選項有 \_ 保證 \_ 非 \_ 封鎖 \_ 回呼</span><span class="sxs-lookup"><span data-stu-id="7d023-584">WINHTTP\_OPTION\_ASSURED\_NON\_BLOCKING\_CALLBACKS</span></span><br/><span data-ttu-id="7d023-585">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-585">**BOOL**</span></span> | <span data-ttu-id="7d023-586">X</span><span class="sxs-lookup"><span data-stu-id="7d023-586">X</span></span> | \- | \- | <span data-ttu-id="7d023-587">X</span><span class="sxs-lookup"><span data-stu-id="7d023-587">X</span></span> | \- |
| <span data-ttu-id="7d023-588">WINHTTP \_ 選項 \_ 自動登入 \_ 原則</span><span class="sxs-lookup"><span data-stu-id="7d023-588">WINHTTP\_OPTION\_AUTOLOGON\_POLICY</span></span><br/><span data-ttu-id="7d023-589">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-589">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-590">X</span><span class="sxs-lookup"><span data-stu-id="7d023-590">X</span></span> | \- | <span data-ttu-id="7d023-591">X</span><span class="sxs-lookup"><span data-stu-id="7d023-591">X</span></span> | \- |
| <span data-ttu-id="7d023-592">WINHTTP \_ 選項 \_ 回呼</span><span class="sxs-lookup"><span data-stu-id="7d023-592">WINHTTP\_OPTION\_CALLBACK</span></span><br/><span data-ttu-id="7d023-593">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="7d023-593">**LPVOID**</span></span> | <span data-ttu-id="7d023-594">X</span><span class="sxs-lookup"><span data-stu-id="7d023-594">X</span></span> | <span data-ttu-id="7d023-595">X</span><span class="sxs-lookup"><span data-stu-id="7d023-595">X</span></span> | <span data-ttu-id="7d023-596">X</span><span class="sxs-lookup"><span data-stu-id="7d023-596">X</span></span> | <span data-ttu-id="7d023-597">X</span><span class="sxs-lookup"><span data-stu-id="7d023-597">X</span></span> | \- |
| <span data-ttu-id="7d023-598">WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 內容</span><span class="sxs-lookup"><span data-stu-id="7d023-598">WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="7d023-599">**憑證 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="7d023-599">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="7d023-600">X</span><span class="sxs-lookup"><span data-stu-id="7d023-600">X</span></span> | \- | <span data-ttu-id="7d023-601">X</span><span class="sxs-lookup"><span data-stu-id="7d023-601">X</span></span> | <span data-ttu-id="7d023-602">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d023-602">Windows Vista</span></span> |
| <span data-ttu-id="7d023-603">WINHTTP \_ 選項 \_ 用戶端憑證 \_ \_ 簽發者 \_ 清單</span><span class="sxs-lookup"><span data-stu-id="7d023-603">WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST</span></span><br/>[<span data-ttu-id="7d023-604">**SecPkgCoNtext \_ IssuerListInfoEx**</span><span class="sxs-lookup"><span data-stu-id="7d023-604">**SecPkgContext\_IssuerListInfoEx**</span></span>](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) | \- | <span data-ttu-id="7d023-605">X</span><span class="sxs-lookup"><span data-stu-id="7d023-605">X</span></span> | <span data-ttu-id="7d023-606">X</span><span class="sxs-lookup"><span data-stu-id="7d023-606">X</span></span> | \- | <span data-ttu-id="7d023-607">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d023-607">Windows Vista</span></span> |
| <span data-ttu-id="7d023-608">WINHTTP \_ 選項 \_ 字碼頁</span><span class="sxs-lookup"><span data-stu-id="7d023-608">WINHTTP\_OPTION\_CODEPAGE</span></span><br/><span data-ttu-id="7d023-609">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-609">**DWORD**</span></span> | <span data-ttu-id="7d023-610">X</span><span class="sxs-lookup"><span data-stu-id="7d023-610">X</span></span> | \- | \- | <span data-ttu-id="7d023-611">X</span><span class="sxs-lookup"><span data-stu-id="7d023-611">X</span></span> | \- |
| <span data-ttu-id="7d023-612">WINHTTP \_ 選項 \_ 設定 \_ PASSPORT \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="7d023-612">WINHTTP\_OPTION\_CONFIGURE\_PASSPORT\_AUTH</span></span><br/><span data-ttu-id="7d023-613">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-613">**DWORD**</span></span> | <span data-ttu-id="7d023-614">X</span><span class="sxs-lookup"><span data-stu-id="7d023-614">X</span></span> | \- | \- | <span data-ttu-id="7d023-615">X</span><span class="sxs-lookup"><span data-stu-id="7d023-615">X</span></span> | \- |
| <span data-ttu-id="7d023-616">WINHTTP \_ 選項 \_ 連接 \_ 重試</span><span class="sxs-lookup"><span data-stu-id="7d023-616">WINHTTP\_OPTION\_CONNECT\_RETRIES</span></span><br/><span data-ttu-id="7d023-617">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-617">**DWORD**</span></span> | <span data-ttu-id="7d023-618">X</span><span class="sxs-lookup"><span data-stu-id="7d023-618">X</span></span> | <span data-ttu-id="7d023-619">X</span><span class="sxs-lookup"><span data-stu-id="7d023-619">X</span></span> | <span data-ttu-id="7d023-620">X</span><span class="sxs-lookup"><span data-stu-id="7d023-620">X</span></span> | <span data-ttu-id="7d023-621">X</span><span class="sxs-lookup"><span data-stu-id="7d023-621">X</span></span> | \- |
| <span data-ttu-id="7d023-622">WINHTTP \_ 選項 \_ 連接 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="7d023-622">WINHTTP\_OPTION\_CONNECT\_TIMEOUT</span></span><br/><span data-ttu-id="7d023-623">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-623">**DWORD**</span></span> | <span data-ttu-id="7d023-624">X</span><span class="sxs-lookup"><span data-stu-id="7d023-624">X</span></span> | <span data-ttu-id="7d023-625">X</span><span class="sxs-lookup"><span data-stu-id="7d023-625">X</span></span> | <span data-ttu-id="7d023-626">X</span><span class="sxs-lookup"><span data-stu-id="7d023-626">X</span></span> | <span data-ttu-id="7d023-627">X</span><span class="sxs-lookup"><span data-stu-id="7d023-627">X</span></span> | \- |
| <span data-ttu-id="7d023-628">WINHTTP \_ 選項 \_ 連接 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="7d023-628">WINHTTP\_OPTION\_CONNECTION\_INFO</span></span><br/>[<span data-ttu-id="7d023-629">**WINHTTP \_ 連接 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="7d023-629">**WINHTTP\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info) | \- | <span data-ttu-id="7d023-630">X</span><span class="sxs-lookup"><span data-stu-id="7d023-630">X</span></span> | <span data-ttu-id="7d023-631">X</span><span class="sxs-lookup"><span data-stu-id="7d023-631">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-632">WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V0</span><span class="sxs-lookup"><span data-stu-id="7d023-632">WINHTTP\_OPTION\_CONNECTION\_STATS\_V0</span></span><br/>[<span data-ttu-id="7d023-633">**TCP \_ 資訊 \_ v0**</span><span class="sxs-lookup"><span data-stu-id="7d023-633">**TCP\_INFO\_v0**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0) | \- | <span data-ttu-id="7d023-634">X</span><span class="sxs-lookup"><span data-stu-id="7d023-634">X</span></span> | <span data-ttu-id="7d023-635">X</span><span class="sxs-lookup"><span data-stu-id="7d023-635">X</span></span> | \- | <span data-ttu-id="7d023-636">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="7d023-636">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7d023-637">WINHTTP \_ 選項 \_ 連接 \_ 統計資料 \_ V1</span><span class="sxs-lookup"><span data-stu-id="7d023-637">WINHTTP\_OPTION\_CONNECTION\_STATS\_V1</span></span><br/>[<span data-ttu-id="7d023-638">**TCP \_ 資訊 \_ v1**</span><span class="sxs-lookup"><span data-stu-id="7d023-638">**TCP\_INFO\_v1**</span></span>](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1) | \- | <span data-ttu-id="7d023-639">X</span><span class="sxs-lookup"><span data-stu-id="7d023-639">X</span></span> | <span data-ttu-id="7d023-640">X</span><span class="sxs-lookup"><span data-stu-id="7d023-640">X</span></span> | \- | <span data-ttu-id="7d023-641">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="7d023-641">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7d023-642">WINHTTP \_ 選項 \_ 內容 \_ 值</span><span class="sxs-lookup"><span data-stu-id="7d023-642">WINHTTP\_OPTION\_CONTEXT\_VALUE</span></span><br/><span data-ttu-id="7d023-643">**DWORD \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-643">**DWORD\_PTR**</span></span> | <span data-ttu-id="7d023-644">X</span><span class="sxs-lookup"><span data-stu-id="7d023-644">X</span></span> | <span data-ttu-id="7d023-645">X</span><span class="sxs-lookup"><span data-stu-id="7d023-645">X</span></span> | <span data-ttu-id="7d023-646">X</span><span class="sxs-lookup"><span data-stu-id="7d023-646">X</span></span> | <span data-ttu-id="7d023-647">X</span><span class="sxs-lookup"><span data-stu-id="7d023-647">X</span></span> | \- |
| <span data-ttu-id="7d023-648">WINHTTP \_ 選項 \_ 解壓縮</span><span class="sxs-lookup"><span data-stu-id="7d023-648">WINHTTP\_OPTION\_DECOMPRESSION</span></span><br/><span data-ttu-id="7d023-649">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-649">**DWORD**</span></span> | <span data-ttu-id="7d023-650">X</span><span class="sxs-lookup"><span data-stu-id="7d023-650">X</span></span> | <span data-ttu-id="7d023-651">X</span><span class="sxs-lookup"><span data-stu-id="7d023-651">X</span></span> | \- | <span data-ttu-id="7d023-652">X</span><span class="sxs-lookup"><span data-stu-id="7d023-652">X</span></span> | <span data-ttu-id="7d023-653">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d023-653">Windows 8.1</span></span> |
| <span data-ttu-id="7d023-654">WINHTTP \_ 選項 \_ 停用 \_ 功能</span><span class="sxs-lookup"><span data-stu-id="7d023-654">WINHTTP\_OPTION\_DISABLE\_FEATURE</span></span><br/><span data-ttu-id="7d023-655">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-655">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-656">X</span><span class="sxs-lookup"><span data-stu-id="7d023-656">X</span></span> | \- | <span data-ttu-id="7d023-657">X</span><span class="sxs-lookup"><span data-stu-id="7d023-657">X</span></span> | \- |
| <span data-ttu-id="7d023-658">WINHTTP \_ 選項 \_ 停用 \_ 安全 \_ 通訊協定 \_ 回復</span><span class="sxs-lookup"><span data-stu-id="7d023-658">WINHTTP\_OPTION\_DISABLE\_SECURE\_PROTOCOL\_FALLBACK</span></span><br/><span data-ttu-id="7d023-659">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-659">**BOOL**</span></span> | <span data-ttu-id="7d023-660">X</span><span class="sxs-lookup"><span data-stu-id="7d023-660">X</span></span> | \- | \- | <span data-ttu-id="7d023-661">X</span><span class="sxs-lookup"><span data-stu-id="7d023-661">X</span></span> | <span data-ttu-id="7d023-662">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="7d023-662">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7d023-663">WINHTTP \_ 選項 \_ 停用 \_ 串流 \_ 佇列</span><span class="sxs-lookup"><span data-stu-id="7d023-663">WINHTTP\_OPTION\_DISABLE\_STREAM\_QUEUE</span></span><br/><span data-ttu-id="7d023-664">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-664">**BOOL**</span></span> | <span data-ttu-id="7d023-665">X</span><span class="sxs-lookup"><span data-stu-id="7d023-665">X</span></span> | <span data-ttu-id="7d023-666">X</span><span class="sxs-lookup"><span data-stu-id="7d023-666">X</span></span> | \- | <span data-ttu-id="7d023-667">X</span><span class="sxs-lookup"><span data-stu-id="7d023-667">X</span></span> | <span data-ttu-id="7d023-668">Windows 10 版本1809</span><span class="sxs-lookup"><span data-stu-id="7d023-668">Windows 10 Version 1809</span></span> |
| <span data-ttu-id="7d023-669">WINHTTP \_ 選項 \_ 啟用 \_ 功能</span><span class="sxs-lookup"><span data-stu-id="7d023-669">WINHTTP\_OPTION\_ENABLE\_FEATURE</span></span><br/><span data-ttu-id="7d023-670">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-670">**DWORD**</span></span> | \* | \* | \- | <span data-ttu-id="7d023-671">X</span><span class="sxs-lookup"><span data-stu-id="7d023-671">X</span></span> | \- |
| <span data-ttu-id="7d023-672">WINHTTP \_ 選項 \_ 啟用 \_ HTTP \_ 通訊協定</span><span class="sxs-lookup"><span data-stu-id="7d023-672">WINHTTP\_OPTION\_ENABLE\_HTTP\_PROTOCOL</span></span><br/><span data-ttu-id="7d023-673">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-673">**DWORD**</span></span> | <span data-ttu-id="7d023-674">X</span><span class="sxs-lookup"><span data-stu-id="7d023-674">X</span></span> | <span data-ttu-id="7d023-675">X</span><span class="sxs-lookup"><span data-stu-id="7d023-675">X</span></span> | \- | <span data-ttu-id="7d023-676">X</span><span class="sxs-lookup"><span data-stu-id="7d023-676">X</span></span> | <span data-ttu-id="7d023-677">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="7d023-677">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="7d023-678">WINHTTP \_ 選項 \_ ENABLE \_ HTTP2 \_ PLUS \_ CLIENT \_ CERT \_ CONTEXT</span><span class="sxs-lookup"><span data-stu-id="7d023-678">WINHTTP\_OPTION\_ENABLE\_HTTP2\_PLUS\_CLIENT\_CERT\_CONTEXT</span></span><br/><span data-ttu-id="7d023-679">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-679">**BOOL**</span></span> | <span data-ttu-id="7d023-680">X</span><span class="sxs-lookup"><span data-stu-id="7d023-680">X</span></span> | \- | \- | <span data-ttu-id="7d023-681">X</span><span class="sxs-lookup"><span data-stu-id="7d023-681">X</span></span> | <span data-ttu-id="7d023-682">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="7d023-682">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7d023-683">WINHTTP \_ 選項 \_ ENABLETRACING</span><span class="sxs-lookup"><span data-stu-id="7d023-683">WINHTTP\_OPTION\_ENABLETRACING</span></span><br/><span data-ttu-id="7d023-684">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-684">**DWORD**</span></span> | \- | \- | <span data-ttu-id="7d023-685">X</span><span class="sxs-lookup"><span data-stu-id="7d023-685">X</span></span> | <span data-ttu-id="7d023-686">X</span><span class="sxs-lookup"><span data-stu-id="7d023-686">X</span></span> | \- |
| <span data-ttu-id="7d023-687">WINHTTP \_ 選項 \_ 編碼 \_ 額外</span><span class="sxs-lookup"><span data-stu-id="7d023-687">WINHTTP\_OPTION\_ENCODE\_EXTRA</span></span><br/><span data-ttu-id="7d023-688">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-688">**BOOL**</span></span> | <span data-ttu-id="7d023-689">X</span><span class="sxs-lookup"><span data-stu-id="7d023-689">X</span></span> | <span data-ttu-id="7d023-690">X</span><span class="sxs-lookup"><span data-stu-id="7d023-690">X</span></span> | \- | <span data-ttu-id="7d023-691">X</span><span class="sxs-lookup"><span data-stu-id="7d023-691">X</span></span> | <span data-ttu-id="7d023-692">Windows 10 版本1803</span><span class="sxs-lookup"><span data-stu-id="7d023-692">Windows 10 Version 1803</span></span> |
| <span data-ttu-id="7d023-693">WINHTTP \_ 選項 \_ 到期 \_ 連接</span><span class="sxs-lookup"><span data-stu-id="7d023-693">WINHTTP\_OPTION\_EXPIRE\_CONNECTION</span></span><br/><span data-ttu-id="7d023-694">N/A</span><span class="sxs-lookup"><span data-stu-id="7d023-694">N/A</span></span> | \- | <span data-ttu-id="7d023-695">X</span><span class="sxs-lookup"><span data-stu-id="7d023-695">X</span></span> | \- | <span data-ttu-id="7d023-696">X</span><span class="sxs-lookup"><span data-stu-id="7d023-696">X</span></span> | <span data-ttu-id="7d023-697">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="7d023-697">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7d023-698">WINHTTP \_ 選項 \_ 延伸 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="7d023-698">WINHTTP\_OPTION\_EXTENDED\_ERROR</span></span><br/><span data-ttu-id="7d023-699">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-699">**DWORD**</span></span> | <span data-ttu-id="7d023-700">X</span><span class="sxs-lookup"><span data-stu-id="7d023-700">X</span></span> | <span data-ttu-id="7d023-701">X</span><span class="sxs-lookup"><span data-stu-id="7d023-701">X</span></span> | <span data-ttu-id="7d023-702">X</span><span class="sxs-lookup"><span data-stu-id="7d023-702">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-703">WINHTTP \_ 選項 \_ 全域 \_ PROXY \_ 認證</span><span class="sxs-lookup"><span data-stu-id="7d023-703">WINHTTP\_OPTION\_GLOBAL\_PROXY\_CREDS</span></span><br/>[<span data-ttu-id="7d023-704">**WINHTTP \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="7d023-704">**WINHTTP\_CREDS**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds) | <span data-ttu-id="7d023-705">X</span><span class="sxs-lookup"><span data-stu-id="7d023-705">X</span></span> | <span data-ttu-id="7d023-706">X</span><span class="sxs-lookup"><span data-stu-id="7d023-706">X</span></span> | \- | <span data-ttu-id="7d023-707">X</span><span class="sxs-lookup"><span data-stu-id="7d023-707">X</span></span> | \- |
| <span data-ttu-id="7d023-708">WINHTTP \_ 選項 \_ 全域 \_ 伺服器 \_ 認證</span><span class="sxs-lookup"><span data-stu-id="7d023-708">WINHTTP\_OPTION\_GLOBAL\_SERVER\_CREDS</span></span><br/>[<span data-ttu-id="7d023-709">**WINHTTP \_ 認證 \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="7d023-709">**WINHTTP\_CREDS\_EX**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) | <span data-ttu-id="7d023-710">X</span><span class="sxs-lookup"><span data-stu-id="7d023-710">X</span></span> | <span data-ttu-id="7d023-711">X</span><span class="sxs-lookup"><span data-stu-id="7d023-711">X</span></span> | \- | <span data-ttu-id="7d023-712">X</span><span class="sxs-lookup"><span data-stu-id="7d023-712">X</span></span> | \- |
| <span data-ttu-id="7d023-713">WINHTTP \_ 選項 \_ 控制碼 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="7d023-713">WINHTTP\_OPTION\_HANDLE\_TYPE</span></span><br/><span data-ttu-id="7d023-714">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-714">**DWORD**</span></span> | <span data-ttu-id="7d023-715">X</span><span class="sxs-lookup"><span data-stu-id="7d023-715">X</span></span> | <span data-ttu-id="7d023-716">X</span><span class="sxs-lookup"><span data-stu-id="7d023-716">X</span></span> | <span data-ttu-id="7d023-717">X</span><span class="sxs-lookup"><span data-stu-id="7d023-717">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-718">\_需要 WINHTTP 選項 \_ HTTP \_ 通訊協定 \_</span><span class="sxs-lookup"><span data-stu-id="7d023-718">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_REQUIRED</span></span><br/><span data-ttu-id="7d023-719">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-719">**BOOL**</span></span> | <span data-ttu-id="7d023-720">X</span><span class="sxs-lookup"><span data-stu-id="7d023-720">X</span></span> | <span data-ttu-id="7d023-721">X</span><span class="sxs-lookup"><span data-stu-id="7d023-721">X</span></span> | \- | <span data-ttu-id="7d023-722">X</span><span class="sxs-lookup"><span data-stu-id="7d023-722">X</span></span> | <span data-ttu-id="7d023-723">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="7d023-723">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7d023-724">使用的 WINHTTP \_ 選項 \_ HTTP \_ 通訊協定 \_</span><span class="sxs-lookup"><span data-stu-id="7d023-724">WINHTTP\_OPTION\_HTTP\_PROTOCOL\_USED</span></span><br/><span data-ttu-id="7d023-725">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-725">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-726">X</span><span class="sxs-lookup"><span data-stu-id="7d023-726">X</span></span> | <span data-ttu-id="7d023-727">X</span><span class="sxs-lookup"><span data-stu-id="7d023-727">X</span></span> | \- | <span data-ttu-id="7d023-728">Windows 10 版本 1607</span><span class="sxs-lookup"><span data-stu-id="7d023-728">Windows 10 Version 1607</span></span> |
| <span data-ttu-id="7d023-729">WINHTTP \_ 選項 \_ HTTP \_ 版本</span><span class="sxs-lookup"><span data-stu-id="7d023-729">WINHTTP\_OPTION\_HTTP\_VERSION</span></span><br/>[<span data-ttu-id="7d023-730">**HTTP \_ 版本 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="7d023-730">**HTTP\_VERSION\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-http_version_info) | <span data-ttu-id="7d023-731">X</span><span class="sxs-lookup"><span data-stu-id="7d023-731">X</span></span> | <span data-ttu-id="7d023-732">X</span><span class="sxs-lookup"><span data-stu-id="7d023-732">X</span></span> | <span data-ttu-id="7d023-733">X</span><span class="sxs-lookup"><span data-stu-id="7d023-733">X</span></span> | <span data-ttu-id="7d023-734">X</span><span class="sxs-lookup"><span data-stu-id="7d023-734">X</span></span> | \- |
| <span data-ttu-id="7d023-735">WINHTTP \_ 選項 \_ HTTP2 \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="7d023-735">WINHTTP\_OPTION\_HTTP2\_KEEPALIVE</span></span><br/><span data-ttu-id="7d023-736">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-736">**DWORD**</span></span> | <span data-ttu-id="7d023-737">X</span><span class="sxs-lookup"><span data-stu-id="7d023-737">X</span></span> | \- | \- | <span data-ttu-id="7d023-738">X</span><span class="sxs-lookup"><span data-stu-id="7d023-738">X</span></span> | <span data-ttu-id="7d023-739">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="7d023-739">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7d023-740">WINHTTP \_ 選項 \_ HTTP2 \_ PLUS \_ 傳輸 \_ 編碼</span><span class="sxs-lookup"><span data-stu-id="7d023-740">WINHTTP\_OPTION\_HTTP2\_PLUS\_TRANSFER\_ENCODING</span></span><br/><span data-ttu-id="7d023-741">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-741">**BOOL**</span></span> | <span data-ttu-id="7d023-742">X</span><span class="sxs-lookup"><span data-stu-id="7d023-742">X</span></span> | <span data-ttu-id="7d023-743">X</span><span class="sxs-lookup"><span data-stu-id="7d023-743">X</span></span> | \- | <span data-ttu-id="7d023-744">X</span><span class="sxs-lookup"><span data-stu-id="7d023-744">X</span></span> | <span data-ttu-id="7d023-745">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="7d023-745">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7d023-746">WINHTTP \_ 選項會 \_ 離線略過憑證 \_ \_ 撤銷 \_</span><span class="sxs-lookup"><span data-stu-id="7d023-746">WINHTTP\_OPTION\_IGNORE\_CERT\_REVOCATION\_OFFLINE</span></span><br/><span data-ttu-id="7d023-747">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-747">**BOOL**</span></span> | \- | <span data-ttu-id="7d023-748">X</span><span class="sxs-lookup"><span data-stu-id="7d023-748">X</span></span> | \- | <span data-ttu-id="7d023-749">X</span><span class="sxs-lookup"><span data-stu-id="7d023-749">X</span></span> | <span data-ttu-id="7d023-750">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="7d023-750">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7d023-751">WINHTTP \_ OPTION \_ IPV6 \_ FAST \_ FALLBACK</span><span class="sxs-lookup"><span data-stu-id="7d023-751">WINHTTP\_OPTION\_IPV6\_FAST\_FALLBACK</span></span><br/><span data-ttu-id="7d023-752">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-752">**BOOL**</span></span> | <span data-ttu-id="7d023-753">X</span><span class="sxs-lookup"><span data-stu-id="7d023-753">X</span></span> | \- | \- | <span data-ttu-id="7d023-754">X</span><span class="sxs-lookup"><span data-stu-id="7d023-754">X</span></span> | <span data-ttu-id="7d023-755">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="7d023-755">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7d023-756">WINHTTP \_ 選項 \_ 為 \_ PROXY \_ CONNECT \_ 回應</span><span class="sxs-lookup"><span data-stu-id="7d023-756">WINHTTP\_OPTION\_IS\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="7d023-757">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-757">**BOOL**</span></span> | <span data-ttu-id="7d023-758">X</span><span class="sxs-lookup"><span data-stu-id="7d023-758">X</span></span> | <span data-ttu-id="7d023-759">X</span><span class="sxs-lookup"><span data-stu-id="7d023-759">X</span></span> | <span data-ttu-id="7d023-760">X</span><span class="sxs-lookup"><span data-stu-id="7d023-760">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-761">\_ \_ \_ \_ 每 \_ 1 \_ 0 部 \_ 伺服器的 WINHTTP 選項 MAX CONNS</span><span class="sxs-lookup"><span data-stu-id="7d023-761">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER</span></span><br/><span data-ttu-id="7d023-762">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-762">**DWORD**</span></span> | <span data-ttu-id="7d023-763">X</span><span class="sxs-lookup"><span data-stu-id="7d023-763">X</span></span> | \- | <span data-ttu-id="7d023-764">X</span><span class="sxs-lookup"><span data-stu-id="7d023-764">X</span></span> | <span data-ttu-id="7d023-765">X</span><span class="sxs-lookup"><span data-stu-id="7d023-765">X</span></span> | \- |
| <span data-ttu-id="7d023-766">每一伺服器的 WINHTTP \_ 選項 \_ MAX \_ CONNS \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d023-766">WINHTTP\_OPTION\_MAX\_CONNS\_PER\_SERVER</span></span><br/><span data-ttu-id="7d023-767">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-767">**DWORD**</span></span> | <span data-ttu-id="7d023-768">X</span><span class="sxs-lookup"><span data-stu-id="7d023-768">X</span></span> | \- | <span data-ttu-id="7d023-769">X</span><span class="sxs-lookup"><span data-stu-id="7d023-769">X</span></span> | <span data-ttu-id="7d023-770">X</span><span class="sxs-lookup"><span data-stu-id="7d023-770">X</span></span> | \- |
| <span data-ttu-id="7d023-771">WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 自動重新 \_ 導向</span><span class="sxs-lookup"><span data-stu-id="7d023-771">WINHTTP\_OPTION\_MAX\_HTTP\_AUTOMATIC\_REDIRECTS</span></span><br/><span data-ttu-id="7d023-772">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-772">**DWORD**</span></span> | <span data-ttu-id="7d023-773">X</span><span class="sxs-lookup"><span data-stu-id="7d023-773">X</span></span> | <span data-ttu-id="7d023-774">X</span><span class="sxs-lookup"><span data-stu-id="7d023-774">X</span></span> | <span data-ttu-id="7d023-775">X</span><span class="sxs-lookup"><span data-stu-id="7d023-775">X</span></span> | <span data-ttu-id="7d023-776">X</span><span class="sxs-lookup"><span data-stu-id="7d023-776">X</span></span> | \- |
| <span data-ttu-id="7d023-777">WINHTTP \_ 選項 \_ 最大 \_ HTTP \_ 狀態 \_ 繼續</span><span class="sxs-lookup"><span data-stu-id="7d023-777">WINHTTP\_OPTION\_MAX\_HTTP\_STATUS\_CONTINUE</span></span><br/><span data-ttu-id="7d023-778">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-778">**DWORD**</span></span> | <span data-ttu-id="7d023-779">X</span><span class="sxs-lookup"><span data-stu-id="7d023-779">X</span></span> | <span data-ttu-id="7d023-780">X</span><span class="sxs-lookup"><span data-stu-id="7d023-780">X</span></span> | <span data-ttu-id="7d023-781">X</span><span class="sxs-lookup"><span data-stu-id="7d023-781">X</span></span> | <span data-ttu-id="7d023-782">X</span><span class="sxs-lookup"><span data-stu-id="7d023-782">X</span></span> | \- |
| <span data-ttu-id="7d023-783">WINHTTP \_ 選項 \_ \_ 回應 \_ 清空最 \_ 大值</span><span class="sxs-lookup"><span data-stu-id="7d023-783">WINHTTP\_OPTION\_MAX\_RESPONSE\_DRAIN\_SIZE</span></span><br/><span data-ttu-id="7d023-784">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-784">**DWORD**</span></span> | <span data-ttu-id="7d023-785">X</span><span class="sxs-lookup"><span data-stu-id="7d023-785">X</span></span> | <span data-ttu-id="7d023-786">X</span><span class="sxs-lookup"><span data-stu-id="7d023-786">X</span></span> | <span data-ttu-id="7d023-787">X</span><span class="sxs-lookup"><span data-stu-id="7d023-787">X</span></span> | <span data-ttu-id="7d023-788">X</span><span class="sxs-lookup"><span data-stu-id="7d023-788">X</span></span> | \- |
| <span data-ttu-id="7d023-789">WINHTTP \_ 選項 \_ 的 \_ 回應 \_ 標頭 \_ 大小上限</span><span class="sxs-lookup"><span data-stu-id="7d023-789">WINHTTP\_OPTION\_MAX\_RESPONSE\_HEADER\_SIZE</span></span><br/><span data-ttu-id="7d023-790">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-790">**DWORD**</span></span> | <span data-ttu-id="7d023-791">X</span><span class="sxs-lookup"><span data-stu-id="7d023-791">X</span></span> | <span data-ttu-id="7d023-792">X</span><span class="sxs-lookup"><span data-stu-id="7d023-792">X</span></span> | <span data-ttu-id="7d023-793">X</span><span class="sxs-lookup"><span data-stu-id="7d023-793">X</span></span> | <span data-ttu-id="7d023-794">X</span><span class="sxs-lookup"><span data-stu-id="7d023-794">X</span></span> | \- |
| <span data-ttu-id="7d023-795">WINHTTP \_ 選項 \_ 父 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="7d023-795">WINHTTP\_OPTION\_PARENT\_HANDLE</span></span><br/>[<span data-ttu-id="7d023-796">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="7d023-796">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="7d023-797">X</span><span class="sxs-lookup"><span data-stu-id="7d023-797">X</span></span> | <span data-ttu-id="7d023-798">X</span><span class="sxs-lookup"><span data-stu-id="7d023-798">X</span></span> | <span data-ttu-id="7d023-799">X</span><span class="sxs-lookup"><span data-stu-id="7d023-799">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-800">WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ 文字</span><span class="sxs-lookup"><span data-stu-id="7d023-800">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_TEXT</span></span><br/><span data-ttu-id="7d023-801">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-801">**LPWSTR**</span></span> | \- | <span data-ttu-id="7d023-802">X</span><span class="sxs-lookup"><span data-stu-id="7d023-802">X</span></span> | <span data-ttu-id="7d023-803">X</span><span class="sxs-lookup"><span data-stu-id="7d023-803">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-804">WINHTTP \_ 選項 \_ PASSPORT \_ COBRANDING \_ URL</span><span class="sxs-lookup"><span data-stu-id="7d023-804">WINHTTP\_OPTION\_PASSPORT\_COBRANDING\_URL</span></span><br/><span data-ttu-id="7d023-805">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-805">**LPWSTR**</span></span> | \- | <span data-ttu-id="7d023-806">X</span><span class="sxs-lookup"><span data-stu-id="7d023-806">X</span></span> | <span data-ttu-id="7d023-807">X</span><span class="sxs-lookup"><span data-stu-id="7d023-807">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-808">WINHTTP \_ 選項 \_ PASSPORT \_ RETURN \_ URL</span><span class="sxs-lookup"><span data-stu-id="7d023-808">WINHTTP\_OPTION\_PASSPORT\_RETURN\_URL</span></span><br/><span data-ttu-id="7d023-809">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="7d023-809">**LPVOID**</span></span> | \- | <span data-ttu-id="7d023-810">X</span><span class="sxs-lookup"><span data-stu-id="7d023-810">X</span></span> | <span data-ttu-id="7d023-811">X</span><span class="sxs-lookup"><span data-stu-id="7d023-811">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-812">WINHTTP \_ 選項 \_ PASSPORT \_ 登出 \_</span><span class="sxs-lookup"><span data-stu-id="7d023-812">WINHTTP\_OPTION\_PASSPORT\_SIGN\_OUT</span></span><br/><span data-ttu-id="7d023-813">**LPVOID**</span><span class="sxs-lookup"><span data-stu-id="7d023-813">**LPVOID**</span></span> | <span data-ttu-id="7d023-814">X</span><span class="sxs-lookup"><span data-stu-id="7d023-814">X</span></span> | \- | \- | <span data-ttu-id="7d023-815">X</span><span class="sxs-lookup"><span data-stu-id="7d023-815">X</span></span> | \- |
| <span data-ttu-id="7d023-816">WINHTTP \_ 選項 \_ 密碼</span><span class="sxs-lookup"><span data-stu-id="7d023-816">WINHTTP\_OPTION\_PASSWORD</span></span><br/><span data-ttu-id="7d023-817">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-817">**LPWSTR**</span></span> | \- | <span data-ttu-id="7d023-818">X</span><span class="sxs-lookup"><span data-stu-id="7d023-818">X</span></span> | <span data-ttu-id="7d023-819">X</span><span class="sxs-lookup"><span data-stu-id="7d023-819">X</span></span> | <span data-ttu-id="7d023-820">X</span><span class="sxs-lookup"><span data-stu-id="7d023-820">X</span></span> | \- |
| <span data-ttu-id="7d023-821">WINHTTP \_ 選項 \_ PROXY</span><span class="sxs-lookup"><span data-stu-id="7d023-821">WINHTTP\_OPTION\_PROXY</span></span><br/>[<span data-ttu-id="7d023-822">**WINHTTP \_ PROXY \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="7d023-822">**WINHTTP\_PROXY\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) | <span data-ttu-id="7d023-823">X</span><span class="sxs-lookup"><span data-stu-id="7d023-823">X</span></span> | <span data-ttu-id="7d023-824">X</span><span class="sxs-lookup"><span data-stu-id="7d023-824">X</span></span> | <span data-ttu-id="7d023-825">X</span><span class="sxs-lookup"><span data-stu-id="7d023-825">X</span></span> | <span data-ttu-id="7d023-826">X</span><span class="sxs-lookup"><span data-stu-id="7d023-826">X</span></span> | \- |
| <span data-ttu-id="7d023-827">WINHTTP \_ 選項 \_ PROXY \_ 密碼</span><span class="sxs-lookup"><span data-stu-id="7d023-827">WINHTTP\_OPTION\_PROXY\_PASSWORD</span></span><br/><span data-ttu-id="7d023-828">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-828">**LPWSTR**</span></span> | \- | <span data-ttu-id="7d023-829">X</span><span class="sxs-lookup"><span data-stu-id="7d023-829">X</span></span> | <span data-ttu-id="7d023-830">X</span><span class="sxs-lookup"><span data-stu-id="7d023-830">X</span></span> | <span data-ttu-id="7d023-831">X</span><span class="sxs-lookup"><span data-stu-id="7d023-831">X</span></span> | \- |
| <span data-ttu-id="7d023-832">已 \_ 使用 WINHTTP 選項 \_ PROXY \_ SPN \_</span><span class="sxs-lookup"><span data-stu-id="7d023-832">WINHTTP\_OPTION\_PROXY\_SPN\_USED</span></span><br/><span data-ttu-id="7d023-833">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-833">**LPWSTR**</span></span> | \- | <span data-ttu-id="7d023-834">X</span><span class="sxs-lookup"><span data-stu-id="7d023-834">X</span></span> | <span data-ttu-id="7d023-835">X</span><span class="sxs-lookup"><span data-stu-id="7d023-835">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-836">WINHTTP \_ 選項 \_ PROXY 使用者 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="7d023-836">WINHTTP\_OPTION\_PROXY\_USERNAME</span></span><br/><span data-ttu-id="7d023-837">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-837">**LPWSTR**</span></span> | \- | <span data-ttu-id="7d023-838">X</span><span class="sxs-lookup"><span data-stu-id="7d023-838">X</span></span> | <span data-ttu-id="7d023-839">X</span><span class="sxs-lookup"><span data-stu-id="7d023-839">X</span></span> | <span data-ttu-id="7d023-840">X</span><span class="sxs-lookup"><span data-stu-id="7d023-840">X</span></span> | \- |
| <span data-ttu-id="7d023-841">WINHTTP \_ 選項 \_ 讀取 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="7d023-841">WINHTTP\_OPTION\_READ\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="7d023-842">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-842">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-843">X</span><span class="sxs-lookup"><span data-stu-id="7d023-843">X</span></span> | <span data-ttu-id="7d023-844">X</span><span class="sxs-lookup"><span data-stu-id="7d023-844">X</span></span> | <span data-ttu-id="7d023-845">X</span><span class="sxs-lookup"><span data-stu-id="7d023-845">X</span></span> | \- |
| <span data-ttu-id="7d023-846">WINHTTP \_ 選項 \_ 接收 \_ PROXY \_ CONNECT \_ 回應</span><span class="sxs-lookup"><span data-stu-id="7d023-846">WINHTTP\_OPTION\_RECEIVE\_PROXY\_CONNECT\_RESPONSE</span></span><br/><span data-ttu-id="7d023-847">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-847">**BOOL**</span></span> | <span data-ttu-id="7d023-848">X</span><span class="sxs-lookup"><span data-stu-id="7d023-848">X</span></span> | <span data-ttu-id="7d023-849">X</span><span class="sxs-lookup"><span data-stu-id="7d023-849">X</span></span> | \- | <span data-ttu-id="7d023-850">X</span><span class="sxs-lookup"><span data-stu-id="7d023-850">X</span></span> | \- |
| <span data-ttu-id="7d023-851">WINHTTP \_ 選項 \_ 接收 \_ 回應 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="7d023-851">WINHTTP\_OPTION\_RECEIVE\_RESPONSE\_TIMEOUT</span></span><br/><span data-ttu-id="7d023-852">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-852">**DWORD**</span></span> | <span data-ttu-id="7d023-853">X</span><span class="sxs-lookup"><span data-stu-id="7d023-853">X</span></span> | <span data-ttu-id="7d023-854">X</span><span class="sxs-lookup"><span data-stu-id="7d023-854">X</span></span> | <span data-ttu-id="7d023-855">X</span><span class="sxs-lookup"><span data-stu-id="7d023-855">X</span></span> | <span data-ttu-id="7d023-856">X</span><span class="sxs-lookup"><span data-stu-id="7d023-856">X</span></span> | \- |
| <span data-ttu-id="7d023-857">WINHTTP \_ 選項 \_ 接收 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="7d023-857">WINHTTP\_OPTION\_RECEIVE\_TIMEOUT</span></span><br/><span data-ttu-id="7d023-858">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-858">**DWORD**</span></span> | <span data-ttu-id="7d023-859">X</span><span class="sxs-lookup"><span data-stu-id="7d023-859">X</span></span> | <span data-ttu-id="7d023-860">X</span><span class="sxs-lookup"><span data-stu-id="7d023-860">X</span></span> | <span data-ttu-id="7d023-861">X</span><span class="sxs-lookup"><span data-stu-id="7d023-861">X</span></span> | <span data-ttu-id="7d023-862">X</span><span class="sxs-lookup"><span data-stu-id="7d023-862">X</span></span> | \- |
| <span data-ttu-id="7d023-863">WINHTTP \_ 選項重新 \_ 導向 \_ 原則</span><span class="sxs-lookup"><span data-stu-id="7d023-863">WINHTTP\_OPTION\_REDIRECT\_POLICY</span></span><br/><span data-ttu-id="7d023-864">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-864">**DWORD**</span></span> | <span data-ttu-id="7d023-865">X</span><span class="sxs-lookup"><span data-stu-id="7d023-865">X</span></span> | <span data-ttu-id="7d023-866">X</span><span class="sxs-lookup"><span data-stu-id="7d023-866">X</span></span> | <span data-ttu-id="7d023-867">X</span><span class="sxs-lookup"><span data-stu-id="7d023-867">X</span></span> | <span data-ttu-id="7d023-868">X</span><span class="sxs-lookup"><span data-stu-id="7d023-868">X</span></span> | \- |
| <span data-ttu-id="7d023-869">WINHTTP \_ 選項 \_ 拒絕 \_ \_ URL 中的 USERPWD \_</span><span class="sxs-lookup"><span data-stu-id="7d023-869">WINHTTP\_OPTION\_REJECT\_USERPWD\_IN\_URL</span></span><br/><span data-ttu-id="7d023-870">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-870">**BOOL**</span></span> | \- | <span data-ttu-id="7d023-871">X</span><span class="sxs-lookup"><span data-stu-id="7d023-871">X</span></span> | \- | <span data-ttu-id="7d023-872">X</span><span class="sxs-lookup"><span data-stu-id="7d023-872">X</span></span> | \- |
| <span data-ttu-id="7d023-873">WINHTTP \_ 選項 \_ 要求 \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="7d023-873">WINHTTP\_OPTION\_REQUEST\_PRIORITY</span></span><br/><span data-ttu-id="7d023-874">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-874">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-875">X</span><span class="sxs-lookup"><span data-stu-id="7d023-875">X</span></span> | <span data-ttu-id="7d023-876">X</span><span class="sxs-lookup"><span data-stu-id="7d023-876">X</span></span> | <span data-ttu-id="7d023-877">X</span><span class="sxs-lookup"><span data-stu-id="7d023-877">X</span></span> | \- |
| <span data-ttu-id="7d023-878">WINHTTP \_ 選項 \_ 要求 \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="7d023-878">WINHTTP\_OPTION\_REQUEST\_STATS</span></span><br/>[<span data-ttu-id="7d023-879">**WINHTTP \_ 要求 \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="7d023-879">**WINHTTP\_REQUEST\_STATS**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats) | \- | <span data-ttu-id="7d023-880">X</span><span class="sxs-lookup"><span data-stu-id="7d023-880">X</span></span> | <span data-ttu-id="7d023-881">X</span><span class="sxs-lookup"><span data-stu-id="7d023-881">X</span></span> | \- | <span data-ttu-id="7d023-882">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="7d023-882">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7d023-883">WINHTTP \_ 選項 \_ 要求 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="7d023-883">WINHTTP\_OPTION\_REQUEST\_TIMES</span></span><br/>[<span data-ttu-id="7d023-884">**WINHTTP \_ 要求 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="7d023-884">**WINHTTP\_REQUEST\_TIMES**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times) | \- | <span data-ttu-id="7d023-885">X</span><span class="sxs-lookup"><span data-stu-id="7d023-885">X</span></span> | <span data-ttu-id="7d023-886">X</span><span class="sxs-lookup"><span data-stu-id="7d023-886">X</span></span> | \- | <span data-ttu-id="7d023-887">Windows 10 版本1903</span><span class="sxs-lookup"><span data-stu-id="7d023-887">Windows 10 Version 1903</span></span> |
| <span data-ttu-id="7d023-888">WINHTTP \_ 選項 \_ 需要 \_ STREAM \_ END</span><span class="sxs-lookup"><span data-stu-id="7d023-888">WINHTTP\_OPTION\_REQUIRE\_STREAM\_END</span></span><br/><span data-ttu-id="7d023-889">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-889">**BOOL**</span></span> | <span data-ttu-id="7d023-890">X</span><span class="sxs-lookup"><span data-stu-id="7d023-890">X</span></span> | <span data-ttu-id="7d023-891">X</span><span class="sxs-lookup"><span data-stu-id="7d023-891">X</span></span> | \- | <span data-ttu-id="7d023-892">X</span><span class="sxs-lookup"><span data-stu-id="7d023-892">X</span></span> | <span data-ttu-id="7d023-893">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="7d023-893">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7d023-894">WINHTTP \_ 選項 \_ 解析 \_ 主機名稱</span><span class="sxs-lookup"><span data-stu-id="7d023-894">WINHTTP\_OPTION\_RESOLUTION\_HOSTNAME</span></span><br/><span data-ttu-id="7d023-895">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-895">**LPWSTR**</span></span> | \- | <span data-ttu-id="7d023-896">X</span><span class="sxs-lookup"><span data-stu-id="7d023-896">X</span></span> | \- | <span data-ttu-id="7d023-897">X</span><span class="sxs-lookup"><span data-stu-id="7d023-897">X</span></span> | <span data-ttu-id="7d023-898">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="7d023-898">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7d023-899">WINHTTP \_ 選項 \_ 解析 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="7d023-899">WINHTTP\_OPTION\_RESOLVE\_TIMEOUT</span></span><br/><span data-ttu-id="7d023-900">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-900">**DWORD**</span></span> | <span data-ttu-id="7d023-901">X</span><span class="sxs-lookup"><span data-stu-id="7d023-901">X</span></span> | <span data-ttu-id="7d023-902">X</span><span class="sxs-lookup"><span data-stu-id="7d023-902">X</span></span> | <span data-ttu-id="7d023-903">X</span><span class="sxs-lookup"><span data-stu-id="7d023-903">X</span></span> | <span data-ttu-id="7d023-904">X</span><span class="sxs-lookup"><span data-stu-id="7d023-904">X</span></span> | \- |
| <span data-ttu-id="7d023-905">WINHTTP \_ 選項 \_ 安全 \_ 通訊協定</span><span class="sxs-lookup"><span data-stu-id="7d023-905">WINHTTP\_OPTION\_SECURE\_PROTOCOLS</span></span><br/><span data-ttu-id="7d023-906">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-906">**DWORD**</span></span> | <span data-ttu-id="7d023-907">X</span><span class="sxs-lookup"><span data-stu-id="7d023-907">X</span></span> | \- | \- | <span data-ttu-id="7d023-908">X</span><span class="sxs-lookup"><span data-stu-id="7d023-908">X</span></span> | \- |
| <span data-ttu-id="7d023-909">WINHTTP \_ 選項 \_ 安全性 \_ 憑證 \_ 結構</span><span class="sxs-lookup"><span data-stu-id="7d023-909">WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT</span></span><br/>[<span data-ttu-id="7d023-910">**WINHTTP \_ 憑證 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="7d023-910">**WINHTTP\_CERTIFICATE\_INFO**</span></span>](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) | \- | <span data-ttu-id="7d023-911">X</span><span class="sxs-lookup"><span data-stu-id="7d023-911">X</span></span> | <span data-ttu-id="7d023-912">X</span><span class="sxs-lookup"><span data-stu-id="7d023-912">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-913">WINHTTP \_ 選項 \_ 安全性 \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="7d023-913">WINHTTP\_OPTION\_SECURITY\_FLAGS</span></span><br/><span data-ttu-id="7d023-914">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-914">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-915">X</span><span class="sxs-lookup"><span data-stu-id="7d023-915">X</span></span> | <span data-ttu-id="7d023-916">X</span><span class="sxs-lookup"><span data-stu-id="7d023-916">X</span></span> | <span data-ttu-id="7d023-917">X</span><span class="sxs-lookup"><span data-stu-id="7d023-917">X</span></span> | \- |
| <span data-ttu-id="7d023-918">WINHTTP \_ 選項 \_ 安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="7d023-918">WINHTTP\_OPTION\_SECURITY\_INFO</span></span><br/>[<span data-ttu-id="7d023-919">**WINHTTP_SECURITY_INFO**</span><span class="sxs-lookup"><span data-stu-id="7d023-919">**WINHTTP_SECURITY_INFO**</span></span>](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info) | \- | <span data-ttu-id="7d023-920">X</span><span class="sxs-lookup"><span data-stu-id="7d023-920">X</span></span> | <span data-ttu-id="7d023-921">X</span><span class="sxs-lookup"><span data-stu-id="7d023-921">X</span></span> | \- | <span data-ttu-id="7d023-922">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="7d023-922">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7d023-923">WINHTTP \_ 選項 \_ 安全性 \_ 金鑰 \_ 位</span><span class="sxs-lookup"><span data-stu-id="7d023-923">WINHTTP\_OPTION\_SECURITY\_KEY\_BITNESS</span></span><br/><span data-ttu-id="7d023-924">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-924">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-925">X</span><span class="sxs-lookup"><span data-stu-id="7d023-925">X</span></span> | <span data-ttu-id="7d023-926">X</span><span class="sxs-lookup"><span data-stu-id="7d023-926">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-927">WINHTTP \_ 選項 \_ 傳送 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="7d023-927">WINHTTP\_OPTION\_SEND\_TIMEOUT</span></span><br/><span data-ttu-id="7d023-928">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-928">**DWORD**</span></span> | <span data-ttu-id="7d023-929">X</span><span class="sxs-lookup"><span data-stu-id="7d023-929">X</span></span> | <span data-ttu-id="7d023-930">X</span><span class="sxs-lookup"><span data-stu-id="7d023-930">X</span></span> | <span data-ttu-id="7d023-931">X</span><span class="sxs-lookup"><span data-stu-id="7d023-931">X</span></span> | <span data-ttu-id="7d023-932">X</span><span class="sxs-lookup"><span data-stu-id="7d023-932">X</span></span> | \- |
| <span data-ttu-id="7d023-933">WINHTTP \_ 選項 \_ 伺服器 \_ CBT</span><span class="sxs-lookup"><span data-stu-id="7d023-933">WINHTTP\_OPTION\_SERVER\_CBT</span></span><br/><span data-ttu-id="7d023-934">[**SecPkgCoNtext \_ 系結**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span><span class="sxs-lookup"><span data-stu-id="7d023-934">[**SecPkgContext\_Bindings**](/windows/desktop/api/sspi/ns-sspi-secpkgcontext_bindings)\*</span></span> | \- | <span data-ttu-id="7d023-935">X</span><span class="sxs-lookup"><span data-stu-id="7d023-935">X</span></span> | <span data-ttu-id="7d023-936">X</span><span class="sxs-lookup"><span data-stu-id="7d023-936">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-937">WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 鏈 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="7d023-937">WINHTTP\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT</span></span><br/>[<span data-ttu-id="7d023-938">**CERT_CHAIN_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="7d023-938">**CERT_CHAIN_CONTEXT**</span></span>](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) | \- | <span data-ttu-id="7d023-939">X</span><span class="sxs-lookup"><span data-stu-id="7d023-939">X</span></span> | <span data-ttu-id="7d023-940">X</span><span class="sxs-lookup"><span data-stu-id="7d023-940">X</span></span> | \- | <span data-ttu-id="7d023-941">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="7d023-941">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7d023-942">WINHTTP \_ 選項 \_ 伺服器 \_ 證書 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="7d023-942">WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT</span></span><br/>[<span data-ttu-id="7d023-943">**憑證內容**</span><span class="sxs-lookup"><span data-stu-id="7d023-943">**CERT CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) | \- | <span data-ttu-id="7d023-944">X</span><span class="sxs-lookup"><span data-stu-id="7d023-944">X</span></span> | <span data-ttu-id="7d023-945">X</span><span class="sxs-lookup"><span data-stu-id="7d023-945">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-946">已 \_ 使用 WINHTTP 選項 \_ 伺服器 \_ SPN \_</span><span class="sxs-lookup"><span data-stu-id="7d023-946">WINHTTP\_OPTION\_SERVER\_SPN\_USED</span></span><br/><span data-ttu-id="7d023-947">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-947">**LPWSTR**</span></span> | \- | <span data-ttu-id="7d023-948">X</span><span class="sxs-lookup"><span data-stu-id="7d023-948">X</span></span> | <span data-ttu-id="7d023-949">X</span><span class="sxs-lookup"><span data-stu-id="7d023-949">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-950">WINHTTP \_ 選項 \_ SPN</span><span class="sxs-lookup"><span data-stu-id="7d023-950">WINHTTP\_OPTION\_SPN</span></span><br/><span data-ttu-id="7d023-951">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-951">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-952">X</span><span class="sxs-lookup"><span data-stu-id="7d023-952">X</span></span> | \- | <span data-ttu-id="7d023-953">X</span><span class="sxs-lookup"><span data-stu-id="7d023-953">X</span></span> | \- |
| <span data-ttu-id="7d023-954">WINHTTP \_ 選項 \_ 資料流程 \_ 錯誤碼 \_</span><span class="sxs-lookup"><span data-stu-id="7d023-954">WINHTTP\_OPTION\_STREAM\_ERROR\_CODE</span></span><br/><span data-ttu-id="7d023-955">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-955">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-956">X</span><span class="sxs-lookup"><span data-stu-id="7d023-956">X</span></span> | <span data-ttu-id="7d023-957">X</span><span class="sxs-lookup"><span data-stu-id="7d023-957">X</span></span> | \- | <span data-ttu-id="7d023-958">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="7d023-958">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7d023-959">WINHTTP \_ 選項 \_ TCP \_ 快速 \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="7d023-959">WINHTTP\_OPTION\_TCP\_FAST\_OPEN</span></span><br/><span data-ttu-id="7d023-960">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-960">**BOOL**</span></span> | <span data-ttu-id="7d023-961">X</span><span class="sxs-lookup"><span data-stu-id="7d023-961">X</span></span> | \- | \- | <span data-ttu-id="7d023-962">X</span><span class="sxs-lookup"><span data-stu-id="7d023-962">X</span></span> | <span data-ttu-id="7d023-963">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="7d023-963">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7d023-964">WINHTTP \_ 選項 \_ TCP \_ KEEPALIVE</span><span class="sxs-lookup"><span data-stu-id="7d023-964">WINHTTP\_OPTION\_TCP\_KEEPALIVE</span></span><br/>[<span data-ttu-id="7d023-965">**tcp \_ keepalive**</span><span class="sxs-lookup"><span data-stu-id="7d023-965">**tcp\_keepalive**</span></span>](/windows/win32/winsock/sio-keepalive-vals) | <span data-ttu-id="7d023-966">X</span><span class="sxs-lookup"><span data-stu-id="7d023-966">X</span></span> | \- | \- | <span data-ttu-id="7d023-967">X</span><span class="sxs-lookup"><span data-stu-id="7d023-967">X</span></span> | <span data-ttu-id="7d023-968">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="7d023-968">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7d023-969">WINHTTP \_ 選項 \_ TLS \_ FALSE \_ START</span><span class="sxs-lookup"><span data-stu-id="7d023-969">WINHTTP\_OPTION\_TLS\_FALSE\_START</span></span><br/><span data-ttu-id="7d023-970">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-970">**BOOL**</span></span> | <span data-ttu-id="7d023-971">X</span><span class="sxs-lookup"><span data-stu-id="7d023-971">X</span></span> | \- | \- | <span data-ttu-id="7d023-972">X</span><span class="sxs-lookup"><span data-stu-id="7d023-972">X</span></span> | <span data-ttu-id="7d023-973">Windows 10 版本2004</span><span class="sxs-lookup"><span data-stu-id="7d023-973">Windows 10 Version 2004</span></span> |
| <span data-ttu-id="7d023-974">WINHTTP \_ 選項 \_ TLS \_ 通訊協定不 \_ 安全 \_ 的回復</span><span class="sxs-lookup"><span data-stu-id="7d023-974">WINHTTP\_OPTION\_TLS\_PROTOCOL\_INSECURE\_FALLBACK</span></span><br/><span data-ttu-id="7d023-975">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-975">**BOOL**</span></span> | <span data-ttu-id="7d023-976">X</span><span class="sxs-lookup"><span data-stu-id="7d023-976">X</span></span> | \- | \- | <span data-ttu-id="7d023-977">X</span><span class="sxs-lookup"><span data-stu-id="7d023-977">X</span></span> | <span data-ttu-id="7d023-978">Windows 10 版本21H1</span><span class="sxs-lookup"><span data-stu-id="7d023-978">Windows 10 Version 21H1</span></span> |
| <span data-ttu-id="7d023-979">WINHTTP \_ 選項 \_ UNLOAD \_ 通知 \_ 事件</span><span class="sxs-lookup"><span data-stu-id="7d023-979">WINHTTP\_OPTION\_UNLOAD\_NOTIFY\_EVENT</span></span><br/>[<span data-ttu-id="7d023-980">HINTERNET</span><span class="sxs-lookup"><span data-stu-id="7d023-980">HINTERNET</span></span>](hinternet-handles-in-winhttp.md) | <span data-ttu-id="7d023-981">X</span><span class="sxs-lookup"><span data-stu-id="7d023-981">X</span></span> | \- | \- | <span data-ttu-id="7d023-982">X</span><span class="sxs-lookup"><span data-stu-id="7d023-982">X</span></span> | \- |
| <span data-ttu-id="7d023-983">WINHTTP \_ 選項 \_ UNSAFE \_ 標頭 \_ 剖析</span><span class="sxs-lookup"><span data-stu-id="7d023-983">WINHTTP\_OPTION\_UNSAFE\_HEADER\_PARSING</span></span><br/><span data-ttu-id="7d023-984">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-984">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-985">X</span><span class="sxs-lookup"><span data-stu-id="7d023-985">X</span></span> | \- | <span data-ttu-id="7d023-986">X</span><span class="sxs-lookup"><span data-stu-id="7d023-986">X</span></span> | \- |
| <span data-ttu-id="7d023-987">WINHTTP \_ 選項 \_ 升級 \_ 至 \_ WEB \_ 通訊端</span><span class="sxs-lookup"><span data-stu-id="7d023-987">WINHTTP\_OPTION\_UPGRADE\_TO\_WEB\_SOCKET</span></span><br/><span data-ttu-id="7d023-988">N/A</span><span class="sxs-lookup"><span data-stu-id="7d023-988">N/A</span></span> | \- | <span data-ttu-id="7d023-989">X</span><span class="sxs-lookup"><span data-stu-id="7d023-989">X</span></span> | \- | <span data-ttu-id="7d023-990">X</span><span class="sxs-lookup"><span data-stu-id="7d023-990">X</span></span> | \- |
| <span data-ttu-id="7d023-991">WINHTTP \_ 選項 \_ URL</span><span class="sxs-lookup"><span data-stu-id="7d023-991">WINHTTP\_OPTION\_URL</span></span><br/><span data-ttu-id="7d023-992">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-992">**LPWSTR**</span></span> | \- | <span data-ttu-id="7d023-993">X</span><span class="sxs-lookup"><span data-stu-id="7d023-993">X</span></span> | <span data-ttu-id="7d023-994">X</span><span class="sxs-lookup"><span data-stu-id="7d023-994">X</span></span> | \- | \- |
| <span data-ttu-id="7d023-995">WINHTTP \_ 選項 \_ 使用 \_ 全域 \_ 伺服器 \_ 認證</span><span class="sxs-lookup"><span data-stu-id="7d023-995">WINHTTP\_OPTION\_USE\_GLOBAL\_SERVER\_CREDENTIALS</span></span><br/><span data-ttu-id="7d023-996">**Bool**</span><span class="sxs-lookup"><span data-stu-id="7d023-996">**BOOL**</span></span> | <span data-ttu-id="7d023-997">X</span><span class="sxs-lookup"><span data-stu-id="7d023-997">X</span></span> | <span data-ttu-id="7d023-998">X</span><span class="sxs-lookup"><span data-stu-id="7d023-998">X</span></span> | \- | <span data-ttu-id="7d023-999">X</span><span class="sxs-lookup"><span data-stu-id="7d023-999">X</span></span> | \- |
| <span data-ttu-id="7d023-1000">WINHTTP \_ 選項 \_ 使用者 \_ 代理程式</span><span class="sxs-lookup"><span data-stu-id="7d023-1000">WINHTTP\_OPTION\_USER\_AGENT</span></span><br/><span data-ttu-id="7d023-1001">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-1001">**LPWSTR**</span></span> | <span data-ttu-id="7d023-1002">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1002">X</span></span> | \- | <span data-ttu-id="7d023-1003">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1003">X</span></span> | <span data-ttu-id="7d023-1004">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1004">X</span></span> | \- |
| <span data-ttu-id="7d023-1005">WINHTTP \_ 選項使用者 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="7d023-1005">WINHTTP\_OPTION\_USERNAME</span></span><br/><span data-ttu-id="7d023-1006">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7d023-1006">**LPWSTR**</span></span> | \- | <span data-ttu-id="7d023-1007">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1007">X</span></span> | <span data-ttu-id="7d023-1008">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1008">X</span></span> | <span data-ttu-id="7d023-1009">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1009">X</span></span> | \- |
| <span data-ttu-id="7d023-1010">WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 關閉 \_ 超時</span><span class="sxs-lookup"><span data-stu-id="7d023-1010">WINHTTP\_OPTION\_WEB\_SOCKET\_CLOSE\_TIMEOUT</span></span><br/><span data-ttu-id="7d023-1011">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-1011">**DWORD**</span></span> | \- | \- | <span data-ttu-id="7d023-1012">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1012">X</span></span> | <span data-ttu-id="7d023-1013">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1013">X</span></span> | \- |
| <span data-ttu-id="7d023-1014">WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ KEEPALIVE \_ 間隔</span><span class="sxs-lookup"><span data-stu-id="7d023-1014">WINHTTP\_OPTION\_WEB\_SOCKET\_KEEPALIVE\_INTERVAL</span></span><br/><span data-ttu-id="7d023-1015">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-1015">**DWORD**</span></span> | \- | \- | <span data-ttu-id="7d023-1016">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1016">X</span></span> | <span data-ttu-id="7d023-1017">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1017">X</span></span> | \- |
| <span data-ttu-id="7d023-1018">WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 接收 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="7d023-1018">WINHTTP\_OPTION\_WEB\_SOCKET\_RECEIVE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="7d023-1019">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-1019">**DWORD**</span></span> | <span data-ttu-id="7d023-1020">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1020">X</span></span> | <span data-ttu-id="7d023-1021">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1021">X</span></span> | <span data-ttu-id="7d023-1022">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1022">X</span></span> | <span data-ttu-id="7d023-1023">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1023">X</span></span> | <span data-ttu-id="7d023-1024">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d023-1024">Windows 8.1</span></span> |
| <span data-ttu-id="7d023-1025">WINHTTP \_ 選項 \_ WEB \_ 通訊端 \_ 傳送 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="7d023-1025">WINHTTP\_OPTION\_WEB\_SOCKET\_SEND\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="7d023-1026">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-1026">**DWORD**</span></span> | <span data-ttu-id="7d023-1027">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1027">X</span></span> | <span data-ttu-id="7d023-1028">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1028">X</span></span> | <span data-ttu-id="7d023-1029">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1029">X</span></span> | <span data-ttu-id="7d023-1030">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1030">X</span></span> | <span data-ttu-id="7d023-1031">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7d023-1031">Windows 8.1</span></span> |
| <span data-ttu-id="7d023-1032">WINHTTP \_ 選項背景 \_ 工作 \_ 執行緒 \_ 計數</span><span class="sxs-lookup"><span data-stu-id="7d023-1032">WINHTTP\_OPTION\_WORKER\_THREAD\_COUNT</span></span><br/><span data-ttu-id="7d023-1033">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-1033">**DWORD**</span></span> | \- | \- | \- | <span data-ttu-id="7d023-1034">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1034">X</span></span> | \- |
| <span data-ttu-id="7d023-1035">WINHTTP \_ 選項 \_ 寫入 \_ 緩衝區 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="7d023-1035">WINHTTP\_OPTION\_WRITE\_BUFFER\_SIZE</span></span><br/><span data-ttu-id="7d023-1036">**Dword**</span><span class="sxs-lookup"><span data-stu-id="7d023-1036">**DWORD**</span></span> | \- | <span data-ttu-id="7d023-1037">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1037">X</span></span> | <span data-ttu-id="7d023-1038">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1038">X</span></span> | <span data-ttu-id="7d023-1039">X</span><span class="sxs-lookup"><span data-stu-id="7d023-1039">X</span></span> | \- |

> [!Note]
> <span data-ttu-id="7d023-1040">針對 Windows XP 和 Windows 2000，請參閱 [執行時間需求](winhttp-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="7d023-1040">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d023-1041">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d023-1041">Requirements</span></span>

| <span data-ttu-id="7d023-1042">需求</span><span class="sxs-lookup"><span data-stu-id="7d023-1042">Requirement</span></span> | <span data-ttu-id="7d023-1043">值</span><span class="sxs-lookup"><span data-stu-id="7d023-1043">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="7d023-1044">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d023-1044">Minimum supported client</span></span> | <span data-ttu-id="7d023-1045">Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d023-1045">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span>            |
| <span data-ttu-id="7d023-1046">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d023-1046">Minimum supported server</span></span> | <span data-ttu-id="7d023-1047">Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]</span><span class="sxs-lookup"><span data-stu-id="7d023-1047">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span>         |
| <span data-ttu-id="7d023-1048">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7d023-1048">Redistributable</span></span>          | <span data-ttu-id="7d023-1049">Windows XP 和 Windows 2000 上的 WinHTTP 5.0 和 Internet Explorer 5.01 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7d023-1049">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span> |
| <span data-ttu-id="7d023-1050">標頭</span><span class="sxs-lookup"><span data-stu-id="7d023-1050">Header</span></span>                   | <span data-ttu-id="7d023-1051">WinHTTP. h</span><span class="sxs-lookup"><span data-stu-id="7d023-1051">Winhttp.h</span></span>                                                                       |

## <a name="see-also"></a><span data-ttu-id="7d023-1052">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d023-1052">See also</span></span>

[<span data-ttu-id="7d023-1053">WinHTTP 版本</span><span class="sxs-lookup"><span data-stu-id="7d023-1053">WinHTTP Versions</span></span>](winhttp-versions.md)
