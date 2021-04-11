---
description: 使用封鎖 i/o、具有網路事件非同步通知的非封鎖 i/o，以及 Windows 通訊端 2 (Winsock) 的完成指示來重迭 i/o。
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: 通訊端 i/o
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113001"
---
# <a name="socket-io"></a>通訊端 i/o

在 Windows 通訊端2中，有三種主要方式可以執行 i/o：

-   封鎖 i/o。
-   非封鎖 i/o，以及網路事件的非同步通知。
-   具有完成指示的重迭 i/o。

我們會在下列各節中描述每個方法。 封鎖 i/o 是預設行為，非封鎖模式可用於置於非封鎖模式的任何通訊端，而重迭的 i/o 只能發生在使用重迭屬性建立的通訊端上。 另外也請注意，兩個傳送的呼叫： [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) 和 [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) ，以及接收： [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) 和 [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) 的兩個呼叫都會執行所有三種 i/o 方法。 服務提供者會根據通訊端模式、屬性和輸入參數值，決定如何執行 i/o 作業。

 

 
