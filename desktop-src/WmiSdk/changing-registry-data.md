---
description: 適用于 WMI 的系統登錄提供者類別 StdRegProv 具有執行下列動作的方法：
ms.assetid: d42248b3-2f96-4771-aee9-a0db139b149e
ms.tgt_platform: multiple
title: 變更登錄資料
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b51f3f18eb718dab7c79f31a4b2188dd7afa529
ms.sourcegitcommit: 3d9eb6638763fee8b87c378657458f814182e36c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106976398"
---
# <a name="changing-registry-data"></a>變更登錄資料

適用于 WMI 的 [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 類別 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 具有執行下列動作的方法：

-   建立或刪除登錄機碼。

    使用 [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) 或 [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov)。

-   建立或刪除命名值，這些值在索引鍵下時稱為專案。

    使用新值的名稱，以及 [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)、 [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)、 [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov)、 [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)或 [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) 來建立名為的值。 使用 [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) 來刪除命名值。

-   變更命名值。

    使用值的名稱和 Set 方法 (在上一個專案符號專案中識別) 來變更索引鍵下現有的已命名值。 您必須知道值的名稱才能加以變更。 如果您不知道索引鍵下的值名稱，請使用 [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) 方法來取得名稱。

本主題將討論下列各節：

-   [使用 VBScript 建立登錄機碼](#creating-a-registry-key-using-vbscript)
-   [使用 PowerShell 和 VBScript 建立命名登錄值](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a>使用 VBScript 建立登錄機碼

因為登錄是作業系統、應用程式和服務的中央設定資料庫，當您將變更寫入登錄值或刪除金鑰時，請特別小心。

> [!Note]  
> 您無法監視 **HKEY \_ 目前 \_ 使用者 (HKCU)** 的 **HKEY \_ 類別 \_ 根** 機碼。 不建議監視 **HKEY \_ 使用者** ，因為載入 hive 時，子機碼會出現並消失。

 

下列程式碼範例示範如何建立新的登錄機碼和子機碼。


```VB
HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set ObjRegistry = GetObject("winmgmts:{impersonationLevel = impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strPath = "SOFTWARE\MyKey\MySubKey"

Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

If Return <> 0 Then
    WScript.Echo "The operation failed." & Err.Number
    WScript.Quit
Else
    wScript.Echo "New registry key created" & VBCRLF & "HKLM\SOFTWARE\MYKey\"

End If
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.CreateKey($HKEY_LOCAL_MACHINE, $strPath)
```





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a>使用 PowerShell 和 VBScript 建立命名登錄值

下列程式碼範例示範如何在先前的腳本所建立的 **HKEY \_ 本機 \_ 電腦** \\ **SOFTWARE** \\ **MyKey** \\ **MySubKey** 機碼下，建立名為 MultiStringValue 的命名值。 腳本會呼叫 [**StdRegProv**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) ，將字串值寫入至新的命名值。


```VB
const HKEY_LOCAL_MACHINE = &H80000002 
strComputer = "."

Set objRegistry = _
    GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\MyKey\MySubKey"
strValueName = "MultiStringValue"
arrStringValues = Array("one", "two","three", "four")

objRegistry.SetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues

' Read the values that were just written
objRegistry.GetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues   

For Each strValue in arrStringValues
    WScript.Echo strValue 
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$strValueName = "MultiStringValue"
$arrStringValues = @("one", "two","three", "four")

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName, $arrStringValues)

$multiValues = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName)
$multiValues.sValue
```

使用 WMI 時，您無法在登錄機碼上設定存取安全性。 不過， [**StdRegProv. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) 方法會將目前使用者的安全性設定與登錄機碼上的安全描述項進行比較，以判斷使用者是否具有特定的許可權，例如 **金鑰 \_ 集 \_ 值**。
