---
description: Windows 通訊端中的名稱解析資料結構 (Winsock) 。
ms.assetid: 87c54141-41e2-4eaa-ae3b-84598e8281d9
title: 名稱解析資料結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e6f3b889d295241bb0cdb9c0182babf0c5b8115e7eff7e86c27b65c992c452
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794788"
---
# <a name="name-resolution-data-structures"></a>名稱解析資料結構

在名稱解析函式中，有數個重要的資料結構廣泛使用。

## <a name="query-related-data-structures"></a>Query-Related 資料結構

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構是用來形成 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)的查詢，用來傳遞 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)的查詢結果。 這是複雜的結構，因為它包含多個其他結構的指標，其中有些參考仍是其他結構。 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構與其參考結構之間的關聯性如下所示。

![wsaqueryset 與其相關結構之間的關聯性](images/ovrvw3-2.png)

在 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構內，大部分的成員都是一目了然的，但有一些額外的說明。 **DwSize** 成員必須一律填入 Sizeof (**WSAQUERYSET**) ，因為這是由命名空間提供者用來偵測及調整可能會在一段時間內出現的不同 **WSAQUERYSET** 結構版本。

命名空間提供者會使用 **dwOutputFlags** 成員來提供查詢結果的其他相關資訊。 如需詳細資訊，請參閱 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) 函數。

**Lpversion** 成員所參考的 [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)結構會用於查詢準則約束和結果。 若為查詢， **dwVersion** 成員會指出所需的服務版本。 **EcHow** 成員是列舉型別，可指定如何進行比較。 選項為 [複合 \_ EQUALS]，其需要在版本中進行完全相符，或 \_ 指定服務的版本號碼不小於 **dwVersion** 成員的值。

**DwNameSpace** 和 **lpNSProviderId** 的解讀取決於結構的使用方式，並在使用此結構的個別函式描述中進一步說明。

**LpszCoNtext** 成員會套用至階層命名空間，並指定查詢的起點或服務所在階層中的位置。 一般規則如下：

-   值為 **Null**、空白 ( "" ) 在預設內容中開始搜尋。
-   "" 的值會 \\ 在命名空間的頂端開始搜尋。
-   任何其他值都會在指定的點開始搜尋。

如果指定了 "" 或 "" 以外的任何專案，則不支援內含專案的提供者可能會傳回錯誤 \\ 。 支援有限內含專案的提供者（例如群組）應接受 ""，' \\ "或指定的點。 內容是特定命名空間。 如果 **dwNameSpace** 成員是 NS \_ ALL，則只應將 "" 或 " \\ " 傳遞為內容，因為所有命名空間都能辨識這些成員。

**LpszQueryString** 成員是用來提供其他命名空間特定的查詢資訊，例如描述已知服務和傳輸通訊協定名稱的字串，例如 "FTP/TCP"。

**LpafpProtocols** 成員所參考的 [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)結構只用于查詢用途，並提供用來限制查詢的通訊協定清單。 這些通訊協定會以 (位址系列、通訊協定) 組表示，因為通訊協定值只有在位址系列的內容中才有意義。

**LpcsaBuffer** 成員所參考之 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構的陣列，包含服務在建立接聽時所需的所有資訊，或是用於建立服務連接的用戶端所需的所有資訊。 **LocalAddr** 和 **RemoteAddr** 成員都直接包含 [**通訊端 \_ 位址**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)結構。

服務會藉由使用 LocalAddr 的元組（ *lpSockaddr->sa \_ 系列*、 *iSocketType* 和 *iProtocol* 作為參數）呼叫 [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)或 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)函式來建立通訊端。 服務會將通訊端系結至本機位址，方法是使用 *LocalAddr. lpSockaddr* 和 *LocalAddr* 做為參數來呼叫 [**bind**](/windows/desktop/api/winsock/nf-winsock-bind)函式。

用戶端會使用 LocalAddr 的元組（ *lpSockaddr->sa \_ 系列*、 *iSocketType* 和 *iProtocol* 作為參數）來呼叫 [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)或 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)函式，以建立其通訊端。 當使用 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)、 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)或 [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)函數進行遠端連線時，用戶端會使用 *RemoteAddr. lpSockaddr* 和 *RemoteAddr* 的組合作為參數。

## <a name="service-class-data-structures"></a>服務類別資料結構

安裝新的服務類別時，必須備妥和提供 [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) 結構。 此結構也包含包含一系列適用于特定命名空間之成員的子結構。 類別資訊資料結構如下所示：

![服務類別資料結構架構](images/ovrvw3-3.png)

每個服務類別都有一個 [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) 結構。 在 [**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow) 結構內，服務類別的唯一識別碼會包含在 **lpServiceClassId** 成員中，而 **lpServiceClassName** 成員會參考相關聯的顯示字串。 這是 [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) 函數所傳回的字串。

[**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)結構中的 **lpClassInfos** 成員會參考 **WSANSCLASSINFO** 結構的陣列，其中每個結構都會提供套用至指定命名空間的命名和具類型成員。 **LpszName** 成員的值範例包括： "SapId"、"TcpPort"、"UdpPort" 等。這些字串通常是針對 **dwNameSpace** 成員中識別的命名空間所特有。 **DwValueType** 成員的一般值可能是 reg \_ DWORD、reg \_ SZ 等等。**DwValueSize** 成員會指出 **lpValue** 所指向之資料項目的長度。

叫用 [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)函式時，會為每個命名空間提供者提供 **WSASERVICECLASSINFO** 結構中所表示的整個資料集合。 接著，每個個別的命名空間提供者會 sifts **WSANSCLASSINFO** 結構的清單，並保留適用的資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)
</dt> <dt>

[**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[名稱解析模型](name-resolution-model-2.md)
</dt> <dt>

[通訊協定獨立名稱解析](protocol-independent-name-resolution-2.md)
</dt> <dt>

[註冊和名稱解析](registration-and-name-resolution-2.md)
</dt> <dt>

[**通訊端 \_ 位址**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)
</dt> <dt>

[名稱解析函數的摘要](summary-of-name-resolution-functions-2.md)
</dt> <dt>

[**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASERVICECLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsaserviceclassinfow)
</dt> </dl>

 

 
