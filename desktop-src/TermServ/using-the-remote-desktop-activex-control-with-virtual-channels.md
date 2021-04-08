---
title: 使用具有虛擬通道的遠端桌面 ActiveX 控制項
description: 如果您已在遠端桌面服務部署中啟用虛擬通道應用程式，則可以將此應用程式提供給用戶端電腦使用。
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c8fa23f1498270bd0d2a29c5f48d50f0b2463
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840172"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>使用具有虛擬通道的遠端桌面 ActiveX 控制項

如果您已在遠端桌面服務部署中啟用虛擬通道應用程式，可以透過遠端桌面 ActiveX 控制項，將此應用程式提供給存取遠端桌面工作階段主機 (RD 工作階段主機) server 的用戶端電腦使用。

**讓虛擬通道應用程式可供使用**

1.  部署應用程式的伺服器端模組，並確定它正在 RD 工作階段主機伺服器上執行。 在 web 伺服器上執行之遠端桌面服務 web 應用程式的 [連接] 頁面中，存取 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)介面的 **PluginDlls** 屬性，以指定虛擬通道 DLL 的名稱。 如果您有一個以上的外掛程式，請指定以逗號分隔的 DLL 名稱清單。 比方說，如果您的虛擬通道外掛程式名為 "MyPlugin.dll"，請使用下列程式碼：

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    如果您有兩個虛擬通道 Dll，請使用下列程式碼。 在此範例中，DLL 檔案名為 "MyPlugin.dll" 和 "Vdriver.dll"：

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    基於安全性理由， **PluginDlls** 屬性只接受虛擬通道 dll 的命名清單。 如果指定了任何格式的檔案系統或 UNC 路徑，控制項就會傳回錯誤。 此外，Dll 的名稱必須只包含英數位元。

2.  確定已將用戶端模組安裝在% windir% \\ system32 目錄中。

虛擬通道 API 不允許在單一進程內載入相同虛擬通道 DLL 的多個實例。 基於這個原因，如果在相同進程中執行的遠端桌面 ActiveX 控制項有多個實例，則只有控制項的第一個實例才能載入虛擬通道 DLL。 如果您要設計的虛擬通道應用程式必須在單一進程內支援多個實例，您必須使用 [動態虛擬通道](dynamic-virtual-channels.md) API 來執行虛擬通道應用程式。

> [!Note]  
> 根據預設，遠端桌面 ActiveX 控制項會從% windir% system32 目錄載入虛擬通道用戶端 Dll \\ 。 系統管理員可以變更此預設用戶端外掛程式 DLL 目錄。 若要這樣做，請在用戶端電腦上編輯 **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** registry key。 此目錄路徑不能以 UNC 格式指定。

 

 

 




