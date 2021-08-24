---
description: 根據預設，當 Windows 以安全模式執行時，不會顯示 Windows Vista 主控台專案。
title: 以保管庫模式存取主控台
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 777a44c7fe30b0481096a1c5d62c98410277a3bc76169925aff4ae5e59e549d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710788"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>以保管庫模式存取主控台

根據預設，當 Windows 以安全模式執行時，不會顯示 Windows Vista 主控台專案。 若要允許以安全模式來查看新的主控台專案，可以設定適用于專案類型的登錄值。 這些值會以下列方式解讀：



| 值 | 意義                                                            |
|-------|--------------------------------------------------------------------|
| 1     | 專案只應以最小的安全模式顯示。                  |
| 2     | 只有在已啟用網路功能的情況下，專案才會顯示在安全模式中。 |
| 3     | 專案應一律以任何形式的安全模式顯示。            |



 

這個範例會顯示實作為 .cpl 或 .dll 檔案的專案所需的專案。 它會指定專案應以具有網路功能的安全模式顯示。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

這個範例會顯示實作為 .exe 檔案的專案所需的專案。 它指定專案應以任何形式的安全模式顯示。

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[主控台專案](control-panel-applications.md)
</dt> <dt>

[使用者體驗指南](user-experience-guidelines.md)
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
</dt> </dl>

 

 



