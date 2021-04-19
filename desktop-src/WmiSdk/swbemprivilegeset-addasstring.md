---
description: 您可以使用 SWbemPrivilegeSet 物件的 AddAsString 方法，將許可權新增至使用許可權字串的 SWbemPrivilegeSet 集合。
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet. AddAsString 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984737"
---
# <a name="swbemprivilegesetaddasstring-method"></a><span data-ttu-id="4fc43-103">SWbemPrivilegeSet. AddAsString 方法</span><span class="sxs-lookup"><span data-stu-id="4fc43-103">SWbemPrivilegeSet.AddAsString method</span></span>

<span data-ttu-id="4fc43-104">您可以使用 [**SWbemPrivilegeSet**](swbemprivilegeset.md)物件的 **AddAsString** 方法，將許可權新增至使用許可權字串的 **SWbemPrivilegeSet** 集合。</span><span class="sxs-lookup"><span data-stu-id="4fc43-104">You can use the **AddAsString** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object to add a privilege to an **SWbemPrivilegeSet** collection using a privilege string.</span></span> <span data-ttu-id="4fc43-105">您可以使用這個方法來新增許可權，或啟用 [**SWbemSecurity**](swbemsecurity.md) 物件的許可權。</span><span class="sxs-lookup"><span data-stu-id="4fc43-105">Use this method to add a privilege or to enable a privilege for [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="4fc43-106">請參閱 [使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="4fc43-106">See [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="4fc43-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="4fc43-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc43-108">語法</span><span class="sxs-lookup"><span data-stu-id="4fc43-108">Syntax</span></span>


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4fc43-109">參數</span><span class="sxs-lookup"><span data-stu-id="4fc43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc43-110">*strPrivilege*</span><span class="sxs-lookup"><span data-stu-id="4fc43-110">*strPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="4fc43-111">必要。</span><span class="sxs-lookup"><span data-stu-id="4fc43-111">Required.</span></span> <span data-ttu-id="4fc43-112">其中一個許可權字串。</span><span class="sxs-lookup"><span data-stu-id="4fc43-112">One of the privilege strings.</span></span> <span data-ttu-id="4fc43-113">如需這些字串和相關 WMI 常數的完整清單，請參閱 [**許可權常數**](privilege-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="4fc43-113">For a complete list of these strings and the associated WMI constants, see [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="4fc43-114">每個許可權字串都代表特定的許可權。</span><span class="sxs-lookup"><span data-stu-id="4fc43-114">Every privilege string represents a specific privilege.</span></span> <span data-ttu-id="4fc43-115">例如，若要新增用來關閉電腦系統的許可權，請使用 **SeShutdownPrivilege** 字串。</span><span class="sxs-lookup"><span data-stu-id="4fc43-115">For example, to add the privilege that use to shut down a computer system, use the **SeShutdownPrivilege** string.</span></span>

</dd> <dt>

<span data-ttu-id="4fc43-116">*bIsEnabled* \[選\]</span><span class="sxs-lookup"><span data-stu-id="4fc43-116">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4fc43-117">啟用或停用此許可權的布林值。</span><span class="sxs-lookup"><span data-stu-id="4fc43-117">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="4fc43-118">預設值是 **True**。</span><span class="sxs-lookup"><span data-stu-id="4fc43-118">The default value is **True**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc43-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fc43-119">Return value</span></span>

<span data-ttu-id="4fc43-120">如果成功，這個方法會傳回代表新許可權的 [**SWbemPrivilege**](swbemprivilege.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="4fc43-120">If successful, this method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="4fc43-121">否則，會傳回 null 物件。</span><span class="sxs-lookup"><span data-stu-id="4fc43-121">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4fc43-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="4fc43-122">Error codes</span></span>

<span data-ttu-id="4fc43-123">**AddAsString** 方法完成後， **Err** 物件可能會包含下列清單中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4fc43-123">Upon the completion of the **AddAsString** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="4fc43-124">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="4fc43-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="4fc43-125">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4fc43-125">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4fc43-126">範例</span><span class="sxs-lookup"><span data-stu-id="4fc43-126">Examples</span></span>

<span data-ttu-id="4fc43-127">下列 VBScript 程式碼範例會使用 [**Win32 \_ TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport)來建立列印伺服器的新埠。</span><span class="sxs-lookup"><span data-stu-id="4fc43-127">The following VBScript code example creates a new port for a print server using [**Win32\_TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport).</span></span> <span data-ttu-id="4fc43-128">這項作業需要 **SeLoadDriverPrivilege** 。</span><span class="sxs-lookup"><span data-stu-id="4fc43-128">The **SeLoadDriverPrivilege** is required for this operation.</span></span> <span data-ttu-id="4fc43-129">請參閱 [執行特殊許可權作業](executing-privileged-operations.md)。</span><span class="sxs-lookup"><span data-stu-id="4fc43-129">See [Executing Privileged Operations](executing-privileged-operations.md).</span></span>


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



<span data-ttu-id="4fc43-130">使用這個方法的程式碼範例也會在 [**SWbemPrivilegeSet**](swbemprivilegeset.md) 主題中說明。</span><span class="sxs-lookup"><span data-stu-id="4fc43-130">A code example using this method is also described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc43-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fc43-131">Requirements</span></span>



| <span data-ttu-id="4fc43-132">需求</span><span class="sxs-lookup"><span data-stu-id="4fc43-132">Requirement</span></span> | <span data-ttu-id="4fc43-133">值</span><span class="sxs-lookup"><span data-stu-id="4fc43-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc43-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fc43-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc43-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4fc43-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4fc43-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fc43-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc43-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fc43-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4fc43-138">標頭</span><span class="sxs-lookup"><span data-stu-id="4fc43-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fc43-139"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc43-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fc43-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4fc43-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="4fc43-141"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4fc43-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4fc43-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4fc43-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fc43-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fc43-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4fc43-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="4fc43-144">CLSID</span></span><br/>                    | <span data-ttu-id="4fc43-145">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="4fc43-145">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="4fc43-146">IID</span><span class="sxs-lookup"><span data-stu-id="4fc43-146">IID</span></span><br/>                      | <span data-ttu-id="4fc43-147">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="4fc43-147">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="4fc43-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fc43-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc43-149">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="4fc43-149">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="4fc43-150">**SWbemPrivilegeSet 新增**</span><span class="sxs-lookup"><span data-stu-id="4fc43-150">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> <dt>

[<span data-ttu-id="4fc43-151">**SWbemPrivilegeSet。移除**</span><span class="sxs-lookup"><span data-stu-id="4fc43-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="4fc43-152">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="4fc43-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="4fc43-153">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="4fc43-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="4fc43-154">執行具有特殊許可權的作業</span><span class="sxs-lookup"><span data-stu-id="4fc43-154">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="4fc43-155">使用 VBScript 執行特殊許可權作業</span><span class="sxs-lookup"><span data-stu-id="4fc43-155">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

