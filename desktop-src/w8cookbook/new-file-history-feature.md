---
title: 新的檔案歷程記錄功能
description: 新的檔案歷程記錄功能
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1502450c1376a57f9de99badc5188c8ce07761e0c28ae3ac2245a84437b5e66d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932188"
---
# <a name="new-file-history-feature"></a>新的檔案歷程記錄功能

## <a name="platform"></a>平台

**用戶端**– Windows 8 


## <a name="description"></a>描述

新的檔案歷程記錄功能會取代現有的備份和還原功能，並為儲存在使用者程式庫中的使用者檔案提供保護。 提供一組 Api，可讓開發人員以程式設計方式啟用檔案歷程記錄並選取特定的儲存體目標。 您可以在 MSDN 上取得這些 Api 的檔。

這可能會影響與資料保護相關的工作流程，以及相依于 Windows 備份和還原功能的檔。

我們不建議同時使用這兩項功能。 檔案歷程記錄會檢查備份排程是否存在且是否為作用中，如果找到的話，就不會讓使用者開啟它。 在此情況下，想要使用檔案歷程記錄的使用者將必須刪除 Windows 備份排程。

## <a name="manifestation"></a>表現

工作流程可能會中斷，而先前存取 Windows 備份和還原功能的方法的檔則需要更新，以反映這些變更。

## <a name="solution"></a>解決方案

修訂應用程式，其中包含會對新的檔案歷程記錄功能造成負面影響的工作流程，以移除任何衝突並併入新的 Api 集。

## <a name="tests"></a>測試

API 可讓開發人員判斷檔案歷程記錄是否已開啟。

 

 




