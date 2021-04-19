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
# <a name="retrieving-information-using-gettcpstatistics"></a>使用 GetTcpStatistics 抓取資訊

[**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)函式會填入 [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh)結構的指標，其中包含本機電腦的 TCP 通訊協定統計資料資訊。

**使用 GetTcpStatistics**

1.  宣告一些需要的變數。

    宣告 `dwRetVal` 將用於錯誤檢查函式呼叫的 DWORD 變數。 宣告名為 *pTCPStats* 之 [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh)變數的指標，並為結構配置記憶體。 檢查是否可以配置記憶體。

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  使用 *pTCPStats* 參數呼叫 [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)函式，以在本機電腦上取得 IPv4 的 TCP 統計資料。 檢查是否有錯誤，並傳回 **DWORD** 變數中的錯誤值 `dwRetVal` 。 如果發生錯誤， `dwRetVal` 變數可以用於更廣泛的錯誤檢查和報告。
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  如果呼叫成功，請存取 *pTCPStats* 參數所指向之 [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh)中傳回的資料。
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  釋放配置給 *pTCPStats* 參數所指向之 [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh)結構的記憶體。 只要應用程式不再需要 *pTCPStats* 參數所傳回的資料，就應該這麼做。
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

下一步： [使用 GetIpStatistics 來抓取資訊](retrieving-information-using-getipstatistics.md)

上一個步驟： [使用 GetIpStatistics 來抓取資訊](retrieving-information-using-getipstatistics.md)

## <a name="complete-source-code"></a>完整的原始程式碼

-   [完整 IP 協助程式的原始程式碼](complete-ip-helper-application-source-code.md)

 

 
