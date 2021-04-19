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
# <a name="obtaining-registry-data"></a><span data-ttu-id="e1164-103">取得登錄資料</span><span class="sxs-lookup"><span data-stu-id="e1164-103">Obtaining Registry Data</span></span>

<span data-ttu-id="e1164-104">您可以使用 WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 類別及其方法，來取得或修改登錄資料。</span><span class="sxs-lookup"><span data-stu-id="e1164-104">You can obtain or modify registry data by using the WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class and its methods.</span></span> <span data-ttu-id="e1164-105">使用 Regedit 公用程式來查看及變更本機電腦上的登錄值時， **StdRegProv** 可讓您使用腳本或應用程式，將本機電腦和遠端電腦上的這類活動自動化。</span><span class="sxs-lookup"><span data-stu-id="e1164-105">While use the Regedit utility to view and change registry values on the local computer, **StdRegProv** allows you to use a script or application to automate such activities on the local computer and remote computers.</span></span>

<span data-ttu-id="e1164-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 包含可執行下列動作的方法：</span><span class="sxs-lookup"><span data-stu-id="e1164-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contains methods to do the following:</span></span>

-   <span data-ttu-id="e1164-107">驗證使用者的存取權限</span><span class="sxs-lookup"><span data-stu-id="e1164-107">Verify the access permissions for a user</span></span>
-   <span data-ttu-id="e1164-108">建立、列舉和刪除登錄機碼</span><span class="sxs-lookup"><span data-stu-id="e1164-108">Create, enumerate, and delete registry keys</span></span>
-   <span data-ttu-id="e1164-109">建立、列舉和刪除子機碼或命名值</span><span class="sxs-lookup"><span data-stu-id="e1164-109">Create, enumerate, and delete subkeys or named values</span></span>
-   <span data-ttu-id="e1164-110">讀取、寫入和刪除資料值</span><span class="sxs-lookup"><span data-stu-id="e1164-110">Read, write, and delete data values</span></span>

<span data-ttu-id="e1164-111">登錄資料是依最上層索引鍵上的子樹、索引鍵和子機碼來組織。</span><span class="sxs-lookup"><span data-stu-id="e1164-111">Registry data is organized by subtrees, keys, and subkeys nested under a top level key.</span></span> <span data-ttu-id="e1164-112">實際的資料值稱為「專案」或「命名值」。</span><span class="sxs-lookup"><span data-stu-id="e1164-112">The actual data values are called entries or named values.</span></span>

<span data-ttu-id="e1164-113">這些子樹包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="e1164-113">The subtrees include the following:</span></span>

-   <span data-ttu-id="e1164-114">**HKEY \_類別 \_ 根目錄** (縮寫為 **HKCR**) </span><span class="sxs-lookup"><span data-stu-id="e1164-114">**HKEY\_CLASSES\_ROOT** (abbreviated as **HKCR**)</span></span>
-   <span data-ttu-id="e1164-115">**HKEY \_目前的 \_ 使用者** (**HKCU**) </span><span class="sxs-lookup"><span data-stu-id="e1164-115">**HKEY\_CURRENT\_USER** (**HKCU**)</span></span>
-   <span data-ttu-id="e1164-116">**HKEY \_本機 \_ 電腦** (**HKLM**) </span><span class="sxs-lookup"><span data-stu-id="e1164-116">**HKEY\_LOCAL\_MACHINE** (**HKLM**)</span></span>
-   <span data-ttu-id="e1164-117">**HKEY \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="e1164-117">**HKEY\_USERS**</span></span>
-   <span data-ttu-id="e1164-118">**HKEY \_ 目前的設定 \_**</span><span class="sxs-lookup"><span data-stu-id="e1164-118">**HKEY\_CURRENT\_CONFIG**</span></span>

<span data-ttu-id="e1164-119">例如，在登錄專案 **HKEY** \\ **SOFTWARE** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion** 中，HKEY 子樹是 **software**; 子機碼是 **Microsoft** 和 **DirectX**; 而命名值專案則是 **InstalledVersion**。</span><span class="sxs-lookup"><span data-stu-id="e1164-119">For example, in the registry entry **HKEY**\\**SOFTWARE**\\**Microsoft**\\**DirectX**\\**InstalledVersion**, the HKEY subtree is **SOFTWARE**; the subkeys are **Microsoft** and **DirectX**; and the named value entry is **InstalledVersion**.</span></span>

<span data-ttu-id="e1164-120">當特定索引鍵的變更發生時，就會發生 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) ，但是專案不會識別值的變更，也不會透過變更低於指定的索引鍵來觸發此事件。</span><span class="sxs-lookup"><span data-stu-id="e1164-120">A [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) occurs when a change to a specific key occurs, but the entry does not identify how the values change nor will this event be triggered by changes below the specified key.</span></span> <span data-ttu-id="e1164-121">若要識別階層式索引鍵結構中任何位置的變更，請使用 [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)，而不會傳回所發生的特定值或索引鍵變更。</span><span class="sxs-lookup"><span data-stu-id="e1164-121">To identify changes anywhere in a hierarchical key structure, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), which does not return specific values or key changes that occur.</span></span> <span data-ttu-id="e1164-122">若要取得特定的專案值變更，請使用 [**registryvaluechangeeven**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent)，然後讀取專案以取得基準值。</span><span class="sxs-lookup"><span data-stu-id="e1164-122">To obtain a specific entry value change, use the [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), and then read the entry to obtain a baseline value.</span></span>

<span data-ttu-id="e1164-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 只有可從 c + + 或腳本呼叫的方法，這與 Win32 類別結構不同。</span><span class="sxs-lookup"><span data-stu-id="e1164-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) only has methods that can be called from C++ or script, which is different from the Win32 class structure.</span></span>

<span data-ttu-id="e1164-124">下列程式碼範例示範如何使用 [**StdRegProv. EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) 方法列出登錄機碼下的所有 Microsoft 軟體子機碼。</span><span class="sxs-lookup"><span data-stu-id="e1164-124">The following code example shows how to use the [**StdRegProv.EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) method to list all of the Microsoft software subkeys under the registry key.</span></span>

<span data-ttu-id="e1164-125">**HKEY \_Microsoft 本機 \_ 電腦** \\ **軟體** \\ </span><span class="sxs-lookup"><span data-stu-id="e1164-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**</span></span>


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





<span data-ttu-id="e1164-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) 有不同的方法可讀取各種登錄專案值資料類型。</span><span class="sxs-lookup"><span data-stu-id="e1164-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) has different methods for reading the various registry entry value data types.</span></span> <span data-ttu-id="e1164-127">如果專案有未知的值，您可以呼叫 [**StdRegProv EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) 來列出它們。</span><span class="sxs-lookup"><span data-stu-id="e1164-127">If the entry has unknown values, then you can call [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) to list them.</span></span> <span data-ttu-id="e1164-128">下表列出 **StdRegProv** 方法與資料類型之間的對應。</span><span class="sxs-lookup"><span data-stu-id="e1164-128">The following table lists the correspondence between **StdRegProv** methods and the data types.</span></span>



| <span data-ttu-id="e1164-129">方法</span><span class="sxs-lookup"><span data-stu-id="e1164-129">Method</span></span>                                                                                  | <span data-ttu-id="e1164-130">資料類型</span><span class="sxs-lookup"><span data-stu-id="e1164-130">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="e1164-131">**GetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="e1164-131">**GetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="e1164-132">**REG \_ 二進位檔**</span><span class="sxs-lookup"><span data-stu-id="e1164-132">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="e1164-133">**GetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="e1164-133">**GetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="e1164-134">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e1164-134">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="e1164-135">**GetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1164-135">**GetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="e1164-136">**REG \_ EXPAND \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e1164-136">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="e1164-137">**GetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1164-137">**GetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="e1164-138">**REG \_ 多重 \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e1164-138">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="e1164-139">**GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1164-139">**GetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="e1164-140">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e1164-140">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="e1164-141">下表列出建立新的索引鍵或值，或變更現有索引鍵或值的對應方法。</span><span class="sxs-lookup"><span data-stu-id="e1164-141">The following table lists the corresponding methods for creating new keys or values, or changing existing ones.</span></span>



| <span data-ttu-id="e1164-142">方法</span><span class="sxs-lookup"><span data-stu-id="e1164-142">Method</span></span>                                                                                  | <span data-ttu-id="e1164-143">資料類型</span><span class="sxs-lookup"><span data-stu-id="e1164-143">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="e1164-144">**SetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="e1164-144">**SetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="e1164-145">**REG \_ 二進位檔**</span><span class="sxs-lookup"><span data-stu-id="e1164-145">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="e1164-146">**SetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="e1164-146">**SetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="e1164-147">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e1164-147">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="e1164-148">**SetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1164-148">**SetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="e1164-149">**REG \_ EXPAND \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e1164-149">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="e1164-150">**SetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1164-150">**SetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="e1164-151">**REG \_ 多重 \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e1164-151">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="e1164-152">**SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1164-152">**SetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="e1164-153">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e1164-153">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="e1164-154">下列範例顯示如何從登錄機碼讀取系統事件記錄檔的來源清單。</span><span class="sxs-lookup"><span data-stu-id="e1164-154">The following example shows how to read the list of sources for the system event log from the registry key.</span></span>

<span data-ttu-id="e1164-155">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **目前的控制集** \\ **服務** \\ **Eventlog** \\ **系統**</span><span class="sxs-lookup"><span data-stu-id="e1164-155">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Services**\\**Eventlog**\\**System**</span></span>

<span data-ttu-id="e1164-156">請注意，multistring 值中的專案會被視為集合或陣列。</span><span class="sxs-lookup"><span data-stu-id="e1164-156">Note that the items in the multistring value are treated as a collection or array.</span></span>


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



<span data-ttu-id="e1164-157">登錄提供者裝載于 LocalService，而不是 LocalSystem。</span><span class="sxs-lookup"><span data-stu-id="e1164-157">The registry provider is hosted in LocalService—not the LocalSystem.</span></span> <span data-ttu-id="e1164-158">因此，不可能從子樹 **HKEY \_ 目前的 \_ 使用者** 取得資訊。</span><span class="sxs-lookup"><span data-stu-id="e1164-158">Therefore, obtaining information remotely from the subtree **HKEY\_CURRENT\_USER** is not possible.</span></span> <span data-ttu-id="e1164-159">不過，在本機電腦上執行的腳本仍然可以存取 **HKEY \_ 目前的 \_ 使用者**。</span><span class="sxs-lookup"><span data-stu-id="e1164-159">However, scripts run on the local computer can still access **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="e1164-160">您可以將裝載模型設定為遠端電腦上的 LocalSystem，但這會造成安全性風險，因為遠端電腦上的登錄很容易遭受惡意存取。</span><span class="sxs-lookup"><span data-stu-id="e1164-160">You can set the hosting model to LocalSystem on a remote machine, but that is a security risk because the registry on the remote machine is vulnerable to hostile access.</span></span> <span data-ttu-id="e1164-161">如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="e1164-161">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e1164-162">範例</span><span class="sxs-lookup"><span data-stu-id="e1164-162">Examples</span></span>

<span data-ttu-id="e1164-163">TechNet 資源庫上的 [讀取二進位登錄值](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript 程式碼範例會使用 WMI 來讀取二進位登錄值。</span><span class="sxs-lookup"><span data-stu-id="e1164-163">The [Read a Binary Registry Value](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript code example on TechNet Gallery uses WMI to read a binary registry value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1164-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1164-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1164-165">WMI 工作：登錄</span><span class="sxs-lookup"><span data-stu-id="e1164-165">WMI Tasks: Registry</span></span>](wmi-tasks--registry.md)
</dt> </dl>

 

 
