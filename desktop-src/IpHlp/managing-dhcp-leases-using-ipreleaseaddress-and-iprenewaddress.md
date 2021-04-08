---
title: 使用 IpReleaseAddress、IpRenewAddress 管理 DHCP 租用
description: IpReleaseAddress 和 IpRenewAddress 函式可用來釋出並更新目前的動態主機設定通訊協定 (DHCP) 租用。
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847951"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a>使用 IpReleaseAddress、IpRenewAddress 管理 DHCP 租用

[**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)和 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress)函式可用來釋出並更新目前的動態主機設定通訊協定 (DHCP) 租用。 **IpReleaseAddress** 函式會釋放先前透過 DHCP 取得的 IPv4 位址。 **IpRenewAddress** 函式會在先前透過 DHCP 取得的 IPv4 位址上更新租用。 通常會搭配使用這兩個函式，先使用 **IpReleaseAddress** 呼叫來釋出租用，然後透過呼叫 **IpRenewAddress** 函式來更新租用。

如果 DHCP 用戶端先前已取得 DHCP 租用，而 [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) 未在 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) 功能之前呼叫，則會將 dhcp 用戶端要求傳送到發出初始 DHCP 租用的 dhcp 伺服器。 此 DHCP 伺服器可能無法使用，或 DHCP 要求可能會失敗。 當主機先前取得 DHCP 租用，且 **IpReleaseAddress** 在 **IpRenewAddress** 函式之前呼叫，DHCP 用戶端會先釋出所取得的 IP 位址，並從任何可用的 dhcp 伺服器傳送回應的 dhcp 用戶端要求。

> [!Note]  
> [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)和 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress)函式需要啟用 DHCP 才能正確執行。

 

[**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)函式會接受 [**IP \_ 介面卡 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map)結構的指標作為唯一的參數。 若要取得此參數，請先呼叫 [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)。 如需 **GetInterfaceInfo** 函式的說明，請參閱 [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)。

**使用 IpReleaseAddress**

1.  使用 [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)函式取得 [**IP \_ 配接器 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map)結構的指標。  (如需 GetInterfaceInfo 函式的說明，請參閱 [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)) 。 建立 **DWORD** 物件 `dwRetVal` (用於錯誤檢查) 。 假設呼叫 **GetInterfaceInfo** 傳回的變數 `pInfo` 。
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  如果 DHCP 已啟用，請呼叫 [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) 函式，並傳遞 [**IP \_ 介面卡 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) 變數 `Adapter` 作為其參數。 檢查是否有一般錯誤，並將其值傳回至 **DWORD** 變數 `dwRetVal` (，以更廣泛的錯誤檢查) 。
    > [!Note]  
    > [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)函式會傳回參數，可用來檢查是否在呼叫這些函式之前啟用 DHCP。 如需 **GetAdaptersInfo** 的協助，請參閱 [使用 GetAdaptersInfo 管理網路介面卡](managing-network-adapters-using-getadaptersinfo.md)。

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> 通常會搭配使用這兩個函式，呼叫 [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) 函式，然後呼叫 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) 函式，將相同的結構作為參數傳遞給這兩個函數。 下列程式假設函數未一起使用;但是，如果同時使用這些函式，請略過步驟1。

 

**使用 IpRenewAddress**

1.  使用 [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)函式取得 [**IP \_ 配接器 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map)結構的指標。  (如需 **GetInterfaceInfo** 函式的說明，請參閱 [使用 GetInterfaceInfo 管理介面](managing-interfaces-using-getinterfaceinfo.md)) 。 宣告 **DWORD** 物件 `dwRetVal` (用於錯誤檢查) 是否未宣告此變數。 假設呼叫 **GetInterfaceInfo** 傳回的變數 `pInfo` 。
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  呼叫 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) 函式，並傳遞 [**IP \_ 介面卡 \_ 索引 \_ 對應**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) 變數 `Adapter` 作為其參數。 檢查是否有一般錯誤，並將其值傳回至 **DWORD** 變數 `dwRetVal` (，以更廣泛的錯誤檢查) 。
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

下一步： [使用 AddIPAddress 和 DeleteIPAddress 管理 IP 位址](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

上一個步驟： [使用 GetIpAddrTable 管理 IP 位址](managing-ip-addresses-using-getipaddrtable.md)

 

 



