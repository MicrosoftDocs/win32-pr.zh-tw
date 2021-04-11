---
description: 下列 VSS 錯誤和狀態資訊會寫入至應用程式事件記錄檔：
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: VSS 錯誤記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113181"
---
# <a name="vss-error-logging"></a>VSS 錯誤記錄

下列 VSS 錯誤和狀態資訊會寫入至應用程式事件記錄檔：

-   使用 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 介面產生的要求者錯誤
-   使用 [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) 類別產生的寫入器錯誤，包括覆寫方法
-   預設提供者產生的錯誤
-   協調提供者、寫入器和要求者活動所產生的 VSS 服務錯誤 (例如產生事件) 

這些錯誤可能有許多原因，包括協力廠商程式碼的程式設計錯誤或與 VSS 相關的設定錯誤。

VSS 驅動程式和較低層級的執行功能會將錯誤寫入系統記錄檔。 協力廠商軟體 (要求者、提供者、寫入器) 可以選擇應用程式記錄檔、系統記錄檔或兩者來寫入錯誤記錄檔專案。

建議高階應用程式 (例如使用者模式程式碼) 使用應用程式記錄檔。 較低層級的應用程式（例如硬體介面和驅動程式）應該使用系統記錄。

 

 



