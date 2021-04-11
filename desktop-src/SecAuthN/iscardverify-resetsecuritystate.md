---
description: 重設智慧卡的目前安全性內容。
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: ISCardVerify：： ResetSecurityState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba96d400258fb58957c8c263438160d6710806db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847721"
---
# <a name="iscardverifyresetsecuritystate-method"></a><span data-ttu-id="6adce-103">ISCardVerify：： ResetSecurityState 方法</span><span class="sxs-lookup"><span data-stu-id="6adce-103">ISCardVerify::ResetSecurityState method</span></span>

<span data-ttu-id="6adce-104">\[**ResetSecurityState** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6adce-104">\[The **ResetSecurityState** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6adce-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6adce-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6adce-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6adce-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6adce-107">**ResetSecurityState** 方法會重設 [*智慧卡*](../secgloss/s-gly.md)的目前 [*安全性內容*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6adce-107">The **ResetSecurityState** method resets the current [*security context*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6adce-108">語法</span><span class="sxs-lookup"><span data-stu-id="6adce-108">Syntax</span></span>


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a><span data-ttu-id="6adce-109">參數</span><span class="sxs-lookup"><span data-stu-id="6adce-109">Parameters</span></span>

<span data-ttu-id="6adce-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6adce-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6adce-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6adce-111">Return value</span></span>

<span data-ttu-id="6adce-112">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="6adce-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="6adce-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6adce-113">Return code</span></span>                                                                                   | <span data-ttu-id="6adce-114">Description</span><span class="sxs-lookup"><span data-stu-id="6adce-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6adce-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6adce-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6adce-116">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="6adce-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6adce-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6adce-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6adce-118">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="6adce-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6adce-119">備註</span><span class="sxs-lookup"><span data-stu-id="6adce-119">Remarks</span></span>

<span data-ttu-id="6adce-120">若要重新啟用 [*安全性內容*](../secgloss/s-gly.md) 而不重設，請呼叫 [**解除封鎖**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6adce-120">To re-enable the [*security context*](../secgloss/s-gly.md) without resetting, call [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span></span>

<span data-ttu-id="6adce-121">如需此介面所定義之所有方法的清單，請參閱 [**ISCardVerify**](iscardverify.md)。</span><span class="sxs-lookup"><span data-stu-id="6adce-121">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="6adce-122">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6adce-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6adce-123">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6adce-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6adce-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6adce-124">Requirements</span></span>



| <span data-ttu-id="6adce-125">需求</span><span class="sxs-lookup"><span data-stu-id="6adce-125">Requirement</span></span> | <span data-ttu-id="6adce-126">值</span><span class="sxs-lookup"><span data-stu-id="6adce-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6adce-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6adce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6adce-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6adce-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6adce-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6adce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6adce-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6adce-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6adce-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6adce-131">End of client support</span></span><br/>    | <span data-ttu-id="6adce-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6adce-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6adce-133">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6adce-133">End of server support</span></span><br/>    | <span data-ttu-id="6adce-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6adce-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6adce-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6adce-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6adce-136">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="6adce-136">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

<span data-ttu-id="6adce-137">[**疏通**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6adce-137">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>
</dt> </dl>

 

 
