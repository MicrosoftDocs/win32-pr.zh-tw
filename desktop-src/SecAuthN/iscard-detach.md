---
description: 關閉智慧卡的開啟連接。
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: 'ISCard：:D etach 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f9fd2b2a6d9ea2df8e886c6ff9851706c2030a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001423"
---
# <a name="iscarddetach-method"></a><span data-ttu-id="e7c84-103">ISCard：:D etach 方法</span><span class="sxs-lookup"><span data-stu-id="e7c84-103">ISCard::Detach method</span></span>

<span data-ttu-id="e7c84-104">\[卸 **離** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e7c84-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e7c84-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="e7c84-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e7c84-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e7c84-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e7c84-107">卸 **離** 方法會關閉 [*智慧卡*](../secgloss/s-gly.md)的開啟連接。</span><span class="sxs-lookup"><span data-stu-id="e7c84-107">The **Detach** method closes the open connection to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7c84-108">語法</span><span class="sxs-lookup"><span data-stu-id="e7c84-108">Syntax</span></span>


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="e7c84-109">參數</span><span class="sxs-lookup"><span data-stu-id="e7c84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7c84-110">*處置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7c84-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7c84-111">指出在連接的 [*讀取器*](../secgloss/r-gly.md)中應如何使用卡片進行哪些操作。</span><span class="sxs-lookup"><span data-stu-id="e7c84-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="e7c84-112">值</span><span class="sxs-lookup"><span data-stu-id="e7c84-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="e7c84-113">意義</span><span class="sxs-lookup"><span data-stu-id="e7c84-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="e7c84-114"><dt>**離開**</dt></span><span class="sxs-lookup"><span data-stu-id="e7c84-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="e7c84-115">將智慧卡保留為目前的 [*狀態*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="e7c84-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="e7c84-116"><dt>**重 置**</dt></span><span class="sxs-lookup"><span data-stu-id="e7c84-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="e7c84-117">將智慧卡重設為某個已知狀態。</span><span class="sxs-lookup"><span data-stu-id="e7c84-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="e7c84-118"><dt>**UNPOWER**</dt></span><span class="sxs-lookup"><span data-stu-id="e7c84-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="e7c84-119">移除智慧卡的電源。</span><span class="sxs-lookup"><span data-stu-id="e7c84-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="e7c84-120"><dt>**彈出**</dt></span><span class="sxs-lookup"><span data-stu-id="e7c84-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="e7c84-121">如果讀取器有退出功能，請將智慧卡彈出。</span><span class="sxs-lookup"><span data-stu-id="e7c84-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7c84-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7c84-122">Return value</span></span>

<span data-ttu-id="e7c84-123">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="e7c84-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e7c84-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e7c84-124">Return code</span></span>                                                                                  | <span data-ttu-id="e7c84-125">Description</span><span class="sxs-lookup"><span data-stu-id="e7c84-125">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e7c84-126"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e7c84-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e7c84-127">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="e7c84-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e7c84-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e7c84-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e7c84-129">配置 *無效。*</span><span class="sxs-lookup"><span data-stu-id="e7c84-129">*Disposition* is not valid.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="e7c84-130">備註</span><span class="sxs-lookup"><span data-stu-id="e7c84-130">Remarks</span></span>

<span data-ttu-id="e7c84-131">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e7c84-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e7c84-132">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="e7c84-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e7c84-133">範例</span><span class="sxs-lookup"><span data-stu-id="e7c84-133">Examples</span></span>

<span data-ttu-id="e7c84-134">下列範例顯示關閉智慧卡的連接。</span><span class="sxs-lookup"><span data-stu-id="e7c84-134">The following example shows closing the connection to the smart card.</span></span>


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="e7c84-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7c84-135">Requirements</span></span>



| <span data-ttu-id="e7c84-136">需求</span><span class="sxs-lookup"><span data-stu-id="e7c84-136">Requirement</span></span> | <span data-ttu-id="e7c84-137">值</span><span class="sxs-lookup"><span data-stu-id="e7c84-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7c84-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7c84-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e7c84-139">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7c84-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e7c84-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7c84-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e7c84-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7c84-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7c84-142">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e7c84-142">End of client support</span></span><br/>    | <span data-ttu-id="e7c84-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e7c84-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e7c84-144">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e7c84-144">End of server support</span></span><br/>    | <span data-ttu-id="e7c84-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7c84-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e7c84-146">標頭</span><span class="sxs-lookup"><span data-stu-id="e7c84-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7c84-147"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="e7c84-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7c84-148">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e7c84-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7c84-149"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e7c84-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e7c84-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e7c84-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7c84-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7c84-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e7c84-152">IID</span><span class="sxs-lookup"><span data-stu-id="e7c84-152">IID</span></span><br/>                      | <span data-ttu-id="e7c84-153">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e7c84-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e7c84-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7c84-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c84-155">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="e7c84-155">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="e7c84-156">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="e7c84-156">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="e7c84-157">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="e7c84-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="e7c84-158">**附加**</span><span class="sxs-lookup"><span data-stu-id="e7c84-158">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
