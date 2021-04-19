---
description: 為了充分利用已啟用 IPv6 的函式，IT 系統管理員必須在其 WPAD 腳本內定義，此函式稱為 FindProxyForURLEx (url，主機) ，其將取代舊版 FindProxyForUrl (url、host) 函數。
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: IPv6-Aware Proxy 協助程式 API 定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988966"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a>IPv6-Aware Proxy 協助程式 API 定義

為了充分利用已啟用 IPv6 的函式，IT 系統管理員必須在其 WPAD 腳本內定義，此函式稱為 FindProxyForURLEx (url，主機) ，其將取代舊版 FindProxyForUrl (url、host) 函數。 只有在新的 FindProxyForURLEx 函式中，系統管理員才能執行新的功能。

我們也嘗試簡化開發人員的工作，方法是讓我們的函式以與其他網路元件相同的喜好設定順序傳回不同類型的 IP 位址，特別是 IPv6 位址，後面接著 IPv4 位址 (亦即 Winsock getaddrinfo ( 的目前行為。) 函式) 。

下列函式是導覽 [器 Proxy 自動設定 (PAC) 檔案格式規格](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) 的擴充功能，可讓 WPAD 腳本處理具備 IPv6 功能的網路。

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a>JavaScript 函式 FindProxyforURLEx 的預先定義函數和環境

以主機名稱為基礎的條件

<dl> <dt>

[**isResolvableEx**](isresolvableex.md)
</dt> <dd>

判斷指定的主機字串是否可解析為 IP 位址。

</dd> <dt>

[**isInNetEx**](isinnetex.md)
</dt> <dd>

判斷 IP 位址是否在特定子網中。

</dd> </dl>

相關公用程式函式

<dl> <dt>

[**dnsResolveEx**](dnsresolveex.md)
</dt> <dd>

將主機字串解析為其 IP 位址。

</dd> <dt>

[**myIPAddressEx**](myipaddressex.md)
</dt> <dd>

尋找 localhost 的所有 IP 位址。

</dd> <dt>

[**sortIpAddressList**](sortipaddresslist.md)
</dt> <dd>

排序 IP 位址清單。

</dd> <dt>

[**getClientVersion**](getclientversion.md)
</dt> <dd>

取得 WPAD 處理引擎的版本。

</dd> </dl>

> [!Note]  
> 這種功能需要 Windows Internet Explorer 7 或更新版本。

 

 

 



