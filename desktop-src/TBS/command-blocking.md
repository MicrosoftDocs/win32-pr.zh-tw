---
title: 命令封鎖
description: 為了保留作業的完整性，平臺上的軟體不允許執行某些 TPM 命令。
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2020
ms.locfileid: "104374892"
---
# <a name="command-blocking"></a>命令封鎖

為了保留作業的完整性，平臺上的軟體不允許執行某些 TPM 命令。 例如，某些命令只能由系統軟體執行。 當 TBS 封鎖某個命令時，會適當地傳回錯誤。 根據預設，TBS 會封鎖可能會影響系統隱私權、安全性和穩定性的命令。 此 TB 也假設軟體堆疊的其他部分可能會限制特定命令的存取權給已授權的實體。

針對 TPM 1.2 版命令，有三個封鎖的命令清單：由群組原則控制的清單、由本機系統管理員控制的清單，以及預設清單。 如果 TPM 命令位於任何清單上，則會予以封鎖。 不過，有群組原則旗標可允許 TB 忽略本機清單和預設清單。 您可以直接編輯或透過群組原則物件編輯器來存取群組原則旗標。

> [!Note]  
> 升級至作業系統之後，不會保留本機封鎖的命令清單。 系統會保留封鎖在群組原則清單上的命令。

 

針對 TPM 2.0 版命令，會反轉封鎖的邏輯;它會使用允許的命令清單。 當第一次建立清單時，此邏輯會自動封鎖未知的命令。 當 Windows 版本發行之後，將命令新增至 TPM 規格時，會自動封鎖這些新的命令。 只有登錄的更新會將這些新的命令新增至允許的命令清單。

從 Windows 10 1809 (Windows Server 2019) ，就無法再透過登錄設定來操作允許的 TPM 2.0 命令。 針對這些 Windows 10 版本，TPM 驅動程式中會修正允許的 TPM 2.0 命令。 TPM 1.2 命令仍可透過登錄變更來封鎖和解除封鎖。 

## <a name="direct-registry-access"></a>Direct Registry 存取

群組原則旗標位於登錄機碼 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Tpm** \\ **BlockedCommands**。

若要判斷哪些清單應用來封鎖 TPM 命令，有兩個 **DWORD** 值會用來做為布林值旗標：

-   "IgnoreDefaultList"

    如果 set (值存在且為非零值) ，則 TB 會忽略預設封鎖的命令清單。

-   "IgnoreLocalList"

    如果 set (值存在且為非零值) ，則 TB 會忽略本機封鎖的命令清單。

## <a name="group-policy-object-editor"></a>群組原則物件編輯器

**存取群組原則物件編輯器**

1.  按一下 [啟動]。
2.  按一下 **[執行]** 。
3.  在 [開啟舊檔] 方塊中，輸入 **gpedit.msc**。 按一下 [確定]  。 群組原則物件編輯器隨即開啟。
4.  展開 [ **電腦** 設定]。
5.  展開 [ **系統管理範本**]。
6.  展開 [ **系統**]。
7.  展開 [ **信賴平臺模組服務**]。

您可以直接在下列位置編輯特定封鎖 TPM 1.2 命令的清單。

-   群組原則清單：

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   本機清單：

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   預設清單：

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

在每個登錄機碼下，都有一個登錄值的清單，也就是 REG \_ SZ 型別。 每個值都代表封鎖的 TPM 命令。 每個登錄機碼都有一個 [值名稱] 欄位和 [值資料] 欄位。 這兩個欄位 ( 「值名稱」和「值資料」 ) ，應完全符合要封鎖之 TPM 命令序數的十進位值。

您可以直接在下列位置編輯特定的允許 TPM 2.0 命令清單。 在登錄機碼底下，有一個登錄值的登錄值清單 \_ 。 每個值都代表一個允許的 TPM 2.0 命令。 每個登錄值都有 **名稱** 和 **值** 欄位。 **名稱** 符合應允許的十六進位 TPM 2.0 命令序數。 如果允許命令， **值** 的值會是1。 如果命令序數不存在或值為0，則會封鎖此命令。

-   預設清單：

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

針對 Windows 8、Windows Server 2012 和更新版本， **BlockedCommands** 和 **AllowedW8Commands** 登錄機碼分別會判斷系統管理員帳戶的封鎖或允許 TPM 命令。 使用者帳戶會在 **BlockedUserCommands** 和 **AllowedW8UserCommands** 登錄機碼中分別有封鎖或允許的 TPM 命令清單。 在 Windows 10 1607 版中，已針對 AppContainer 應用程式導入了新的登錄機碼： **BlockedAppContainerCommands** 和 **AllowedW8AppContainerCommands**。

 

 




