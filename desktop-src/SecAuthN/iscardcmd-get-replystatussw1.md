---
description: 抓取回復 Apdu SW1 狀態位元組。
ms.assetid: 5f74d0c9-cf82-4694-bca6-a2655e717a1f
title: 'ISCardCmd：： get_ReplyStatusSW1 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92bcf490a3cb1fc533bcf9a1046642d3c3e55b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511561"
---
# <a name="iscardcmdget_replystatussw1-method"></a><span data-ttu-id="ae5a7-103">ISCardCmd：： get \_ ReplyStatusSW1 方法</span><span class="sxs-lookup"><span data-stu-id="ae5a7-103">ISCardCmd::get\_ReplyStatusSW1 method</span></span>

<span data-ttu-id="ae5a7-104">\[**Get \_ ReplyStatusSW1** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-104">\[The **get\_ReplyStatusSW1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ae5a7-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ae5a7-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ae5a7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ae5a7-107">**Get \_ ReplyStatusSW1** 方法會抓取 [*reply apdu*](../secgloss/r-gly.md) SW1 status byte。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-107">The **get\_ReplyStatusSW1** method retrieves the [*reply APDUs*](../secgloss/r-gly.md) SW1 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae5a7-108">語法</span><span class="sxs-lookup"><span data-stu-id="ae5a7-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW1(
  [out] LPBYTE pbySW1
);
```



## <a name="parameters"></a><span data-ttu-id="ae5a7-109">參數</span><span class="sxs-lookup"><span data-stu-id="ae5a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae5a7-110">*pbySW1* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ae5a7-110">*pbySW1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae5a7-111">傳回時，包含 SW1 位元組值的位元組指標。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-111">Pointer to the byte that contains the value of the SW1 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae5a7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae5a7-112">Return value</span></span>

<span data-ttu-id="ae5a7-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ae5a7-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ae5a7-114">Return code</span></span>                                                                                   | <span data-ttu-id="ae5a7-115">Description</span><span class="sxs-lookup"><span data-stu-id="ae5a7-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="ae5a7-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ae5a7-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ae5a7-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="ae5a7-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ae5a7-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ae5a7-119">*PbySW1* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-119">The *pbySW1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ae5a7-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="ae5a7-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ae5a7-121">在 *pbySW1* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-121">A bad pointer was passed in *pbySW1*.</span></span><br/> |
| <dl> <span data-ttu-id="ae5a7-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ae5a7-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ae5a7-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="ae5a7-124">備註</span><span class="sxs-lookup"><span data-stu-id="ae5a7-124">Remarks</span></span>

<span data-ttu-id="ae5a7-125">[*回復 APDU 的*](../secgloss/r-gly.md)SW1 狀態位元組是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-125">The [*reply APDU's*](../secgloss/r-gly.md) SW1 status byte is read-only.</span></span>

<span data-ttu-id="ae5a7-126">若要取得回復 APDU 的 SW2 狀態位元組，請呼叫 [**get \_ ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-126">To retrieve the reply APDU's SW2 status byte, call [**get\_ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).</span></span>

<span data-ttu-id="ae5a7-127">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="ae5a7-128">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ae5a7-129">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ae5a7-130">範例</span><span class="sxs-lookup"><span data-stu-id="ae5a7-130">Examples</span></span>

<span data-ttu-id="ae5a7-131">下列範例示範如何取出 [*回復 APDU*](../secgloss/r-gly.md)的 SW1 狀態位元組。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-131">The following example shows how to retrieve the SW1 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="ae5a7-132">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="ae5a7-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW1;
HRESULT  hr;

// Retrieve the reply status SW1 byte.
hr = pISCardCmd->get_ReplyStatusSW1(&bySW1);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="ae5a7-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae5a7-133">Requirements</span></span>



| <span data-ttu-id="ae5a7-134">需求</span><span class="sxs-lookup"><span data-stu-id="ae5a7-134">Requirement</span></span> | <span data-ttu-id="ae5a7-135">值</span><span class="sxs-lookup"><span data-stu-id="ae5a7-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5a7-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae5a7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ae5a7-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae5a7-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ae5a7-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae5a7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ae5a7-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae5a7-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae5a7-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ae5a7-140">End of client support</span></span><br/>    | <span data-ttu-id="ae5a7-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ae5a7-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ae5a7-142">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ae5a7-142">End of server support</span></span><br/>    | <span data-ttu-id="ae5a7-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ae5a7-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ae5a7-144">標頭</span><span class="sxs-lookup"><span data-stu-id="ae5a7-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae5a7-145"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="ae5a7-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ae5a7-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ae5a7-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae5a7-147"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ae5a7-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ae5a7-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ae5a7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae5a7-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae5a7-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae5a7-150">IID</span><span class="sxs-lookup"><span data-stu-id="ae5a7-150">IID</span></span><br/>                      | <span data-ttu-id="ae5a7-151">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ae5a7-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ae5a7-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae5a7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae5a7-153">**取得 \_ ReplyStatusSW2**</span><span class="sxs-lookup"><span data-stu-id="ae5a7-153">**get\_ReplyStatusSW2**</span></span>](iscardcmd-get-replystatussw2.md)
</dt> <dt>

[<span data-ttu-id="ae5a7-154">**取得 \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="ae5a7-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="ae5a7-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="ae5a7-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
