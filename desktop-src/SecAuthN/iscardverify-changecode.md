---
description: 以新的 CHV 代碼取代目前的 CHV (卡持有者驗證) 程式碼。
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: ISCardVerify：： ChangeCode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6fcb6d79e6135293ad91e3ea18fa535ef4edbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693320"
---
# <a name="iscardverifychangecode-method"></a><span data-ttu-id="b741d-103">ISCardVerify：： ChangeCode 方法</span><span class="sxs-lookup"><span data-stu-id="b741d-103">ISCardVerify::ChangeCode method</span></span>

<span data-ttu-id="b741d-104">\[**ChangeCode** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b741d-104">\[The **ChangeCode** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b741d-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="b741d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b741d-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="b741d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b741d-107">**ChangeCode** 方法會以新的 CHV 程式碼取代目前的 CHV (卡持有者驗證) 程式碼。</span><span class="sxs-lookup"><span data-stu-id="b741d-107">The **ChangeCode** method replaces the current CHV (card holder verification) code with new CHV code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b741d-108">語法</span><span class="sxs-lookup"><span data-stu-id="b741d-108">Syntax</span></span>


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="b741d-109">參數</span><span class="sxs-lookup"><span data-stu-id="b741d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b741d-110">*pOldCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b741d-110">*pOldCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b741d-111">[**IByteBuffer**](ibytebuffer.md)的指標，其中包含使用者的目前程式碼。</span><span class="sxs-lookup"><span data-stu-id="b741d-111">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the user's current code.</span></span>

</dd> <dt>

<span data-ttu-id="b741d-112">*pNewCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b741d-112">*pNewCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b741d-113">包含新程式碼的 [**IByteBuffer**](ibytebuffer.md) 指標，該程式碼會在變更過程中向 [*智慧卡*](../secgloss/s-gly.md) 呈現，以驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="b741d-113">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the new code that will be presented to the [*smart card*](../secgloss/s-gly.md) during the change process to authenticate the user.</span></span>

</dd> <dt>

<span data-ttu-id="b741d-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b741d-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b741d-115">指出程式碼為全域或本機，以及程式碼是否應啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="b741d-115">Indicates whether the code is global or local, and whether the code should be enabled or disabled.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="b741d-116">**SC \_ FL \_ 的 \_ 通用**</span><span class="sxs-lookup"><span data-stu-id="b741d-116">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="b741d-117">**SC \_ FL \_ 的 \_ 本機 IHV**</span><span class="sxs-lookup"><span data-stu-id="b741d-117">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

<span data-ttu-id="b741d-118">**SC \_ FL 的 \_ IHV \_ 啟用**</span><span class="sxs-lookup"><span data-stu-id="b741d-118">**SC\_FL\_IHV\_ENABLE**</span></span>
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

<span data-ttu-id="b741d-119">**SC \_ FL 的 \_ IHV \_ 停用**</span><span class="sxs-lookup"><span data-stu-id="b741d-119">**SC\_FL\_IHV\_DISABLE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b741d-120">*lRef* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b741d-120">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b741d-121">智慧卡特定參考。</span><span class="sxs-lookup"><span data-stu-id="b741d-121">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b741d-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="b741d-122">Return value</span></span>

<span data-ttu-id="b741d-123">方法會傳回下列其中一個可能的值：</span><span class="sxs-lookup"><span data-stu-id="b741d-123">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="b741d-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b741d-124">Return code</span></span>                                                                                   | <span data-ttu-id="b741d-125">Description</span><span class="sxs-lookup"><span data-stu-id="b741d-125">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b741d-126"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b741d-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b741d-127">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="b741d-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b741d-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b741d-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b741d-129">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="b741d-129">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="b741d-130"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="b741d-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b741d-131">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="b741d-131">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="b741d-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b741d-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b741d-133">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="b741d-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b741d-134">備註</span><span class="sxs-lookup"><span data-stu-id="b741d-134">Remarks</span></span>

<span data-ttu-id="b741d-135">如需此介面所定義之所有方法的清單，請參閱 [**ISCardVerify**](iscardverify.md)。</span><span class="sxs-lookup"><span data-stu-id="b741d-135">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="b741d-136">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b741d-136">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b741d-137">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="b741d-137">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b741d-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="b741d-138">Requirements</span></span>



| <span data-ttu-id="b741d-139">需求</span><span class="sxs-lookup"><span data-stu-id="b741d-139">Requirement</span></span> | <span data-ttu-id="b741d-140">值</span><span class="sxs-lookup"><span data-stu-id="b741d-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b741d-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b741d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b741d-142">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b741d-142">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b741d-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b741d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b741d-144">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b741d-144">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b741d-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b741d-145">End of client support</span></span><br/>    | <span data-ttu-id="b741d-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b741d-146">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b741d-147">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="b741d-147">End of server support</span></span><br/>    | <span data-ttu-id="b741d-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b741d-148">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b741d-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b741d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b741d-150">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="b741d-150">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> <dt>

[<span data-ttu-id="b741d-151">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="b741d-151">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

[<span data-ttu-id="b741d-152">智慧卡傳回值</span><span class="sxs-lookup"><span data-stu-id="b741d-152">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
