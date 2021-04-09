---
title: 新的檔案歷程記錄功能
description: 新的檔案歷程記錄功能
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104093428"
---
# <a name="new-file-history-feature"></a>新的檔案歷程記錄功能

## <a name="platform"></a>平台

**用戶端** – Windows 8 


## <a name="description"></a>Description

新的檔案歷程記錄功能會取代現有的備份和還原功能，並為儲存在使用者程式庫中的使用者檔案提供保護。 提供一組 Api，可讓開發人員以程式設計方式啟用檔案歷程記錄並選取特定的儲存體目標。 您可以在 MSDN 上取得這些 Api 的檔。

這可能會影響與資料保護相關的工作流程，以及相依于 Windows 備份和還原功能的檔。

我們不建議同時使用這兩項功能。 檔案歷程記錄會檢查備份排程是否存在且是否為作用中，如果找到的話，就不會讓使用者開啟它。 在此情況下，想要使用檔案歷程記錄的使用者將必須刪除 Windows 備份排程。

## <a name="manifestation"></a>表現

工作流程可能會中斷，而先前存取 Windows 備份和還原功能的方法的檔則需要更新，以反映這些變更。

## <a name="solution"></a>解決方法

修訂應用程式，其中包含會對新的檔案歷程記錄功能造成負面影響的工作流程，以移除任何衝突並併入新的 Api 集。

## <a name="tests"></a>測試

API 可讓開發人員判斷檔案歷程記錄是否已開啟。

 

 




