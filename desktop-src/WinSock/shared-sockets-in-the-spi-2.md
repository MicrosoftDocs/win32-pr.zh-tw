---
description: Windows 通訊端中的通訊端共用 (Winsock) 。
ms.assetid: dad31820-6f60-4c3b-9cdf-e301a5ffce48
title: SPI 中的共用通訊端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0992768a7f3b38f27e4d40c54673e63e855687d0e9b9162e8b9e3cd1d1711d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559696"
---
# <a name="shared-sockets-in-the-spi"></a>SPI 中的共用通訊端

Windows 通訊端中進程之間的通訊端共用會依照下列方式執行。 來源進程會呼叫 [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) 來取得特殊的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構。 它會使用一些處理序間通訊 (IPC) 機制，將此結構的內容傳遞至目標進程。 然後，目標進程會在 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)的呼叫中使用 **WSAPROTOCOL \_ 資訊** 結構。 這個函式所傳回的通訊端描述項會是基礎通訊端的額外通訊端描述元，因此會變成共用。

服務提供者必須負責執行來源進程內容中所需的任何作業，以及建立 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構，當它之後顯示為參數，以在目標進程的內容中 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) 時，將會加以辨識。 **WSAPROTOCOL \_ 資訊** 結構的 **dwProviderReserved** 成員適用于服務提供者的使用，可用來儲存任何有用的內容資訊，包括重複的控制碼。

這項機制的設計目的是要適用于 Windows 的單一執行緒和搶先式多執行緒版本。 不過請注意，在指定進程中的執行緒之間可共用該通訊端，而不使用 [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) 函式，因為通訊端描述項在所有進程的執行緒中都是有效的。

如同區段描述項配置中所述，當新的通訊端描述項 [配置](descriptor-allocation-2.md)時，IFS 提供者必須呼叫 [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) ，而非 IFS 提供者必須呼叫 [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle)。

下表說明在切換模式下建立和使用共用通訊端的一個可能案例。

| 來源程序                                                                                                                          | IPC    | 目的地進程                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)、 [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) 要求目標處理序識別碼。                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) 接收處理常式識別碼要求和回應。                          |
| 4) 接收處理常式識別碼。                                                                                                         | <== |                                                                               |
| 5) 呼叫 [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) 來取得特殊的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構。 |        |                                                                               |
| 6) 將 **WSAPROTOCOL \_ 資訊** 結構傳送至目標。                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) 接收 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構。        |
|                                                                                                                                         |        | 8) 會呼叫 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) 來建立共用通訊端描述項。 |
|                                                                                                                                         |        | 9) 使用共用通訊端進行資料交換。                                       |
| 10) [ **WSPClosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
