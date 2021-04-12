---
description: SWbemPrivilegeSet 物件的 Item 方法會傳回集合中的 SWbemPrivilege 物件。 Item 方法是 SWbemPrivilegeSet 物件的預設方法。
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet 專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848615"
---
# <a name="swbemprivilegesetitem-method"></a><span data-ttu-id="b89df-104">SWbemPrivilegeSet 專案方法</span><span class="sxs-lookup"><span data-stu-id="b89df-104">SWbemPrivilegeSet.Item method</span></span>

<span data-ttu-id="b89df-105">[**SWbemPrivilegeSet**](swbemprivilegeset.md)物件的 **Item** 方法會傳回集合中的 [**SWbemPrivilege**](swbemprivilege.md)物件。</span><span class="sxs-lookup"><span data-stu-id="b89df-105">The **Item** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object returns an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="b89df-106">**Item** 方法是 **SWbemPrivilegeSet** 物件的預設方法。</span><span class="sxs-lookup"><span data-stu-id="b89df-106">The **Item** method is the default method of an **SWbemPrivilegeSet** object.</span></span>

<span data-ttu-id="b89df-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="b89df-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b89df-108">語法</span><span class="sxs-lookup"><span data-stu-id="b89df-108">Syntax</span></span>


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="b89df-109">參數</span><span class="sxs-lookup"><span data-stu-id="b89df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b89df-110">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="b89df-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="b89df-111">必要。</span><span class="sxs-lookup"><span data-stu-id="b89df-111">Required.</span></span> <span data-ttu-id="b89df-112">[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)群組中的其中一個 WMI 常數。</span><span class="sxs-lookup"><span data-stu-id="b89df-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="b89df-113">這些常數基本上是代表特定許可權的整數。</span><span class="sxs-lookup"><span data-stu-id="b89df-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="b89df-114">例如，若要取得可讓您關閉 Windows 系統的許可權，請使用 **wbemPrivilegeShutdown** 常數或等同于 23 (0x17) 的數位。</span><span class="sxs-lookup"><span data-stu-id="b89df-114">For example, to get the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 23 (0x17).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b89df-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b89df-115">Return value</span></span>

<span data-ttu-id="b89df-116">如果成功，則會傳回要求的 [**SWbemPrivilege**](swbemprivilege.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b89df-116">If successful, the requested [**SWbemPrivilege**](swbemprivilege.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b89df-117">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b89df-117">Error codes</span></span>

<span data-ttu-id="b89df-118">當 **專案** 方法完成時， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b89df-118">Upon the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b89df-119">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="b89df-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b89df-120">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b89df-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b89df-121">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="b89df-121">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="b89df-122">指定的許可權不存在。</span><span class="sxs-lookup"><span data-stu-id="b89df-122">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b89df-123">範例</span><span class="sxs-lookup"><span data-stu-id="b89df-123">Examples</span></span>

<span data-ttu-id="b89df-124">下列 VBScript 程式碼範例使用 **Item** 方法</span><span class="sxs-lookup"><span data-stu-id="b89df-124">The following VBScript code example uses the **Item** method</span></span>


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a><span data-ttu-id="b89df-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b89df-125">Requirements</span></span>



| <span data-ttu-id="b89df-126">需求</span><span class="sxs-lookup"><span data-stu-id="b89df-126">Requirement</span></span> | <span data-ttu-id="b89df-127">值</span><span class="sxs-lookup"><span data-stu-id="b89df-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b89df-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b89df-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b89df-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b89df-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b89df-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b89df-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b89df-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b89df-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b89df-132">標頭</span><span class="sxs-lookup"><span data-stu-id="b89df-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b89df-133"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="b89df-133"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b89df-134">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b89df-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="b89df-135"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b89df-135"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b89df-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b89df-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b89df-137"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b89df-137"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b89df-138">CLSID</span><span class="sxs-lookup"><span data-stu-id="b89df-138">CLSID</span></span><br/>                    | <span data-ttu-id="b89df-139">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="b89df-139">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="b89df-140">IID</span><span class="sxs-lookup"><span data-stu-id="b89df-140">IID</span></span><br/>                      | <span data-ttu-id="b89df-141">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="b89df-141">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="b89df-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b89df-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b89df-143">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="b89df-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="b89df-144">執行具有特殊許可權的作業</span><span class="sxs-lookup"><span data-stu-id="b89df-144">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="b89df-145">**SWbemPrivilege**</span><span class="sxs-lookup"><span data-stu-id="b89df-145">**SWbemPrivilege**</span></span>](swbemprivilege.md)
</dt> </dl>

 

 




