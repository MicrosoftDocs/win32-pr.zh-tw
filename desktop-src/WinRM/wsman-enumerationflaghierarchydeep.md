---
title: 'EnumerationFlagHierarchyDeep 方法 (WSManDisp .h) '
description: 傳回列舉旗標 EnumerationFlagHierarchyDeep 的值，以用於 Session 的 flags 參數。
ms.assetid: b84b82fa-0b2e-418e-850f-6d7a4749fdc1
ms.tgt_platform: multiple
keywords:
- EnumerationFlagHierarchyDeep 方法 Windows 遠端管理
- EnumerationFlagHierarchyDeep 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，EnumerationFlagHierarchyDeep 方法
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeep
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61982c6117d0a91ec253af35657f0cbbf5af12c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934957"
---
# <a name="wsmanenumerationflaghierarchydeep-method"></a><span data-ttu-id="12188-106">WSMan. EnumerationFlagHierarchyDeep 方法</span><span class="sxs-lookup"><span data-stu-id="12188-106">WSMan.EnumerationFlagHierarchyDeep method</span></span>

<span data-ttu-id="12188-107">**EnumerationFlagHierarchyDeep** 方法會傳回列舉旗標 **EnumerationFlagHierarchyDeep** 的值，以用於 [**Session**](session-enumerate.md)的 *flags* 參數。</span><span class="sxs-lookup"><span data-stu-id="12188-107">The **EnumerationFlagHierarchyDeep** method returns the value of the enumeration flag **EnumerationFlagHierarchyDeep** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="12188-108">這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。</span><span class="sxs-lookup"><span data-stu-id="12188-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="12188-109">如需如何呼叫這個方法的詳細資訊，請參閱 [會話常數](session-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="12188-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="12188-110">**EnumerationFlagHierarchyDeep** 是 **\_ WSManEnumFlags** 列舉中的常數，並且會在 [**列舉常數**](enumeration-constants.md)中描述。</span><span class="sxs-lookup"><span data-stu-id="12188-110">**EnumerationFlagHierarchyDeep** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="12188-111">語法</span><span class="sxs-lookup"><span data-stu-id="12188-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyDeep( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="12188-112">參數</span><span class="sxs-lookup"><span data-stu-id="12188-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12188-113">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="12188-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12188-114">常數的值。</span><span class="sxs-lookup"><span data-stu-id="12188-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12188-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="12188-115">Return value</span></span>

<span data-ttu-id="12188-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="12188-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="12188-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="12188-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="12188-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="12188-118">Requirements</span></span>



| <span data-ttu-id="12188-119">需求</span><span class="sxs-lookup"><span data-stu-id="12188-119">Requirement</span></span> | <span data-ttu-id="12188-120">值</span><span class="sxs-lookup"><span data-stu-id="12188-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12188-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12188-121">Minimum supported client</span></span><br/> | <span data-ttu-id="12188-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12188-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="12188-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12188-123">Minimum supported server</span></span><br/> | <span data-ttu-id="12188-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12188-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="12188-125">標頭</span><span class="sxs-lookup"><span data-stu-id="12188-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="12188-126"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="12188-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="12188-127">Idl</span><span class="sxs-lookup"><span data-stu-id="12188-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12188-128"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="12188-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="12188-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="12188-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="12188-130"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="12188-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="12188-131">DLL</span><span class="sxs-lookup"><span data-stu-id="12188-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12188-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12188-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12188-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12188-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12188-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="12188-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="12188-135">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="12188-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





