---
description: 主控台專案必須註冊，才能出現在 [主控台] 視窗中。
title: 註冊主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: daa86bfd9975df5cd057dd3e577f443bafa6c363061e267e67adad69b590e678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661078"
---
# <a name="registering-control-panel-items"></a>註冊主控台專案

主控台專案必須註冊，才能出現在 [主控台] 視窗中。 如果主控台專案實作為 .exe 檔案的一部分，則會將它註冊為 command 物件。 如果專案實作為匯出 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式的 .dll 檔案，則註冊會有所不同。

這些主題會討論特定的需求：

-   [如何註冊可執行檔主控台專案](how-to-register-an-executable-control-panel-item-registration-.md)
-   [如何註冊 DLL 主控台專案](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[主控台專案](control-panel-applications.md)
</dt> <dt>

[使用者體驗指南](user-experience-guidelines.md)
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

[在 Windows Vista 下存取保管庫模式下的主控台](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
