---
description: COMREPL 是一個公用程式，它會將指定來源電腦的 COM + 類別目錄複寫到一或多部目的電腦。
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: COMREPL 複製公用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936439"
---
# <a name="the-comrepl-replication-utility"></a>COMREPL 複製公用程式

COMREPL 是一個公用程式，它會將指定來源電腦的 COM + 類別目錄複寫到一或多部目的電腦。 請考慮代表「主要設定」的來源電腦。 COMREPL 用來複寫此主要設定，以維護一組設定相同的電腦。

複寫的單位是主要電腦上的整個 COM + 設定。 主要複本上的所有 COM + 應用程式都會複寫到目的電腦;全部或沒有東西。 此外，先前安裝在目的電腦上的所有 COM + 應用程式（COM + 預先安裝的應用程式除外）將會在複寫過程中刪除。

COMREPL 只會複寫 COM + 設定資料。 這包括 COM + 應用程式和 COM + 特定電腦設定。 Microsoft Internet Information Services (IIS) 都有類似的公用程式 (IISSync) ，這會使用 COMREPL 來複寫 IIS 和 COM + 設定。

如需啟動和使用 COMREPL 的詳細資訊，請參閱本節中的下列主題：

-   [使用 COMREPL](using-comrepl.md)
-   [複寫的內容](what-gets-replicated.md)
-   [複寫階段](replication-phases.md)
-   [檔案管理](file-management.md)
-   [記錄和錯誤報表](logging-and-error-reporting.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 COM + 應用程式的安裝套件](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[部署應用程式 proxy](deploying-application-proxies.md)
</dt> <dt>

[COM + 類別目錄](the-com--catalog.md)
</dt> </dl>

 

 



