---
description: Windows 通訊端傳輸和命名空間&\# 8211; 服務提供者是 dll，分別具有服務提供者初始化函數 WSPStartup 或 NSPStartup 的單一匯出程式進入點。
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: 函數介面模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972217"
---
# <a name="function-interface-model"></a>函數介面模型

Windows 通訊端傳輸和命名空間-服務提供者是具有單一匯出程式進入點的 Dll，分別適用于服務提供者初始化函數 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) 或 [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)。 Ws2 \_32.dll 可透過服務提供者的分派資料表存取所有其他服務提供者函數。 只有在需要時，Ws232.dll 會將服務提供者 DLL 載入記憶體中，並在不再需要服務提供者 DLL \_ 時將其卸載。

SPI 也會定義傳輸服務提供者呼叫 Ws2 \_32.dll (upcalls) 以取得 DLL 支援服務的幾種情況。 \_透過 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)的 *UpcallTable* 參數，提供 Ws232.dll 的 upcall 分派資料表給傳輸服務提供者 DLL。

服務提供者的副檔名必須從 "DLL" 變更為 "。WSP 「或」。NSP」。 這項需求不是嚴格的。 服務提供者仍會使用具有任何副檔名的 Ws232.dll 來操作 \_ 。

Winsock SPI 會使用下列函數首碼命名慣例：

| 前置詞 | 意義                          | Description                                       |
|--------|----------------------------------|---------------------------------------------------|
| WSP    | Windows 通訊端服務提供者 | 傳輸服務提供者進入點           |
| WPU    | Windows 通訊端提供者 Upcall  | \_服務提供者的 Ws232.dll 進入點    |
| WSC    | Windows 通訊端設定    | WS2 \_ 安裝 applet 的32.dll 進入點 |
| Nsp    | 命名空間提供者               | 命名空間提供者進入點                   |



 

如上所述，這些進入點不會匯出 (除了 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) 和 [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)) 之外，還可以透過 exchange 分派資料表來存取。

 

 



