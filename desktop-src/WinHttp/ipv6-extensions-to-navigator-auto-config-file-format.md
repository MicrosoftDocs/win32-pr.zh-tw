---
description: Microsoft 已將延伸模組的陣列實作為導覽器自動設定檔案格式，以便在 WinINet 和 WinHTTP WPAD helper 函式中新增 IPv6 支援。
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: 瀏覽器自動設定檔案格式的 IPv6 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a6db6d687cfde0c3289026e8fa36c77c3ff5372727d1604652160b0683169b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644007"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a>瀏覽器自動設定檔案格式的 IPv6 擴充功能

Microsoft 已將延伸模組的陣列實作為導覽器自動設定檔案格式，以便在 WinINet 和 WinHTTP WPAD helper 函式中新增 IPv6 支援。

最晚在1990年的網際網路爆炸造成了未預期的 IPv4 位址水源不足情形，且每天都會消耗殆盡集區。 IPv6 提供解決此問題的解決方案，雖然目前尚未廣泛部署，但其使用方式肯定會在未來更普遍。 [WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) 是一種通訊協定，可讓 web 用戶端自動偵測其連出流量的正確 proxy 設定。 這對公司部署而言非常有用，因為它可讓 IT 系統管理員設定複雜的腳本，以根據用戶端嘗試連線的目標伺服器，將所有用戶端的流量路由傳送至特定的 proxy。 WinINet 和 WinHTTP 支援依導覽器 [Proxy 自動設定 (PAC) 檔案格式規格](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html)所定義的 WPAD 協助程式函式，這項功能已成為事實標準。 可惜的是，此規格是以1996撰寫，且不會定義在具有 IPv6 功能的網路中部署 WPAD 腳本時的函式行為。

因為 IPv6 是未來的浪潮，所以所有 Windows 元件現在都支援雙 stack (的 IPv4 和 ipv6) 以及僅限 IPv6 的網路。 為了支援 IPv6，而不會影響現有的部署，Microsoft 將6個新的 helper 類別功能新增為 Navigator Proxy 自動設定 (PAC) 檔案格式規格的延伸模組，並新增一個名為 **FindProxyForURLEx** 的新 IPv6 功能，讓系統管理員可以在 WPAD 腳本中執行此功能。

<dl> <dt>

[IPv6 感知 Proxy Helper API 定義](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[IPv6-Aware WPAD Helper 函式和舊版 WPAD Helper 函數之間的差異](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
</dt> <dd></dd> </dl>

> [!Note]  
> 這種功能需要 Windows Internet Explorer 7 或更新版本。

 

 

 



