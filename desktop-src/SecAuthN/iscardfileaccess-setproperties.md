---
description: SetProperties 方法會設定指定之物件的 TLVs (tag、length、value) 所參考的基本類型。
ms.assetid: f8f75c8e-14f4-4bc4-b49d-b232ede374b0
title: ISCardFileAccess：： SetProperties 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.SetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: b54c2193ec17bca9f9b3ba00b2c2bc133707dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982376"
---
# <a name="iscardfileaccesssetproperties-method"></a><span data-ttu-id="0c6e9-103">ISCardFileAccess：： SetProperties 方法</span><span class="sxs-lookup"><span data-stu-id="0c6e9-103">ISCardFileAccess::SetProperties method</span></span>

<span data-ttu-id="0c6e9-104">\[**SetProperties** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-104">\[The **SetProperties** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0c6e9-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0c6e9-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="0c6e9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0c6e9-107">**SetProperties** 方法會設定指定之物件的 TLVs (tag、length、value) 所參考的基本類型。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-107">The **SetProperties** method sets the primitive referred by TLVs (tag, length, value) for the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c6e9-108">語法</span><span class="sxs-lookup"><span data-stu-id="0c6e9-108">Syntax</span></span>


```C++
HRESULT SetProperties(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags,
  [in] LPTLV_TABLE pTable
);
```



## <a name="parameters"></a><span data-ttu-id="0c6e9-109">參數</span><span class="sxs-lookup"><span data-stu-id="0c6e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c6e9-110">*refType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c6e9-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c6e9-111">*BstrPathSpec* 中使用的參考型別。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="0c6e9-112">**SC \_ 類型（ \_ 依 \_ 名稱）**</span><span class="sxs-lookup"><span data-stu-id="0c6e9-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="0c6e9-113">**SC \_ 類型（ \_ 依 \_ 識別碼）**</span><span class="sxs-lookup"><span data-stu-id="0c6e9-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="0c6e9-114">**SC \_ 類型 \_ （ \_ 簡短）**</span><span class="sxs-lookup"><span data-stu-id="0c6e9-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="0c6e9-115">**SC \_ 類型（ \_ 依 \_ 任何**</span><span class="sxs-lookup"><span data-stu-id="0c6e9-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0c6e9-116">*bstrPathSpec* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c6e9-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c6e9-117">檔案</span><span class="sxs-lookup"><span data-stu-id="0c6e9-117">File.</span></span>

</dd> <dt>

<span data-ttu-id="0c6e9-118">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c6e9-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c6e9-119">指定是否應使用安全訊息。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-119">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="0c6e9-120">**SC \_ FL \_ 安全 \_ 訊息**</span><span class="sxs-lookup"><span data-stu-id="0c6e9-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0c6e9-121">*pTable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0c6e9-121">*pTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c6e9-122">應設定其值的 TLV 結構指標。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-122">Pointer to TLV structures whose value should be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c6e9-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c6e9-123">Return value</span></span>

<span data-ttu-id="0c6e9-124">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-124">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0c6e9-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0c6e9-125">Return code</span></span>                                                                                   | <span data-ttu-id="0c6e9-126">Description</span><span class="sxs-lookup"><span data-stu-id="0c6e9-126">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0c6e9-127"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0c6e9-127"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0c6e9-128">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-128">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0c6e9-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0c6e9-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0c6e9-130">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-130">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="0c6e9-131"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="0c6e9-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0c6e9-132">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-132">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="0c6e9-133"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0c6e9-133"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0c6e9-134">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-134">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0c6e9-135">備註</span><span class="sxs-lookup"><span data-stu-id="0c6e9-135">Remarks</span></span>

<span data-ttu-id="0c6e9-136">如需此介面所定義之所有方法的清單，請參閱 [**ISCardFileAccess**](iscardfileaccess.md)。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="0c6e9-137">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-137">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0c6e9-138">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="0c6e9-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c6e9-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c6e9-139">Requirements</span></span>



| <span data-ttu-id="0c6e9-140">需求</span><span class="sxs-lookup"><span data-stu-id="0c6e9-140">Requirement</span></span> | <span data-ttu-id="0c6e9-141">值</span><span class="sxs-lookup"><span data-stu-id="0c6e9-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c6e9-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c6e9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0c6e9-143">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c6e9-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0c6e9-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c6e9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0c6e9-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c6e9-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0c6e9-146">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0c6e9-146">End of client support</span></span><br/>    | <span data-ttu-id="0c6e9-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c6e9-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="0c6e9-148">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="0c6e9-148">End of server support</span></span><br/>    | <span data-ttu-id="0c6e9-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c6e9-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="0c6e9-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c6e9-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c6e9-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="0c6e9-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
