---
description: Ws2 \_32.dll 會使用標準的 Microsoft Windows 動態連結程式庫載入機制，將服務提供者的介面 DLL 載入系統中，並藉由呼叫 WSPStartup 將它初始化。
ms.assetid: 6df28d93-8757-45b3-8f05-86381c3be64e
title: 初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d6ef10db421ef15f2bb94eb67e96fc2cfc5924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973844"
---
# <a name="initialization"></a>初始化

*Ws2 \_32.dll* 會使用標準的 Microsoft Windows 動態連結程式庫載入機制，將服務提供者的介面 DLL 載入系統中，並藉由呼叫 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)將它初始化。 這通常是由呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 或 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) 的應用程式所觸發，以建立新的通訊端，以與目前未將其介面 DLL 載入記憶體中的服務提供者產生關聯。 安裝服務提供者時， *Ws2 \_32.dll* 會儲存每個服務提供者介面 DLL 的路徑。 如需詳細資訊，請參閱 [安裝和設定功能](installation-and-configuration-functions-2.md) 。

在一段時間內，Winsock Dll、應用程式和服務提供者可能會有不同的版本。 新版本可能會定義新的功能，以及資料結構和位參數等的新參數。因此，版本號碼會指出如何解讀不同的資料結構。

為了讓不同版本的應用程式、版本的 Ws232.dll 本身以及不同廠商的服務提供者版本達到最佳混合和比對， \_ SPI 提供了在 *Ws2 \_32.dll* 與服務提供者之間使用的版本協商機制。 此版本的協商是由 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)處理。 基本上， *Ws2 \_32.dll* 會將其相容的最高版本號碼傳遞給服務提供者。 服務提供者會將它與本身支援的版本號碼範圍進行比較。 如果這些範圍重迭，服務提供者會傳回範圍中重迭部分的值，做為協商的結果。 通常，這應該是最大的可能值。 如果範圍不重迭，則這兩個合作物件不相容，且函數會傳回錯誤。

每個用戶端進程至少必須呼叫一次 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) ，並可透過 Ws2 \_32.dll 或其他實體多次呼叫。 必須針對每個成功的 **WSPStartup** 呼叫呼叫相符的 [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) 。 服務提供者應該以每個進程為基礎來維護參考計數。 在每個 **WSPStartup** 呼叫上，呼叫端都可以指定 SP DLL 所支援的任何版本號碼。

服務提供者必須將指標儲存至用戶端的 upcall 分派資料表（以每個進程為基礎，以 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) 參數形式接收）。 如果指定的進程多次呼叫 **WSPStartup** ，服務提供者必須只使用最近提供的分派資料表指標。

在服務提供者初始化過程中，Ws2 \_32.dll 會透過 *lpProcTable* 參數抓取服務提供者的分派資料表，以取得本檔中所指定之其餘 SPI 函式的進入點。

使用分派資料表 (，而不是一般用來存取進入點的 DLL 機制) 有兩個用途：

-   Ws232.dll 比較方便，因為您 \_ 可以進行單一呼叫，以探索整組進入點。
-   它可讓形成通訊協定鏈的多層式服務提供者更有效率地運作。

## <a name="initializing-protocol-chains"></a>正在初始化通訊協定鏈

在安裝通訊協定鏈的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構時，也會指定鏈中第一個分層提供者的路徑。 當通訊協定鏈初始化時，Ws2 \_32.dll 會使用這個路徑來載入提供者 DLL，然後叫用 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)。 由於 **WSPStartup** 包含鏈的 **WSAPROTOCOL \_ 資訊** 結構的指標作為其參數之一，因此多層提供者可以決定要將其初始化的鏈類型，以及鏈中下一個較低層的識別。 然後，多層提供者會接著載入鏈中的下一個通訊協定提供者，並使用 **WSPStartup** 呼叫來初始化它。 每當下一個較低的層級為另一個分層提供者時， **WSPStartup** 呼叫中就必須參考鏈的 **WSAPROTOCOL \_ 資訊** 結構。 當下一個較低的圖層是基底通訊協定 (表示鏈) 的結尾時，就不會再向下傳播鏈的 **WSAPROTOCOL \_ 資訊** 結構。 相反地，目前的圖層必須參考對應于基底提供者應使用之通訊協定的 **WSAPROTOCOL \_ 資訊** 結構。 因此，基底提供者沒有與通訊協定鏈相關的概念。

任何給定分層提供者所提供的分派資料表，在許多情況下都會複製基礎提供者的進入點。 多層提供者只會針對需要直接參與的函式插入自己的進入點。 不過，請注意，多層提供者必須在通訊協定鏈中的下一個較低層呼叫 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) 時，不修改所收到的 upcall 資料表內容。 這些 upcalls 必須直接對 Windows 通訊端 2 DLL 進行。

 

 
