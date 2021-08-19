---
description: 本主題中的程式會識別如何建立 Windows Installer 套件來安裝 Win32 元件。
ms.assetid: 2d4bc2be-cce6-45e6-b6a7-7ff96d28eb96
title: 在 Windows XP 上安裝 Win32 元件以私用應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f478bddeb04ca9112610bd88338437002082204cc62078bde200539a8a18b6bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893808"
---
# <a name="installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp"></a>在 Windows XP 上安裝 Win32 元件以私用應用程式

本主題中的程式會識別如何建立 Windows Installer 套件來安裝 Win32 元件。 封裝會將元件和應用程式資訊清單檔案安裝到應用程式所使用的撰寫資料夾中。 應用程式資訊清單會指定應用程式在私用元件上的相依性。 安裝封裝之後，私用元件可用於應用程式的專屬用途。 應用程式資訊清單中指定的元件相依性會覆寫此應用程式 (，) 組件資訊清單檔中所指定的任何其他全域程式集相依性。

繼續進行之前，最好先瞭解如何撰寫不含元件的 Windows Installer 套件。 如需詳細資訊，請參閱 [安裝範例](an-installation-example.md)。

**在 Windows XP 上安裝私用元件**

1.  定義包含 Win32 元件和應用程式資訊清單檔的 Windows Installer 元件。 此元件可以包含應該一律隨元件一起安裝或移除的其他資源。 此程式的其餘步驟說明如何編寫安裝資料庫來安裝此元件。
2.  針對包含 Win32 元件和應用程式資訊清單檔的元件，將資料列加入 [元件資料表](component-table.md) 中。 輸入此元件程式碼的有效 Windows Installer [GUID](guid.md) 。 如需詳細資訊，請參閱 [變更元件程式碼](changing-the-component-code.md) ，以及 [元件規則是否中斷時會發生什麼事？](what-happens-if-the-component-rules-are-broken.md)
3.  安裝程式會將組件資訊清單檔複製到包含 MsiAssembly 資料表的 [檔應用程式] 欄位中所指定之檔案的資料夾中 \_ 。 [](msiassembly-table.md)
4.  將資料列加入至[FeatureComponents 資料表](featurecomponents-table.md)，以將元件與 Windows Installer 功能系結。 如需詳細資訊，請參閱 [元件和功能](components-and-features.md)。 Windows Installer 的功能應該是使用者可辨識的應用程式功能的一部分。 當使用者選取這項功能或應用程式發生錯誤時，就會啟動元件。 如果元件定義了額外的功能，請在功能 [資料表](feature-table.md) 中為功能屬性新增一個額外的資料列。 如果撰寫合併模組，則不需要此步驟。
5.  針對並存元件，系結和啟用資訊（例如 COM 類別、介面和類型程式庫）會儲存在資訊清單檔中，而不是儲存在登錄中。 私用元件會將這項資訊儲存在組件資訊清單中。 在支援並存元件的系統上，安裝程式會略過處理 [延伸模組資料表](extension-table.md)、 [動詞資料表](verb-table.md)、 [TypeLib 資料表](typelib-table.md)、 [MIME 資料表](mime-table.md)、 [類別資料表](class-table.md)、 [ProgId 資料表](progid-table.md)和 [AppId 資料表](appid-table.md)中所輸入元件的任何相關資訊。 您可以在資料表中輸入系結和啟用資訊，以供不支援並存元件共用的系統使用。
6.  並存安裝不會全域註冊元件。 如果 [SelfReg 資料表](selfreg-table.md)中輸入了任何自我註冊資訊，安裝程式會略過自我註冊元件。 您可以在 SelfReg 資料表中輸入自我註冊資訊，以便在不支援並存元件共用的系統上自行註冊元件。
7.  在登錄 [資料表](registry-table.md)、 [RemoveRegistry 資料表](removeregistry-table.md)和 [環境資料表](environment-table.md)中，新增任何其他登錄資訊，包括系結和啟用或自我註冊元件。
8.  安裝程式會在支援並存共用的作業系統上，略過此元件的 [IsolatedComponent 資料表](isolatedcomponent-table.md) 。 如果您想要元件在支援本機檔案的系統上是私用的，請在這個資料表中輸入資訊。
9.  針對包含 Win32 元件的元件，將資料列加入至 [MsiAssembly 資料表](msiassembly-table.md) 。 在 MsiAssembly 資料表的 [屬性] 欄位中輸入1的值，以指定這是 Win32 元件。 在 MsiAssembly 資料表的 [檔案應用程式] 欄位中，輸入私用元件的檔案索引鍵 \_ 。 [](msiassembly-table.md) 將 [MsiPublishAssemblies 動作](msipublishassemblies-action.md) 加入至 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 或 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)。 將 [MsiUnpublishAssemblies 動作](msiunpublishassemblies-action.md) 加入至 InstallExecuteSequence 資料表。 將元件和資訊清單檔案的資料夾製作到 [目錄資料表](directory-table.md)中。 此資料夾應該位於應用程式的根目錄中，並且包含 MsiAssembly 資料表的 [檔應用程式] 欄位中指定的檔案 \_ 。 [](msiassembly-table.md) 在應用程式安裝期間，安裝程式會解析 [目錄資料表](directory-table.md) 以取得此資料夾的路徑。 如需詳細資訊，請參閱 [使用目錄資料表](using-the-directory-table.md)。
10. 將資料列加入至元件的 [MsiAssemblyName 資料表](msiassemblyname-table.md) 。 針對資訊清單的 assemblyIdentity 區段中指定的每個名稱和值組，各加入一個資料列。 如需詳細資訊，請參閱 [MsiAssemblyName 資料表](msiassemblyname-table.md)。

 

 



