---
description: 以下說明如何建立 Windows Installer 套件來安裝 Win32 元件。
ms.assetid: 1234e904-fc7f-4eb7-8c50-0c959bbf5261
title: 安裝適用于並存共用的 Win32 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea72c9bcb7bd85ac38dfc8857030d6b9d6afbf23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997937"
---
# <a name="installing-win32-assemblies-for-side-by-side-sharing"></a>安裝適用于並存共用的 Win32 元件

以下說明如何建立 Windows Installer 套件來安裝 Win32 元件。 封裝會在 Winsxs 資料夾中安裝並存元件，以供共用應用程式使用。 安裝封裝之後，共用的元件可供任何應用程式使用，以指定組件資訊清單檔中元件的相依性。 安裝程式不會在系統上全域註冊並存元件。

請注意，您可以使用 [合併模組](merge-modules.md)安裝共用並存元件。

繼續之前，您應該瞭解如何撰寫不含元件的 Windows Installer 套件。 如需如何編寫簡單安裝的範例，請參閱 [安裝範例](an-installation-example.md)。

**並存安裝共用元件**

1.  定義包含 Win32 元件的 Windows Installer 元件。 此元件可能包含應一律隨元件一起安裝或移除的其他資源。 您可以撰寫應用程式的所有其他元件，就像是沒有元件的安裝一樣。 針對包含 Win32 元件的元件，將資料列加入 [元件資料表](component-table.md) 中。 輸入此元件程式碼的有效 Windows Installer [GUID](guid.md) 。 請勿使用資訊清單檔作為此元件的金鑰路徑。
2.  將資料列加入至 [FeatureComponents 資料表](featurecomponents-table.md) ，以將元件與 Windows Installer 功能系結。 如需詳細資訊，請參閱 [元件和功能](components-and-features.md)。 Windows Installer 的功能應該是可辨識給使用者的應用程式功能部分。 當使用者選取這項功能或應用程式發生錯誤時，就會啟動元件。 如果元件定義了額外的功能，請在功能 [資料表](feature-table.md) 中為功能的屬性新增一個額外的資料列。 撰寫合併模組時，不需要執行此步驟。
3.  針對並存元件，系結和啟用資訊（例如 COM 類別、介面和類型程式庫）會儲存在資訊清單檔中，而不是儲存在登錄中。 共用的元件會將這項資訊儲存在組件資訊清單中。 在支援並存元件的系統上，安裝程式會略過處理 [延伸模組資料表](extension-table.md)、 [動詞資料表](verb-table.md)、 [TypeLib 資料表](typelib-table.md)、 [MIME 資料表](mime-table.md)、 [類別資料表](class-table.md)、 [ProgId 資料表](progid-table.md)和 [AppId 資料表](appid-table.md)中所輸入元件的任何資訊。 您可以在這些資料表中輸入系結和啟用資訊，以供不支援並存元件共用的系統使用。
4.  並存安裝不會全域登錄元件，如果在 [SelfReg 資料表](selfreg-table.md)中輸入任何自我註冊資訊，安裝程式會略過自我註冊元件。 您可以在 SelfReg 資料表中輸入自我註冊資訊，以便在不支援並存元件共用的系統上自行註冊元件。
5.  在登錄 [資料表](registry-table.md)、 [RemoveRegistry 資料表](removeregistry-table.md)和 [環境資料表](environment-table.md)中，新增任何其他登錄資訊，包括系結和啟用或自我註冊元件。
6.  因為這是共用的元件，所以不會產生本機檔案。 請勿在 [IsolatedComponent 資料表](isolatedcomponent-table.md)中包含此元件的資訊。 安裝程式會在支援並存共用的作業系統上，略過此元件的 IsolatedComponent 資料表。 如果您希望元件在支援本機檔案的系統上是私用的，請將資訊新增至 IsolatedComponent 資料表。
7.  若要啟用並存共用，必須將 Win32 元件安裝在 Winsxs 資料夾中。 這是藉由將元件的 \_ [MsiAssembly 資料表](msiassembly-table.md) 的 File Application 資料行保留為 null 來完成。 這會告知安裝程式將元件安裝到 WinSxS 資料夾，而不是元件的資料夾。 針對包含 Win32 元件的元件，將資料列加入至 [MsiAssembly 資料表](msiassembly-table.md) 。 在 MsiAssembly 資料表的 [屬性] 欄位中輸入1的值，以指定這是 Win32 元件。 若為共用的元件，請將 [檔案 \_ 應用程式] 欄位保留空白。 將 [MsiPublishAssemblies 動作](msipublishassemblies-action.md) 加入至 [InstallExecuteSequence 資料表](installexecutesequence-table.md) 或 [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)。 將 [MsiUnpublishAssemblies 動作](msiunpublishassemblies-action.md) 加入至 InstallExecuteSequence 資料表。
8.  將資料列加入至元件的 [MsiAssemblyName 資料表](msiassemblyname-table.md) 。 針對資訊清單的 assemblyIdentity 區段中指定的每個名稱和值組，各加入一個資料列。 如需範例，請參閱 [MsiAssemblyName 資料表](msiassemblyname-table.md)。

 

 



