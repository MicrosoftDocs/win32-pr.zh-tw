---
title: RAS 伺服器管理
description: Windows NT伺服器4.0 提供一組功能，可用來管理 Windows NT/Windows 2000 RAS 伺服器上的使用者權限和埠。
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- 伺服器管理，RAS
- 管理，RAS 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6760e8cc06e5c7b389d01f690497dc070974cada5e9a922ec5576e48b2a328fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789187"
---
# <a name="ras-server-administration"></a>RAS 伺服器管理

Windows NT伺服器4.0 提供一組功能，可用來管理 Windows NT/Windows 2000 RAS 伺服器上的使用者權限和埠。 Windows 95 不支援這些功能。 您可以使用這些功能來開發 RAS 伺服器管理應用程式，以執行下列工作：

-   列舉擁有一組指定 RAS 許可權的使用者
-   指派或撤銷指定使用者的 RAS 許可權
-   列舉 RAS 伺服器上設定的埠
-   取得 RAS 伺服器上指定埠的相關資訊和統計資料
-   重設指定埠的統計資料計數器
-   中斷指定埠的連接

您也可以安裝 RAS 伺服器管理 DLL 來審核使用者連線，以及將 IP 位址指派給撥入使用者。 當使用者嘗試連線或中斷連線時，DLL 會匯出一組 RAS 伺服器所呼叫的函數。

 

 




