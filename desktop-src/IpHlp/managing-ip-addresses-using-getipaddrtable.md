---
description: GetIpAddrTable 函式會填入 MIB IPADDRTABLE 結構的指標， \_ 其中包含與系統相關聯之目前 IP 位址的相關資訊。
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: 使用 GetIpAddrTable 管理 IP 位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3d94eb4de22a428e20a4cb0fdc8970d7f65fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849169"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a><span data-ttu-id="8b81f-103">使用 GetIpAddrTable 管理 IP 位址</span><span class="sxs-lookup"><span data-stu-id="8b81f-103">Managing IP Addresses Using GetIpAddrTable</span></span>

<span data-ttu-id="8b81f-104">[**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable)函式會填入 [**MIB \_ IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable)結構的指標，其中包含與系統相關聯之目前 IP 位址的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8b81f-104">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function fills a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) structure with information about the current IP addresses associated with the system.</span></span>

<span data-ttu-id="8b81f-105">**使用 GetIpAddrTable**</span><span class="sxs-lookup"><span data-stu-id="8b81f-105">**To use GetIpAddrTable**</span></span>

1.  <span data-ttu-id="8b81f-106">宣告名為 *pIPAddrTable* 之 [**MIB \_ IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable)物件的指標，以及名為 *dwSize* 的 **DWORD** 物件。</span><span class="sxs-lookup"><span data-stu-id="8b81f-106">Declare a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) object called *pIPAddrTable*, and a **DWORD** object called *dwSize*.</span></span> <span data-ttu-id="8b81f-107">這些變數會以參數形式傳遞至 [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 函數。</span><span class="sxs-lookup"><span data-stu-id="8b81f-107">These variables are passed as parameters to the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="8b81f-108">此外，請建立名為 *dwRetVal* (的 **DWORD** 變數，以用於錯誤檢查) 。</span><span class="sxs-lookup"><span data-stu-id="8b81f-108">Also create a **DWORD** variable called *dwRetVal* (used for error checking).</span></span>
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="8b81f-109">配置結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8b81f-109">Allocate memory for the structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="8b81f-110">*DwSize* 的大小不足以容納資訊。</span><span class="sxs-lookup"><span data-stu-id="8b81f-110">The size of *dwSize* is not sufficient to hold the information.</span></span> <span data-ttu-id="8b81f-111">請參閱下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="8b81f-111">See the next step.</span></span>

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  <span data-ttu-id="8b81f-112">對 [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 進行初始呼叫，以取得 *dwSize* 變數所需的大小。</span><span class="sxs-lookup"><span data-stu-id="8b81f-112">Make an initial call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) to get the size needed into the *dwSize* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="8b81f-113">對函式的呼叫會失敗，並用來確保 *dwSize* 變數所指定的大小足以容納所有傳回給 *pIPAddrTable* 的資訊。</span><span class="sxs-lookup"><span data-stu-id="8b81f-113">This call to the function is meant to fail, and is used to ensure that the *dwSize* variable specifies a size sufficient for holding all the information returned to *pIPAddrTable*.</span></span> <span data-ttu-id="8b81f-114">這是此類型之資料結構和函式的通用程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="8b81f-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  <span data-ttu-id="8b81f-115">使用一般錯誤檢查進行 [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 的第二個呼叫，並將其值傳回至 **DWORD** 變數 *dwRetVal* (，以進行更高階的錯誤檢查) 。</span><span class="sxs-lookup"><span data-stu-id="8b81f-115">Make a second call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) with general error checking and return its value to the **DWORD** variable *dwRetVal* (for more advanced error checking).</span></span>
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  <span data-ttu-id="8b81f-116">如果呼叫成功，則存取 *pIPAddrTable* 資料結構中的資料。</span><span class="sxs-lookup"><span data-stu-id="8b81f-116">If the call was successful, access the data from the *pIPAddrTable* data structure.</span></span>
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  <span data-ttu-id="8b81f-117">釋放配置給 *pIPAddrTable* 結構的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="8b81f-117">Free any memory allocated for the *pIPAddrTable* structure.</span></span>
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> <span data-ttu-id="8b81f-118">**DWORD** 物件 *dwAddr* 和 *dwMask* 會以主機位元組順序的數值傳回，而不是以網路位元組順序傳回。</span><span class="sxs-lookup"><span data-stu-id="8b81f-118">The **DWORD** objects *dwAddr* and *dwMask* are returned as numerical values in host byte order, not network byte order.</span></span> <span data-ttu-id="8b81f-119">這些值不是以點分隔的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8b81f-119">These values are not dotted IP addresses.</span></span>

 

<span data-ttu-id="8b81f-120">下一步： [使用 IpReleaseAddress 和 IpRenewAddress 管理 DHCP 租用](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="8b81f-120">Next Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

<span data-ttu-id="8b81f-121">上一個步驟： [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="8b81f-121">Previous Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

 

 
