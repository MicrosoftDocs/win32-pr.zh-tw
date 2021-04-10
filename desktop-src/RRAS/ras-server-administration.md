---
title: RAS 伺服器管理
description: Windows NT Server 4.0 提供一組功能，可在 Windows NT/Windows 2000 RAS 伺服器上管理使用者權限和埠。
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- 伺服器管理，RAS
- 管理，RAS 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183955"
---
# <a name="ras-server-administration"></a>RAS 伺服器管理

Windows NT Server 4.0 提供一組功能，可在 Windows NT/Windows 2000 RAS 伺服器上管理使用者權限和埠。 Windows 95 不支援這些功能。 您可以使用這些功能來開發 RAS 伺服器管理應用程式，以執行下列工作：

-   列舉擁有一組指定 RAS 許可權的使用者
-   指派或撤銷指定使用者的 RAS 許可權
-   列舉 RAS 伺服器上設定的埠
-   取得 RAS 伺服器上指定埠的相關資訊和統計資料
-   重設指定埠的統計資料計數器
-   中斷指定埠的連接

您也可以安裝 RAS 伺服器管理 DLL 來審核使用者連線，以及將 IP 位址指派給撥入使用者。 當使用者嘗試連線或中斷連線時，DLL 會匯出一組 RAS 伺服器所呼叫的函數。

 

 




