---
title: 'SessionFlagUTF8 方法 (WSManDisp .h) '
description: 傳回 WSManFlagUTF8 authentication 旗標的值，以便在 CreateSession 的 flags 參數中使用。
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- SessionFlagUTF8 方法 Windows 遠端管理
- SessionFlagUTF8 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，SessionFlagUTF8 方法
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 985763131c2f3d4227f1a24af612ea3141237832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686336"
---
# <a name="wsmansessionflagutf8-method"></a><span data-ttu-id="4475d-106">WSMan. SessionFlagUTF8 方法</span><span class="sxs-lookup"><span data-stu-id="4475d-106">WSMan.SessionFlagUTF8 method</span></span>

<span data-ttu-id="4475d-107">**SessionFlagUTF8** 方法會傳回 **WSManFlagUTF8** authentication 旗標的值，以用於 [**WSMan. CreateSession**](wsman-createsession.md)的 *flags* 參數。</span><span class="sxs-lookup"><span data-stu-id="4475d-107">The **WSMan.SessionFlagUTF8** method returns the value of the **WSManFlagUTF8** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="4475d-108">這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。</span><span class="sxs-lookup"><span data-stu-id="4475d-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="4475d-109">如需如何呼叫這個方法的詳細資訊，請參閱 [會話常數](session-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="4475d-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="4475d-110">**WSManFlagUTF8** 是 **\_ \_ WSManSessionFlags** 列舉中的常數。</span><span class="sxs-lookup"><span data-stu-id="4475d-110">**WSManFlagUTF8** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="4475d-111">如需詳細資訊，請參閱 [其他會話常數](other-session-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="4475d-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4475d-112">語法</span><span class="sxs-lookup"><span data-stu-id="4475d-112">Syntax</span></span>


```VB
WSMan.SessionFlagUTF8( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="4475d-113">參數</span><span class="sxs-lookup"><span data-stu-id="4475d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4475d-114">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4475d-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4475d-115">常數的值。</span><span class="sxs-lookup"><span data-stu-id="4475d-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4475d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4475d-116">Return value</span></span>

<span data-ttu-id="4475d-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4475d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4475d-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4475d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4475d-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4475d-119">Requirements</span></span>



| <span data-ttu-id="4475d-120">需求</span><span class="sxs-lookup"><span data-stu-id="4475d-120">Requirement</span></span> | <span data-ttu-id="4475d-121">值</span><span class="sxs-lookup"><span data-stu-id="4475d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4475d-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4475d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4475d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4475d-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="4475d-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4475d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4475d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4475d-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4475d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4475d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4475d-127"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="4475d-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4475d-128">Idl</span><span class="sxs-lookup"><span data-stu-id="4475d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4475d-129"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4475d-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="4475d-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="4475d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="4475d-131"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4475d-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4475d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4475d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4475d-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4475d-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4475d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4475d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4475d-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="4475d-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="4475d-136">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="4475d-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





