---
description: Microsoft 已將延伸模組的陣列實作為導覽器自動設定檔案格式，以便在 WinINet 和 WinHTTP WPAD helper 函式中新增 IPv6 支援。
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: 瀏覽器自動設定檔案格式的 IPv6 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b57fce93caaf7790136ee9ac7db04017d9ac11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994477"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a><span data-ttu-id="ccfc5-103">瀏覽器自動設定檔案格式的 IPv6 擴充功能</span><span class="sxs-lookup"><span data-stu-id="ccfc5-103">IPv6 Extensions to Navigator Auto-Config File Format</span></span>

<span data-ttu-id="ccfc5-104">Microsoft 已將延伸模組的陣列實作為導覽器自動設定檔案格式，以便在 WinINet 和 WinHTTP WPAD helper 函式中新增 IPv6 支援。</span><span class="sxs-lookup"><span data-stu-id="ccfc5-104">Microsoft has implemented an array of extensions to the Navigator Auto-Config File Format in order to add IPv6 support in the WinINet and WinHTTP WPAD helper functions.</span></span>

<span data-ttu-id="ccfc5-105">最晚在1990年的網際網路爆炸造成了未預期的 IPv4 位址水源不足情形，且每天都會消耗殆盡集區。</span><span class="sxs-lookup"><span data-stu-id="ccfc5-105">The explosion of the Internet in the late 1990’s has caused an unexpected scarcity of IPv4 addresses, with the pool depleting on a daily basis.</span></span> <span data-ttu-id="ccfc5-106">IPv6 提供解決此問題的解決方案，雖然目前尚未廣泛部署，但其使用方式肯定會在未來更普遍。</span><span class="sxs-lookup"><span data-stu-id="ccfc5-106">IPv6 provides a solution to this problem and although it is currently not widely deployed, its use will definitely become more prevalent in the future.</span></span> <span data-ttu-id="ccfc5-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) 是一種通訊協定，可讓 web 用戶端自動偵測其連出流量的正確 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="ccfc5-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) is a protocol that allows web clients to automatically detect what the correct proxy configuration should be for their outgoing traffic.</span></span> <span data-ttu-id="ccfc5-108">這對公司部署而言非常有用，因為它可讓 IT 系統管理員設定複雜的腳本，以根據用戶端嘗試連線的目標伺服器，將所有用戶端的流量路由傳送至特定的 proxy。</span><span class="sxs-lookup"><span data-stu-id="ccfc5-108">This is very useful for corporate deployments because it allows IT administrators to setup complex scripts that can route traffic for all clients to specific proxies based on the target server the clients are attempting to connect to.</span></span> <span data-ttu-id="ccfc5-109">WinINet 和 WinHTTP 支援依導覽器 [Proxy 自動設定 (PAC) 檔案格式規格](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html)所定義的 WPAD 協助程式函式，這項功能已成為事實標準。</span><span class="sxs-lookup"><span data-stu-id="ccfc5-109">WinINet and WinHTTP support WPAD helper functions as defined by the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), which has become a defacto standard.</span></span> <span data-ttu-id="ccfc5-110">可惜的是，此規格是以1996撰寫，且不會定義在具有 IPv6 功能的網路中部署 WPAD 腳本時的函式行為。</span><span class="sxs-lookup"><span data-stu-id="ccfc5-110">Unfortunately this specification was written in 1996 and does not define what the function behaviors should be when a WPAD script is deployed in an IPv6 capable network.</span></span>

<span data-ttu-id="ccfc5-111">由於 IPv6 是未來的浪潮，因此所有 Windows 元件現在都支援 (IPv4 和 IPv6) 和 IPv6 私人網路絡的雙協定堆疊。</span><span class="sxs-lookup"><span data-stu-id="ccfc5-111">Since IPv6 is the wave of the future, all Windows components now support dual stack (IPv4 and IPv6) and IPv6 only networks.</span></span> <span data-ttu-id="ccfc5-112">為了支援 IPv6，而不會影響現有的部署，Microsoft 將6個新的 helper 類別功能新增為 Navigator Proxy 自動設定 (PAC) 檔案格式規格的延伸模組，並新增一個名為 **FindProxyForURLEx** 的新 IPv6 功能，讓系統管理員可以在 WPAD 腳本中執行此功能。</span><span class="sxs-lookup"><span data-stu-id="ccfc5-112">In order to support IPv6 without affecting existing deployment, Microsoft added 6 new helper class functions as an extension to the Navigator Proxy Auto-Config (PAC) File Format specification and also added a new IPv6 capable function called **FindProxyForURLEx** that administrators can implement in the WPAD script.</span></span>

<dl> <dt>

[<span data-ttu-id="ccfc5-113">IPv6 感知 Proxy Helper API 定義</span><span class="sxs-lookup"><span data-stu-id="ccfc5-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[<span data-ttu-id="ccfc5-114">IPv6-Aware WPAD Helper 函式和舊版 WPAD Helper 函數之間的差異</span><span class="sxs-lookup"><span data-stu-id="ccfc5-114">Differences Between IPv6-Aware WPAD Helper Functions and Legacy WPAD Helper Functions</span></span>](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
<span data-ttu-id="ccfc5-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ccfc5-115"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="ccfc5-116">這種功能需要 Windows Internet Explorer 7 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ccfc5-116">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



