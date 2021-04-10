---
title: 路由通訊協定介面函式
description: 針對路由通訊協定 DLL 執行下列功能
ms.assetid: fd780458-ef23-4ef2-8fe8-29b32100917f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b696d516cf0fc0b13d66fdc53b384a28fac8696a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933570"
---
# <a name="routing-protocol-interface-functions"></a><span data-ttu-id="0c2c9-103">路由通訊協定介面函式</span><span class="sxs-lookup"><span data-stu-id="0c2c9-103">Routing Protocol Interface Functions</span></span>

<span data-ttu-id="0c2c9-104">針對路由通訊協定 DLL 來執行下列功能：</span><span class="sxs-lookup"><span data-stu-id="0c2c9-104">Implement the following functions for a routing protocol DLL:</span></span>

[<span data-ttu-id="0c2c9-105">**AddInterface**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-105">**AddInterface**</span></span>](/windows/desktop/api/Routprot/nc-routprot-padd_interface)

[<span data-ttu-id="0c2c9-106">**ConnectClient**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-106">**ConnectClient**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pconnect_client)

[<span data-ttu-id="0c2c9-107">**DeleteInterface**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-107">**DeleteInterface**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface)

[<span data-ttu-id="0c2c9-108">**DisconnectClient**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-108">**DisconnectClient**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pdisconnect_client)

[<span data-ttu-id="0c2c9-109">**DoUpdateRoutes**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-109">**DoUpdateRoutes**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pdo_update_routes)

<span data-ttu-id="0c2c9-110">[*DoUpdateServices*](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c2c9-110">[*DoUpdateServices*](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span></span>

[<span data-ttu-id="0c2c9-111">**GetEventMessage**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-111">**GetEventMessage**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_event_message)

[<span data-ttu-id="0c2c9-112">**GetGlobalInfo**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-112">**GetGlobalInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)

[<span data-ttu-id="0c2c9-113">**GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-113">**GetInterfaceInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)

[<span data-ttu-id="0c2c9-114">**GetMfeStatus**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-114">**GetMfeStatus**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_mfe_status)

[<span data-ttu-id="0c2c9-115">**GetNeighbors**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-115">**GetNeighbors**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pget_neighbors)

[<span data-ttu-id="0c2c9-116">**InterfaceStatus**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-116">**InterfaceStatus**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pinterface_status)

[<span data-ttu-id="0c2c9-117">**MibCreate**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-117">**MibCreate**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_create)

[<span data-ttu-id="0c2c9-118">**MibDelete**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-118">**MibDelete**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)

[<span data-ttu-id="0c2c9-119">**MibGet**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-119">**MibGet**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get)

[<span data-ttu-id="0c2c9-120">**MibGetFirst**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-120">**MibGetFirst**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)

[<span data-ttu-id="0c2c9-121">**MibGetNext**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-121">**MibGetNext**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)

[<span data-ttu-id="0c2c9-122">*MibGetTrapInfo*</span><span class="sxs-lookup"><span data-stu-id="0c2c9-122">*MibGetTrapInfo*</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)

[<span data-ttu-id="0c2c9-123">**MibSet**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-123">**MibSet**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_set)

[<span data-ttu-id="0c2c9-124">**MibSetTrapInfo**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-124">**MibSetTrapInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

[<span data-ttu-id="0c2c9-125">**QueryPower**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-125">**QueryPower**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pquery_power)

[<span data-ttu-id="0c2c9-126">**RegisterProtocol**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-126">**RegisterProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)

[<span data-ttu-id="0c2c9-127">**SetGlobalInfo**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-127">**SetGlobalInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)

[<span data-ttu-id="0c2c9-128">**SetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-128">**SetInterfaceInfo**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

[<span data-ttu-id="0c2c9-129">**SetPower**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-129">**SetPower**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pset_power)

[<span data-ttu-id="0c2c9-130">**StartComplete**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-130">**StartComplete**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pstart_complete)

[<span data-ttu-id="0c2c9-131">**StartProtocol**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-131">**StartProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol)

[<span data-ttu-id="0c2c9-132">**StopProtocol**</span><span class="sxs-lookup"><span data-stu-id="0c2c9-132">**StopProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pstop_protocol)

<span data-ttu-id="0c2c9-133">[**UnbindInterface**](/previous-versions/windows/desktop/legacy/aa382296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c2c9-133">[**UnbindInterface**](/previous-versions/windows/desktop/legacy/aa382296(v=vs.85))</span></span>

<span data-ttu-id="0c2c9-134">如果路由通訊協定支援服務處理，除了上述所列的函式之外，還會執行下列功能：</span><span class="sxs-lookup"><span data-stu-id="0c2c9-134">If the routing protocol supports service handling, implement the following function in addition to those listed preceding:</span></span>

<span data-ttu-id="0c2c9-135">[**DoUpdateServices**](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c2c9-135">[**DoUpdateServices**](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))</span></span>

 

 