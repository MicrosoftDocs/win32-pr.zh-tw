---
title: 對網路的最佳路由變更
description: 針對指定目的地網路的最佳路由，下列其中一個值的變更，會導致路由表管理員產生傳送至每個已註冊用戶端和轉寄站的通知訊息。
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966406"
---
# <a name="changes-to-the-best-route-to-a-network"></a><span data-ttu-id="a7eaf-103">對網路的最佳路由變更</span><span class="sxs-lookup"><span data-stu-id="a7eaf-103">Changes to the Best Route to a Network</span></span>

<span data-ttu-id="a7eaf-104">**Windows Server 2003：** 此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。</span><span class="sxs-lookup"><span data-stu-id="a7eaf-104">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="a7eaf-105">新的應用程式應該使用路由表管理員第2版 API。</span><span class="sxs-lookup"><span data-stu-id="a7eaf-105">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="a7eaf-106">針對指定目的地網路的最佳路由，下列其中一個值的變更，會導致路由表管理員產生傳送至每個已註冊用戶端和轉寄站的通知訊息：</span><span class="sxs-lookup"><span data-stu-id="a7eaf-106">A change in any of the following values for the best route to a given destination network causes the routing table manager to generate a notification message sent to each registered client and to the forwarders:</span></span>

-   <span data-ttu-id="a7eaf-107">通訊協定識別碼</span><span class="sxs-lookup"><span data-stu-id="a7eaf-107">Protocol identifier</span></span>
-   <span data-ttu-id="a7eaf-108">介面索引</span><span class="sxs-lookup"><span data-stu-id="a7eaf-108">Interface index</span></span>
-   <span data-ttu-id="a7eaf-109">下個躍點路由器的位址</span><span class="sxs-lookup"><span data-stu-id="a7eaf-109">Address of next-hop router</span></span>
-   <span data-ttu-id="a7eaf-110">包含路由計量的通訊協定系列特定資料</span><span class="sxs-lookup"><span data-stu-id="a7eaf-110">Protocol family-specific data that includes route metrics</span></span>

<span data-ttu-id="a7eaf-111">新增、更好的路由專案，或當目前的最佳路由專案已刪除或過時，並將另一個路由保留為新的最佳路由時，就會發生通訊協定識別碼、介面索引或下一個躍點路由器位址的變更。</span><span class="sxs-lookup"><span data-stu-id="a7eaf-111">A change in protocol identifier, interface index, or next-hop router address occurs when a new, better-route entry is added, or when the current best-route entry is deleted or aged out, and leaves another route as the new best route.</span></span>

 

 




