---
description: 從應用程式協定資料單位抓取第三個參數 (P3) 位元組 (APDU) 。
ms.assetid: 5fe90686-f542-42be-91ed-6600eaee3e7b
title: 'ISCardCmd：： get_P3 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P3
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b1072fc9c4ca3b2a238cc8893104df1a831c99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113224"
---
# <a name="iscardcmdget_p3-method"></a><span data-ttu-id="61baa-103">ISCardCmd：： get \_ P3 方法</span><span class="sxs-lookup"><span data-stu-id="61baa-103">ISCardCmd::get\_P3 method</span></span>

<span data-ttu-id="61baa-104">\[**取得 \_ P3** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="61baa-104">\[The **get\_P3** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="61baa-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="61baa-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="61baa-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="61baa-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="61baa-107">**取得 \_ P3** 方法會從 [*應用程式協定資料單位*](../secgloss/a-gly.md)（ (APDU) ）抓取第三個參數 (P3) 位元組。</span><span class="sxs-lookup"><span data-stu-id="61baa-107">The **get\_P3** method retrieves the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="61baa-108">這個唯讀位元組值代表 APDU 的資料部分大小。</span><span class="sxs-lookup"><span data-stu-id="61baa-108">This read-only byte value represents the size of the data portion of the APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="61baa-109">語法</span><span class="sxs-lookup"><span data-stu-id="61baa-109">Syntax</span></span>


```C++
HRESULT get_P3(
  [out] BYTE *pbyP3
);
```



## <a name="parameters"></a><span data-ttu-id="61baa-110">參數</span><span class="sxs-lookup"><span data-stu-id="61baa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61baa-111">*pbyP3* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61baa-111">*pbyP3* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61baa-112">從傳回的 APDU 到 P3 的位元組指標。</span><span class="sxs-lookup"><span data-stu-id="61baa-112">Pointer to the byte that is the P3 from the APDU on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61baa-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="61baa-113">Return value</span></span>

<span data-ttu-id="61baa-114">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="61baa-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="61baa-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="61baa-115">Return code</span></span>                                                                                   | <span data-ttu-id="61baa-116">Description</span><span class="sxs-lookup"><span data-stu-id="61baa-116">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="61baa-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="61baa-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="61baa-118">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="61baa-118">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="61baa-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="61baa-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="61baa-120">*PbyP3* 無效。</span><span class="sxs-lookup"><span data-stu-id="61baa-120">The *pbyP3* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="61baa-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="61baa-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="61baa-122">在 *pbyP3* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="61baa-122">A bad pointer was passed in *pbyP3*.</span></span><br/> |
| <dl> <span data-ttu-id="61baa-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="61baa-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="61baa-124">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="61baa-124">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="61baa-125">備註</span><span class="sxs-lookup"><span data-stu-id="61baa-125">Remarks</span></span>

<span data-ttu-id="61baa-126">P3 參數是唯讀的，因此無法設定。</span><span class="sxs-lookup"><span data-stu-id="61baa-126">The P3 parameter is read-only, and therefore cannot be set.</span></span>

<span data-ttu-id="61baa-127">若要取得 P1 或 P2 參數，請呼叫 [**get \_ P1**](iscardcmd-get-p1.md) 並分別 [**取得 \_ p2**](iscardcmd-get-p2.md) 。</span><span class="sxs-lookup"><span data-stu-id="61baa-127">To get the P1 or P2 parameters, call [**get\_P1**](iscardcmd-get-p1.md) and [**get\_P2**](iscardcmd-get-p2.md) respectively.</span></span>

<span data-ttu-id="61baa-128">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="61baa-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="61baa-129">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="61baa-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="61baa-130">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="61baa-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="61baa-131">範例</span><span class="sxs-lookup"><span data-stu-id="61baa-131">Examples</span></span>

<span data-ttu-id="61baa-132">下列範例示範如何從 [*應用程式協定資料單位*](../secgloss/a-gly.md) 取出第三個參數 (P3) 位元組 (APDU) 。</span><span class="sxs-lookup"><span data-stu-id="61baa-132">The following example shows how to retrieve the third parameter (P3) byte from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="61baa-133">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="61baa-133">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE  byP3;
HRESULT  hr;

// Retrieve the P3 byte.
hr = pISCardCmd->get_P3(&byP3);
if (FAILED(hr))
{
  printf("Failed get_P3\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="61baa-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="61baa-134">Requirements</span></span>



| <span data-ttu-id="61baa-135">需求</span><span class="sxs-lookup"><span data-stu-id="61baa-135">Requirement</span></span> | <span data-ttu-id="61baa-136">值</span><span class="sxs-lookup"><span data-stu-id="61baa-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61baa-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61baa-137">Minimum supported client</span></span><br/> | <span data-ttu-id="61baa-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61baa-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="61baa-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61baa-139">Minimum supported server</span></span><br/> | <span data-ttu-id="61baa-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61baa-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="61baa-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="61baa-141">End of client support</span></span><br/>    | <span data-ttu-id="61baa-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="61baa-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="61baa-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="61baa-143">End of server support</span></span><br/>    | <span data-ttu-id="61baa-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61baa-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="61baa-145">標頭</span><span class="sxs-lookup"><span data-stu-id="61baa-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="61baa-146"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="61baa-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="61baa-147">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="61baa-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="61baa-148"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="61baa-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="61baa-149">DLL</span><span class="sxs-lookup"><span data-stu-id="61baa-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61baa-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61baa-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="61baa-151">IID</span><span class="sxs-lookup"><span data-stu-id="61baa-151">IID</span></span><br/>                      | <span data-ttu-id="61baa-152">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="61baa-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="61baa-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61baa-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61baa-154">**取得 \_ P1**</span><span class="sxs-lookup"><span data-stu-id="61baa-154">**get\_P1**</span></span>](iscardcmd-get-p1.md)
</dt> <dt>

[<span data-ttu-id="61baa-155">**取得 \_ P2**</span><span class="sxs-lookup"><span data-stu-id="61baa-155">**get\_P2**</span></span>](iscardcmd-get-p2.md)
</dt> <dt>

[<span data-ttu-id="61baa-156">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="61baa-156">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
