---
description: 要求使用者的驗證。
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: ISCardVerify：： Verify 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976875"
---
# <a name="iscardverifyverify-method"></a><span data-ttu-id="75043-103">ISCardVerify：： Verify 方法</span><span class="sxs-lookup"><span data-stu-id="75043-103">ISCardVerify::Verify method</span></span>

<span data-ttu-id="75043-104">\[[ **驗證** ] 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="75043-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="75043-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="75043-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="75043-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="75043-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="75043-107">**Verify** 方法會要求使用者的驗證。</span><span class="sxs-lookup"><span data-stu-id="75043-107">The **Verify** method requests a verification of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="75043-108">語法</span><span class="sxs-lookup"><span data-stu-id="75043-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="75043-109">參數</span><span class="sxs-lookup"><span data-stu-id="75043-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75043-110">*pCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75043-110">*pCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75043-111">包含要在 CHV (卡持有者驗證) 處理常式中呈現給 [*智慧卡*](../secgloss/s-gly.md) 的程式碼。</span><span class="sxs-lookup"><span data-stu-id="75043-111">Contains the code to be presented to the [*smart card*](../secgloss/s-gly.md) in the CHV (card holder verification) process.</span></span>

</dd> <dt>

<span data-ttu-id="75043-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="75043-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75043-113">指出程式碼是否為全域或本機。</span><span class="sxs-lookup"><span data-stu-id="75043-113">Indicates whether the code is global or local.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="75043-114">**SC \_ FL \_ 的 \_ 通用**</span><span class="sxs-lookup"><span data-stu-id="75043-114">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="75043-115">**SC \_ FL \_ 的 \_ 本機 IHV**</span><span class="sxs-lookup"><span data-stu-id="75043-115">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="75043-116">*lRef* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75043-116">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75043-117">智慧卡特定參考。</span><span class="sxs-lookup"><span data-stu-id="75043-117">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75043-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="75043-118">Return value</span></span>

<span data-ttu-id="75043-119">**Verify** 方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="75043-119">The **Verify** method returns one of the following values:</span></span>



| <span data-ttu-id="75043-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="75043-120">Return code</span></span>                                                                                   | <span data-ttu-id="75043-121">Description</span><span class="sxs-lookup"><span data-stu-id="75043-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="75043-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="75043-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="75043-123">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="75043-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="75043-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="75043-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="75043-125">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="75043-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="75043-126"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="75043-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="75043-127">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="75043-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="75043-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="75043-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="75043-129">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="75043-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="75043-130">備註</span><span class="sxs-lookup"><span data-stu-id="75043-130">Remarks</span></span>

<span data-ttu-id="75043-131">如需此介面所定義之所有方法的清單，請參閱 [**ISCardVerify**](iscardverify.md)。</span><span class="sxs-lookup"><span data-stu-id="75043-131">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="75043-132">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="75043-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="75043-133">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="75043-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75043-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="75043-134">Requirements</span></span>



| <span data-ttu-id="75043-135">需求</span><span class="sxs-lookup"><span data-stu-id="75043-135">Requirement</span></span> | <span data-ttu-id="75043-136">值</span><span class="sxs-lookup"><span data-stu-id="75043-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75043-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75043-137">Minimum supported client</span></span><br/> | <span data-ttu-id="75043-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75043-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="75043-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75043-139">Minimum supported server</span></span><br/> | <span data-ttu-id="75043-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="75043-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="75043-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="75043-141">End of client support</span></span><br/>    | <span data-ttu-id="75043-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="75043-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="75043-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="75043-143">End of server support</span></span><br/>    | <span data-ttu-id="75043-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75043-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="75043-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75043-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75043-146">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="75043-146">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
