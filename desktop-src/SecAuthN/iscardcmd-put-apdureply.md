---
description: 設定新的回復 APDU。
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: 'ISCardCmd：:p ut_ApduReply 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0292f3ebd4e5f18638ad496cdf15cd9f5c4320f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848049"
---
# <a name="iscardcmdput_apdureply-method"></a><span data-ttu-id="2568b-103">ISCardCmd：:p 的 \_ ApduReply 方法</span><span class="sxs-lookup"><span data-stu-id="2568b-103">ISCardCmd::put\_ApduReply method</span></span>

<span data-ttu-id="2568b-104">\[**Put \_ ApduReply** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2568b-104">\[The **put\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2568b-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="2568b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2568b-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="2568b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2568b-107">**Put \_ ApduReply** 方法會設定新的 [*回復 APDU*](../secgloss/r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="2568b-107">The **put\_ApduReply** method sets a new [*reply APDU*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2568b-108">語法</span><span class="sxs-lookup"><span data-stu-id="2568b-108">Syntax</span></span>


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="2568b-109">參數</span><span class="sxs-lookup"><span data-stu-id="2568b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2568b-110">*pReplyApdu* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2568b-110">*pReplyApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2568b-111">位元組緩衝區的指標 (透過包含傳回之重新執行 APDU 訊息的 **IStream** 物件) 對應。</span><span class="sxs-lookup"><span data-stu-id="2568b-111">Pointer to the byte buffer (mapped through an **IStream** object) that contains the replay APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2568b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2568b-112">Return value</span></span>

<span data-ttu-id="2568b-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="2568b-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2568b-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2568b-114">Return code</span></span>                                                                                   | <span data-ttu-id="2568b-115">Description</span><span class="sxs-lookup"><span data-stu-id="2568b-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="2568b-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2568b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2568b-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="2568b-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="2568b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2568b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2568b-119">*PReplyApdu* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="2568b-119">The *pReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="2568b-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="2568b-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2568b-121">在 *pReplyApdu* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="2568b-121">A bad pointer was passed in *pReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="2568b-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2568b-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2568b-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="2568b-123">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="2568b-124">備註</span><span class="sxs-lookup"><span data-stu-id="2568b-124">Remarks</span></span>

<span data-ttu-id="2568b-125">若要取得現有的回復 APDU，請呼叫 [**get \_ ApduReply**](iscardcmd-get-apdureply.md)。</span><span class="sxs-lookup"><span data-stu-id="2568b-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="2568b-126">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="2568b-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="2568b-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2568b-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2568b-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="2568b-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2568b-129">範例</span><span class="sxs-lookup"><span data-stu-id="2568b-129">Examples</span></span>

<span data-ttu-id="2568b-130">下列範例顯示如何設定新的 [*回復 APDU*](../secgloss/r-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="2568b-130">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="2568b-131">此範例假設 pIByteReply 是 [**IByteBuffer**](ibytebuffer.md)實例的有效指標，而且 PISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="2568b-131">The example assumes that pIByteReply is a valid pointer to an instance of [**IByteBuffer**](ibytebuffer.md), and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="2568b-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="2568b-132">Requirements</span></span>



| <span data-ttu-id="2568b-133">需求</span><span class="sxs-lookup"><span data-stu-id="2568b-133">Requirement</span></span> | <span data-ttu-id="2568b-134">值</span><span class="sxs-lookup"><span data-stu-id="2568b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2568b-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2568b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2568b-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2568b-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2568b-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2568b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2568b-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2568b-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2568b-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2568b-139">End of client support</span></span><br/>    | <span data-ttu-id="2568b-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2568b-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2568b-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2568b-141">End of server support</span></span><br/>    | <span data-ttu-id="2568b-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2568b-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2568b-143">標頭</span><span class="sxs-lookup"><span data-stu-id="2568b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2568b-144"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="2568b-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="2568b-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2568b-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="2568b-146"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2568b-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2568b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2568b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2568b-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2568b-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2568b-149">IID</span><span class="sxs-lookup"><span data-stu-id="2568b-149">IID</span></span><br/>                      | <span data-ttu-id="2568b-150">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2568b-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="2568b-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2568b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2568b-152">**取得 \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="2568b-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="2568b-153">**取得 \_ ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="2568b-153">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="2568b-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="2568b-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
