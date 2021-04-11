---
description: 隨附檔案的安裝狀態不會相依于自己的檔案版本設定資訊，而是在其附屬父系的版本控制上。
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: 隨附檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944765"
---
# <a name="companion-files"></a>隨附檔案

隨附檔案的安裝狀態不會相依于自己的檔案版本設定資訊，而是在其附屬父系的版本控制上。 請參閱檔案 [版本控制規則](file-versioning-rules.md)。 若要指定附屬檔案，必須將檔案 [資料表](file-table.md) 中附屬父系的主鍵撰寫到附屬記錄的 [版本] 欄中。

在下列範例中，>filea.docx 是隨附的父系，而 >fileb.docx 則是隨附的檔案。

[檔資料表](file-table.md) (部分) 



| 檔案  | 版本 |
|-------|---------|
| >filea.docx | 1.0.0.0 |
| >fileb.docx | >filea.docx   |



 

在此範例中，>fileb.docx 的安裝狀態取決於檔案 [版本控制規則](file-versioning-rules.md) 和 >filea.docx 的版本設定資訊。 如果安裝程式判斷套件中的 >filea.docx 版本應該安裝在使用者電腦上已存在的舊版 >filea.docx 上，它也會從套件安裝 >fileb.docx，不論任何已安裝的 >fileb.docx 版本為何。

請注意，檔案是其元件的金鑰路徑，不能是附屬檔案。 這會導致金鑰路徑檔案的版本控制邏輯由隨附的父檔案所決定。

 

 



