---
description: 重新附加方法會重設或重新初始化智慧卡。
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: 'ISCard：：重新附加方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.ReAttach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f5ff4cd46b2b523b0031e1389b96d9c2c3973a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191855"
---
# <a name="iscardreattach-method"></a><span data-ttu-id="6c24a-103">ISCard：：重新附加方法</span><span class="sxs-lookup"><span data-stu-id="6c24a-103">ISCard::ReAttach method</span></span>

<span data-ttu-id="6c24a-104">\[[重新 **附加** ] 方法可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6c24a-104">\[The **ReAttach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6c24a-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6c24a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6c24a-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6c24a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6c24a-107">重新 **附加** 方法會重設或重新初始化 [*智慧卡*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6c24a-107">The **ReAttach** method resets, or reinitializes, the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c24a-108">語法</span><span class="sxs-lookup"><span data-stu-id="6c24a-108">Syntax</span></span>


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a><span data-ttu-id="6c24a-109">參數</span><span class="sxs-lookup"><span data-stu-id="6c24a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c24a-110">*ShareMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c24a-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c24a-111">要在其中共用或獨佔擁有智慧卡連接的模式。</span><span class="sxs-lookup"><span data-stu-id="6c24a-111">Mode in which to share or exclusively own the connection to the smart card.</span></span>



| <span data-ttu-id="6c24a-112">值</span><span class="sxs-lookup"><span data-stu-id="6c24a-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="6c24a-113">意義</span><span class="sxs-lookup"><span data-stu-id="6c24a-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="6c24a-114"><dt>**獨家**</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="6c24a-115">沒有其他人使用此智慧卡連線。</span><span class="sxs-lookup"><span data-stu-id="6c24a-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="6c24a-116"><dt>**共用**</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="6c24a-117">其他應用程式可以使用此連接。</span><span class="sxs-lookup"><span data-stu-id="6c24a-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="6c24a-118">*InitState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c24a-118">*InitState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c24a-119">指出如何處理卡片。</span><span class="sxs-lookup"><span data-stu-id="6c24a-119">Indicates what to do with the card.</span></span>



| <span data-ttu-id="6c24a-120">值</span><span class="sxs-lookup"><span data-stu-id="6c24a-120">Value</span></span>                                                                                                                                      | <span data-ttu-id="6c24a-121">意義</span><span class="sxs-lookup"><span data-stu-id="6c24a-121">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="6c24a-122"><dt>**離開**</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-122"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="6c24a-123">將智慧卡保留為目前的 [*狀態*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6c24a-123">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="6c24a-124"><dt>**重 置**</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-124"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="6c24a-125">將智慧卡重設為某個已知狀態。</span><span class="sxs-lookup"><span data-stu-id="6c24a-125">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="6c24a-126"><dt>**UNPOWER**</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-126"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="6c24a-127">移除智慧卡的電源。</span><span class="sxs-lookup"><span data-stu-id="6c24a-127">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="6c24a-128"><dt>**彈出**</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-128"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="6c24a-129">如果讀取器有退出功能，請將智慧卡彈出。</span><span class="sxs-lookup"><span data-stu-id="6c24a-129">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c24a-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c24a-130">Return value</span></span>

<span data-ttu-id="6c24a-131">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="6c24a-131">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6c24a-132">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6c24a-132">Return code</span></span>                                                                                  | <span data-ttu-id="6c24a-133">Description</span><span class="sxs-lookup"><span data-stu-id="6c24a-133">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c24a-134"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-134"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6c24a-135">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="6c24a-135">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="6c24a-136"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-136"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6c24a-137">傳遞至函式的一或多個參數發生問題。</span><span class="sxs-lookup"><span data-stu-id="6c24a-137">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c24a-138">備註</span><span class="sxs-lookup"><span data-stu-id="6c24a-138">Remarks</span></span>

<span data-ttu-id="6c24a-139">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6c24a-139">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6c24a-140">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6c24a-140">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6c24a-141">範例</span><span class="sxs-lookup"><span data-stu-id="6c24a-141">Examples</span></span>

<span data-ttu-id="6c24a-142">下列範例顯示重新初始化智慧卡。</span><span class="sxs-lookup"><span data-stu-id="6c24a-142">The following example shows reinitializing the smart card.</span></span>


```C++
HRESULT    hr;

// Reattach the smart card.
hr = pISCard->ReAttach(SHARED, LEAVE);
if (FAILED(hr))
{
   printf("Failed ReAttach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="6c24a-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c24a-143">Requirements</span></span>



| <span data-ttu-id="6c24a-144">需求</span><span class="sxs-lookup"><span data-stu-id="6c24a-144">Requirement</span></span> | <span data-ttu-id="6c24a-145">值</span><span class="sxs-lookup"><span data-stu-id="6c24a-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c24a-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c24a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6c24a-147">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c24a-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6c24a-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c24a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6c24a-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c24a-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6c24a-150">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6c24a-150">End of client support</span></span><br/>    | <span data-ttu-id="6c24a-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c24a-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6c24a-152">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6c24a-152">End of server support</span></span><br/>    | <span data-ttu-id="6c24a-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c24a-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6c24a-154">標頭</span><span class="sxs-lookup"><span data-stu-id="6c24a-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c24a-155"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-155"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c24a-156">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6c24a-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="6c24a-157"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-157"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6c24a-158">DLL</span><span class="sxs-lookup"><span data-stu-id="6c24a-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c24a-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c24a-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6c24a-160">IID</span><span class="sxs-lookup"><span data-stu-id="6c24a-160">IID</span></span><br/>                      | <span data-ttu-id="6c24a-161">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6c24a-161">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6c24a-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c24a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c24a-163">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="6c24a-163">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="6c24a-164">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="6c24a-164">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="6c24a-165">**中斷連結**</span><span class="sxs-lookup"><span data-stu-id="6c24a-165">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="6c24a-166">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="6c24a-166">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
