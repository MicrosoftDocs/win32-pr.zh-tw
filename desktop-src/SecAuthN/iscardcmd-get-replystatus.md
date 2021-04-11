---
description: 抓取回復 APDU 的訊息狀態字組。
ms.assetid: c8a4b713-4ae9-49f2-a623-6ee305123638
title: 'ISCardCmd：： get_ReplyStatus 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 021c5395dbca6275161a53cb7e8a0c2247ab9410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113217"
---
# <a name="iscardcmdget_replystatus-method"></a><span data-ttu-id="da754-103">ISCardCmd：： get \_ ReplyStatus 方法</span><span class="sxs-lookup"><span data-stu-id="da754-103">ISCardCmd::get\_ReplyStatus method</span></span>

<span data-ttu-id="da754-104">\[**Get \_ ReplyStatus** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="da754-104">\[The **get\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="da754-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="da754-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="da754-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="da754-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="da754-107">**Get \_ ReplyStatus** 方法會抓取 [*回復 APDU 的*](../secgloss/r-gly.md)訊息狀態字組。</span><span class="sxs-lookup"><span data-stu-id="da754-107">The **get\_ReplyStatus** method retrieves the [*reply APDU's*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="da754-108">語法</span><span class="sxs-lookup"><span data-stu-id="da754-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatus(
  [out] LPWORD pwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="da754-109">參數</span><span class="sxs-lookup"><span data-stu-id="da754-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da754-110">*pwStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="da754-110">*pwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da754-111">傳回時狀態的文字指標。</span><span class="sxs-lookup"><span data-stu-id="da754-111">Pointer to the word that is the status on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da754-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="da754-112">Return value</span></span>

<span data-ttu-id="da754-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="da754-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="da754-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="da754-114">Return code</span></span>                                                                                   | <span data-ttu-id="da754-115">Description</span><span class="sxs-lookup"><span data-stu-id="da754-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="da754-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="da754-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="da754-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="da754-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="da754-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="da754-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="da754-119">*PwStatus* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="da754-119">The *pwStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="da754-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="da754-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="da754-121">在 *pwStatus* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="da754-121">A bad pointer was passed in *pwStatus*.</span></span><br/> |
| <dl> <span data-ttu-id="da754-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="da754-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="da754-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="da754-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="da754-124">備註</span><span class="sxs-lookup"><span data-stu-id="da754-124">Remarks</span></span>

<span data-ttu-id="da754-125">若要設定回復 APDU 的訊息狀態文字，請呼叫 [**put \_ ReplyStatus**](iscardcmd-put-replystatus.md)。</span><span class="sxs-lookup"><span data-stu-id="da754-125">To set the reply APDU's message status word, call [**put\_ReplyStatus**](iscardcmd-put-replystatus.md).</span></span>

<span data-ttu-id="da754-126">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="da754-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="da754-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="da754-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="da754-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="da754-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="da754-129">範例</span><span class="sxs-lookup"><span data-stu-id="da754-129">Examples</span></span>

<span data-ttu-id="da754-130">下列範例示範如何取出 [*回復 APDU*](../secgloss/r-gly.md)的訊息狀態字組。</span><span class="sxs-lookup"><span data-stu-id="da754-130">The following example shows how to retrieve the message status word of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="da754-131">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="da754-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD    wReplyStatus;
HRESULT hr;

// Get reply status.
hr = pISCardCmd->get_ReplyStatus(&wReplyStatus);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatus\n");
  // Take other error handling action as needed.
}
else
{
  if (wReplyStatus != 0x9000)
  {
    printf("APDU failed - Error [0x%x]\n", wReplyStatus);
    // Take other error handling action as needed.
  }
}
```



## <a name="requirements"></a><span data-ttu-id="da754-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="da754-132">Requirements</span></span>



| <span data-ttu-id="da754-133">需求</span><span class="sxs-lookup"><span data-stu-id="da754-133">Requirement</span></span> | <span data-ttu-id="da754-134">值</span><span class="sxs-lookup"><span data-stu-id="da754-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da754-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da754-135">Minimum supported client</span></span><br/> | <span data-ttu-id="da754-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da754-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="da754-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da754-137">Minimum supported server</span></span><br/> | <span data-ttu-id="da754-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da754-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="da754-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="da754-139">End of client support</span></span><br/>    | <span data-ttu-id="da754-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="da754-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="da754-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="da754-141">End of server support</span></span><br/>    | <span data-ttu-id="da754-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="da754-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="da754-143">標頭</span><span class="sxs-lookup"><span data-stu-id="da754-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="da754-144"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="da754-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="da754-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="da754-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="da754-146"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="da754-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="da754-147">DLL</span><span class="sxs-lookup"><span data-stu-id="da754-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da754-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da754-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="da754-149">IID</span><span class="sxs-lookup"><span data-stu-id="da754-149">IID</span></span><br/>                      | <span data-ttu-id="da754-150">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="da754-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="da754-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da754-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da754-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="da754-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="da754-153">**put \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="da754-153">**put\_ReplyStatus**</span></span>](iscardcmd-put-replystatus.md)
</dt> </dl>

 

 
