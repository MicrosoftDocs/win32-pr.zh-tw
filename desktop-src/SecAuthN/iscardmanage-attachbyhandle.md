---
description: 使用智慧卡資源管理員所傳回的控制碼，建立智慧卡 (ICC) 的通訊連結。
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: ISCardManage：： AttachByHandle 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849896"
---
# <a name="iscardmanageattachbyhandle-method"></a><span data-ttu-id="0a74a-103">ISCardManage：： AttachByHandle 方法</span><span class="sxs-lookup"><span data-stu-id="0a74a-103">ISCardManage::AttachByHandle method</span></span>

<span data-ttu-id="0a74a-104">\[**AttachByHandle** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="0a74a-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0a74a-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="0a74a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0a74a-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="0a74a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0a74a-107">**AttachByHandle** 方法會使用智慧卡 [*資源管理員*](../secgloss/r-gly.md)所傳回的控制碼，建立 [*智慧卡*](../secgloss/s-gly.md) (ICC) 的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="0a74a-107">The **AttachByHandle** method creates a communication link to a [*smart card*](../secgloss/s-gly.md) (ICC) using a handle returned by the smart card [*resource manager*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a74a-108">語法</span><span class="sxs-lookup"><span data-stu-id="0a74a-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a><span data-ttu-id="0a74a-109">參數</span><span class="sxs-lookup"><span data-stu-id="0a74a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a74a-110">*hICC* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0a74a-110">*hICC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a74a-111">智慧卡的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0a74a-111">A handle to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a74a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a74a-112">Return value</span></span>

<span data-ttu-id="0a74a-113">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="0a74a-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="0a74a-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0a74a-114">Return code</span></span>                                                                                   | <span data-ttu-id="0a74a-115">Description</span><span class="sxs-lookup"><span data-stu-id="0a74a-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="0a74a-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0a74a-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0a74a-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="0a74a-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="0a74a-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0a74a-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0a74a-119">*HICC* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="0a74a-119">The *hICC* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="0a74a-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0a74a-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0a74a-121">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="0a74a-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="0a74a-122">備註</span><span class="sxs-lookup"><span data-stu-id="0a74a-122">Remarks</span></span>

<span data-ttu-id="0a74a-123">附加 [*讀取器*](../secgloss/r-gly.md) 呼叫 [**AttachByIFD**](iscardmanage-attachbyifd.md)。</span><span class="sxs-lookup"><span data-stu-id="0a74a-123">To attach a [*reader*](../secgloss/r-gly.md) call [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="0a74a-124">若要釋放附件呼叫卸 [**離**](iscardmanage-detach.md)。</span><span class="sxs-lookup"><span data-stu-id="0a74a-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="0a74a-125">若要在不呼叫卸 [**離**](iscardmanage-detach.md) 和 **AttachByHandle** 的情況下與智慧卡重新連接，請呼叫 [**reconnect**](iscardmanage-reconnect.md)。</span><span class="sxs-lookup"><span data-stu-id="0a74a-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByHandle**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="0a74a-126">如需 [**ISCardManage**](iscardmanage.md) 介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。</span><span class="sxs-lookup"><span data-stu-id="0a74a-126">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="0a74a-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0a74a-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0a74a-128">如需智慧卡錯誤碼的詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="0a74a-128">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a74a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a74a-129">Requirements</span></span>



| <span data-ttu-id="0a74a-130">需求</span><span class="sxs-lookup"><span data-stu-id="0a74a-130">Requirement</span></span> | <span data-ttu-id="0a74a-131">值</span><span class="sxs-lookup"><span data-stu-id="0a74a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a74a-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a74a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0a74a-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a74a-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0a74a-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a74a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0a74a-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a74a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0a74a-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0a74a-136">End of client support</span></span><br/>    | <span data-ttu-id="0a74a-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0a74a-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="0a74a-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="0a74a-138">End of server support</span></span><br/>    | <span data-ttu-id="0a74a-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0a74a-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="0a74a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a74a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a74a-141">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="0a74a-141">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="0a74a-142">**中斷連結**</span><span class="sxs-lookup"><span data-stu-id="0a74a-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="0a74a-143">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="0a74a-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="0a74a-144">**重新連接**</span><span class="sxs-lookup"><span data-stu-id="0a74a-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
