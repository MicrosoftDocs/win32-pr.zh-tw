---
description: HKEY \_ 類別 \_ ROOT (HKCR) 機碼包含副檔名關聯和 COM 類別註冊資訊，例如 Progid、Clsid 和 iid。 它主要是為了與16位 Windows 中的登錄相容。
ms.assetid: b404875f-11e1-48f2-98d2-0378a0646ed3
title: HKEY_CLASSES_ROOT 金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7aebe0e59424eb5ff7584fe61c2c5089eb887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852048"
---
# <a name="hkey_classes_root-key"></a>HKEY \_ 類別 \_ 根金鑰

**HKEY \_ 類別 \_ ROOT** (**HKCR**) 機碼包含副檔名關聯和 COM 類別註冊資訊，例如 [progid](../com/-progid--key.md)、 [clsid](../com/clsid-key-hklm.md)和 [iid](../com/interface-key.md)。 它主要是為了與16位 Windows 中的登錄相容。

類別註冊和副檔名資訊都會儲存在 **HKEY \_ 本機 \_ 電腦** 和 **HKEY \_ 目前的 \_ 使用者** 金鑰之下。 **HKEY \_ 本機電腦 \_ \\ 軟體 \\ 類別** 機碼包含可套用至本機電腦上所有使用者的預設設定。 **HKEY \_ CURRENT \_ user \\ Software \\** class 機碼包含僅適用于互動式使用者的設定。 **HKEY \_ 類別 \_ 根金鑰** 會提供登錄的視圖，以合併這兩個來源的資訊。 **HKEY \_類別 \_ 根目錄** 也會針對針對舊版 Windows 設計的應用程式，提供此合併的觀點。

使用者特定設定的優先順序高於預設設定。 例如，預設設定可能會指定特定的應用程式來處理 .doc 檔。 但是，使用者可以藉由在登錄中指定不同的應用程式來覆寫此設定。

諸如 [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) 或 [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) 等登錄功能，可讓您指定 **HKEY \_ 類別 \_ 根金鑰** 。 當您從在互動式使用者帳戶中執行的進程呼叫這些函式時，系統會將 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 中的預設設定與 **HKEY \_ 目前 \_ 使用者 \\ 軟體 \\ 類別** 的互動式使用者設定合併。 如需有關如何合併這些設定的詳細資訊，請參閱 [HKEY \_ 類別 \_ 根目錄的合併觀點](merged-view-of-hkey-classes-root.md)。

若要變更互動式使用者的設定，請將變更儲存在 **HKEY \_ CURRENT \_ user \\ Software \\ 類別** 下，而不是 **HKEY \_ 類別 \_ ROOT**。

若要變更預設設定，請在 [ **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別**] 下儲存變更。 如果您將金鑰寫入 **HKEY \_ 類別 \_ 根目錄** 下的金鑰，系統會將資訊儲存在 [ **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別**] 下。 如果您將值寫入至 **HKEY \_ 類別 \_ 根目錄** 下的索引鍵，而且索引鍵已經存在於 **HKEY 的 \_ 目前 \_ 使用者 \\ 軟體 \\ 類別** 下，則系統會在該處儲存資訊，而不是在 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 下儲存資訊。

在非互動式使用者的安全性內容中執行的進程，不應該使用 **HKEY \_ 類別 \_ 根金鑰** 搭配登錄函式。 相反地，這類進程可以明確開啟 [ **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別] 機** 碼來存取預設設定。 若要開啟登錄機碼，以將 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 的內容與指定使用者的設定合併，這些程式可呼叫 [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) 函式。 例如，模擬用戶端的執行緒如果需要為模擬的用戶端抓取合併的視圖 [，則可以](/windows/desktop/SecAuthZ/client-impersonation) 呼叫 **RegOpenUserClassesRoot** 。 請注意，如果指定之使用者的使用者設定檔尚未載入， **RegOpenUserClassesRoot** 就會失敗。 系統會在登入時自動載入互動式使用者的設定檔。 若為其他使用者，您必須呼叫 [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) 函式來明確載入使用者的設定檔。

如果應用程式是以系統管理員許可權執行，而且已停用 [使用者帳戶控制]，則 COM 執行時間會忽略每一使用者的 COM 設定，並只存取個別電腦的 COM 設定。 需要系統管理員許可權的應用程式應該在安裝期間，將相依的 COM 物件註冊到個別電腦的 COM 設定存放區 (**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別**) 。 如需詳細資訊，請參閱 [AC： UAC： COM Per-User](/previous-versions/bb756926(v=msdn.10))設定。

**Windows Server 2003 和 WINDOWS XP/2000：** 應用程式可以將相依的 COM 物件註冊到個別電腦或個別使用者的 COM 設定存放區 (**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 或 **HKEY 目前的 \_ \_ 使用者 \\ 軟體 \\ 類別**) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[HKEY \_ 類別 \_ 根目錄 (資源套件登錄參考) ](/previous-versions/windows/it-pro/windows-server-2003/cc739822(v=ws.10))
</dt> </dl>

 

 
