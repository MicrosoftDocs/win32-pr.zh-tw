---
description: 設定新的回復 APDU 訊息狀態字組。
ms.assetid: 17b498eb-2268-451a-9f5c-c53cb7e42019
title: 'ISCardCmd：:p ut_ReplyStatus 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 55e6de81cd7e2c98b527d0852ea31a25f8256c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112181"
---
# <a name="iscardcmdput_replystatus-method"></a><span data-ttu-id="5dde5-103">ISCardCmd：:p 的 \_ ReplyStatus 方法</span><span class="sxs-lookup"><span data-stu-id="5dde5-103">ISCardCmd::put\_ReplyStatus method</span></span>

<span data-ttu-id="5dde5-104">\[**Put \_ ReplyStatus** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5dde5-104">\[The **put\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5dde5-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="5dde5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5dde5-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="5dde5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5dde5-107">**Put \_ ReplyStatus** 方法會設定新的 [*回復 APDU*](../secgloss/r-gly.md)訊息狀態字組。</span><span class="sxs-lookup"><span data-stu-id="5dde5-107">The **put\_ReplyStatus** method sets a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dde5-108">語法</span><span class="sxs-lookup"><span data-stu-id="5dde5-108">Syntax</span></span>


```C++
HRESULT put_ReplyStatus(
  [in] WORD wStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5dde5-109">參數</span><span class="sxs-lookup"><span data-stu-id="5dde5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dde5-110">*wStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5dde5-110">*wStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dde5-111">狀態的單字。</span><span class="sxs-lookup"><span data-stu-id="5dde5-111">Word that is the status.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dde5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5dde5-112">Return value</span></span>

<span data-ttu-id="5dde5-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="5dde5-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="5dde5-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5dde5-114">Return code</span></span>                                                                                   | <span data-ttu-id="5dde5-115">Description</span><span class="sxs-lookup"><span data-stu-id="5dde5-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="5dde5-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5dde5-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5dde5-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="5dde5-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="5dde5-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5dde5-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5dde5-119">*WStatus* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="5dde5-119">The *wStatus* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="5dde5-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5dde5-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5dde5-121">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="5dde5-121">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="5dde5-122">備註</span><span class="sxs-lookup"><span data-stu-id="5dde5-122">Remarks</span></span>

<span data-ttu-id="5dde5-123">若要取得回復 APDU 的訊息狀態文字，請呼叫 [**get \_ ReplyStatus**](iscardcmd-get-replystatus.md)。</span><span class="sxs-lookup"><span data-stu-id="5dde5-123">To get the reply APDU's message status word, call [**get\_ReplyStatus**](iscardcmd-get-replystatus.md).</span></span>

<span data-ttu-id="5dde5-124">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="5dde5-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="5dde5-125">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5dde5-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="5dde5-126">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="5dde5-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5dde5-127">範例</span><span class="sxs-lookup"><span data-stu-id="5dde5-127">Examples</span></span>

<span data-ttu-id="5dde5-128">下列範例顯示如何設定新的 [*回復 APDU*](../secgloss/r-gly.md) 訊息狀態字組。</span><span class="sxs-lookup"><span data-stu-id="5dde5-128">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span> <span data-ttu-id="5dde5-129">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="5dde5-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD     wNewStatus = 0x0000;
HRESULT  hr;

// Set reply status.
hr = pISCardCmd->put_ReplyStatus(wNewStatus);
if (FAILED(hr))
{
  printf("Failed put_ReplyStatus\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="5dde5-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="5dde5-130">Requirements</span></span>



| <span data-ttu-id="5dde5-131">需求</span><span class="sxs-lookup"><span data-stu-id="5dde5-131">Requirement</span></span> | <span data-ttu-id="5dde5-132">值</span><span class="sxs-lookup"><span data-stu-id="5dde5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dde5-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5dde5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5dde5-134">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dde5-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5dde5-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5dde5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5dde5-136">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dde5-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5dde5-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5dde5-137">End of client support</span></span><br/>    | <span data-ttu-id="5dde5-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5dde5-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5dde5-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5dde5-139">End of server support</span></span><br/>    | <span data-ttu-id="5dde5-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5dde5-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5dde5-141">標頭</span><span class="sxs-lookup"><span data-stu-id="5dde5-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dde5-142"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="5dde5-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dde5-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5dde5-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="5dde5-144"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5dde5-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5dde5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5dde5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dde5-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dde5-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5dde5-147">IID</span><span class="sxs-lookup"><span data-stu-id="5dde5-147">IID</span></span><br/>                      | <span data-ttu-id="5dde5-148">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="5dde5-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="5dde5-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5dde5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dde5-150">**取得 \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="5dde5-150">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="5dde5-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="5dde5-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
