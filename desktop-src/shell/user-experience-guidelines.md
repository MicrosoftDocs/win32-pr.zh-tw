---
description: 任何主控台專案的主要責任是顯示一個視窗，讓使用者能夠查看和操作設定。
title: 使用者體驗指南
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 15ef54d44a466f3c766075eae771ccac9d74e20c0622d6092530f1015a538425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857077"
---
# <a name="user-experience-guidelines"></a>使用者體驗指南

任何主控台專案的主要責任是顯示一個視窗，讓使用者能夠查看和操作設定。 請參閱 [控制項面板使用者體驗 (UX) 指導方針](../uxguide/winenv-ctrl-panels.md) ，以瞭解主控台專案的行為與設計。 本主題所討論的指導方針會顯示組織主控台專案的工作流程方法。 這會將最重要的設定放在首頁上。 較不常使用的設定會放在輪輻頁面上，或從側邊窗格中的連結存取。

主控台包含許多遵循這些指導方針的專案，例如輕鬆存取中心和網路和共用中心。 其他主控台專案使用索引標籤式對話方塊屬性工作表格式，如同舊版的 Windows。 範例包括滑鼠專案和網際網路選項。 應停止使用屬性工作表格式。 如果您建立新的主控台專案，則應遵循工作流程指導方針。

在過去，主控台專案封裝成 .cpl 檔案。 不再需要。 新的主控台專案應實作為獨立 .exe 檔案，或作為應用程式主要可執行檔的命令列旗標選項來執行。

> [!Note]  
> 在64位系統上，當選取 **View 32-bit 主控台 items 資料夾** 選項時，主控台會顯示32位主控台專案。 32位專案必須位於要顯示的% SystemRoot% \\ SysWOW64 資料夾中。 它們不需要任何進一步的註冊。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[主控台專案](control-panel-applications.md)
</dt> <dt>

[註冊主控台專案](registering-control-panel-items.md)
</dt> <dt>

[使用 CPLApplet](using-cplapplet.md)
</dt> <dt>

[主控台訊息處理](message-processing.md)
</dt> <dt>

[執行主控台專案](executing-control-panel-items.md)
</dt> <dt>

[擴充系統主控台專案](extending-system-control-panel-items.md)
</dt> <dt>

[指派主控台分類](assigning-control-panel-categories.md)
</dt> <dt>

[建立主控台專案的可搜尋工作連結](creating-searchable-task-links.md)
</dt> <dt>

[以保管庫模式存取主控台](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



