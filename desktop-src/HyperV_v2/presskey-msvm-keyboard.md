---
description: 模擬按鍵的按鍵。
ms.assetid: 42C11F92-6143-40D7-9C07-56A6514EB4D1
title: Msvm_Keyboard 類別的 PressKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.PressKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9f196c5af3f8946460564e56bb425ffc24b51c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981882"
---
# <a name="presskey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="67e5e-103">Msvm 鍵盤類別的 PressKey 方法 \_</span><span class="sxs-lookup"><span data-stu-id="67e5e-103">PressKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="67e5e-104">模擬按鍵的按鍵。</span><span class="sxs-lookup"><span data-stu-id="67e5e-104">Simulates a key press.</span></span> <span data-ttu-id="67e5e-105">當成功時，金鑰會處於關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="67e5e-105">When successful the key will be in the down state.</span></span>

## <a name="syntax"></a><span data-ttu-id="67e5e-106">語法</span><span class="sxs-lookup"><span data-stu-id="67e5e-106">Syntax</span></span>


```mof
uint32 PressKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="67e5e-107">參數</span><span class="sxs-lookup"><span data-stu-id="67e5e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67e5e-108">*keyCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="67e5e-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67e5e-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67e5e-109">Type: **uint32**</span></span>

<span data-ttu-id="67e5e-110">要按下之按鍵的虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="67e5e-110">The virtual-key code of the key to press.</span></span> <span data-ttu-id="67e5e-111">如需虛擬機器碼的清單，請參閱 [**虛擬金鑰代碼**](../inputdev/virtual-key-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="67e5e-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67e5e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="67e5e-112">Return value</span></span>

<span data-ttu-id="67e5e-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="67e5e-113">Type: **uint32**</span></span>

<span data-ttu-id="67e5e-114">傳回值為零表示成功。</span><span class="sxs-lookup"><span data-stu-id="67e5e-114">A return value of zero indicates success.</span></span> <span data-ttu-id="67e5e-115">非零值表示無法修改金鑰狀態。</span><span class="sxs-lookup"><span data-stu-id="67e5e-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="67e5e-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="67e5e-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="67e5e-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="67e5e-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="67e5e-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="67e5e-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="67e5e-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="67e5e-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="67e5e-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-124">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="67e5e-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="67e5e-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="67e5e-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="67e5e-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="67e5e-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="67e5e-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="67e5e-129">備註</span><span class="sxs-lookup"><span data-stu-id="67e5e-129">Remarks</span></span>

<span data-ttu-id="67e5e-130">**PressKey** 方法會將 [VK] **\_ 功能表** 的參考（ (18) 、 **VK \_ CONTROL** (17) 和 **VK \_ SHIFT** (16) 分別對應至 **VK \_ LMENU** (164) 、 **VK \_ LCONTROL** (162) 和 **VK \_ LSHIFT** (160) ，因為 **VK \_ 功能表**、 **VK \_ 控制項** 和 **VK \_ SHIFT** 虛擬按鍵代碼不代表鍵盤上的實際按鍵。</span><span class="sxs-lookup"><span data-stu-id="67e5e-130">The **PressKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="67e5e-131">[**Msvm \_ 鍵盤**](msvm-keyboard.md)類別的存取權可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="67e5e-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="67e5e-132">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="67e5e-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="67e5e-133">範例</span><span class="sxs-lookup"><span data-stu-id="67e5e-133">Examples</span></span>

<span data-ttu-id="67e5e-134">下列 c # 範例會模擬按鍵的按鍵。</span><span class="sxs-lookup"><span data-stu-id="67e5e-134">The following C# sample simulates a key press.</span></span> <span data-ttu-id="67e5e-135">您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。</span><span class="sxs-lookup"><span data-stu-id="67e5e-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class PressKeyClass
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

        static void PressKey(string vmName, int keyCode)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("PressKey");

            inParams["keyCode"] = keyCode;

            ManagementBaseObject outParams = keyboard.InvokeMethod("PressKey", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Key {0} was pressed on {1}", keyCode, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to press key {0}' on {1}", keyCode, vm["ElementName"]);
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
                Console.WriteLine("Usage: PressKey vmName keyCode");
                return;
            }
            string vmName = args[0];
            int keyCode = int.Parse(args[1]);
            PressKey(args[0], keyCode);
        }

    }
}

```



<span data-ttu-id="67e5e-136">下列 Visual Basic Scripting Edition (VBScript) 範例會模擬按鍵。</span><span class="sxs-lookup"><span data-stu-id="67e5e-136">The following Visual Basic Scripting Edition (VBScript) sample simulates a key press.</span></span>


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
    
    dim computer, objArgs, vmName, computerSystem, keycode, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       keycode = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript PressKey.vbs vmName keycode"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if PressKey(keyboard, keycode) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "PressKey failed"
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
' Press the key with the given key code on the given keyboard
'-----------------------------------------------------------------
Function PressKey(keyboard, keyCode)
    WriteLog Format2("PressKey({0}, {1})", keyboard.ElementName, keyCode)
    
    dim objInParam, objOutParams
    
    PressKey = false
    set objInParam = keyboard.Methods_("PressKey").InParameters.SpawnInstance_()
    objInParam.keyCode = keyCode

    set objOutParams = keyboard.ExecMethod_("PressKey", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("The key with code '{0}' is typed on {1}.", keyCode, keyboard.ElementName)
        PressKey = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\PressKey.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="67e5e-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="67e5e-137">Requirements</span></span>



| <span data-ttu-id="67e5e-138">需求</span><span class="sxs-lookup"><span data-stu-id="67e5e-138">Requirement</span></span> | <span data-ttu-id="67e5e-139">值</span><span class="sxs-lookup"><span data-stu-id="67e5e-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67e5e-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67e5e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="67e5e-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67e5e-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="67e5e-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67e5e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="67e5e-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67e5e-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67e5e-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="67e5e-144">Namespace</span></span><br/>                | <span data-ttu-id="67e5e-145">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="67e5e-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="67e5e-146">MOF</span><span class="sxs-lookup"><span data-stu-id="67e5e-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67e5e-147"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="67e5e-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67e5e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="67e5e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67e5e-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67e5e-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67e5e-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67e5e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e5e-151">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="67e5e-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="67e5e-152">**虛擬金鑰碼**</span><span class="sxs-lookup"><span data-stu-id="67e5e-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

