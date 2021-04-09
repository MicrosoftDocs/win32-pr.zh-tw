---
description: SWbemPrivilegeSet 物件的 Remove 方法會從集合中刪除許可權。
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet： Remove 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f277e291a4296253d7c0b1b11c694952ddc17ddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849561"
---
# <a name="swbemprivilegesetremove-method"></a><span data-ttu-id="2c659-103">SWbemPrivilegeSet 方法</span><span class="sxs-lookup"><span data-stu-id="2c659-103">SWbemPrivilegeSet.Remove method</span></span>

<span data-ttu-id="2c659-104">[**SWbemPrivilegeSet**](swbemprivilegeset.md)物件的 **Remove** 方法會從集合中刪除許可權。</span><span class="sxs-lookup"><span data-stu-id="2c659-104">The **Remove** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object deletes a privilege from the collection.</span></span>

<span data-ttu-id="2c659-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="2c659-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c659-106">語法</span><span class="sxs-lookup"><span data-stu-id="2c659-106">Syntax</span></span>


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="2c659-107">參數</span><span class="sxs-lookup"><span data-stu-id="2c659-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c659-108">*iPrivilege*</span><span class="sxs-lookup"><span data-stu-id="2c659-108">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="2c659-109">必要。</span><span class="sxs-lookup"><span data-stu-id="2c659-109">Required.</span></span> <span data-ttu-id="2c659-110">這是 [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) 群組中的其中一個 WMI 常數。</span><span class="sxs-lookup"><span data-stu-id="2c659-110">This is one of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="2c659-111">這些常數基本上是代表特定許可權的整數。</span><span class="sxs-lookup"><span data-stu-id="2c659-111">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="2c659-112">例如，若要移除允許您關閉 Windows 系統的許可權，請使用 **wbemPrivilegeShutdown** 常數或相當於0x17 的數位。</span><span class="sxs-lookup"><span data-stu-id="2c659-112">For example, to remove the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 0x17.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c659-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c659-113">Return value</span></span>

<span data-ttu-id="2c659-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2c659-114">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2c659-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2c659-115">Error codes</span></span>

<span data-ttu-id="2c659-116">完成 **移除** 方法時， **Err** 物件可能會包含下列清單中的其中一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c659-116">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="2c659-117">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="2c659-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2c659-118">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c659-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2c659-119">**wbemErrNotFound** -2147749890 (0x80041002) </span><span class="sxs-lookup"><span data-stu-id="2c659-119">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="2c659-120">指定的許可權不存在。</span><span class="sxs-lookup"><span data-stu-id="2c659-120">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c659-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c659-121">Requirements</span></span>



| <span data-ttu-id="2c659-122">需求</span><span class="sxs-lookup"><span data-stu-id="2c659-122">Requirement</span></span> | <span data-ttu-id="2c659-123">值</span><span class="sxs-lookup"><span data-stu-id="2c659-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c659-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c659-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2c659-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c659-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c659-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c659-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2c659-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c659-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c659-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2c659-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c659-129"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c659-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c659-130">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2c659-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c659-131"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2c659-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2c659-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2c659-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c659-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c659-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c659-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="2c659-134">CLSID</span></span><br/>                    | <span data-ttu-id="2c659-135">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="2c659-135">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="2c659-136">IID</span><span class="sxs-lookup"><span data-stu-id="2c659-136">IID</span></span><br/>                      | <span data-ttu-id="2c659-137">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="2c659-137">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="2c659-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c659-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c659-139">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="2c659-139">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="2c659-140">**SWbemPrivilegeSet 新增**</span><span class="sxs-lookup"><span data-stu-id="2c659-140">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> </dl>

 

 




