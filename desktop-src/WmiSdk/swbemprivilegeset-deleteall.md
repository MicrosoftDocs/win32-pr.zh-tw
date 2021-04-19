---
description: SWbemPrivilegeSet 物件的 DeleteAll 方法會移除集合中的擁有權限，因此將它清空。
ms.assetid: 368caa14-1c53-4090-8569-97ea743905de
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet. DeleteAll 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 382382b0c22c029f41c9ab33fb959287e5222d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985318"
---
# <a name="swbemprivilegesetdeleteall-method"></a><span data-ttu-id="2d0b5-103">SWbemPrivilegeSet. DeleteAll 方法</span><span class="sxs-lookup"><span data-stu-id="2d0b5-103">SWbemPrivilegeSet.DeleteAll method</span></span>

<span data-ttu-id="2d0b5-104">[**SWbemPrivilegeSet**](swbemprivilegeset.md)物件的 **DeleteAll** 方法會移除集合中的擁有權限，因此將它清空。</span><span class="sxs-lookup"><span data-stu-id="2d0b5-104">The **DeleteAll** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object removes all privileges from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d0b5-105">語法</span><span class="sxs-lookup"><span data-stu-id="2d0b5-105">Syntax</span></span>


```VB
SWbemPrivilegeSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="2d0b5-106">參數</span><span class="sxs-lookup"><span data-stu-id="2d0b5-106">Parameters</span></span>

<span data-ttu-id="2d0b5-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2d0b5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d0b5-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d0b5-108">Return value</span></span>

<span data-ttu-id="2d0b5-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2d0b5-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2d0b5-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2d0b5-110">Error codes</span></span>

<span data-ttu-id="2d0b5-111">**DeleteAll** 方法完成後， **Err** 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2d0b5-111">Upon the completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="2d0b5-112">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="2d0b5-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2d0b5-113">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2d0b5-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d0b5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d0b5-114">Requirements</span></span>



| <span data-ttu-id="2d0b5-115">需求</span><span class="sxs-lookup"><span data-stu-id="2d0b5-115">Requirement</span></span> | <span data-ttu-id="2d0b5-116">值</span><span class="sxs-lookup"><span data-stu-id="2d0b5-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d0b5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d0b5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2d0b5-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d0b5-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d0b5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d0b5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2d0b5-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d0b5-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d0b5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2d0b5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d0b5-122"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d0b5-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d0b5-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2d0b5-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d0b5-124"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2d0b5-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2d0b5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2d0b5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d0b5-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d0b5-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2d0b5-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="2d0b5-127">CLSID</span></span><br/>                    | <span data-ttu-id="2d0b5-128">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="2d0b5-128">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="2d0b5-129">IID</span><span class="sxs-lookup"><span data-stu-id="2d0b5-129">IID</span></span><br/>                      | <span data-ttu-id="2d0b5-130">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="2d0b5-130">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="2d0b5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d0b5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d0b5-132">**SWbemPrivilegeSet**</span><span class="sxs-lookup"><span data-stu-id="2d0b5-132">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="2d0b5-133">執行具有特殊許可權的作業</span><span class="sxs-lookup"><span data-stu-id="2d0b5-133">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="2d0b5-134">**SWbemPrivilegeSet。移除**</span><span class="sxs-lookup"><span data-stu-id="2d0b5-134">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> </dl>

 

 




