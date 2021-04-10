---
description: GetChallenge 方法會建立應用程式協定資料單位 (APDU) 命令來發出挑戰 (例如，) 用於安全性相關程式的亂數。
ms.assetid: 61f6db1c-b83a-4c1f-8ace-0222a12560ff
title: 'ISCardISO7816：： GetChallenge 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetChallenge
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 05fe18ad73de6c7c3ea30f986c7bb3420bc465b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027186"
---
# <a name="iscardiso7816getchallenge-method"></a><span data-ttu-id="98e82-103">ISCardISO7816：： GetChallenge 方法</span><span class="sxs-lookup"><span data-stu-id="98e82-103">ISCardISO7816::GetChallenge method</span></span>

<span data-ttu-id="98e82-104">\[**GetChallenge** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="98e82-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="98e82-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="98e82-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="98e82-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="98e82-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="98e82-107">**GetChallenge** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令來發出挑戰 (例如，) 用於安全性相關程式的亂數。</span><span class="sxs-lookup"><span data-stu-id="98e82-107">The **GetChallenge** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that issue a challenge (for example, a random number) for use in a security-related procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e82-108">語法</span><span class="sxs-lookup"><span data-stu-id="98e82-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in]      LONG       lBytesExpected,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="98e82-109">參數</span><span class="sxs-lookup"><span data-stu-id="98e82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e82-110">*lBytesExpected* \[在\]</span><span class="sxs-lookup"><span data-stu-id="98e82-110">*lBytesExpected* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98e82-111">預期回應的最大長度。</span><span class="sxs-lookup"><span data-stu-id="98e82-111">Maximum length of the expected response.</span></span>

</dd> <dt>

<span data-ttu-id="98e82-112">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="98e82-112">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98e82-113">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="98e82-113">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="98e82-114">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="98e82-114">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="98e82-115">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並透過 *ppCmd* 指標傳回。</span><span class="sxs-lookup"><span data-stu-id="98e82-115">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e82-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="98e82-116">Return value</span></span>

<span data-ttu-id="98e82-117">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="98e82-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="98e82-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="98e82-118">Return code</span></span>                                                                                   | <span data-ttu-id="98e82-119">Description</span><span class="sxs-lookup"><span data-stu-id="98e82-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="98e82-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="98e82-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="98e82-121">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="98e82-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="98e82-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="98e82-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="98e82-123">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="98e82-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="98e82-124"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="98e82-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="98e82-125">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="98e82-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="98e82-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="98e82-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="98e82-127">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="98e82-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="98e82-128">備註</span><span class="sxs-lookup"><span data-stu-id="98e82-128">Remarks</span></span>

<span data-ttu-id="98e82-129">這項挑戰至少適用于下一個命令。</span><span class="sxs-lookup"><span data-stu-id="98e82-129">The challenge is valid at least for the next command.</span></span>

<span data-ttu-id="98e82-130">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="98e82-130">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="98e82-131">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="98e82-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="98e82-132">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="98e82-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98e82-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="98e82-133">Requirements</span></span>



| <span data-ttu-id="98e82-134">需求</span><span class="sxs-lookup"><span data-stu-id="98e82-134">Requirement</span></span> | <span data-ttu-id="98e82-135">值</span><span class="sxs-lookup"><span data-stu-id="98e82-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98e82-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98e82-136">Minimum supported client</span></span><br/> | <span data-ttu-id="98e82-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98e82-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="98e82-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98e82-138">Minimum supported server</span></span><br/> | <span data-ttu-id="98e82-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98e82-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98e82-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="98e82-140">End of client support</span></span><br/>    | <span data-ttu-id="98e82-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="98e82-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="98e82-142">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="98e82-142">End of server support</span></span><br/>    | <span data-ttu-id="98e82-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="98e82-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="98e82-144">標頭</span><span class="sxs-lookup"><span data-stu-id="98e82-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="98e82-145"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="98e82-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="98e82-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="98e82-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="98e82-147"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="98e82-147"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="98e82-148">DLL</span><span class="sxs-lookup"><span data-stu-id="98e82-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98e82-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98e82-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="98e82-150">IID</span><span class="sxs-lookup"><span data-stu-id="98e82-150">IID</span></span><br/>                      | <span data-ttu-id="98e82-151">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="98e82-151">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="98e82-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98e82-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e82-153">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="98e82-153">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="98e82-154">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="98e82-154">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="98e82-155">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="98e82-155">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
