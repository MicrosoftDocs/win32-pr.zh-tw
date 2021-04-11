---
description: 決定應用程式協定資料單位 (APDU) 的長度（以位元組為單位）。
ms.assetid: 005345d0-afdd-4534-9926-12378546d0ef
title: 'ISCardCmd：： get_ApduLength 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1535d2b4b67861b42719506ebd48cca4c49d5c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695384"
---
# <a name="iscardcmdget_apdulength-method"></a><span data-ttu-id="d7a77-103">ISCardCmd：： get \_ ApduLength 方法</span><span class="sxs-lookup"><span data-stu-id="d7a77-103">ISCardCmd::get\_ApduLength method</span></span>

<span data-ttu-id="d7a77-104">\[**Get \_ ApduLength** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d7a77-104">\[The **get\_ApduLength** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d7a77-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="d7a77-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d7a77-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d7a77-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d7a77-107">**Get \_ ApduLength** 方法會決定 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d7a77-107">The **get\_ApduLength** method determines the length, in bytes, f the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7a77-108">語法</span><span class="sxs-lookup"><span data-stu-id="d7a77-108">Syntax</span></span>


```C++
HRESULT get_ApduLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="d7a77-109">參數</span><span class="sxs-lookup"><span data-stu-id="d7a77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a77-110">*plSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d7a77-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7a77-111">APDU 長度的指標。</span><span class="sxs-lookup"><span data-stu-id="d7a77-111">Pointer to the length of the APDU.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7a77-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7a77-112">Return value</span></span>

<span data-ttu-id="d7a77-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="d7a77-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d7a77-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d7a77-114">Return code</span></span>                                                                                   | <span data-ttu-id="d7a77-115">Description</span><span class="sxs-lookup"><span data-stu-id="d7a77-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="d7a77-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a77-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d7a77-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="d7a77-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="d7a77-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a77-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d7a77-119">*PlSize* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="d7a77-119">The *plSize* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="d7a77-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a77-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d7a77-121">在 *plSize* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="d7a77-121">A bad pointer was passed in *plSize*.</span></span><br/> |
| <dl> <span data-ttu-id="d7a77-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d7a77-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d7a77-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="d7a77-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="d7a77-124">備註</span><span class="sxs-lookup"><span data-stu-id="d7a77-124">Remarks</span></span>

<span data-ttu-id="d7a77-125">若要取出原始的 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 從透過包含 APDU 訊息的 **IStream** 對應的位元組緩衝區，呼叫 [**get \_ APDU**](iscardcmd-get-apdu.md)。</span><span class="sxs-lookup"><span data-stu-id="d7a77-125">To retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="d7a77-126">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="d7a77-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="d7a77-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d7a77-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d7a77-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="d7a77-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d7a77-129">範例</span><span class="sxs-lookup"><span data-stu-id="d7a77-129">Examples</span></span>

<span data-ttu-id="d7a77-130">下列範例示範如何取得 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 長度。</span><span class="sxs-lookup"><span data-stu-id="d7a77-130">The following example shows how to retrieve the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) length.</span></span> <span data-ttu-id="d7a77-131">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="d7a77-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU length.
hr = pISCardCmd->get_ApduLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a><span data-ttu-id="d7a77-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7a77-132">Requirements</span></span>



| <span data-ttu-id="d7a77-133">需求</span><span class="sxs-lookup"><span data-stu-id="d7a77-133">Requirement</span></span> | <span data-ttu-id="d7a77-134">值</span><span class="sxs-lookup"><span data-stu-id="d7a77-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a77-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7a77-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a77-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7a77-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7a77-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7a77-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a77-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7a77-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7a77-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d7a77-139">End of client support</span></span><br/>    | <span data-ttu-id="d7a77-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7a77-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d7a77-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d7a77-141">End of server support</span></span><br/>    | <span data-ttu-id="d7a77-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d7a77-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d7a77-143">標頭</span><span class="sxs-lookup"><span data-stu-id="d7a77-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a77-144"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a77-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7a77-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d7a77-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7a77-146"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7a77-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7a77-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d7a77-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7a77-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7a77-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d7a77-149">IID</span><span class="sxs-lookup"><span data-stu-id="d7a77-149">IID</span></span><br/>                      | <span data-ttu-id="d7a77-150">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d7a77-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="d7a77-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7a77-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a77-152">**取得 \_ Apdu**</span><span class="sxs-lookup"><span data-stu-id="d7a77-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="d7a77-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="d7a77-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
