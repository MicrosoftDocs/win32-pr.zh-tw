---
description: 使用多語系消費者介面
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: 使用多語系消費者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195432"
---
# <a name="using-multilingual-user-interface"></a>使用多語系消費者介面

本節說明如何使用多語系消費者介面 (MUI) 功能來設計和執行您的應用程式。 以下是在應用程式生命週期的大部分階段中將扮演的 MUI 技術層面。

-   應用程式開發，包括資源準備、應用程式語言喜好設定的設定、尋找和載入資源
-   建立和當地語系化應用程式
-   部署應用程式

以下是設計和執行 MUI 應用程式時要考慮的一些問題。

-   應用程式將支援哪些 Windows 版本？
-   應用程式在哪些語言中會當地語系化？
-   應用程式語言設定是否應該一律遵循作業系統的語言設定，或應用程式使用者是否可以設定特定語言？
-   應用程式使用何種類型的使用者介面資源，以及它們的儲存位置為何？

本節包含下列主題。 描述會假設以 Windows Vista 和更新版本為目標的 MUI 應用程式。 此應用程式的資源是 Win32 資源，其特定語言的資源和可執行程式碼位於不同的 Win32 PE 檔案中。 針對 Windows Vista 前版作業系統或不同資源類型的支援，會視需要新增特殊的考慮。

-   [準備資源](preparing-resources.md)
-   [設定應用程式語言喜好設定](setting-application-language-preferences.md)
-   [尋找 Win32 PE 資源](locating-win32-pe-resources.md)
-   [尋找非 Win32 PE 資源](locating-non-win32-pe-resources.md)
-   [當地語系化資源和建立應用程式](localizing-resources-and-building-the-application.md)
-   [MUI：系統設定應用程式範例](mui-system-settings-application-sample.md)
-   [MUI： (Windows Vista) 的 Application-Specific 設定範例 ](mui-application-specific-settings-sample-vista.md)
-   [MUI： (Windows Vista 之前的 Application-Specific 設定範例) ](mui-application-specific-settings-sample-pre-vista.md)

 

 



