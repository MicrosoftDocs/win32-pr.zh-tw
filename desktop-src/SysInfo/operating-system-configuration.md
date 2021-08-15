---
description: Windows 目錄是包含以 Windows 為基礎的應用程式、初始化檔和說明檔的目錄。 GetWindowsDirectory 函式會捕獲此目錄的路徑。
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: 作業系統設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 747a881568f9814152a230880d38891590d33ffc67cfa5e8178adfa66c1a01fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885285"
---
# <a name="operating-system-configuration"></a>作業系統設定

*Windows 目錄* 是包含以 Windows 為基礎的應用程式、初始化檔和說明檔的目錄。 [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)函式會捕獲此目錄的路徑。

*系統目錄* 是包含動態連結程式庫、驅動程式和字型檔案的目錄。 [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)函式會捕獲此目錄的路徑。

[**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea)函式會捕獲目前登入系統的使用者名稱。 如果登錄中包含後者，使用者名稱可以是登入名稱或使用者的完整名稱。

*環境變數* 是代表系統某些元素的符號變數，例如路徑、檔案名或其他常值資料。 例如，環境變數路徑代表用來搜尋可執行檔的目錄。 當使用者登入時，系統會根據登錄的環境區段初始化環境變數。 [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa)函式會捕獲指定環境變數的值。

[**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo)介面會提供其他資訊。

 

 
