---
description: Microsoft Windows HTTP Services (WinHTTP) 為開發人員提供 HTTP 用戶端應用程式開發介面， (API) 將要求透過 HTTP 通訊協定傳送給其他 HTTP 伺服器。
ms.assetid: 354ab65d-5e46-451d-b36b-2f8166a1a048
title: Windows HTTP 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f03a3204257410e4db0182724ab63743116f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991726"
---
# <a name="windows-http-services"></a><span data-ttu-id="99547-103">Windows HTTP 服務</span><span class="sxs-lookup"><span data-stu-id="99547-103">Windows HTTP Services</span></span>

## <a name="purpose"></a><span data-ttu-id="99547-104">目的</span><span class="sxs-lookup"><span data-stu-id="99547-104">Purpose</span></span>

<span data-ttu-id="99547-105">Microsoft Windows HTTP Services (WinHTTP) 為開發人員提供 HTTP 用戶端應用程式開發介面， (API) 將要求透過 HTTP 通訊協定傳送給其他 HTTP 伺服器。</span><span class="sxs-lookup"><span data-stu-id="99547-105">Microsoft Windows HTTP Services (WinHTTP) provides developers with an HTTP client application programming interface (API) to send requests through the HTTP protocol to other HTTP servers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="99547-106">適用時</span><span class="sxs-lookup"><span data-stu-id="99547-106">Where applicable</span></span>

<span data-ttu-id="99547-107">WinHTTP 支援桌面用戶端應用程式、Windows 服務和 Windows server 架構的應用程式。</span><span class="sxs-lookup"><span data-stu-id="99547-107">WinHTTP supports desktop client applications, Windows services, and Windows server-based applications.</span></span>

<span data-ttu-id="99547-108">如需有關如何針對以 Microsoft .NET Framework 為基礎的應用程式使用 WinHTTP 的詳細資訊，請參閱 [WINHTTPHANDLER API](/dotnet/api/system.net.http?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="99547-108">For more information on how to use WinHTTP for applications built on the Microsoft .NET Framework, see the [WinHttpHandler API](/dotnet/api/system.net.http?view=netframework-4.8)</span></span>

## <a name="developer-audience"></a><span data-ttu-id="99547-109">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="99547-109">Developer audience</span></span>

<span data-ttu-id="99547-110">WinHTTP 提供 (API) 的 C/c + + 應用程式開發介面，以及 (COM) 自動化元件的元件物件模型，適用于在 (ASP) 架構的應用程式中使用的 Active Server 網頁。</span><span class="sxs-lookup"><span data-stu-id="99547-110">WinHTTP offers both a C/C++ application programming interface (API) and a Component Object Model (COM) automation component suitable for use in Active Server Pages (ASP) based applications.</span></span>

<span data-ttu-id="99547-111">使用其中一個介面時，對 HTTP 通訊協定的基本瞭解相當重要。</span><span class="sxs-lookup"><span data-stu-id="99547-111">A basic understanding of the HTTP protocol is important to use either interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="99547-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="99547-112">Run-time requirements</span></span>

<span data-ttu-id="99547-113">WinHTTP 5.1 提供優於5.0 版的增強功能。</span><span class="sxs-lookup"><span data-stu-id="99547-113">WinHTTP 5.1 offers improvements over version 5.0.</span></span> <span data-ttu-id="99547-114">它包含在作業系統中。</span><span class="sxs-lookup"><span data-stu-id="99547-114">It is included in the operating system.</span></span> <span data-ttu-id="99547-115">如需新功能的詳細資訊，請參閱 [WinHTTP 5.1 的新](what-s-new-in-winhttp-5-1.md) 功能和 [windows Server 2008 和 Windows Vista 的新](what-s-new-in-windows-longhorn.md)功能。</span><span class="sxs-lookup"><span data-stu-id="99547-115">For more information about new features, see [What's New in WinHTTP 5.1](what-s-new-in-winhttp-5-1.md) and [What's New in Windows Server 2008 and Windows Vista](what-s-new-in-windows-longhorn.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99547-116">WinHTTP 5.0 下載已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="99547-116">The WinHTTP 5.0 download is no longer available.</span></span> <span data-ttu-id="99547-117">自2004年10月1日起，Microsoft 已移除從 MSDN 下載的 WinHTTP 5.0 SDK，並已終止版本5.0 的產品支援。</span><span class="sxs-lookup"><span data-stu-id="99547-117">As of October 1, 2004, Microsoft removed the WinHTTP 5.0 SDK download from MSDN and terminated product support for version 5.0.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="99547-118">本節內容</span><span class="sxs-lookup"><span data-stu-id="99547-118">In this section</span></span>

-   [<span data-ttu-id="99547-119">關於 WinHTTP</span><span class="sxs-lookup"><span data-stu-id="99547-119">About WinHTTP</span></span>](about-winhttp.md)
-   [<span data-ttu-id="99547-120">使用 WinHTTP</span><span class="sxs-lookup"><span data-stu-id="99547-120">Using WinHTTP</span></span>](using-winhttp.md)
-   [<span data-ttu-id="99547-121">WinHTTP 參考</span><span class="sxs-lookup"><span data-stu-id="99547-121">WinHTTP Reference</span></span>](winhttp-reference.md)

 

 
