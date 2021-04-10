---
description: 適用于通訊端建立作業的 Winsock 網路追蹤事件。
ms.assetid: 59B9A570-5AEC-429D-AF71-AB6D8325C341
title: AFD_EVENT_CREATE 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CREATE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3216e1adccca6c7c7d64a22f77babe3cbb699c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848030"
---
# <a name="afd_event_create-event"></a><span data-ttu-id="b70cd-103">AFD \_ 事件 \_ 建立事件</span><span class="sxs-lookup"><span data-stu-id="b70cd-103">AFD\_EVENT\_CREATE event</span></span>

<span data-ttu-id="b70cd-104">**AFD \_ 事件 \_ 建立** 事件是通訊端建立作業的 Winsock 網路追蹤事件。</span><span class="sxs-lookup"><span data-stu-id="b70cd-104">The **AFD\_EVENT\_CREATE** event is a Winsock network tracing event for a socket creation operation.</span></span>


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a><span data-ttu-id="b70cd-105">參數</span><span class="sxs-lookup"><span data-stu-id="b70cd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b70cd-106">*EnterExit*</span><span class="sxs-lookup"><span data-stu-id="b70cd-106">*EnterExit*</span></span> 
</dt> <dd>

<span data-ttu-id="b70cd-107">此事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="b70cd-107">Information on this event.</span></span>

<span data-ttu-id="b70cd-108">下表列出 *EnterExit* 參數的可能值：</span><span class="sxs-lookup"><span data-stu-id="b70cd-108">The following table lists the possible values for the *EnterExit* parameter:</span></span>



| <span data-ttu-id="b70cd-109">值</span><span class="sxs-lookup"><span data-stu-id="b70cd-109">Value</span></span>                                                                        | <span data-ttu-id="b70cd-110">意義</span><span class="sxs-lookup"><span data-stu-id="b70cd-110">Meaning</span></span>                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b70cd-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="b70cd-112">Winsock 要求的開始。</span><span class="sxs-lookup"><span data-stu-id="b70cd-112">The start of a Winsock request.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="b70cd-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b70cd-114">Winsock 要求已完成。</span><span class="sxs-lookup"><span data-stu-id="b70cd-114">The Winsock request completed.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="b70cd-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b70cd-116">Winsock AFD 驅動程式採取內部動作 (中止連線，例如) 。</span><span class="sxs-lookup"><span data-stu-id="b70cd-116">The Winsock AFD driver took an internal action (aborting a connection, for example).</span></span><br/>      |
| <dl> <span data-ttu-id="b70cd-117"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-117"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b70cd-118">TCP/IP 驅動程式導致此事件發生。</span><span class="sxs-lookup"><span data-stu-id="b70cd-118">The TCP/IP driver caused this event to occur.</span></span> <span data-ttu-id="b70cd-119">這通常表示資料通知。</span><span class="sxs-lookup"><span data-stu-id="b70cd-119">This usually indicates a data notification.</span></span><br/> |
| <dl> <span data-ttu-id="b70cd-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-120"><dt>4</dt></span></span> </dl> | <span data-ttu-id="b70cd-121">Winsock AFD 驅動程式會導致此事件發生 (設定 socket 選項，例如) 。</span><span class="sxs-lookup"><span data-stu-id="b70cd-121">The Winsock AFD driver caused this event to occur (setting a socket option, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b70cd-122">*位置*</span><span class="sxs-lookup"><span data-stu-id="b70cd-122">*Location*</span></span> 
</dt> <dd>

<span data-ttu-id="b70cd-123">內部使用的私用欄位。</span><span class="sxs-lookup"><span data-stu-id="b70cd-123">A private field used internally.</span></span>

</dd> <dt>

<span data-ttu-id="b70cd-124">*處理*</span><span class="sxs-lookup"><span data-stu-id="b70cd-124">*Process*</span></span> 
</dt> <dd>

<span data-ttu-id="b70cd-125">擁有相關通訊端之進程的 [EPROCESS](/windows-hardware/drivers/kernel/eprocess) 位址。</span><span class="sxs-lookup"><span data-stu-id="b70cd-125">The [EPROCESS](/windows-hardware/drivers/kernel/eprocess) address of the process that owns the related socket.</span></span> <span data-ttu-id="b70cd-126">這是一個不透明的結構，可作為進程的處理常式物件。</span><span class="sxs-lookup"><span data-stu-id="b70cd-126">This is an opaque structure that serves as the process object for a process.</span></span> <span data-ttu-id="b70cd-127">如需詳細資訊，請參閱 [EPROCESS](/windows-hardware/drivers/kernel/eprocess) 結構的 Windows 驅動程式套件檔。</span><span class="sxs-lookup"><span data-stu-id="b70cd-127">For more information, see the Windows Driver Kit documentation for the [EPROCESS](/windows-hardware/drivers/kernel/eprocess) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b70cd-128">*端點*</span><span class="sxs-lookup"><span data-stu-id="b70cd-128">*Endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="b70cd-129">\_通訊端的 AFD 端點位址。</span><span class="sxs-lookup"><span data-stu-id="b70cd-129">The AFD\_ENDPOINT address of the socket.</span></span>

</dd> <dt>

<span data-ttu-id="b70cd-130">*AddressFamily*</span><span class="sxs-lookup"><span data-stu-id="b70cd-130">*AddressFamily*</span></span> 
</dt> <dd>

<span data-ttu-id="b70cd-131">通訊端的位址系列規格。</span><span class="sxs-lookup"><span data-stu-id="b70cd-131">The address family specification for the socket.</span></span> <span data-ttu-id="b70cd-132">位址家族的可能值定義于 *Ws2def .h* 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="b70cd-132">Possible values for the address family are defined in the *Ws2def.h* header file.</span></span> <span data-ttu-id="b70cd-133">請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。</span><span class="sxs-lookup"><span data-stu-id="b70cd-133">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

<span data-ttu-id="b70cd-134">目前支援的值為 AF \_ INET 或 af \_ INET6，也就是 IPv4 和 IPv6 的網際網路位址家族格式。</span><span class="sxs-lookup"><span data-stu-id="b70cd-134">The values currently supported are AF\_INET or AF\_INET6, which are the Internet address family formats for IPv4 and IPv6.</span></span> <span data-ttu-id="b70cd-135">位址家族的其他選項 (AF \_ netbios 搭配 netbios 使用，例如，如果已安裝位址家族的 Windows 通訊端服務提供者，則支援) 。</span><span class="sxs-lookup"><span data-stu-id="b70cd-135">Other options for address family (AF\_NETBIOS for use with NetBIOS, for example) are supported if a Windows Sockets service provider for the address family is installed.</span></span>

<span data-ttu-id="b70cd-136">下表列出位址家族的一般值，雖然可能有許多其他值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-136">The table below lists common values for address family although many other values are possible.</span></span>



| <span data-ttu-id="b70cd-137">Af</span><span class="sxs-lookup"><span data-stu-id="b70cd-137">Af</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="b70cd-138">意義</span><span class="sxs-lookup"><span data-stu-id="b70cd-138">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <span data-ttu-id="b70cd-139"><dt>**AF \_UNSPEC**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-139"><dt>**AF\_UNSPEC**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="b70cd-140">未指定位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-140">The address family is unspecified.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="b70cd-141"><dt>**AF \_INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-141"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>                 | <span data-ttu-id="b70cd-142">第四版網際網路協定 (IPv4) 位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-142">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <span data-ttu-id="b70cd-143"><dt>**AF \_IPX**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-143"><dt>**AF\_IPX**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="b70cd-144">IPX/SPX 位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-144">The IPX/SPX address family.</span></span> <span data-ttu-id="b70cd-145">只有在安裝了 NWLink IPX/SPX NetBIOS 相容的傳輸通訊協定時，才支援此位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-145">This address family is only supported if the NWLink IPX/SPX NetBIOS Compatible Transport protocol is installed.</span></span> <br/> <span data-ttu-id="b70cd-146">Windows Vista 和更新版本不支援此位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-146">This address family is not supported on Windows Vista and later.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <span data-ttu-id="b70cd-147"><dt>**AF \_APPLETALK**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-147"><dt>**AF\_APPLETALK**</dt> <dt>16</dt></span></span> </dl> | <span data-ttu-id="b70cd-148">AppleTalk 位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-148">The AppleTalk address family.</span></span> <span data-ttu-id="b70cd-149">只有在已安裝 AppleTalk 通訊協定的情況下，才支援此位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-149">This address family is only supported if the AppleTalk protocol is installed.</span></span> <br/> <span data-ttu-id="b70cd-150">Windows Vista 和更新版本不支援此位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-150">This address family is not supported on Windows Vista and later.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <span data-ttu-id="b70cd-151"><dt>**AF \_NETBIOS**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-151"><dt>**AF\_NETBIOS**</dt> <dt>17</dt></span></span> </dl>       | <span data-ttu-id="b70cd-152">NetBIOS 位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-152">The NetBIOS address family.</span></span> <span data-ttu-id="b70cd-153">只有在已安裝適用于 NetBIOS 的 Windows 通訊端提供者時，才支援此位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-153">This address family is only supported if the Windows Sockets provider for NetBIOS is installed.</span></span> <br/> <span data-ttu-id="b70cd-154">32位版本的 Windows 上支援適用于 NetBIOS 的 Windows 通訊端提供者。</span><span class="sxs-lookup"><span data-stu-id="b70cd-154">The Windows Sockets provider for NetBIOS is supported on 32-bit versions of Windows.</span></span> <span data-ttu-id="b70cd-155">預設會在32位版本的 Windows 上安裝此提供者。</span><span class="sxs-lookup"><span data-stu-id="b70cd-155">This provider is installed by default on 32-bit versions of Windows.</span></span> <br/> <span data-ttu-id="b70cd-156">64位版本的 windows 不支援 NetBIOS 的 Windows 通訊端提供者。</span><span class="sxs-lookup"><span data-stu-id="b70cd-156">The Windows Sockets provider for NetBIOS is not supported on 64-bit versions of windows.</span></span> <br/> <span data-ttu-id="b70cd-157">適用于 NetBIOS 的 Windows 通訊端提供者僅支援將 *type* 參數設定為 **SOCK \_ DGRAM** 的通訊端。</span><span class="sxs-lookup"><span data-stu-id="b70cd-157">The Windows Sockets provider for NetBIOS only supports sockets where the *type* parameter is set to **SOCK\_DGRAM**.</span></span><br/> <span data-ttu-id="b70cd-158">NetBIOS 的 Windows 通訊端提供者與 [netbios](/previous-versions/windows/desktop/netbios/portal) 程式設計介面不直接相關。</span><span class="sxs-lookup"><span data-stu-id="b70cd-158">The Windows Sockets provider for NetBIOS is not directly related to the [NetBIOS](/previous-versions/windows/desktop/netbios/portal) programming interface.</span></span> <span data-ttu-id="b70cd-159">Windows Vista、Windows Server 2008 及更新版本不支援 NetBIOS 程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="b70cd-159">The NetBIOS programming interface is not supported on Windows Vista, Windows Server 2008, and later.</span></span><br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="b70cd-160"><dt>**AF \_INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-160"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl>             | <span data-ttu-id="b70cd-161">網際網路通訊協定第6版 (IPv6) 位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-161">The Internet Protocol version 6 (IPv6) address family.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <span data-ttu-id="b70cd-162"><dt>**AF \_IRDA**</dt> <dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-162"><dt>**AF\_IRDA**</dt> <dt>26</dt></span></span> </dl>                | <span data-ttu-id="b70cd-163">紅外線資料關聯 (IrDA) 位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-163">The Infrared Data Association (IrDA) address family.</span></span> <br/> <span data-ttu-id="b70cd-164">只有在電腦已安裝紅外線埠和驅動程式時，才支援此位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-164">This address family is only supported if the computer has an infrared port and driver installed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <span data-ttu-id="b70cd-165"><dt>**AF \_BTH**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-165"><dt>**AF\_BTH**</dt> <dt>32</dt></span></span> </dl>                   | <span data-ttu-id="b70cd-166">藍牙位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-166">The Bluetooth address family.</span></span> <br/> <span data-ttu-id="b70cd-167">只有在電腦已安裝 Bluetooth 介面卡和驅動程式時，才支援此位址系列。</span><span class="sxs-lookup"><span data-stu-id="b70cd-167">This address family is only supported if the computer has a Bluetooth adapter and driver installed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="b70cd-168">*SocketType*</span><span class="sxs-lookup"><span data-stu-id="b70cd-168">*SocketType*</span></span> 
</dt> <dd>

<span data-ttu-id="b70cd-169">新通訊端的類型規格。</span><span class="sxs-lookup"><span data-stu-id="b70cd-169">The type specification for the new socket.</span></span> <span data-ttu-id="b70cd-170">可能會在 *Winsock2* 標頭檔中定義通訊端類型的值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-170">Possible values for the socket type are defined in the *Winsock2.h* header file.</span></span>

<span data-ttu-id="b70cd-171">下表列出 Windows 通訊端2支援之 *類型* 參數的可能值：</span><span class="sxs-lookup"><span data-stu-id="b70cd-171">The following table lists the possible values for the *type* parameter supported for Windows Sockets 2:</span></span>



| <span data-ttu-id="b70cd-172">類型</span><span class="sxs-lookup"><span data-stu-id="b70cd-172">Type</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="b70cd-173">意義</span><span class="sxs-lookup"><span data-stu-id="b70cd-173">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <span data-ttu-id="b70cd-174"><dt>**SOCK \_串流**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-174"><dt>**SOCK\_STREAM**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="b70cd-175">通訊端類型，提供具有 OOB 資料傳輸機制的已排序、可靠、雙向、以連接為基礎的位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="b70cd-175">A socket type that provides sequenced, reliable, two-way, connection-based byte streams with an OOB data transmission mechanism.</span></span> <span data-ttu-id="b70cd-176">此通訊端類型會使用網際網路位址系列 (AF \_ INET 或 af INET6)  (TCP) 的傳輸控制通訊協定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b70cd-176">This socket type uses the Transmission Control Protocol (TCP) for the Internet address family (AF\_INET or AF\_INET6).</span></span><br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <span data-ttu-id="b70cd-177"><dt>**SOCK \_DGRAM**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-177"><dt>**SOCK\_DGRAM**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="b70cd-178">支援資料包的通訊端型別，這些是固定 (的不可靠緩衝區通常很小) 最大長度。</span><span class="sxs-lookup"><span data-stu-id="b70cd-178">A socket type that supports datagrams, which are connectionless, unreliable buffers of a fixed (typically small) maximum length.</span></span> <span data-ttu-id="b70cd-179">此通訊端類型會針對網際網路位址系列使用使用者資料包協定 (UDP)  (AF \_ INET 或 af \_ INET6) 。</span><span class="sxs-lookup"><span data-stu-id="b70cd-179">This socket type uses the User Datagram Protocol (UDP) for the Internet address family (AF\_INET or AF\_INET6).</span></span><br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <span data-ttu-id="b70cd-180"><dt>**SOCK \_原始**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-180"><dt>**SOCK\_RAW**</dt> <dt>3</dt></span></span> </dl>                   | <span data-ttu-id="b70cd-181">提供原始通訊端的通訊端類型，可讓應用程式操作下一個上層通訊協定標頭。</span><span class="sxs-lookup"><span data-stu-id="b70cd-181">A socket type that provides a raw socket that allows an application to manipulate the next upper-layer protocol header.</span></span> <span data-ttu-id="b70cd-182">若要操作 IPv4 標頭，必須在通訊端上設定 [**IP \_ HDRINCL**](ipproto-ip-socket-options.md) 通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="b70cd-182">To manipulate the IPv4 header, the [**IP\_HDRINCL**](ipproto-ip-socket-options.md) socket option must be set on the socket.</span></span> <span data-ttu-id="b70cd-183">若要操作 IPv6 標頭，必須在通訊端上設定 [**ipv6 \_ HDRINCL**](ipproto-ipv6-socket-options.md) 通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="b70cd-183">To manipulate the IPv6 header, the [**IPV6\_HDRINCL**](ipproto-ipv6-socket-options.md) socket option must be set on the socket.</span></span> <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <span data-ttu-id="b70cd-184"><dt>**SOCK \_RDM**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-184"><dt>**SOCK\_RDM**</dt> <dt>4</dt></span></span> </dl>                   | <span data-ttu-id="b70cd-185">提供可靠訊息資料包的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="b70cd-185">A socket type that provides a reliable message datagram.</span></span> <span data-ttu-id="b70cd-186">這種類型的範例是 Windows 中的實際一般多播 (PGM) 多播通訊協定，通常稱為可靠的 [多播程式設計](reliable-multicast-programming--pgm-.md)。</span><span class="sxs-lookup"><span data-stu-id="b70cd-186">An example of this type is the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as [reliable multicast programming](reliable-multicast-programming--pgm-.md).</span></span> <br/> <span data-ttu-id="b70cd-187">只有在已安裝可靠多播通訊協定的情況下，才支援此 *類型* 值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-187">This *type* value is only supported if the Reliable Multicast Protocol is installed.</span></span><br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <span data-ttu-id="b70cd-188"><dt>**SOCK \_SEQPACKET**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-188"><dt>**SOCK\_SEQPACKET**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="b70cd-189">提供以資料包為基礎之虛擬資料流程封包的通訊端類型。</span><span class="sxs-lookup"><span data-stu-id="b70cd-189">A socket type that provides a pseudo-stream packet based on datagrams.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="b70cd-190">*通訊協定*</span><span class="sxs-lookup"><span data-stu-id="b70cd-190">*Protocol*</span></span> 
</dt> <dd>

<span data-ttu-id="b70cd-191">要使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b70cd-191">The protocol to be used.</span></span> <span data-ttu-id="b70cd-192">通訊 *協定* 參數的可能選項是指定的位址系列和通訊端類型專用的。</span><span class="sxs-lookup"><span data-stu-id="b70cd-192">The possible options for the *protocol* parameter are specific to the address family and socket type specified.</span></span> <span data-ttu-id="b70cd-193">*通訊協定* 的可能值定義于 *Wsrm* 標頭檔中，以及 *Ws2def .h* 標頭檔中定義的 **IPPROTO** 列舉類型。</span><span class="sxs-lookup"><span data-stu-id="b70cd-193">Possible values for the *protocol* are defined in the *Wsrm.h* header file and the **IPPROTO** enumeration type defined in the *Ws2def.h* header file.</span></span> <span data-ttu-id="b70cd-194">請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。</span><span class="sxs-lookup"><span data-stu-id="b70cd-194">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

<span data-ttu-id="b70cd-195">如果指定0值，呼叫端不會想要指定通訊協定，而服務提供者將選擇要使用的 *通訊協定* 。</span><span class="sxs-lookup"><span data-stu-id="b70cd-195">If a value of 0 is specified, the caller does not wish to specify a protocol and the service provider will choose the *protocol* to use.</span></span>

<span data-ttu-id="b70cd-196">下表列出 *通訊協定* 的通用值（雖然可能有許多其他值）。</span><span class="sxs-lookup"><span data-stu-id="b70cd-196">The table below lists common values for the *protocol* although many other values are possible.</span></span>



| <span data-ttu-id="b70cd-197">protocol</span><span class="sxs-lookup"><span data-stu-id="b70cd-197">protocol</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="b70cd-198">意義</span><span class="sxs-lookup"><span data-stu-id="b70cd-198">Meaning</span></span>                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <span data-ttu-id="b70cd-199"><dt>**IPPROTO \_ICMP**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-199"><dt>**IPPROTO\_ICMP**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="b70cd-200">網際網路控制訊息通訊協定 (ICMP) 。</span><span class="sxs-lookup"><span data-stu-id="b70cd-200">The Internet Control Message Protocol (ICMP).</span></span> <span data-ttu-id="b70cd-201">如果 *af* 參數為 **af \_ UNSPEC**、 **af \_ INET** 或 **af \_ INET6** ，且 *類型* 參數為 **SOCK \_ RAW** 或未指定，則這是可能的值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-201">This is a possible value when the *af* parameter is **AF\_UNSPEC**, **AF\_INET**, or **AF\_INET6** and the *type* parameter is **SOCK\_RAW** or unspecified.</span></span><br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <span data-ttu-id="b70cd-202"><dt>**IPPROTO \_IGMP**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-202"><dt>**IPPROTO\_IGMP**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="b70cd-203">網際網路群組管理通訊協定 (IGMP) 。</span><span class="sxs-lookup"><span data-stu-id="b70cd-203">The Internet Group Management Protocol (IGMP).</span></span> <span data-ttu-id="b70cd-204">如果 *af* 參數為 **af \_ UNSPEC**、 **af \_ INET** 或 **af \_ INET6** ，且 *類型* 參數為 **SOCK \_ RAW** 或未指定，則這是可能的值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-204">This is a possible value when the *af* parameter is **AF\_UNSPEC**, **AF\_INET**, or **AF\_INET6** and the *type* parameter is **SOCK\_RAW** or unspecified.</span></span><br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <span data-ttu-id="b70cd-205"><dt>**BTHPROTO \_RFCOMM**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-205"><dt>**BTHPROTO\_RFCOMM**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="b70cd-206">藍牙無線電頻率通訊 (藍牙 RFCOMM) 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b70cd-206">The Bluetooth Radio Frequency Communications (Bluetooth RFCOMM) protocol.</span></span> <span data-ttu-id="b70cd-207">當 *af* 參數為 **af \_ BTH** 且 *類型* 參數為 **SOCK \_ 串流** 時，這是可能的值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-207">This is a possible value when the *af* parameter is **AF\_BTH** and the *type* parameter is **SOCK\_STREAM**.</span></span> <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <span data-ttu-id="b70cd-208"><dt>**IPPROTO \_TCP**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-208"><dt>**IPPROTO\_TCP**</dt> <dt>6</dt></span></span> </dl>             | <span data-ttu-id="b70cd-209"> (TCP) 的傳輸控制通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b70cd-209">The Transmission Control Protocol (TCP).</span></span> <span data-ttu-id="b70cd-210">當 *af* 參數為 **Af \_ INET** 或 **Af \_ INET6** 且 *類型* 參數為 **SOCK \_ 串流** 時，這是可能的值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-210">This is a possible value when the *af* parameter is **AF\_INET** or **AF\_INET6** and the *type* parameter is **SOCK\_STREAM**.</span></span><br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <span data-ttu-id="b70cd-211"><dt>**IPPROTO \_UDP**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-211"><dt>**IPPROTO\_UDP**</dt> <dt>17</dt></span></span> </dl>            | <span data-ttu-id="b70cd-212">使用者資料包協定 (UDP) 。</span><span class="sxs-lookup"><span data-stu-id="b70cd-212">The User Datagram Protocol (UDP).</span></span> <span data-ttu-id="b70cd-213">當 *af* 參數為 **Af \_ INET** 或 **Af \_ INET6** 且 *類型* 參數為 **SOCK \_ DGRAM** 時，這是可能的值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-213">This is a possible value when the *af* parameter is **AF\_INET** or **AF\_INET6** and the *type* parameter is **SOCK\_DGRAM**.</span></span><br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <span data-ttu-id="b70cd-214"><dt>**IPPROTO \_ICMPV6**</dt> <dt>58</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-214"><dt>**IPPROTO\_ICMPV6**</dt> <dt>58</dt></span></span> </dl>   | <span data-ttu-id="b70cd-215">網際網路控制訊息通訊協定第6版 (ICMPv6) 。</span><span class="sxs-lookup"><span data-stu-id="b70cd-215">The Internet Control Message Protocol Version 6 (ICMPv6).</span></span> <span data-ttu-id="b70cd-216">如果 *af* 參數為 **af \_ UNSPEC**、 **af \_ INET** 或 **af \_ INET6** ，且 *類型* 參數為 **SOCK \_ RAW** 或未指定，則這是可能的值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-216">This is a possible value when the *af* parameter is **AF\_UNSPEC**, **AF\_INET**, or **AF\_INET6** and the *type* parameter is **SOCK\_RAW** or unspecified.</span></span><br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <span data-ttu-id="b70cd-217"><dt>**IPPROTO \_RM**</dt> <dt>113</dt></span><span class="sxs-lookup"><span data-stu-id="b70cd-217"><dt>**IPPROTO\_RM**</dt> <dt>113</dt></span></span> </dl>              | <span data-ttu-id="b70cd-218">適用于可靠多播的 PGM 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b70cd-218">The PGM protocol for reliable multicast.</span></span> <span data-ttu-id="b70cd-219">如果 *af* 參數為 **af \_ INET** ，且 *類型* 參數為 **SOCK \_ RDM**，則這是可能的值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-219">This is a possible value when the *af* parameter is **AF\_INET** and the *type* parameter is **SOCK\_RDM**.</span></span> <span data-ttu-id="b70cd-220">此通訊協定也稱為 **IPPROTO \_ PGM**。</span><span class="sxs-lookup"><span data-stu-id="b70cd-220">This protocol is also called **IPPROTO\_PGM**.</span></span> <br/> <span data-ttu-id="b70cd-221">只有在已安裝可靠多播通訊協定的情況下，才支援此 *通訊協定* 值。</span><span class="sxs-lookup"><span data-stu-id="b70cd-221">This *protocol* value is only supported if the Reliable Multicast Protocol is installed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b70cd-222">*進程*</span><span class="sxs-lookup"><span data-stu-id="b70cd-222">*ProcessId*</span></span> 
</dt> <dd>

<span data-ttu-id="b70cd-223">實際的處理序識別碼或指標，如果事件是在系統進程或延遲程序呼叫中執行 Winsock 程式碼的結果， (DPC) 在使用者進程) 以外的內容 (內容。</span><span class="sxs-lookup"><span data-stu-id="b70cd-223">The actual process ID or an indicator if the event was a result of Winsock code run in a system process or in a deferred procedure call (DPC) context (contexts outside the user process).</span></span>

</dd> <dt>

<span data-ttu-id="b70cd-224">*狀態*</span><span class="sxs-lookup"><span data-stu-id="b70cd-224">*Status*</span></span> 
</dt> <dd>

<span data-ttu-id="b70cd-225">運算的 NTSTATUS 程式碼。</span><span class="sxs-lookup"><span data-stu-id="b70cd-225">The NTSTATUS code for the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b70cd-226">備註</span><span class="sxs-lookup"><span data-stu-id="b70cd-226">Remarks</span></span>

<span data-ttu-id="b70cd-227">**AFD \_ 事件 \_ 建立** 事件是針對 Winsock 網路作業進行追蹤，以建立通訊端。</span><span class="sxs-lookup"><span data-stu-id="b70cd-227">The **AFD\_EVENT\_CREATE** event is traced for a Winsock network operation to create a socket.</span></span> <span data-ttu-id="b70cd-228">此事件的通道是 Winsock-AFD。</span><span class="sxs-lookup"><span data-stu-id="b70cd-228">The channel for this event is Winsock-AFD.</span></span> <span data-ttu-id="b70cd-229">此事件的層級為資訊。</span><span class="sxs-lookup"><span data-stu-id="b70cd-229">The level for this event is informational.</span></span>

## <a name="requirements"></a><span data-ttu-id="b70cd-230">規格需求</span><span class="sxs-lookup"><span data-stu-id="b70cd-230">Requirements</span></span>



| <span data-ttu-id="b70cd-231">需求</span><span class="sxs-lookup"><span data-stu-id="b70cd-231">Requirement</span></span> | <span data-ttu-id="b70cd-232">值</span><span class="sxs-lookup"><span data-stu-id="b70cd-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b70cd-233">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b70cd-233">Minimum supported client</span></span><br/> | <span data-ttu-id="b70cd-234">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b70cd-234">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b70cd-235">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b70cd-235">Minimum supported server</span></span><br/> | <span data-ttu-id="b70cd-236">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b70cd-236">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b70cd-237">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b70cd-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b70cd-238">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="b70cd-238">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="b70cd-239">**事件 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="b70cd-239">**EVENT\_DESCRIPTOR**</span></span>](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[<span data-ttu-id="b70cd-240">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="b70cd-240">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="b70cd-241">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="b70cd-241">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="b70cd-242">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="b70cd-242">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

