---
title: 藍牙和 WSALookupServiceEnd
description: 藍牙使用 WSALookupServiceEnd 函式來終止先前呼叫 WSALookupServiceBegin 時起始的查詢，而且可能會在後續的 WSALookupServiceNext 呼叫中延伸。
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- 藍牙和 WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933325"
---
# <a name="bluetooth-and-wsalookupserviceend"></a><span data-ttu-id="b93ff-106">藍牙和 WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="b93ff-106">Bluetooth and WSALookupServiceEnd</span></span>

<span data-ttu-id="b93ff-107">藍牙使用 [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) 函式來終止先前呼叫 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)時起始的查詢，而且可能會在後續的 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)呼叫中延伸。</span><span class="sxs-lookup"><span data-stu-id="b93ff-107">Bluetooth uses the [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) function to terminate a query initiated in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), and perhaps extended in subsequent calls to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span> <span data-ttu-id="b93ff-108">呼叫 **WSALookupServiceEnd** 會終止查詢並清除內容。</span><span class="sxs-lookup"><span data-stu-id="b93ff-108">The call to **WSALookupServiceEnd** terminates the query and cleans up the context.</span></span>

<span data-ttu-id="b93ff-109">在藍牙中進行裝置查詢和服務探索的步驟，與進行不同的處理方式有足夠的差異。</span><span class="sxs-lookup"><span data-stu-id="b93ff-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="b93ff-110">如需藍牙和裝置查詢的 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) 函式的詳細資訊，請參閱 [藍牙和 WSALookupServiceBegin 中的裝置查詢](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)。</span><span class="sxs-lookup"><span data-stu-id="b93ff-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="b93ff-111">如需有關藍牙和服務探索之 **WSALookupServiceBegin** 功能的詳細資訊，請參閱 [適用于服務探索的藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="b93ff-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b93ff-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="b93ff-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b93ff-113">探索藍牙裝置和服務</span><span class="sxs-lookup"><span data-stu-id="b93ff-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="b93ff-114">適用于裝置查詢的藍牙和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="b93ff-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="b93ff-115">適用于服務探索的藍牙和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="b93ff-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="b93ff-116">藍牙和 WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="b93ff-116">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="b93ff-117">**BTH \_ 查詢 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="b93ff-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="b93ff-118">**連線**</span><span class="sxs-lookup"><span data-stu-id="b93ff-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="b93ff-119">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="b93ff-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="b93ff-120">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="b93ff-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="b93ff-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="b93ff-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="b93ff-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="b93ff-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="b93ff-123">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="b93ff-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="b93ff-124">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="b93ff-124">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 