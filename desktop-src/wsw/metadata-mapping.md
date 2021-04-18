---
title: 中繼資料對應
description: 元資料檔案的內容會以下列各節所述的方式對應至中繼資料 API。
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- 適用于 Windows 的中繼資料對應 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9da067768569e78ba6bb98ee219e11917d3201
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106983308"
---
# <a name="metadata-mapping"></a><span data-ttu-id="bd098-106">中繼資料對應</span><span class="sxs-lookup"><span data-stu-id="bd098-106">Metadata Mapping</span></span>

<span data-ttu-id="bd098-107">元資料檔案的內容會以下列各節所述的方式對應至中繼資料 API。</span><span class="sxs-lookup"><span data-stu-id="bd098-107">The contents of a metadata document map to the metadata API in the ways explained in the following sections.</span></span>


<span data-ttu-id="bd098-108">本檔中使用下列命名空間前置詞：</span><span class="sxs-lookup"><span data-stu-id="bd098-108">The following namespace prefixes are used throughout this documentation:</span></span>

``` syntax
wsdl   => http://schemas.xmlsoap.org/wsdl/
soap11 => http://schemas.xmlsoap.org/wsdl/soap/
soap12 => http://schemas.xmlsoap.org/wsdl/soap12/
wsa09  => http://schemas.xmlsoap.org/ws/2004/08/addressing
wsa10  => http://www.w3.org/2005/08/addressing
wsa09p => http://schemas.xmlsoap.org/ws/2004/08/addressing/policy
wsa10p => http://www.w3.org/2006/05/addressing/wsdl
binp   => http://schemas.microsoft.com/ws/06/2004/mspolicy/netbinary1
mtomp  => http://schemas.xmlsoap.org/ws/2004/09/policy/optimizedmimeserialization
sp     => http://schemas.xmlsoap.org/ws/2005/07/securitypolicy
wsp    => http://schemas.xmlsoap.org/ws/2004/09/policy
netf   => http://schemas.microsoft.com/ws/2006/05/framing/policy
httpp  => http://schemas.microsoft.com/ws/06/2004/policy/http
wst10  => http://schemas.xmlsoap.org/ws/2005/02/trust
wsi    => http://schemas.xmlsoap.org/ws/2005/05/identity
```

<span data-ttu-id="bd098-109">後續各節將描述 API 結構，以及它們所對應的 (WSDL 或原則) 的元資料結構。</span><span class="sxs-lookup"><span data-stu-id="bd098-109">The subsequent sections describe API constructs along with what metadata constructs (WSDL or Policy) they correspond to.</span></span>

<span data-ttu-id="bd098-110">熟悉中繼資料規格（例如 WSDL 和原則）將有助於瞭解這一節。</span><span class="sxs-lookup"><span data-stu-id="bd098-110">Familiarity with metadata specifications such as WSDL and Policy will aid in understanding this section.</span></span>

## <a name="endpoint-address"></a><span data-ttu-id="bd098-111">端點位址</span><span class="sxs-lookup"><span data-stu-id="bd098-111">Endpoint address</span></span>

<span data-ttu-id="bd098-112">端點的位址 (查看 [**WS \_ 端點 \_ 位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) 是從 wsdl 檔的 wsdl： port 元素內的擴充性元素取得。</span><span class="sxs-lookup"><span data-stu-id="bd098-112">The address of an endpoint (see [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) is obtained from an extensibility element within the wsdl:port element of the WSDL document.</span></span> <span data-ttu-id="bd098-113">下列擴充性元素支援指定位址：</span><span class="sxs-lookup"><span data-stu-id="bd098-113">The following extensibility elements are supported for specifying the address:</span></span>

``` syntax
<wsdl:port...>
    <soap11:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <soap12:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa09:EndpointReference.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa10:EndpointReference.../>
</wsdl:port>
```

## <a name="ws_channel_binding"></a><span data-ttu-id="bd098-114">WS \_ 通道系結 \_</span><span class="sxs-lookup"><span data-stu-id="bd098-114">WS\_CHANNEL\_BINDING</span></span>

<span data-ttu-id="bd098-115">通道系結 (查看 [**WS \_ 通道 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) 系結) 是由使用的 soap 系結所決定，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bd098-115">The channel binding (see [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) is determined by the transport the soap binding used, as follows:</span></span>

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a><span data-ttu-id="bd098-116">WS \_ 通道 \_ 屬性 \_ 信封 \_ 版本</span><span class="sxs-lookup"><span data-stu-id="bd098-116">WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION</span></span>

<span data-ttu-id="bd098-117">信封版本 (請參閱 [**WS \_ 通道 \_ 屬性 \_ 信封 \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) 取決於使用的 soap 系結，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bd098-117">The envelope version (see [**WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by which soap binding is used, as follows:</span></span>

``` syntax
<wsdl:binding...>
    <soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

``` syntax
<wsdl:binding...>
    <soap12:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_2
</wsdl:binding>
```

## <a name="addressing-version"></a><span data-ttu-id="bd098-118">定址版本</span><span class="sxs-lookup"><span data-stu-id="bd098-118">Addressing Version</span></span>

<span data-ttu-id="bd098-119">定址版本 (請參閱 [**WS \_ 通道 \_ 屬性 \_ 定址 \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) 是由端點原則中的下列判斷提示所決定：</span><span class="sxs-lookup"><span data-stu-id="bd098-119">The addressing version (see [**WS\_CHANNEL\_PROPERTY\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <wsa09p:UsingAddressing.../> => WS_ADDRESSING_VERSION_0_9
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <wsa10p:UsingAddressing.../> => WS_ADDRESSING_VERSION_1_0
</wsp:Policy>
```

<span data-ttu-id="bd098-120">如果沒有定址判斷提示，則會假設為 [**WS \_ 定址 \_ 版本 \_ 傳輸**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) 。</span><span class="sxs-lookup"><span data-stu-id="bd098-120">If an addressing assertion is not present, then [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) is assumed.</span></span>

## <a name="message-encoding"></a><span data-ttu-id="bd098-121">訊息編碼</span><span class="sxs-lookup"><span data-stu-id="bd098-121">Message Encoding</span></span>

<span data-ttu-id="bd098-122">訊息的編碼 (查看 [**WS \_ 通道 \_ 屬性 \_ 編碼**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) 是由端點原則中的下列判斷提示所決定：</span><span class="sxs-lookup"><span data-stu-id="bd098-122">The encoding of the message (see [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

<span data-ttu-id="bd098-123">請注意，二進位編碼原則判斷提示不包含二進位編碼會話或無會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bd098-123">Note that the binary encoding policy assertion does not include information about whether the binary encoding is sessionful or sessionless.</span></span> <span data-ttu-id="bd098-124">這取決於編碼屬性條件約束 (應根據所使用的 [**WS \_ 通道 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) 是否會話或不) 來適當地進行。</span><span class="sxs-lookup"><span data-stu-id="bd098-124">This is determined by the encoding property constraint (which should be appropriate according to whether or not the [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) being used is sessionful or not).</span></span>

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

<span data-ttu-id="bd098-125">如果上述的判斷提示都不存在，則會使用文字編碼： [**ws \_ 編碼 \_ xml \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)、 **ws 編碼 xml \_ \_ \_ UTF16LE**、 **ws \_ 編碼 \_ xml \_ UTF16BE**。</span><span class="sxs-lookup"><span data-stu-id="bd098-125">If neither of the above assertions are present, then a text encoding is used: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS\_ENCODING\_XML\_UTF16LE**, **WS\_ENCODING\_XML\_UTF16BE**.</span></span>

<span data-ttu-id="bd098-126">請注意，原則不包含 MTOM 或文字編碼字元集的相關資訊 (是否為 UTF8、UTF16LE 或 UTF16BE) 。</span><span class="sxs-lookup"><span data-stu-id="bd098-126">Note that policy does not include information about the character set for MTOM or text encodings (whether it is UTF8, UTF16LE or UTF16BE).</span></span> <span data-ttu-id="bd098-127">使用的實際字元集值是由編碼屬性條件約束所決定。</span><span class="sxs-lookup"><span data-stu-id="bd098-127">The actual character set value used is determined by the encoding property constraint.</span></span>

## <a name="constraints-with-http-header-authentication"></a><span data-ttu-id="bd098-128">HTTP 標頭驗證的條件約束</span><span class="sxs-lookup"><span data-stu-id="bd098-128">Constraints with HTTP Header Authentication</span></span>

<span data-ttu-id="bd098-129">當指定 [**WS \_ HTTP \_ 標頭 \_ 驗證安全性系 \_ 結 \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) 安全性系結條件約束時，就會套用此區段。</span><span class="sxs-lookup"><span data-stu-id="bd098-129">This section applies when the [**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) security binding constraint is specified.</span></span>

<span data-ttu-id="bd098-130">此安全性系結會透過不同的判斷提示在原則中指出，指出應該使用 HTTP 標頭驗證，以及應該使用特定的驗證配置。</span><span class="sxs-lookup"><span data-stu-id="bd098-130">This security binding is indicated in the policy by different assertions that states both that HTTP header authentication should be used, and that a particular authentication scheme should be used.</span></span> <span data-ttu-id="bd098-131">原則判斷提示會對應到 [**WS \_ SECURITY \_ BINDING \_ PROPERTY \_ HTTP \_ 標頭 \_ 驗證 \_ 配置**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) 的值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bd098-131">The policy assertions correspond to the values of the [**WS\_SECURITY\_BINDING\_PROPERTY\_HTTP\_HEADER\_AUTH\_SCHEME**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) as follows:</span></span>

``` syntax
<wsp:Policy...>
    <httpp:BasicAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_BASIC
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NegotiateAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NtlmAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NTLM
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:DigestAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_DIGEST
</wsp:Policy>
```

## <a name="constraints-with-sll-transport-security"></a><span data-ttu-id="bd098-132">SLL 傳輸安全性的條件約束</span><span class="sxs-lookup"><span data-stu-id="bd098-132">Constraints with SLL Transport Security</span></span>

<span data-ttu-id="bd098-133">當指定 [**WS \_ SSL \_ 傳輸安全性系結 \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) 安全性系結條件約束時，就會套用此區段。</span><span class="sxs-lookup"><span data-stu-id="bd098-133">This section applies when the [**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="bd098-134">在此情況下，會使用下列原則判斷提示：</span><span class="sxs-lookup"><span data-stu-id="bd098-134">The following policy assertions are used in this case:</span></span>

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <sp:HttpsToken.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constraints-with-sspi-transport-security"></a><span data-ttu-id="bd098-135">SSPI 傳輸安全性的條件約束</span><span class="sxs-lookup"><span data-stu-id="bd098-135">Constraints with SSPI Transport Security</span></span>

<span data-ttu-id="bd098-136">當指定 [**WS \_ TCP \_ SSPI \_ 傳輸 \_ 安全性 \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) 系結條件約束安全性系結條件約束時，就會套用此區段。</span><span class="sxs-lookup"><span data-stu-id="bd098-136">This section applies when the [**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="bd098-137">在此情況下，會使用下列原則判斷提示：</span><span class="sxs-lookup"><span data-stu-id="bd098-137">The following policy assertions are used in this case:</span></span>

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <netf:WindowsTransportSecurity.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constrains-with-transport-security"></a><span data-ttu-id="bd098-138">限制傳輸安全性</span><span class="sxs-lookup"><span data-stu-id="bd098-138">Constrains with Transport Security</span></span>

<span data-ttu-id="bd098-139">如果指定了任何安全性系結條件約束，則可以指定 [**WS \_ 安全性 \_ 屬性 \_ 傳輸 \_ 保護 \_ 等級**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) 屬性條件約束：</span><span class="sxs-lookup"><span data-stu-id="bd098-139">The [**WS\_SECURITY\_PROPERTY\_TRANSPORT\_PROTECTION\_LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) property constraint can be specified if any of the security binding constraints are specified:</span></span>

-   [<span data-ttu-id="bd098-140">**WS \_ SSL \_ 傳輸 \_ 安全性系結 \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-140">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    <span data-ttu-id="bd098-141">原則中的值一律是 [**WS \_ 保護 \_ 等級的 \_ 正負號 \_ 和 \_ 加密**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)。</span><span class="sxs-lookup"><span data-stu-id="bd098-141">The value from policy is always [**WS\_PROTECTION\_LEVEL\_SIGN\_AND\_ENCRYPT**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

-   [<span data-ttu-id="bd098-142">**WS \_ TCP \_ SSPI \_ 傳輸 \_ 安全性系結 \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-142">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    <span data-ttu-id="bd098-143">原則中的值會指定為 WindowsTransportSecurity 判斷提示的一部分，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bd098-143">The value from policy is specified as part of the WindowsTransportSecurity assertion, as follows:</span></span>

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [<span data-ttu-id="bd098-144">**WS \_ HTTP \_ 標頭 \_ 驗證安全性系結 \_ \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-144">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    <span data-ttu-id="bd098-145">原則中的值一律為 [**WS \_ 保護 \_ 層級 \_ 無**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)。</span><span class="sxs-lookup"><span data-stu-id="bd098-145">The value from policy is always [**WS\_PROTECTION\_LEVEL\_NONE**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

## <a name="constraints-with-kerberos-apreq-security-binding"></a><span data-ttu-id="bd098-146">Kerberos APREQ 安全性系結的條件約束</span><span class="sxs-lookup"><span data-stu-id="bd098-146">Constraints with Kerberos APREQ Security Binding</span></span>

<span data-ttu-id="bd098-147">當指定 [**WS \_ KERBEROS \_ APREQ \_ 訊息安全性系結 \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) 安全性系結條件約束時，就會套用此區段。</span><span class="sxs-lookup"><span data-stu-id="bd098-147">This section applies when the [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="bd098-148">在此情況下，會使用下列原則判斷提示：</span><span class="sxs-lookup"><span data-stu-id="bd098-148">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a><span data-ttu-id="bd098-149">訊息安全性系結的條件約束</span><span class="sxs-lookup"><span data-stu-id="bd098-149">Constraints with Message Security Binding</span></span>

<span data-ttu-id="bd098-150">當指定 [**WS 使用者 \_ 名稱訊息安全性系結 \_ \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) 安全性系結條件約束時，就會套用此區段。</span><span class="sxs-lookup"><span data-stu-id="bd098-150">This section applies when the [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="bd098-151">在此情況下，會使用下列原則判斷提示：</span><span class="sxs-lookup"><span data-stu-id="bd098-151">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a><span data-ttu-id="bd098-152">WS \_ CERT \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束</span><span class="sxs-lookup"><span data-stu-id="bd098-152">WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="bd098-153">當指定 [**WS \_ CERT \_ MESSAGE SECURITY 系結 \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) 安全性系結條件約束時，就會套用這個區段。</span><span class="sxs-lookup"><span data-stu-id="bd098-153">This section applies when the [**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="bd098-154">在此情況下，會使用下列原則判斷提示：</span><span class="sxs-lookup"><span data-stu-id="bd098-154">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a><span data-ttu-id="bd098-155">WS \_ 發出的 \_ 權杖 \_ 訊息安全性系結 \_ \_ \_ 條件約束</span><span class="sxs-lookup"><span data-stu-id="bd098-155">WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="bd098-156">當指定了 [**WS 簽發的 \_ \_ 權杖 \_ 訊息安全性系結 \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) 安全性系結條件約束時，就會套用這個區段。</span><span class="sxs-lookup"><span data-stu-id="bd098-156">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="bd098-157">在此情況下，會使用下列原則判斷提示：</span><span class="sxs-lookup"><span data-stu-id="bd098-157">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:IssuedToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:RequestSecurityTokenTemplate TrustVersion='xs:anyURI&quot;?>
                ...
                <wst10:Claims>
                    <wsi:ClaimType Optional='xs:boolean'?>xs:anyURI<wt:ClaimType>*
                </wst10:Claims>
                ...
            </wsp:RequestSecurityTokenTemplate>
            <wsp:Policy>
                <sp:RequireDerivedKeys/> ?
                <sp:RequireExternalReference/> ?
                <sp:RequireInternalReference/> ?
            </wsp:Policy> ?
        </sp:IssuedToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

<span data-ttu-id="bd098-158">以下描述 [**WS \_ 發出的 \_ 權杖訊息安全性系結 \_ \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) 的欄位對應至上述原則：</span><span class="sxs-lookup"><span data-stu-id="bd098-158">The following describes the mapping of fields of the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) to the above policy:</span></span>

-   <span data-ttu-id="bd098-159">ClaimConstraints 欄位是用來驗證出現在上述 wsi： ClaimType 元素內的一組宣告類型 Uri。</span><span class="sxs-lookup"><span data-stu-id="bd098-159">The claimConstraints field is used to verify the set of claim type URIs that appear within the wsi:ClaimType element above.</span></span>

-   <span data-ttu-id="bd098-160">IssuerAddress 欄位對應于上述的 wsp： Issuer 元素，這是可發出權杖之服務的 [**WS \_ 端點 \_ 位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) 。</span><span class="sxs-lookup"><span data-stu-id="bd098-160">The issuerAddress field corresponds to the wsp:Issuer element above, which is the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) of the service that can issue the token.</span></span>

-   <span data-ttu-id="bd098-161">RequestSecurityTokenTemplate 欄位會對應至 wsp： RequestSecurityTokenTemplate 元素的子項目。</span><span class="sxs-lookup"><span data-stu-id="bd098-161">The requestSecurityTokenTemplate field corresponds to the child elements of the wsp:RequestSecurityTokenTemplate element.</span></span>

## <a name="ws_security_context_message_security_binding_constraint"></a><span data-ttu-id="bd098-162">WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性系結 \_ \_ 條件約束</span><span class="sxs-lookup"><span data-stu-id="bd098-162">WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="bd098-163">當指定 [**WS \_ 安全性 \_ 內容 \_ 訊息安全性系結 \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) 安全性系結條件約束時，就會套用此區段。</span><span class="sxs-lookup"><span data-stu-id="bd098-163">This section applies when the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="bd098-164">在此情況下，會使用下列原則判斷提示：</span><span class="sxs-lookup"><span data-stu-id="bd098-164">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:SecureConversationToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:Policy>
                <sp:RequireDerivedKeys.../>?
                <sp:RequireExternalUriReference.../>?
                <sp:SC10SecurityContextToken.../>? => WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005
                <sp:BootstrapPolicy... >?
                   <wsp:Policy> ...  </wsp:Policy> => WS_SECURITY_CONSTRAINTS
                </sp:BootstrapPolicy>
            </wsp:Policy>
        </wsp:SecureConversationToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

<span data-ttu-id="bd098-165">熵模式取決於 <sp： Trust10> 判斷提示。</span><span class="sxs-lookup"><span data-stu-id="bd098-165">The entropy mode is determined by the <sp:Trust10> assertion.</span></span> <span data-ttu-id="bd098-166"><sp： RequireClientEntropy/> 和 <sp： RequireServerEntropy/> => [**ws \_ 安全性 \_ 金鑰 \_ 熵 \_ 模式 \_ 組合**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <Sp： RequireClientEntropy/> => **ws-management \_ 安全性 \_ 金鑰 \_ 熵 \_ 模式 \_ 用戶端 \_ 僅** <sp： RequireServerEntropy/> => **ws-management \_ 安全性 \_ 金鑰 \_ 熵 \_ 模式 \_ 伺服器 \_**</span><span class="sxs-lookup"><span data-stu-id="bd098-166"><sp:RequireClientEntropy/> and <sp:RequireServerEntropy/> => [**WS\_SECURITY\_KEY\_ENTROPY\_MODE\_COMBINED**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <sp:RequireClientEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_CLIENT\_ONLY** <sp:RequireServerEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_SERVER\_ONLY**</span></span>

## <a name="ws_request_security_token_property_trust_version"></a><span data-ttu-id="bd098-167">WS \_ 要求 \_ 安全性 \_ 權杖 \_ 屬性 \_ 信任 \_ 版本</span><span class="sxs-lookup"><span data-stu-id="bd098-167">WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION</span></span>

<span data-ttu-id="bd098-168">當指定了 [**WS 簽發的 \_ \_ 權杖 \_ 訊息安全性系結 \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) 安全性系結條件約束時，就會套用這個區段。</span><span class="sxs-lookup"><span data-stu-id="bd098-168">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="bd098-169">下列原則判斷提示用來識別 [**Ws-trust \_ \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) 和相關聯的選項。</span><span class="sxs-lookup"><span data-stu-id="bd098-169">The following policy assertions are used to identify the [**WS\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) and associated options.</span></span>

``` syntax
<sp:Trust10> => WS_TRUST_VERSION_FEBRUARY_2005
    <sp:Policy>
        <sp:MustSupportClientChallenge/> ?
        <sp:MustSupportServerChallenge/> ?
        <sp:RequireClientEntropy/> ?
        <sp:RequireServerEntropy/> ?
        <sp:MustSupportIssuedTokens/> ?
    </sp:Policy>
</sp:Trust10>
```

<span data-ttu-id="bd098-170">您可以使用 [**ws \_ request \_ security \_ token \_ 屬性 \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) ，並將屬性識別碼為 [**ws \_ request \_ security \_ token \_ property \_ trust \_ version**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)來指定信任版本。</span><span class="sxs-lookup"><span data-stu-id="bd098-170">The trust version can be specified using the [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) with a property id of [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span></span>

## <a name="ws_security_property_security_header_version"></a><span data-ttu-id="bd098-171">WS \_ 安全性 \_ 屬性 \_ 安全性 \_ 標頭 \_ 版本</span><span class="sxs-lookup"><span data-stu-id="bd098-171">WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION</span></span>

<span data-ttu-id="bd098-172">當使用下列任何一個系結條件約束時，就適用本節：</span><span class="sxs-lookup"><span data-stu-id="bd098-172">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="bd098-173">**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-173">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="bd098-174">**WS 使用者 \_ 名稱 \_ 訊息安全性系結 \_ \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-174">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="bd098-175">**WS \_ CERT \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-175">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="bd098-176">**WS \_ 發出的 \_ 權杖 \_ 訊息安全性系結 \_ \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-176">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="bd098-177">由 [**WS \_ security \_ PROPERTY \_ security \_ header \_ version**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) 指定的標頭安全性版本 (由下列其中一個原則判斷提示所決定：</span><span class="sxs-lookup"><span data-stu-id="bd098-177">The header security version (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a><span data-ttu-id="bd098-178">標頭安全性配置的條件約束</span><span class="sxs-lookup"><span data-stu-id="bd098-178">Constraints with Header Security Layout</span></span>

<span data-ttu-id="bd098-179">當使用下列任何一個系結條件約束時，就適用本節：</span><span class="sxs-lookup"><span data-stu-id="bd098-179">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="bd098-180">**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-180">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="bd098-181">**WS 使用者 \_ 名稱 \_ 訊息安全性系結 \_ \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-181">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="bd098-182">**WS \_ CERT \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-182">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="bd098-183">**WS \_ 發出的 \_ 權杖 \_ 訊息安全性系結 \_ \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-183">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="bd098-184">由 [**WS \_ 安全性 \_ 屬性 \_ 安全性 \_ 標頭 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) 配置所指定的安全性標頭配置 (，) 是由下列其中一個原則判斷提示所決定：</span><span class="sxs-lookup"><span data-stu-id="bd098-184">The security header layout (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_LAYOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Lax.../> => WS_SECURITY_HEADER_LAYOUT_LAX
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Strict.../> => WS_SECURITY_HEADER_LAYOUT_STRICT
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsFirst.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsLast.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

## <a name="constraints-with-timestamp-security"></a><span data-ttu-id="bd098-185">具有時間戳記安全性的條件約束</span><span class="sxs-lookup"><span data-stu-id="bd098-185">Constraints with Timestamp Security</span></span>

<span data-ttu-id="bd098-186">當使用下列任何一個系結條件約束時，就適用本節：</span><span class="sxs-lookup"><span data-stu-id="bd098-186">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="bd098-187">**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-187">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="bd098-188">**WS 使用者 \_ 名稱 \_ 訊息安全性系結 \_ \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-188">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="bd098-189">**WS \_ CERT \_ MESSAGE \_ SECURITY \_ BINDING \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-189">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="bd098-190">**WS \_ 發出的 \_ 權杖 \_ 訊息安全性系結 \_ \_ \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="bd098-190">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="bd098-191">時間戳記是否包含在安全性標頭 (如 [**WS \_ 安全性 \_ 屬性 \_ 時間戳記 \_ 使用量**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) 所指定) 是由下列位置中的 sp： IncludeTimestamp 所決定：</span><span class="sxs-lookup"><span data-stu-id="bd098-191">Whether or not a timestamp is included in the security header (as specified by [**WS\_SECURITY\_PROPERTY\_TIMESTAMP\_USAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by the presence of the sp:IncludeTimestamp in the following location:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

<span data-ttu-id="bd098-192">如果有 sp： IncludeTimestamp 判斷提示存在，來自原則的值 [**一律為 WS \_ 安全性 \_ 時間戳記 \_ 使用 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)方式。</span><span class="sxs-lookup"><span data-stu-id="bd098-192">If the sp:IncludeTimestamp assertion is present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

<span data-ttu-id="bd098-193">如果 sp： IncludeTimestamp 判斷提示不存在，來自原則的值為 [**WS \_ 安全性 \_ 時間戳記 \_ 使用 \_ 永不**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)。</span><span class="sxs-lookup"><span data-stu-id="bd098-193">If the sp:IncludeTimestamp assertion is not present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

 

 




