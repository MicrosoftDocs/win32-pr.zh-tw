---
description: 名稱解析函式可以分為三種類別：服務安裝、用戶端查詢和 helper (與宏) 。
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: 名稱解析函數的摘要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690376"
---
# <a name="summary-of-name-resolution-functions"></a>名稱解析函數的摘要

名稱解析函式可以分為三種類別：服務安裝、用戶端查詢和 helper (與宏) 。 接下來的各節會識別每個類別中的函式，並簡要描述其預定用途。 也會描述重要的資料結構。

## <a name="service-installation"></a>服務安裝

-   [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

當必要的服務類別不存在時，應用程式會使用 [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) 來安裝新的服務類別，方法是提供服務類別名稱、服務類別識別碼的 GUID，以及一系列的 [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) 結構。 這些結構各自適用于特定的命名空間，並提供一般值，例如建議的 TCP 埠號碼或 NetWare SAP 識別碼。 您可以藉由呼叫 [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) 並提供對應至類別識別碼的 GUID，來移除服務類別。

服務類別存在之後，就可以透過 [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)安裝或移除服務的特定實例。 此函式會採用 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構做為輸入參數，以及作業程式碼和作業旗標。 作業程式碼會指出服務是否正在安裝或移除。 **WSAQUERYSET** 結構提供服務的所有相關資訊，包括服務類別識別碼、此實例的服務名稱 () 、適用的命名空間識別碼和通訊協定資訊，以及服務接聽的一組傳輸位址。 服務應該在初始化時叫用 **WSASetService** ，以通告其在動態命名空間中的存在。

## <a name="client-query"></a>用戶端查詢

-   [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

[**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)函式可讓應用程式探索可透過 Winsock 名稱解析功能存取哪些命名空間。 它也可讓應用程式判斷是否有一個以上的命名空間提供者支援指定的命名空間，以及探索任何特定命名空間提供者的提供者識別碼。 使用提供者識別碼，應用程式可以將查詢作業限制為指定的命名空間提供者。

Winsock 命名空間–查詢作業牽涉到一連串的呼叫： [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)，後面接著一或多個 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 的呼叫，然後以 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)的呼叫結尾。 **WSALookupServiceBegin** 會採用 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構作為輸入，來定義查詢參數以及一組旗標，以提供對搜尋作業的額外控制。 它會傳回查詢控制碼，此控制碼用於後續呼叫 **WSALookupServiceNext** 和 **WSALookupServiceEnd**。

應用程式會叫用 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 來取得查詢結果，並在應用程式提供的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 緩衝區中提供結果。 應用程式會繼續呼叫 **WSALookupServiceNext** ，直到錯誤碼 \_ \_ 不會再傳回錯誤訊息 \_ ，指出已取出所有結果。 然後搜尋會透過呼叫 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)來終止。 從另一個執行緒呼叫時， **WSALookupServiceEnd** 函式也可以用來取消目前暫止的 **WSALookupServiceNext** 。

在 Windows 通訊端2中，WSAENOMORE (10102) 和 WSA \_ E \_ 不再 \_ (10110) 定義了衝突的錯誤碼。 錯誤碼 WSAENOMORE 將會在未來的版本中移除，而且只有 WSA \_ E \_ 不再有 \_ 其他會保留。 但是針對 Windows 通訊端2，應用程式應該同時檢查 WSAENOMORE 和 WSA \_ E \_ ， \_ 以找出最廣泛的可能與使用其中一個命名空間提供者的相容性。

## <a name="helper-functions"></a>輔助函式

-   [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [**WSAGetServiceClassInfo**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

名稱解析協助程式函式包含函式，可在給定服務類別識別碼的情況下，取得服務類別名稱、一組用來在 [**SOCKADDR**](sockaddr-2.md) 結構與 ASCII 字串表示之間轉譯傳輸位址的函式、用來取得指定服務類別之服務類別架構資訊的函式，以及用來將已知服務對應至預先配置 guid 的一組宏。

下列來自 Winsock2 的宏有助於在知名的服務類別與這些命名空間之間進行對應：

| 巨集                                                                                                            | Description                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| SVCID \_ TCP (埠) SVCID \_ UDP (埠) <br/> SVCID \_ NETWARE (物件類型) <br/>                              | 如果有 TCP/IP 或 UDP/IP 的通訊埠，或是 NetWare 的物件類型，則會以主機順序) 傳回 GUID (埠號碼。 |
| 是 \_ SVCID \_ TCP (GUID) 是 \_ SVCID \_ UDP (guid) <br/> 是 \_ SVCID \_ NETWARE (GUID) <br/>                          | 如果 GUID 位於允許的範圍內，則傳回 **TRUE** 。                                                                |
| 設定 \_ TCP \_ SVCID (guid，PORT) set \_ UDP \_ SVCID (guid，port) <br/>                                                | 使用與 TCP 或 UDP 埠號碼相等的 GUID 來初始化 GUID 結構， (埠號碼必須在主機順序) 中。    |
| \_從 \_ SVCID \_ TCP (GUID) 埠 \_ 從 \_ SVCID \_ UDP (guid 的埠) <br/> \_從 \_ SVCID \_ NETWARE (GUID) SAPID<br/> | 傳回與主機順序) 中的 GUID (埠號碼相關聯的埠或物件類型。                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[名稱解析資料結構](name-resolution-data-structures-2.md)
</dt> <dt>

[名稱解析模型](name-resolution-model-2.md)
</dt> <dt>

[通訊協定獨立名稱解析](protocol-independent-name-resolution-2.md)
</dt> <dt>

[註冊和名稱解析](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




