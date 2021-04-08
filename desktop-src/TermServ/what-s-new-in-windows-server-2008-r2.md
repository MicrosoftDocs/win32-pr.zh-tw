---
title: Windows Server 2008 R2 的新功能
description: Windows Server 2008 R2 為遠端桌面服務引進了下列新的程式設計項目。
ms.assetid: 605a9a34-11fa-433a-9ccd-8368c75b10f0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fec9c29a142d8c97a17d4a73ee1015f84702851
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "103932886"
---
# <a name="whats-new-in-windows-server-2008-r2"></a><span data-ttu-id="682b6-103">Windows Server 2008 R2 的新功能</span><span class="sxs-lookup"><span data-stu-id="682b6-103">What's New in Windows Server 2008 R2</span></span>

<span data-ttu-id="682b6-104">Windows Server 2008 R2 為遠端桌面服務引進了下列新的程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="682b6-104">Windows Server 2008 R2 introduces the following new programming elements for Remote Desktop Services.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="682b6-105">終端機服務現在遠端桌面服務</span><span class="sxs-lookup"><span data-stu-id="682b6-105">Terminal Services Is Now Remote Desktop Services</span></span><br/></td>
<td><span data-ttu-id="682b6-106">終端機服務已重新命名為遠端桌面服務。</span><span class="sxs-lookup"><span data-stu-id="682b6-106">Terminal Services has been renamed Remote Desktop Services.</span></span> <span data-ttu-id="682b6-107">已安裝遠端桌面工作階段主機 (RD 工作階段主機) 角色服務的伺服器現在稱為 RD 工作階段主機伺服器，而不是終端機伺服器。</span><span class="sxs-lookup"><span data-stu-id="682b6-107">A server that has the Remote Desktop Session Host (RD Session Host) role service installed is now called an RD Session Host server, instead of a terminal server.</span></span><br/>
<ul>
<li><span data-ttu-id="682b6-108"><a href="terminal-services-is-now-remote-desktop-services.md">終端機服務現在遠端桌面服務</a></span><span class="sxs-lookup"><span data-stu-id="682b6-108"><a href="terminal-services-is-now-remote-desktop-services.md">Terminal Services Is Now Remote Desktop Services</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="682b6-109">遠端桌面虛擬化 API</span><span class="sxs-lookup"><span data-stu-id="682b6-109">Remote Desktop Virtualization API</span></span><br/></td>
<td><span data-ttu-id="682b6-110">遠端桌面虛擬化 API 提供了列舉、介面和結構，可讓您用來建立自訂外掛程式，以覆寫遠端桌面連線代理人 (RD 連線代理人) 的標準重新導向邏輯。</span><span class="sxs-lookup"><span data-stu-id="682b6-110">The Remote Desktop Virtualization API provides enumerations, interfaces, and structures that you can use to create custom plug-ins that override the standard redirection logic of Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="682b6-111">RD 連線代理人 (之前稱為「TS 會話代理人」) 已擴充為支援虛擬機器的連線。</span><span class="sxs-lookup"><span data-stu-id="682b6-111">RD Connection Broker (formerly known as TS Session Broker) was expanded to support connections to virtual machines.</span></span><br/>
<ul>
<li><span data-ttu-id="682b6-112"><a href="using-the-remote-desktop-virtualization-api.md">使用遠端桌面虛擬化 API</a></span><span class="sxs-lookup"><span data-stu-id="682b6-112"><a href="using-the-remote-desktop-virtualization-api.md">Using the Remote Desktop Virtualization API</a></span></span></li>
<li><span data-ttu-id="682b6-113"><a href="terminal-services-virtualization-api-reference.md">遠端桌面虛擬化 API 參考</a></span><span class="sxs-lookup"><span data-stu-id="682b6-113"><a href="terminal-services-virtualization-api-reference.md">Remote Desktop Virtualization API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="682b6-114">遠端桌面通訊協定提供者</span><span class="sxs-lookup"><span data-stu-id="682b6-114">Remote Desktop Protocol Provider</span></span><br/></td>
<td><span data-ttu-id="682b6-115">遠端桌面通訊協定提供者 API 可以用來建立自訂遠端桌面服務服務與桌面用戶端之間互動的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="682b6-115">The Remote Desktop Protocol Provider API can be used to create a protocol that customizes the interaction between the Remote Desktop Services service and desktop clients.</span></span><br/>
<ul>
<li><span data-ttu-id="682b6-116"><a href="creating-a-custom-remote-protocol.md">建立遠端桌面通訊協定提供者</a></span><span class="sxs-lookup"><span data-stu-id="682b6-116"><a href="creating-a-custom-remote-protocol.md">Creating a Remote Desktop Protocol Provider</a></span></span></li>
<li><span data-ttu-id="682b6-117"><a href="custom-remote-protocol-reference.md">遠端桌面通訊協定提供者參考</a></span><span class="sxs-lookup"><span data-stu-id="682b6-117"><a href="custom-remote-protocol-reference.md">Remote Desktop Protocol Provider Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="682b6-118">遠端桌面服務 AudioEndpoint API</span><span class="sxs-lookup"><span data-stu-id="682b6-118">Remote Desktop Services AudioEndpoint API</span></span><br/></td>
<td><span data-ttu-id="682b6-119">遠端桌面服務 AudioEndpoint API 支援用於音訊端點註冊和資料傳輸的列舉、介面和結構。</span><span class="sxs-lookup"><span data-stu-id="682b6-119">The Remote Desktop Services AudioEndpoint API supports enumeration, interfaces, and structures for audio endpoint registration and data transport.</span></span><br/>
<ul>
<li><span data-ttu-id="682b6-120"><a href="terminal-services-audioendpoint-api-reference.md">遠端桌面服務 AudioEndpoint API 參考</a></span><span class="sxs-lookup"><span data-stu-id="682b6-120"><a href="terminal-services-audioendpoint-api-reference.md">Remote Desktop Services AudioEndpoint API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="682b6-121">RemoteApp 和桌面連線管理服務 API</span><span class="sxs-lookup"><span data-stu-id="682b6-121">RemoteApp and Desktop Connection Management Service API</span></span><br/></td>
<td><span data-ttu-id="682b6-122">RemoteApp 和桌面連線管理服務 API 支援介面和結構，可讓您用來執行自訂的資源篩選，並支援 Windows Server 2008 R2 原生不支援的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="682b6-122">The RemoteApp and Desktop Connection Management Service API supports interfaces and structures that you can use to perform custom filtering of resources and provide support for file types that are not natively supported in Windows Server 2008 R2.</span></span><br/>
<ul>
<li><span data-ttu-id="682b6-123"><a href="centralized-publishing-api-reference.md">RemoteApp 和桌面連線管理服務 API 參考</a></span><span class="sxs-lookup"><span data-stu-id="682b6-123"><a href="centralized-publishing-api-reference.md">RemoteApp and Desktop Connection Management Service API Reference</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 





