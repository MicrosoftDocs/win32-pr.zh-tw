---
title: DNS WMI 提供者總覽
description: 提供者是 Windows Management Instrumentation (WMI) 的架構元素。
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- 網域名稱系統、WMI 提供者、架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aed54d0d9cbac4070483e8e72e9917607e824c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021319"
---
# <a name="dns-wmi-provider-overview"></a><span data-ttu-id="a6ab9-104">DNS WMI 提供者總覽</span><span class="sxs-lookup"><span data-stu-id="a6ab9-104">DNS WMI Provider Overview</span></span>

<span data-ttu-id="a6ab9-105">提供者是 *Windows Management Instrumentation (WMI)* 的架構元素。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-105">A provider is an architectural element of *Windows Management Instrumentation (WMI)*.</span></span> <span data-ttu-id="a6ab9-106">WMI 會定義用來描述、存取和檢測物件的統一架構。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-106">WMI defines a unified architecture for describing, accessing, and instrumenting objects.</span></span> <span data-ttu-id="a6ab9-107">此架構的一部分是用來在特定物件上執行遠端系統管理工作之 WMI 類別的大型資料庫。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-107">Part of this architecture is a large database of WMI classes used to carry out remote management tasks on specific objects.</span></span>

<span data-ttu-id="a6ab9-108">WMI 提供者可作為 WMI 和一或多個受管理物件之間的媒介。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-108">WMI providers act as intermediaries between WMI and one or more managed objects.</span></span> <span data-ttu-id="a6ab9-109">當 WMI 收到來自管理應用程式的要求，以找出 CIM 存放庫中無法使用的資料，或是 WMI 不支援的事件通知時，它會將要求轉送到提供者。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-109">When WMI receives a request from a management application for data that is not available from the CIM repository or for notifications of events that WMI does not support, it forwards the request to a provider.</span></span> <span data-ttu-id="a6ab9-110">提供者對特定網域的特定受管理物件提供資料與事件通知。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-110">Providers supply data and event notifications for managed objects that are specific to their particular domain.</span></span> <span data-ttu-id="a6ab9-111">提供者會擴充類別的 WMI 架構，以允許 WMI 使用新的物件類型。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-111">A provider extends the WMI schema of classes to allow WMI to work with new types of objects.</span></span> <span data-ttu-id="a6ab9-112">DNS WMI 提供者會定義用來查詢和設定 DNS 伺服器的類別，以及其相關聯的 DNS 區域和 DNS 記錄。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-112">The DNS WMI Provider defines classes for querying and configuring a DNS Server, along with its associated DNS zones and DNS records.</span></span>

<span data-ttu-id="a6ab9-113">DNS WMI 提供者會向用戶端公開一些 DNS 物件，包括 DNS 伺服器、DNS 網域和 DNS RR 物件。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-113">The DNS WMI provider exposes a number of DNS objects to clients, including DNS Server, DNS domain, and DNS RR objects.</span></span> <span data-ttu-id="a6ab9-114">透過這些物件，用戶端就能夠執行 DNS 管理活動。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-114">Through those objects, clients are able to perform DNS management activities.</span></span>

<span data-ttu-id="a6ab9-115">使用 DNS WMI 提供者時，您可以建立自己的工具來執行大部分的 DNS 伺服器管理工作。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-115">Using the DNS WMI Provider, you can create your own tools to perform most DNS Server administration tasks.</span></span> <span data-ttu-id="a6ab9-116">例如，您可以建立、刪除和查看區域和記錄;重設伺服器和區域屬性;並執行例行的管理作業，例如更新區域、重載區域、重新整理區域、將區域寫回檔案或 Active Directory、暫停和繼續區域、清除快取、停止和啟動 DNS 服務，以及查看統計資料。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-116">For example, you can create, delete, and view zones and records; reset server and zone properties; and perform routine administration operations such as updating the zone, reloading the zone, refreshing the zone, writing the zone back to a file or Active Directory, pausing and resuming the zone, clearing the cache, stopping and starting the DNS service, and viewing statistics.</span></span>

<span data-ttu-id="a6ab9-117">DNS WMI 提供者有一組在其他提供者中找不到的獨特行為。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-117">The DNS WMI Provider has a set of unique behaviors not found in other providers.</span></span> <span data-ttu-id="a6ab9-118">如需類別的詳細資料，請參閱 [DNS WMI 提供者參考](dns-wmi-provider-reference.md) 。</span><span class="sxs-lookup"><span data-stu-id="a6ab9-118">See the [DNS WMI Provider Reference](dns-wmi-provider-reference.md) for class details.</span></span>

 

 




