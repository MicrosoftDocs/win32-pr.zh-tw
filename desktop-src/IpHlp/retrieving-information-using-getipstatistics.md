---
description: GetIpStatistics 函式會填入 MIB IPSTATS 結構的指標， \_ 其中包含與系統相關聯之目前 IP 統計資料的相關資訊。
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: 使用 GetIpStatistics 抓取資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6267c3939548c8f8ea9ab2705ea1769360748e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979199"
---
# <a name="retrieving-information-using-getipstatistics"></a><span data-ttu-id="3fd16-103">使用 GetIpStatistics 抓取資訊</span><span class="sxs-lookup"><span data-stu-id="3fd16-103">Retrieving Information Using GetIpStatistics</span></span>

<span data-ttu-id="3fd16-104">[**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics)函式會填入 [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh)結構的指標，其中包含與系統相關聯之目前 IP 統計資料的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3fd16-104">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function fills a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure with information about the current IP statistics associated with the system.</span></span>

<span data-ttu-id="3fd16-105">**使用 GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="3fd16-105">**To use GetIpStatistics**</span></span>

1.  <span data-ttu-id="3fd16-106">宣告一些需要的變數。</span><span class="sxs-lookup"><span data-stu-id="3fd16-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="3fd16-107">宣告 `dwRetval` 將用於錯誤檢查函式呼叫的 DWORD 變數。</span><span class="sxs-lookup"><span data-stu-id="3fd16-107">Declare a **DWORD** variable `dwRetval` that will be using for error checking function calls.</span></span> <span data-ttu-id="3fd16-108">宣告名為 *pStats* 之 [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh)變數的指標，並為結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="3fd16-108">Declare a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) variable called *pStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="3fd16-109">檢查是否可以配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="3fd16-109">Check that memory could be allocated.</span></span>

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  <span data-ttu-id="3fd16-110">使用 *pStats* 參數呼叫 [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics)函數，以取出本機電腦的 IP 統計資料。</span><span class="sxs-lookup"><span data-stu-id="3fd16-110">Call the [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function with the *pStats* parameter to retrieve IP statistics for the local computer.</span></span> <span data-ttu-id="3fd16-111">檢查是否有錯誤，並傳回 **DWORD** 變數中的錯誤值 `dwRetval` 。</span><span class="sxs-lookup"><span data-stu-id="3fd16-111">Check for errors and return the error value in the **DWORD** variable `dwRetval`.</span></span> <span data-ttu-id="3fd16-112">如果發生錯誤， `dwRetval` 變數可以用於更廣泛的錯誤檢查和報告。</span><span class="sxs-lookup"><span data-stu-id="3fd16-112">If an error occurs, the `dwRetval` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  <span data-ttu-id="3fd16-113">如果 [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics)的呼叫成功，請將 *pStats* 參數所指向的 [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh)結構中的某些資料列印出來。</span><span class="sxs-lookup"><span data-stu-id="3fd16-113">If the call to [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) was successful, print out some of the data in the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span>
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  <span data-ttu-id="3fd16-114">釋放配置給 *pStats* 參數所指向之 [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh)結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3fd16-114">Free the memory allocated for the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span> <span data-ttu-id="3fd16-115">只要應用程式不再需要 *pStats* 參數所傳回的資料，就應該這麼做。</span><span class="sxs-lookup"><span data-stu-id="3fd16-115">This should be done once the application no longer needs the data returned by the *pStats* parameter.</span></span>
    ```C++
    if (pStats)
        free(pStats);
    ```

    

<span data-ttu-id="3fd16-116">下一步： [使用 GetTcpStatistics 來抓取資訊](retrieving-information-using-gettcpstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="3fd16-116">Next Step: [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span></span>

<span data-ttu-id="3fd16-117">上一個步驟： [使用 AddIPAddress 和 DeleteIPAddress 管理 IP 位址](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="3fd16-117">Previous Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

 

 
