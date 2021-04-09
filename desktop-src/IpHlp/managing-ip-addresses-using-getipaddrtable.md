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
# <a name="managing-ip-addresses-using-getipaddrtable"></a>使用 GetIpAddrTable 管理 IP 位址

[**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable)函式會填入 [**MIB \_ IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable)結構的指標，其中包含與系統相關聯之目前 IP 位址的相關資訊。

**使用 GetIpAddrTable**

1.  宣告名為 *pIPAddrTable* 之 [**MIB \_ IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable)物件的指標，以及名為 *dwSize* 的 **DWORD** 物件。 這些變數會以參數形式傳遞至 [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 函數。 此外，請建立名為 *dwRetVal* (的 **DWORD** 變數，以用於錯誤檢查) 。
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  配置結構的記憶體。
    > [!Note]  
    > *DwSize* 的大小不足以容納資訊。 請參閱下一個步驟。

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  對 [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 進行初始呼叫，以取得 *dwSize* 變數所需的大小。
    > [!Note]  
    > 對函式的呼叫會失敗，並用來確保 *dwSize* 變數所指定的大小足以容納所有傳回給 *pIPAddrTable* 的資訊。 這是此類型之資料結構和函式的通用程式設計模型。

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  使用一般錯誤檢查進行 [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 的第二個呼叫，並將其值傳回至 **DWORD** 變數 *dwRetVal* (，以進行更高階的錯誤檢查) 。
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  如果呼叫成功，則存取 *pIPAddrTable* 資料結構中的資料。
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  釋放配置給 *pIPAddrTable* 結構的任何記憶體。
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> **DWORD** 物件 *dwAddr* 和 *dwMask* 會以主機位元組順序的數值傳回，而不是以網路位元組順序傳回。 這些值不是以點分隔的 IP 位址。

 

下一步： [使用 IpReleaseAddress 和 IpRenewAddress 管理 DHCP 租用](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

上一個步驟： [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)

 

 
