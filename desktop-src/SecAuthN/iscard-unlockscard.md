---
description: 釋放智慧卡的獨佔存取權。
ms.assetid: 12256c91-faf2-4a06-9501-f00d0115a069
title: 'ISCard：： UnlockSCard 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.UnlockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 68907e157e60518d1df3855fbca69709f2c21437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691771"
---
# <a name="iscardunlockscard-method"></a><span data-ttu-id="d0856-103">ISCard：： UnlockSCard 方法</span><span class="sxs-lookup"><span data-stu-id="d0856-103">ISCard::UnlockSCard method</span></span>

<span data-ttu-id="d0856-104">\[**UnlockScard** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d0856-104">\[The **UnlockScard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d0856-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="d0856-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d0856-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d0856-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d0856-107">**UnlockScard** 方法會釋放 [*智慧卡*](../secgloss/s-gly.md)的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="d0856-107">The **UnlockScard** method releases exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0856-108">語法</span><span class="sxs-lookup"><span data-stu-id="d0856-108">Syntax</span></span>


```C++
HRESULT UnlockSCard(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="d0856-109">參數</span><span class="sxs-lookup"><span data-stu-id="d0856-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0856-110">*處置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0856-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0856-111">指出在連接的 [*讀取器*](../secgloss/r-gly.md)中應如何使用卡片進行哪些操作。</span><span class="sxs-lookup"><span data-stu-id="d0856-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="d0856-112">值</span><span class="sxs-lookup"><span data-stu-id="d0856-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="d0856-113">意義</span><span class="sxs-lookup"><span data-stu-id="d0856-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="d0856-114"><dt>**離開**</dt></span><span class="sxs-lookup"><span data-stu-id="d0856-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="d0856-115">將智慧卡保留為目前的 [*狀態*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="d0856-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="d0856-116"><dt>**重 置**</dt></span><span class="sxs-lookup"><span data-stu-id="d0856-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="d0856-117">將智慧卡重設為某個已知狀態。</span><span class="sxs-lookup"><span data-stu-id="d0856-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="d0856-118"><dt>**UNPOWER**</dt></span><span class="sxs-lookup"><span data-stu-id="d0856-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="d0856-119">移除智慧卡的電源。</span><span class="sxs-lookup"><span data-stu-id="d0856-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="d0856-120"><dt>**彈出**</dt></span><span class="sxs-lookup"><span data-stu-id="d0856-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="d0856-121">如果讀取器有退出功能，請將智慧卡彈出。</span><span class="sxs-lookup"><span data-stu-id="d0856-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0856-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0856-122">Return value</span></span>

<span data-ttu-id="d0856-123">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="d0856-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d0856-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d0856-124">Return code</span></span>                                                                                  | <span data-ttu-id="d0856-125">Description</span><span class="sxs-lookup"><span data-stu-id="d0856-125">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="d0856-126"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d0856-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d0856-127">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="d0856-127">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="d0856-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d0856-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d0856-129">*處置* 參數無效</span><span class="sxs-lookup"><span data-stu-id="d0856-129">The *Disposition* parameter is not valid</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0856-130">備註</span><span class="sxs-lookup"><span data-stu-id="d0856-130">Remarks</span></span>

<span data-ttu-id="d0856-131">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d0856-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d0856-132">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="d0856-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d0856-133">範例</span><span class="sxs-lookup"><span data-stu-id="d0856-133">Examples</span></span>

<span data-ttu-id="d0856-134">下列範例顯示釋出智慧卡的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="d0856-134">The following example shows releasing exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Unlock the smart card.
hr = pISCard->UnlockSCard(LEAVE);
if (FAILED(hr))
{
   printf("Failed UnlockSCard\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="d0856-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0856-135">Requirements</span></span>



| <span data-ttu-id="d0856-136">需求</span><span class="sxs-lookup"><span data-stu-id="d0856-136">Requirement</span></span> | <span data-ttu-id="d0856-137">值</span><span class="sxs-lookup"><span data-stu-id="d0856-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0856-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0856-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d0856-139">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0856-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d0856-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0856-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d0856-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0856-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0856-142">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d0856-142">End of client support</span></span><br/>    | <span data-ttu-id="d0856-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0856-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d0856-144">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d0856-144">End of server support</span></span><br/>    | <span data-ttu-id="d0856-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0856-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d0856-146">標頭</span><span class="sxs-lookup"><span data-stu-id="d0856-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0856-147"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0856-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0856-148">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d0856-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0856-149"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d0856-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d0856-150">DLL</span><span class="sxs-lookup"><span data-stu-id="d0856-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0856-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0856-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0856-152">IID</span><span class="sxs-lookup"><span data-stu-id="d0856-152">IID</span></span><br/>                      | <span data-ttu-id="d0856-153">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d0856-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d0856-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0856-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0856-155">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="d0856-155">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="d0856-156">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="d0856-156">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> </dl>

 

 
