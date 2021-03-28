---
description: Windows UI 可讓使用者存取執行應用程式和管理作業系統所需的各種物件。
title: Shell 開發人員指南
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991150"
---
# <a name="shell-developers-guide"></a>Shell 開發人員指南

Windows UI 可讓使用者存取執行應用程式和管理作業系統所需的各種物件。 這些物件最多與熟悉的是位於電腦磁片磁碟機上的資料夾和檔案。 另外還有一些虛擬物件，可讓使用者進行工作，例如將檔案傳送至遠端印表機或存取資源回收筒。 Shell 會將這些物件組織成階層命名空間，並為使用者和應用程式提供一致且有效率的方式來存取和管理物件。

## <a name="in-this-section"></a>本節內容

-   [安全性考慮： Microsoft Windows Shell](sec-shell.md)
-   [執行擴充功能的指引 In-Process](shell-and-managed-code.md)
-   [Shell 和通用控制項版本](versions.md)
-   [執行基本資料夾物件介面](nse-implement.md)
-   [執行自訂檔案格式](customizing-file-types-bumper.md)
-   [Shell 擴充性 (建立資料來源) ](shell-extensibility-bumper.md)
-   [執行主控台專案](control-panel-applications.md)
-   [支援 Shell 應用程式](application-support-bumper.md)
-   [舊版 Shell 主題](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a>文件慣例

Shell 開發人員指南遵循一般 Windows 軟體開發套件 (SDK) 檔慣例。 請特別注意兩個慣例：

-   範例程式碼會省略正常的錯誤修正程式碼。 這段程式碼已移除，使程式碼更容易閱讀。 您應該在自己的應用程式中包含所有適當的錯誤修正程式碼。
-   若要清除範例登錄專案，請使用標準字型來顯示機碼、子機碼和專案名稱以及值。 使用者或應用程式定義的專案名稱為斜體。

 

 



