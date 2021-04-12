---
description: Delete 方法會刪除智慧卡檔案系統內指定位置的檔案。
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: ISCardFileAccess：:D elete 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6331225cd3baf105682e2d275ad6be53f16f5b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318416"
---
# <a name="iscardfileaccessdelete-method"></a><span data-ttu-id="9d2fc-103">ISCardFileAccess：:D elete 方法</span><span class="sxs-lookup"><span data-stu-id="9d2fc-103">ISCardFileAccess::Delete method</span></span>

<span data-ttu-id="9d2fc-104">\[**Delete** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9d2fc-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9d2fc-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="9d2fc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9d2fc-107">**Delete** 方法會刪除 [*智慧卡*](../secgloss/s-gly.md)檔案系統內指定位置的檔案。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-107">The **Delete** method deletes a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d2fc-108">語法</span><span class="sxs-lookup"><span data-stu-id="9d2fc-108">Syntax</span></span>


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="9d2fc-109">參數</span><span class="sxs-lookup"><span data-stu-id="9d2fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d2fc-110">*refType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d2fc-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d2fc-111">*BstrPathSpec* 中使用的參考型別。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="9d2fc-112">**SC \_ 類型（ \_ 依 \_ 名稱）**</span><span class="sxs-lookup"><span data-stu-id="9d2fc-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="9d2fc-113">**SC \_ 類型（ \_ 依 \_ 識別碼）**</span><span class="sxs-lookup"><span data-stu-id="9d2fc-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="9d2fc-114">**SC \_ 類型 \_ （ \_ 簡短）**</span><span class="sxs-lookup"><span data-stu-id="9d2fc-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="9d2fc-115">**SC \_ 類型（ \_ 依 \_ 任何**</span><span class="sxs-lookup"><span data-stu-id="9d2fc-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="9d2fc-116">*bstrPathSpec* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d2fc-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d2fc-117">要刪除之檔案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-117">Identifier of the file to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="9d2fc-118">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d2fc-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d2fc-119">指定是否必須使用安全訊息，並預先配置資料。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-119">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="9d2fc-120">**SC \_ FL \_ 安全 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="9d2fc-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="9d2fc-121">**SC \_ FL 預先配置 \_**</span><span class="sxs-lookup"><span data-stu-id="9d2fc-121">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d2fc-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d2fc-122">Return value</span></span>

<span data-ttu-id="9d2fc-123">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9d2fc-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9d2fc-124">Return code</span></span>                                                                                  | <span data-ttu-id="9d2fc-125">Description</span><span class="sxs-lookup"><span data-stu-id="9d2fc-125">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="9d2fc-126"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9d2fc-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9d2fc-127">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-127">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="9d2fc-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9d2fc-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9d2fc-129">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-129">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="9d2fc-130"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="9d2fc-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="9d2fc-131">介面尚未執行此方法。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-131">The interface has not implemented this method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9d2fc-132">備註</span><span class="sxs-lookup"><span data-stu-id="9d2fc-132">Remarks</span></span>

<span data-ttu-id="9d2fc-133">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="9d2fc-134">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9d2fc-135">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="9d2fc-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d2fc-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d2fc-136">Requirements</span></span>



| <span data-ttu-id="9d2fc-137">需求</span><span class="sxs-lookup"><span data-stu-id="9d2fc-137">Requirement</span></span> | <span data-ttu-id="9d2fc-138">值</span><span class="sxs-lookup"><span data-stu-id="9d2fc-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9d2fc-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d2fc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9d2fc-140">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d2fc-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9d2fc-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d2fc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9d2fc-142">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d2fc-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9d2fc-143">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9d2fc-143">End of client support</span></span><br/>    | <span data-ttu-id="9d2fc-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d2fc-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="9d2fc-145">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9d2fc-145">End of server support</span></span><br/>    | <span data-ttu-id="9d2fc-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d2fc-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="9d2fc-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d2fc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d2fc-148">**建立**</span><span class="sxs-lookup"><span data-stu-id="9d2fc-148">**Create**</span></span>](iscardfileaccess-create.md)
</dt> <dt>

[<span data-ttu-id="9d2fc-149">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="9d2fc-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
