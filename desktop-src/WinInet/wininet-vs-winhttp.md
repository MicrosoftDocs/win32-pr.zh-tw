---
title: WinINet 與 WinHTTP
description: 有幾個例外狀況，WinINet 是 WinHTTP 的超集合。 當您在這兩者之間進行選取時，除非您打算在需要模擬和會話隔離的服務或類似服務的進程內執行，否則您應該使用 WinINet。
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- WinINet 與 WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: c4d161992c2202505e8c84c660ca1edc92cc7993
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965663"
---
# <a name="wininet-vs-winhttp"></a>WinINet 與 WinHTTP

有幾個例外狀況， [WinINet](portal.md) 是 [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)的超集合。 當您在這兩者之間進行選取時，除非您打算在需要模擬和會話隔離的服務或類似服務的進程內執行，否則您應該使用 WinINet。

## <a name="comparison-of-features"></a>功能比較

| 功能 | WinINet | WinHTTP |
|-|-|-|
| **認證** 快取允許 Windows Internet Explorer 中的所有內建應用程式自動取得認證。 它也允許在 Internet Explorer 外部執行的應用程式，只會提示/指定伺服器的認證一次。 然後，要求上的會自動。 | 是 | 不可以 |
| **認證提示** 提供可讓呼叫程式碼提示使用者輸入認證的 API。 | 是 | 不可以 |
| **FTP** | 是 | 不可以 |
| **自動撥號/RAS 支援** 這是舊版的功能。 請改用 [遠端存取](/windows/desktop/RRAS/portal) 。 | 是 | 不可以 |
| **區域** 自動整合 Internet Explorer 安全性區域。 | 是 | 不可以 |
| **IDNA 支援** IDNA RFC/Punycode 的整合式支援。 | 是 | 是 |
| **Cookie Jar api** 支援持續性和非持續性 cookie。 任何應用程式或腳本都可以使用它來查看與瀏覽器相同的 cookie。 | 是 | 不可以 |
| **受保護模式 IE 支援** | 是 | 不可以 |
| **解壓縮支援** 支援 gzip 和 deflate 壓縮配置。 | 是 | 是 |
| **區塊上傳支援** 用戶端程式代碼必須執行區塊化。 | 不可以 | 是 |
| **SOCKS V4 支援** 不包含 v4a 或 v5。 | 是 | 不可以 |
| **雙向傳送和接收** | 否 | 不可以 |
| **重迭 i/o** | 否 | 不可以 |
| 檔案 **配置支援** 適用于具有檔案配置的 proxy 腳本。 | 是 | 不可以 |
| **InternetOpenUrl** 簡化的程式碼以開啟 URL。 | 是 | 不可以 |
| **服務支援** 可以從服務或服務帳戶執行。 | 不可以 | 是 |
| **會話隔離** 不同的會話不會互相影響。 | 不可以 | 是 |
| 模擬支援線上程模擬不同使用者時呼叫。 | 不可以 | 是 |

## <a name="related-topics"></a>相關主題

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [WinINet](/windows/desktop/WinInet/about-wininet)