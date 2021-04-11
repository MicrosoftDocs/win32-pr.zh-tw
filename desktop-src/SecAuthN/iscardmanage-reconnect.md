---
description: 允許應用程式重新連線到智慧卡或讀取器，而不需要分別發出卸離呼叫和 AttachByHandle 或 AttachByIFD 呼叫。
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: ISCardManage：： Reconnect 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8b05e6292a92267569eb1f53e10f6143554aba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848755"
---
# <a name="iscardmanagereconnect-method"></a><span data-ttu-id="660e1-103">ISCardManage：： Reconnect 方法</span><span class="sxs-lookup"><span data-stu-id="660e1-103">ISCardManage::Reconnect method</span></span>

<span data-ttu-id="660e1-104">\[**Reconnect** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="660e1-104">\[The **Reconnect** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="660e1-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="660e1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="660e1-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="660e1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="660e1-107">**Reconnect** 方法可讓應用程式重新連線到 [*智慧卡*](../secgloss/s-gly.md)或 [*讀取器*](../secgloss/r-gly.md)，而不需要分別發出卸 [**離**](iscardmanage-detach.md)呼叫，然後再發出 [**AttachByHandle**](iscardmanage-attachbyhandle.md)或 [**AttachByIFD**](iscardmanage-attachbyifd.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="660e1-107">The **Reconnect** method allows an application to reconnect to a [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) without having to issue a [**Detach**](iscardmanage-detach.md) call followed by an [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md) call respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="660e1-108">語法</span><span class="sxs-lookup"><span data-stu-id="660e1-108">Syntax</span></span>


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a><span data-ttu-id="660e1-109">參數</span><span class="sxs-lookup"><span data-stu-id="660e1-109">Parameters</span></span>

<span data-ttu-id="660e1-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="660e1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="660e1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="660e1-111">Return value</span></span>

<span data-ttu-id="660e1-112">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="660e1-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="660e1-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="660e1-113">Return code</span></span>                                                                                   | <span data-ttu-id="660e1-114">Description</span><span class="sxs-lookup"><span data-stu-id="660e1-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="660e1-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="660e1-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="660e1-116">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="660e1-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="660e1-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="660e1-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="660e1-118">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="660e1-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="660e1-119">備註</span><span class="sxs-lookup"><span data-stu-id="660e1-119">Remarks</span></span>

<span data-ttu-id="660e1-120">連接智慧卡呼叫 [**AttachByHandle**](iscardmanage-attachbyhandle.md) 或 [**AttachByIFD**](iscardmanage-attachbyifd.md)。</span><span class="sxs-lookup"><span data-stu-id="660e1-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="660e1-121">若要卸離智慧卡，請呼叫卸 [**離**](iscardmanage-detach.md)。</span><span class="sxs-lookup"><span data-stu-id="660e1-121">To detach a smart card, call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="660e1-122">如需此介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。</span><span class="sxs-lookup"><span data-stu-id="660e1-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="660e1-123">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="660e1-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="660e1-124">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="660e1-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="660e1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="660e1-125">Requirements</span></span>



| <span data-ttu-id="660e1-126">需求</span><span class="sxs-lookup"><span data-stu-id="660e1-126">Requirement</span></span> | <span data-ttu-id="660e1-127">值</span><span class="sxs-lookup"><span data-stu-id="660e1-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="660e1-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="660e1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="660e1-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="660e1-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="660e1-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="660e1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="660e1-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="660e1-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="660e1-132">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="660e1-132">End of client support</span></span><br/>    | <span data-ttu-id="660e1-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="660e1-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="660e1-134">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="660e1-134">End of server support</span></span><br/>    | <span data-ttu-id="660e1-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="660e1-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="660e1-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="660e1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="660e1-137">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="660e1-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="660e1-138">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="660e1-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="660e1-139">**中斷連結**</span><span class="sxs-lookup"><span data-stu-id="660e1-139">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="660e1-140">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="660e1-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
