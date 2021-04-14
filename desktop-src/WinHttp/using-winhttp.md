---
description: 本節說明如何使用適用于 Microsoft Windows HTTP Services (WinHTTP) 的 C/c + + API，以及 WinHttpRequest 物件所公開的 COM 介面。
ms.assetid: 16178bb8-5e95-46a5-825a-880edc402445
title: 使用 WinHTTP
ms.topic: article
ms.date: 07/22/2020
ms.openlocfilehash: cda0a7772b88dfd9c03675c522f4b7504ea00b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469085"
---
# <a name="using-winhttp"></a><span data-ttu-id="b5779-103">使用 WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b5779-103">Using WinHTTP</span></span>

<span data-ttu-id="b5779-104">本節說明如何使用適用于 Microsoft Windows HTTP Services (WinHTTP) 的 C/c + + API，以及 **WinHttpRequest** 物件所公開的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="b5779-104">This section describes how to use both the C/C++ API for Microsoft Windows HTTP Services (WinHTTP) and the COM interface exposed by the **WinHttpRequest** Object.</span></span> <span data-ttu-id="b5779-105">如需這些介面的比較，請參閱 [選擇 WinHTTP 介面](choosing-a-winhttp-interface.md) 。</span><span class="sxs-lookup"><span data-stu-id="b5779-105">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span> <span data-ttu-id="b5779-106">它也會說明如何使用 WinHTTP 隨附的系統管理工具。</span><span class="sxs-lookup"><span data-stu-id="b5779-106">It also describes how to use the administrative tools included with WinHTTP.</span></span>

## <a name="how-to-topics"></a><span data-ttu-id="b5779-107">如何主題</span><span class="sxs-lookup"><span data-stu-id="b5779-107">How-To Topics</span></span>

[<span data-ttu-id="b5779-108">使用 WinHTTP C/c + + API</span><span class="sxs-lookup"><span data-stu-id="b5779-108">Using the WinHTTP C/C++ API</span></span>](using-the-winhttp-c-c---api.md)

-   [<span data-ttu-id="b5779-109">WinHTTP 會話總覽</span><span class="sxs-lookup"><span data-stu-id="b5779-109">WinHTTP Sessions Overview</span></span>](winhttp-sessions-overview.md)
-   [<span data-ttu-id="b5779-110">WinHTTP 中的 HINTERNET 控制碼</span><span class="sxs-lookup"><span data-stu-id="b5779-110">HINTERNET Handles in WinHTTP</span></span>](hinternet-handles-in-winhttp.md)
-   [<span data-ttu-id="b5779-111">WinHTTP 中)  (Url 的統一資源定位器</span><span class="sxs-lookup"><span data-stu-id="b5779-111">Uniform Resource Locators (URLs) in WinHTTP</span></span>](uniform-resource-locators--urls--in-winhttp.md)
-   [<span data-ttu-id="b5779-112">WinHTTP 中的驗證</span><span class="sxs-lookup"><span data-stu-id="b5779-112">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
-   [<span data-ttu-id="b5779-113">WinHTTP 中的 Passport 驗證</span><span class="sxs-lookup"><span data-stu-id="b5779-113">Passport Authentication in WinHTTP</span></span>](passport-authentication-in-winhttp.md)
-   [<span data-ttu-id="b5779-114">WinHTTP 中的 SSL</span><span class="sxs-lookup"><span data-stu-id="b5779-114">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
-   [<span data-ttu-id="b5779-115">使用 WinHTTP 作為並存元件</span><span class="sxs-lookup"><span data-stu-id="b5779-115">Using WinHTTP as a Side-by-side Assembly</span></span>](using-winhttp-as-a-side-by-side-assembly.md)
-   [<span data-ttu-id="b5779-116">WinHTTP 中的 Cookie 處理</span><span class="sxs-lookup"><span data-stu-id="b5779-116">Cookie Handling in WinHTTP</span></span>](cookie-handling-in-winhttp.md)
-   [<span data-ttu-id="b5779-117">WinHTTP 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="b5779-117">Error Handling in WinHTTP</span></span>](error-handling-in-winhttp.md)
-   [<span data-ttu-id="b5779-118">WinHTTP 自動代理支援</span><span class="sxs-lookup"><span data-stu-id="b5779-118">WinHTTP AutoProxy Support</span></span>](winhttp-autoproxy-support.md)

[<span data-ttu-id="b5779-119">使用 WinHttpRequest COM 物件</span><span class="sxs-lookup"><span data-stu-id="b5779-119">Using the WinHttpRequest COM Object</span></span>](using-the-winhttprequest-com-object.md)

-   [<span data-ttu-id="b5779-120">使用腳本來抓取資料</span><span class="sxs-lookup"><span data-stu-id="b5779-120">Retrieving Data Using Script</span></span>](retrieving-data-using-script.md)
-   [<span data-ttu-id="b5779-121">使用腳本進行驗證</span><span class="sxs-lookup"><span data-stu-id="b5779-121">Authentication Using Script</span></span>](authentication-using-script.md)

[<span data-ttu-id="b5779-122">使用 WinHTTP 工具</span><span class="sxs-lookup"><span data-stu-id="b5779-122">Using WinHTTP Tools</span></span>](using-winhttp-tools.md)

-   [<span data-ttu-id="b5779-123">WinHttpCfg.exe，憑證設定工具</span><span class="sxs-lookup"><span data-stu-id="b5779-123">WinHttpCfg.exe, a Certificate Configuration Tool</span></span>](winhttpcertcfg-exe--a-certificate-configuration-tool.md)
-   [<span data-ttu-id="b5779-124">ProxyCfg.exe，Proxy 設定工具</span><span class="sxs-lookup"><span data-stu-id="b5779-124">ProxyCfg.exe, a Proxy Configuration Tool</span></span>](proxycfg-exe--a-proxy-configuration-tool.md)
-   [<span data-ttu-id="b5779-125">WinHttpTraceCfg，Trace Configuration Tool</span><span class="sxs-lookup"><span data-stu-id="b5779-125">WinHttpTraceCfg, a Trace Configuration Tool</span></span>](winhttptracecfg-exe--a-trace-configuration-tool.md)

 

 



