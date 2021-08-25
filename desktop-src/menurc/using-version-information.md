---
title: 使用版本資訊
description: 本主題討論如何使用版本資訊函數。
ms.assetid: 447b57c9-9e94-4a28-897e-f7b87d9cb25a
keywords:
- 資源，版本資訊
- 版本資訊
- 安裝檔案資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0447bc1dfc3b2d5d5006bb5ff9ca3e9fa8f3d488e9b5621acb932c843fc3630f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846988"
---
# <a name="using-version-information"></a>使用版本資訊

安裝程式通常具有下列目標：

-   將檔案放在正確的位置。
-   若要在安裝程式中將現有的檔案取代為相當不同的版本（例如，以英文檔案取代德文語言的檔案，或以較舊的檔案取代較新的檔案），請通知使用者。

撰寫安裝程式時，每個檔案都必須有下列資訊：

-   檔案的名稱和位置 (稱為原始程式檔) 。
-   使用者硬碟上對等檔案的名稱 (稱為目的地檔案) 。 此名稱通常與安裝磁片上的檔案名相同。
-   檔案的共用狀態-也就是，檔案是否私用於正在安裝的應用程式，或是可由多個應用程式共用。

安裝程式可以使用 [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) 函式來判斷應該將檔案複製到磁片上的位置。 此函式也可用來指定檔案是否為應用程式的私用或可共用。 如果在尋找檔案時發生問題， **VerFindFile** 會傳回錯誤值。 例如，如果系統使用目的地檔案， **VerFindFile** 會傳回 **VFF \_ FILEINUSE**。 安裝程式必須通知使用者問題，並回應使用者的決策以繼續或結束安裝。

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)函式會將原始程式檔複製到 [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)所指定之目錄中的暫存檔案。 如有必要， **VerInstallFile** 會使用資料解壓縮程式庫中的函式來展開檔案。

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) 會比較暫存檔案的版本資訊與目的地檔案的版本資訊。 如果兩個不同， **VerInstallFile** 會傳回一或多個錯誤值。 例如，如果暫存檔比目的地檔案還舊，則會傳回 **VIF \_ SRCOLD** ，如果檔案具有不同的語言識別項或字碼頁值，則會傳回 **VIF \_ DIFFLANG** 。 安裝程式必須通知使用者問題，並回應使用者的決策以繼續或結束安裝。

某些 [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) 錯誤可復原。 也就是說，安裝程式可以再次呼叫 **VerInstallFile** ，指定 **VIFF \_ FORCEINSTALL** 選項，以安裝檔案，而不論版本是否衝突。 如果 **VerInstallFile** 傳回 **VIF \_ TEMPFILE** ，且使用者選擇不強制安裝，則安裝程式應該刪除暫存檔案。

嘗試強制安裝時， [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)可能會發生無法恢復的錯誤，即使先前的錯誤尚未存在也是一樣。 例如，檔案可能會在安裝程式嘗試強制安裝之前，由另一位使用者鎖定。 如果安裝程式嘗試在無法復原的錯誤之後強制安裝， **VerInstallFile** 就會失敗。 安裝程式必須包含可從這類錯誤中復原的常式。

建議的解決方案是顯示對話方塊，其中包含 [ **安裝**]、[ **略過**] 和 [ **全部安裝**] 按鈕。  (另一個方案是具有 [**是**]、 **[是]、[全部]、[****略過**] 和 [**取消**] 按鈕的對話方塊。 ) [**全部安裝**] 按鈕應該會在 [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)的所有後續使用中包含 **VIFF \_ FORCEINSTALL** 選項，以防止安裝程式提示使用者有關類似的錯誤。 針對無法恢復的錯誤，應該停用 [ **安裝** 和 **安裝所有** ] 按鈕。

若要向使用者顯示有用的錯誤訊息，安裝程式通常必須從衝突檔案的版本資源中取出資訊。 安裝程式有四個可用於此用途的功能：

-   [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)
-   [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)
-   [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
-   [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)

[**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) 會傳回版本資訊的大小。 [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) 會使用 **GetFileVersionInfoSize** 抓取的資訊，以抓取包含版本資訊的結構。 [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) 會從該結構抓取特定的成員。

例如，如果 [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) 傳回 **VIF \_ DIFFTYPE** 錯誤，則安裝程式應該在暫存和目的地檔案上使用 [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)、 [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)和 [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) 函數，以取得每個檔案的一般類型。 如果檔案的語言發生衝突，安裝程式也應該使用 [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea) 將二進位語言識別項轉譯成語言的文字標記法。  (例如，0x040C 會轉譯為 "法文" 字串。) 

如果 [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) 傳回檔案錯誤（例如 **VIF \_ ACCESSVIOLATION**），則安裝程式應該使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函式來取得最新的錯誤值。 程式應該將此值轉譯成可向使用者顯示的資訊訊息。 程式不能在呼叫 **VerInstallFile** 和 **GetLastError** 之間產生控制權。

 

 