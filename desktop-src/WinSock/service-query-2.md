---
description: Windows 通訊端中的名稱服務查詢 (Winsock) 。
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: 服務查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5452c94c3768cbff387b0125fe183a3026f7ab6c64d90325341ce5f2a9366de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740417"
---
# <a name="service-query"></a>服務查詢

-   [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

名稱服務查詢牽涉到一連串的呼叫： [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)，後面接著一或多個 [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) 的呼叫，然後以 [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)的呼叫結尾。 [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) 會採用 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構作為輸入，以便定義查詢參數以及一組旗標，以提供對搜尋作業的額外控制。 它會傳回查詢控制碼，此控制碼用於後續呼叫 **NSPLookupServiceNext** 和 **NSPLookupServiceEnd**。

命名空間 SPI 用戶端會叫用 [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) 來取得查詢結果，並在用戶端提供的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 緩衝區中提供結果。 用戶端會繼續呼叫 **NSPLookupServiceNext** ，直到錯誤碼 \_ \_ 不會再傳回錯誤訊息 \_ ，指出已取出所有結果。 然後搜尋會透過呼叫 [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)來終止。 從另一個執行緒呼叫時， **NSPLookupServiceEnd** 函式也可以用來取消目前暫止的 **NSPLookupServiceNext** 。

在 Windows 通訊端2中，衝突的錯誤碼是針對 WSAENOMORE (10102) 所定義，而 WSA \_ E 則 \_ 不再 \_ (10110) 。 錯誤碼 WSAENOMORE 將會在未來的版本中移除，而且只有 WSA \_ E \_ 不再有 \_ 其他會保留。 命名空間提供者應該儘快切換為使用不會再使用的 \_ \_ \_ 錯誤代碼，以維持與最廣泛的應用程式之間的相容性。

 

 



