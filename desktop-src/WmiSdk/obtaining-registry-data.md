---
description: 您可以使用 WMI StdRegProv 類別及其方法，來取得或修改登錄資料。
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: 取得登錄資料
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986283"
---
# <a name="obtaining-registry-data"></a>取得登錄資料

您可以使用 WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 類別及其方法，來取得或修改登錄資料。 使用 Regedit 公用程式來查看及變更本機電腦上的登錄值時， **StdRegProv** 可讓您使用腳本或應用程式，將本機電腦和遠端電腦上的這類活動自動化。

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 包含可執行下列動作的方法：

-   驗證使用者的存取權限
-   建立、列舉和刪除登錄機碼
-   建立、列舉和刪除子機碼或命名值
-   讀取、寫入和刪除資料值

登錄資料是依最上層索引鍵上的子樹、索引鍵和子機碼來組織。 實際的資料值稱為「專案」或「命名值」。

這些子樹包括下列各項：

-   **HKEY \_類別 \_ 根目錄** (縮寫為 **HKCR**) 
-   **HKEY \_目前的 \_ 使用者** (**HKCU**) 
-   **HKEY \_本機 \_ 電腦** (**HKLM**) 
-   **HKEY \_ 使用者**
-   **HKEY \_ 目前的設定 \_**

例如，在登錄專案 **HKEY** \\ **SOFTWARE** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion** 中，HKEY 子樹是 **software**; 子機碼是 **Microsoft** 和 **DirectX**; 而命名值專案則是 **InstalledVersion**。

當特定索引鍵的變更發生時，就會發生 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ，但是專案不會識別值的變更，也不會透過變更低於指定的索引鍵來觸發此事件。 若要識別階層式索引鍵結構中任何位置的變更，請使用 [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)，而不會傳回所發生的特定值或索引鍵變更。 若要取得特定的專案值變更，請使用 [**registryvaluechangeeven**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent)，然後讀取專案以取得基準值。

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 只有可從 c + + 或腳本呼叫的方法，這與 Win32 類別結構不同。

下列程式碼範例示範如何使用 [**StdRegProv. EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) 方法列出登錄機碼下的所有 Microsoft 軟體子機碼。

**HKEY \_Microsoft 本機 \_ 電腦** \\ **軟體** \\ 


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 有不同的方法可讀取各種登錄專案值資料類型。 如果專案有未知的值，您可以呼叫 [**StdRegProv EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) 來列出它們。 下表列出 **StdRegProv** 方法與資料類型之間的對應。



| 方法                                                                                  | 資料類型           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**GetBinaryValue**](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | **REG \_ 二進位檔**     |
| [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**GetExpandedStringValue**](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | **REG \_ EXPAND \_ SZ** |
| [**GetMultiStringValue**](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | **REG \_ 多重 \_ SZ**  |
| [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

下表列出建立新的索引鍵或值，或變更現有索引鍵或值的對應方法。



| 方法                                                                                  | 資料類型           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | **REG \_ 二進位檔**     |
| [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | **REG \_ EXPAND \_ SZ** |
| [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | **REG \_ 多重 \_ SZ**  |
| [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

下列範例顯示如何從登錄機碼讀取系統事件記錄檔的來源清單。

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **目前的控制集** \\ **服務** \\ **Eventlog** \\ **系統**

請注意，multistring 值中的專案會被視為集合或陣列。


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



登錄提供者裝載于 LocalService，而不是 LocalSystem。 因此，不可能從子樹 **HKEY \_ 目前的 \_ 使用者** 取得資訊。 不過，在本機電腦上執行的腳本仍然可以存取 **HKEY \_ 目前的 \_ 使用者**。 您可以將裝載模型設定為遠端電腦上的 LocalSystem，但這會造成安全性風險，因為遠端電腦上的登錄很容易遭受惡意存取。 如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。

## <a name="examples"></a>範例

TechNet 資源庫上的 [讀取二進位登錄值](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript 程式碼範例會使用 WMI 來讀取二進位登錄值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 工作：登錄](wmi-tasks--registry.md)
</dt> </dl>

 

 
