---
description: RegOpenUserClassesRoot 函式會針對處理非互動式使用者用戶端的進程（例如服務）提供合併的視圖。
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: HKEY_CLASSES_ROOT 的合併視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52b48be32ec524cdac42808d7f4efddfc78854b56133e647d6f5a9b06ae88bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885416"
---
# <a name="merged-view-of-hkey_classes_root"></a>HKEY \_ 類別根目錄的合併 \_ 視圖

[**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot)函式會針對處理非互動式使用者用戶端的進程（例如服務）提供合併的視圖。 在此情況下， **HKEY \_ 類別 \_ 根金鑰** 會提供登錄的視圖，該登錄會將 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 中的資訊，與 **HKEY \_ 目前 \_ 使用者 \\ 軟體 \\ 類別** 的資訊合併。

系統會使用下列規則來合併兩個來源中的資訊：

-   合併的視圖包含 **HKEY \_ 目前 \_ 使用者 \\ 軟體 \\ 類別** 金鑰的所有子機碼。
-   合併的視圖包含 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰的所有立即子機碼，不會複製 HKEY 的 **\_ 目前 \_ 使用者 \\ 軟體 \\ 類別** 的子機碼。
-   本主題結尾處是在 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 和 **HKEY \_ 目前 \_ 使用者 \\ 軟體 \\ 類別** 中找到的子機碼清單。 **HKEY \_ 本機 \_ 電腦** 樹狀結構中這些機碼的立即子機碼，只會包含在合併的視圖中（如果它們不是 **HKEY \_ 目前 \_ 使用者** 樹狀結構中的立即子機碼的複本）。 合併的視圖不包含重複子 **機碼的 HKEY \_ 本機 \_ 電腦** 內容。

如果使用系統管理員許可權來執行應用程式，且已停用 [使用者帳戶控制]，則 COM 執行時間會忽略個別使用者的 COM 設定，並只存取每一電腦的 COM 設定。 需要系統管理員許可權的應用程式應該在安裝期間，將相依的 COM 物件註冊到個別電腦的 COM 設定存放區 (**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別**) 。 如需詳細資訊，請參閱 [AC： UAC： COM Per-User](/previous-versions/bb756926(v=msdn.10))設定。

**Windows Server 2003 和 Windows XP/2000：** 應用程式可以將相依的 COM 物件註冊到個別電腦或個別使用者的 COM 設定存放區 (**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 或 **HKEY 目前的 \_ \_ 使用者 \\ 軟體 \\ 類別**) 。

下列範例顯示 **HKEY \_ 本機 \_ 電腦** 底下的一組子機碼，並 **HKEY \_ 目前的 \_ 使用者** 金鑰，以及 **HKEY \_ 類別 \_ 根目錄** 的結果合併觀點。

**HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別**    **CLSID**       *2*       *4*          **inprocserver32**          **localserver32**       *7*

**HKEY \_目前 \_ 的 \\ 使用者軟體 \\ 類別**    **CLSID**       *1*       *4*          **localserver**       *6*       *10*          **localserver**

**HKEY \_類別 \_ 根目錄**    **CLSID**       *1*       *2*       *4*          **inprocserver32**          **localserver**          **localserver32**       *6*       *7*       *10*          **localserver**

下列子機碼可在 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 和 **HKEY 目前的 \_ \_ 使用者 \\ 軟體 \\ 類別** 中找到。 從 **HKEY \_ 本機 \_ 電腦** 樹狀目錄中，只有當這些金鑰與 **HKEY \_ 目前 \_ 使用者** 樹狀結構中的立即子機碼不重複時，才會將這些機碼的立即子機碼包含在合併的視圖中。 合併的視圖不包含重複子 **機碼的 HKEY \_ 本機 \_ 電腦** 內容。

**\***  
**\*\\shellex**  
**\*\\shellex \\ CoNtextMenuHandlers**  
**\*\\shellex \\ PropertySheetHandlers**  
**AppID**  
**Clsid**  
**元件類別**  
**磁碟機**  
**磁片磁碟機 \\ shellex**  
**磁片磁碟機 \\ shellex \\ CoNtextMenuHandlers**  
**磁片磁碟機 \\ shellex \\ PropertySheetHandlers**  
**FileType**  
**資料夾**  
**資料夾 \\ shellex**  
**資料夾 \\ shellex \\ ColumnHandler**  
**資料夾 \\ shellex \\ CoNtextMenuHandlers**  
**資料夾 \\ shellex \\ ExtShellFolderViews**  
**資料夾 \\ shellex \\ PropertySheetHandlers**  
**安裝程式 \\ 元件**  
**安裝程式 \\ 功能**  
**安裝程式 \\ 產品**  
**介面**  
**Mime**  
**Mime \\ 資料庫**  
**Mime \\ 資料庫 \\ 字元集**  
**Mime \\ 資料庫 \\ 字碼頁**  
**Mime \\ 資料庫 \\ 內容類型**  
**類型**  


 

 
