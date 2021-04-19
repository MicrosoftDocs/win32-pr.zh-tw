---
title: 探索藍牙裝置和服務
description: 為了協助探索藍牙裝置和服務，Windows 會將藍牙服務探索通訊協定 (SDP) 對應至 Windows 通訊端命名空間介面。
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- 藍牙，工作，探索裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/07/2020
ms.locfileid: "106966025"
---
# <a name="discovering-bluetooth-devices-and-services"></a><span data-ttu-id="361ab-104">探索藍牙裝置和服務</span><span class="sxs-lookup"><span data-stu-id="361ab-104">Discovering Bluetooth Devices and Services</span></span>

<span data-ttu-id="361ab-105">為了協助探索藍牙裝置和服務，Windows 會將藍牙服務探索通訊協定 (SDP) 對應至 Windows 通訊端命名空間介面。</span><span class="sxs-lookup"><span data-stu-id="361ab-105">To facilitate the discovery of Bluetooth devices and services, Windows maps the Bluetooth Service Discovery Protocol (SDP) onto the Windows Sockets namespace interfaces.</span></span> <span data-ttu-id="361ab-106">用於此對應的主要函式為 [**WSASetService**](bluetooth-and-wsasetservice.md)、 [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)、 [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)和 [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="361ab-106">The primary functions used for this mapping are the [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) functions.</span></span> <span data-ttu-id="361ab-107">[**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)結構也會與這些函式一起使用。</span><span class="sxs-lookup"><span data-stu-id="361ab-107">The [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure is also used in conjunction with these functions.</span></span>

<span data-ttu-id="361ab-108">由於藍牙 SDP 的特定概念和參數不一定會直接對應至 [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) 結構，因此必須將注意的方式納入其成員的建立與使用方式。</span><span class="sxs-lookup"><span data-stu-id="361ab-108">Because certain concepts and parameters from the Bluetooth SDP do not necessarily map directly into the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure, attention must be paid to how its members are created and used.</span></span> <span data-ttu-id="361ab-109">針對許多複雜的藍牙作業（例如建立 SDP 記錄），會使用 **WSAQUERYSET** 的 **lpBlob** 成員。</span><span class="sxs-lookup"><span data-stu-id="361ab-109">For many complex Bluetooth operations, such as the creation of SDP records, the **lpBlob** member of the **WSAQUERYSET** is used.</span></span> <span data-ttu-id="361ab-110">當需要這類特殊考慮時，會特別說明，例如在 [**藍牙和 WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)等參考頁面中。</span><span class="sxs-lookup"><span data-stu-id="361ab-110">When such special consideration is necessary, it is specifically described, such as in reference pages like [**Bluetooth and WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and others.</span></span>

<span data-ttu-id="361ab-111">請務必瞭解，SDP 註冊與通訊端控制不同。</span><span class="sxs-lookup"><span data-stu-id="361ab-111">It is important to understand that SDP registration is separate from socket control.</span></span> <span data-ttu-id="361ab-112">當伺服器應用程式準備接受用戶端連接時，它應該呼叫 [**WSASetService**](bluetooth-and-wsasetservice.md) 函式來登錄與該服務對應的藍牙 SDP 記錄。</span><span class="sxs-lookup"><span data-stu-id="361ab-112">When a server application is prepared to accept client connection, it should call the [**WSASetService**](bluetooth-and-wsasetservice.md) function to register a Bluetooth SDP record that corresponds to that service.</span></span> <span data-ttu-id="361ab-113">藍牙應用程式必須在關閉之前再次呼叫 **WSASetService** 函式，以取消註冊藍牙 SDP 記錄。</span><span class="sxs-lookup"><span data-stu-id="361ab-113">That Bluetooth application must call the **WSASetService** function again before closing, to deregister the Bluetooth SDP record.</span></span>

<span data-ttu-id="361ab-114">使用此頁面所述的對應函式時， \_ 會指派 NS BTH 命名空間。</span><span class="sxs-lookup"><span data-stu-id="361ab-114">When using the mapping functions described on this page, the NS\_BTH namespace is assigned.</span></span>

<span data-ttu-id="361ab-115">如需探索裝置和服務的詳細資訊，請參閱下列參考頁面：</span><span class="sxs-lookup"><span data-stu-id="361ab-115">For further information about discovering devices and services, consult the following reference pages:</span></span>

-   [<span data-ttu-id="361ab-116">**藍牙和 WSASetService**</span><span class="sxs-lookup"><span data-stu-id="361ab-116">**Bluetooth and WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
-   [<span data-ttu-id="361ab-117">**適用于裝置查詢的藍牙和 WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="361ab-117">**Bluetooth and WSALookupServiceBegin for Device Inquiry**</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [<span data-ttu-id="361ab-118">**適用于服務探索的藍牙和 WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="361ab-118">**Bluetooth and WSALookupServiceBegin for Service Discovery**</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [<span data-ttu-id="361ab-119">**藍牙和 WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="361ab-119">**Bluetooth and WSALookupServiceNext**</span></span>](bluetooth-and-wsalookupservicenext.md)
-   [<span data-ttu-id="361ab-120">**藍牙和 WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="361ab-120">**Bluetooth and WSALookupServiceEnd**</span></span>](bluetooth-and-wsalookupserviceend.md)
-   [<span data-ttu-id="361ab-121">**藍牙和 BLOB**</span><span class="sxs-lookup"><span data-stu-id="361ab-121">**Bluetooth and BLOB**</span></span>](bluetooth-and-blob.md)
-   [<span data-ttu-id="361ab-122">**藍牙和 WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="361ab-122">**Bluetooth and WSAQUERYSET**</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)

<span data-ttu-id="361ab-123">您也可以下載 [藍牙連線範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) ，以取得完整的範例。</span><span class="sxs-lookup"><span data-stu-id="361ab-123">You can also download the [Bluetooth connection sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) for a complete example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="361ab-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="361ab-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="361ab-125">使用 Windows 通訊端進行藍牙程式設計</span><span class="sxs-lookup"><span data-stu-id="361ab-125">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[<span data-ttu-id="361ab-126">藍牙連接範例</span><span class="sxs-lookup"><span data-stu-id="361ab-126">Bluetooth connection sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




