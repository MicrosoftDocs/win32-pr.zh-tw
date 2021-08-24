---
title: RAS 設定和連接資訊
description: 在 Windows NT 4.0 和更新版本上執行的應用程式，以及 Windows 95，都可以使用 RasEnumConnections 函式來取得本機電腦上現有連接的相關資訊。
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- 設定和連線，RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af528af93318247b7f88a50dc1db240670d17bcc48e11a7d683bfccd9054d671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673428"
---
# <a name="ras-configuration-and-connection-information"></a>RAS 設定和連接資訊

在 Windows NT 4.0 和更新版本上執行的應用程式，以及 Windows 95，都可以使用 [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa)函式來取得本機電腦上現有連接的相關資訊。 每個連線的資訊包含連接控制碼，以及用來建立連線的電話簿專案名稱。 您可以在 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 函數的呼叫中使用連接控制碼取得連接的目前狀態。

Windows NT伺服器4.0 和更新版本提供兩個新功能，可供您用來抓取 RAS 資訊。 Windows 95does 不支援這些功能。

[**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa)函式會傳回在本機電腦上設定且支援 RAS 之裝置的名稱和類型。

[**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa)函式會指定事件物件，系統會在建立或終止 RAS 連接時發出通知。

 

 




