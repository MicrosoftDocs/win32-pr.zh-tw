---
description: WMI IP 路由提供者和網路類別可提供 IPv4 位址的資料。 從 Windows Vista 開始，WMI 也提供對 IPv6 網路功能的有限支援。
ms.assetid: 8ab6287d-be3f-4fa2-a9f5-fa5e1aba66c8
ms.tgt_platform: multiple
title: WMI 中的 IPv6 和 IPv4 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107872b2a65ffe02f34245a39e0a803d2ac53a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984991"
---
# <a name="ipv6-and-ipv4-support-in-wmi"></a><span data-ttu-id="2f78e-104">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="2f78e-104">IPv6 and IPv4 Support in WMI</span></span>

<span data-ttu-id="2f78e-105">WMI [IP 路由提供者](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) 和網路類別可提供 IPv4 位址的資料。</span><span class="sxs-lookup"><span data-stu-id="2f78e-105">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="2f78e-106">從 Windows Vista 開始，WMI 也提供對 IPv6 網路功能的有限支援。</span><span class="sxs-lookup"><span data-stu-id="2f78e-106">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span>

## <a name="wmi-ip-data"></a><span data-ttu-id="2f78e-107">WMI IP 資料</span><span class="sxs-lookup"><span data-stu-id="2f78e-107">WMI IP Data</span></span>

<span data-ttu-id="2f78e-108">下列類別僅提供 IPv4 資料：</span><span class="sxs-lookup"><span data-stu-id="2f78e-108">The following classes supply only IPv4 data:</span></span>

-   [<span data-ttu-id="2f78e-109">**Win32 \_ IP4RouteTable**</span><span class="sxs-lookup"><span data-stu-id="2f78e-109">**Win32\_IP4RouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)
-   [<span data-ttu-id="2f78e-110">**Win32 \_ IP4PersistedRouteTable**</span><span class="sxs-lookup"><span data-stu-id="2f78e-110">**Win32\_IP4PersistedRouteTable**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable)
-   [<span data-ttu-id="2f78e-111">**Win32 \_ IP4RouteTableEvent**</span><span class="sxs-lookup"><span data-stu-id="2f78e-111">**Win32\_IP4RouteTableEvent**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)
-   [<span data-ttu-id="2f78e-112">**Win32 \_ ActiveRoute**</span><span class="sxs-lookup"><span data-stu-id="2f78e-112">**Win32\_ActiveRoute**</span></span>](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)
-   [<span data-ttu-id="2f78e-113">**Win32 \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="2f78e-113">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)

<span data-ttu-id="2f78e-114">下列類別會為 IPv4 和 IPv6 提供資料。</span><span class="sxs-lookup"><span data-stu-id="2f78e-114">The following classes supply data for both IPv4 and IPv6.</span></span>

-   [<span data-ttu-id="2f78e-115">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="2f78e-115">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

    <span data-ttu-id="2f78e-116">**IpAddess** 屬性包含 ipv6 網路中電腦的 ipv6 位址。</span><span class="sxs-lookup"><span data-stu-id="2f78e-116">The **IpAddess** property contains the IPv6 address of the computer in an IPv6 network.</span></span>

-   [<span data-ttu-id="2f78e-117">**Win32 \_ PingStatus**</span><span class="sxs-lookup"><span data-stu-id="2f78e-117">**Win32\_PingStatus**</span></span>](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)

    <span data-ttu-id="2f78e-118">[**Win32 \_PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) 可以傳回 IPv4 或 IPv6 位址的資料。</span><span class="sxs-lookup"><span data-stu-id="2f78e-118">[**Win32\_PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus) can return data for either IPv4 or IPv6 addresses.</span></span>

## <a name="ipv4-and-ipv6-connections-to-wmi"></a><span data-ttu-id="2f78e-119">對 WMI 的 IPv4 和 IPv6 連線</span><span class="sxs-lookup"><span data-stu-id="2f78e-119">IPv4 and IPv6 Connections to WMI</span></span>

<span data-ttu-id="2f78e-120">連接至遠端電腦上的 WMI 命名空間時，目的電腦必須執行與連接電腦相同的 IP 軟體。</span><span class="sxs-lookup"><span data-stu-id="2f78e-120">When connecting to a WMI namespace on a remote computer, the target computer must be running the same IP software as the connecting computer.</span></span> <span data-ttu-id="2f78e-121">例如，執行 IPv4 的電腦無法連線到執行 IPv6 的電腦，即使在呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)、 [**wbemscripting.swbemlocator ConnectServer**](swbemlocator-connectserver.md)或使用「標記」連接的情況下，使用電腦名稱稱嘗試連接也是一樣 `winmgmts` 。</span><span class="sxs-lookup"><span data-stu-id="2f78e-121">For example, a computer running IPv4 cannot connect to a computer running IPv6, even if the connection is attempted by using a computer name in the call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), or by using the `winmgmts` moniker connection.</span></span> <span data-ttu-id="2f78e-122">相反的情況也是如此：只執行 IPv6 的電腦無法連線到只執行 IPv4 的電腦。</span><span class="sxs-lookup"><span data-stu-id="2f78e-122">The reverse is also true: a computer running only IPv6 cannot connect to a computer running only IPv4.</span></span>

<span data-ttu-id="2f78e-123">如果目的電腦同時執行 IPv4 和 IPv6，則可以從執行任一 IP 軟體的電腦進行連線。</span><span class="sxs-lookup"><span data-stu-id="2f78e-123">If the target computer is running both IPv4 and IPv6, then a connection can be made from a computer running either IP software.</span></span> <span data-ttu-id="2f78e-124">您可以在與 WMI 命名空間的連線中，提供 IPv4 或 IPv6 格式的電腦名稱稱或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2f78e-124">A computer name or an IP address in either IPv4 or IPv6 format can be supplied in the connection to a WMI namespace.</span></span>

<span data-ttu-id="2f78e-125">同時執行 IPv4 和 IPv6 並連接到只執行 IPv4 或僅 IPv6 的目的電腦的電腦，必須為目的電腦 IP 軟體提供適當的格式的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2f78e-125">A computer that runs both IPv4 and IPv6 and connects to a target computer running only IPv4 or only IPv6 must supply an IP address in the appropriate format for the target computer IP software.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f78e-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f78e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f78e-127">關於 WMI</span><span class="sxs-lookup"><span data-stu-id="2f78e-127">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
