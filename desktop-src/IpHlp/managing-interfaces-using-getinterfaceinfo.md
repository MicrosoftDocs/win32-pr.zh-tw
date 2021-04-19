---
description: GetInterfaceInfo 函式會 \_ \_ 使用與系統相關聯之介面的相關資訊，填入 IP 介面資訊結構的指標。
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: 使用 GetInterfaceInfo 管理介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973044"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a><span data-ttu-id="4c563-103">使用 GetInterfaceInfo 管理介面</span><span class="sxs-lookup"><span data-stu-id="4c563-103">Managing Interfaces Using GetInterfaceInfo</span></span>

<span data-ttu-id="4c563-104">[**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)函式會使用與系統相關聯之介面的相關資訊，填入 [**IP \_ 介面 \_ 資訊**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4c563-104">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function fills a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) structure with information about the interfaces associated with the system.</span></span>

<span data-ttu-id="4c563-105">**使用 GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="4c563-105">**To use GetInterfaceInfo**</span></span>

1.  <span data-ttu-id="4c563-106">宣告名為之 [**IP \_ 介面 \_ 資訊**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) 物件的指標 `pInfo` ，以及名為的 **ULONG** 物件 `ulOutBufLen` 。</span><span class="sxs-lookup"><span data-stu-id="4c563-106">Declare a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) object called `pInfo`, and a **ULONG** object called `ulOutBufLen`.</span></span> <span data-ttu-id="4c563-107">也宣告一個稱為 `dwRetVal` (的 DWORD 物件，用於錯誤檢查) 。</span><span class="sxs-lookup"><span data-stu-id="4c563-107">Also declare a **DWORD** object called `dwRetVal` (used for error checking).</span></span>
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  <span data-ttu-id="4c563-108">配置結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4c563-108">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="4c563-109">的大小不足 `ulOutBufLen` 以容納資訊。</span><span class="sxs-lookup"><span data-stu-id="4c563-109">The size of `ulOutBufLen` is not sufficient to hold the information.</span></span> <span data-ttu-id="4c563-110">請參閱下一個步驟。</span><span class="sxs-lookup"><span data-stu-id="4c563-110">See the next step.</span></span>

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  <span data-ttu-id="4c563-111">對 [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) 進行初始呼叫，以取得變數所需的大小 `ulOutBufLen` 。</span><span class="sxs-lookup"><span data-stu-id="4c563-111">Make an initial call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) to get the size needed into the `ulOutBufLen` variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="4c563-112">對函式的呼叫會失敗，並用來確保 `ulOutBufLen` 變數所指定的大小足以容納所有傳回的資訊 `pInfo` 。</span><span class="sxs-lookup"><span data-stu-id="4c563-112">This call to the function is meant to fail, and is used to ensure that the `ulOutBufLen` variable specifies a size sufficient for holding all the information returned to `pInfo`.</span></span> <span data-ttu-id="4c563-113">這是此類型之資料結構和函式的 IP 協助程式中常見的程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="4c563-113">This is a common programming model in IP Helper for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  <span data-ttu-id="4c563-114">使用一般錯誤檢查進行 [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) 的第二個呼叫，並將其值傳回至 **DWORD** 變數 (，以 `dwRetVal` 進行更先進的錯誤檢查) 。</span><span class="sxs-lookup"><span data-stu-id="4c563-114">Make a second call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) with general error checking and return its value to the **DWORD** variable `dwRetVal` (for more advanced error checking).</span></span>
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  <span data-ttu-id="4c563-115">如果呼叫成功，請從 `pInfo` 資料結構存取資料。</span><span class="sxs-lookup"><span data-stu-id="4c563-115">If the call was successful, access the data from the `pInfo` data structure.</span></span>

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="4c563-116">第一行的% ws 表示寬字元串。</span><span class="sxs-lookup"><span data-stu-id="4c563-116">The %ws in the first line denotes a wide string.</span></span> <span data-ttu-id="4c563-117">這是因為 [**IP \_ 配接器 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map)結構的 **名稱** 屬性 `Adapter` 是 **WCHAR**，也就是 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="4c563-117">This is used because the **Name** attribute of the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure `Adapter` is a **WCHAR**, which is a Unicode string.</span></span>

     

6.  <span data-ttu-id="4c563-118">釋放配置給 *pInfo* 結構的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="4c563-118">Free any memory allocated for the *pInfo* structure.</span></span>
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

<span data-ttu-id="4c563-119">下一步： [使用 GetIpAddrTable 管理 IP 位址](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="4c563-119">Next Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

<span data-ttu-id="4c563-120">上一個步驟： [使用 GetAdaptersInfo 管理網路介面卡](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="4c563-120">Previous Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

 

 



