---
title: 藍牙與系結
description: 藍牙使用系結函式來系結至通訊端。
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- 藍牙與系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842680"
---
# <a name="bluetooth-and-bind"></a><span data-ttu-id="03983-107">藍牙與系結</span><span class="sxs-lookup"><span data-stu-id="03983-107">Bluetooth and bind</span></span>

<span data-ttu-id="03983-108">藍牙使用系[](/windows/desktop/api/winsock/nf-winsock-bind)結函式來系結至通訊端。</span><span class="sxs-lookup"><span data-stu-id="03983-108">Bluetooth uses the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function to bind to a socket.</span></span> <span data-ttu-id="03983-109">若要系結藍牙通訊端， 請使用 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構來呼叫系結函式。</span><span class="sxs-lookup"><span data-stu-id="03983-109">To bind a Bluetooth socket, call the **bind** function using the [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure.</span></span> <span data-ttu-id="03983-110">使用 **SOCKADDR \_ BTH** 結構搭配下列設定：</span><span class="sxs-lookup"><span data-stu-id="03983-110">Use the **SOCKADDR\_BTH** structure with the following settings:</span></span>

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

<span data-ttu-id="03983-111">在用戶端應用程式上，埠成員必須為零，才能讓指派適當的本機端點。</span><span class="sxs-lookup"><span data-stu-id="03983-111">On client applications, the port member must be zero to enable an appropriate local endpoint to be assigned.</span></span> <span data-ttu-id="03983-112">在伺服器應用程式上，埠成員必須是有效的埠號碼或 BT \_ 埠 \_ any; 使用 BT 埠自動指派的埠， \_ \_ 之後可能會透過呼叫 [**getsockname**](bluetooth-and-getsockname.md) 函式來進行查詢。</span><span class="sxs-lookup"><span data-stu-id="03983-112">On server applications, the port member must be a valid port number or BT\_PORT\_ANY; ports automatically assigned using BT\_PORT\_ANY may be queried subsequently with a call to the [**getsockname**](bluetooth-and-getsockname.md) function.</span></span> <span data-ttu-id="03983-113">要求特定 RFCOMM 埠的有效範圍是1到30。</span><span class="sxs-lookup"><span data-stu-id="03983-113">The valid range for requesting a specific RFCOMM port is 1 through 30.</span></span> <span data-ttu-id="03983-114">伺服器通道是全域資源，而且在任何 Bluetooth 裝置上都只能使用30個伺服器通道 RFCOMM，而這些裝置必須由屬於藍牙位址家族的所有 Windows 通訊端共用。</span><span class="sxs-lookup"><span data-stu-id="03983-114">Server channels are global resource, and only 30 server channels are available for RFCOMM on any Bluetooth device, which must be shared by all Windows Sockets that belong to the Bluetooth address family.</span></span> <span data-ttu-id="03983-115">如果沒有可用的伺服器通道，或指定的伺服器通道已經保留，系 [**結呼叫就**](/windows/desktop/api/winsock/nf-winsock-bind) 會失敗。</span><span class="sxs-lookup"><span data-stu-id="03983-115">If no server channel is available, or if the specified server channel is already reserved, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) call fails.</span></span>

<span data-ttu-id="03983-116">從 bind 成功傳回時，會保留伺服器通道，直到通訊端關閉為止。</span><span class="sxs-lookup"><span data-stu-id="03983-116">Upon successful return from bind, the server channel is reserved until the socket is closed.</span></span> <span data-ttu-id="03983-117">使用 [**getsockname**](bluetooth-and-getsockname.md) 函式來取得 SDP 註冊的通道號碼。</span><span class="sxs-lookup"><span data-stu-id="03983-117">Use the [**getsockname**](bluetooth-and-getsockname.md) function to retrieve the channel number for SDP registration.</span></span>

<span data-ttu-id="03983-118">應用程式應該使用伺服器通道的自動設定。</span><span class="sxs-lookup"><span data-stu-id="03983-118">Applications should use auto-allocation for the server channel.</span></span>

<span data-ttu-id="03983-119">系 [](/windows/desktop/api/winsock/nf-winsock-bind)結函式不會使用藍牙 SDP 自動通告伺服器應用程式;應用程式必須呼叫 [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)函式，以供遠端藍牙應用程式找到。</span><span class="sxs-lookup"><span data-stu-id="03983-119">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function does not automatically advertise the server application using the Bluetooth SDP; applications must call the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to be found by remote Bluetooth applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03983-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="03983-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03983-121">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="03983-121">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="03983-122">**綁定**</span><span class="sxs-lookup"><span data-stu-id="03983-122">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 