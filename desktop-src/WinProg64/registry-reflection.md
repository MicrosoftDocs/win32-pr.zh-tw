---
title: 登錄反映
description: 登錄重新導向程式會在 WOW64 上提供登錄某些部分的個別邏輯視圖，以隔離32位和64位應用程式。 不過，在32位和64位視圖中，某些登錄機碼的值必須相同。
ms.assetid: eac9038b-9f59-4ac7-8974-f94a4a62a257
keywords:
- 登錄反映64位 Windows 程式設計
- 反映64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523041004d9570bbdf101050e30f5d9139031913
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968292"
---
# <a name="registry-reflection"></a>登錄反映

\[本主題中的資訊適用于 Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP。 從 Windows 7 和 Windows Server 2008 R2 開始，WOW64 不再使用登錄反映，而是改為共用先前反映的金鑰。 如需詳細資訊，請參閱 [受 WOW64 影響的](shared-registry-keys.md)登錄機碼。\]

登錄 [重定向](registry-redirector.md) 程式會在 WOW64 上提供登錄某些部分的個別邏輯視圖，以隔離32位和64位應用程式。 不過，在32位和64位視圖中，某些登錄機碼的值必須相同。

登錄 *反映* 程式會複製登錄機碼和兩個登錄視圖之間的值，讓它們保持同步。 每個視圖都有個別的實體複本，分別包含每個反映的登錄機碼，一個用於32位的登錄視圖，另一個則用於64位登錄視圖。

藉由呼叫 [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey)來關閉索引鍵時，會複製反映的金鑰。 請注意，這會導致可能的競爭情形：如果有一個以上的進程變更了反映的索引鍵，則最後一個 **RegCloseKey** 呼叫會決定金鑰的最終值。

反映程式會在兩個視圖之間複製本機伺服器的 COM 啟用資料，但不會複製同進程資料，因為64位的 Windows 上不允許有32/64 的同進程資料混合。

未重新導向的共用登錄機碼或登錄機碼的反映未啟用。 例如，未針對 **HKEY \_ 本機 \_ 電腦 \\ 系統** 金鑰啟用反映。 如需重新導向、共用或反映的登錄機碼清單，請參閱 [受 WOW64 影響](shared-registry-keys.md)的登錄機碼。

登錄反映會使用「最後寫入者獲勝」原則，如下列範例所示：

-   在64位 Windows 的全新安裝之後，會註冊64位 Wordpad.exe，以處理 .doc 檔。 反映器會從64位登錄視圖將 .doc 註冊複製到32位登錄視圖中。
-   系統管理員會安裝32位 Office，在32位登錄視圖中註冊32位 Winword.exe 以處理 .doc 檔。 登錄反映程式會將這項資訊複製到64位的登錄視圖，因此32位和64位應用程式會為 .doc 檔案啟動32位版本的 Winword.exe。
-   系統管理員會安裝64位 Office，在64位登錄視圖中註冊64位 Winword.exe 以處理 .doc 檔。 登錄反映程式會將這項資訊複製到32位登錄中，因此32位和64位應用程式會為 .doc 檔案啟動64位版本的 Winword.exe。

因此，最近安裝的應用程式會保留檔案關聯資訊。

這對32位和64位應用程式來說非常有用，可共用通常會寫入個別登錄區的特定登錄機碼值。 例如，可提供32位和64位用戶端要求的32位 OLE 伺服器，可以將其32位登錄資料提供給系統登錄的64位視圖。

當元件在系統登錄中寫入資料時，WOW64 會分析該資訊，並在適當的情況下，于登錄的替代視圖中建立資料複本。 一般而言，此程式會在登錄的兩個瀏覽器中保留相同登錄機碼的兩個不同實體複本，而且稱為「登錄反映」或「登錄鏡像」。

類別根目錄底下的大部分索引鍵都是在這個類別中。 當更新完成且金鑰的控制碼關閉時，會反映金鑰的更新。 在特定情況下，如果金鑰有一些位相依性，則不會反映寫入金鑰。 例如，32位的 InprocServer32 金鑰與64位應用程式無關，因此 InprocServer32 索引鍵不會反映在64位登錄視圖中。 不過，64位應用程式可使用32位的 LocalServer32 金鑰，而 LocalServer32 索引鍵會反映出來。

針對 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ clsid** 和 **HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ 類別 \\ clsid**，只會反映未指定 InprocServer32 或 InprocHandler32 的 clsid。 只有 LocalServer32 Clsid 會反映出來，因為它們會跨進程執行，而且可以由32或64位應用程式啟用。 不會反映 InProcServer32 Clsid，因為無法載入32位 DLL 以在64位進程中執行，或使用64位 DLL 在32位進程中執行。

針對 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ appid** 和 **HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ 類別 \\ appid**，如果 [DllSurrogate](../com/dllsurrogate.md) 和 [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) 登錄值為空字串，則不會反映這些值。

若要停用並啟用特定反映索引鍵的登錄反映，請使用 [**RegDisableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey) 和 [**RegEnableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey) 函數。 這些函式不會影響在本主題稍早所反映之索引鍵清單中的索引鍵。 應用程式應該只針對其所建立的登錄機碼停用反映，而不會嘗試停用預先定義之索引鍵的反映，例如 **HKEY \_ 本機 \_ 電腦** 或 **HKEY \_ 目前的 \_ 使用者**。 若要判斷反映清單上的索引鍵是否已停用，請使用 [**RegQueryReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey) 函數。

交易式登錄作業中不應使用反映的索引鍵。 在交易期間寫入至反映的索引鍵，可能會導致交易失敗。 如需交易的詳細資訊，請參閱 [核心交易管理員](/windows/desktop/Ktm/kernel-transaction-manager-portal)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[登錄重新導向程式](registry-redirector.md)
</dt> <dt>

[Windows 中的登錄反映](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)
</dt> <dt>

[受 WOW64 影響的登錄機碼](shared-registry-keys.md)
</dt> </dl>

 

 