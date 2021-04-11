---
description: 抓取回復 APDU SW2 狀態位元組。
ms.assetid: 24ad0164-84fc-4a99-b9dd-0f7d789dff92
title: 'ISCardCmd：： get_ReplyStatusSW2 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7ff503758a50437b4b7ff974fe4455d4b92ce978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113216"
---
# <a name="iscardcmdget_replystatussw2-method"></a><span data-ttu-id="d6a0d-103">ISCardCmd：： get \_ ReplyStatusSW2 方法</span><span class="sxs-lookup"><span data-stu-id="d6a0d-103">ISCardCmd::get\_ReplyStatusSW2 method</span></span>

<span data-ttu-id="d6a0d-104">\[**Get \_ ReplyStatusSW2** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-104">\[The **get\_ReplyStatusSW2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d6a0d-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d6a0d-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d6a0d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d6a0d-107">**Get \_ ReplyStatusSW2** 方法會抓取 [*回復 APDU*](../secgloss/r-gly.md) SW2 狀態位元組。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-107">The **get\_ReplyStatusSW2** method retrieves the [*reply APDU*](../secgloss/r-gly.md) SW2 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a0d-108">語法</span><span class="sxs-lookup"><span data-stu-id="d6a0d-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW2(
  [out] LPBYTE pbySW2
);
```



## <a name="parameters"></a><span data-ttu-id="d6a0d-109">參數</span><span class="sxs-lookup"><span data-stu-id="d6a0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a0d-110">*pbySW2* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d6a0d-110">*pbySW2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a0d-111">傳回時，包含 SW2 位元組值的位元組指標。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-111">Pointer to the byte that contains the value of the SW2 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a0d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6a0d-112">Return value</span></span>

<span data-ttu-id="d6a0d-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d6a0d-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d6a0d-114">Return code</span></span>                                                                                   | <span data-ttu-id="d6a0d-115">Description</span><span class="sxs-lookup"><span data-stu-id="d6a0d-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d6a0d-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a0d-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d6a0d-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="d6a0d-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a0d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d6a0d-119">*PbySW2* 無效。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-119">The *pbySW2* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="d6a0d-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a0d-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d6a0d-121">在 *pbySW2* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-121">A bad pointer was passed in *pbySW2*.</span></span><br/> |
| <dl> <span data-ttu-id="d6a0d-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a0d-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d6a0d-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="d6a0d-124">備註</span><span class="sxs-lookup"><span data-stu-id="d6a0d-124">Remarks</span></span>

<span data-ttu-id="d6a0d-125">回復 APDU 的 SW2 狀態位元組是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-125">The reply APDU's SW2 status byte is read-only.</span></span>

<span data-ttu-id="d6a0d-126">若要取得回復 APDU 的 SW1 狀態位元組，請呼叫 [**get \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-126">To retrieve the reply APDU's SW1 status byte, call [**get\_ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).</span></span>

<span data-ttu-id="d6a0d-127">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="d6a0d-128">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d6a0d-129">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d6a0d-130">範例</span><span class="sxs-lookup"><span data-stu-id="d6a0d-130">Examples</span></span>

<span data-ttu-id="d6a0d-131">下列範例示範如何取出 [*回復 APDU*](../secgloss/r-gly.md)的 SW2 狀態位元組。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-131">The following example shows how to retrieve the SW2 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="d6a0d-132">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="d6a0d-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW2;
HRESULT  hr;

// Retrieve the reply status SW2 byte.
hr = pISCardCmd->get_ReplyStatusSW2(&bySW2);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="d6a0d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6a0d-133">Requirements</span></span>



| <span data-ttu-id="d6a0d-134">需求</span><span class="sxs-lookup"><span data-stu-id="d6a0d-134">Requirement</span></span> | <span data-ttu-id="d6a0d-135">值</span><span class="sxs-lookup"><span data-stu-id="d6a0d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a0d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6a0d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a0d-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6a0d-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d6a0d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6a0d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a0d-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6a0d-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d6a0d-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d6a0d-140">End of client support</span></span><br/>    | <span data-ttu-id="d6a0d-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6a0d-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d6a0d-142">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d6a0d-142">End of server support</span></span><br/>    | <span data-ttu-id="d6a0d-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d6a0d-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d6a0d-144">標頭</span><span class="sxs-lookup"><span data-stu-id="d6a0d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6a0d-145"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="d6a0d-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6a0d-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d6a0d-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6a0d-147"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d6a0d-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d6a0d-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d6a0d-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6a0d-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6a0d-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6a0d-150">IID</span><span class="sxs-lookup"><span data-stu-id="d6a0d-150">IID</span></span><br/>                      | <span data-ttu-id="d6a0d-151">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d6a0d-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d6a0d-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6a0d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a0d-153">**取得 \_ ReplyStatusSW1**</span><span class="sxs-lookup"><span data-stu-id="d6a0d-153">**get\_ReplyStatusSW1**</span></span>](iscardcmd-get-replystatussw1.md)
</dt> <dt>

[<span data-ttu-id="d6a0d-154">**取得 \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="d6a0d-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="d6a0d-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="d6a0d-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
