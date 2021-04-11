---
description: Create 方法會在智慧卡檔案系統內的指定位置建立檔案。
ms.assetid: 6bfe0b22-6aad-4818-bb2a-d5b0af4ee3a6
title: ISCardFileAccess：： Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Create
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2cfc7e1492505191a7912f23e5471f5fa72fdcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113201"
---
# <a name="iscardfileaccesscreate-method"></a><span data-ttu-id="6bbf3-103">ISCardFileAccess：： Create 方法</span><span class="sxs-lookup"><span data-stu-id="6bbf3-103">ISCardFileAccess::Create method</span></span>

<span data-ttu-id="6bbf3-104">\[**Create** 方法可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-104">\[The **Create** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6bbf3-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6bbf3-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6bbf3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6bbf3-107">**Create** 方法會在 [*智慧卡*](../secgloss/s-gly.md)檔案系統內的指定位置建立檔案。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-107">The **Create** method creates a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bbf3-108">語法</span><span class="sxs-lookup"><span data-stu-id="6bbf3-108">Syntax</span></span>


```C++
HRESULT Create(
  [in] REFTYPE      refType,
  [in] BSTR         bstrPathSpec,
  [in] TLV_TABLE    TLV,
  [in] SCARD_FLAGS  flags,
  [in] LPBYTEBUFFER pDataBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="6bbf3-109">參數</span><span class="sxs-lookup"><span data-stu-id="6bbf3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bbf3-110">*refType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6bbf3-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbf3-111">*BstrPathSpec* 中使用的參考型別。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="6bbf3-112">**SC \_ 類型（ \_ 依 \_ 名稱）**</span><span class="sxs-lookup"><span data-stu-id="6bbf3-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="6bbf3-113">**SC \_ 類型（ \_ 依 \_ 識別碼）**</span><span class="sxs-lookup"><span data-stu-id="6bbf3-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="6bbf3-114">**SC \_ 類型 \_ （ \_ 簡短）**</span><span class="sxs-lookup"><span data-stu-id="6bbf3-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="6bbf3-115">**SC \_ 類型（ \_ 依 \_ 任何**</span><span class="sxs-lookup"><span data-stu-id="6bbf3-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="6bbf3-116">*bstrPathSpec* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6bbf3-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbf3-117">要在目前內容中建立的檔案識別碼。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-117">File ID to be created within the current context.</span></span>

</dd> <dt>

<span data-ttu-id="6bbf3-118">*TLV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6bbf3-118">*TLV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbf3-119">您必須設定哪些值，才能 (標記、長度、值) 結構的 TLV 清單。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-119">List of TLV (tag,length,value) structures which values have to be set.</span></span>

</dd> <dt>

<span data-ttu-id="6bbf3-120">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6bbf3-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbf3-121">指定是否必須使用安全訊息，並預先配置資料。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-121">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="6bbf3-122">**SC \_ FL \_ 安全 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="6bbf3-122">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="6bbf3-123">**SC \_ FL 預先配置 \_**</span><span class="sxs-lookup"><span data-stu-id="6bbf3-123">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="6bbf3-124">*pDataBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6bbf3-124">*pDataBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bbf3-125">預先配置資料的指標。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-125">Pointer to preallocated data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bbf3-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="6bbf3-126">Return value</span></span>

<span data-ttu-id="6bbf3-127">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6bbf3-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6bbf3-128">Return code</span></span>                                                                                   | <span data-ttu-id="6bbf3-129">Description</span><span class="sxs-lookup"><span data-stu-id="6bbf3-129">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6bbf3-130"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6bbf3-130"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6bbf3-131">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-131">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6bbf3-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6bbf3-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6bbf3-133">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-133">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6bbf3-134"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="6bbf3-134"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6bbf3-135">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-135">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6bbf3-136"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6bbf3-136"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6bbf3-137">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-137">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6bbf3-138">備註</span><span class="sxs-lookup"><span data-stu-id="6bbf3-138">Remarks</span></span>

<span data-ttu-id="6bbf3-139">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-139">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="6bbf3-140">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-140">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6bbf3-141">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6bbf3-141">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6bbf3-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bbf3-142">Requirements</span></span>



| <span data-ttu-id="6bbf3-143">需求</span><span class="sxs-lookup"><span data-stu-id="6bbf3-143">Requirement</span></span> | <span data-ttu-id="6bbf3-144">值</span><span class="sxs-lookup"><span data-stu-id="6bbf3-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6bbf3-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bbf3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6bbf3-146">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bbf3-146">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6bbf3-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bbf3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6bbf3-148">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bbf3-148">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6bbf3-149">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6bbf3-149">End of client support</span></span><br/>    | <span data-ttu-id="6bbf3-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6bbf3-150">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6bbf3-151">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6bbf3-151">End of server support</span></span><br/>    | <span data-ttu-id="6bbf3-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6bbf3-152">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6bbf3-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bbf3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bbf3-154">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="6bbf3-154">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
