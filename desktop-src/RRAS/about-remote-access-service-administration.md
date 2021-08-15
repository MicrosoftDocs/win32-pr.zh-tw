---
title: 關於遠端存取服務管理
description: Windows 2000 和更新版本的作業系統提供一組功能，可在 RAS 伺服器上管理使用者權限和埠。
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- 路由及遠端存取服務 RRAS、RAS 管理
- 路由及遠端存取服務 RRAS、RAS 管理、描述
- RAS 系統管理 RRAS
- RAS 管理 RRAS，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67939d142763f45bc2eb52e959d8448904559c98357544c6c858b46e8f87a917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792281"
---
# <a name="about-remote-access-service-administration"></a>關於遠端存取服務管理

Windows 2000 和更新版本的作業系統提供一組功能，可在 RAS 伺服器上管理使用者權限和埠。 您可以使用這些功能來開發 RAS 伺服器管理應用程式，以執行下列工作：

-   列舉擁有一組指定 RAS 許可權的使用者
-   指派或撤銷指定使用者的 RAS 許可權
-   列舉 RAS 伺服器上設定的埠
-   取得 RAS 伺服器上指定埠的相關資訊和統計資料
-   重設指定埠的統計資料計數器
-   中斷指定埠的連接

您也可以安裝 RAS 伺服器管理 DLL 來審核使用者連線，並將 IP 位址指派給撥入使用者。 當使用者嘗試連線或中斷連線時，DLL 會匯出一組 RAS 伺服器所呼叫的函數。

本檔將說明下列主題：

-   [函數比較： Windows 2000 與 RRAS 可轉散發套件](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [RAS 使用者管理](ras-user-administration.md)
-   [RAS 伺服器和埠管理](ras-server-and-port-administration.md)
-   [RAS 系統管理 DLL](ras-administration-dll.md)
-   [RAS 管理 DLL 登錄設定](ras-administration-dll-registry-setup.md)

 

 




