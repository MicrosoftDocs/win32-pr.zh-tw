---
title: 隨選連接路由協助程式 API 參考
description: 下列主題提供隨選連接路由協助程式的詳細資料。
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049c62d7784af6430e8b93240ec79464b098043
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092315"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a><span data-ttu-id="e7a6e-103">隨選連接路由協助程式 API 參考</span><span class="sxs-lookup"><span data-stu-id="e7a6e-103">On Demand Connection Routing Helper API reference</span></span>

<span data-ttu-id="e7a6e-104">下列主題提供隨選連接路由協助程式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e7a6e-104">The following topics provide details for the On Demand Connection Routing Helper.</span></span>



| <span data-ttu-id="e7a6e-105">參考</span><span class="sxs-lookup"><span data-stu-id="e7a6e-105">Reference</span></span>                                                                          | <span data-ttu-id="e7a6e-106">Description</span><span class="sxs-lookup"><span data-stu-id="e7a6e-106">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7a6e-107">**OnDemandGetRoutingHint**</span><span class="sxs-lookup"><span data-stu-id="e7a6e-107">**OnDemandGetRoutingHint**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | <span data-ttu-id="e7a6e-108">查閱路由要求快取中的目的地，如果找到相符的，則會傳回對應的介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7a6e-108">Look up a destination in the Route Request cache and, if a match is found, returns the corresponding Interface ID.</span></span><br/>                                               |
| [<span data-ttu-id="e7a6e-109">**OnDemandRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="e7a6e-109">**OnDemandRegisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | <span data-ttu-id="e7a6e-110">註冊，以在修改路由要求快取時收到通知。</span><span class="sxs-lookup"><span data-stu-id="e7a6e-110">Register to be notified when the Route Requests cache is modified.</span></span><br/>                                                                                               |
| [<span data-ttu-id="e7a6e-111">**OnDemandUnregisterNotification**</span><span class="sxs-lookup"><span data-stu-id="e7a6e-111">**OnDemandUnregisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | <span data-ttu-id="e7a6e-112">取消註冊通知並清除資源。</span><span class="sxs-lookup"><span data-stu-id="e7a6e-112">Unregister for notifications and clean up resources.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="e7a6e-113">**網路 \_ 介面 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="e7a6e-113">**NET\_INTERFACE\_CONTEXT**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | <span data-ttu-id="e7a6e-114">屬於 [**NET \_ interface \_ coNtext \_ TABLE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) 結構一部分的介面內容。</span><span class="sxs-lookup"><span data-stu-id="e7a6e-114">The interface context that is part of the [**NET\_INTERFACE\_CONTEXT\_TABLE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) structure.</span></span><br/>                                       |
| [<span data-ttu-id="e7a6e-115">**NET \_ 介面 \_ 內容 \_ 表**</span><span class="sxs-lookup"><span data-stu-id="e7a6e-115">**NET\_INTERFACE\_CONTEXT\_TABLE**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | <span data-ttu-id="e7a6e-116">[**NET \_ 介面 \_ 內容**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)結構的資料表。</span><span class="sxs-lookup"><span data-stu-id="e7a6e-116">The table of [**NET\_INTERFACE\_CONTEXT**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) structures.</span></span><br/>                                                                                |
| [<span data-ttu-id="e7a6e-117">**GetInterfaceCoNtextTableForHostName**</span><span class="sxs-lookup"><span data-stu-id="e7a6e-117">**GetInterfaceContextTableForHostName**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | <span data-ttu-id="e7a6e-118">此函式會針對指定的主機名稱和連接設定檔篩選器，抓取介面內容表。</span><span class="sxs-lookup"><span data-stu-id="e7a6e-118">This function retrieves an interface context table for the given hostname and connection profile filter.</span></span><br/>                                                         |
| [<span data-ttu-id="e7a6e-119">**FreeInterfaceCoNtextTable**</span><span class="sxs-lookup"><span data-stu-id="e7a6e-119">**FreeInterfaceContextTable**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | <span data-ttu-id="e7a6e-120">此函式會釋出使用 [**GetInterfaceCoNtextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) 函數抓取的介面內容資料表。</span><span class="sxs-lookup"><span data-stu-id="e7a6e-120">This function frees the interface context table retrieved using the [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) function.</span></span><br/> |



 

 

 





