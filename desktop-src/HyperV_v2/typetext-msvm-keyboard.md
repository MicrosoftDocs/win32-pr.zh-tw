---
description: 模擬一連串的類型字元。
ms.assetid: 5D4C9F27-84AA-4131-A9A3-2C72DB2E8909
title: Msvm_Keyboard 類別的 TypeText 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeText
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 37e8227a545975a6193be63a8bd363e10e9805f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979331"
---
# <a name="typetext-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="782b3-103">Msvm 鍵盤類別的 TypeText 方法 \_</span><span class="sxs-lookup"><span data-stu-id="782b3-103">TypeText method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="782b3-104">模擬一連串的類型字元。</span><span class="sxs-lookup"><span data-stu-id="782b3-104">Simulates a series of typed characters.</span></span> <span data-ttu-id="782b3-105">這相當於針對字串中的每個字元呼叫 [**PressKey**](presskey-msvm-keyboard.md) ，後面接著 [**ReleaseKey**](releasekey-msvm-keyboard.md) 。</span><span class="sxs-lookup"><span data-stu-id="782b3-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md) for each character in the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="782b3-106">語法</span><span class="sxs-lookup"><span data-stu-id="782b3-106">Syntax</span></span>


```mof
uint32 TypeText(
  [in] string asciiText
);
```



## <a name="parameters"></a><span data-ttu-id="782b3-107">參數</span><span class="sxs-lookup"><span data-stu-id="782b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="782b3-108">*asciiText* \[在\]</span><span class="sxs-lookup"><span data-stu-id="782b3-108">*asciiText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="782b3-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="782b3-109">Type: **string**</span></span>

<span data-ttu-id="782b3-110">要輸入的 ASCII 或 Unicode 字元系列。</span><span class="sxs-lookup"><span data-stu-id="782b3-110">The series of ASCII or Unicode characters to type.</span></span> <span data-ttu-id="782b3-111">這個字串的最大長度取決於字串中的字元類型。</span><span class="sxs-lookup"><span data-stu-id="782b3-111">The maximum length of this string depends on the type of characters in the string.</span></span>



| <span data-ttu-id="782b3-112">字串類型</span><span class="sxs-lookup"><span data-stu-id="782b3-112">String type</span></span>        | <span data-ttu-id="782b3-113">最大字元數</span><span class="sxs-lookup"><span data-stu-id="782b3-113">Maximum characters</span></span>                                                               |
|--------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="782b3-114">ASCII</span><span class="sxs-lookup"><span data-stu-id="782b3-114">ASCII</span></span><br/>   | <span data-ttu-id="782b3-115">512</span><span class="sxs-lookup"><span data-stu-id="782b3-115">512</span></span><br/>                                                                   |
| <span data-ttu-id="782b3-116">Unicode</span><span class="sxs-lookup"><span data-stu-id="782b3-116">Unicode</span></span><br/> | <span data-ttu-id="782b3-117">256至512，視字串中的代理組數目而定。</span><span class="sxs-lookup"><span data-stu-id="782b3-117">256 to 512, depending on the number of surrogate pairs in the string.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="782b3-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="782b3-118">Return value</span></span>

<span data-ttu-id="782b3-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="782b3-119">Type: **uint32**</span></span>

<span data-ttu-id="782b3-120">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="782b3-120">A return value of zero indicates success.</span></span> <span data-ttu-id="782b3-121">傳回值為1，表示輸入字串中的 nontranslatable 字元造成的失敗。</span><span class="sxs-lookup"><span data-stu-id="782b3-121">A return value of one indicates a failure caused by nontranslatable characters in the input string.</span></span> <span data-ttu-id="782b3-122">所有其他非零值則表示無法修改金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="782b3-122">All other nonzero values indicate a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="782b3-123">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="782b3-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="782b3-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-125">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="782b3-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-126">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="782b3-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-127">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="782b3-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-128">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="782b3-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-129">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="782b3-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-130">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="782b3-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-131">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="782b3-131">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-132">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="782b3-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-133">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="782b3-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-134">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="782b3-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="782b3-135">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="782b3-135">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="782b3-136">備註</span><span class="sxs-lookup"><span data-stu-id="782b3-136">Remarks</span></span>

<span data-ttu-id="782b3-137">[**Msvm \_ 鍵盤**](msvm-keyboard.md)類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="782b3-137">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="782b3-138">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="782b3-138">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="782b3-139">範例</span><span class="sxs-lookup"><span data-stu-id="782b3-139">Examples</span></span>

<span data-ttu-id="782b3-140">下列 c # 範例會模擬輸入文字。</span><span class="sxs-lookup"><span data-stu-id="782b3-140">The following C# sample simulates typing text.</span></span> <span data-ttu-id="782b3-141">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="782b3-141">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class TypeTextClass
    {
        static ManagementObject GetComputerKeyboard(ManagementObject vm)
        {
            ManagementObjectCollection keyboardCollection = vm.GetRelated
            (
                "Msvm_Keyboard",
                "Msvm_SystemDevice",
                null,
                null,
                "PartComponent",
                "GroupComponent",
                false,
                null
            );

            ManagementObject keyboard = null;

            foreach (ManagementObject instance in keyboardCollection)
            {
                keyboard = instance;
                break;
            }

            return keyboard;
        }

        static void TypeText(string vmName, string text)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("TypeText");

            inParams["asciiText"] = text;

            ManagementBaseObject outParams = keyboard.InvokeMethod("TypeText", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Text {0} was typed on {1}", text, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to type '{0}' on {1}", text, vm["ElementName"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            keyboard.Dispose();
            vm.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: TypeText vmName Text");
                return;
            }
            TypeText(args[0], args[1]);
        }
    }
}

```



<span data-ttu-id="782b3-142">下列 Visual Basic Scripting Edition (VBScript) 範例會模擬輸入文字。</span><span class="sxs-lookup"><span data-stu-id="782b3-142">The following Visual Basic Scripting Edition (VBScript) sample simulates typing text.</span></span>


```VB
option explicit 

dim objWMIService
dim fileSystem
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    dim computer, objArgs, vmName, computerSystem, text, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       text = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript TypeText.vbs vmName text"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if TypeText(keyboard, text) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "TypeText operation failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    dim query
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_Keyboard from given computer system
' 
'-----------------------------------------------------------------
Function GetComputerKeyboard(computerSystem)
    dim query
    On Error Resume Next
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_Keyboard", computerSystem.Path_.Path)
    set GetComputerKeyboard = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' Type the given text to the given keyboard
'-----------------------------------------------------------------
Function TypeText(keyboard, text)
    WriteLog Format2("TypeText({0}, {1})", keyboard.ElementName, text)
    
    dim objInParam, objOutParams

    TypeText = false
    set objInParam = keyboard.Methods_("TypeText").InParameters.SpawnInstance_()
    objInParam.asciiText = text

    set objOutParams = keyboard.ExecMethod_("TypeText", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("'{0}' was typed on {1}", text, keyboard.ElementName)
        TypeText = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\Typetext.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="782b3-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="782b3-143">Requirements</span></span>



| <span data-ttu-id="782b3-144">需求</span><span class="sxs-lookup"><span data-stu-id="782b3-144">Requirement</span></span> | <span data-ttu-id="782b3-145">值</span><span class="sxs-lookup"><span data-stu-id="782b3-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="782b3-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="782b3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="782b3-147">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="782b3-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="782b3-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="782b3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="782b3-149">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="782b3-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="782b3-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="782b3-150">Namespace</span></span><br/>                | <span data-ttu-id="782b3-151">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="782b3-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="782b3-152">MOF</span><span class="sxs-lookup"><span data-stu-id="782b3-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="782b3-153"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="782b3-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="782b3-154">DLL</span><span class="sxs-lookup"><span data-stu-id="782b3-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="782b3-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="782b3-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="782b3-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="782b3-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="782b3-157">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="782b3-157">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

