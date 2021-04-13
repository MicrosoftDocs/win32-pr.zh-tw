---
title: 名稱服務
description: 本主題討論動態資料交換管理程式庫如何讓伺服器應用程式註冊其支援的服務名稱。
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- 'Windows 消費者介面，動態資料交換 (DDE) '
- 動態資料交換 (的 DDE) ，名稱服務
- DDE (動態資料交換) ，名稱服務
- '資料交換、動態資料交換 (DDE) '
- 'Windows 消費者介面、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換管理程式庫 (DDEML) ，名稱服務
- DDEML (動態資料交換管理程式庫) ，名稱服務
- '資料交換、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換 (的 DDE) ，服務名稱註冊
- DDE (動態資料交換) ，服務名稱註冊
- 動態資料交換管理程式庫 (DDEML) ，服務名稱註冊
- DDEML (動態資料交換管理程式庫) ，服務名稱註冊
- 動態資料交換 (的 DDE) ，服務名稱篩選
- DDE (動態資料交換) ，服務名稱篩選
- 動態資料交換管理程式庫 (DDEML) ，服務名稱篩選
- DDEML (動態資料交換管理程式庫) ，服務名稱篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f958ab73164e70177cb5deeb5f400f44695015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311499"
---
# <a name="name-service"></a><span data-ttu-id="34883-119">名稱服務</span><span class="sxs-lookup"><span data-stu-id="34883-119">Name Service</span></span>

<span data-ttu-id="34883-120">動態資料交換管理程式庫 (DDEML) 讓伺服器應用程式能夠註冊它所支援的服務名稱，以及防止 DDEML 將不支援之服務名稱的 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易傳送到伺服器動態資料交換 (的) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="34883-120">The Dynamic Data Exchange Management Library (DDEML) makes it possible for a server application to register the service names that it supports and to prevent the DDEML from sending [**XTYP\_CONNECT**](xtyp-connect.md) transactions for unsupported service names to the server's Dynamic Data Exchange (DDE) callback function.</span></span>

<span data-ttu-id="34883-121">下列主題描述名稱服務。</span><span class="sxs-lookup"><span data-stu-id="34883-121">The following topics describe the name service.</span></span>

-   [<span data-ttu-id="34883-122">服務名稱註冊</span><span class="sxs-lookup"><span data-stu-id="34883-122">Service Name Registration</span></span>](#service-name-registration)
-   [<span data-ttu-id="34883-123">服務名稱篩選</span><span class="sxs-lookup"><span data-stu-id="34883-123">Service Name Filter</span></span>](#service-name-filter)

## <a name="service-name-registration"></a><span data-ttu-id="34883-124">服務名稱註冊</span><span class="sxs-lookup"><span data-stu-id="34883-124">Service Name Registration</span></span>

<span data-ttu-id="34883-125">藉由向 DDEML 註冊其服務名稱，伺服器會通知系統中有新伺服器可用的其他 DDE 應用程式。</span><span class="sxs-lookup"><span data-stu-id="34883-125">By registering its service names with the DDEML, a server informs other DDE applications in the system that a new server is available.</span></span> <span data-ttu-id="34883-126">伺服器會藉由呼叫 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) 函數並指定可識別名稱的字串控制碼，來註冊服務名稱。</span><span class="sxs-lookup"><span data-stu-id="34883-126">A server registers a service name by calling the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function and specifying a string handle that identifies the name.</span></span> <span data-ttu-id="34883-127">在回應中，DDEML 會將 [**XTYP \_**](xtyp-register.md)暫存器交易傳送到系統 (中每個 DDEML 應用程式的回呼函式，除了在 DdeInitialize 函式中指定 CBF \_ SKIP \_ 註冊篩選旗標的) 。 [](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)</span><span class="sxs-lookup"><span data-stu-id="34883-127">In response, the DDEML sends an [**XTYP\_REGISTER**](xtyp-register.md) transaction to the callback function of each DDEML application in the system (except those that specified the CBF\_SKIP\_REGISTRATIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span> <span data-ttu-id="34883-128">**XTYP \_ REGISTER** 交易會將兩個字串控制碼傳遞給回呼函式：第一個會識別指定基底服務名稱的字串，而第二個則會識別指定實例特定服務的字串。</span><span class="sxs-lookup"><span data-stu-id="34883-128">The **XTYP\_REGISTER** transaction passes two string handles to a callback function: the first identifies the string specifying the base service name, and the second identifies the string specifying the instance-specific service.</span></span> <span data-ttu-id="34883-129">用戶端通常會使用可用伺服器清單中的基本服務名稱，讓使用者可以從清單中選取伺服器。</span><span class="sxs-lookup"><span data-stu-id="34883-129">A client typically uses the base service name in a list of available servers, so the user can select a server from the list.</span></span> <span data-ttu-id="34883-130">如果有多個實例正在執行，則用戶端會使用實例特定服務名稱來建立與伺服器應用程式之特定實例的交談。</span><span class="sxs-lookup"><span data-stu-id="34883-130">The client uses the instance-specific service name to establish a conversation with a specific instance of a server application, if more than one instance is running.</span></span>

<span data-ttu-id="34883-131">伺服器可以使用 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) 來取消註冊服務名稱。</span><span class="sxs-lookup"><span data-stu-id="34883-131">A server can use [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to unregister a service name.</span></span> <span data-ttu-id="34883-132">此函式會讓 DDEML 將 [**XTYP \_ 取消註冊**](xtyp-unregister.md) 交易傳送到系統中的其他 DDE 應用程式，通知他們無法再使用該名稱來建立交談。</span><span class="sxs-lookup"><span data-stu-id="34883-132">This function causes the DDEML to send [**XTYP\_UNREGISTER**](xtyp-unregister.md) transactions to the other DDE applications in the system, informing them that they can no longer use the name to establish conversations.</span></span>

<span data-ttu-id="34883-133">在呼叫 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)之後，伺服器必須呼叫 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)來立即註冊其服務名稱。</span><span class="sxs-lookup"><span data-stu-id="34883-133">A server must call [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names soon after calling [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span></span> <span data-ttu-id="34883-134">伺服器必須在呼叫 [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)函式之前，先使用 **DdeNameService** 取消註冊其服務名稱。</span><span class="sxs-lookup"><span data-stu-id="34883-134">A server must unregister its service names by using **DdeNameService** just before calling the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span>

## <a name="service-name-filter"></a><span data-ttu-id="34883-135">服務名稱篩選</span><span class="sxs-lookup"><span data-stu-id="34883-135">Service Name Filter</span></span>

<span data-ttu-id="34883-136">除了註冊服務名稱之外， [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) 還可讓伺服器開啟或關閉其服務名稱篩選。</span><span class="sxs-lookup"><span data-stu-id="34883-136">In addition to registering service names, [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) enables a server to turn its service name filter on or off.</span></span> <span data-ttu-id="34883-137">當伺服器關閉其服務名稱篩選時，DDEML 會在任何用戶端呼叫 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)函式時，不論函式中指定的服務名稱為何，都會將 [**XTYP \_ CONNECT**](xtyp-connect.md)交易傳送到伺服器的 DDE 回呼函式。</span><span class="sxs-lookup"><span data-stu-id="34883-137">When a server turns off its service name filter, the DDEML sends the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the server's DDE callback function whenever any client calls the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function, regardless of the service name specified in the function.</span></span> <span data-ttu-id="34883-138">當伺服器開啟其服務名稱篩選時，DDEML 只會在 **DdeConnect** 指定伺服器在 **DdeNameService** 呼叫中指定的服務名稱時，才會將 **XTYP \_ CONNECT** 交易傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="34883-138">When a server turns on its service name filter, the DDEML sends the **XTYP\_CONNECT** transaction to the server only when **DdeConnect** specifies a service name the server has specified in a call to **DdeNameService**.</span></span>

<span data-ttu-id="34883-139">根據預設，當應用程式呼叫 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)時，服務名稱篩選為開啟。</span><span class="sxs-lookup"><span data-stu-id="34883-139">By default, the service name filter is on when an application calls [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span></span> <span data-ttu-id="34883-140">此預設值可防止 DDEML 在伺服器建立字串處理所需的字串之前，將 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="34883-140">This default prevents the DDEML from sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to a server before the server has created the string handles it needs.</span></span> <span data-ttu-id="34883-141">伺服器可以在呼叫 DdeNameService 時指定 DNS FILTEROFF 旗標，以關閉其服務名稱篩選 \_ 。 [](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)</span><span class="sxs-lookup"><span data-stu-id="34883-141">A server can turn off its service name filter by specifying the DNS\_FILTEROFF flag in a call to [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="34883-142">DNS \_ 篩選旗標會開啟篩選。</span><span class="sxs-lookup"><span data-stu-id="34883-142">The DNS\_FILTERON flag turns on the filter.</span></span>

 

 




