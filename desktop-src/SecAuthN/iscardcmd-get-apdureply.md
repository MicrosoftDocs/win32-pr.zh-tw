---
description: 抓取回復 APDU，將它放在特定的位元組緩衝區中。
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'ISCardCmd：： get_ApduReply 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027532"
---
# <a name="iscardcmdget_apdureply-method"></a><span data-ttu-id="46365-103">ISCardCmd：： get \_ ApduReply 方法</span><span class="sxs-lookup"><span data-stu-id="46365-103">ISCardCmd::get\_ApduReply method</span></span>

<span data-ttu-id="46365-104">\[**Get \_ ApduReply** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="46365-104">\[The **get\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="46365-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="46365-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="46365-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="46365-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="46365-107">**Get \_ ApduReply** 方法會抓取 [*回復 APDU*](../secgloss/r-gly.md)，並將其放在特定的位元組緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="46365-107">The **get\_ApduReply** method retrieves the [*reply APDU*](../secgloss/r-gly.md), placing it in a specific byte buffer.</span></span> <span data-ttu-id="46365-108">如果未在命令 APDU 上執行任何 [*交易*](../secgloss/t-gly.md)，回復可能會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="46365-108">The reply may be **NULL** if no [*transaction*](../secgloss/t-gly.md) has been performed on the command APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="46365-109">語法</span><span class="sxs-lookup"><span data-stu-id="46365-109">Syntax</span></span>


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="46365-110">參數</span><span class="sxs-lookup"><span data-stu-id="46365-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46365-111">*ppReplyApdu* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46365-111">*ppReplyApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46365-112">位元組緩衝區的指標 (透過包含傳回之 APDU 回復訊息的 **IStream** 物件) 對應。</span><span class="sxs-lookup"><span data-stu-id="46365-112">Pointer to the byte buffer (mapped through an **IStream** object) that contains the APDU reply message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46365-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="46365-113">Return value</span></span>

<span data-ttu-id="46365-114">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="46365-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="46365-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="46365-115">Return code</span></span>                                                                                   | <span data-ttu-id="46365-116">Description</span><span class="sxs-lookup"><span data-stu-id="46365-116">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="46365-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="46365-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="46365-118">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="46365-118">Operation completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="46365-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="46365-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="46365-120">*PpReplyApdu* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="46365-120">The *ppReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="46365-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="46365-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="46365-122">在 *ppReplyApdu* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="46365-122">A bad pointer was passed in *ppReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="46365-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="46365-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="46365-124">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="46365-124">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="46365-125">備註</span><span class="sxs-lookup"><span data-stu-id="46365-125">Remarks</span></span>

<span data-ttu-id="46365-126">若要判斷 APDU 回復的長度，請呼叫 [**get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md)。</span><span class="sxs-lookup"><span data-stu-id="46365-126">To determine the length of the APDU reply, call [**get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span></span>

<span data-ttu-id="46365-127">若要設定新的回復 APDU，請呼叫 [**put \_ ApduReply**](iscardcmd-put-apdureply.md)。</span><span class="sxs-lookup"><span data-stu-id="46365-127">To set a new reply APDU, call [**put\_ApduReply**](iscardcmd-put-apdureply.md).</span></span>

<span data-ttu-id="46365-128">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="46365-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="46365-129">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="46365-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="46365-130">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="46365-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="46365-131">範例</span><span class="sxs-lookup"><span data-stu-id="46365-131">Examples</span></span>

<span data-ttu-id="46365-132">下列範例示範如何取出回復資料。</span><span class="sxs-lookup"><span data-stu-id="46365-132">The following example shows how to retrieve reply data.</span></span> <span data-ttu-id="46365-133">此範例假設 lLe 是 **LONG** 類型的變數，其值是由先前的 [**ISCardCmd：： get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md) 方法呼叫所設定，該 pIByteReply 是 [**IByteBuffer**](ibytebuffer.md) 介面實例的有效指標，而且 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="46365-133">The example assumes that lLe is a variable of type **LONG** whose value was set by a previous call to the [**ISCardCmd::get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md) method, that pIByteReply is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="46365-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="46365-134">Requirements</span></span>



| <span data-ttu-id="46365-135">需求</span><span class="sxs-lookup"><span data-stu-id="46365-135">Requirement</span></span> | <span data-ttu-id="46365-136">值</span><span class="sxs-lookup"><span data-stu-id="46365-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46365-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46365-137">Minimum supported client</span></span><br/> | <span data-ttu-id="46365-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46365-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="46365-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46365-139">Minimum supported server</span></span><br/> | <span data-ttu-id="46365-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46365-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46365-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="46365-141">End of client support</span></span><br/>    | <span data-ttu-id="46365-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="46365-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="46365-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="46365-143">End of server support</span></span><br/>    | <span data-ttu-id="46365-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46365-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="46365-145">標頭</span><span class="sxs-lookup"><span data-stu-id="46365-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="46365-146"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="46365-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="46365-147">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="46365-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="46365-148"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46365-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46365-149">DLL</span><span class="sxs-lookup"><span data-stu-id="46365-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46365-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46365-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="46365-151">IID</span><span class="sxs-lookup"><span data-stu-id="46365-151">IID</span></span><br/>                      | <span data-ttu-id="46365-152">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="46365-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="46365-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46365-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46365-154">**取得 \_ ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="46365-154">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="46365-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="46365-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="46365-156">**put \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="46365-156">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
