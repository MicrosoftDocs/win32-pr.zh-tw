---
title: Windows 7 備份和還原已淘汰
description: Windows 7 備份和還原已淘汰
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5975483797423515a4c04a35f8766de241553cb98a386bd53adcc7970977f7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211227"
---
# <a name="windows-7-backup-and-restore-deprecated"></a>Windows 7 備份和還原已淘汰

## <a name="platform"></a>平台

**用戶端**– Windows 8 


## <a name="description"></a>Description

雖然備份和還原沒有任何行為變更，但這項功能已被取代，而且將不會更新。 它很少使用，且其功能已由新的檔案歷程記錄功能取代。 它將隨附于 Windows 8，而從 Windows 7 升級到 Windows 8 或相依于備份和還原或磁片映射備份的愛好者仍能使用它。 不過，除了主控台之外，所有備份和還原的存取點都已移除。 備份和還原所使用的主控台小程式已重新命名為 Windows 7 檔復原。

設定登錄機碼以停用其映射中的備份通知的 Oem 將不再需要這麼做。

我們不建議同時使用這兩項功能。 檔案歷程記錄會檢查備份排程是否存在且是否為作用中，如果找到的話，就不會讓使用者開啟它。 在此情況下，想要使用檔案歷程記錄的使用者將必須刪除 Windows 備份排程。

## <a name="manifestation"></a>表現

工作流程可能會中斷，而參考先前存取 Windows 備份和還原功能的檔則需要更新，以反映這些變更。

## <a name="mitigation"></a>降低

應重新撰寫可能觸發備份和還原的應用程式，以檢查檔案歷程記錄是否開啟，並讓使用者選擇其慣用的方法。

 

 




