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
# <a name="managing-network-adapters-using-getadaptersinfo"></a><span data-ttu-id="c2234-103">使用 GetAdaptersInfo 管理網路介面卡</span><span class="sxs-lookup"><span data-stu-id="c2234-103">Managing Network Adapters Using GetAdaptersInfo</span></span>

<span data-ttu-id="c2234-104">[**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)函式會使用與系統相關聯之網路介面卡的相關資訊，填入 [**IP \_ 介面卡 \_ 資訊**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c2234-104">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function fills a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structure with information about the network adapters associated with the system.</span></span>

<span data-ttu-id="c2234-105">**使用 GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="c2234-105">**To use GetAdaptersInfo**</span></span>

1.  <span data-ttu-id="c2234-106">宣告名為 *pAdapterInfo* 之 [**IP \_ 配接器 \_ 資訊**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info)變數的指標，以及名為 *ulOutBufLen* 的 **ULONG** 變數。</span><span class="sxs-lookup"><span data-stu-id="c2234-106">Declare a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) variable called *pAdapterInfo*, and a **ULONG** variable called *ulOutBufLen*.</span></span> <span data-ttu-id="c2234-107">這些變數會以參數形式傳遞至 [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="c2234-107">These variables are passed as parameters to the [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function.</span></span> <span data-ttu-id="c2234-108">此外，請建立名為 *dwRetVal* (的 **DWORD** 變數，以) 檢查錯誤。</span><span class="sxs-lookup"><span data-stu-id="c2234-108">Also create a **DWORD** variable called *dwRetVal* (for error checking).</span></span>
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="c2234-109">配置結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="c2234-109">Allocate memory for the structures.</span></span>
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  <span data-ttu-id="c2234-110">對 [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) 進行初始呼叫，以取得 *ulOutBufLen* 變數所需的大小。</span><span class="sxs-lookup"><span data-stu-id="c2234-110">Make an initial call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) to get the size needed into the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="c2234-111">對函式的呼叫會失敗，並用來確保 *ulOutBufLen* 變數所指定的大小足以容納所有傳回給 *pAdapterInfo* 的資訊。</span><span class="sxs-lookup"><span data-stu-id="c2234-111">This call to the function is meant to fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the information returned to *pAdapterInfo*.</span></span> <span data-ttu-id="c2234-112">這是此類型之資料結構和函式的通用程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="c2234-112">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  <span data-ttu-id="c2234-113">對 [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)進行第二次呼叫，將 *pAdapterInfo* 和 *ulOutBufLen* 做為參數傳遞，並執行一般錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="c2234-113">Make a second call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passing *pAdapterInfo* and *ulOutBufLen* as parameters and doing general error checking.</span></span> <span data-ttu-id="c2234-114">將其值傳回至 **DWORD** 變數 *dwRetVal* (，以) 進行更廣泛的錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="c2234-114">Return its value to the **DWORD** variable *dwRetVal* (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  <span data-ttu-id="c2234-115">如果呼叫成功，請存取 *pAdapterInfo* 結構中的某些資料。</span><span class="sxs-lookup"><span data-stu-id="c2234-115">If the call was successful, access some of the data in the *pAdapterInfo* structure.</span></span>
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

    

6.  <span data-ttu-id="c2234-116">釋放配置給 *pAdapterInfo* 結構的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="c2234-116">Free any memory allocated for the *pAdapterInfo* structure.</span></span>
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

<span data-ttu-id="c2234-117">下一步： [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="c2234-117">Next Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

<span data-ttu-id="c2234-118">上一個步驟： [使用 GetNetworkParams 來抓取資訊](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="c2234-118">Previous Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 



