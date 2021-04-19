---
description: 有時候，您可能只想要更新一部分的實例。
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: 更新部分實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971714"
---
# <a name="updating-part-of-an-instance"></a><span data-ttu-id="2420e-103">更新部分實例</span><span class="sxs-lookup"><span data-stu-id="2420e-103">Updating Part of an Instance</span></span>

<span data-ttu-id="2420e-104">有時候，您可能只想要更新一部分的實例。</span><span class="sxs-lookup"><span data-stu-id="2420e-104">Occasionally, you may want to update only part of an instance.</span></span> <span data-ttu-id="2420e-105">例如，某些實例有大量的屬性。</span><span class="sxs-lookup"><span data-stu-id="2420e-105">For example, some instances have a large number of properties.</span></span> <span data-ttu-id="2420e-106">如果您必須更新大量的實例，可能會降低系統效能。</span><span class="sxs-lookup"><span data-stu-id="2420e-106">If you had to update a large number of these instances, you may reduce system performance.</span></span> <span data-ttu-id="2420e-107">因此，您可以選擇只更新部分的實例，進而減少您必須在 WMI 中傳送和取出的資訊量。</span><span class="sxs-lookup"><span data-stu-id="2420e-107">Therefore, you can choose to update only part of the instance, and thus reduce the amount of information you must send and retrieve to and from WMI.</span></span> <span data-ttu-id="2420e-108">不過，WMI 不直接支援部分實例作業，也不會執行大部分的提供者。</span><span class="sxs-lookup"><span data-stu-id="2420e-108">However, WMI does not directly support partial-instance operations, nor do most providers.</span></span> <span data-ttu-id="2420e-109">因此，如果您撰寫的應用程式會使用部分實例作業，請使用 **wbem \_ e \_ 提供者 \_ 無法 \_** 使用或 **\_ \_ 不 \_ 支援** 在 c + + 中使用 wbem e 的錯誤碼，來準備您的呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="2420e-109">Therefore, if you write an application that uses partial-instance operations, be prepared for your calls to fail with either the **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** or **WBEM\_E\_NOT\_SUPPORTED** error code in C++.</span></span> <span data-ttu-id="2420e-110">在指令碼語言中，錯誤碼可能是 **wbemErrProviderNotCapable** 或 **wbemErrNotSupported**。</span><span class="sxs-lookup"><span data-stu-id="2420e-110">In scripting languages the error codes are either **wbemErrProviderNotCapable** or **wbemErrNotSupported**.</span></span>

<span data-ttu-id="2420e-111">在腳本中，這項作業只有在透過企業更新極大量物件中的一或兩個可寫入屬性時，才需要協助效能。</span><span class="sxs-lookup"><span data-stu-id="2420e-111">In scripting, this operation is only necessary to aid performance when updating one or two writeable properties in a very large number of objects over an enterprise.</span></span> <span data-ttu-id="2420e-112">否則，一般 VBScript 會呼叫 [**SWbemObject. Put \_**](swbemobject-put-.md)或 [**SWbemObject PutAsync \_**](swbemobject-putasync-.md)，而如同寫入整個物件時，實際上只會更新提供者已啟用寫入的屬性。</span><span class="sxs-lookup"><span data-stu-id="2420e-112">Otherwise, the normal VBScript calls to [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md), while seeming to write the entire object, are actually only updating the properties which the provider has write-enabled.</span></span>

<span data-ttu-id="2420e-113">下列程式描述如何使用 PowerShell 要求部分實例更新。</span><span class="sxs-lookup"><span data-stu-id="2420e-113">The following procedure describes how to request a partial-instance update using PowerShell.</span></span>

<span data-ttu-id="2420e-114">**使用 PowerShell 要求部分實例更新**</span><span class="sxs-lookup"><span data-stu-id="2420e-114">**To request a partial-instance update using PowerShell**</span></span>

1.  <span data-ttu-id="2420e-115">取得您想要更新之物件的路徑。</span><span class="sxs-lookup"><span data-stu-id="2420e-115">Retrieve the path of the object you wish to update.</span></span>

    <span data-ttu-id="2420e-116">您可以手動描述路徑，或查詢物件，然後取得 **\_ \_ path** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2420e-116">You can describe the path either manually, or else query the object and then retrieve the **\_\_Path** property.</span></span>

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  <span data-ttu-id="2420e-117">設定雜湊表，其中列出要更新的屬性名稱，並在 [set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true)的呼叫中使用此雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2420e-117">Set up a hash table listing the names of the properties to be updated, and use this hash table in a call to [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

<span data-ttu-id="2420e-118">下列程式說明如何使用 c # 要求部分實例更新。</span><span class="sxs-lookup"><span data-stu-id="2420e-118">The following procedure describes how to request a partial-instance update using C#.</span></span>

> [!Note]  
> <span data-ttu-id="2420e-119">**系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。</span><span class="sxs-lookup"><span data-stu-id="2420e-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="2420e-120">**使用 C 要求部分實例更新#**</span><span class="sxs-lookup"><span data-stu-id="2420e-120">**To request a partial-instance update using C#**</span></span>

1.  <span data-ttu-id="2420e-121">建立新的 [system.management.managementobject](/dotnet/api/system.management.managementobject) 物件，代表要更新的特定實例。</span><span class="sxs-lookup"><span data-stu-id="2420e-121">Create a new [ManagementObject](/dotnet/api/system.management.managementobject) object that represents the specific instance to update.</span></span>

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  <span data-ttu-id="2420e-122">使用 [system.management.managementobject. SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_)的呼叫來設定屬性值。</span><span class="sxs-lookup"><span data-stu-id="2420e-122">Set the property value with a call to [ManagementObject.SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span></span>

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

<span data-ttu-id="2420e-123">下列程式描述如何使用 VBScript 要求部分實例更新。</span><span class="sxs-lookup"><span data-stu-id="2420e-123">The following procedure describes how to request a partial-instance update using VBScript.</span></span>

<span data-ttu-id="2420e-124">**使用 VBScript 要求部分實例更新**</span><span class="sxs-lookup"><span data-stu-id="2420e-124">**To request a partial-instance update using VBScript**</span></span>

1.  <span data-ttu-id="2420e-125">建立 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 內容物件。</span><span class="sxs-lookup"><span data-stu-id="2420e-125">Create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object.</span></span>

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  <span data-ttu-id="2420e-126">使用 SWbemNamedValueSet. Add 方法，將 Put 延伸模組值「 \_ \_ put \_ 延伸」和「 \_ \_ put \_ EXT CLIENT 要求」新增 \_ \_ 至內容物件。 [](swbemnamedvalueset-add.md)</span><span class="sxs-lookup"><span data-stu-id="2420e-126">Add the Put extension values "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" to the context object using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span>

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  <span data-ttu-id="2420e-127">設定陣列，其中列出要更新的屬性名稱，並將此陣列新增至副檔名值[](swbemnamedvalueset.md)為 " \_ \_ put \_ EXT \_ properties" 的 SWbemNamedValueSet 內容物件。</span><span class="sxs-lookup"><span data-stu-id="2420e-127">Set up an array listing the names of the properties to be updated and add this array to the [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object with the Put extension value "\_\_PUT\_EXT\_PROPERTIES".</span></span>

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  <span data-ttu-id="2420e-128">將 SWbemObject 的 *iFlags* 參數設定為 **wbemChangeFlagUpdateOnly** 的 [**Put \_**](swbemobject-put-.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="2420e-128">Set the *iFlags* parameter of the [**SWbemObject.Put\_**](swbemobject-put-.md) call to **wbemChangeFlagUpdateOnly**.</span></span> <span data-ttu-id="2420e-129">若未使用此旗標，則呼叫會失敗，並出現不正確內容。</span><span class="sxs-lookup"><span data-stu-id="2420e-129">Without this flag the call will fail with an invalid context.</span></span>

5.  <span data-ttu-id="2420e-130">在 [**SWbemObject. Put \_**](swbemobject-put-.md)或 [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md)的 *objwbemNamedValueSet* 參數中，將您的旗標和內容物件傳遞給提供者。</span><span class="sxs-lookup"><span data-stu-id="2420e-130">Pass your flag and context object to the provider in the *objwbemNamedValueSet* parameter of either [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md).</span></span>

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

<span data-ttu-id="2420e-131">下列程式描述如何使用 c + + 要求部分實例更新。</span><span class="sxs-lookup"><span data-stu-id="2420e-131">The following procedure describes how to request a partial-instance update using C++.</span></span>

<span data-ttu-id="2420e-132">**使用 c + + 要求部分實例更新**</span><span class="sxs-lookup"><span data-stu-id="2420e-132">**To request a partial-instance update using C++**</span></span>

1.  <span data-ttu-id="2420e-133">使用對 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來建立 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)物件。</span><span class="sxs-lookup"><span data-stu-id="2420e-133">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="2420e-134">內容物件是 WMI 用來將更多資訊傳遞給 WMI 提供者的物件。</span><span class="sxs-lookup"><span data-stu-id="2420e-134">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="2420e-135">在此情況下，您會使用 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 物件來指示提供者接受部分實例更新。</span><span class="sxs-lookup"><span data-stu-id="2420e-135">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to accept partial-instance updates.</span></span>

2.  <span data-ttu-id="2420e-136">\_ \_ \_ 使用 IWbemCoNtext：： SetValue 的呼叫，將「put 延伸」和「 \_ \_ put \_ EXT \_ CLIENT \_ 要求」命名值新增 [](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue)至 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)物件。</span><span class="sxs-lookup"><span data-stu-id="2420e-136">Add the "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" named values to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="2420e-137">下表列出「put 延伸模組」 \_ \_ \_ 和「 \_ \_ put \_ EXT \_ CLIENT \_ 要求」的意義。</span><span class="sxs-lookup"><span data-stu-id="2420e-137">The following table lists the meaning of "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST".</span></span>

    

    | <span data-ttu-id="2420e-138">命名值</span><span class="sxs-lookup"><span data-stu-id="2420e-138">Named value</span></span>                     | <span data-ttu-id="2420e-139">Description</span><span class="sxs-lookup"><span data-stu-id="2420e-139">Description</span></span>                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2420e-140">" \_ \_ PUT \_ EXTENSIONS"</span><span class="sxs-lookup"><span data-stu-id="2420e-140">"\_\_PUT\_EXTENSIONS"</span></span>           | <span data-ttu-id="2420e-141">**VT \_BOOL** 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="2420e-141">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="2420e-142">值，指出已指定一個或多個其他內容值。</span><span class="sxs-lookup"><span data-stu-id="2420e-142">A value indicating that one or more of the other context values has been specified.</span></span> <span data-ttu-id="2420e-143">這可讓您快速檢查提供者內的內容物件，以判斷是否正在使用部分實例更新。</span><span class="sxs-lookup"><span data-stu-id="2420e-143">This allows a quick check of the context object inside the provider to determine if partial-instance updates are being used.</span></span> |
    | <span data-ttu-id="2420e-144">「 \_ \_ 放置 \_ EXT \_ 用戶端 \_ 要求」</span><span class="sxs-lookup"><span data-stu-id="2420e-144">"\_\_PUT\_EXT\_CLIENT\_REQUEST"</span></span> | <span data-ttu-id="2420e-145">**VT \_BOOL** 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="2420e-145">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="2420e-146">在初始要求期間由用戶端設定。</span><span class="sxs-lookup"><span data-stu-id="2420e-146">Set by the client during the initial request.</span></span> <span data-ttu-id="2420e-147">此值可用來防止重新進入錯誤。</span><span class="sxs-lookup"><span data-stu-id="2420e-147">This value is used to prevent reentrancy errors.</span></span>                                                                                                                   |

    

     

3.  <span data-ttu-id="2420e-148">\_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 使用 [**IWbemCoNtext：： SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue)的另一個呼叫，在 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)物件中加入 put ext STRICT null、put ext 屬性，或將 ext 不可部分完成的任何組合。</span><span class="sxs-lookup"><span data-stu-id="2420e-148">Add the \_\_PUT\_EXT\_STRICT\_NULLS, \_\_PUT\_EXT\_PROPERTIES, or \_\_PUT\_EXT\_ATOMIC in any combination as needed to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with another call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="2420e-149">下表列出已命名值的意義。</span><span class="sxs-lookup"><span data-stu-id="2420e-149">The following table lists the meaning of the named values.</span></span>

    

    | <span data-ttu-id="2420e-150">命名值</span><span class="sxs-lookup"><span data-stu-id="2420e-150">Named value</span></span>                   | <span data-ttu-id="2420e-151">Description</span><span class="sxs-lookup"><span data-stu-id="2420e-151">Description</span></span>                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2420e-152">" \_ \_ PUT \_ EXT \_ STRICT \_ Null"</span><span class="sxs-lookup"><span data-stu-id="2420e-152">"\_\_PUT\_EXT\_STRICT\_NULLS"</span></span> | <span data-ttu-id="2420e-153">**VT \_BOOL** 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="2420e-153">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="2420e-154">指出用戶端已刻意將屬性設為 **VT \_ Null** ，並預期寫入作業成功。</span><span class="sxs-lookup"><span data-stu-id="2420e-154">Indicates that the client has intentionally set properties to **VT\_NULL** and expects the write operation to succeed.</span></span> <span data-ttu-id="2420e-155">如果提供者無法將值設定為 **Null**，則應該回報錯誤。</span><span class="sxs-lookup"><span data-stu-id="2420e-155">If the provider cannot set the values to **NULL**, an error should be reported.</span></span> |
    | <span data-ttu-id="2420e-156">" \_ \_ PUT \_ EXT \_ PROPERTIES"</span><span class="sxs-lookup"><span data-stu-id="2420e-156">"\_\_PUT\_EXT\_PROPERTIES"</span></span>    | <span data-ttu-id="2420e-157">字串的 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) ，包含要更新之屬性名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="2420e-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings containing a list of property names to be updated.</span></span> <span data-ttu-id="2420e-158">可以單獨使用，或搭配「 \_ \_ PUT \_ EXT 屬性」一起使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2420e-158">May be used alone or in combination with "\_\_PUT\_EXT\_PROPERTIES".</span></span> <span data-ttu-id="2420e-159">這些值位於所寫入的實例中。</span><span class="sxs-lookup"><span data-stu-id="2420e-159">The values are in the instance being written.</span></span>                           |
    | <span data-ttu-id="2420e-160">" \_ \_ PUT EXT 不可部分完成 \_ \_ "</span><span class="sxs-lookup"><span data-stu-id="2420e-160">"\_\_PUT\_EXT\_ATOMIC"</span></span>        | <span data-ttu-id="2420e-161">**VT \_BOOL** 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="2420e-161">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="2420e-162">指出所有更新都必須同時成功 (不可部分完成的語義) 或提供者必須還原。</span><span class="sxs-lookup"><span data-stu-id="2420e-162">Indicates that all updates must succeed simultaneously (atomic semantics) or the provider must revert back.</span></span> <span data-ttu-id="2420e-163">可能沒有部分成功。</span><span class="sxs-lookup"><span data-stu-id="2420e-163">There can be no partial success.</span></span> <span data-ttu-id="2420e-164">可以單獨使用，也可以與其他旗標搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2420e-164">May be used alone or in combination with other flags.</span></span>     |

    

     

4.  <span data-ttu-id="2420e-165">將 *iFlags* 參數設定為 **[ \_ \_ \_ 僅限 WBEM 旗標更新**]。</span><span class="sxs-lookup"><span data-stu-id="2420e-165">Set the *iFlags* parameter to **WBEM\_FLAG\_UPDATE\_ONLY**.</span></span> <span data-ttu-id="2420e-166">若未使用此旗標，則呼叫會失敗，並出現不正確內容。</span><span class="sxs-lookup"><span data-stu-id="2420e-166">Without this flag the call will fail with an invalid context.</span></span>
5.  <span data-ttu-id="2420e-167">將 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)內容物件傳遞至 *pCtx* 參數中的任何 [**IWbemServices：:P Utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)或 [**iwbemservices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="2420e-167">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) in the *pCtx* parameter.</span></span>

    <span data-ttu-id="2420e-168">傳遞 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 物件會指示提供者允許部分實例更新。</span><span class="sxs-lookup"><span data-stu-id="2420e-168">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance updates.</span></span> <span data-ttu-id="2420e-169">在完整實例的更新中，您會將 *pCtx* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2420e-169">In a full-instance update, you would set *pCtx* to **NULL**.</span></span>

    <span data-ttu-id="2420e-170">如果出現在呼叫中的內容物件不包含「PUT 延伸模組」，則提供者可能會寫入任何必要的屬性 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="2420e-170">The provider may write any necessary properties if the context object present in the call does not contain "\_\_PUT\_EXTENSIONS".</span></span> <span data-ttu-id="2420e-171">如果 \_ \_ \_ 內容物件中有「PUT 延伸模組」，WMI 就會要求提供者必須遵守作業的語法，否則也會導致呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="2420e-171">If "\_\_PUT\_EXTENSIONS" is present in the context object, WMI requires the provider to either obey the semantics of the operation exactly or else fail the call.</span></span> <span data-ttu-id="2420e-172">如需詳細資訊，請參閱 [處理提供者中的拒絕存取訊息](impersonating-a-client.md)。</span><span class="sxs-lookup"><span data-stu-id="2420e-172">For more information, see [Handling Access Denied Messages in a Provider](impersonating-a-client.md).</span></span>

 

 
