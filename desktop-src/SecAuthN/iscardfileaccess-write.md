---
description: Write 方法會將資料寫入目前開啟的檔案。
ms.assetid: 0c92af34-a9db-4242-8b6e-d1010a0d7afa
title: ISCardFileAccess：： Write 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 48091d39fff49e54d57f5a26fb7d033bfd8e5952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115337"
---
# <a name="iscardfileaccesswrite-method"></a><span data-ttu-id="e99e2-103">ISCardFileAccess：： Write 方法</span><span class="sxs-lookup"><span data-stu-id="e99e2-103">ISCardFileAccess::Write method</span></span>

<span data-ttu-id="e99e2-104">\[**Write** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e99e2-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e99e2-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="e99e2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e99e2-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e99e2-107">**Write** 方法會將資料寫入目前開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="e99e2-107">The **Write** method writes data to a current opened file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e99e2-108">語法</span><span class="sxs-lookup"><span data-stu-id="e99e2-108">Syntax</span></span>


```C++
HRESULT Write(
  [in] HSCARD_FILE  hFile,
  [in] LPBYTEBUFFER pData,
  [in] SCARD_FLAGS  flags
);
```



## <a name="parameters"></a><span data-ttu-id="e99e2-109">參數</span><span class="sxs-lookup"><span data-stu-id="e99e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e99e2-110">*hFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e2-111">開啟檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e99e2-111">A handle to an open file.</span></span>

</dd> <dt>

<span data-ttu-id="e99e2-112">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e2-113">要寫入的物件/資料。</span><span class="sxs-lookup"><span data-stu-id="e99e2-113">Object/data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="e99e2-114">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e99e2-115">指定是否應使用安全訊息。</span><span class="sxs-lookup"><span data-stu-id="e99e2-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="e99e2-116">**SC \_ FL \_ 安全 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="e99e2-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e99e2-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e99e2-117">Return value</span></span>

<span data-ttu-id="e99e2-118">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="e99e2-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e99e2-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e99e2-119">Return code</span></span>                                                                                   | <span data-ttu-id="e99e2-120">Description</span><span class="sxs-lookup"><span data-stu-id="e99e2-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e99e2-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e99e2-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e99e2-122">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="e99e2-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e99e2-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e99e2-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e99e2-124">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="e99e2-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="e99e2-125"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="e99e2-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e99e2-126">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="e99e2-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="e99e2-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e99e2-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e99e2-128">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="e99e2-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e99e2-129">備註</span><span class="sxs-lookup"><span data-stu-id="e99e2-129">Remarks</span></span>

<span data-ttu-id="e99e2-130">若要開啟或關閉檔案，請分別呼叫 [**open**](iscardfileaccess-open.md) 或 [**close**](iscardfileaccess-close.md)。</span><span class="sxs-lookup"><span data-stu-id="e99e2-130">To open or close a file, call [**Open**](iscardfileaccess-open.md) or [**Close**](iscardfileaccess-close.md), respectively.</span></span>

<span data-ttu-id="e99e2-131">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="e99e2-131">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="e99e2-132">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e99e2-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e99e2-133">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="e99e2-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e99e2-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="e99e2-134">Requirements</span></span>



| <span data-ttu-id="e99e2-135">需求</span><span class="sxs-lookup"><span data-stu-id="e99e2-135">Requirement</span></span> | <span data-ttu-id="e99e2-136">值</span><span class="sxs-lookup"><span data-stu-id="e99e2-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e99e2-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e99e2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e99e2-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e99e2-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e99e2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e99e2-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e99e2-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e99e2-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e99e2-141">End of client support</span></span><br/>    | <span data-ttu-id="e99e2-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e99e2-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="e99e2-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e99e2-143">End of server support</span></span><br/>    | <span data-ttu-id="e99e2-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e99e2-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="e99e2-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e99e2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e99e2-146">**關閉**</span><span class="sxs-lookup"><span data-stu-id="e99e2-146">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="e99e2-147">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="e99e2-147">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="e99e2-148">**打開**</span><span class="sxs-lookup"><span data-stu-id="e99e2-148">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
