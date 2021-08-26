---
description: GetIpStatistics 函式會填入 MIB IPSTATS 結構的指標， \_ 其中包含與系統相關聯之目前 IP 統計資料的相關資訊。
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: 使用 GetIpStatistics 抓取資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c383c49b316eb48e240a8272957dae8ee3ec1671304df8d466b869b7bf4ec0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050268"
---
# <a name="retrieving-information-using-getipstatistics"></a>使用 GetIpStatistics 抓取資訊

[**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics)函式會填入 [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh)結構的指標，其中包含與系統相關聯之目前 IP 統計資料的相關資訊。

**使用 GetIpStatistics**

1.  宣告一些需要的變數。

    宣告 `dwRetval` 將用於錯誤檢查函式呼叫的 DWORD 變數。 宣告名為 *pStats* 之 [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh)變數的指標，並為結構配置記憶體。 檢查是否可以配置記憶體。

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  使用 *pStats* 參數呼叫 [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics)函數，以取出本機電腦的 IP 統計資料。 檢查是否有錯誤，並傳回 **DWORD** 變數中的錯誤值 `dwRetval` 。 如果發生錯誤， `dwRetval` 變數可以用於更廣泛的錯誤檢查和報告。
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  如果 [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics)的呼叫成功，請將 *pStats* 參數所指向的 [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh)結構中的某些資料列印出來。
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  釋放配置給 *pStats* 參數所指向之 [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh)結構的記憶體。 只要應用程式不再需要 *pStats* 參數所傳回的資料，就應該這麼做。
    ```C++
    if (pStats)
        free(pStats);
    ```

    

下一步： [使用 GetTcpStatistics 來抓取資訊](retrieving-information-using-gettcpstatistics.md)

上一個步驟： [使用 AddIPAddress 和 DeleteIPAddress 管理 IP 位址](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

 

 
