---
description: 記錄和錯誤報表
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: 記錄和錯誤報表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970739"
---
# <a name="logging-and-error-reporting"></a>記錄和錯誤報表

## <a name="log-file"></a>記錄檔

COMREPL 會產生包含狀態和錯誤訊息的記錄檔。 此檔案會儲存在 COMREPL 于% systemdir% \\ com replication COMREPL 中啟動的電腦上 \\ \\ 。

當複製階段開始時，會清除此記錄檔。 後續的目標安裝將會附加至檔案。

## <a name="error-handling"></a>錯誤處理

錯誤會記錄在上述的記錄檔中。 您也可以在來源或目的電腦的事件記錄檔中找到詳細的錯誤資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案管理](file-management.md)
</dt> <dt>

[複寫階段](replication-phases.md)
</dt> <dt>

[使用 COMREPL](using-comrepl.md)
</dt> <dt>

[複寫的內容](what-gets-replicated.md)
</dt> </dl>

 

 



