---
description: SWbemPrivilegeSet 物件的 Add 方法會將 SWbemPrivilege 物件加入至 SWbemPrivilegeSet 集合。 如果集合中已經存在具有相同名稱的許可權，則會予以取代。
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet： Add 方法 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026487"
---
# <a name="swbemprivilegesetadd-method"></a><span data-ttu-id="d7e81-104">SWbemPrivilegeSet 新增方法</span><span class="sxs-lookup"><span data-stu-id="d7e81-104">SWbemPrivilegeSet.Add method</span></span>

<span data-ttu-id="d7e81-105">[**SWbemPrivilegeSet**](swbemprivilegeset.md)物件的 **Add** 方法會將 [**SWbemPrivilege**](swbemprivilege.md)物件加入至 **SWbemPrivilegeSet** 集合。</span><span class="sxs-lookup"><span data-stu-id="d7e81-105">The **Add** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection.</span></span> <span data-ttu-id="d7e81-106">如果集合中已經存在具有相同名稱的許可權，則會予以取代。</span><span class="sxs-lookup"><span data-stu-id="d7e81-106">If a privilege with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="d7e81-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="d7e81-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7e81-108">語法</span><span class="sxs-lookup"><span data-stu-id="d7e81-108">Syntax</span></span>


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d7e81-109">參數</span><span class="sxs-lookup"><span data-stu-id="d7e81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7e81-110">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="d7e81-110">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="d7e81-111">必要。</span><span class="sxs-lookup"><span data-stu-id="d7e81-111">Required.</span></span> <span data-ttu-id="d7e81-112">[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)群組中的其中一個 WMI 常數。</span><span class="sxs-lookup"><span data-stu-id="d7e81-112">One of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="d7e81-113">這些常數基本上是代表特定許可權的整數。</span><span class="sxs-lookup"><span data-stu-id="d7e81-113">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="d7e81-114">例如，若要新增可讓您關閉電腦系統的許可權，請使用 **wbemPrivilegeShutdown** 常數。</span><span class="sxs-lookup"><span data-stu-id="d7e81-114">For example, to add the privilege that allows you to shut down a computer system, use the **wbemPrivilegeShutdown** constant.</span></span> <span data-ttu-id="d7e81-115">在腳本中，您必須使用等同于 23 (0x17) 的數位。</span><span class="sxs-lookup"><span data-stu-id="d7e81-115">In a script, you must use the numeric equivalent of 23 (0x17).</span></span> <span data-ttu-id="d7e81-116">如需這些常數和相關聯的許可權字串的完整清單，請參閱 [**許可權常數**](privilege-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="d7e81-116">For a complete list of these constants and the associated privilege strings, see [**Privilege Constants**](privilege-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7e81-117">*bIsEnabled* \[選\]</span><span class="sxs-lookup"><span data-stu-id="d7e81-117">*bIsEnabled* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7e81-118">啟用或停用此許可權的布林值。</span><span class="sxs-lookup"><span data-stu-id="d7e81-118">Boolean value that enables or disables this privilege.</span></span> <span data-ttu-id="d7e81-119">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d7e81-119">The default value is **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7e81-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7e81-120">Return value</span></span>

<span data-ttu-id="d7e81-121">如果成功，此方法會傳回代表新許可權的 [**SWbemPrivilege**](swbemprivilege.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d7e81-121">If successful, the method returns an [**SWbemPrivilege**](swbemprivilege.md) object that represents the new privilege.</span></span> <span data-ttu-id="d7e81-122">否則，會傳回 null 物件。</span><span class="sxs-lookup"><span data-stu-id="d7e81-122">Otherwise, a null object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d7e81-123">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="d7e81-123">Error codes</span></span>

<span data-ttu-id="d7e81-124">完成 **Add** 方法時， **Err** 物件可能會包含下列清單中的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d7e81-124">Upon the completion of the **Add** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d7e81-125">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="d7e81-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d7e81-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d7e81-126">Unspecified error.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d7e81-127">範例</span><span class="sxs-lookup"><span data-stu-id="d7e81-127">Examples</span></span>

<span data-ttu-id="d7e81-128">使用這個方法的程式碼範例如 [**SWbemPrivilegeSet**](swbemprivilegeset.md) 主題中所述。</span><span class="sxs-lookup"><span data-stu-id="d7e81-128">A code example using this method is described in the [**SWbemPrivilegeSet**](swbemprivilegeset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7e81-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7e81-129">Requirements</span></span>



| <span data-ttu-id="d7e81-130">需求</span><span class="sxs-lookup"><span data-stu-id="d7e81-130">Requirement</span></span> | <span data-ttu-id="d7e81-131">值</span><span class="sxs-lookup"><span data-stu-id="d7e81-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e81-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7e81-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d7e81-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7e81-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7e81-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7e81-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d7e81-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7e81-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7e81-136">標頭</span><span class="sxs-lookup"><span data-stu-id="d7e81-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7e81-137"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7e81-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7e81-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d7e81-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7e81-139"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7e81-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7e81-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d7e81-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7e81-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7e81-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d7e81-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="d7e81-142">CLSID</span></span><br/>                    | <span data-ttu-id="d7e81-143">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="d7e81-143">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="d7e81-144">IID</span><span class="sxs-lookup"><span data-stu-id="d7e81-144">IID</span></span><br/>                      | <span data-ttu-id="d7e81-145">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="d7e81-145">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="d7e81-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7e81-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7e81-147">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="d7e81-147">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="d7e81-148">執行具有特殊許可權的作業</span><span class="sxs-lookup"><span data-stu-id="d7e81-148">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="d7e81-149">使用 VBScript 執行特殊許可權作業</span><span class="sxs-lookup"><span data-stu-id="d7e81-149">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="d7e81-150">**SWbemPrivilegeSet.AddAsString**</span><span class="sxs-lookup"><span data-stu-id="d7e81-150">**SWbemPrivilegeSet.AddAsString**</span></span>](swbemprivilegeset-addasstring.md)
</dt> <dt>

[<span data-ttu-id="d7e81-151">**SWbemPrivilegeSet。移除**</span><span class="sxs-lookup"><span data-stu-id="d7e81-151">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> <dt>

[<span data-ttu-id="d7e81-152">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="d7e81-152">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="d7e81-153">**許可權常數**</span><span class="sxs-lookup"><span data-stu-id="d7e81-153">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




