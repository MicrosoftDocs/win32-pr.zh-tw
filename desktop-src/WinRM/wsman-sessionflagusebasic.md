---
title: 'SessionFlagUseBasic 方法 (WSManDisp .h) '
description: 傳回驗證旗標 WSManFlagUseBasic 的值，以便在 CreateSession 方法的 flags 參數中使用。
ms.assetid: 789ecef9-7871-43af-9d63-018f1d99bd09
ms.tgt_platform: multiple
keywords:
- SessionFlagUseBasic 方法 Windows 遠端管理
- SessionFlagUseBasic 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，SessionFlagUseBasic 方法
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseBasic
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41641e0398791ab46c81f71f967f2d43700a2984
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024744"
---
# <a name="wsmansessionflagusebasic-method"></a><span data-ttu-id="bffb9-106">WSMan. SessionFlagUseBasic 方法</span><span class="sxs-lookup"><span data-stu-id="bffb9-106">WSMan.SessionFlagUseBasic method</span></span>

<span data-ttu-id="bffb9-107">**SessionFlagUseBasic** 方法會傳回 authentication 旗 *標* **WSManFlagUseBasic** 的值，以用於 [**WSMan. CreateSession**](wsman-createsession.md)方法的 flags 參數。</span><span class="sxs-lookup"><span data-stu-id="bffb9-107">The **WSMan.SessionFlagUseBasic** method returns the value of the authentication flag **WSManFlagUseBasic** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="bffb9-108">這個方法提供更有效率的語法來使用常數，因此不需要腳本來設定常數值。</span><span class="sxs-lookup"><span data-stu-id="bffb9-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="bffb9-109">如需如何呼叫這個方法的詳細資訊，請參閱 [會話常數](session-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="bffb9-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="bffb9-110">**WSManFlagUseBasic** 是 **\_ \_ WSManSessionFlags** 列舉中的常數。</span><span class="sxs-lookup"><span data-stu-id="bffb9-110">**WSManFlagUseBasic** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="bffb9-111">如需詳細資訊，請參閱 [**驗證常數**](authentication-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="bffb9-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bffb9-112">語法</span><span class="sxs-lookup"><span data-stu-id="bffb9-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseBasic( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="bffb9-113">參數</span><span class="sxs-lookup"><span data-stu-id="bffb9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bffb9-114">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bffb9-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bffb9-115">常數的值。</span><span class="sxs-lookup"><span data-stu-id="bffb9-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bffb9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="bffb9-116">Return value</span></span>

<span data-ttu-id="bffb9-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="bffb9-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bffb9-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bffb9-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bffb9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bffb9-119">Requirements</span></span>



| <span data-ttu-id="bffb9-120">需求</span><span class="sxs-lookup"><span data-stu-id="bffb9-120">Requirement</span></span> | <span data-ttu-id="bffb9-121">值</span><span class="sxs-lookup"><span data-stu-id="bffb9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bffb9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bffb9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bffb9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bffb9-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="bffb9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bffb9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bffb9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bffb9-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bffb9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="bffb9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bffb9-127"><dt>WSManDisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="bffb9-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bffb9-128">Idl</span><span class="sxs-lookup"><span data-stu-id="bffb9-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bffb9-129"><dt>WSManDisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bffb9-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="bffb9-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="bffb9-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="bffb9-131"><dt>WSManDisp .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bffb9-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bffb9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bffb9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bffb9-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bffb9-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bffb9-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bffb9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffb9-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="bffb9-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="bffb9-136">**工作階段**</span><span class="sxs-lookup"><span data-stu-id="bffb9-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





