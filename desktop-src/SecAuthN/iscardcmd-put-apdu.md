---
description: 將 IByteBuffer (IStream) 物件中的應用程式協定資料單位 (APDU) 複製到包裝在此介面物件中的 APDU。
ms.assetid: 28dac222-ee7a-40aa-903b-e9c0b7757c9c
title: 'ISCardCmd：:p ut_Apdu 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee615e7f2e8d7555cfed276658e8de1a97ddf73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943443"
---
# <a name="iscardcmdput_apdu-method"></a><span data-ttu-id="57520-103">ISCardCmd：:p 內容] \_ Apdu 方法</span><span class="sxs-lookup"><span data-stu-id="57520-103">ISCardCmd::put\_Apdu method</span></span>

<span data-ttu-id="57520-104">\[**Put \_ Apdu** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="57520-104">\[The **put\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="57520-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="57520-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="57520-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="57520-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="57520-107">**Put \_ Apdu** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md) (Apdu) 從 [**IByteBuffer**](ibytebuffer.md) (**IStream**) 物件複製到包裝在此介面物件中的 apdu。</span><span class="sxs-lookup"><span data-stu-id="57520-107">The **put\_Apdu** method copies the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="57520-108">語法</span><span class="sxs-lookup"><span data-stu-id="57520-108">Syntax</span></span>


```C++
HRESULT put_Apdu(
  [in] LPBYTEBUFFER pApdu
);
```



## <a name="parameters"></a><span data-ttu-id="57520-109">參數</span><span class="sxs-lookup"><span data-stu-id="57520-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57520-110">*pApdu* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57520-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57520-111">要在其中複製的 ISO 7816-4 APDU 指標。</span><span class="sxs-lookup"><span data-stu-id="57520-111">Pointer to the ISO 7816-4 APDU to be copied in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57520-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="57520-112">Return value</span></span>

<span data-ttu-id="57520-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="57520-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="57520-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="57520-114">Return code</span></span>                                                                                   | <span data-ttu-id="57520-115">Description</span><span class="sxs-lookup"><span data-stu-id="57520-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="57520-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="57520-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="57520-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="57520-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="57520-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="57520-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="57520-119">*PApdu* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="57520-119">The *pApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="57520-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="57520-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="57520-121">在 *pApdu* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="57520-121">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="57520-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="57520-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="57520-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="57520-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="57520-124">備註</span><span class="sxs-lookup"><span data-stu-id="57520-124">Remarks</span></span>

<span data-ttu-id="57520-125">若要從透過包含 APDU 訊息的 **IStream** 對應的位元組緩衝區取出原始的 APDU，請呼叫 [**get \_ APDU**](iscardcmd-get-apdu.md)。</span><span class="sxs-lookup"><span data-stu-id="57520-125">To retrieve the raw APDU from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="57520-126">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="57520-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="57520-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57520-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="57520-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="57520-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="57520-129">範例</span><span class="sxs-lookup"><span data-stu-id="57520-129">Examples</span></span>

<span data-ttu-id="57520-130">下列範例示範如何將 [**IByteBuffer**](ibytebuffer.md) (**IStream**) 物件中的 apdu 複製到包裝在 INTERFACE 物件中的 apdu。</span><span class="sxs-lookup"><span data-stu-id="57520-130">The following example shows how to copy an APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in an interface object.</span></span> <span data-ttu-id="57520-131">此範例假設 pIByteApdu 是 **IByteBuffer** 實例的有效指標，而且 PISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="57520-131">The example assumes that pIByteApdu is a valid pointer to an instance of **IByteBuffer** and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;


// Set the APDU.
hr = pISCardCmd->put_Apdu(pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed put_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="57520-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="57520-132">Requirements</span></span>



| <span data-ttu-id="57520-133">需求</span><span class="sxs-lookup"><span data-stu-id="57520-133">Requirement</span></span> | <span data-ttu-id="57520-134">值</span><span class="sxs-lookup"><span data-stu-id="57520-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57520-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57520-135">Minimum supported client</span></span><br/> | <span data-ttu-id="57520-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57520-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="57520-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57520-137">Minimum supported server</span></span><br/> | <span data-ttu-id="57520-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57520-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57520-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="57520-139">End of client support</span></span><br/>    | <span data-ttu-id="57520-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="57520-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="57520-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="57520-141">End of server support</span></span><br/>    | <span data-ttu-id="57520-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="57520-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="57520-143">標頭</span><span class="sxs-lookup"><span data-stu-id="57520-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="57520-144"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="57520-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="57520-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="57520-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="57520-146"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="57520-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="57520-147">DLL</span><span class="sxs-lookup"><span data-stu-id="57520-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57520-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57520-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="57520-149">IID</span><span class="sxs-lookup"><span data-stu-id="57520-149">IID</span></span><br/>                      | <span data-ttu-id="57520-150">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="57520-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="57520-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57520-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57520-152">**取得 \_ Apdu**</span><span class="sxs-lookup"><span data-stu-id="57520-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="57520-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="57520-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
