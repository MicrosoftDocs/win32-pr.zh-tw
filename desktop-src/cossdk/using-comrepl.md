---
description: 使用 COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: 使用 COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688996"
---
# <a name="using-comrepl"></a>使用 COMREPL

若要啟動 COMREPL 命令列公用程式，請使用下列步驟：

1.  \\ \\ 在命令提示字元中輸入下列命令，將% windir% system32 Com 新增至預設環境路徑：

    **set path =% PATH%;% windir% \\ system32 \\ Com**

2.  輸入下列 COMREPL 命令：

    **COMREPL** *sourceComputer* *targetComputerList* **\[ \[ /n \] /v \]**

    其中：

    -   *sourceComputer* 是來源的電腦名稱稱

    -   *targetComputerList* 是以空格分隔的目標電腦名稱稱

    -   **/n** 在開始複寫之前隱藏確認提示

    -   **/v** 將記錄檔輸出回顯至主控台

## <a name="notes"></a>備註

-   由於 COM + 不會複寫 (只有設定資料和應用程式) ，所有目的電腦都必須已安裝 COM +。
-   使用者必須在來源和目的電腦上通過系統應用程式的角色檢查。
-   不會複寫角色可使用的本機電腦帳戶。
-   目的電腦 (s) 必須在線上。
-   使用者必須負責複寫所有非 COM + 資料 (例如，資料庫資料表、資料檔案等等，) 到目的電腦 (s) 。
-   叢集可以參與複寫，但請注意，COMREPL 只會複寫到已命名的電腦。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案管理](file-management.md)
</dt> <dt>

[記錄和錯誤報表](logging-and-error-reporting.md)
</dt> <dt>

[複寫階段](replication-phases.md)
</dt> <dt>

[複寫的內容](what-gets-replicated.md)
</dt> </dl>

 

 



