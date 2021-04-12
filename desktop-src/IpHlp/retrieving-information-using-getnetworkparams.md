---
description: '\_使用目前網路設定的相關資料，填滿固定資訊結構的指標。'
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: 使用 GetNetworkParams 抓取資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20aed9b1ffa761ec53637d4d5b165e3fd2c2673d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193128"
---
# <a name="retrieving-information-using-getnetworkparams"></a><span data-ttu-id="9d565-103">使用 GetNetworkParams 抓取資訊</span><span class="sxs-lookup"><span data-stu-id="9d565-103">Retrieving Information Using GetNetworkParams</span></span>

<span data-ttu-id="9d565-104">[**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams)函式會使用目前網路設定的相關資料，填滿 [**固定 \_ 資訊**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9d565-104">The [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function fills a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) structure with data about the current network settings.</span></span>

<span data-ttu-id="9d565-105">**使用 GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="9d565-105">**To use GetNetworkParams**</span></span>

1.  <span data-ttu-id="9d565-106">宣告名為 *pFixedInfo* 的 [**固定 \_ 資訊**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1)物件指標，以及名為 *ulOutBufLen* 的 **ULONG** 物件。</span><span class="sxs-lookup"><span data-stu-id="9d565-106">Declare a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) object called *pFixedInfo*, and a **ULONG** object called *ulOutBufLen*.</span></span> <span data-ttu-id="9d565-107">這些變數會以參數形式傳遞至 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 函數。</span><span class="sxs-lookup"><span data-stu-id="9d565-107">These variables are passed as parameters to the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="9d565-108">此外，也請建立 **DWORD** 變數 *dwRetVal* (用於錯誤檢查) 。</span><span class="sxs-lookup"><span data-stu-id="9d565-108">Also create a **DWORD** variable *dwRetVal* (used for error checking).</span></span>
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  <span data-ttu-id="9d565-109">配置結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9d565-109">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="9d565-110">*UlOutBufLen* 的大小不足以容納資訊。</span><span class="sxs-lookup"><span data-stu-id="9d565-110">The size of *ulOutBufLen* is not sufficient to hold the information.</span></span> <span data-ttu-id="9d565-111">請參閱下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="9d565-111">See the next step.</span></span>

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  <span data-ttu-id="9d565-112">對 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 進行初始呼叫，以取得 *ulOutBufLen* 變數所需的大小。</span><span class="sxs-lookup"><span data-stu-id="9d565-112">Make an initial call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) to get the size required for the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="9d565-113">此函數函式將會失敗，並會用來確保 *ulOutBufLen* 變數所指定的大小足以容納所有傳回給 *pFixedInfo* 的資料。</span><span class="sxs-lookup"><span data-stu-id="9d565-113">This function function will fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the data returned to *pFixedInfo*.</span></span> <span data-ttu-id="9d565-114">這是此類型之資料結構和函式的通用程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="9d565-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  <span data-ttu-id="9d565-115">使用一般錯誤檢查對 [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) 進行第二次呼叫，並將其值傳回至 **DWORD** 變數 *dwRetVal*;用於更先進的錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="9d565-115">Make a second call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) using general error checking and returning its value to the **DWORD** variable *dwRetVal*; used for more advanced error checking.</span></span>
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  <span data-ttu-id="9d565-116">如果呼叫成功，則存取 *pFixedInfo* 資料結構中的資料。</span><span class="sxs-lookup"><span data-stu-id="9d565-116">If the call was successful, access the data from the *pFixedInfo* data structure.</span></span>
    ```C++
            printf("\tHost Name: %s\n", pFixedInfo->HostName);
            printf("\tDomain Name: %s\n", pFixedInfo->DomainName);
            printf("\tDNS Servers:\n");
            printf("\t\t%s\n", pFixedInfo->DnsServerList.IpAddress.String);

            pIPAddr = pFixedInfo->DnsServerList.Next;
            while (pIPAddr) {
                printf("\t\t%s\n", pIPAddr->IpAddress.String);
                pIPAddr = pIPAddr->Next;
            }

            printf("\tNode Type: ");
            switch (pFixedInfo->NodeType) {
            case 1:
                printf("%s\n", "Broadcast");
                break;
            case 2:
                printf("%s\n", "Peer to peer");
                break;
            case 4:
                printf("%s\n", "Mixed");
                break;
            case 8:
                printf("%s\n", "Hybrid");
                break;
            default:
                printf("\n");
            }

            printf("\tNetBIOS Scope ID: %s\n", pFixedInfo->ScopeId);

            if (pFixedInfo->EnableRouting)
                printf("\tIP Routing Enabled: Yes\n");
            else
                printf("\tIP Routing Enabled: No\n");

            if (pFixedInfo->EnableProxy)
                printf("\tWINS Proxy Enabled: Yes\n");
            else
                printf("\tWINS Proxy Enabled: No\n");

            if (pFixedInfo->EnableDns)
                printf("\tNetBIOS Resolution Uses DNS: Yes\n");
            else
                printf("\tNetBIOS Resolution Uses DNS: No\n");
    ```

    

6.  <span data-ttu-id="9d565-117">釋放配置給 *pFixedInfo* 結構的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="9d565-117">Free any memory allocated for the *pFixedInfo* structure.</span></span>
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

<span data-ttu-id="9d565-118">下一步： [使用 GetAdaptersInfo 管理網路介面卡](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="9d565-118">Next Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

<span data-ttu-id="9d565-119">上一個步驟： [建立基本 IP 協助程式應用程式](creating-a-basic-ip-helper-application.md)</span><span class="sxs-lookup"><span data-stu-id="9d565-119">Previous Step: [Creating a Basic IP Helper Application](creating-a-basic-ip-helper-application.md)</span></span>

 

 



