---
description: 釋出已連接智慧卡的專用用途。
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: ISCardManage：： SCardUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192209"
---
# <a name="iscardmanagescardunlock-method"></a><span data-ttu-id="2ab1b-103">ISCardManage：： SCardUnlock 方法</span><span class="sxs-lookup"><span data-stu-id="2ab1b-103">ISCardManage::SCardUnlock method</span></span>

<span data-ttu-id="2ab1b-104">\[**SCardUnlock** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-104">\[The **SCardUnlock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2ab1b-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2ab1b-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="2ab1b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2ab1b-107">**SCardUnlock** 方法會釋出已連接 [*智慧卡*](../secgloss/s-gly.md)的專用用途。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-107">The **SCardUnlock** method releases exclusive use of the connected [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab1b-108">語法</span><span class="sxs-lookup"><span data-stu-id="2ab1b-108">Syntax</span></span>


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="2ab1b-109">參數</span><span class="sxs-lookup"><span data-stu-id="2ab1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ab1b-110">*處置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2ab1b-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab1b-111">釋放鎖定時要離開智慧卡的狀態。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-111">The state to leave the smart card in when the lock is released.</span></span>

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

<span data-ttu-id="2ab1b-112">**離開**</span><span class="sxs-lookup"><span data-stu-id="2ab1b-112">**LEAVE**</span></span>
</dt><span id="RESET"></span><span id="reset"></span><dt>

<span data-ttu-id="2ab1b-113">**RESET**</span><span class="sxs-lookup"><span data-stu-id="2ab1b-113">**RESET**</span></span>
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

<span data-ttu-id="2ab1b-114">**UNPOWER**</span><span class="sxs-lookup"><span data-stu-id="2ab1b-114">**UNPOWER**</span></span>
</dt><span id="EJECT"></span><span id="eject"></span><dt>

<span data-ttu-id="2ab1b-115">**彈出**</span><span class="sxs-lookup"><span data-stu-id="2ab1b-115">**EJECT**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ab1b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ab1b-116">Return value</span></span>

<span data-ttu-id="2ab1b-117">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2ab1b-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2ab1b-118">Return code</span></span>                                                                                  | <span data-ttu-id="2ab1b-119">Description</span><span class="sxs-lookup"><span data-stu-id="2ab1b-119">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="2ab1b-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2ab1b-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2ab1b-121">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-121">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="2ab1b-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2ab1b-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2ab1b-123">*處置* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-123">The *Disposition* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2ab1b-124">備註</span><span class="sxs-lookup"><span data-stu-id="2ab1b-124">Remarks</span></span>

<span data-ttu-id="2ab1b-125">若要鎖定連接的智慧卡，請呼叫 [**SCardLock**](iscardmanage-scardlock.md)。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-125">To lock the connected smart card, call [**SCardLock**](iscardmanage-scardlock.md).</span></span>

<span data-ttu-id="2ab1b-126">如需此介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="2ab1b-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2ab1b-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="2ab1b-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab1b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ab1b-129">Requirements</span></span>



| <span data-ttu-id="2ab1b-130">需求</span><span class="sxs-lookup"><span data-stu-id="2ab1b-130">Requirement</span></span> | <span data-ttu-id="2ab1b-131">值</span><span class="sxs-lookup"><span data-stu-id="2ab1b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2ab1b-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ab1b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2ab1b-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ab1b-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2ab1b-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ab1b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2ab1b-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ab1b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2ab1b-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2ab1b-136">End of client support</span></span><br/>    | <span data-ttu-id="2ab1b-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2ab1b-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="2ab1b-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2ab1b-138">End of server support</span></span><br/>    | <span data-ttu-id="2ab1b-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ab1b-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="2ab1b-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ab1b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab1b-141">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="2ab1b-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="2ab1b-142">**SCardLock**</span><span class="sxs-lookup"><span data-stu-id="2ab1b-142">**SCardLock**</span></span>](iscardmanage-scardlock.md)
</dt> </dl>

 

 
