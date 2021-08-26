---
description: 記錄和錯誤報表
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: 記錄和錯誤報表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d974b4043b4365839aec6a4fae392ae1d84900e8b8347949147b8df13326bd1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990758"
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

 

 



