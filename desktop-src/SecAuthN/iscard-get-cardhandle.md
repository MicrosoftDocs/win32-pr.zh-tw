---
description: 抓取已連接智慧卡的控制碼。 \*如果未連接，這個方法會傳回 (pHandle) = = Null。
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: 'ISCard：： get_CardHandle 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d7e945f0f4a300dfed444c7e8f5921b806d96b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936611"
---
# <a name="iscardget_cardhandle-method"></a><span data-ttu-id="d2c62-104">ISCard：： get \_ CardHandle 方法</span><span class="sxs-lookup"><span data-stu-id="d2c62-104">ISCard::get\_CardHandle method</span></span>

<span data-ttu-id="d2c62-105">\[**Get \_ CardHandle** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d2c62-105">\[The **get\_CardHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d2c62-106">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="d2c62-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d2c62-107">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d2c62-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d2c62-108">**Get \_ CardHandle** 方法會抓取連接 [*智慧卡*](../secgloss/s-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d2c62-108">The **get\_CardHandle** method retrieves the handle for a connected [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="d2c62-109">\*如果未連接，這個方法會傳回 (pHandle) = = **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d2c62-109">This method returns (\*pHandle) == **NULL** if not connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c62-110">語法</span><span class="sxs-lookup"><span data-stu-id="d2c62-110">Syntax</span></span>


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a><span data-ttu-id="d2c62-111">參數</span><span class="sxs-lookup"><span data-stu-id="d2c62-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c62-112">*pHandle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d2c62-112">*pHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c62-113">傳回時的智慧卡控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="d2c62-113">Pointer to the card handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2c62-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2c62-114">Return value</span></span>

<span data-ttu-id="d2c62-115">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="d2c62-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d2c62-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d2c62-116">Return code</span></span>                                                                                  | <span data-ttu-id="d2c62-117">Description</span><span class="sxs-lookup"><span data-stu-id="d2c62-117">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="d2c62-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d2c62-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d2c62-119">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="d2c62-119">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="d2c62-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d2c62-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d2c62-121">*PHandle* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="d2c62-121">The *pHandle* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="d2c62-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d2c62-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="d2c62-123">在 *pHandle* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="d2c62-123">A bad pointer was passed in *pHandle*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2c62-124">備註</span><span class="sxs-lookup"><span data-stu-id="d2c62-124">Remarks</span></span>

<span data-ttu-id="d2c62-125">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d2c62-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d2c62-126">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="d2c62-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d2c62-127">範例</span><span class="sxs-lookup"><span data-stu-id="d2c62-127">Examples</span></span>

<span data-ttu-id="d2c62-128">下列範例顯示如何取出智慧卡控制碼。</span><span class="sxs-lookup"><span data-stu-id="d2c62-128">The following example shows retrieving the smart card handle.</span></span>


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
```



## <a name="requirements"></a><span data-ttu-id="d2c62-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2c62-129">Requirements</span></span>



| <span data-ttu-id="d2c62-130">需求</span><span class="sxs-lookup"><span data-stu-id="d2c62-130">Requirement</span></span> | <span data-ttu-id="d2c62-131">值</span><span class="sxs-lookup"><span data-stu-id="d2c62-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c62-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2c62-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d2c62-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2c62-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d2c62-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2c62-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d2c62-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2c62-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2c62-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d2c62-136">End of client support</span></span><br/>    | <span data-ttu-id="d2c62-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2c62-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d2c62-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d2c62-138">End of server support</span></span><br/>    | <span data-ttu-id="d2c62-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2c62-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d2c62-140">標頭</span><span class="sxs-lookup"><span data-stu-id="d2c62-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2c62-141"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c62-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2c62-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d2c62-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="d2c62-143"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d2c62-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d2c62-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d2c62-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2c62-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2c62-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d2c62-146">IID</span><span class="sxs-lookup"><span data-stu-id="d2c62-146">IID</span></span><br/>                      | <span data-ttu-id="d2c62-147">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d2c62-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d2c62-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2c62-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2c62-149">**取得 \_ Atr**</span><span class="sxs-lookup"><span data-stu-id="d2c62-149">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="d2c62-150">**取得 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="d2c62-150">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="d2c62-151">**取得 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="d2c62-151">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="d2c62-152">**取得 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="d2c62-152">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="d2c62-153">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="d2c62-153">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
