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
# <a name="changing-registry-data"></a><span data-ttu-id="93fa4-103">變更登錄資料</span><span class="sxs-lookup"><span data-stu-id="93fa4-103">Changing Registry Data</span></span>

<span data-ttu-id="93fa4-104">適用于 WMI 的 [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider) 類別 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 具有執行下列動作的方法：</span><span class="sxs-lookup"><span data-stu-id="93fa4-104">The [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) class [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) for WMI has methods that do the following:</span></span>

-   <span data-ttu-id="93fa4-105">建立或刪除登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="93fa4-105">Create or delete registry keys.</span></span>

    <span data-ttu-id="93fa4-106">使用 [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) 或 [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov)。</span><span class="sxs-lookup"><span data-stu-id="93fa4-106">Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) or [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span></span>

-   <span data-ttu-id="93fa4-107">建立或刪除命名值，這些值在索引鍵下時稱為專案。</span><span class="sxs-lookup"><span data-stu-id="93fa4-107">Create or delete named values, which are called entries when they are under keys.</span></span>

    <span data-ttu-id="93fa4-108">使用新值的名稱，以及 [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)、 [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)、 [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov)、 [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)或 [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) 來建立名為的值。</span><span class="sxs-lookup"><span data-stu-id="93fa4-108">Use the name of a new value and [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov), or [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) to create a named value.</span></span> <span data-ttu-id="93fa4-109">使用 [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) 來刪除命名值。</span><span class="sxs-lookup"><span data-stu-id="93fa4-109">Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) to delete a named value.</span></span>

-   <span data-ttu-id="93fa4-110">變更命名值。</span><span class="sxs-lookup"><span data-stu-id="93fa4-110">Change named values.</span></span>

    <span data-ttu-id="93fa4-111">使用值的名稱和 Set 方法 (在上一個專案符號專案中識別) 來變更索引鍵下現有的已命名值。</span><span class="sxs-lookup"><span data-stu-id="93fa4-111">Use the name of a value and the Set methods (identified in the previous bulleted item) to change existing named values under a key.</span></span> <span data-ttu-id="93fa4-112">您必須知道值的名稱才能加以變更。</span><span class="sxs-lookup"><span data-stu-id="93fa4-112">You must know the name of a value to change it.</span></span> <span data-ttu-id="93fa4-113">如果您不知道索引鍵下的值名稱，請使用 [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) 方法來取得名稱。</span><span class="sxs-lookup"><span data-stu-id="93fa4-113">If you do not know the value names under a key, use the [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) method to obtain the names.</span></span>

<span data-ttu-id="93fa4-114">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="93fa4-114">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="93fa4-115">使用 VBScript 建立登錄機碼</span><span class="sxs-lookup"><span data-stu-id="93fa4-115">Creating a Registry Key Using VBScript</span></span>](#creating-a-registry-key-using-vbscript)
-   [<span data-ttu-id="93fa4-116">使用 PowerShell 和 VBScript 建立命名登錄值</span><span class="sxs-lookup"><span data-stu-id="93fa4-116">Creating a Named Registry Value Using PowerShell and VBScript</span></span>](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a><span data-ttu-id="93fa4-117">使用 VBScript 建立登錄機碼</span><span class="sxs-lookup"><span data-stu-id="93fa4-117">Creating a Registry Key Using VBScript</span></span>

<span data-ttu-id="93fa4-118">因為登錄是作業系統、應用程式和服務的中央設定資料庫，當您將變更寫入登錄值或刪除金鑰時，請特別小心。</span><span class="sxs-lookup"><span data-stu-id="93fa4-118">Because the registry is the central configuration database for the operating system, applications, and services, use caution when you write changes to registry values or delete keys.</span></span>

> [!Note]  
> <span data-ttu-id="93fa4-119">您無法監視 **HKEY \_ 目前 \_ 使用者 (HKCU)** 的 **HKEY \_ 類別 \_ 根** 機碼。</span><span class="sxs-lookup"><span data-stu-id="93fa4-119">You cannot monitor the **HKEY\_CLASSES\_ROOT** subkey of **HKEY\_CURRENT\_USER(HKCU)**.</span></span> <span data-ttu-id="93fa4-120">不建議監視 **HKEY \_ 使用者** ，因為載入 hive 時，子機碼會出現並消失。</span><span class="sxs-lookup"><span data-stu-id="93fa4-120">Monitoring **HKEY\_USERS** is not recommended because the subkeys appear and disappear as hives are loaded.</span></span>

 

<span data-ttu-id="93fa4-121">下列程式碼範例示範如何建立新的登錄機碼和子機碼。</span><span class="sxs-lookup"><span data-stu-id="93fa4-121">The following code examples show how to create a new registry key and a subkey.</span></span>


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





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a><span data-ttu-id="93fa4-122">使用 PowerShell 和 VBScript 建立命名登錄值</span><span class="sxs-lookup"><span data-stu-id="93fa4-122">Creating a Named Registry Value Using PowerShell and VBScript</span></span>

<span data-ttu-id="93fa4-123">下列程式碼範例示範如何在先前的腳本所建立的 **HKEY \_ 本機 \_ 電腦** \\ **SOFTWARE** \\ **MyKey** \\ **MySubKey** 機碼下，建立名為 MultiStringValue 的命名值。</span><span class="sxs-lookup"><span data-stu-id="93fa4-123">The following code example shows how to create a named value called **MultiStringValue** under the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**MyKey**\\**MySubKey** key that the previous script creates.</span></span> <span data-ttu-id="93fa4-124">腳本會呼叫 [**StdRegProv**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) ，將字串值寫入至新的命名值。</span><span class="sxs-lookup"><span data-stu-id="93fa4-124">The script calls [**StdRegProv.SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) to write string values to a new named value.</span></span>


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

<span data-ttu-id="93fa4-125">使用 WMI 時，您無法在登錄機碼上設定存取安全性。</span><span class="sxs-lookup"><span data-stu-id="93fa4-125">Using WMI, you cannot set access security on a registry key.</span></span> <span data-ttu-id="93fa4-126">不過， [**StdRegProv. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) 方法會將目前使用者的安全性設定與登錄機碼上的安全描述項進行比較，以判斷使用者是否具有特定的許可權，例如 **金鑰 \_ 集 \_ 值**。</span><span class="sxs-lookup"><span data-stu-id="93fa4-126">However, the [**StdRegProv.CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) method compares the security settings of the current user to the security descriptor on a registry key to determine if the user has a specific permission, such as **KEY\_SET\_VALUE**.</span></span>
