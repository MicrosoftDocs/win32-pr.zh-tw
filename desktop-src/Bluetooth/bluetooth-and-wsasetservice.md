---
title: 藍牙和 WSASetService
description: 藍牙使用 WSASetService 函式來註冊或移除藍牙命名空間內的服務實例， (NS \_ BTH) 從登錄。
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- 藍牙藍牙
- WSASetService 藍牙
- 藍牙與 WSASetService 藍牙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463209"
---
# <a name="bluetooth-and-wsasetservice"></a><span data-ttu-id="6e2a9-106">藍牙和 WSASetService</span><span class="sxs-lookup"><span data-stu-id="6e2a9-106">Bluetooth and WSASetService</span></span>

<span data-ttu-id="6e2a9-107">藍牙使用 [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) 函式來註冊或移除藍牙命名空間內的服務實例， (NS \_ BTH) 從登錄。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-107">Bluetooth uses the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to register or remove a service instance within the Bluetooth namespace (NS\_BTH) from the registry.</span></span> <span data-ttu-id="6e2a9-108">這項作業所傳回的控制碼只能用來刪除服務。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-108">The handle returned by this operation may only be used to delete the service.</span></span>

<span data-ttu-id="6e2a9-109">藍牙有兩種使用 [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) 函式來通告服務的方法：</span><span class="sxs-lookup"><span data-stu-id="6e2a9-109">Bluetooth has two means of advertising services using the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function:</span></span>

-   <span data-ttu-id="6e2a9-110">此應用程式可以讓系統通告簡單的藍牙 SDP 服務記錄，並從 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) 結構中的標準成員進行建立。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-110">The application can have the system advertise a simple Bluetooth SDP service record, constructed from standard members in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span>
-   <span data-ttu-id="6e2a9-111">應用程式可以讓系統通告自己的藍牙 SDP 記錄，方法是在 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的 **lpBlob** 成員中傳遞 [**BTH \_ SET \_ 服務**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)結構。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-111">The application can have the system advertise their own Bluetooth SDP record by passing a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure in the **lpBlob** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="6e2a9-112">這是更複雜的方法。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-112">This is a more complex approach.</span></span>

> [!Note]  
> <span data-ttu-id="6e2a9-113">[**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)公告的 SDP 記錄不會在發行它們的進程結束後保存。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-113">SDP records advertised by [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) do not persist after the process that published them has quit.</span></span>

 

<span data-ttu-id="6e2a9-114">使用 [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) 搭配藍牙有下列需求：</span><span class="sxs-lookup"><span data-stu-id="6e2a9-114">Use of [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="6e2a9-115">*LpqsRegInfo* 參數是要註冊之 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構的位址。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-115">The *lpqsRegInfo* parameter is the address of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to be registered.</span></span>
-   <span data-ttu-id="6e2a9-116">*EssOperation* 參數是一種列舉，其中包含下表所示的其中一項作業。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-116">The *essOperation* parameter is an enumeration that contains one of the operations shown in the following table.</span></span>



| <span data-ttu-id="6e2a9-117">值</span><span class="sxs-lookup"><span data-stu-id="6e2a9-117">Value</span></span>                  | <span data-ttu-id="6e2a9-118">描述</span><span class="sxs-lookup"><span data-stu-id="6e2a9-118">Description</span></span>                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e2a9-119">RNRSERVICE \_ 註冊</span><span class="sxs-lookup"><span data-stu-id="6e2a9-119">RNRSERVICE\_REGISTER</span></span>   | <span data-ttu-id="6e2a9-120">使用藍牙 SDP 通訊協定開始通告服務，以進行遠端無線電波查詢。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-120">Starts advertising the service to remote radios querying using the Bluetooth SDP protocol.</span></span> |
| <span data-ttu-id="6e2a9-121">RNRSERVICE 取消 \_ 註冊</span><span class="sxs-lookup"><span data-stu-id="6e2a9-121">RNRSERVICE\_DEREGISTER</span></span> | <span data-ttu-id="6e2a9-122">無效。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-122">Not valid.</span></span> <span data-ttu-id="6e2a9-123">傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-123">Returns an error.</span></span>                                                               |
| <span data-ttu-id="6e2a9-124">RNRSERVICE \_ 刪除</span><span class="sxs-lookup"><span data-stu-id="6e2a9-124">RNRSERVICE\_DELETE</span></span>     | <span data-ttu-id="6e2a9-125">停止通告服務。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-125">Stops advertising the service.</span></span>                                                             |



 

> [!Note]  
> <span data-ttu-id="6e2a9-126">在 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) 或 [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) 呼叫期間探索到的服務控制碼與 RNRSERVICE 刪除作業不相容 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-126">Service handles discovered during a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) or [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) call are incompatible with the RNRSERVICE\_DELETE operation.</span></span>

 

-   <span data-ttu-id="6e2a9-127">*DwControlFlags* 參數是保留的，而且必須為零。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-127">The *dwControlFlags* parameter is reserved, and must be zero.</span></span>

<span data-ttu-id="6e2a9-128">如需詳細資訊和藍牙通訊端選項的清單，請參閱 [藍牙和通訊端選項](bluetooth-and-socket-options.md)。</span><span class="sxs-lookup"><span data-stu-id="6e2a9-128">For more information and a list of Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e2a9-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e2a9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e2a9-130">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6e2a9-130">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 