---
description: 將與指定索引相關聯的 SWbemObject 傳回集合中。
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: 'Swbemobjectset 搭配使用. ItemIndex 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992080"
---
# <a name="swbemobjectsetitemindex-method"></a><span data-ttu-id="711d3-103">Swbemobjectset 搭配使用. ItemIndex 方法</span><span class="sxs-lookup"><span data-stu-id="711d3-103">SWbemObjectSet.ItemIndex method</span></span>

<span data-ttu-id="711d3-104">**ItemIndex** 方法會將與指定索引相關聯的 [**SWbemObject**](swbemobject.md)傳回集合中。</span><span class="sxs-lookup"><span data-stu-id="711d3-104">The **ItemIndex** method returns the [**SWbemObject**](swbemobject.md) associated with the specified index into the collection.</span></span> <span data-ttu-id="711d3-105">索引會指出元素在集合中的位置。</span><span class="sxs-lookup"><span data-stu-id="711d3-105">The index indicates the position of the element within the collection.</span></span> <span data-ttu-id="711d3-106">集合編號從零開始。</span><span class="sxs-lookup"><span data-stu-id="711d3-106">Collection numbering starts at zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="711d3-107">語法</span><span class="sxs-lookup"><span data-stu-id="711d3-107">Syntax</span></span>


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a><span data-ttu-id="711d3-108">參數</span><span class="sxs-lookup"><span data-stu-id="711d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="711d3-109">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="711d3-109">*lIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="711d3-110">集合中專案的索引。</span><span class="sxs-lookup"><span data-stu-id="711d3-110">Index of the item in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="711d3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="711d3-111">Return value</span></span>

<span data-ttu-id="711d3-112">如果成功，要求的 [**SWbemObject**](swbemobject.md) 物件就會傳回。</span><span class="sxs-lookup"><span data-stu-id="711d3-112">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="711d3-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="711d3-113">Error codes</span></span>

<span data-ttu-id="711d3-114">當 [**專案**](swbemobjectset-item.md) 方法完成時， **Err** 物件可能會包含下列其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="711d3-114">Upon completion of the [**Item**](swbemobjectset-item.md) method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="711d3-115">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="711d3-115">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="711d3-116">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="711d3-116">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="711d3-117">**wbemErrInvalidParameter** -2147749896 (0x80041008) </span><span class="sxs-lookup"><span data-stu-id="711d3-117">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="711d3-118">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="711d3-118">Invalid parameter was specified.</span></span> <span data-ttu-id="711d3-119">如果提供了負索引編號，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="711d3-119">This error is returned if a negative index number is supplied.</span></span>

</dd> <dt>

<span data-ttu-id="711d3-120">**wbemErrOutOfMemory** -2147749894 (0x80041006) </span><span class="sxs-lookup"><span data-stu-id="711d3-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="711d3-121">記憶體不足，無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="711d3-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="711d3-122">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="711d3-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="711d3-123">找不到要求的專案。</span><span class="sxs-lookup"><span data-stu-id="711d3-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="711d3-124">備註</span><span class="sxs-lookup"><span data-stu-id="711d3-124">Remarks</span></span>

<span data-ttu-id="711d3-125">**ItemIndex** 方法可讓以任何語言撰寫的 WMI 用戶端腳本和應用程式以一致的方式來操作集合（例如陣列）。</span><span class="sxs-lookup"><span data-stu-id="711d3-125">The **ItemIndex** method allows WMI clients scripts and applications written in any language a uniform way to manipulate a collection like an array.</span></span> <span data-ttu-id="711d3-126">這個方法可以與 [**swbemobjectset 搭配使用**](swbemobjectset.md) 集合搭配使用。</span><span class="sxs-lookup"><span data-stu-id="711d3-126">This method can be used with [**SWbemObjectSet**](swbemobjectset.md) collections.</span></span> <span data-ttu-id="711d3-127">查詢，例如 [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)、 [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)、 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)或 [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 會傳回 **swbemobjectset 搭配使用** 集合。</span><span class="sxs-lookup"><span data-stu-id="711d3-127">Queries, such as [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md), [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md), [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), or [**SWbemServices.ExecQuery**](swbemservices-execquery.md) return **SWbemObjectSet** collections.</span></span> <span data-ttu-id="711d3-128">**ItemIndex** 方法無法用於不包含 [**SWbemObjects**](swbemobject.md)的集合，例如 [**SWbemMethodSet**](swbemmethodset.md)、 [**SWbemNamedValueSet**](swbemnamedvalueset.md)、 [**SWbemPrivilegeSet**](swbemprivilegeset.md)、[**內含**](swbempropertyset.md)和 [**SWbemQualifierSet**](swbemqualifierset.md)。</span><span class="sxs-lookup"><span data-stu-id="711d3-128">The **ItemIndex** method does not work with collections which do not contain [**SWbemObjects**](swbemobject.md), such as [**SWbemMethodSet**](swbemmethodset.md), [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), [**SWbemPropertySet**](swbempropertyset.md), and [**SWbemQualifierSet**](swbemqualifierset.md).</span></span>

<span data-ttu-id="711d3-129">**ItemIndex** 也可用來取得單一類別的單一實例。</span><span class="sxs-lookup"><span data-stu-id="711d3-129">**ItemIndex** can also be used to obtain the single instance of a singleton class.</span></span>

## <a name="examples"></a><span data-ttu-id="711d3-130">範例</span><span class="sxs-lookup"><span data-stu-id="711d3-130">Examples</span></span>

<span data-ttu-id="711d3-131">下列 VBScript 程式碼範例會查詢所有 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 實例的集合，然後顯示前三個處理常式的名稱。</span><span class="sxs-lookup"><span data-stu-id="711d3-131">The following VBScript code example queries for a collection of all the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instances then displays the names of the first three processes.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



<span data-ttu-id="711d3-132">每個作業系統安裝都只會有一個 [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) 實例存在。</span><span class="sxs-lookup"><span data-stu-id="711d3-132">Only one instance of [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) exists for each operating system installation.</span></span> <span data-ttu-id="711d3-133">建立 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) 路徑以取得單一實例很麻煩，因此腳本通常會列舉 **Win32 \_ 作業系統** ，即使只有一個實例可用也一樣。</span><span class="sxs-lookup"><span data-stu-id="711d3-133">Creating the [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) path to obtain the single instance is awkward so scripts normally enumerate **Win32\_OperatingSystem** even though only one instance is available.</span></span> <span data-ttu-id="711d3-134">下列 VBScript 程式碼範例示範如何使用 **ItemIndex** 方法來取得一個 **Win32 \_ 作業系統** ，而不使用 **for each** 迴圈。</span><span class="sxs-lookup"><span data-stu-id="711d3-134">The following VBScript code example shows how to use the **ItemIndex** method to get to the one **Win32\_OperatingSystem** without using a **For Each** loop.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



<span data-ttu-id="711d3-135">下列 VBScript 程式碼範例會取得與 [**win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)（例如 [**win32 \_ SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem)）相關聯的實例。</span><span class="sxs-lookup"><span data-stu-id="711d3-135">The following VBScript code example gets instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem), such as [**Win32\_SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



<span data-ttu-id="711d3-136">下列程式碼範例輸出顯示與 [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)相關聯的實例。</span><span class="sxs-lookup"><span data-stu-id="711d3-136">The following code example output shows instances associated with [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
```

## <a name="requirements"></a><span data-ttu-id="711d3-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="711d3-137">Requirements</span></span>



| <span data-ttu-id="711d3-138">需求</span><span class="sxs-lookup"><span data-stu-id="711d3-138">Requirement</span></span> | <span data-ttu-id="711d3-139">值</span><span class="sxs-lookup"><span data-stu-id="711d3-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="711d3-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="711d3-140">Minimum supported client</span></span><br/> | <span data-ttu-id="711d3-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="711d3-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="711d3-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="711d3-142">Minimum supported server</span></span><br/> | <span data-ttu-id="711d3-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="711d3-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="711d3-144">標頭</span><span class="sxs-lookup"><span data-stu-id="711d3-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="711d3-145"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="711d3-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="711d3-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="711d3-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="711d3-147"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="711d3-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="711d3-148">DLL</span><span class="sxs-lookup"><span data-stu-id="711d3-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="711d3-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="711d3-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="711d3-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="711d3-150">CLSID</span></span><br/>                    | <span data-ttu-id="711d3-151">CLSID \_ swbemobjectset 搭配使用</span><span class="sxs-lookup"><span data-stu-id="711d3-151">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="711d3-152">IID</span><span class="sxs-lookup"><span data-stu-id="711d3-152">IID</span></span><br/>                      | <span data-ttu-id="711d3-153">IID \_ ISWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="711d3-153">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="711d3-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="711d3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="711d3-155">**Swbemobjectset 搭配使用**</span><span class="sxs-lookup"><span data-stu-id="711d3-155">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

