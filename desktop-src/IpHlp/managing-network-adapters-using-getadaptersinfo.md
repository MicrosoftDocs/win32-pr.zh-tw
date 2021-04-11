---
description: GetAdaptersInfo 函式會 \_ \_ 使用與系統相關聯之網路介面卡的相關資訊，填入 IP 介面卡資訊結構的指標。
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: 使用 GetAdaptersInfo 管理網路介面卡
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470e0ce7682a86b29df912fa4d4b1297c2263382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027102"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a>使用 GetAdaptersInfo 管理網路介面卡

[**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)函式會使用與系統相關聯之網路介面卡的相關資訊，填入 [**IP \_ 介面卡 \_ 資訊**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info)結構的指標。

**使用 GetAdaptersInfo**

1.  宣告名為 *pAdapterInfo* 之 [**IP \_ 配接器 \_ 資訊**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info)變數的指標，以及名為 *ulOutBufLen* 的 **ULONG** 變數。 這些變數會以參數形式傳遞至 [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) 函數。 此外，請建立名為 *dwRetVal* (的 **DWORD** 變數，以) 檢查錯誤。
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  配置結構的記憶體。
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  對 [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) 進行初始呼叫，以取得 *ulOutBufLen* 變數所需的大小。
    > [!Note]  
    > 對函式的呼叫會失敗，並用來確保 *ulOutBufLen* 變數所指定的大小足以容納所有傳回給 *pAdapterInfo* 的資訊。 這是此類型之資料結構和函式的通用程式設計模型。

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  對 [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)進行第二次呼叫，將 *pAdapterInfo* 和 *ulOutBufLen* 做為參數傳遞，並執行一般錯誤檢查。 將其值傳回至 **DWORD** 變數 *dwRetVal* (，以) 進行更廣泛的錯誤檢查。
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  如果呼叫成功，請存取 *pAdapterInfo* 結構中的某些資料。
    ```C++
    PIP_ADAPTER_INFO pAdapter = pAdapterInfo;
    while (pAdapter) {
        printf("Adapter Name: %s\n", pAdapter->AdapterName);
        printf("Adapter Desc: %s\n", pAdapter->Description);
        printf("\tAdapter Addr: \t");
        for (UINT i = 0; i < pAdapter->AddressLength; i++) {
            if (i == (pAdapter->AddressLength - 1))
                printf("%.2X\n",(int)pAdapter->Address[i]);
            else
                printf("%.2X-",(int)pAdapter->Address[i]);
        }
        printf("IP Address: %s\n", pAdapter->IpAddressList.IpAddress.String);
        printf("IP Mask: %s\n", pAdapter->IpAddressList.IpMask.String);
        printf("\tGateway: \t%s\n", pAdapter->GatewayList.IpAddress.String);
        printf("\t***\n");
        if (pAdapter->DhcpEnabled) {
            printf("\tDHCP Enabled: Yes\n");
            printf("\t\tDHCP Server: \t%s\n", pAdapter->DhcpServer.IpAddress.String);
        }
        else
          printf("\tDHCP Enabled: No\n");

      pAdapter = pAdapter->Next;
    }
    
    ```

    

6.  釋放配置給 *pAdapterInfo* 結構的任何記憶體。
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

下一步： [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)

上一個步驟： [使用 GetNetworkParams 來抓取資訊](retrieving-information-using-getnetworkparams.md)

 

 



