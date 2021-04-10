---
description: 每個合併模組都需要元件資料表。
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: 撰寫合併模組元件資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026643"
---
# <a name="authoring-merge-module-component-tables"></a>撰寫合併模組元件資料表

每個合併模組都需要 [元件資料表](component-table.md) 。 此資料表包含合併模組傳遞至目標 .msi 檔案的每個元件記錄。 請注意，這些元件中的每一個都必須在[撰寫 ModuleComponents 資料表](authoring-modulecomponents-tables.md)中所述的[ModuleComponents 資料表](modulecomponents-table.md)中指定。

在元件資料行中輸入名稱時，請使用標準命名慣例，以確保每個元件的識別碼在所有合併模組和安裝資料庫中都是唯一的。 如需詳細資訊，請參閱 [命名合併模組資料庫中的主鍵](naming-primary-keys-in-merge-module-databases.md)。

依 [元件表格](component-table.md)中的安裝資料庫所述，完成每筆記錄中剩餘的欄位。 合併模組新增至封裝的元件必須遵循下列各節中所述之有效 Windows Installer 元件的指導方針：

-   [Windows Installer 元件](windows-installer-components.md)
-   [將應用程式組織成元件](organizing-applications-into-components.md)

 

 



