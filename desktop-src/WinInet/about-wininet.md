---
title: 關於 WinINet
description: Windows Internet (WinINet) 應用程式開發介面 (API) 可讓您的應用程式與 FTP 和 HTTP 通訊協定互動以存取網際網路資源。
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- 關於 WinINet WinINet
- WinINet WinINet，關於
- WinINet WinINet，起始頁
- Windows 網際網路 WinINet
- 網際網路，Windows 網際網路 WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103932968"
---
# <a name="about-wininet"></a>關於 WinINet

> [!NOTE]
> 針對應用程式容器，自 Windows 10，版本1709，HTTP/2 (請參閱 [RFC7540](https://tools.ietf.org/html/rfc7540)) 預設為開啟。

Windows Internet (WinINet) 應用程式開發介面 (API) 可讓您的應用程式與 FTP 和 HTTP 通訊協定互動以存取網際網路資源。 當標準演進時，這些函式會處理基礎通訊協定中的變更，讓它們能夠維持一致的行為。

**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：** 也啟用了與 Gopher 互動的應用程式。

如需詳細資訊，請參閱

-   [WinINet 與 WinHTTP](wininet-vs-winhttp.md)
-   [HINTERNET 控制碼](appendix-a-hinternet-handles.md)
-   [IP 版本6支援](ip-version-6-support.md)
-   [內容 \_ 編碼](content-encoding.md)
-   [Caching](caching.md)
-   [一般函數](common-functions.md)
-   [FTP 會話](ftp-sessions.md)
-   [HTTP 會話](http-sessions.md)
-   [HTTP Cookie](http-cookies.md)
-   [非同步作業](asynchronous-operation.md)
-   [處理驗證](handling-authentication.md)
-   [處理統一資源定位器](handling-uniform-resource-locators.md)
-   [安全性 \_ 指導方針](security-guidelines.md)

## <a name="internet-protocols"></a>網際網路通訊協定

這兩個主要的網際網路通訊協定是 FTP 和 HTTP。 如需這些通訊協定的詳細資訊，請參閱適用于 FTP 和 HTTP 的 (RFC) 檔的批註要求：

-   [RFC 959](https://www.ietf.org/rfc/rfc0959.txt)， *檔案傳輸通訊協定 (FTP)*。
-   [RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt)， *超文字傳輸通訊協定-HTTP/1.0*。
-   [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)， *超文字傳輸通訊協定-HTTP/1.1*。

> [!NOTE]  
>  (這些資源可能無法在某些語言及國家/地區使用。 ) 

**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：** 此外也支援 Gopher 通訊協定。 請參閱 [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt)（ *網際網路 Gopher 通訊協定*）。
