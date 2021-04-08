---
title: 'EnumerationFlagNonXmlText 方法 (WSManDisp .h) '
description: 傳回列舉常數 WSManFlagNonXmlText 的值，以用於 Session 的 flags 參數。列舉方法。
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- EnumerationFlagNonXmlText 方法 Windows 遠端管理
- EnumerationFlagNonXmlText 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，EnumerationFlagNonXmlText 方法
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a9547f85a07702dc3735129842e5bc286ee9b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686122"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a><span data-ttu-id="74765-106">WSMan. EnumerationFlagNonXmlText 方法</span><span class="sxs-lookup"><span data-stu-id="74765-106">WSMan.EnumerationFlagNonXmlText method</span></span>

<span data-ttu-id="74765-107">**EnumerationFlagNonXmlText** 會傳回列舉常數 **WSManFlagNonXmlText** 的值，以用於 Session 的 *flags* 參數。[**列舉**](session-enumerate.md)方法。</span><span class="sxs-lookup"><span data-stu-id="74765-107">The **WSMan.EnumerationFlagNonXmlText** returns the value of the enumeration constant **WSManFlagNonXmlText** for use in the *flags* parameter of the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="74765-108">這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。</span><span class="sxs-lookup"><span data-stu-id="74765-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="74765-109">如需如何呼叫這個方法的詳細資訊，請參閱 [會話常數](session-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="74765-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="74765-110">**WSManFlagNonXmlText** 是 **\_ \_ WSManEnumFlags** 列舉中的常數。</span><span class="sxs-lookup"><span data-stu-id="74765-110">**WSManFlagNonXmlText** is a constant in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="74765-111">如需詳細資訊，請參閱 [**列舉常數**](enumeration-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="74765-111">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="74765-112">語法</span><span class="sxs-lookup"><span data-stu-id="74765-112">Syntax</span></span>


```VB
WSMan.EnumerationFlagNonXmlText( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="74765-113">參數</span><span class="sxs-lookup"><span data-stu-id="74765-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74765-114">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="74765-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74765-115">常數的值。</span><span class="sxs-lookup"><span data-stu-id="74765-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74765-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="74765-116">Return value</span></span>

<span data-ttu-id="74765-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="74765-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="74765-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="74765-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="74765-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="74765-119">Requirements</span></span>



| <span data-ttu-id="74765-120">需求</span><span class="sxs-lookup"><span data-stu-id="74765-120">Requirement</span></span> | <span data-ttu-id="74765-121">值</span><span class="sxs-lookup"><span data-stu-id="74765-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="74765-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74765-122">Minimum supported client</span></span><br/> | <span data-ttu-id="74765-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74765-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="74765-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74765-124">Minimum supported server</span></span><br/> | <span data-ttu-id="74765-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74765-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="74765-126">標頭</span><span class="sxs-lookup"><span data-stu-id="74765-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="74765-127"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="74765-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="74765-128">Idl</span><span class="sxs-lookup"><span data-stu-id="74765-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="74765-129"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="74765-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="74765-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="74765-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="74765-131"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="74765-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="74765-132">DLL</span><span class="sxs-lookup"><span data-stu-id="74765-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74765-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74765-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74765-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74765-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74765-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="74765-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="74765-136">**IWSManEx**</span><span class="sxs-lookup"><span data-stu-id="74765-136">**IWSManEx**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[<span data-ttu-id="74765-137">**Iwsmansession.invoke**</span><span class="sxs-lookup"><span data-stu-id="74765-137">**IWSManSession**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





