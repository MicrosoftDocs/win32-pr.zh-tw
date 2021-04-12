---
description: SWbemNamedValueSet 物件的 DeleteAll 方法會從集合中移除所有命名值，因此請將它清空。
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet. DeleteAll 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9df7b08dddf4cf9f1a687a262721452c0780267a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193260"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a><span data-ttu-id="fa2ea-103">SWbemNamedValueSet. DeleteAll 方法</span><span class="sxs-lookup"><span data-stu-id="fa2ea-103">SWbemNamedValueSet.DeleteAll method</span></span>

<span data-ttu-id="fa2ea-104">[**SWbemNamedValueSet**](swbemnamedvalueset.md)物件的 **DeleteAll** 方法會從集合中移除所有命名值，因此請將它清空。</span><span class="sxs-lookup"><span data-stu-id="fa2ea-104">The **DeleteAll** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object removes all named values from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa2ea-105">語法</span><span class="sxs-lookup"><span data-stu-id="fa2ea-105">Syntax</span></span>


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="fa2ea-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa2ea-106">Parameters</span></span>

<span data-ttu-id="fa2ea-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fa2ea-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa2ea-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa2ea-108">Return value</span></span>

<span data-ttu-id="fa2ea-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fa2ea-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fa2ea-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="fa2ea-110">Error codes</span></span>

<span data-ttu-id="fa2ea-111">**DeleteAll** 方法完成後， **Err** 物件可能會包含下列錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fa2ea-111">Upon completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="fa2ea-112">**wbemErrFailed** -2147749889 (0x80041001) </span><span class="sxs-lookup"><span data-stu-id="fa2ea-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="fa2ea-113">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fa2ea-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa2ea-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa2ea-114">Requirements</span></span>



| <span data-ttu-id="fa2ea-115">需求</span><span class="sxs-lookup"><span data-stu-id="fa2ea-115">Requirement</span></span> | <span data-ttu-id="fa2ea-116">值</span><span class="sxs-lookup"><span data-stu-id="fa2ea-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2ea-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa2ea-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2ea-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa2ea-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa2ea-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa2ea-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2ea-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa2ea-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa2ea-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fa2ea-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa2ea-122"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa2ea-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa2ea-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fa2ea-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="fa2ea-124"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fa2ea-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fa2ea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fa2ea-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa2ea-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa2ea-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fa2ea-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="fa2ea-127">CLSID</span></span><br/>                    | <span data-ttu-id="fa2ea-128">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="fa2ea-128">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="fa2ea-129">IID</span><span class="sxs-lookup"><span data-stu-id="fa2ea-129">IID</span></span><br/>                      | <span data-ttu-id="fa2ea-130">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="fa2ea-130">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="fa2ea-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa2ea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2ea-132">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="fa2ea-132">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> <dt>

[<span data-ttu-id="fa2ea-133">**SWbemNamedValueSet。移除**</span><span class="sxs-lookup"><span data-stu-id="fa2ea-133">**SWbemNamedValueSet.Remove**</span></span>](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 




