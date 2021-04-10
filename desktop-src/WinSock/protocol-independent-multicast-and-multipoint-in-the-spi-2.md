---
description: Windows 通訊端 (Winsock) 和通訊協定獨立的 multipoint 和多播功能。
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: 在 SPI 中 Protocol-Independent 多播和 Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115060"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a>在 SPI 中 Protocol-Independent 多播和 Multipoint

就像 Windows 通訊端2允許以一般方式存取許多傳輸通訊協定的基本資料傳輸功能一樣，它也提供了一般的方式來使用可執行這些功能之傳輸的 multipoint 和多播功能。 為了簡化，此處會使用 *multipoint* 這一詞來參考多播和 multipoint 通訊。

目前的 multipoint 執行 (例如，IP 多播、ST-II、T. 120、ATM 單向) 在節點加入 multipoint 會話的方式有很大的差異，不論特定節點是否指定為中央或根節點，以及資料是否要在所有節點之間交換，或只在根節點與不同分葉節點之間進行交換。 Windows 通訊端 2 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構是用來宣告通訊協定的 multipoint 屬性。 藉由檢查這些屬性，程式設計人員將知道使用適用的 Winsock 函式來設定、使用和卸載 multipoint 會話時應遵循的慣例。

支援多播的 Windows 通訊端2功能可摘要如下：

-   [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構中有三個屬性位。
-   針對 [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)的 *dwFlags* 參數定義的四個旗標
-   一個函式 [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)，用於將分葉節點新增至 multipoint 會話。
-   用於控制 multipoint 回送和建立多播傳輸範圍的兩個 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) 命令代碼。  (後者對應至 IP 多播的存留時間或 TTL 參數。 ) 

> [!Note]  
> 在 Windows 通訊端2中包含這些 multipoint 功能，並不會妨礙服務提供者也支援現有的通訊協定相依介面，例如 IP 多播的 Deering 通訊端選項。

 

 

 
