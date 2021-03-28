---
description: Windows UI 可讓使用者存取執行應用程式和管理作業系統所需的各種物件。
title: Windows Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973324"
---
# <a name="windows-shell"></a>Windows Shell

Windows UI 可讓使用者存取執行應用程式和管理作業系統所需的各種物件。 這些物件最多與熟悉的是位於電腦磁片磁碟機上的資料夾和檔案。 另外還有一些虛擬物件，可讓使用者執行工作，例如將檔案傳送至遠端印表機或存取資源回收筒。 Shell 會將這些物件組織成階層命名空間，並為使用者和應用程式提供一致且有效率的方式來存取和管理物件。

## <a name="shell-development-scenarios"></a>Shell 開發案例

下列開發案例與應用程式開發有關：

-   擴充 Shell，其包含建立資料來源 (與取用 Shell 資料模型) 
-   執行 Shell 資料來源工作的子集
-   支援 Windows 檔案總管中的程式庫和專案視圖
-   使用一般檔案對話方塊
-   執行主控台專案
-   管理通知

下列開發案例與檔案格式擁有權有關：

-   執行 Shell 資料來源工作的子集
-   執行任何處理程式
-   支援桌面搜尋

下列開發案例與資料儲存體擁有權有關：

-   支援桌面搜尋和 OpenSearch
-    (虛擬資料夾執行 Shell 資料來源工作的子集) 
-   Windows 檔案總管中的支援程式庫

下列開發案例與裝置支援相關：

-   自動執行和自動播放

## <a name="windows-shell-sdk-documentation"></a>Windows Shell SDK 檔

本檔分為三個主要部分：

-   [Shell 開發人員指南](intro.md)提供有關 Shell 如何運作的概念資料，以及如何在您的應用程式中使用 SHELL 的 API。
-   [ [Shell 參考](shell-reference-bumper.md) ] 區段記錄組成各種 Shell api 的程式設計項目。
-   [Shell 範例](samples-entry.md) 提供相關程式碼範例的連結。

下表提供 [Shell 參考] 區段的大綱。 除非另有說明，否則所有程式設計項目都會記載在非受控 c + + 中。



| 區段                                                               | 描述                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Shell 類別](classes.md)                                          | 本節說明如何選取 Windows Shell 類別。                                                                 |
| [Shell 介面](interfaces.md)                                    | 本節說明 (COM) 介面的 Windows Shell 元件物件模型。                                    |
| [Shell 函數](functions.md)                                      | 本節說明 Windows Shell 函數。                                                                  |
| [Shell 回呼函數](callbacks.md)                             | 本節說明 Windows Shell 回呼函式範本。                                               |
| [Shell 常數、列舉和旗標](consts-enums-flags.md)    | 本節說明 Shell Api 中所使用的 Windows Shell 常數、列舉和旗標。                  |
| [Shell 輕量公用程式函式](shlwapi.md)                    | 本節說明 Shlwapi.dll 中提供的 Windows Shell 輕量公用程式函式。                      |
| [Shell 宏](macros.md)                                            | 本節說明 Windows Shell 公用程式宏。                                                             |
| [Shell 訊息和通知](messages.md)                      | 本節說明 Windows Shell 的元素所傳送的訊息和通知。                         |
| [腳本和 Microsoft Visual Basic 的 Shell 物件](objects.md) | 本節描述 Shell 所執行的 Windows 物件，以用於腳本和 Microsoft Visual Basic。 |
| [C + + 的 Shell 物件](objects-cpp.md)                              | 本節說明 Shell 所執行的 c + + Windows 物件。                                             |
| [Shell 架構](schemas.md)                                          | 本節說明 Windows Shell 所使用的程式庫、屬性和傳輸資訊清單架構。                   |
| [Shell 結構](structures.md)                                    | 本節說明 Shell Api 中使用的 Windows Shell 結構。                                          |



 

 

 



