---
description: WSAQUERYSET 結構是用來形成 NSPLookupServiceBegin 函數的查詢，並用來傳遞 NSPLookupServiceNext 函數的查詢結果。
ms.assetid: 017b5828-bc6e-42b7-aba7-21648b2dd707
title: SPI 中的 Query-Related 資料結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ce5a7016bd2ad96f464137177036b470c64a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555024"
---
# <a name="query-related-data-structures-in-the-spi"></a>SPI 中的 Query-Related 資料結構

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構是用來形成 [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)的查詢，用來傳遞 [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)的查詢結果。 這是複雜的結構，因為它包含多個其他結構的指標，其中有些參考仍是其他結構。 **WSAQUERYSET** 與它所參考之結構之間的關聯性如下所示：

![wsaqueryset 結構](images/ovrvw3-2.png)

在 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構內，大部分的成員都是一目了然的，但有一些額外的說明。 **DwSize** 將會填入 Sizeof ( **WSAQUERYSET**) ，並且可供命名空間提供者用來偵測及調整可能出現的不同 **WSAQUERYSET** 結構版本。

命名空間提供者會使用 **dwOutputFlags** 成員來提供查詢結果的其他相關資料。 如需詳細資訊，請參閱 [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)。

**Lpversion** 所參考的 [**WSAECOMPARATOR**](/windows/desktop/api/Winsock2/ne-winsock2-wsaecomparator)結構會用於查詢準則約束和結果。 若為查詢， **dwVersion** 成員會指出所需的服務版本。 **EcHow** 成員是列舉型別，會指定如何進行比較。 選項為 [複合 \_ EQUALS]，其需要在版本中進行完全相符，或 \_ 指定服務的版本號碼不小於 **dwVersion** 的值的 [複合] NOTLESS。

**DwNameSpace** 和 **lpNSProviderId** 的解讀取決於結構的使用方式，並在使用此結構的個別函式描述中進一步說明。

**LpszCoNtext** 成員會套用至階層命名空間，並指定查詢的起點或服務所在階層中的位置。 一般規則如下：

-   值為 **Null**、空白 ( "" ) 將在預設內容中開始搜尋。
-   "" 的值會 \\ 在命名空間的頂端開始搜尋。
-   任何其他值都會在指定的點開始搜尋。

如果指定了 "" 或 "" 以外的任何專案，則不支援內含專案的提供者可能會傳回錯誤 \\ 。 支援有限內含專案的提供者（例如群組）應接受 ""，' \\ "或指定的點。 內容是特定命名空間。 如果 **dwNameSpace** 為 NS \_ ALL，則只應將 "" 或 " \\ " 傳遞為內容，因為所有命名空間都能辨識這些內容。

**LpszQueryString** 成員是用來提供其他命名空間特定的查詢資訊，例如描述已知服務和傳輸通訊協定名稱的字串，例如 "ftp/tcp"。

**LpafpProtocols** 所參考的 [**AFPROTOCOLS**](/windows/desktop/api/Winsock2/ns-winsock2-afprotocols)結構僅用於查詢用途，並提供用來限制查詢的通訊協定清單。 這些通訊協定會以 (位址系列、通訊協定) 組表示，因為通訊協定值只有在位址系列的內容中才有意義。

**LpcsaBuffer** 所參考之 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構的陣列，包含服務在建立接聽時所需的所有資訊，或是用來建立服務連接的用戶端。 **LocalAddr** 和 **RemoteAddr** 成員都直接包含 [**通訊端 \_ 位址**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address)結構。 服務會使用元組 (LocalAddr lpSockaddr >sa \_ 系列、iSocketType、iProtocol) 來建立通訊端。 它會使用 LocalAddr lpSockaddr 和 LocalAddr，將通訊端系結至本機位址。 用戶端會使用元組 (RemoteAddr lpSockaddr >sa \_ 系列、iSocketType、iProtocol) 建立其通訊端，並在建立遠端連線時使用 RemoteAddr. lpSockaddr 和 RemoteAddr 的組合。

 

 
