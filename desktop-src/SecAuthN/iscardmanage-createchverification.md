---
description: 建立 ISCardVerify 介面。
ms.assetid: 6338e672-83cd-46fe-8f94-f4ba6e2581ea
title: ISCardManage：： CreateCHVerification 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCHVerification
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a5909a8782571f9bd01a1c31e5ccd04c3d029df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194505"
---
# <a name="iscardmanagecreatechverification-method"></a><span data-ttu-id="43003-103">ISCardManage：： CreateCHVerification 方法</span><span class="sxs-lookup"><span data-stu-id="43003-103">ISCardManage::CreateCHVerification method</span></span>

<span data-ttu-id="43003-104">\[**CreateCHVerification** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="43003-104">\[The **CreateCHVerification** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="43003-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="43003-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="43003-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="43003-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="43003-107">**CreateCHVerification** 方法會建立 [**ISCardVerify**](iscardverify.md)介面。</span><span class="sxs-lookup"><span data-stu-id="43003-107">The **CreateCHVerification** method creates an [**ISCardVerify**](iscardverify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="43003-108">語法</span><span class="sxs-lookup"><span data-stu-id="43003-108">Syntax</span></span>


```C++
HRESULT CreateCHVerification(
  [out] ISCardVerify **ppISCardVerify
);
```



## <a name="parameters"></a><span data-ttu-id="43003-109">參數</span><span class="sxs-lookup"><span data-stu-id="43003-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43003-110">*ppISCardVerify* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="43003-110">*ppISCardVerify* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43003-111">傳回已建立之 [**ISCardVerify**](iscardverify.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="43003-111">Returned pointer to the created [**ISCardVerify**](iscardverify.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43003-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="43003-112">Return value</span></span>

<span data-ttu-id="43003-113">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="43003-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="43003-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="43003-114">Return code</span></span>                                                                                   | <span data-ttu-id="43003-115">Description</span><span class="sxs-lookup"><span data-stu-id="43003-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="43003-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="43003-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="43003-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="43003-117">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="43003-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="43003-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="43003-119">*PpISCardVerify* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="43003-119">The *ppISCardVerify* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="43003-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="43003-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="43003-121">在 *ppISCardVerify* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="43003-121">A bad pointer was passed in *ppISCardVerify*.</span></span><br/> |
| <dl> <span data-ttu-id="43003-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="43003-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="43003-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="43003-123">Out of memory.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="43003-124">備註</span><span class="sxs-lookup"><span data-stu-id="43003-124">Remarks</span></span>

<span data-ttu-id="43003-125">如需此介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。</span><span class="sxs-lookup"><span data-stu-id="43003-125">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="43003-126">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="43003-126">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="43003-127">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="43003-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43003-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="43003-128">Requirements</span></span>



| <span data-ttu-id="43003-129">需求</span><span class="sxs-lookup"><span data-stu-id="43003-129">Requirement</span></span> | <span data-ttu-id="43003-130">值</span><span class="sxs-lookup"><span data-stu-id="43003-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="43003-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43003-131">Minimum supported client</span></span><br/> | <span data-ttu-id="43003-132">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43003-132">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="43003-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43003-133">Minimum supported server</span></span><br/> | <span data-ttu-id="43003-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43003-134">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="43003-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="43003-135">End of client support</span></span><br/>    | <span data-ttu-id="43003-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="43003-136">Windows XP</span></span><br/>                                |
| <span data-ttu-id="43003-137">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="43003-137">End of server support</span></span><br/>    | <span data-ttu-id="43003-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="43003-138">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="43003-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43003-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43003-140">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="43003-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="43003-141">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="43003-141">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
