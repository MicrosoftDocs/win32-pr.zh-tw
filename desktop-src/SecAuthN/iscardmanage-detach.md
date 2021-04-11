---
description: 分別釋出 AttachByHandle 和 AttachByIFD 所配置的特定智慧卡或讀取器的附件。
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: ISCardManage：:D etach 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc5a48f76a643447b3e3d836d61ad7a769c56ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114537"
---
# <a name="iscardmanagedetach-method"></a><span data-ttu-id="448f2-103">ISCardManage：:D etach 方法</span><span class="sxs-lookup"><span data-stu-id="448f2-103">ISCardManage::Detach method</span></span>

<span data-ttu-id="448f2-104">\[卸 **離** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="448f2-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="448f2-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="448f2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="448f2-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="448f2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="448f2-107">卸 **離** 方法會分別將附件釋出至特定 [*智慧卡*](../secgloss/s-gly.md)或 [**AttachByHandle**](iscardmanage-attachbyhandle.md)和 [**AttachByIFD**](iscardmanage-attachbyifd.md)所配置的 [*讀取器*](../secgloss/r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="448f2-107">The **Detach** method releases the attachment to a particular [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) allocated by [**AttachByHandle**](iscardmanage-attachbyhandle.md) and [**AttachByIFD**](iscardmanage-attachbyifd.md) respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="448f2-108">語法</span><span class="sxs-lookup"><span data-stu-id="448f2-108">Syntax</span></span>


```C++
HRESULT Detach();
```



## <a name="parameters"></a><span data-ttu-id="448f2-109">參數</span><span class="sxs-lookup"><span data-stu-id="448f2-109">Parameters</span></span>

<span data-ttu-id="448f2-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="448f2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="448f2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="448f2-111">Return value</span></span>

<span data-ttu-id="448f2-112">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="448f2-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="448f2-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="448f2-113">Return code</span></span>                                                                                   | <span data-ttu-id="448f2-114">Description</span><span class="sxs-lookup"><span data-stu-id="448f2-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="448f2-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="448f2-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="448f2-116">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="448f2-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="448f2-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="448f2-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="448f2-118">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="448f2-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="448f2-119">備註</span><span class="sxs-lookup"><span data-stu-id="448f2-119">Remarks</span></span>

<span data-ttu-id="448f2-120">連接智慧卡呼叫 [**AttachByHandle**](iscardmanage-attachbyhandle.md) 或 [**AttachByIFD**](iscardmanage-attachbyifd.md)。</span><span class="sxs-lookup"><span data-stu-id="448f2-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="448f2-121">若要在不呼叫卸 **離** 和 [**AttachByHandle**](iscardmanage-attachbyhandle.md)的情況下與智慧卡重新連接，請呼叫 [**reconnect**](iscardmanage-reconnect.md)。</span><span class="sxs-lookup"><span data-stu-id="448f2-121">To reconnect with the smart card without calling **Detach** and [**AttachByHandle**](iscardmanage-attachbyhandle.md), call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="448f2-122">如需此介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。</span><span class="sxs-lookup"><span data-stu-id="448f2-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="448f2-123">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="448f2-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="448f2-124">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="448f2-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="448f2-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="448f2-125">Requirements</span></span>



| <span data-ttu-id="448f2-126">需求</span><span class="sxs-lookup"><span data-stu-id="448f2-126">Requirement</span></span> | <span data-ttu-id="448f2-127">值</span><span class="sxs-lookup"><span data-stu-id="448f2-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="448f2-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="448f2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="448f2-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="448f2-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="448f2-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="448f2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="448f2-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="448f2-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="448f2-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="448f2-132">End of client support</span></span><br/>    | <span data-ttu-id="448f2-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="448f2-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="448f2-134">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="448f2-134">End of server support</span></span><br/>    | <span data-ttu-id="448f2-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="448f2-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="448f2-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="448f2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448f2-137">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="448f2-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="448f2-138">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="448f2-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="448f2-139">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="448f2-139">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="448f2-140">**重新連接**</span><span class="sxs-lookup"><span data-stu-id="448f2-140">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
