---
description: " (應用程式協定資料單位) 物件，執行智慧卡命令的寫入和讀取作業。"
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'ISCard：： Transaction 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993034"
---
# <a name="iscardtransaction-method"></a><span data-ttu-id="c1544-103">ISCard：： Transaction 方法</span><span class="sxs-lookup"><span data-stu-id="c1544-103">ISCard::Transaction method</span></span>

<span data-ttu-id="c1544-104">\[**交易** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c1544-104">\[The **Transaction** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c1544-105">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c1544-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c1544-106">**交易** 方法會在 [*智慧卡*](../secgloss/s-gly.md)命令 ([*應用程式協定資料單位*](../secgloss/a-gly.md)) 物件上執行寫入和讀取作業。</span><span class="sxs-lookup"><span data-stu-id="c1544-106">The **Transaction** method executes a write and read operation on the [*smart card*](../secgloss/s-gly.md) command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span> <span data-ttu-id="c1544-107">在此函式傳回之後，將可存取智慧卡中為傳送至智慧卡之卡片中所定義之命令字串的回復字串。</span><span class="sxs-lookup"><span data-stu-id="c1544-107">The reply string from the smart card for the command string defined in the card that was sent to the smart card will be accessible after this function returns.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1544-108">語法</span><span class="sxs-lookup"><span data-stu-id="c1544-108">Syntax</span></span>


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="c1544-109">參數</span><span class="sxs-lookup"><span data-stu-id="c1544-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1544-110">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c1544-110">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1544-111">智慧卡命令物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c1544-111">A pointer to the smart card command object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1544-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1544-112">Return value</span></span>

<span data-ttu-id="c1544-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="c1544-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c1544-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c1544-114">Return code</span></span>                                                                                   | <span data-ttu-id="c1544-115">Description</span><span class="sxs-lookup"><span data-stu-id="c1544-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="c1544-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c1544-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c1544-117">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="c1544-117">The operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="c1544-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c1544-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c1544-119">*PpCmd* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="c1544-119">The *ppCmd* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="c1544-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c1544-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c1544-121">在 *ppCmd* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="c1544-121">A bad pointer was passed in *ppCmd*.</span></span><br/>          |
| <dl> <span data-ttu-id="c1544-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c1544-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c1544-123">無法取得滿足要求的記憶體。</span><span class="sxs-lookup"><span data-stu-id="c1544-123">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c1544-124">備註</span><span class="sxs-lookup"><span data-stu-id="c1544-124">Remarks</span></span>

<span data-ttu-id="c1544-125">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1544-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c1544-126">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="c1544-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c1544-127">範例</span><span class="sxs-lookup"><span data-stu-id="c1544-127">Examples</span></span>

<span data-ttu-id="c1544-128">下列範例顯示在智慧卡命令物件上執行寫入和讀取作業。</span><span class="sxs-lookup"><span data-stu-id="c1544-128">The following example shows executing a write and read operation on the smart card command object.</span></span>


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="c1544-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1544-129">Requirements</span></span>



| <span data-ttu-id="c1544-130">需求</span><span class="sxs-lookup"><span data-stu-id="c1544-130">Requirement</span></span> | <span data-ttu-id="c1544-131">值</span><span class="sxs-lookup"><span data-stu-id="c1544-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1544-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1544-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c1544-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1544-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c1544-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1544-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c1544-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1544-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1544-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c1544-136">End of client support</span></span><br/>    | <span data-ttu-id="c1544-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c1544-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c1544-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c1544-138">End of server support</span></span><br/>    | <span data-ttu-id="c1544-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1544-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c1544-140">標頭</span><span class="sxs-lookup"><span data-stu-id="c1544-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1544-141"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1544-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1544-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c1544-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1544-143"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1544-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1544-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c1544-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1544-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1544-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1544-146">IID</span><span class="sxs-lookup"><span data-stu-id="c1544-146">IID</span></span><br/>                      | <span data-ttu-id="c1544-147">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="c1544-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c1544-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1544-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1544-149">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="c1544-149">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="c1544-150">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="c1544-150">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="c1544-151">**中斷連結**</span><span class="sxs-lookup"><span data-stu-id="c1544-151">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="c1544-152">**取得 \_ Atr**</span><span class="sxs-lookup"><span data-stu-id="c1544-152">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="c1544-153">**取得 \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="c1544-153">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="c1544-154">**取得 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="c1544-154">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="c1544-155">**取得 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="c1544-155">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="c1544-156">**取得 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="c1544-156">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="c1544-157">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="c1544-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="c1544-158">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="c1544-158">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> <dt>

[<span data-ttu-id="c1544-159">**附加**</span><span class="sxs-lookup"><span data-stu-id="c1544-159">**ReAttach**</span></span>](iscard-reattach.md)
</dt> <dt>

[<span data-ttu-id="c1544-160">**UnlockSCard**</span><span class="sxs-lookup"><span data-stu-id="c1544-160">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
