---
title: IP 版本6支援
description: 從 IE7 和更新版本開始，WinINet 支援主機名稱中的 IPv6 常值，以及 URI 的授權單位部分。
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- IP 版本6支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a024c792995780769a078c84b0493b7abba8647189fa2cee835d93dcb83770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113628"
---
# <a name="ip-version-6-support"></a>IP 版本6支援

從 IE7 和更新版本開始，WinINet 支援主機名稱中的 IPv6 常值，以及 URI 的授權單位部分。 WinINet 也支援在 HTTP 通訊協定的相關部分（例如，在 Location 標頭中）使用 IPv6 常值。

## <a name="hostname-ipv6-literals-and-uri-components"></a>主機名稱 IPv6 常值和 URI 元件

WinINet 會根據 RFC 3513 中的規格來實行 IPv6 常值。 如這個 RFC 所指定，URI 中的 IPv6 常值必須以括弧括住。 例如，HTTPs:// \[ ：： 1 \] /是有效的 IPv6 URI; 不含括弧 (的格式無效 https://::1/) 。 不過，主機名稱 IPv6 常值不是 URI 的一部分，因此不需要用括弧括住;WinINet 可以接受兩種形式。 例如，"：： 1" 和 " \[ ：： 1 \] " 是 IPv6 主機名稱常值的可接受形式。 其他 Api （例如 WinSock API）也會接受這兩種形式。 因此，應用程式應該準備好處理這兩種形式的 IPv6 主機名稱常值。

## <a name="scope-id"></a>範圍識別碼

URI 中的 IPv6 常值位址可以包含範圍識別碼。 範圍識別碼可以是介面識別碼，例如 \[ FE80：： 1% 1 \] 。 URI 標準（記載于 RFC 3986 中）並不會定義範圍識別碼的語法，而在存在範圍識別碼時，URI 會視為非統一。 但是，WinINet 會接受 URI 的授權單位元件和主機名稱 IPv6 常值中的範圍識別碼。

存在於 URI 中時，IPv6 常值位址中的百分比字元 (% ) 必須是轉義百分比。 例如，範圍識別碼 FE80：： 2% 3 必須以 "HTTPs:// \[ FE80：： 2% 253/" 的 URI 形式出現 \] ，其中 %25 是十六進位編碼百分比字元 (% ) 。 如果應用程式從 Unicode API （例如 Winsock [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) API）抓取 URI，則應用程式必須在 URI 的主機名稱中加入% 字元 (% ) 的轉義版本。 若要建立 URI 的轉義版本，應用程式會呼叫 [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) ，並將 *dwFlags* 參數設定為 **ICU \_ ESCAPE \_ 授權** 單位，以及在 *lpUrlComponents* 參數中指定的 URL 元件結構中指定的 IPv6 主機名稱。

針對所有通訊端作業，WinINet 會使用範圍識別碼。 不過，因為範圍識別碼只有本機主機的重要性，所以不會在要求中做為 HTTP 通訊協定標頭的一部分傳送。 例如，呼叫 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 時，會以 *lpszUrl* 參數中的下列 URL 呼叫。

``` syntax
https://[fec0::2%251]:80/path.htm
```

傳送此 URL 的 HTTP 要求時，WinINet 會移除 URL 的範圍識別碼部分。 要求包含下列標頭：

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> WinINet 不支援伺服器實施。 此外，它不應該從服務使用。 若為伺服器執行或服務，請使用[Microsoft Windows HTTP 服務 (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。

 

 

 