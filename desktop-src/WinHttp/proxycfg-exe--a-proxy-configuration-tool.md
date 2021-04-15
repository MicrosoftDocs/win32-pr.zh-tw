---
description: 本主題說明如何使用 Microsoft Windows HTTP 服務 (WinHTTP) proxy 設定工具 &\# 0034; ProxyCfg.exe&\# 0034;。
ms.assetid: f96adf59-59be-414e-ad6f-9eac05f4b975
title: Netsh.exe 和 ProxyCfg.exe Proxy 組態工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a33e832d324a5863652673b8e25725fba72e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510871"
---
# <a name="netshexe-and-proxycfgexe-proxy-configuration-tools"></a><span data-ttu-id="82807-103">Netsh.exe 和 ProxyCfg.exe Proxy 組態工具</span><span class="sxs-lookup"><span data-stu-id="82807-103">Netsh.exe and ProxyCfg.exe Proxy Configuration Tools</span></span>

<span data-ttu-id="82807-104">\* \* Windows Vista 和 Windows Server 2008： \* \*</span><span class="sxs-lookup"><span data-stu-id="82807-104">\*\*Windows Vista and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="82807-105">ProxyCfg.exe 已被取代。</span><span class="sxs-lookup"><span data-stu-id="82807-105">ProxyCfg.exe has been deprecated.</span></span> <span data-ttu-id="82807-106">它是由 [Netsh.exe winHTTP](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)) 命令所取代。</span><span class="sxs-lookup"><span data-stu-id="82807-106">It is replaced by the [Netsh.exe winhttp](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)) commands.</span></span>

<span data-ttu-id="82807-107">本主題說明如何使用 [Microsoft WINDOWS HTTP 服務 (WinHTTP) ](about-winhttp.md) proxy 設定工具 "ProxyCfg.exe"。</span><span class="sxs-lookup"><span data-stu-id="82807-107">This topic explains the use of the [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) proxy configuration tool, "ProxyCfg.exe".</span></span>

<span data-ttu-id="82807-108">有兩種方式可透過使用 Microsoft Windows HTTP Services (WinHTTP) 的 proxy (HTTPS) 伺服器來存取 HTTP 和安全超文字傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="82807-108">There are two ways to access HTTP and Secure Hypertext Transfer Protocol (HTTPS) servers through a proxy using Microsoft Windows HTTP Services (WinHTTP).</span></span> <span data-ttu-id="82807-109">首先，您可以從 WinHTTP 應用程式內指定 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-109">First, you can specify proxy settings from within your WinHTTP application.</span></span> <span data-ttu-id="82807-110">其次，您可以使用位於% windir% system32 目錄中的 proxy 設定公用程式，從您的應用程式外部指定預設 proxy 設定 \\ 。</span><span class="sxs-lookup"><span data-stu-id="82807-110">Second, you can specify default proxy settings from outside your application using the proxy configuration utility located in the %windir%\\system32 directory.</span></span>

<span data-ttu-id="82807-111">您可以透過程式設計方式，從您的應用程式或腳本內設定 proxy 資料。</span><span class="sxs-lookup"><span data-stu-id="82807-111">You can programmatically set the proxy data from within your application or script.</span></span> <span data-ttu-id="82807-112">如果您使用 WinHTTP API 來撰寫應用程式，請使用下列兩種方法之一來變更 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-112">If you are writing an application using the WinHTTP API, use one of the following two techniques to change proxy settings.</span></span>

-   <span data-ttu-id="82807-113">使用 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) 函數。</span><span class="sxs-lookup"><span data-stu-id="82807-113">Use the [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) function.</span></span> <span data-ttu-id="82807-114">在第二個參數中指定存取類型、第三個參數中指定 proxy 的名稱，並在第四個參數中指定 [略過] 清單。</span><span class="sxs-lookup"><span data-stu-id="82807-114">Specify access type in the second parameter, the name of the proxy in the third parameter, and a bypass list in the fourth parameter.</span></span> <span data-ttu-id="82807-115">下列範例會示範如何使用 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) 函數來設定 proxy 資料。</span><span class="sxs-lookup"><span data-stu-id="82807-115">The following example shows how the [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) function can be used to set proxy data.</span></span>

    ``` syntax
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_NAMED_PROXY,
                            L"proxy_name", 
                            L"<local>", 
                            0);
    ```

-   <span data-ttu-id="82807-116">使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函數。</span><span class="sxs-lookup"><span data-stu-id="82807-116">Use the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function.</span></span> <span data-ttu-id="82807-117">[**WinHTTP \_ 選項 \_ PROXY**](option-flags.md)旗標可讓您使用 [**winHTTP \_ proxy \_ 資訊**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)結構來指定 PROXY 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-117">The [**WINHTTP\_OPTION\_PROXY**](option-flags.md) flag enables you to specify proxy settings with a [**WINHTTP\_PROXY\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) structure.</span></span> <span data-ttu-id="82807-118">下列範例程式碼顯示如何使用 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函數來設定 proxy 資料。</span><span class="sxs-lookup"><span data-stu-id="82807-118">The following example code shows how the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function can be used to set proxy data.</span></span>

    ``` syntax
    WINHTTP_PROXY_INFO proxyInfo;
    proxyInfo.dwAccessType = WINHTTP_ACCESS_TYPE_NAMED_PROXY;
    proxyInfo.lpszProxy = L"proxy_name";
    proxyInfo.lpszProxyBypass = L"<local>";
        
    // Set the proxy information for this session.
    WinHttpSetOption( hSession, 
                      WINHTTP_OPTION_PROXY, 
                      &proxyInfo, 
                      sizeof(proxyInfo));
    ```

<span data-ttu-id="82807-119">如果您是使用 [**WinHttpRequest**](winhttprequest.md) 物件來撰寫腳本或應用程式，請使用下列技巧來變更 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-119">If you are writing a script or an application using the [**WinHttpRequest**](winhttprequest.md) object, use the following technique to change proxy settings.</span></span>

-   <span data-ttu-id="82807-120">使用 [**SetProxy**](iwinhttprequest-setproxy.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="82807-120">Use the [**SetProxy**](iwinhttprequest-setproxy.md) method.</span></span> <span data-ttu-id="82807-121">指定第一個參數的存取類型、第二個參數中的 proxy 名稱，以及第三個參數中的 [略過] 清單。</span><span class="sxs-lookup"><span data-stu-id="82807-121">Specify the access type in the first parameter, the name of the proxy in the second parameter, and a bypass list in the third parameter.</span></span> <span data-ttu-id="82807-122">下列範例顯示如何在腳本中使用 [**SetProxy**](iwinhttprequest-setproxy.md) 方法來設定 proxy 資料。</span><span class="sxs-lookup"><span data-stu-id="82807-122">The following example shows how the [**SetProxy**](iwinhttprequest-setproxy.md) method can be used in script to set proxy data.</span></span>

    ``` syntax
    WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                         "proxy_server:80", 
                         "*.microsoft.com");
    ```

<span data-ttu-id="82807-123">若要指定預設設定，而不需要使用 [**SetProxy**](iwinhttprequest-setproxy.md) 方法或 [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) 函數，請使用 proxy 設定公用程式。</span><span class="sxs-lookup"><span data-stu-id="82807-123">To specify default settings and eliminate the need to use either the [**SetProxy**](iwinhttprequest-setproxy.md) method or the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function, use the proxy configuration utility.</span></span> <span data-ttu-id="82807-124">您可以使用此公用程式，指定您的應用程式透過 proxy 直接存取網路，或透過指定略過清單來透過直接和 proxy 存取的組合來存取網路。</span><span class="sxs-lookup"><span data-stu-id="82807-124">Using this utility, you can specify that your application access a network either directly, through a proxy, or through a combination of direct and proxy access by specifying a bypass list.</span></span> <span data-ttu-id="82807-125">當您使用 WinHTTP API 時，proxy 設定工具只會決定當您將 **winHTTP \_ 存取 \_ 類型 \_ 預設** 旗標傳遞給 [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) API 時的設定。</span><span class="sxs-lookup"><span data-stu-id="82807-125">When you use the WinHTTP API, the proxy configuration tool only determines the settings when you pass the **WINHTTP\_ACCESS\_TYPE\_DEFAULT** flag to the [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) API.</span></span> <span data-ttu-id="82807-126">根據預設， [**WinHttpRequest**](winhttprequest.md) 物件會使用 proxy 設定工具設定。</span><span class="sxs-lookup"><span data-stu-id="82807-126">The [**WinHttpRequest**](winhttprequest.md) object uses the proxy configuration tool settings by default.</span></span>

<span data-ttu-id="82807-127">WinHTTP 的 proxy 設定不是 Microsoft Internet Explorer 的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-127">The proxy settings for WinHTTP are not the proxy settings for Microsoft Internet Explorer.</span></span> <span data-ttu-id="82807-128">您無法在 Microsoft Windows 主控台中設定 WinHTTP 的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-128">You cannot configure the proxy settings for WinHTTP in the Microsoft Windows Control Panel.</span></span> <span data-ttu-id="82807-129">使用 WinHTTP proxy 設定公用程式並不會改變您用來 Internet Explorer 的設定。</span><span class="sxs-lookup"><span data-stu-id="82807-129">Using the WinHTTP proxy configuration utility does not alter the settings you use for Internet Explorer.</span></span>

> [!Note]  
> <span data-ttu-id="82807-130">如果您嘗試使用 WinHTTP 開啟和傳送 HTTP 要求，但 proxy 設定不正確，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="82807-130">If you attempt to open and send an HTTP request using WinHTTP and the proxy settings are incorrect, an error occurs.</span></span>

 

## <a name="command-line-parameters"></a><span data-ttu-id="82807-131">命令列參數</span><span class="sxs-lookup"><span data-stu-id="82807-131">Command Line Parameters</span></span>

<span data-ttu-id="82807-132">下表列出可搭配 ProxyCfg.exe 工具使用的命令列參數。</span><span class="sxs-lookup"><span data-stu-id="82807-132">The following table lists the command line parameters available for use with the ProxyCfg.exe tool.</span></span>



| <span data-ttu-id="82807-133">參數</span><span class="sxs-lookup"><span data-stu-id="82807-133">Parameter</span></span> | <span data-ttu-id="82807-134">Description</span><span class="sxs-lookup"><span data-stu-id="82807-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82807-135">無</span><span class="sxs-lookup"><span data-stu-id="82807-135">none</span></span>      | <span data-ttu-id="82807-136">如果未指定任何參數，則會顯示目前的 WinHTTP proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-136">When no parameters are specified, the current WinHTTP proxy settings are displayed.</span></span>                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="82807-137">?</span><span class="sxs-lookup"><span data-stu-id="82807-137">?</span></span>         | <span data-ttu-id="82807-138">說明資訊隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="82807-138">Help information is displayed.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="82807-139">d</span><span class="sxs-lookup"><span data-stu-id="82807-139">d</span></span>         | <span data-ttu-id="82807-140">指定 WinHTTP 應用程式直接存取網路，而不使用 proxy。</span><span class="sxs-lookup"><span data-stu-id="82807-140">Specifies that WinHTTP applications access the network directly, without a proxy.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="82807-141">p</span><span class="sxs-lookup"><span data-stu-id="82807-141">p</span></span>         | <span data-ttu-id="82807-142">指定 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="82807-142">Specifies the proxy server.</span></span> <span data-ttu-id="82807-143">您也可以指定不使用 proxy 存取的選擇性伺服器清單。</span><span class="sxs-lookup"><span data-stu-id="82807-143">You can also specify an optional list of servers that are accessed without a proxy.</span></span>                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="82807-144">u</span><span class="sxs-lookup"><span data-stu-id="82807-144">u</span></span>         | <span data-ttu-id="82807-145">指定 WinHTTP 應用程式使用目前使用者的 proxy 設定進行 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="82807-145">Specifies that WinHTTP applications use the current user's proxy settings for Internet Explorer.</span></span> <span data-ttu-id="82807-146">如果 Internet Explorer 自動偵測 proxy 設定，或使用自動設定 URL 來設定 proxy 資訊，則此參數無法運作。</span><span class="sxs-lookup"><span data-stu-id="82807-146">This parameter does not work if Internet Explorer is automatically detecting proxy settings, or if it is using an automatic configuration URL to set the proxy information.</span></span>                                                                                                                                                      |
| <span data-ttu-id="82807-147">i</span><span class="sxs-lookup"><span data-stu-id="82807-147">i</span></span>         | <span data-ttu-id="82807-148">指定 WinHTTP 應用程式使用目前使用者的 proxy 設定進行 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="82807-148">Specifies that WinHTTP applications use the current user's proxy settings for Internet Explorer.</span></span> <span data-ttu-id="82807-149">這僅適用于先前未使用 ProxyCfg.exe 時。</span><span class="sxs-lookup"><span data-stu-id="82807-149">This only works when ProxyCfg.exe was not previously used.</span></span> <span data-ttu-id="82807-150">如果已安裝 ProxyCfg.exe，請指定 "u" 命令列參數使用手動設定。</span><span class="sxs-lookup"><span data-stu-id="82807-150">If ProxyCfg.exe is installed, specify that the "u" command line parameter use the manual settings.</span></span> <span data-ttu-id="82807-151">如果 Internet Explorer 自動偵測 proxy 設定，或使用自動設定 URL 來設定 proxy 資訊，則此參數無法運作。</span><span class="sxs-lookup"><span data-stu-id="82807-151">This parameter does not work if Internet Explorer automatically detects proxy settings, or if it uses an automatic configuration URL to set the proxy information.</span></span> |



 

<span data-ttu-id="82807-152">您可以在以空格分隔的字串中指定 proxy。</span><span class="sxs-lookup"><span data-stu-id="82807-152">You can specify proxies in a space-delimited string.</span></span> <span data-ttu-id="82807-153">Proxy 清單可以包含用來存取 proxy 的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="82807-153">The proxy listings can contain the port number that is used to access the proxy.</span></span> <span data-ttu-id="82807-154">若要列出特定通訊協定的 proxy，字串必須遵循下列格式： <protocol> = HTTPs://<proxy \_ 名稱>。</span><span class="sxs-lookup"><span data-stu-id="82807-154">To list a proxy for a specific protocol, the string must follow the format, <protocol>=https://<proxy\_name>.</span></span> <span data-ttu-id="82807-155">有效的通訊協定為 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="82807-155">The valid protocols are HTTP and HTTPS.</span></span> <span data-ttu-id="82807-156">例如，若要列出 HTTP proxy，有效的字串為 HTTP = https://http\_proxy\_name:80 ，其中 HTTP \_ proxy \_ 名稱是 proxy 伺服器的名稱，而80則是您必須用來存取 proxy 的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="82807-156">For example, to list an HTTP proxy, a valid string is http=https://http\_proxy\_name:80, where http\_proxy\_name is the name of the proxy server and 80 is the port number that you must use to access the proxy.</span></span> <span data-ttu-id="82807-157">如果 proxy 使用該通訊協定的預設通訊埠號碼，則您可以省略埠號碼。</span><span class="sxs-lookup"><span data-stu-id="82807-157">If the proxy uses the default port number for that protocol, then you can omit the port number.</span></span> <span data-ttu-id="82807-158">如果 proxy 名稱本身列出，您可以使用它做為任何沒有指定 proxy 之通訊協定的預設 proxy。</span><span class="sxs-lookup"><span data-stu-id="82807-158">If a proxy name is listed by itself, you can use it as the default proxy for any protocols that do not have a specified proxy.</span></span> <span data-ttu-id="82807-159">例如，HTTP = https://http\_proxy 其他 \_ proxy 會 \_ 對任何 HTTP 作業使用 HTTP PROXY，而 HTTPS 通訊協定會使用名為其他 \_ proxy 的 proxy。</span><span class="sxs-lookup"><span data-stu-id="82807-159">For example, http=https://http\_proxy other\_proxy uses http\_proxy for any HTTP operations, while the HTTPS protocol uses the proxy named other\_proxy.</span></span>

<span data-ttu-id="82807-160">您可以在 [proxy 略過] 清單中列出本機已知的主機名稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="82807-160">You can list locally known host names or IP addresses in the proxy bypass list.</span></span> <span data-ttu-id="82807-161">這份清單可以包含萬用字元，例如 " \* "，這會導致應用程式針對符合指定模式的位址略過 proxy 伺服器，例如 " \* . microsoft.com" 或 " \* org"。</span><span class="sxs-lookup"><span data-stu-id="82807-161">This list can contain wildcards, such as "\*", that cause the application to bypass the proxy server for addresses that fit the specified pattern, for example, "\*.microsoft.com" or "\*.org".</span></span> <span data-ttu-id="82807-162">萬用字元必須是清單中最左邊的字元。</span><span class="sxs-lookup"><span data-stu-id="82807-162">Wildcard characters must be the left-most characters in the list.</span></span> <span data-ttu-id="82807-163">例如，"aaa"。 \*不受支援。</span><span class="sxs-lookup"><span data-stu-id="82807-163">For example, "aaa.\*" is not supported.</span></span> <span data-ttu-id="82807-164">若要列出多個位址和主機名稱，請在 proxy 略過字串中使用空格或分號分隔。</span><span class="sxs-lookup"><span data-stu-id="82807-164">To list multiple addresses and host names, separate them with blank spaces or semicolons in the proxy bypass string.</span></span> <span data-ttu-id="82807-165">如果您指定 <local> 宏，函式會略過不包含句號的任何主機名稱。</span><span class="sxs-lookup"><span data-stu-id="82807-165">If you specify the <local> macro, the function bypasses any host name that does not contain a period.</span></span>

> [!WARNING]
> <span data-ttu-id="82807-166">Proxycfg.exe 執行之後，您就無法還原先前的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-166">After Proxycfg.exe runs, you cannot restore the previous proxy settings.</span></span> <span data-ttu-id="82807-167">不過，您可以完全移除 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-167">However, you can remove the proxy settings entirely.</span></span>

 

## <a name="usage"></a><span data-ttu-id="82807-168">使用方式</span><span class="sxs-lookup"><span data-stu-id="82807-168">Usage</span></span>

<span data-ttu-id="82807-169">若要使用 proxy 設定工具，請開啟命令提示字元視窗，然後使用適當的命令列參數來執行 proxy 設定公用程式。</span><span class="sxs-lookup"><span data-stu-id="82807-169">To use the proxy configuration tool, open a command prompt window and run the proxy configuration utility with the appropriate command line parameters.</span></span> <span data-ttu-id="82807-170">下一節提供語法範例。</span><span class="sxs-lookup"><span data-stu-id="82807-170">The following section provides syntax examples.</span></span>

## <a name="example-syntax"></a><span data-ttu-id="82807-171">範例語法</span><span class="sxs-lookup"><span data-stu-id="82807-171">Example Syntax</span></span>

### <a name="example-1-use-a-proxy-only-for-external-resources"></a><span data-ttu-id="82807-172">範例1：僅針對外部資源使用 proxy</span><span class="sxs-lookup"><span data-stu-id="82807-172">Example 1: Use a proxy only for external resources</span></span>

<span data-ttu-id="82807-173">以下是最常見的 Proxycfg.exe 用途。</span><span class="sxs-lookup"><span data-stu-id="82807-173">The following is the most common use for Proxycfg.exe.</span></span> <span data-ttu-id="82807-174">此命令會指定透過名為「proxy 伺服器」的 proxy 伺服器來存取 HTTP 和 HTTPS 伺服器 \_ ，但不包含句點的主機名稱除外。</span><span class="sxs-lookup"><span data-stu-id="82807-174">This command specifies that both HTTP and HTTPS servers are accessed through the proxy server named "proxy\_server", except for host names that do not contain a period.</span></span>

<span data-ttu-id="82807-175">**proxycfg.exe-p proxy \_ 伺服器 " <local> "**</span><span class="sxs-lookup"><span data-stu-id="82807-175">**proxycfg -p proxy\_server "<local>"**</span></span>

### <a name="example-2-use-a-proxy-for-all-resources"></a><span data-ttu-id="82807-176">範例2：針對所有資源使用 proxy</span><span class="sxs-lookup"><span data-stu-id="82807-176">Example 2: Use a proxy for all resources</span></span>

<span data-ttu-id="82807-177">下列範例會指定透過名為「proxy 伺服器」的 proxy 伺服器來存取 HTTP 和 HTTPS 伺服器 \_ 。</span><span class="sxs-lookup"><span data-stu-id="82807-177">The following example specifies that both HTTP and HTTPS servers are accessed through the proxy server named "proxy\_server".</span></span> <span data-ttu-id="82807-178">未指定任何略過清單。</span><span class="sxs-lookup"><span data-stu-id="82807-178">No bypass list is specified.</span></span>

<span data-ttu-id="82807-179">**proxycfg.exe-p proxy \_ 伺服器**</span><span class="sxs-lookup"><span data-stu-id="82807-179">**proxycfg -p proxy\_server**</span></span>

### <a name="example-3-use-a-different-proxy-for-secure-resources"></a><span data-ttu-id="82807-180">範例3：針對安全資源使用不同的 proxy</span><span class="sxs-lookup"><span data-stu-id="82807-180">Example 3: Use a different proxy for secure resources</span></span>

<span data-ttu-id="82807-181">下列範例會指定透過 HTTP proxy proxy 存取 HTTP 伺服器 \_ ，並透過 HTTPs proxy 存取 HTTPs 伺服器 \_ 。</span><span class="sxs-lookup"><span data-stu-id="82807-181">The following example specifies that HTTP servers are accessed through the http\_proxy proxy and HTTPS servers are accessed through https\_proxy.</span></span> <span data-ttu-id="82807-182">近端內部網路網站與 microsoft.com 網域中的任何網站都會 \* 略過 proxy。</span><span class="sxs-lookup"><span data-stu-id="82807-182">Local intranet sites and any site in the \*.microsoft.com domain bypass the proxy.</span></span>

<span data-ttu-id="82807-183">**proxycfg.exe-p "HTTP = HTTP \_ proxy HTTPs = HTTPs \_ proxy" " <local> ; \* 。microsoft.com "**</span><span class="sxs-lookup"><span data-stu-id="82807-183">**proxycfg -p "http=http\_proxy https=https\_proxy" "<local>;\*.microsoft.com"**</span></span>

## <a name="removing-proxycfgexe"></a><span data-ttu-id="82807-184">移除 ProxyCfg.exe</span><span class="sxs-lookup"><span data-stu-id="82807-184">Removing ProxyCfg.exe</span></span>

<span data-ttu-id="82807-185">使用 proxy 設定工具之後，您就無法還原原始 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-185">After using the proxy configuration tool, you cannot restore your original proxy settings.</span></span> <span data-ttu-id="82807-186">不過，如有必要，您可以移除公用程式所建立的登錄設定。</span><span class="sxs-lookup"><span data-stu-id="82807-186">However, if necessary, you can remove the registry settings that the utility creates.</span></span> <span data-ttu-id="82807-187">若要移除 ProxyCfg.exe 建立的登錄專案，您必須從下列登錄機碼中刪除 **WinHttpSettings** 值。</span><span class="sxs-lookup"><span data-stu-id="82807-187">To remove the registry entries that ProxyCfg.exe creates, you must delete the **WinHttpSettings** value from the following registry key.</span></span>

<span data-ttu-id="82807-188">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **網際網路設定** \\ **連接** \\ **WinHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="82807-188">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Internet Settings**\\**Connections**\\**WinHttpSettings**</span></span>

<span data-ttu-id="82807-189">刪除 *WinHttpSettings* 值會移除所有的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="82807-189">Deleting the *WinHttpSettings* value removes all proxy configurations.</span></span>

## <a name="proxycfgexe-and-authentication"></a><span data-ttu-id="82807-190">ProxyCfg.exe 和驗證</span><span class="sxs-lookup"><span data-stu-id="82807-190">ProxyCfg.exe and Authentication</span></span>

<span data-ttu-id="82807-191">Proxy 設定公用程式會設定預設的驗證原則。</span><span class="sxs-lookup"><span data-stu-id="82807-191">The proxy configuration utility sets the default authentication policy.</span></span> <span data-ttu-id="82807-192">因為您不應該使用不受信任的主機執行 NTLM 驗證，所以根據預設，NTLM 驗證只會自動在 proxy 略過清單上與主機一起進行。</span><span class="sxs-lookup"><span data-stu-id="82807-192">Because you should not perform NTLM authentication with untrusted hosts, by default, NTLM authentication only occurs automatically with hosts on the proxy bypass list.</span></span> <span data-ttu-id="82807-193">如果沒有 proxy，您仍然可以使用 ProxyCfg.exe 來指定您信任用來執行 NTLM 驗證之主機的略過清單。</span><span class="sxs-lookup"><span data-stu-id="82807-193">If there is no proxy, you can still use ProxyCfg.exe to specify a bypass list of hosts that you trust to perform NTLM authentication.</span></span> <span data-ttu-id="82807-194">基於此目的使用 ProxyCfg.exe 時需要 proxy 名稱，但您可以使用任何有效的字串來取代實際的 proxy 名稱。</span><span class="sxs-lookup"><span data-stu-id="82807-194">A proxy name is required when using ProxyCfg.exe for this purpose, but you can use any valid string in place of a real proxy name.</span></span>

<span data-ttu-id="82807-195">如需有關自動登入原則的詳細資訊，請參閱 [自動登入原則](authentication-in-winhttp.md)。</span><span class="sxs-lookup"><span data-stu-id="82807-195">For more information about the auto-logon policy, see [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

 

 
