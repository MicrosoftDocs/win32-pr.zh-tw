---
title: 藍牙和 BLOB
description: 藍牙會在呼叫 WSASetService 或 WSALookupService \ 函式期間，使用 BLOB 結構來傳遞或接收傳輸特定資料到 WSAQUERYSET 結構。
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- 藍牙和 BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968714"
---
# <a name="bluetooth-and-blob"></a><span data-ttu-id="aea7d-107">藍牙和 BLOB</span><span class="sxs-lookup"><span data-stu-id="aea7d-107">Bluetooth and BLOB</span></span>

<span data-ttu-id="aea7d-108">藍牙在呼叫 [**WSASetService**](bluetooth-and-wsasetservice.md)或 **WSALookupService** 函式時，會使用 [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)結構，在 [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)結構中傳遞或接收傳輸特定資料 \* 。</span><span class="sxs-lookup"><span data-stu-id="aea7d-108">Bluetooth uses the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure to pass or receive transport-specific data to the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure during calls to the [**WSASetService**](bluetooth-and-wsasetservice.md) or **WSALookupService**\* functions.</span></span>

<span data-ttu-id="aea7d-109">若要搭配藍牙和 [**WSASetService**](bluetooth-and-wsasetservice.md) 函式使用， [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) 結構成員必須具有下列設定：</span><span class="sxs-lookup"><span data-stu-id="aea7d-109">For use with Bluetooth and the [**WSASetService**](bluetooth-and-wsasetservice.md) function, the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure members are required to have the following settings:</span></span>

-   <span data-ttu-id="aea7d-110">**Cbsize** 成員必須設定為 **pBlobData** 成員中使用的 [**BTH \_ 集 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)結構大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="aea7d-110">The **cbsize** member must be set to the size of the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="aea7d-111">**PBlobData** 成員必須是 [**BTH \_ 設定 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aea7d-111">The **pBlobData** member must be a pointer to a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure.</span></span>

<span data-ttu-id="aea7d-112">若要搭配使用藍牙和 [WSALookupServiceBegin 來查詢裝置](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)，請使用下列設定：</span><span class="sxs-lookup"><span data-stu-id="aea7d-112">For use with Bluetooth and [WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use the following settings:</span></span>

-   <span data-ttu-id="aea7d-113">**Cbsize** 成員必須設定為 **pBlobData** 成員中使用的 [**BTH \_ 查詢 \_ 裝置**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)結構大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="aea7d-113">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="aea7d-114">**PBlobData** 成員必須是 [**BTH \_ 查詢 \_ 裝置**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aea7d-114">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure.</span></span>

<span data-ttu-id="aea7d-115">若要搭配使用藍牙和 [WSALookupServiceBegin 進行服務探索](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)，請使用下列設定：</span><span class="sxs-lookup"><span data-stu-id="aea7d-115">For use with Bluetooth and [WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use the following settings:</span></span>

-   <span data-ttu-id="aea7d-116">**Cbsize** 成員必須設定為 **pBlobData** 成員中使用的 [**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)結構大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="aea7d-116">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="aea7d-117">**PBlobData** 成員必須是 [**BTH \_ 查詢 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aea7d-117">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure.</span></span>

<span data-ttu-id="aea7d-118">如需詳細資訊，請參閱 [**BTH \_ 設定 \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) 結構參考頁面中的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="aea7d-118">For more information, see the Remarks section in the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure reference page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aea7d-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="aea7d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aea7d-120">適用于裝置查詢的藍牙和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="aea7d-120">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="aea7d-121">適用于服務探索的藍牙和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="aea7d-121">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="aea7d-122">藍牙和 WSASetService</span><span class="sxs-lookup"><span data-stu-id="aea7d-122">Bluetooth and WSASetService</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

[<span data-ttu-id="aea7d-123">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="aea7d-123">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="aea7d-124">**Blob**</span><span class="sxs-lookup"><span data-stu-id="aea7d-124">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="aea7d-125">**BTH \_ 查詢 \_ 裝置**</span><span class="sxs-lookup"><span data-stu-id="aea7d-125">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="aea7d-126">**BTH \_ 查詢 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="aea7d-126">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="aea7d-127">**BTH \_ 設定 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="aea7d-127">**BTH\_SET\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[<span data-ttu-id="aea7d-128">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="aea7d-128">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="aea7d-129">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="aea7d-129">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="aea7d-130">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="aea7d-130">**WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 