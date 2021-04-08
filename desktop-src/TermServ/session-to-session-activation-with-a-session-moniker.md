---
title: 使用會話標記的會話對會話啟用
description: 會話對會話啟用 (也稱為跨會話啟用) 可讓用戶端進程啟動 (在指定的會話) 本機伺服器處理常式。
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682937"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a>使用會話標記的會話對會話啟用

會話對會話啟用 (也稱為跨會話啟用) 可讓用戶端進程啟動 (在指定的會話) 本機伺服器處理常式。 這項功能適用于設定為在互動式使用者的安全性內容中執行的應用程式，也稱為「RunAs 互動式使用者」物件啟用模式。 如需安全性環境的詳細資訊，請參閱 [用戶端的安全性內容](/windows/desktop/SecAuthZ/the-client-security-context)。

分散式 COM (DCOM) 使用系統提供的 [會話標記](session-monikers.md)，啟用每個會話的物件啟用。 其他系統提供的標記包括檔案的 [名字](../com/file-monikers.md)、 [專案的名字](../com/item-monikers.md)、泛型 [複合](../com/composite-monikers.md)標記、 [反](../com/anti-monikers.md)標記、 [指標](../com/pointer-monikers.md)標記以及 [URL 的名字](../com/url-monikers.md)。

若要能夠使用會話的標記，必須將 DCOM 應用程式設定為以互動式使用者的形式執行。 您可以使用 [元件服務] 系統管理工具、查看 DCOM 應用程式的內容，然後在 [身分 **識別**] 索引標籤上選取 **互動式使用者**，來設定此選項。如需有關將 DCOM 應用程式設定為在遠端桌面服務環境中以互動式使用者身分執行的可能安全性風險的詳細資訊，請參閱平臺軟體發展工具組 (SDK) 之 COM 檔的「應用程式識別 (COM) 」一節。

如果選取任何其他類型的使用者來執行應用程式，應用程式將會忽略會話的標記。 COM + 伺服器應用程式也會忽略會話的標記。 如需有關選取要執行應用程式之使用者類型之其他方法的詳細資訊，請參閱 Platform SDK 中的 COM 檔。

若要建立會話的標記，您必須使用指定進程伺服器類別識別碼的類別指定識別碼，撰寫遠端桌面服務會話的會話識別碼。

**若要建立會話的標記**

1.  使用下列語法，將類別名字標記的顯示名稱加上前置詞，並將其顯示為會話的名字：

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    其中 *數位* 代表將啟動伺服器進程之會話的會話識別碼，而 *類別識別碼* 代表伺服器的類別識別碼。 請注意，會話識別碼是以10為底數的數位。

    若為執行 Windows XP 或更新版本的電腦，使用下列語法將會導致 COM 將啟用傳送至目前作用中的實體主控台會話（不論其會話識別碼為何）：

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  建立會話的標記之後，您可以將結果傳遞給 [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) 函數或 [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) 函數。

您可以使用會話的標記，就像使用任何其他的標記一樣。

如需示範如何在指定的會話上啟動本機伺服器進程的程式碼範例，請參閱 [使用會話的標記](using-a-session-moniker.md)。

如需物件啟用、系統提供的名字和類別標記的詳細資訊，請參閱 Platform SDK 中的 COM 檔。

> [!Note]  
> 跨會話建立的進程具有環境區塊大小的上限。 這項限制約為 4 KB，但可能較大或較小，這取決於建立程式所需的其他資訊 (例如) 的新進程的檔案名、目錄和參數。

 

 

 