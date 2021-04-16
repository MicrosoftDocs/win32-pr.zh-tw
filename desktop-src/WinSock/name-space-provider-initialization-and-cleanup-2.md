---
description: 在 Windows 通訊端中使用 NSPStartup 和 NSPCleanup 進行命名空間提供者初始化和清除 (Winsock) SPI。
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: 命名空間提供者初始化和清除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fedd7b40d79e755262df581c92e1fe3bdbfb06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511420"
---
# <a name="namespace-provider-initialization-and-cleanup"></a>命名空間提供者初始化和清除

-   [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

就像傳輸 SPI 的情況一樣，命名空間提供者會透過呼叫 [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) 來初始化，並在最後一次呼叫 [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)時終止。 啟動函式的呼叫可能會進行嵌套，但會透過對應的清除函數呼叫來比對。 提供者應該採用參考計數，以判斷何時發生 **NSPCleanup** 的最後呼叫。

 

 



