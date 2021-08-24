---
title: WinINet 與 WinHTTP
description: 瞭解如何在 WinInet 和 WinHTTP 之間進行選擇。 閱讀功能的比較和檢查相關主題。
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- WinINet 與 WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: 20bd0ced1d0ea897dba05680258cae4a2b1a248b204824ded7d2ec5be30ff00b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899088"
---
# <a name="wininet-vs-winhttp"></a>WinINet 與 WinHTTP

有幾個例外狀況， [WinINet](portal.md) 是 [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)的超集合。 當您在這兩者之間進行選取時，除非您打算在需要模擬和會話隔離的服務或類似服務的進程內執行，否則您應該使用 WinINet。

## <a name="comparison-of-features"></a>功能比較

| 功能 | WinINet | WinHTTP |
|-|-|-|
| **認證** 快取允許 Windows Internet Explorer 中的所有內建應用程式自動取得認證。 它也允許在 Internet Explorer 外部執行的應用程式，只會提示/指定伺服器的認證一次。 然後，要求上的會自動。 | 是 | 否 |
| **認證提示** 提供可讓呼叫程式碼提示使用者輸入認證的 API。 | 是 | 否 |
| **FTP** | 是 | 否 |
| **自動撥號/RAS 支援** 這是舊版的功能。 請改用 [遠端存取](/windows/desktop/RRAS/portal) 。 | 是 | 否 |
| **區域** 自動整合 Internet Explorer 安全性區域。 | 是 | 否 |
| **IDNA 支援** IDNA RFC/Punycode 的整合式支援。 | 是 | 是 |
| **Cookie Jar api** 支援持續性和非持續性 cookie。 任何應用程式或腳本都可以使用它來查看與瀏覽器相同的 cookie。 | 是 | 否 |
| **受保護模式 IE 支援** | 是 | 否 |
| **解壓縮支援** 支援 gzip 和 deflate 壓縮配置。 | 是 | 是 |
| **區塊 Upload 支援** 用戶端程式代碼必須執行區塊化。 | 否 | 是 |
| **SOCKS V4 支援** 不包含 v4a 或 v5。 | 是 | 否 |
| **雙向傳送和接收** | 否 | 否 |
| **重迭 i/o** | 否 | 否 |
| 檔案 **配置支援** 適用于具有檔案配置的 proxy 腳本。 | 是 | 否 |
| **InternetOpenUrl** 簡化的程式碼以開啟 URL。 | 是 | 否 |
| **服務支援** 可以從服務或服務帳戶執行。 | 否 | 是 |
| **會話隔離** 不同的會話不會互相影響。 | 否 | 是 |
| 模擬支援線上程模擬不同使用者時呼叫。 | 否 | 是 |

## <a name="related-topics"></a>相關主題

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [WinINet](/windows/desktop/WinInet/about-wininet)