---
description: 鎖定已連線的智慧卡以進行獨佔使用。
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: ISCardManage：： SCardLock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192211"
---
# <a name="iscardmanagescardlock-method"></a><span data-ttu-id="e6daa-103">ISCardManage：： SCardLock 方法</span><span class="sxs-lookup"><span data-stu-id="e6daa-103">ISCardManage::SCardLock method</span></span>

<span data-ttu-id="e6daa-104">\[**SCardLock** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e6daa-104">\[The **SCardLock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e6daa-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="e6daa-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e6daa-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e6daa-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e6daa-107">**SCardLock** 方法會鎖定連線的 [*智慧卡*](../secgloss/s-gly.md)以供獨佔使用。</span><span class="sxs-lookup"><span data-stu-id="e6daa-107">The **SCardLock** method locks a connected [*smart card*](../secgloss/s-gly.md) for exclusive use.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6daa-108">語法</span><span class="sxs-lookup"><span data-stu-id="e6daa-108">Syntax</span></span>


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a><span data-ttu-id="e6daa-109">參數</span><span class="sxs-lookup"><span data-stu-id="e6daa-109">Parameters</span></span>

<span data-ttu-id="e6daa-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e6daa-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6daa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6daa-111">Return value</span></span>

<span data-ttu-id="e6daa-112">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="e6daa-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="e6daa-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e6daa-113">Return code</span></span>                                                                            | <span data-ttu-id="e6daa-114">Description</span><span class="sxs-lookup"><span data-stu-id="e6daa-114">Description</span></span>                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e6daa-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e6daa-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e6daa-116">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="e6daa-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e6daa-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="e6daa-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e6daa-118">作業無法完成。</span><span class="sxs-lookup"><span data-stu-id="e6daa-118">Operation failed to complete.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e6daa-119">備註</span><span class="sxs-lookup"><span data-stu-id="e6daa-119">Remarks</span></span>

<span data-ttu-id="e6daa-120">若要釋出已連接智慧卡的獨佔使用，請呼叫 [**SCardUnlock**](iscardmanage-scardunlock.md)。</span><span class="sxs-lookup"><span data-stu-id="e6daa-120">To releases exclusive use of the connected smart card, call [**SCardUnlock**](iscardmanage-scardunlock.md).</span></span>

<span data-ttu-id="e6daa-121">如需此介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。</span><span class="sxs-lookup"><span data-stu-id="e6daa-121">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="e6daa-122">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e6daa-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e6daa-123">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="e6daa-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6daa-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6daa-124">Requirements</span></span>



| <span data-ttu-id="e6daa-125">需求</span><span class="sxs-lookup"><span data-stu-id="e6daa-125">Requirement</span></span> | <span data-ttu-id="e6daa-126">值</span><span class="sxs-lookup"><span data-stu-id="e6daa-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6daa-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6daa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e6daa-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6daa-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e6daa-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6daa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e6daa-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6daa-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e6daa-131">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e6daa-131">End of client support</span></span><br/>    | <span data-ttu-id="e6daa-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e6daa-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="e6daa-133">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e6daa-133">End of server support</span></span><br/>    | <span data-ttu-id="e6daa-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e6daa-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="e6daa-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6daa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6daa-136">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="e6daa-136">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="e6daa-137">**SCardUnlock**</span><span class="sxs-lookup"><span data-stu-id="e6daa-137">**SCardUnlock**</span></span>](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
