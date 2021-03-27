---
description: 瞭解如何延伸 Windows 檔案總管功能區。
title: 擴充功能區
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511036"
---
# <a name="extending-the-ribbon"></a>擴充功能區

在 Windows 檔案總管中，功能區有助於讓常見的終端使用者檔案管理活動更容易且更容易探索，但應用程式開發人員也有變更比賽即將展開。 例如，舊的命令列可自由擴充，但此時功能區會受到更多的限制。 此外，所有命名空間延伸模組預設都不會顯示功能區，所以您必須選擇取得功能區;否則，您會取得較舊的命令列。

使用者可以在功能區上使用的動作可以分為三種擴充性類別：

-   不需要擴充性。 範例：複製、貼上、刪除。 Windows 會為您處理這些動詞。
-   目前不允許擴充性：範例： Zip、Close Session 和其他自訂動作。 使用內容功能表來涵蓋這些案例。
-   擴充功能內建于動作本身。 範例：搜尋、電子郵件、列印、新專案。 您必須註冊這些動詞，以將您的應用程式或檔案格式包含在功能區中。

本檔說明如何加入宣告以取得功能區，以及如何註冊來處理特定功能區動詞。

## <a name="opting-in-to-the-ribbon"></a>加入宣告功能區

若要加入宣告功能區，您的 [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2)執行應該在 [**IExplorerPaneVisibility：： GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate)中指定 **EP \_ 功能區**，並在上傳回 **eps \_ 強制** \| **eps \_ 預設值 \_**。

## <a name="extending-the-ribbon-for-file-extensions"></a>擴充副檔名的功能區

這些功能區按鈕可根據副檔名進行擴充：

-   全部解壓縮
-   \| (ISO) 掛接燒錄
-   播放播放 \| 全部 \| 新增至播放清單 (動詞：排入佇列) 
-   開啟
-   編輯
-   屬性

當您註冊以靜態方式處理新檔案類型的相關動詞時，功能區會適當地處理動詞。 您可以像操作功能表動詞一樣註冊。 如需檔案關聯和註冊動詞命令的詳細資訊，請參閱 [動詞和檔案關聯](fa-verbs.md) 和 [建立快捷方式功能表處理常式](context-menu-handlers.md)。

## <a name="registering-as-a-default-handler-for-actionids"></a>註冊為 ActionIds 的預設處理常式

首先，在適當的 AssocActionId 子機碼下註冊您的 ProgId。 每個 AssocActionId 子機碼代表使用者可以從功能區叫用的動詞或動作。 在此範例中，應用程式會註冊 ZipSelection ActionID，以擴充功能區上的 [全部解壓縮] 按鈕。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

註冊完成之後，您必須接著註冊來處理通訊協定，就像平常一樣，如 [預設程式](default-programs.md)中所述。

 

 



