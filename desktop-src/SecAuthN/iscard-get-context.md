---
description: 抓取目前的 resource manager 內容控制碼。 \*如果未建立任何內容，這個方法會傳回 (pCoNtext) = = Null。
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'ISCard：： get_CoNtext 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851735"
---
# <a name="iscardget_context-method"></a><span data-ttu-id="359b4-104">ISCard：： get \_ CoNtext 方法</span><span class="sxs-lookup"><span data-stu-id="359b4-104">ISCard::get\_Context method</span></span>

<span data-ttu-id="359b4-105">\[**取得 \_ 內容** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="359b4-105">\[The **get\_Context** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="359b4-106">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="359b4-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="359b4-107">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="359b4-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="359b4-108">**Get \_ CoNtext** 方法會抓取目前的 [*resource manager 內容*](../secgloss/r-gly.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="359b4-108">The **get\_Context** method retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span> <span data-ttu-id="359b4-109">\*如果未建立任何內容，這個方法會傳回 (*pCoNtext*) = = **Null** 。</span><span class="sxs-lookup"><span data-stu-id="359b4-109">This method returns (\**pContext*) == **NULL** if no context has been established.</span></span>

## <a name="syntax"></a><span data-ttu-id="359b4-110">語法</span><span class="sxs-lookup"><span data-stu-id="359b4-110">Syntax</span></span>


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="359b4-111">參數</span><span class="sxs-lookup"><span data-stu-id="359b4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="359b4-112">*pCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="359b4-112">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="359b4-113">傳回時的內容控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="359b4-113">Pointer to the context handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="359b4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="359b4-114">Return value</span></span>

<span data-ttu-id="359b4-115">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="359b4-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="359b4-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="359b4-116">Return code</span></span>                                                                                  | <span data-ttu-id="359b4-117">Description</span><span class="sxs-lookup"><span data-stu-id="359b4-117">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="359b4-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="359b4-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="359b4-119">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="359b4-119">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="359b4-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="359b4-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="359b4-121">*PCoNtext* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="359b4-121">The *pContext* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="359b4-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="359b4-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="359b4-123">在 *pCoNtext* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="359b4-123">A bad pointer was passed in *pContext*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="359b4-124">備註</span><span class="sxs-lookup"><span data-stu-id="359b4-124">Remarks</span></span>

<span data-ttu-id="359b4-125">資源管理員內容是藉由呼叫 [*智慧卡*](../secgloss/s-gly.md) 函式 [**SCardEstablishCoNtext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)來設定。</span><span class="sxs-lookup"><span data-stu-id="359b4-125">The resource manager context is set by calling the [*smart card*](../secgloss/s-gly.md) function [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span></span>

<span data-ttu-id="359b4-126">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="359b4-126">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="359b4-127">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="359b4-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="359b4-128">範例</span><span class="sxs-lookup"><span data-stu-id="359b4-128">Examples</span></span>

<span data-ttu-id="359b4-129">下列範例顯示如何取出目前的 [*resource manager 內容*](../secgloss/r-gly.md) 控制碼。</span><span class="sxs-lookup"><span data-stu-id="359b4-129">The following example shows retrieving the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span>


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
```



## <a name="requirements"></a><span data-ttu-id="359b4-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="359b4-130">Requirements</span></span>



| <span data-ttu-id="359b4-131">需求</span><span class="sxs-lookup"><span data-stu-id="359b4-131">Requirement</span></span> | <span data-ttu-id="359b4-132">值</span><span class="sxs-lookup"><span data-stu-id="359b4-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="359b4-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="359b4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="359b4-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="359b4-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="359b4-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="359b4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="359b4-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="359b4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="359b4-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="359b4-137">End of client support</span></span><br/>    | <span data-ttu-id="359b4-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="359b4-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="359b4-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="359b4-139">End of server support</span></span><br/>    | <span data-ttu-id="359b4-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="359b4-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="359b4-141">標頭</span><span class="sxs-lookup"><span data-stu-id="359b4-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="359b4-142"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="359b4-142"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="359b4-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="359b4-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="359b4-144"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="359b4-144"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="359b4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="359b4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="359b4-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="359b4-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="359b4-147">IID</span><span class="sxs-lookup"><span data-stu-id="359b4-147">IID</span></span><br/>                      | <span data-ttu-id="359b4-148">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="359b4-148">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="359b4-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="359b4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="359b4-150">**取得 \_ Atr**</span><span class="sxs-lookup"><span data-stu-id="359b4-150">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="359b4-151">**取得 \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="359b4-151">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="359b4-152">**取得 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="359b4-152">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="359b4-153">**取得 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="359b4-153">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="359b4-154">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="359b4-154">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="359b4-155">**SCardEstablishCoNtext**</span><span class="sxs-lookup"><span data-stu-id="359b4-155">**SCardEstablishContext**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
