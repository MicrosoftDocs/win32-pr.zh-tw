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
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>使用 AddIPAddress、DeleteIPAddress 管理 IP 位址

[**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress)函式會將指定的 IPv4 位址加入至指定的介面卡。 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)函數會從指定的介面卡刪除指定的 IPv4 位址。 這些函式可用來新增及刪除網路介面卡的 IPv4 位址。

[**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress)函數新增的 IPv4 位址不是持續性。 只有在介面卡物件存在時，IPv4 位址才會存在。 重新開機電腦會終結 IPv4 位址，就像手動重設網路介面卡 (NIC) 一樣。

成功呼叫 [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) 之後，就會針對已新增的 IP 位址停用 DHCP。 因此，需要啟用 DHCP 的函式（例如 [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)）在新增的 IP 位址上將無法運作。 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)函式可以用來刪除新增的 IPv4 位址。

> [!Note]  
> 群組原則、企業原則和網路上的其他限制可能會導致這些功能無法順利完成。 嘗試使用這些函式之前，請先確定應用程式具有必要的網路許可權。

 

**使用 AddIPAddress**

1.  宣告名為 `NTEContext` 和的 ULONG 變數 `NTEInstance` ，兩者皆初始化為零。
    > [!Note]  
    > `NTEContext`變數是 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)函式唯一的參數。若要刪除加入的 IP 位址， `NTEContext` 必須儲存且不變更。

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  分別針對名為和的 IPAddr 和 IPMask 結構宣告變數 `iaIPAddress` `iaIPMask` 。 這些值只是不帶正負號的整數。 `iaIPAddress` `iaIPMask` 使用 [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)函數初始化和變數。
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  呼叫 [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) 函數來新增 IPv4 位址。 檢查是否有錯誤，並將錯誤值傳回至 **DWORD** 變數 (，以 `dwRetVal` 更廣泛的錯誤檢查) 。
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > 第三個參數是介面卡索引，可以藉由呼叫 [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 函式取得。 假設這個函式所傳回的變數命名為 `pIPAddrTable` 。 如需 **GetIpAddrTable** 函式的說明，請參閱 [使用 GetIpAddrTable 管理 IP 位址](managing-ip-addresses-using-getipaddrtable.md)。

     

**使用 DeleteIpAddress**

-   呼叫 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) 函數，並傳遞 `NTEContext` 變數作為其參數。 檢查是否有錯誤，並將錯誤值傳回至 **DWORD** 變數 (，以 `dwRetVal` 更廣泛的錯誤檢查) 。
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> 若要使用 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)，必須先呼叫 [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) 以取得控制碼 `NTEContext` 。 先前的程式假設在程式碼中的某處已經呼叫 **AddIPAddress** ，而且已 `NTEContext` 儲存並保持未受損壞。

 

下一步： [使用 GetIpStatistics 來抓取資訊](retrieving-information-using-getipstatistics.md)

上一個步驟： [使用 IpReleaseAddress 和 IpRenewAddress 管理 DHCP 租用](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 
