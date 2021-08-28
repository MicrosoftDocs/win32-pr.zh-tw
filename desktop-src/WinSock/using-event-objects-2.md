---
description: Windows通訊端事件物件是可建立和關閉、設定和清除、等候和輪詢的簡單結構。
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: '使用事件物件 (Windows 通訊端 2) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d500656279d328046e2792b47a296bc2347e3478e36c7d81a5e781023887dc51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121158"
---
# <a name="using-event-objects-windows-sockets-2"></a>使用事件物件 (Windows 通訊端 2) 

Windows通訊端事件物件是可建立和關閉、設定和清除、等候和輪詢的簡單結構。 接受的模型可讓用戶端建立事件物件，並提供控制碼做為參數 (或作為參數結構的元件，) 在 [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) 和 [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))等函式中。 當提名條件發生時，服務提供者會藉由呼叫 [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent)來使用此控制碼來設定事件物件。 同時，Winsock SPI 用戶端可能會封鎖並等候或輪詢，直到事件物件變成設定 (通知) 。 用戶端可能會接著清除或重設事件物件，並再次使用它。

 

 
