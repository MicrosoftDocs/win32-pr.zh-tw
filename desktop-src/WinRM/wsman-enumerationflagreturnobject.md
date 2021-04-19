---
title: 'EnumerationFlagReturnObject 方法 (WSManDisp .h) '
description: 傳回列舉旗標 EnumerationFlagReturnObject 的值，以用於 Session 的 flags 參數。
ms.assetid: a1d82530-63d7-4050-9e82-e31bec93bf38
ms.tgt_platform: multiple
keywords:
- EnumerationFlagReturnObject 方法 Windows 遠端管理
- EnumerationFlagReturnObject 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，EnumerationFlagReturnObject 方法
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObject
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3019f880503f91d1488a2b7a41574cadc2df987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966946"
---
# <a name="wsmanenumerationflagreturnobject-method"></a><span data-ttu-id="5da02-106">WSMan. EnumerationFlagReturnObject 方法</span><span class="sxs-lookup"><span data-stu-id="5da02-106">WSMan.EnumerationFlagReturnObject method</span></span>

<span data-ttu-id="5da02-107">**EnumerationFlagReturnObject** 方法會傳回列舉旗標 **EnumerationFlagReturnObject** 的值，以用於 [**Session**](session-enumerate.md)的 *flags* 參數。</span><span class="sxs-lookup"><span data-stu-id="5da02-107">The **WSMan.EnumerationFlagReturnObject** method returns the value of the enumeration flag **EnumerationFlagReturnObject** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="5da02-108">這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。</span><span class="sxs-lookup"><span data-stu-id="5da02-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="5da02-109">如需如何呼叫這個方法的詳細資訊，請參閱 [會話常數](session-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="5da02-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="5da02-110">**EnumerationFlagReturnObject** 是 **\_ WSManEnumFlags** 列舉中的常數，並且會在 [**列舉常數**](enumeration-constants.md)中描述。</span><span class="sxs-lookup"><span data-stu-id="5da02-110">**EnumerationFlagReturnObject** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5da02-111">語法</span><span class="sxs-lookup"><span data-stu-id="5da02-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagReturnObject( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="5da02-112">參數</span><span class="sxs-lookup"><span data-stu-id="5da02-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5da02-113">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5da02-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5da02-114">常數的值。</span><span class="sxs-lookup"><span data-stu-id="5da02-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5da02-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5da02-115">Return value</span></span>

<span data-ttu-id="5da02-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5da02-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5da02-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5da02-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5da02-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5da02-118">Requirements</span></span>



| <span data-ttu-id="5da02-119">需求</span><span class="sxs-lookup"><span data-stu-id="5da02-119">Requirement</span></span> | <span data-ttu-id="5da02-120">值</span><span class="sxs-lookup"><span data-stu-id="5da02-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5da02-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5da02-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5da02-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5da02-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5da02-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5da02-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5da02-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5da02-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5da02-125">標頭</span><span class="sxs-lookup"><span data-stu-id="5da02-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5da02-126"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="5da02-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5da02-127">Idl</span><span class="sxs-lookup"><span data-stu-id="5da02-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5da02-128"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5da02-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5da02-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="5da02-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="5da02-130"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5da02-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5da02-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5da02-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5da02-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5da02-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5da02-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5da02-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da02-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="5da02-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="5da02-135">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="5da02-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





