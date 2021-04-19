---
description: 使指定的檔案 (EF 或 DF) 無效。 使用加速復原之前，其他方法無法存取不正確檔案。
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: ISCardFileAccess：：無效方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e1d74885f97eca64f403155f1dba52e398b9426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979286"
---
# <a name="iscardfileaccessinvalidate-method"></a><span data-ttu-id="51bca-104">ISCardFileAccess：：無效方法</span><span class="sxs-lookup"><span data-stu-id="51bca-104">ISCardFileAccess::Invalidate method</span></span>

<span data-ttu-id="51bca-105">\[無效 **的方法可** 用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="51bca-105">\[The **Invalidate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="51bca-106">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="51bca-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="51bca-107">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="51bca-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="51bca-108">無效 **方法會** 使指定的檔案 (EF 或 DF) 無效。</span><span class="sxs-lookup"><span data-stu-id="51bca-108">The **Invalidate** method makes the specified file (EF or DF) not valid.</span></span> <span data-ttu-id="51bca-109">使用 [**加速復原**](iscardfileaccess-rehabilitate.md)之前，其他方法無法存取不正確檔案。</span><span class="sxs-lookup"><span data-stu-id="51bca-109">A file that is not valid cannot be accessed by other methods prior to using [**Rehabilitate**](iscardfileaccess-rehabilitate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="51bca-110">語法</span><span class="sxs-lookup"><span data-stu-id="51bca-110">Syntax</span></span>


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="51bca-111">參數</span><span class="sxs-lookup"><span data-stu-id="51bca-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51bca-112">*bstrPathSpec* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51bca-112">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51bca-113">檔案</span><span class="sxs-lookup"><span data-stu-id="51bca-113">File.</span></span>

</dd> <dt>

<span data-ttu-id="51bca-114">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51bca-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51bca-115">指定是否應使用安全訊息。</span><span class="sxs-lookup"><span data-stu-id="51bca-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="51bca-116">**SC \_ FL \_ 安全 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="51bca-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51bca-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="51bca-117">Return value</span></span>

<span data-ttu-id="51bca-118">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="51bca-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="51bca-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="51bca-119">Return code</span></span>                                                                                   | <span data-ttu-id="51bca-120">Description</span><span class="sxs-lookup"><span data-stu-id="51bca-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="51bca-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="51bca-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="51bca-122">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="51bca-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="51bca-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="51bca-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="51bca-124">參數無效。</span><span class="sxs-lookup"><span data-stu-id="51bca-124">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="51bca-125"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="51bca-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="51bca-126">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="51bca-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="51bca-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="51bca-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="51bca-128">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="51bca-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="51bca-129">備註</span><span class="sxs-lookup"><span data-stu-id="51bca-129">Remarks</span></span>

<span data-ttu-id="51bca-130">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="51bca-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="51bca-131">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="51bca-131">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="51bca-132">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="51bca-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51bca-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="51bca-133">Requirements</span></span>



| <span data-ttu-id="51bca-134">需求</span><span class="sxs-lookup"><span data-stu-id="51bca-134">Requirement</span></span> | <span data-ttu-id="51bca-135">值</span><span class="sxs-lookup"><span data-stu-id="51bca-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51bca-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51bca-136">Minimum supported client</span></span><br/> | <span data-ttu-id="51bca-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51bca-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="51bca-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51bca-138">Minimum supported server</span></span><br/> | <span data-ttu-id="51bca-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51bca-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="51bca-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="51bca-140">End of client support</span></span><br/>    | <span data-ttu-id="51bca-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="51bca-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="51bca-142">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="51bca-142">End of server support</span></span><br/>    | <span data-ttu-id="51bca-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51bca-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="51bca-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51bca-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51bca-145">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="51bca-145">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="51bca-146">**恢復**</span><span class="sxs-lookup"><span data-stu-id="51bca-146">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
