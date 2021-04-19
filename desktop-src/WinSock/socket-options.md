---
description: Windows 通訊端 (Winsock) 通訊端選項的流覽頁面。
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: 通訊端選項
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967126"
---
# <a name="socket-options"></a><span data-ttu-id="3f9a2-103">通訊端選項</span><span class="sxs-lookup"><span data-stu-id="3f9a2-103">Socket Options</span></span>

<span data-ttu-id="3f9a2-104">本節說明各種 Windows 作業系統版本的 Winsock 通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-104">This section describes Winsock Socket Options for various editions of Windows operating systems.</span></span> <span data-ttu-id="3f9a2-105">使用 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數來取得和設定通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-105">Use the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) functions for more getting and setting socket options.</span></span> <span data-ttu-id="3f9a2-106">若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 函式。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-106">To enumerate protocols and discover supported properties for each installed protocol, use the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

<span data-ttu-id="3f9a2-107">有些通訊端選項需要比這些資料表可以傳達的更多說明;這類選項包含其他頁面的連結。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-107">Some socket options require more explanation than these tables can convey; such options contain links to additional pages.</span></span>

<dl> <dt>

<span data-ttu-id="3f9a2-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO \_ IP**</span><span class="sxs-lookup"><span data-stu-id="3f9a2-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f9a2-109">適用于 IPv4 層級的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-109">Socket options applicable at the IPv4 level.</span></span> <span data-ttu-id="3f9a2-110">如需詳細資訊，請參閱 [**IPPROTO \_ IP 通訊端選項**](ipproto-ip-socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-110">For more information, see the [**IPPROTO\_IP Socket Options**](ipproto-ip-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f9a2-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO \_ IPV6**</span><span class="sxs-lookup"><span data-stu-id="3f9a2-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO\_IPV6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f9a2-112">適用于 IPv6 層級的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-112">Socket options applicable at the IPv6 level.</span></span> <span data-ttu-id="3f9a2-113">如需詳細資訊，請參閱 [**IPPROTO \_ IPV6 通訊端選項**](ipproto-ipv6-socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-113">For more information, see the [**IPPROTO\_IPV6 Socket Options**](ipproto-ipv6-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f9a2-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**</span><span class="sxs-lookup"><span data-stu-id="3f9a2-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO\_RM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f9a2-115">適用于可靠多播層級的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-115">Socket options applicable at the reliable multicast level.</span></span> <span data-ttu-id="3f9a2-116">如需詳細資訊，請參閱 [**IPPROTO \_ RM 通訊端選項**](ipproto-rm-socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-116">For more information, see the [**IPPROTO\_RM Socket Options**](ipproto-rm-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f9a2-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="3f9a2-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO\_TCP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f9a2-118">適用于 TCP 層級的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-118">Socket options applicable at the TCP level.</span></span> <span data-ttu-id="3f9a2-119">如需詳細資訊，請參閱 [**IPPROTO \_ TCP 通訊端選項**](ipproto-tcp-socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-119">For more information, see the [**IPPROTO\_TCP Socket Options**](ipproto-tcp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f9a2-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="3f9a2-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO\_UDP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f9a2-121">適用于 UDP 層級的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-121">Socket options applicable at the UDP level.</span></span> <span data-ttu-id="3f9a2-122">如需詳細資訊，請參閱 [**IPPROTO \_ UDP 通訊端選項**](ipproto-udp-socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-122">For more information, see the [**IPPROTO\_UDP Socket Options**](ipproto-udp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f9a2-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="3f9a2-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO\_IPX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f9a2-124">適用于 IPX 層級的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-124">Socket options applicable at the IPX level.</span></span> <span data-ttu-id="3f9a2-125">如需詳細資訊，請參閱 [**NSPROTO \_ IPX 通訊端選項**](nsproto-ipx-socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-125">For more information, see the [**NSPROTO\_IPX Socket Options**](nsproto-ipx-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f9a2-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL \_ APPLETALK**</span><span class="sxs-lookup"><span data-stu-id="3f9a2-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL\_APPLETALK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f9a2-127">適用于 AppleTalk 層級的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-127">Socket options applicable at the AppleTalk level.</span></span> <span data-ttu-id="3f9a2-128">如需詳細資訊，請參閱 [**SOL \_ APPLETALK 通訊端選項**](sol-appletalk-socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-128">For more information, see the [**SOL\_APPLETALK Socket Options**](sol-appletalk-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f9a2-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL \_ IRLMP**</span><span class="sxs-lookup"><span data-stu-id="3f9a2-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL\_IRLMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f9a2-130">適用于紅外線連結管理通訊協定層級的通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-130">Socket options applicable at the InfraRed Link Management Protocol level.</span></span> <span data-ttu-id="3f9a2-131">For more information, see the [**SOL\_IRLMP Socket Options**](sol-irlmp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="3f9a2-131">For more information, see the [**SOL\_IRLMP Socket Options**](sol-irlmp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f9a2-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOL \_ 通訊端**</span><span class="sxs-lookup"><span data-stu-id="3f9a2-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOL\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f9a2-133">通訊端選項適用于通訊端層級。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-133">Socket options applicable at the socket level.</span></span> <span data-ttu-id="3f9a2-134">如需詳細資訊，請參閱 [**SOL \_ 通訊端通訊端選項**](sol-socket-socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-134">For more information, see the [**SOL\_SOCKET Socket Options**](sol-socket-socket-options.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f9a2-135">備註</span><span class="sxs-lookup"><span data-stu-id="3f9a2-135">Remarks</span></span>

<span data-ttu-id="3f9a2-136">所有 \_ \* 通訊端選項都同樣適用于 IPv4 和 IPv6 (但 \_ 因為廣播不是在 IPv6) 中執行，所以廣播除外。</span><span class="sxs-lookup"><span data-stu-id="3f9a2-136">All SO\_\* socket options apply equally to IPv4 and IPv6 (except SO\_BROADCAST, since broadcast is not implemented in IPv6).</span></span>

 

 



