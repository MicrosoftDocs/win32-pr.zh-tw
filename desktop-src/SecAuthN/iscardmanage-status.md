---
description: 取得智慧卡或讀取器的目前狀態。
ms.assetid: ae285e2e-6591-43ab-b92f-1ec755872379
title: ISCardManage：： Status 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 26683823b5b709d86b36f4345b47f306f2000ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971735"
---
# <a name="iscardmanagestatus-method"></a><span data-ttu-id="b9eea-103">ISCardManage：： Status 方法</span><span class="sxs-lookup"><span data-stu-id="b9eea-103">ISCardManage::Status method</span></span>

<span data-ttu-id="b9eea-104">\[**Status** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b9eea-104">\[The **Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b9eea-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="b9eea-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b9eea-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="b9eea-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b9eea-107">**Status** 方法會取得 [*智慧卡*](../secgloss/s-gly.md)或 [*讀取器*](../secgloss/r-gly.md)的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b9eea-107">The **Status** method gets the current status of the [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9eea-108">語法</span><span class="sxs-lookup"><span data-stu-id="b9eea-108">Syntax</span></span>


```C++
HRESULT Status(
  [out] SCARD_STATES    *pStatus,
  [out] SCARD_PROTOCOLS *pProtocols
);
```



## <a name="parameters"></a><span data-ttu-id="b9eea-109">參數</span><span class="sxs-lookup"><span data-stu-id="b9eea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9eea-110">*pStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b9eea-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9eea-111">捨棄 \_ 狀態列舉值的指標。</span><span class="sxs-lookup"><span data-stu-id="b9eea-111">Pointer to an SCARD\_STATES enumeration value.</span></span> <span data-ttu-id="b9eea-112">傳回時，包含目前的狀態/狀態。</span><span class="sxs-lookup"><span data-stu-id="b9eea-112">On return, contains the current status/state.</span></span>

</dd> <dt>

<span data-ttu-id="b9eea-113">*pProtocols* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b9eea-113">*pProtocols* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9eea-114">捨棄 \_ 通訊協定列舉值的指標。</span><span class="sxs-lookup"><span data-stu-id="b9eea-114">Pointer to an SCARD\_PROTOCOLS enumeration value.</span></span> <span data-ttu-id="b9eea-115">傳回時，包含目前的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b9eea-115">On return, contains the current protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9eea-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9eea-116">Return value</span></span>

<span data-ttu-id="b9eea-117">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="b9eea-117">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="b9eea-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b9eea-118">Return code</span></span>                                                                                   | <span data-ttu-id="b9eea-119">Description</span><span class="sxs-lookup"><span data-stu-id="b9eea-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b9eea-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b9eea-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b9eea-121">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="b9eea-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b9eea-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b9eea-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b9eea-123">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="b9eea-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="b9eea-124"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="b9eea-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b9eea-125">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="b9eea-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="b9eea-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b9eea-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b9eea-127">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="b9eea-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b9eea-128">備註</span><span class="sxs-lookup"><span data-stu-id="b9eea-128">Remarks</span></span>

<span data-ttu-id="b9eea-129">如需此介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。</span><span class="sxs-lookup"><span data-stu-id="b9eea-129">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="b9eea-130">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b9eea-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b9eea-131">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="b9eea-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9eea-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9eea-132">Requirements</span></span>



| <span data-ttu-id="b9eea-133">需求</span><span class="sxs-lookup"><span data-stu-id="b9eea-133">Requirement</span></span> | <span data-ttu-id="b9eea-134">值</span><span class="sxs-lookup"><span data-stu-id="b9eea-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9eea-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9eea-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b9eea-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9eea-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b9eea-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9eea-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b9eea-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9eea-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b9eea-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b9eea-139">End of client support</span></span><br/>    | <span data-ttu-id="b9eea-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b9eea-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b9eea-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="b9eea-141">End of server support</span></span><br/>    | <span data-ttu-id="b9eea-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b9eea-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b9eea-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9eea-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9eea-144">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="b9eea-144">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
