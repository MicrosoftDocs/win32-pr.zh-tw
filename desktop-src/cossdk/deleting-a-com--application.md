---
description: 由於現有的應用程式已過期或不再使用，因此您可能需要移除它們。
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: 刪除 COM + 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8332cd59ecde4115daa43ea97bc87d4354338e3ea94073317bfa293102deb78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047506"
---
# <a name="deleting-a-com-application"></a>刪除 COM + 應用程式

由於現有的應用程式已過期或不再使用，因此您可能需要移除它們。

**若要刪除 COM + 應用程式**

1.  在 [元件服務] 系統管理工具的主控台樹中，選取您要刪除應用程式的電腦。

2.  開啟指定電腦的 [ **Com + 應用程式** ] 資料夾，以顯示所有應用程式。

3.  選取您要移除的應用程式。

4.  如果您是選取伺服器應用程式，請關閉應用程式。 您可以在 [元件服務] 系統管理工具中選取應用程式，以滑鼠右鍵按一下，然後按一下 [ **關機**]，以關閉應用程式。 如果您選取了程式庫應用程式，請確定目前使用此程式庫應用程式的所有進程都已關閉。

5.  在 [ **動作** ] 功能表上，按一下 [ **刪除**]。 您也可以用滑鼠右鍵按一下應用程式名稱，然後按一下 [ **刪除**]。 您也可以在 [元件服務] 系統管理工具中選取應用程式，然後按下 **delete** 鍵，也可以選取應用程式、按一下滑鼠右鍵，然後按一下 [ **刪除**]，以刪除應用程式。

6.  當系統提示您確認您的動作時，請按一下 **[是]** 。

此外，如果使用 Windows Installer (的電腦上安裝了伺服器應用程式或應用程式 proxy （如 < 安裝 com + 應用程式) 中所述），您可以透過 Microsoft Windows 主控台中的 [新增/移除程式] 公用程式來刪除它。 或者，您可以使用 Windows Installer 命令列語法來刪除已安裝的伺服器應用程式或應用程式 proxy：

**msiexec-x** *應用程式 \_ 名稱 * * * .msi**

這些方法特別適用于在未執行「元件服務」系統管理工具的用戶端電腦上刪除 COM + 應用程式。

刪除應用程式也會刪除應用程式中包含的任何元件。 如果這些元件相依于其他資源 (資料庫連線、資料或文字檔、IIS 虛擬根目錄設定等等) ，則必須透過 [元件服務] 系統管理工具以外的機制移除這些資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[複製元件](copying-components.md)
</dt> <dt>

[建立新的 COM + 應用程式](creating-a-new-com--application.md)
</dt> <dt>

[匯入元件](importing-components.md)
</dt> <dt>

[安裝新元件](installing-new-components.md)
</dt> <dt>

[移動元件](moving-components.md)
</dt> <dt>

[從 COM + 應用程式移除元件](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



