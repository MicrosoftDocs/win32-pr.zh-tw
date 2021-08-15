---
description: 應用程式可以將部分登錄儲存在檔案中，然後將檔案的內容載入至登錄中。
ms.assetid: a71a564d-934a-46e8-b555-989a6fa82337
title: 登錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a5caa34a075e4bffe48a542d02eec896ab28dd93fbdc2745dbc5a08effb9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763811"
---
# <a name="registry-files"></a>登錄檔

應用程式可以將部分登錄儲存在檔案中，然後將檔案的內容載入至登錄中。 當正在操作大量資料、在登錄中進行許多專案時，或是當資料是暫時性且必須載入，然後再卸載時，登錄檔會很有用。 備份與還原登錄元件的應用程式很可能會使用登錄檔。

若要將金鑰和其子機碼和值儲存至登錄檔，應用程式可以呼叫 [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) 或 [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) 函式。

[**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) 和 [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) 會使用封存屬性來建立檔案。 檔案會建立在本機密鑰之進程的目前的目錄中，以及遠端金鑰的% systemroot% \\ system32 目錄中。

登錄檔具有下列兩種格式：標準和最新。 標準格式是 Windows 2000 所支援的唯一格式。 較新版本的 Windows 也支援，以提供回溯相容性。 [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) 會以標準格式建立檔案。

從 Windows XP 開始支援最新的格式。 無法在 Windows 2000 上載入以此格式建立的登錄檔。 [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) 可以藉由指定 reg \_ 標準 \_ 格式或 reg \_ 最新格式，以任何一種格式儲存登錄檔 \_ 。 因此，它可以用來將使用標準格式的登錄檔轉換為最新的格式。

若要將登錄檔寫回登錄，應用程式可以使用 [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya)、 [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)或 [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) 功能，如下所示。

-   **RegLoadKey** 會將指定檔案中的登錄資料，載入至呼叫應用程式電腦或遠端電腦上的 **HKEY \_ USERS** 或 **HKEY \_ LOCAL \_ MACHINE** 下的指定子機碼。 如果指定的子機碼不存在，則此函式會建立該子機碼。 在呼叫此函式之後，應用程式可以使用 [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya) 函式將登錄還原至先前的狀態。
-   [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya) 會以指定檔案中包含的資料取代登錄中的機碼及其所有子機碼和值。 新的資料會在系統下次啟動時生效。
-   [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) 會將指定檔案中的登錄資料載入至呼叫應用程式電腦或遠端電腦上的指定機碼。 此函式會將指定索引鍵的子機碼和值取代為檔案中最上層金鑰後面的子機碼和值。

[**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya)函式會在另一部電腦上建立與預先定義之登錄控制碼的連接。 應用程式通常會使用此功能，從網路環境中其他電腦上的遠端登入存取訊號，您也可以使用登錄編輯程式來進行此作業。 您可能會想要存取遠端登入來備份登錄或管制其網路存取。 請注意，您必須具有適當的許可權，才能使用此功能來存取遠端登入。

 

 



