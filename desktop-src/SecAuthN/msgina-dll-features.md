---
description: 如果您要撰寫 GINA 來取代 Microsoft standard GINA DLL (MSGina.dll) ，您可能會想要提供部分或所有標準 GINA 功能。
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: MSGina.dll 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf5d1e7e9dccf9581b27ea2fef3deb1c2c8aa218a1b0a711b7015134e1d2d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786747"
---
# <a name="msginadll-features"></a>MSGina.dll 功能

如果您要撰寫 [*GINA*](../secgloss/g-gly.md) 來取代 MICROSOFT STANDARD GINA DLL (MSGina.dll) ，您可能會想要提供部分或所有標準 GINA 功能。 以下是標準功能的清單，以及如何控制這些功能的簡短描述。

> [!Note]  
> Windows Vista 會忽略 GINA dll。

 

登錄機碼值控制許多這些標準 GINA 功能的可用性或行為。 除非另有說明，否則這些金鑰值屬於 Winlogon 登錄機碼，而且具有數值型別的 \[ REG \_ SZ \] 。 [*Winlogon*](../secgloss/w-gly.md)金鑰的實際路徑是：

**\\HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon**

-   **法律聲明對話方塊**

    在某些地方，有權存取工作站以登入並開始工作的任何人都是合法的，除非有通知指出系統僅供授權使用者使用。 此外，許多使用者都想要在一般登入之前顯示公司特定的訊息。 標準 GINA 會使用兩個 Winlogon 登錄機碼值，讓系統在登入之前顯示資訊。 如果有任一個索引鍵值存在且包含非 null 字串，則會在一般歡迎畫面之前顯示法律聲明對話方塊。 下表顯示這些機碼值的名稱。

    

    | 機碼值名稱         | 目錄                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **LegalNoticeCaption** | 要顯示為 [法律聲明] 對話方塊標題的字串 |
    | **LegalNoticeText**    | 要顯示為 [法律聲明] 對話方塊訊息的字串 |

    

     

-   **顯示最後的使用者名稱**

    根據預設，登入畫面會顯示最後一個使用者的名稱，以成功登入工作站。 這項功能是由 **DontDisplayLastUserName** 登錄機碼值所控制。 當此機碼值設定為1時，使用者名稱不會顯示在 [登入] 對話方塊中。

-   **自動登入**

    這項功能可讓系統在每次系統啟動時，自動登入使用者，方法是使用預設資訊，並停用 CTRL + ALT + DEL 登入方塊。

    這項功能會使用 Winlogon 金鑰的下列值。

    

    | 值                 | 目錄                                           |
    |-----------------------|----------------------------------------------------|
    | **AutoAdminLogon**    | 1                                                  |
    | **AutoLogonCount**    | 要自動登入的次數       |
    | **DefaultUserName**   | 使用者帳戶的名稱                       |
    | **DefaultDomainName** | 使用者帳戶所在網域的名稱 |

    

     

    如果 **AutoAdminLogon** 索引鍵值存在且包含一個，而且 **AutoLogonCount** 索引鍵值不存在，則每次目前使用者登出或系統重新開機時，就會發生自動登入。 要登入的帳戶是使用 **DefaultUserName** 和 **DefaultDomainName** 索引鍵值指定的。 您可以用兩種方式之一來指定帳戶的密碼。 如果電腦執行的是 Windows Server 2003 或 Windows XP 作業系統之一，則應該使用 [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata)函式，將密碼儲存為秘密。 如需詳細資訊，請參閱 [保護自動登入密碼](protecting-the-automatic-logon-password.md)。 另一種儲存密碼的方式，是以純文字形式儲存在 Winlogon 金鑰的 **DefaultPassword** 專案中;基於安全性考慮，應避免使用此技術。 如果您使用 **LsaStorePrivateData** 函式來儲存密碼，則請勿在 Winlogon 金鑰中提供 **DefaultPassword** 專案。

    如果 **AutoAdminLogon** 索引鍵值存在且包含一個值，而且如果 **AutoLogonCount** 索引鍵值存在且不是零，則 **AutoLogonCount** 將會決定所發生的自動登入次數。 每次重新開機系統時， **AutoLogonCount** 的值就會遞減1，直到達到零為止。 當 **AutoLogonCount** 到達零時，系統將不會自動登入任何帳戶， **AutoLogonCount** 索引鍵值和 **DefaultPassword** 索引鍵值（如果有使用的話）將會從登錄中刪除，而且 **AutoAdminLogon** 會設定為零。

    使用 **AutoAdminLogon** 有另外一點要注意：根據預設，MSGina.dll 會在 **AutoAdminLogon** 為1時檢查 SHIFT 鍵的狀態。 如果在開機過程中保留 SHIFT 鍵，MSGina.dll 將會忽略 **AutoAdminLogon** 金鑰值，並以互動方式提示使用者提供識別和驗證資訊。 當您要對專用應用程式進行偵錯工具時，這是很有用的功能。 若要停用 SHIFT 鍵的意義，請將 **IgnoreShiftOverride** 索引鍵值設定為一個。

-   **允許未經驗證的關機**

    您可以在 [登入] 對話方塊中，將預設 [*GINA*](../secgloss/g-gly.md) 設定為包含 [ **關閉** ] 按鈕。 這可讓使用者在不先登入的情況下關閉系統。 下列索引鍵值控制是否包含此按鈕。

    

    | 值                    | 描述                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | 其中一個包含按鈕;零以排除按鈕 |

    

     

-   **Userinit.exe 啟用**

    Userinit.exe 是由使用者登入 MSGina.dll 所執行的應用程式。 它會在新登入的使用者 [*內容*](../secgloss/c-gly.md) 和應用程式桌面上執行。 其目的是要設定使用者的環境，包括還原網路使用、建立字型和螢幕色彩等設定檔設定，以及執行登入腳本。 完成這些工作之後，Userinit.exe 會執行使用者 shell 程式。 Shell 程式會繼承 Userinit.exe 設定的環境。 Userinit.exe 執行的特定 shell 程式會儲存在 Winlogon 登錄機碼下的 **shell** 索引鍵值中。

    **Shell** 金鑰值可以包含要執行的程式清單（以逗號分隔）。 WindowsExplorer 是預設的 shell 程式，如果 **shell** 索引鍵值為 null 或不存在，就會執行此程式。 預設會列出 Windows 檔案總管。

-   **登入的安全性選項**

    登入時，如果使用者輸入 (SAS) 的 [*安全注意順序*](../secgloss/s-gly.md) ，使用者會看到 [安全性選項] 畫面。 其中所列的選項包括：

    -   關閉系統。
    -   登出。
    -   變更密碼。
    -   移至 [工作] 清單。
    -   鎖定工作站。

    當使用者登入時收到 SAS 事件時，取代 GINA 可以提供類似的選項。

 

 
