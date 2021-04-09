---
title: 藍牙和 WSALookupServiceNext
description: 藍牙使用 WSALookupServiceNext 函式來比對 WSALookupServiceBegin 先前呼叫中所指定的查詢。
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- 藍牙和 WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3ece06e27c9e80e25f22ef0fb09a5790cdf69b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842351"
---
# <a name="bluetooth-and-wsalookupservicenext"></a><span data-ttu-id="665db-106">藍牙和 WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="665db-106">Bluetooth and WSALookupServiceNext</span></span>

<span data-ttu-id="665db-107">藍牙使用 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) 函式來比對 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)先前呼叫中所指定的查詢。</span><span class="sxs-lookup"><span data-stu-id="665db-107">Bluetooth uses the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function to match queries specified in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span></span> <span data-ttu-id="665db-108">**WSALookupServiceNext** 函式的結果取決於在初始 **WSALookupServiceBegin** 函式呼叫中傳遞的 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構中所設定的設定。</span><span class="sxs-lookup"><span data-stu-id="665db-108">The results of the **WSALookupServiceNext** function are determined by settings set forth in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed in the initial **WSALookupServiceBegin** function call.</span></span>

<span data-ttu-id="665db-109">在藍牙中進行裝置查詢和服務探索的步驟，與進行不同的處理方式有足夠的差異。</span><span class="sxs-lookup"><span data-stu-id="665db-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="665db-110">如需藍牙和裝置查詢的 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) 函式的詳細資訊，請參閱 [藍牙和 WSALookupServiceBegin 中的裝置查詢](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)。</span><span class="sxs-lookup"><span data-stu-id="665db-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="665db-111">如需有關藍牙和服務探索之 **WSALookupServiceBegin** 功能的詳細資訊，請參閱 [適用于服務探索的藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="665db-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="665db-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="665db-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="665db-113">探索藍牙裝置和服務</span><span class="sxs-lookup"><span data-stu-id="665db-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="665db-114">適用于裝置查詢的藍牙和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="665db-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="665db-115">適用于服務探索的藍牙和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="665db-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="665db-116">藍牙和 WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="665db-116">Bluetooth and WSALookupServiceEnd</span></span>](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="665db-117">**BTH \_ 查詢 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="665db-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="665db-118">**連線**</span><span class="sxs-lookup"><span data-stu-id="665db-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="665db-119">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="665db-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="665db-120">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="665db-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="665db-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="665db-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="665db-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="665db-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="665db-123">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="665db-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 