---
description: 名稱解析函式可以分為三種類別：服務安裝、用戶端查詢和 helper (與宏) 。
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: 名稱解析函數的摘要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690376"
---
# <a name="summary-of-name-resolution-functions"></a><span data-ttu-id="29295-103">名稱解析函數的摘要</span><span class="sxs-lookup"><span data-stu-id="29295-103">Summary of Name Resolution Functions</span></span>

<span data-ttu-id="29295-104">名稱解析函式可以分為三種類別：服務安裝、用戶端查詢和 helper (與宏) 。</span><span class="sxs-lookup"><span data-stu-id="29295-104">The name resolution functions can be grouped into three categories: Service installation, client queries, and helper (with macros).</span></span> <span data-ttu-id="29295-105">接下來的各節會識別每個類別中的函式，並簡要描述其預定用途。</span><span class="sxs-lookup"><span data-stu-id="29295-105">The sections that follow identify the functions in each category and briefly describe their intended use.</span></span> <span data-ttu-id="29295-106">也會描述重要的資料結構。</span><span class="sxs-lookup"><span data-stu-id="29295-106">Key data structures are also described.</span></span>

## <a name="service-installation"></a><span data-ttu-id="29295-107">服務安裝</span><span class="sxs-lookup"><span data-stu-id="29295-107">Service Installation</span></span>

-   [<span data-ttu-id="29295-108">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="29295-108">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [<span data-ttu-id="29295-109">**WSARemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="29295-109">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [<span data-ttu-id="29295-110">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="29295-110">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

<span data-ttu-id="29295-111">當必要的服務類別不存在時，應用程式會使用 [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) 來安裝新的服務類別，方法是提供服務類別名稱、服務類別識別碼的 GUID，以及一系列的 [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) 結構。</span><span class="sxs-lookup"><span data-stu-id="29295-111">When the required service class does not already exist, an application uses [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="29295-112">這些結構各自適用于特定的命名空間，並提供一般值，例如建議的 TCP 埠號碼或 NetWare SAP 識別碼。</span><span class="sxs-lookup"><span data-stu-id="29295-112">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="29295-113">您可以藉由呼叫 [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) 並提供對應至類別識別碼的 GUID，來移除服務類別。</span><span class="sxs-lookup"><span data-stu-id="29295-113">A service class can be removed by calling [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="29295-114">服務類別存在之後，就可以透過 [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)安裝或移除服務的特定實例。</span><span class="sxs-lookup"><span data-stu-id="29295-114">Once a service class exists, specific instances of a service can be installed or removed through [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span></span> <span data-ttu-id="29295-115">此函式會採用 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構做為輸入參數，以及作業程式碼和作業旗標。</span><span class="sxs-lookup"><span data-stu-id="29295-115">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="29295-116">作業程式碼會指出服務是否正在安裝或移除。</span><span class="sxs-lookup"><span data-stu-id="29295-116">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="29295-117">**WSAQUERYSET** 結構提供服務的所有相關資訊，包括服務類別識別碼、此實例的服務名稱 () 、適用的命名空間識別碼和通訊協定資訊，以及服務接聽的一組傳輸位址。</span><span class="sxs-lookup"><span data-stu-id="29295-117">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses at which the service listens.</span></span> <span data-ttu-id="29295-118">服務應該在初始化時叫用 **WSASetService** ，以通告其在動態命名空間中的存在。</span><span class="sxs-lookup"><span data-stu-id="29295-118">Services should invoke **WSASetService** when they initialize to advertise their presence in dynamic namespaces.</span></span>

## <a name="client-query"></a><span data-ttu-id="29295-119">用戶端查詢</span><span class="sxs-lookup"><span data-stu-id="29295-119">Client Query</span></span>

-   [<span data-ttu-id="29295-120">**WSAEnumNameSpaceProviders**</span><span class="sxs-lookup"><span data-stu-id="29295-120">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [<span data-ttu-id="29295-121">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="29295-121">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [<span data-ttu-id="29295-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="29295-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [<span data-ttu-id="29295-123">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="29295-123">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

<span data-ttu-id="29295-124">[**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)函式可讓應用程式探索可透過 Winsock 名稱解析功能存取哪些命名空間。</span><span class="sxs-lookup"><span data-stu-id="29295-124">The [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) function allows an application to discover which namespaces are accessible through Winsock name resolution facilities.</span></span> <span data-ttu-id="29295-125">它也可讓應用程式判斷是否有一個以上的命名空間提供者支援指定的命名空間，以及探索任何特定命名空間提供者的提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="29295-125">It also allows an application to determine whether a given namespace is supported by more than one namespace provider, and to discover the provider identifier for any particular namespace provider.</span></span> <span data-ttu-id="29295-126">使用提供者識別碼，應用程式可以將查詢作業限制為指定的命名空間提供者。</span><span class="sxs-lookup"><span data-stu-id="29295-126">Using a provider identifier, the application can restrict a query operation to a specified namespace provider.</span></span>

<span data-ttu-id="29295-127">Winsock 命名空間–查詢作業牽涉到一連串的呼叫： [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)，後面接著一或多個 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 的呼叫，然後以 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)的呼叫結尾。</span><span class="sxs-lookup"><span data-stu-id="29295-127">Winsock namespace–query operations involve a series of calls: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), followed by one or more calls to [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) and ending with a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="29295-128">**WSALookupServiceBegin** 會採用 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構作為輸入，來定義查詢參數以及一組旗標，以提供對搜尋作業的額外控制。</span><span class="sxs-lookup"><span data-stu-id="29295-128">**WSALookupServiceBegin** takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as input to define the query parameters along with a set of flags to provide additional control over the search operation.</span></span> <span data-ttu-id="29295-129">它會傳回查詢控制碼，此控制碼用於後續呼叫 **WSALookupServiceNext** 和 **WSALookupServiceEnd**。</span><span class="sxs-lookup"><span data-stu-id="29295-129">It returns a query handle which is used in the subsequent calls to **WSALookupServiceNext** and **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="29295-130">應用程式會叫用 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 來取得查詢結果，並在應用程式提供的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 緩衝區中提供結果。</span><span class="sxs-lookup"><span data-stu-id="29295-130">The application invokes [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) to obtain query results, with results supplied in an application-supplied [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) buffer.</span></span> <span data-ttu-id="29295-131">應用程式會繼續呼叫 **WSALookupServiceNext** ，直到錯誤碼 \_ \_ 不會再傳回錯誤訊息 \_ ，指出已取出所有結果。</span><span class="sxs-lookup"><span data-stu-id="29295-131">The application continues to call **WSALookupServiceNext** until the error code WSA\_E\_NO\_MORE is returned indicating that all results have been retrieved.</span></span> <span data-ttu-id="29295-132">然後搜尋會透過呼叫 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)來終止。</span><span class="sxs-lookup"><span data-stu-id="29295-132">The search is then terminated by a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="29295-133">從另一個執行緒呼叫時， **WSALookupServiceEnd** 函式也可以用來取消目前暫止的 **WSALookupServiceNext** 。</span><span class="sxs-lookup"><span data-stu-id="29295-133">The **WSALookupServiceEnd** function can also be used to cancel a currently pending **WSALookupServiceNext** when called from another thread.</span></span>

<span data-ttu-id="29295-134">在 Windows 通訊端2中，WSAENOMORE (10102) 和 WSA \_ E \_ 不再 \_ (10110) 定義了衝突的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="29295-134">In Windows Sockets 2, conflicting error codes are defined for WSAENOMORE (10102) and WSA\_E\_NO\_MORE (10110).</span></span> <span data-ttu-id="29295-135">錯誤碼 WSAENOMORE 將會在未來的版本中移除，而且只有 WSA \_ E \_ 不再有 \_ 其他會保留。</span><span class="sxs-lookup"><span data-stu-id="29295-135">The error code WSAENOMORE will be removed in a future version and only WSA\_E\_NO\_MORE will remain.</span></span> <span data-ttu-id="29295-136">但是針對 Windows 通訊端2，應用程式應該同時檢查 WSAENOMORE 和 WSA \_ E \_ ， \_ 以找出最廣泛的可能與使用其中一個命名空間提供者的相容性。</span><span class="sxs-lookup"><span data-stu-id="29295-136">For Windows Sockets 2, however, applications should check for both WSAENOMORE and WSA\_E\_NO\_MORE for the widest possible compatibility with namespace providers that use either one.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="29295-137">輔助函式</span><span class="sxs-lookup"><span data-stu-id="29295-137">Helper Functions</span></span>

-   [<span data-ttu-id="29295-138">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="29295-138">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [<span data-ttu-id="29295-139">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="29295-139">**WSAAddressToString**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [<span data-ttu-id="29295-140">**WSAStringToAddress**</span><span class="sxs-lookup"><span data-stu-id="29295-140">**WSAStringToAddress**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [<span data-ttu-id="29295-141">**WSAGetServiceClassInfo**</span><span class="sxs-lookup"><span data-stu-id="29295-141">**WSAGetServiceClassInfo**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

<span data-ttu-id="29295-142">名稱解析協助程式函式包含函式，可在給定服務類別識別碼的情況下，取得服務類別名稱、一組用來在 [**SOCKADDR**](sockaddr-2.md) 結構與 ASCII 字串表示之間轉譯傳輸位址的函式、用來取得指定服務類別之服務類別架構資訊的函式，以及用來將已知服務對應至預先配置 guid 的一組宏。</span><span class="sxs-lookup"><span data-stu-id="29295-142">The name resolution helper functions include a function to retrieve a service class name given a service class identifier, a pair of functions used to translate a transport address between a [**SOCKADDR**](sockaddr-2.md) structure and an ASCII string representation, a function to retrieve the service class schema information for a given service class, and a set of macros for mapping well known services to preallocated GUIDs.</span></span>

<span data-ttu-id="29295-143">下列來自 Winsock2 的宏有助於在知名的服務類別與這些命名空間之間進行對應：</span><span class="sxs-lookup"><span data-stu-id="29295-143">The following macros from Winsock2.h aid in mapping between well known service classes and these namespaces:</span></span>

| <span data-ttu-id="29295-144">巨集</span><span class="sxs-lookup"><span data-stu-id="29295-144">Macro</span></span>                                                                                                            | <span data-ttu-id="29295-145">Description</span><span class="sxs-lookup"><span data-stu-id="29295-145">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29295-146">SVCID \_ TCP (埠) SVCID \_ UDP (埠) </span><span class="sxs-lookup"><span data-stu-id="29295-146">SVCID\_TCP(Port) SVCID\_UDP(Port)</span></span><br/> <span data-ttu-id="29295-147">SVCID \_ NETWARE (物件類型) </span><span class="sxs-lookup"><span data-stu-id="29295-147">SVCID\_NETWARE(Object Type)</span></span><br/>                              | <span data-ttu-id="29295-148">如果有 TCP/IP 或 UDP/IP 的通訊埠，或是 NetWare 的物件類型，則會以主機順序) 傳回 GUID (埠號碼。</span><span class="sxs-lookup"><span data-stu-id="29295-148">Given a port for TCP/IP or UDP/IP or the object type in the case of NetWare, returns the GUID (port number in host order).</span></span> |
| <span data-ttu-id="29295-149">是 \_ SVCID \_ TCP (GUID) 是 \_ SVCID \_ UDP (guid) </span><span class="sxs-lookup"><span data-stu-id="29295-149">IS\_SVCID\_TCP(GUID)IS\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="29295-150">是 \_ SVCID \_ NETWARE (GUID) </span><span class="sxs-lookup"><span data-stu-id="29295-150">IS\_SVCID\_NETWARE(GUID)</span></span><br/>                          | <span data-ttu-id="29295-151">如果 GUID 位於允許的範圍內，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="29295-151">Returns **TRUE** if the GUID is within the allowable range.</span></span>                                                                |
| <span data-ttu-id="29295-152">設定 \_ TCP \_ SVCID (guid，PORT) set \_ UDP \_ SVCID (guid，port) </span><span class="sxs-lookup"><span data-stu-id="29295-152">SET\_TCP\_SVCID(GUID, port)SET\_UDP\_SVCID(GUID, port)</span></span><br/>                                                | <span data-ttu-id="29295-153">使用與 TCP 或 UDP 埠號碼相等的 GUID 來初始化 GUID 結構， (埠號碼必須在主機順序) 中。</span><span class="sxs-lookup"><span data-stu-id="29295-153">Initializes a GUID structure with the GUID equivalent for a TCP or UDP port number (port number must be in host order).</span></span>    |
| <span data-ttu-id="29295-154">\_從 \_ SVCID \_ TCP (GUID) 埠 \_ 從 \_ SVCID \_ UDP (guid 的埠) </span><span class="sxs-lookup"><span data-stu-id="29295-154">PORT\_FROM\_SVCID\_TCP(GUID)PORT\_FROM\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="29295-155">\_從 \_ SVCID \_ NETWARE (GUID) SAPID</span><span class="sxs-lookup"><span data-stu-id="29295-155">SAPID\_FROM\_SVCID\_NETWARE(GUID)</span></span><br/> | <span data-ttu-id="29295-156">傳回與主機順序) 中的 GUID (埠號碼相關聯的埠或物件類型。</span><span class="sxs-lookup"><span data-stu-id="29295-156">Returns the port or object type associated with the GUID (port number in host order).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="29295-157">相關主題</span><span class="sxs-lookup"><span data-stu-id="29295-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29295-158">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="29295-158">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="29295-159">**GetAddrInfoEx**</span><span class="sxs-lookup"><span data-stu-id="29295-159">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[<span data-ttu-id="29295-160">**GetAddrInfoW**</span><span class="sxs-lookup"><span data-stu-id="29295-160">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[<span data-ttu-id="29295-161">**getnameinfo**</span><span class="sxs-lookup"><span data-stu-id="29295-161">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[<span data-ttu-id="29295-162">**GetNameInfoW**</span><span class="sxs-lookup"><span data-stu-id="29295-162">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[<span data-ttu-id="29295-163">名稱解析資料結構</span><span class="sxs-lookup"><span data-stu-id="29295-163">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="29295-164">名稱解析模型</span><span class="sxs-lookup"><span data-stu-id="29295-164">Name Resolution Model</span></span>](name-resolution-model-2.md)
</dt> <dt>

[<span data-ttu-id="29295-165">通訊協定獨立名稱解析</span><span class="sxs-lookup"><span data-stu-id="29295-165">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="29295-166">註冊和名稱解析</span><span class="sxs-lookup"><span data-stu-id="29295-166">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="29295-167">**SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="29295-167">**SOCKADDR**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="29295-168">**WSAEnumNameSpaceProviders**</span><span class="sxs-lookup"><span data-stu-id="29295-168">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[<span data-ttu-id="29295-169">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="29295-169">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[<span data-ttu-id="29295-170">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="29295-170">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[<span data-ttu-id="29295-171">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="29295-171">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="29295-172">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="29295-172">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="29295-173">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="29295-173">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="29295-174">**WSARemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="29295-174">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[<span data-ttu-id="29295-175">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="29295-175">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[<span data-ttu-id="29295-176">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="29295-176">**WSAQUERYSET**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="29295-177">**WSANSCLASSINFO**</span><span class="sxs-lookup"><span data-stu-id="29295-177">**WSANSCLASSINFO**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




