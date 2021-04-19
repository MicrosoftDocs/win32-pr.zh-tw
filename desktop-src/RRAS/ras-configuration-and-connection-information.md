---
title: RAS 設定和連接資訊
description: 在 Windows NT 4.0 和更新版本以及 Windows 95 上執行的應用程式，可以使用 RasEnumConnections 函式來取得本機電腦上現有連接的相關資訊。
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- 設定和連線，RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966796"
---
# <a name="ras-configuration-and-connection-information"></a>RAS 設定和連接資訊

在 Windows NT 4.0 和更新版本以及 Windows 95 上執行的應用程式，可以使用 [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) 函式來取得本機電腦上現有連接的相關資訊。 每個連線的資訊包含連接控制碼，以及用來建立連線的電話簿專案名稱。 您可以在 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 函數的呼叫中使用連接控制碼取得連接的目前狀態。

Windows NT Server 4.0 和更新版本提供兩個新功能，可供您用來抓取 RAS 資訊。 Windows 95does 不支援這些功能。

[**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa)函式會傳回在本機電腦上設定且支援 RAS 之裝置的名稱和類型。

[**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa)函式會指定事件物件，系統會在建立或終止 RAS 連接時發出通知。

 

 




