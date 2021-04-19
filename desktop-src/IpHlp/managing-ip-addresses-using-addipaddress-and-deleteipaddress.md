---
title: 使用 AddIPAddress、DeleteIPAddress 管理 IP 位址
description: AddIPAddress 函式會將指定的 IPv4 位址加入至指定的介面卡。
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982409"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a><span data-ttu-id="43cbc-103">使用 AddIPAddress、DeleteIPAddress 管理 IP 位址</span><span class="sxs-lookup"><span data-stu-id="43cbc-103">Manage IP addresses with AddIPAddress, DeleteIPAddress</span></span>

<span data-ttu-id="43cbc-104">[**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress)函式會將指定的 IPv4 位址加入至指定的介面卡。</span><span class="sxs-lookup"><span data-stu-id="43cbc-104">The [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function adds the specified IPv4 address to the specified adapter.</span></span> <span data-ttu-id="43cbc-105">[**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)函數會從指定的介面卡刪除指定的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="43cbc-105">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function deletes the specified IPv4 address from the specified adapter.</span></span> <span data-ttu-id="43cbc-106">這些函式可用來新增及刪除網路介面卡的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="43cbc-106">These functions can be used to add and delete IPv4 addresses to a network adapter.</span></span>

<span data-ttu-id="43cbc-107">[**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress)函數新增的 IPv4 位址不是持續性。</span><span class="sxs-lookup"><span data-stu-id="43cbc-107">An IPv4 address added by the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function is not persistent.</span></span> <span data-ttu-id="43cbc-108">只有在介面卡物件存在時，IPv4 位址才會存在。</span><span class="sxs-lookup"><span data-stu-id="43cbc-108">The IPv4 address exists only as long as the adapter object exists.</span></span> <span data-ttu-id="43cbc-109">重新開機電腦會終結 IPv4 位址，就像手動重設網路介面卡 (NIC) 一樣。</span><span class="sxs-lookup"><span data-stu-id="43cbc-109">Restarting the computer destroys the IPv4 address, as does manually resetting the network interface card (NIC).</span></span>

<span data-ttu-id="43cbc-110">成功呼叫 [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) 之後，就會針對已新增的 IP 位址停用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="43cbc-110">After [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) has been called successfully, DHCP will be disabled for the IP address that was added.</span></span> <span data-ttu-id="43cbc-111">因此，需要啟用 DHCP 的函式（例如 [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)）在新增的 IP 位址上將無法運作。</span><span class="sxs-lookup"><span data-stu-id="43cbc-111">Therefore, functions such as [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), which require DHCP to be enabled, will not be functional on the added IP address.</span></span> <span data-ttu-id="43cbc-112">[**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)函式可以用來刪除新增的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="43cbc-112">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function can be used to delete the added IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="43cbc-113">群組原則、企業原則和網路上的其他限制可能會導致這些功能無法順利完成。</span><span class="sxs-lookup"><span data-stu-id="43cbc-113">Group policies, enterprise policies, and other restrictions on the network may prevent these functions from completing successfully.</span></span> <span data-ttu-id="43cbc-114">嘗試使用這些函式之前，請先確定應用程式具有必要的網路許可權。</span><span class="sxs-lookup"><span data-stu-id="43cbc-114">Ensure that the application has the necessary network permissions before attempting to use these functions.</span></span>

 

<span data-ttu-id="43cbc-115">**使用 AddIPAddress**</span><span class="sxs-lookup"><span data-stu-id="43cbc-115">**To use AddIPAddress**</span></span>

1.  <span data-ttu-id="43cbc-116">宣告名為 `NTEContext` 和的 ULONG 變數 `NTEInstance` ，兩者皆初始化為零。</span><span class="sxs-lookup"><span data-stu-id="43cbc-116">Declare **ULONG** variables named `NTEContext` and `NTEInstance`, both initialized to zero.</span></span>
    > [!Note]  
    > <span data-ttu-id="43cbc-117">`NTEContext`變數是 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)函式唯一的參數。若要刪除加入的 IP 位址， `NTEContext` 必須儲存且不變更。</span><span class="sxs-lookup"><span data-stu-id="43cbc-117">The `NTEContext` variable is the only parameter to the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function; to delete the IP address that is added, `NTEContext` must be stored and unchanged.</span></span>

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  <span data-ttu-id="43cbc-118">分別針對名為和的 IPAddr 和 IPMask 結構宣告變數 `iaIPAddress` `iaIPMask` 。</span><span class="sxs-lookup"><span data-stu-id="43cbc-118">Declare variables for the IPAddr and IPMask structures named `iaIPAddress` and `iaIPMask`, respectively.</span></span> <span data-ttu-id="43cbc-119">這些值只是不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="43cbc-119">These values are simply unsigned integers.</span></span> <span data-ttu-id="43cbc-120">`iaIPAddress` `iaIPMask` 使用 [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)函數初始化和變數。</span><span class="sxs-lookup"><span data-stu-id="43cbc-120">Initialize the `iaIPAddress` and `iaIPMask` variables using the [**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) function.</span></span>
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  <span data-ttu-id="43cbc-121">呼叫 [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) 函數來新增 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="43cbc-121">Call the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add the IPv4 address.</span></span> <span data-ttu-id="43cbc-122">檢查是否有錯誤，並將錯誤值傳回至 **DWORD** 變數 (，以 `dwRetVal` 更廣泛的錯誤檢查) 。</span><span class="sxs-lookup"><span data-stu-id="43cbc-122">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > <span data-ttu-id="43cbc-123">第三個參數是介面卡索引，可以藉由呼叫 [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 函式取得。</span><span class="sxs-lookup"><span data-stu-id="43cbc-123">The third parameter is the adapter index, which can be obtained by calling the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="43cbc-124">假設這個函式所傳回的變數命名為 `pIPAddrTable` 。</span><span class="sxs-lookup"><span data-stu-id="43cbc-124">It is assumed that the variable returned by this function is named `pIPAddrTable`.</span></span> <span data-ttu-id="43cbc-125">如需 **GetIpAddrTable** 函式的說明，請參閱 [使用 GetIpAddrTable 管理 IP 位址](managing-ip-addresses-using-getipaddrtable.md)。</span><span class="sxs-lookup"><span data-stu-id="43cbc-125">For help with the **GetIpAddrTable** function, see [Managing IP Address Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

     

<span data-ttu-id="43cbc-126">**使用 DeleteIpAddress**</span><span class="sxs-lookup"><span data-stu-id="43cbc-126">**To use DeleteIpAddress**</span></span>

-   <span data-ttu-id="43cbc-127">呼叫 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) 函數，並傳遞 `NTEContext` 變數作為其參數。</span><span class="sxs-lookup"><span data-stu-id="43cbc-127">Call the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function, passing the `NTEContext` variable as its parameter.</span></span> <span data-ttu-id="43cbc-128">檢查是否有錯誤，並將錯誤值傳回至 **DWORD** 變數 (，以 `dwRetVal` 更廣泛的錯誤檢查) 。</span><span class="sxs-lookup"><span data-stu-id="43cbc-128">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> <span data-ttu-id="43cbc-129">若要使用 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)，必須先呼叫 [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) 以取得控制碼 `NTEContext` 。</span><span class="sxs-lookup"><span data-stu-id="43cbc-129">To use [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) must first be called to get the handle `NTEContext`.</span></span> <span data-ttu-id="43cbc-130">先前的程式假設在程式碼中的某處已經呼叫 **AddIPAddress** ，而且已 `NTEContext` 儲存並保持未受損壞。</span><span class="sxs-lookup"><span data-stu-id="43cbc-130">The previous procedure assumes that **AddIPAddress** has already been called somewhere in the code, and `NTEContext` has been saved and remains uncorrupted.</span></span>

 

<span data-ttu-id="43cbc-131">下一步： [使用 GetIpStatistics 來抓取資訊](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="43cbc-131">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="43cbc-132">上一個步驟： [使用 IpReleaseAddress 和 IpRenewAddress 管理 DHCP 租用](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="43cbc-132">Previous Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

 

 
