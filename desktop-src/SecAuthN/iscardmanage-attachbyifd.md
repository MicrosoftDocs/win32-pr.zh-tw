---
description: 使用提供的讀取器顯示名稱，建立讀取器的通訊連結。
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: ISCardManage：： AttachByIFD 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980337"
---
# <a name="iscardmanageattachbyifd-method"></a><span data-ttu-id="c9f0d-103">ISCardManage：： AttachByIFD 方法</span><span class="sxs-lookup"><span data-stu-id="c9f0d-103">ISCardManage::AttachByIFD method</span></span>

<span data-ttu-id="c9f0d-104">\[**AttachByIFD** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-104">\[The **AttachByIFD** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c9f0d-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c9f0d-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c9f0d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c9f0d-107">**AttachByIFD** 方法會使用提供的讀取器顯示名稱，建立 [*讀取器*](../secgloss/r-gly.md)的通訊連結。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-107">The **AttachByIFD** method creates a communication link to a [*reader*](../secgloss/r-gly.md), using a supplied display name for the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f0d-108">語法</span><span class="sxs-lookup"><span data-stu-id="c9f0d-108">Syntax</span></span>


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a><span data-ttu-id="c9f0d-109">參數</span><span class="sxs-lookup"><span data-stu-id="c9f0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9f0d-110">*bstrIFDName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9f0d-110">*bstrIFDName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9f0d-111">讀取器的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-111">The display name of the reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9f0d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9f0d-112">Return value</span></span>

<span data-ttu-id="c9f0d-113">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="c9f0d-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="c9f0d-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c9f0d-114">Return code</span></span>                                                                                   | <span data-ttu-id="c9f0d-115">Description</span><span class="sxs-lookup"><span data-stu-id="c9f0d-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="c9f0d-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f0d-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c9f0d-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="c9f0d-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f0d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c9f0d-119">*BstrIFDName* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-119">The *bstrIFDName* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="c9f0d-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c9f0d-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c9f0d-121">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-121">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="c9f0d-122">備註</span><span class="sxs-lookup"><span data-stu-id="c9f0d-122">Remarks</span></span>

<span data-ttu-id="c9f0d-123">連接 [*智慧卡*](../secgloss/s-gly.md) 通話 [**AttachByHandle**](iscardmanage-attachbyhandle.md)。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-123">To attach a [*smart card*](../secgloss/s-gly.md) call [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span></span>

<span data-ttu-id="c9f0d-124">若要釋放附件呼叫卸 [**離**](iscardmanage-detach.md)。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="c9f0d-125">若要在不呼叫卸 [**離**](iscardmanage-detach.md) 和 **AttachByIFD** 的情況下與智慧卡重新連接，請呼叫 [**reconnect**](iscardmanage-reconnect.md)。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByIFD**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="c9f0d-126">如需此介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="c9f0d-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c9f0d-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="c9f0d-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9f0d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9f0d-129">Requirements</span></span>



| <span data-ttu-id="c9f0d-130">需求</span><span class="sxs-lookup"><span data-stu-id="c9f0d-130">Requirement</span></span> | <span data-ttu-id="c9f0d-131">值</span><span class="sxs-lookup"><span data-stu-id="c9f0d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9f0d-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9f0d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c9f0d-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9f0d-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c9f0d-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9f0d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c9f0d-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9f0d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c9f0d-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c9f0d-136">End of client support</span></span><br/>    | <span data-ttu-id="c9f0d-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c9f0d-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="c9f0d-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c9f0d-138">End of server support</span></span><br/>    | <span data-ttu-id="c9f0d-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9f0d-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="c9f0d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9f0d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f0d-141">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="c9f0d-141">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="c9f0d-142">**中斷連結**</span><span class="sxs-lookup"><span data-stu-id="c9f0d-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="c9f0d-143">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="c9f0d-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="c9f0d-144">**重新連接**</span><span class="sxs-lookup"><span data-stu-id="c9f0d-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
