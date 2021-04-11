---
title: 使用 IpReleaseAddress、IpRenewAddress 管理 DHCP 租用
description: IpReleaseAddress 和 IpRenewAddress 函式可用來釋出並更新目前的動態主機設定通訊協定 (DHCP) 租用。
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847951"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a><span data-ttu-id="7e9a0-103">使用 IpReleaseAddress、IpRenewAddress 管理 DHCP 租用</span><span class="sxs-lookup"><span data-stu-id="7e9a0-103">Manage DHCP leases with IpReleaseAddress, IpRenewAddress</span></span>

<span data-ttu-id="7e9a0-104">[**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)和 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress)函式可用來釋出並更新目前的動態主機設定通訊協定 (DHCP) 租用。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-104">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions are used to release and renew the current Dynamic Host Configuration Protocol (DHCP) lease.</span></span> <span data-ttu-id="7e9a0-105">**IpReleaseAddress** 函式會釋放先前透過 DHCP 取得的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-105">The **IpReleaseAddress** function releases an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="7e9a0-106">**IpRenewAddress** 函式會在先前透過 DHCP 取得的 IPv4 位址上更新租用。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-106">The **IpRenewAddress** function renews a lease on an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="7e9a0-107">通常會搭配使用這兩個函式，先使用 **IpReleaseAddress** 呼叫來釋出租用，然後透過呼叫 **IpRenewAddress** 函式來更新租用。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-107">It is common to use these two functions together, first releasing the lease with a call to **IpReleaseAddress**, and then renewing the lease with a call to the **IpRenewAddress** function.</span></span>

<span data-ttu-id="7e9a0-108">如果 DHCP 用戶端先前已取得 DHCP 租用，而 [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) 未在 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) 功能之前呼叫，則會將 dhcp 用戶端要求傳送到發出初始 DHCP 租用的 dhcp 伺服器。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-108">When a DHCP client has previously obtained a DHCP lease and [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) is not called before the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, the DHCP client request is sent to the DHCP server that issued the initial DHCP lease.</span></span> <span data-ttu-id="7e9a0-109">此 DHCP 伺服器可能無法使用，或 DHCP 要求可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-109">This DHCP server may not available or the DHCP request may fail.</span></span> <span data-ttu-id="7e9a0-110">當主機先前取得 DHCP 租用，且 **IpReleaseAddress** 在 **IpRenewAddress** 函式之前呼叫，DHCP 用戶端會先釋出所取得的 IP 位址，並從任何可用的 dhcp 伺服器傳送回應的 dhcp 用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-110">When a host has previously obtained a DHCP lease and **IpReleaseAddress** is called before the **IpRenewAddress** function, the DHCP client first releases the IP address obtained and sends a DHCP client request for a response from any available DHCP server.</span></span>

> [!Note]  
> <span data-ttu-id="7e9a0-111">[**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)和 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress)函式需要啟用 DHCP 才能正確執行。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require that DHCP be enabled to perform correctly.</span></span>

 

<span data-ttu-id="7e9a0-112">[**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)函式會接受 [**IP \_ 介面卡 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map)結構的指標作為唯一的參數。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-112">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function takes a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure as its only parameter.</span></span> <span data-ttu-id="7e9a0-113">若要取得此參數，請先呼叫 [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-113">To obtain this parameter, first call [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span></span> <span data-ttu-id="7e9a0-114">如需 **GetInterfaceInfo** 函式的說明，請參閱 [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-114">For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="7e9a0-115">**使用 IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="7e9a0-115">**To use IpReleaseAddress**</span></span>

1.  <span data-ttu-id="7e9a0-116">使用 [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)函式取得 [**IP \_ 配接器 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-116">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="7e9a0-117"> (如需 GetInterfaceInfo 函式的說明，請參閱 [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-117">(For help with the GetInterfaceInfo function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="7e9a0-118">建立 **DWORD** 物件 `dwRetVal` (用於錯誤檢查) 。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-118">Create a **DWORD** object `dwRetVal` (used for error checking).</span></span> <span data-ttu-id="7e9a0-119">假設呼叫 **GetInterfaceInfo** 傳回的變數 `pInfo` 。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-119">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="7e9a0-120">如果 DHCP 已啟用，請呼叫 [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) 函式，並傳遞 [**IP \_ 介面卡 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) 變數 `Adapter` 作為其參數。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-120">If DHCP is enabled, call the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="7e9a0-121">檢查是否有一般錯誤，並將其值傳回至 **DWORD** 變數 `dwRetVal` (，以更廣泛的錯誤檢查) 。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-121">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    > [!Note]  
    > <span data-ttu-id="7e9a0-122">[**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)函式會傳回參數，可用來檢查是否在呼叫這些函式之前啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-122">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns a parameter that can be used to check whether DHCP is enabled before calling these functions.</span></span> <span data-ttu-id="7e9a0-123">如需 **GetAdaptersInfo** 的協助，請參閱 [使用 GetAdaptersInfo 管理網路介面卡](managing-network-adapters-using-getadaptersinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-123">For help with **GetAdaptersInfo**, see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> <span data-ttu-id="7e9a0-124">通常會搭配使用這兩個函式，呼叫 [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) 函式，然後呼叫 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) 函式，將相同的結構作為參數傳遞給這兩個函數。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-124">It is common to use these two functions together, calling the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function and then calling the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the same structure as the parameter to both functions.</span></span> <span data-ttu-id="7e9a0-125">下列程式假設函數未一起使用;但是，如果同時使用這些函式，請略過步驟1。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-125">The following procedure assumes that the functions are not used together; however, if the functions are used together, skip step 1.</span></span>

 

<span data-ttu-id="7e9a0-126">**使用 IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="7e9a0-126">**To use IpRenewAddress**</span></span>

1.  <span data-ttu-id="7e9a0-127">使用 [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)函式取得 [**IP \_ 配接器 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-127">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="7e9a0-128"> (如需 **GetInterfaceInfo** 函式的說明，請參閱 [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-128">(For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="7e9a0-129">宣告 **DWORD** 物件 `dwRetVal` (用於錯誤檢查) 是否未宣告此變數。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-129">Declare a **DWORD** object `dwRetVal` (used for error checking) if this variable has not been declared.</span></span> <span data-ttu-id="7e9a0-130">假設呼叫 **GetInterfaceInfo** 傳回的變數 `pInfo` 。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-130">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="7e9a0-131">呼叫 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) 函式，並傳遞 [**IP \_ 介面卡 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) 變數 `Adapter` 作為其參數。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-131">Call the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="7e9a0-132">檢查是否有一般錯誤，並將其值傳回至 **DWORD** 變數 `dwRetVal` (，以更廣泛的錯誤檢查) 。</span><span class="sxs-lookup"><span data-stu-id="7e9a0-132">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

<span data-ttu-id="7e9a0-133">下一步： [使用 AddIPAddress 和 DeleteIPAddress 管理 IP 位址](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="7e9a0-133">Next Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

<span data-ttu-id="7e9a0-134">上一個步驟： [使用 GetIpAddrTable 管理 IP 位址](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="7e9a0-134">Previous Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

 

 



