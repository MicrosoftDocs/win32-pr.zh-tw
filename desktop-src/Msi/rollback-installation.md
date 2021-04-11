---
description: 當 Windows Installer 處理產品或應用程式安裝的安裝腳本時，它會同時產生復原腳本，並在安裝期間儲存每個已刪除檔案的複本。
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: 復原安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114549"
---
# <a name="rollback-installation"></a>復原安裝

當 Windows Installer 處理產品或應用程式安裝的安裝腳本時，它會同時產生復原腳本，並在安裝期間儲存每個已刪除檔案的複本。 這些檔案會保存在隱藏的系統目錄中，並在成功完成安裝之後自動刪除。 但是，如果安裝失敗，安裝程式會自動執行復原安裝，將系統復原為其原始狀態。

自動復原失敗的安裝是安裝程式的預設行為。 若要在安裝期間停用復原，請使用下列其中一項：

-   [**DISABLEROLLBACK 屬性**](-disablerollback.md)
-   [**PROMPTROLLBACKCOST 屬性**](promptrollbackcost.md)
-   [DisableRollback 動作](disablerollback-action.md)
-   [DisableRollback](disablerollback.md)
-   [EnableRollback ControlEvent](enablerollback-controlevent.md)

一旦停用復原，安裝程式就會設定 [**RollbackDisabled**](rollbackdisabled.md) 屬性。

如果安裝使用 [自訂動作](custom-actions.md)，則需要額外撰寫安裝套件才能使用復原功能。 如需詳細資訊，請參閱 [復原自訂動作](rollback-custom-actions.md)。

 

 



