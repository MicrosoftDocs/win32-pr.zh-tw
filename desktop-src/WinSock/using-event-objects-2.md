---
description: Windows 通訊端事件物件是可建立和關閉、設定和清除、等候和輪詢的簡單結構。
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: '使用事件物件 (Windows 通訊端 2) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973841"
---
# <a name="using-event-objects-windows-sockets-2"></a>使用事件物件 (Windows 通訊端 2) 

Windows 通訊端事件物件是可建立和關閉、設定和清除、等候和輪詢的簡單結構。 接受的模型可讓用戶端建立事件物件，並提供控制碼做為參數 (或作為參數結構的元件，) 在 [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) 和 [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))等函式中。 當提名條件發生時，服務提供者會藉由呼叫 [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent)來使用此控制碼來設定事件物件。 同時，Winsock SPI 用戶端可能會封鎖並等候或輪詢，直到事件物件變成設定 (通知) 。 用戶端可能會接著清除或重設事件物件，並再次使用它。

 

 
