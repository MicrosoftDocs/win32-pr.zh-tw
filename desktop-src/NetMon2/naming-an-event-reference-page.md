---
description: 在 (ERP) 原始檔 HTML 檔案中撰寫事件參考頁面之後，您必須先將它命名，才能網路監視器可以在事件檢視器中顯示。
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: 命名事件參考頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991375"
---
# <a name="naming-an-event-reference-page"></a>命名事件參考頁面

在 (ERP) 原始檔 HTML 檔案中撰寫事件參考頁面之後，您必須先將它命名，才能網路監視器可以在事件檢視器中顯示。

使用下列格式的名稱監視和專家 ERP 檔案：

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**
</dt> <dd>

DLL 檔案名，但不含副檔名。

</dd> <dt>

<span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**
</dt> <dd>

專家 ERP 的事件識別碼。

事件識別碼也可以在 **NMEVENTDATA** 結構的 **EventIdent** 成員中找到。

</dd> </dl>

如需有關建立 ERP 的詳細資訊，請參閱下列主題：

-   [建立專家和監視事件參考頁面](creating-expert-and-monitor-event-reference-pages.md)
-   [撰寫事件參考頁面](writing-an-event-reference-page.md)
-   [測試事件參考頁面](testing-an-event-reference-page.md)

 

 



