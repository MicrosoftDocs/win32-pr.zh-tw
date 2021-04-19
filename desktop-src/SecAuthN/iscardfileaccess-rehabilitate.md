---
description: 使用不正確方法（可由應用程式存取），使檔案 (EF 或 DF) 。
ms.assetid: 1906fcc5-ae76-4950-b2eb-e5ce1882637f
title: ISCardFileAccess：：加速復原方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Rehabilitate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7ed02131de08104dab8aff23ee9054659fd4cd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993169"
---
# <a name="iscardfileaccessrehabilitate-method"></a><span data-ttu-id="b40c6-103">ISCardFileAccess：：加速復原方法</span><span class="sxs-lookup"><span data-stu-id="b40c6-103">ISCardFileAccess::Rehabilitate method</span></span>

<span data-ttu-id="b40c6-104">\[**加速復原** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b40c6-104">\[The **Rehabilitate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b40c6-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="b40c6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b40c6-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="b40c6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b40c6-107">**加速復原**[**方法會使用無效方法（**](iscardfileaccess-invalidate.md)可由應用程式存取），將檔案 (EF 或 DF) 。</span><span class="sxs-lookup"><span data-stu-id="b40c6-107">The **Rehabilitate** method makes a file (EF or DF) that was previously made not valid by using the [**Invalidate**](iscardfileaccess-invalidate.md) method, accessible by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="b40c6-108">語法</span><span class="sxs-lookup"><span data-stu-id="b40c6-108">Syntax</span></span>


```C++
HRESULT Rehabilitate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="b40c6-109">參數</span><span class="sxs-lookup"><span data-stu-id="b40c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b40c6-110">*bstrPathSpec* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b40c6-110">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40c6-111">要加速復原的檔案。</span><span class="sxs-lookup"><span data-stu-id="b40c6-111">File to rehabilitate.</span></span>

</dd> <dt>

<span data-ttu-id="b40c6-112">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b40c6-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40c6-113">指定是否應使用安全訊息。</span><span class="sxs-lookup"><span data-stu-id="b40c6-113">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="b40c6-114">**SC \_ FL \_ 安全 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="b40c6-114">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b40c6-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b40c6-115">Return value</span></span>

<span data-ttu-id="b40c6-116">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="b40c6-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b40c6-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b40c6-117">Return code</span></span>                                                                                   | <span data-ttu-id="b40c6-118">Description</span><span class="sxs-lookup"><span data-stu-id="b40c6-118">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b40c6-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b40c6-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b40c6-120">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="b40c6-120">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b40c6-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b40c6-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b40c6-122">參數無效。</span><span class="sxs-lookup"><span data-stu-id="b40c6-122">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="b40c6-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b40c6-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b40c6-124">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="b40c6-124">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b40c6-125">備註</span><span class="sxs-lookup"><span data-stu-id="b40c6-125">Remarks</span></span>

<span data-ttu-id="b40c6-126">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="b40c6-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="b40c6-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b40c6-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b40c6-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="b40c6-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b40c6-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b40c6-129">Requirements</span></span>



| <span data-ttu-id="b40c6-130">需求</span><span class="sxs-lookup"><span data-stu-id="b40c6-130">Requirement</span></span> | <span data-ttu-id="b40c6-131">值</span><span class="sxs-lookup"><span data-stu-id="b40c6-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b40c6-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b40c6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b40c6-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b40c6-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b40c6-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b40c6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b40c6-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b40c6-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b40c6-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b40c6-136">End of client support</span></span><br/>    | <span data-ttu-id="b40c6-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b40c6-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b40c6-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="b40c6-138">End of server support</span></span><br/>    | <span data-ttu-id="b40c6-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b40c6-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b40c6-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b40c6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b40c6-141">**無效**</span><span class="sxs-lookup"><span data-stu-id="b40c6-141">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)
</dt> <dt>

[<span data-ttu-id="b40c6-142">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="b40c6-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
