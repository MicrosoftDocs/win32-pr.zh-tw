---
description: 安裝套件的作者可以指定安裝程式將共用檔案 (共用的) 應用程式複製到該應用程式的資料夾，而不是共用位置。
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: 隔離的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08095e72862a94474b7096950ac5ed3b331e806456e72982ee9d7374ab9511b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013176"
---
# <a name="isolated-components"></a>隔離的元件

安裝套件的作者可以指定安裝程式將共用檔案 (共用的) 應用程式複製到該應用程式的資料夾，而不是共用位置。 只有應用程式才會使用這組私用的檔案 (Dll) 。 以這種方式將應用程式與共享的元件隔離，有下列優點：

-   應用程式一律會使用所部署的共用檔案版本。
-   安裝應用程式不會覆寫其他應用程式的其他版本的共用檔案。
-   後續使用不同版本的共用檔案安裝其他應用程式時，將無法覆寫此應用程式所使用的檔案。

由於目前的 COM 執行會在每個 CLSID/內容配對的登錄中保留單一完整路徑，因此它會強制所有應用程式使用相同版本的共用 DLL。 為了讓應用程式保留 COM 伺服器的私用複本，Windows 2000 中的系統載入器會檢查是否存在。應用程式資料夾中的本機檔案。 如果系統載入器偵測到。本機檔案，它會改變其搜尋邏輯，以偏好位於與應用程式相同資料夾中的 Dll。

當 Windows Installer 執行[IsolateComponents 動作](isolatecomponents-action.md)時，它們會將元件的檔案複製 (通常是在 IsolatedComponent 資料表的元件共用資料行中指定的共用 DLL) ， \_ (通常是 [元件應用程式] 資料行中指定 .exe 檔案) [](isolatedcomponent-table.md) \_ 。 安裝程式會在此目錄中建立檔案（長度為零個位元組），具有元件應用程式金鑰檔的簡短檔案名 \_ (通常是與應用程式的 .exe) 附加的相同名稱。當地。 安裝程式會使用該元件在其共用位置的註冊，且不會針對私人位置中的元件複本寫入任何註冊資訊。

如需詳細資訊，請參閱

-   [獨立元件的安裝](installation-of-isolated-components.md)
-   [重新安裝隔離的元件](reinstallation-of-isolated-components.md)
-   [移除隔離的元件](removal-of-isolated-components.md)
-   [使用隔離的元件](using-isolated-components.md)

 

 



