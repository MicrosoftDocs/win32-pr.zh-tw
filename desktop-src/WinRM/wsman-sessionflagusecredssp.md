---
title: 'SessionFlagUseCredSsp 方法 (WSManDisp .h) '
description: 傳回 WSManFlagUseCredSsp authentication 旗標的值，以便在 CreateSession 方法的 flags 參數中使用。
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- SessionFlagUseCredSsp 方法 Windows 遠端管理
- SessionFlagUseCredSsp 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，SessionFlagUseCredSsp 方法
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465405"
---
# <a name="wsmansessionflagusecredssp-method"></a><span data-ttu-id="bf1c6-106">WSMan. SessionFlagUseCredSsp 方法</span><span class="sxs-lookup"><span data-stu-id="bf1c6-106">WSMan.SessionFlagUseCredSsp method</span></span>

<span data-ttu-id="bf1c6-107">傳回 **WSManFlagUseCredSsp** authentication 旗標的值，以便在 [**CreateSession**](wsman-createsession.md)方法的 *flags* 參數中使用。</span><span class="sxs-lookup"><span data-stu-id="bf1c6-107">Returns the value of the **WSManFlagUseCredSsp** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="bf1c6-108">這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。</span><span class="sxs-lookup"><span data-stu-id="bf1c6-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="bf1c6-109">如需如何呼叫這個方法的詳細資訊，請參閱 [會話常數](session-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="bf1c6-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="bf1c6-110">**WSManFlagUseCredSsp** 是 **\_ \_ WSManSessionFlags** 列舉中的常數。</span><span class="sxs-lookup"><span data-stu-id="bf1c6-110">**WSManFlagUseCredSsp** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="bf1c6-111">如需詳細資訊，請參閱 [驗證常數](authentication-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="bf1c6-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1c6-112">語法</span><span class="sxs-lookup"><span data-stu-id="bf1c6-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseCredSsp( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="bf1c6-113">參數</span><span class="sxs-lookup"><span data-stu-id="bf1c6-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf1c6-114">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bf1c6-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1c6-115">常數的值。</span><span class="sxs-lookup"><span data-stu-id="bf1c6-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf1c6-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf1c6-116">Return value</span></span>

<span data-ttu-id="bf1c6-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="bf1c6-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bf1c6-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bf1c6-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf1c6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf1c6-119">Requirements</span></span>



| <span data-ttu-id="bf1c6-120">需求</span><span class="sxs-lookup"><span data-stu-id="bf1c6-120">Requirement</span></span> | <span data-ttu-id="bf1c6-121">值</span><span class="sxs-lookup"><span data-stu-id="bf1c6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf1c6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf1c6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bf1c6-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bf1c6-123">Windows 7</span></span><br/>                                                                                                        |
| <span data-ttu-id="bf1c6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf1c6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bf1c6-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf1c6-125">Windows Server 2008 R2</span></span><br/>                                                                                           |
| <span data-ttu-id="bf1c6-126">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="bf1c6-126">Redistributable</span></span><br/>          | <span data-ttu-id="bf1c6-127">Windows Server 2008 （含 SP2）、Windows Vista SP1 和 Windows Vista （含 SP2）的 Windows Management Framework</span><span class="sxs-lookup"><span data-stu-id="bf1c6-127">Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2</span></span><br/> |
| <span data-ttu-id="bf1c6-128">標頭</span><span class="sxs-lookup"><span data-stu-id="bf1c6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf1c6-129"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf1c6-129"><dt>WSManDisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="bf1c6-130">Idl</span><span class="sxs-lookup"><span data-stu-id="bf1c6-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bf1c6-131"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bf1c6-131"><dt>WSManDisp.idl</dt></span></span> </dl>                                    |
| <span data-ttu-id="bf1c6-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="bf1c6-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf1c6-133"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf1c6-133"><dt>WSManDisp.tlb</dt></span></span> </dl>                                    |
| <span data-ttu-id="bf1c6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bf1c6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf1c6-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf1c6-135"><dt>WSMAuto.dll</dt></span></span> </dl>                                      |



## <a name="see-also"></a><span data-ttu-id="bf1c6-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf1c6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1c6-137">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="bf1c6-137">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="bf1c6-138">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="bf1c6-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





