---
description: GetTcpStatistics 函式會填入 MIB TCPSTATS 結構的指標， \_ 其中包含本機電腦的 TCP 通訊協定統計資料資訊。
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: 使用 GetTcpStatistics 抓取資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f4d4d42c2716d258ff72e3dd91ab750baaed20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974488"
---
# <a name="retrieving-information-using-gettcpstatistics"></a><span data-ttu-id="56f93-103">使用 GetTcpStatistics 抓取資訊</span><span class="sxs-lookup"><span data-stu-id="56f93-103">Retrieving Information Using GetTcpStatistics</span></span>

<span data-ttu-id="56f93-104">[**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)函式會填入 [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh)結構的指標，其中包含本機電腦的 TCP 通訊協定統計資料資訊。</span><span class="sxs-lookup"><span data-stu-id="56f93-104">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function fills a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure with information on the TCP protocol statistics for the local computer.</span></span>

<span data-ttu-id="56f93-105">**使用 GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="56f93-105">**To use GetTcpStatistics**</span></span>

1.  <span data-ttu-id="56f93-106">宣告一些需要的變數。</span><span class="sxs-lookup"><span data-stu-id="56f93-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="56f93-107">宣告 `dwRetVal` 將用於錯誤檢查函式呼叫的 DWORD 變數。</span><span class="sxs-lookup"><span data-stu-id="56f93-107">Declare a **DWORD** variable `dwRetVal` that will be using for error checking function calls.</span></span> <span data-ttu-id="56f93-108">宣告名為 *pTCPStats* 之 [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh)變數的指標，並為結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="56f93-108">Declare a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) variable called *pTCPStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="56f93-109">檢查是否可以配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="56f93-109">Check that memory could be allocated.</span></span>

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  <span data-ttu-id="56f93-110">使用 *pTCPStats* 參數呼叫 [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)函式，以在本機電腦上取得 IPv4 的 TCP 統計資料。</span><span class="sxs-lookup"><span data-stu-id="56f93-110">Call the [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function with the *pTCPStats* parameter to retrieve TCP statistics for IPv4 on the local computer.</span></span> <span data-ttu-id="56f93-111">檢查是否有錯誤，並傳回 **DWORD** 變數中的錯誤值 `dwRetVal` 。</span><span class="sxs-lookup"><span data-stu-id="56f93-111">Check for errors and return the error value in the **DWORD** variable `dwRetVal`.</span></span> <span data-ttu-id="56f93-112">如果發生錯誤， `dwRetVal` 變數可以用於更廣泛的錯誤檢查和報告。</span><span class="sxs-lookup"><span data-stu-id="56f93-112">If an error occurs, the `dwRetVal` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  <span data-ttu-id="56f93-113">如果呼叫成功，請存取 *pTCPStats* 參數所指向之 [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh)中傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="56f93-113">If the call was successful, access the data returned in the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) pointed to by the *pTCPStats* parameter.</span></span>
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  <span data-ttu-id="56f93-114">釋放配置給 *pTCPStats* 參數所指向之 [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh)結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="56f93-114">Free the memory allocated for the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure pointed to by the *pTCPStats* parameter.</span></span> <span data-ttu-id="56f93-115">只要應用程式不再需要 *pTCPStats* 參數所傳回的資料，就應該這麼做。</span><span class="sxs-lookup"><span data-stu-id="56f93-115">This should be done once the application no longer needs the data returned by the *pTCPStats* parameter.</span></span>
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

<span data-ttu-id="56f93-116">下一步： [使用 GetIpStatistics 來抓取資訊](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="56f93-116">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="56f93-117">上一個步驟： [使用 GetIpStatistics 來抓取資訊](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="56f93-117">Previous Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

## <a name="complete-source-code"></a><span data-ttu-id="56f93-118">完整的原始程式碼</span><span class="sxs-lookup"><span data-stu-id="56f93-118">Complete Source Code</span></span>

-   [<span data-ttu-id="56f93-119">完整 IP 協助程式的原始程式碼</span><span class="sxs-lookup"><span data-stu-id="56f93-119">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

 

 
