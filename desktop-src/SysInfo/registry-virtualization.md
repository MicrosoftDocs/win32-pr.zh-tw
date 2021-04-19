---
description: 登錄虛擬化是一種應用程式相容性技術，可讓具有全域影響的登錄寫入作業重新導向至每個使用者的位置。
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: 登錄虛擬化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642bda46b43fc0b4f7efa60cfcd9e2178643811f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991374"
---
# <a name="registry-virtualization"></a>登錄虛擬化

登錄 *虛擬化* 是一種應用程式相容性技術，可讓具有全域影響的登錄寫入作業重新導向至每個使用者的位置。 對於讀取或寫入登錄的應用程式而言，此重新導向是透明的。 從 Windows Vista 開始支援。

這種形式的虛擬化是暫時的應用程式相容性技術;Microsoft 打算將它從未來版本的 Windows 作業系統中移除，因為更多應用程式都與 Windows Vista 和更新版本的 Windows 相容。 因此，您的應用程式不一定會依賴系統中的登錄虛擬化行為。

虛擬化的目的只是為了提供現有應用程式的相容性。 針對 Windows Vista 和更新版本的 Windows 設計的應用程式不應寫入敏感性系統區域，也不應該依賴虛擬化來補救任何問題。 當更新現有的程式碼以在 Windows Vista 和更新版本的 Windows 上執行時，開發人員應該確保應用程式只會將資料儲存在每個使用者的位置，或是儲存在% alluserprofile% 內的電腦位置，以正確地使用存取控制清單 (ACL) 。

如需建立符合 UAC 規範之應用程式的詳細資訊，請參閱《 [Uac 開發人員指南》](/previous-versions/dotnet/articles/aa480150(v=msdn.10))。

## <a name="virtualization-overview"></a>虛擬化總覽

在 Windows Vista 之前，應用程式通常是由系統管理員執行。 因此，應用程式可以自由地存取系統檔案和登錄機碼。 如果這些應用程式是由標準使用者執行，則會因為存取權限不足而失敗。 Windows Vista 和更新版本的 Windows 會自動重新導向這些作業，藉此改善應用程式的應用程式相容性。 例如，全域存放區 (**HKEY \_ 本機 \_ 電腦 \\ 軟體** 的登錄操作，) 會重新導向至使用者設定檔中的每個使用者位置，稱為「*虛擬存放區*」 (**HKEY \_ USERS \\ <User SID> \_ 類別 \\ VirtualStore \\ 電腦 \\ 軟體**) 。

登錄虛擬化可以廣泛分類為下列類型：

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>開啟登錄虛擬化
</dt> <dd>

如果呼叫端沒有金鑰的寫入權限，而且嘗試開啟金鑰，則會以該呼叫者的最大允許存取來開啟金鑰。

如果登錄機 \_ 碼 \_ 不 \_ \_ 會針對機碼設定無訊息失敗旗標，則作業會失敗，且不會開啟金鑰。 如需詳細資訊，請參閱本主題稍後的「控制登錄虛擬化」。

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>撰寫登錄虛擬化
</dt> <dd>

如果呼叫端沒有金鑰的寫入存取權，並嘗試將值寫入其中或建立子機碼，則會將值寫入虛擬存放區。

例如，如果受限的使用者嘗試將值寫入下列機碼： **HKEY \_ 本機 \_ 電腦 \\ 軟體** \\ *AppKey1*，虛擬化會將寫入作業重新導向至 **HKEY \_ 使用者 \\ <User SID> \_ 類別 \\ VirtualStore \\ 電腦 \\ 軟體** \\ *AppKey1*。

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>讀取登錄虛擬化
</dt> <dd>

如果呼叫端從已虛擬化的機碼讀取，則登錄會顯示虛擬化值 (從虛擬存放區) 和 (從全域存放區) 到呼叫端的非虛擬值的合併觀點。

例如，假設 **HKEY \_ LOCAL \_ MACHINE \\ Software** \\ *AppKey1* 包含兩個值 V1 和 V2，而且限制使用者將值 V3 寫入機碼。 當使用者嘗試從此索引鍵讀取值時，合併的視圖會包含來自全域存放區的值 V1 和 V2，以及來自虛擬存放區的值 V3。

請注意，虛擬值會優先于全域值（如果有的話）。 在上述範例中，即使全域存儲區在此機碼底下具有值 V3，值 V3 仍會從虛擬存放區傳回給呼叫端。 如果要從虛擬存放區刪除 V3，則會從全域存放區傳回 V3。 換句話說，如果 V3 要從 **HKEY \_ USERS 類別中刪除 \\ <User SID> \_ \\ VirtualStore \\ Machine \\ software** \\ *AppKey1* 但是 **HKEY \_ LOCAL \_ Machine \\ software** \\ *AppKey1* 具有值 V3，則會從全域存放區傳回該值。

</dd> </dl>

## <a name="registry-virtualization-scope"></a>登錄虛擬化範圍

登錄虛擬化只會針對下列各項啟用：

-   32位的互動式進程。
-   **HKEY \_ 本機 \_ 電腦 \\ 軟體** 中的金鑰。
-   系統管理員可以寫入的金鑰。  (如果系統管理員無法寫入金鑰，則應用程式在舊版的 Windows 上會失敗，即使是由系統管理員執行也一樣。 ) 

已針對下列各項停用登錄虛擬化：

-   64位進程。
-   不是互動式的進程，例如服務。

    請注意，使用登錄作為處理序間通訊 () 服務 (或未) 啟用虛擬化之任何其他進程之間的 IPC 機制，而且如果金鑰已虛擬化，應用程式將無法正常運作。 比方說，如果防毒軟體服務根據應用程式所設定的值來更新其簽章檔案，服務將永遠不會更新其簽章檔案，因為服務會讀取全域存放區，但應用程式會寫入虛擬存放區。

-   模擬使用者的進程。 如果進程在模擬使用者時嘗試操作，該作業將不會虛擬化。
-   核心模式進程，例如驅動程式。
-   在資訊清單中指定 **並無 requestedexecutionlevel** 的進程。
-   **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 的金鑰和子機碼、 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ microsoft \\ Windows**，以及 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ microsoft \\ Windows NT**。

## <a name="controlling-registry-virtualization"></a>控制登錄虛擬化

除了在資訊清單中使用 **並無 requestedexecutionlevel** 來控制應用層級的虛擬化，系統管理員還可以針對 **HKEY \_ 本機 \_ 電腦 \\ 軟體** 中的金鑰，以每個金鑰為基礎來啟用或停用虛擬化。 若要這樣做，請使用 Reg.exe 命令列公用程式旗標選項以及下表所列的旗標。



| 旗標                         | 意義                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| REG 機碼不是無訊息的 \_ \_ \_ \_ 失敗 | 此旗標會停用開啟的登錄虛擬化。 如果設定此旗標，且已啟用虛擬化的金鑰上的開啟作業失敗，則登錄不會嘗試重新開啟金鑰。 如果清除此旗標，登錄會嘗試以允許的最大存取權來重新開啟金鑰， \_ 而不是所要求的存取權。                                                                   |
| REG 機碼不會 \_ \_ \_ 虛擬化   | 此旗標會停用寫入登錄虛擬化。 如果設定此旗標，且 create key 或 set value 作業失敗，因為呼叫端沒有父機碼的足夠存取權限，則登錄會導致作業失敗。 如果清除此旗標，登錄會嘗試寫入虛擬存放區中的機碼或值。 呼叫 \_ 端必須在父機碼上具有讀取權限。 |
| REG \_ KEY \_ 遞迴 \_ 旗標      | 如果設定此旗標，則會從父機碼傳播登錄虛擬旗標。 如果清除此旗標，則不會傳播登錄虛擬旗標。 變更此旗標只會影響在旗標變更之後所建立的新子索引鍵。 它不會針對現有的子機碼設定或清除這些旗標。                                                                  |



 

下列範例示範如何使用 Reg.exe 命令列公用程式搭配 FLAGS 選項，以查詢金鑰之虛擬化旗標的狀態。

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

每次在虛擬機器上啟用審核功能時，系統就會產生新的虛擬化 audit 事件，以指出金鑰已虛擬化 (一般的 audit 事件) 。 系統管理員可以使用這項資訊來監視系統上虛擬化的狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用使用者帳戶控制開始使用](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[瞭解及設定使用者帳戶控制](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[最低許可權環境中應用程式的開發人員最佳做法和指導方針](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
