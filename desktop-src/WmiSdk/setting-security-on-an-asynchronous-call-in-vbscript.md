---
description: 最常呼叫的效能通常適用于大部分的情況。
ms.assetid: f665fc60-68bd-495d-a441-e3a9473f9d89
ms.tgt_platform: multiple
title: 在 VBScript 中設定非同步呼叫的安全性
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 972947e0cb4f5d385e4d2d27b7c14298771ac4e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994542"
---
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a><span data-ttu-id="20974-103">在 VBScript 中設定非同步呼叫的安全性</span><span class="sxs-lookup"><span data-stu-id="20974-103">Setting Security on an Asynchronous Call in VBScript</span></span>

<span data-ttu-id="20974-104">最 [*常呼叫的*](gloss-s.md) 效能通常適用于大部分的情況。</span><span class="sxs-lookup"><span data-stu-id="20974-104">The performance of [*semisynchronous*](gloss-s.md) calls is usually adequate for most situations.</span></span> <span data-ttu-id="20974-105">非同步呼叫通常不是腳本的建議作法。</span><span class="sxs-lookup"><span data-stu-id="20974-105">Asynchronous calls are generally not a recommended practice for scripts.</span></span> <span data-ttu-id="20974-106">但是，如果必須進行非同步呼叫，就可以將登錄值設定為強制 WMI 在非同步呼叫上執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="20974-106">However, if asynchronous calls must be made, a registry value can be set to force WMI to perform access checks on asynchronous calls.</span></span>


<span data-ttu-id="20974-107">**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** 登錄值可控制當傳回非同步呼叫的資料時，WMI 是否會檢查是否有可接受的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="20974-107">The **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault** registry value controls whether WMI checks for an acceptable authentication level when returning data for an asynchronous call.</span></span> <span data-ttu-id="20974-108">回呼可在較低的驗證層級傳回，而不是原始的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="20974-108">The callback can be returned at a lower authentication level than that of the original asynchronous call.</span></span> <span data-ttu-id="20974-109">依預設，此值設定為零，因此不會檢查回呼。</span><span class="sxs-lookup"><span data-stu-id="20974-109">By default, this value is set to zero so that callbacks are not checked.</span></span> <span data-ttu-id="20974-110">若要保護腳本中的非同步呼叫，您必須將登錄機碼設定為 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="20974-110">To secure asynchronous calls in scripting, you must set the registry key to 1 (one).</span></span>

<span data-ttu-id="20974-111">腳本可以使用登錄物件 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)的 [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)和 [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)方法來變更 **UnsecAppAccessControlDefault** 登錄值的設定。</span><span class="sxs-lookup"><span data-stu-id="20974-111">Scripts can use the [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) and [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) methods of the registry object [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) to change the setting of the **UnsecAppAccessControlDefault** registry value.</span></span> <span data-ttu-id="20974-112">如需遠端存取所需的驗證和模擬層級的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="20974-112">For more information about authentication and impersonation levels required for remote access, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-set-asynchronous-call-security-in-vbscript"></a><span data-ttu-id="20974-113">設定 VBScript 中的非同步呼叫安全性</span><span class="sxs-lookup"><span data-stu-id="20974-113">To set asynchronous call security in VBScript</span></span>

<span data-ttu-id="20974-114">下列 VBScript 程式碼範例說明如何變更登錄值，以控制回呼的 WMI 驗證。</span><span class="sxs-lookup"><span data-stu-id="20974-114">The following VBScript code example shows you how to change the registry value to control WMI authentication of callbacks.</span></span>

<span data-ttu-id="20974-115">腳本會將 **UnsecAppAccessControlDefault** 的值從零變更為1，如果值已設定，則會將值從1變更為零。</span><span class="sxs-lookup"><span data-stu-id="20974-115">The script changes the value of **UnsecAppAccessControlDefault** from zero to one, or if the value is already set, from one to zero.</span></span> <span data-ttu-id="20974-116">新安裝的系統上的預設值為零。</span><span class="sxs-lookup"><span data-stu-id="20974-116">Zero is the default on a newly installed system.</span></span> <span data-ttu-id="20974-117">設定旗標之後，設定會在重新開機或 WMI 重新開機時持續保存。</span><span class="sxs-lookup"><span data-stu-id="20974-117">Once the flag is set, the setting persists across reboot or WMI restart.</span></span>

<span data-ttu-id="20974-118">腳本會使用 [**SWbemMethod. InParameters**](swbemmethod-inparameters.md) 物件，並 [**SWbemObject.ExeCMethod**](swbemobject-execmethod-.md) 來呼叫 [**StdRegProv. GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) 和 [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)。</span><span class="sxs-lookup"><span data-stu-id="20974-118">The script uses a [**SWbemMethod.InParameters**](swbemmethod-inparameters.md) object and [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) to call [**StdRegProv.GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) and [**StdRegProv.SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).</span></span> <span data-ttu-id="20974-119">如需有關設定 **InParameters** 物件中之值的詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="20974-119">For more information about setting the values in an **InParameters** object, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span> <span data-ttu-id="20974-120">如需使用 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)進行登錄呼叫的範例，請參閱 [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)。</span><span class="sxs-lookup"><span data-stu-id="20974-120">For an example of a registry call using [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), see [**StdRegProv.SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).</span></span>


```VB
' Registry key value in hex
Const hklm = &h800000002  
' Subkey string 
Const Subkey = "software\\microsoft\\wbem\\cimom" 
' Asynchronous access control
Const sValueName = "UnsecAppAccessControlDefault" 

' Obtain registry object
Set objReg = GetObject("winmgmts:root\default:StdRegProv") 

' Get the initial value of the asynchronous 
'   access control registry key
' Use an InParameters object to set up the 
'   parameters for the ExecMethod call
' For more information see Constructing InParameters Objects 
'   topic and SWbemObject.ExecMethod_ topic

Set InParams = objReg.methods_("GetStringValue").InParameters.SpawnInstance_
InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName

' Get return value from OutParameters object returned by ExecMethod. 
' For more information see Parsing OutParameters Objects topic

Set OutParams = objReg.Execmethod_("GetStringValue",InParams)

If (OutParams.ReturnValue <> 0) then
   Wscript.Echo "GetStringValue returned " & OutParams.ReturnValue
   Wscript.Quit 1
End If

Svalue = OutParams.sValue
If (sValue = 0) Then
   AccessControl = "WMI not performing asynch access control"
Else 
   AccessControl = "WMI performing asynch access control"  
End If
Wscript.Echo sValueName & " = " _
    & sValue & VBNewLine & AccessControl

' Change asynchronous access control registry key value
Set InParams = objReg.methods_("SetStringValue").InParameters.SpawnInstance_

InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName
InParams.sValue = sValue XOR 1

Set OutParams = objReg.ExecMethod_("SetStringValue",InParams)

If (OutParams.Returnvalue <> 0) Then
    Wscript.Echo "SetStringValue returned " & OutParams.Returnvalue
    Wscript.Quit 1
End If

Wscript.Echo SValueName & " changed to " & (sValue XOR 1)
```



 

 
