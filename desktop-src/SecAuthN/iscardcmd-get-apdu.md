---
description: 抓取原始應用程式協定資料單位 (APDU) 。
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'ISCardCmd：： get_Apdu 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026238"
---
# <a name="iscardcmdget_apdu-method"></a><span data-ttu-id="8a510-103">ISCardCmd：：取得 \_ Apdu 方法</span><span class="sxs-lookup"><span data-stu-id="8a510-103">ISCardCmd::get\_Apdu method</span></span>

<span data-ttu-id="8a510-104">\[「 **取得 \_ Apdu** 」方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8a510-104">\[The **get\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8a510-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="8a510-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8a510-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="8a510-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8a510-107">「 **取得 \_ apdu** 」方法會抓取原始的 [*應用程式協定資料單位*](../secgloss/a-gly.md) (Apdu) 。</span><span class="sxs-lookup"><span data-stu-id="8a510-107">The **get\_Apdu** method retrieves the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a510-108">語法</span><span class="sxs-lookup"><span data-stu-id="8a510-108">Syntax</span></span>


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a><span data-ttu-id="8a510-109">參數</span><span class="sxs-lookup"><span data-stu-id="8a510-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a510-110">*ppApdu* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8a510-110">*ppApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a510-111">透過包含傳回之 APDU 訊息的 **IStream** 物件對應的位元組緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="8a510-111">Pointer to the byte buffer mapped through an **IStream** object that contains the APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a510-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a510-112">Return value</span></span>

<span data-ttu-id="8a510-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="8a510-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8a510-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8a510-114">Return code</span></span>                                                                                   | <span data-ttu-id="8a510-115">Description</span><span class="sxs-lookup"><span data-stu-id="8a510-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="8a510-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8a510-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8a510-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="8a510-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="8a510-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8a510-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8a510-119">*PpApdu* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="8a510-119">The *ppApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="8a510-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="8a510-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8a510-121">在 *ppApdu* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="8a510-121">A bad pointer was passed in *ppApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="8a510-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8a510-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8a510-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="8a510-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="8a510-124">備註</span><span class="sxs-lookup"><span data-stu-id="8a510-124">Remarks</span></span>

<span data-ttu-id="8a510-125">若要從 [**IByteBuffer**](ibytebuffer.md) 將 APDU 複製到包裝在此介面物件中的 Apdu (**IStream**) 物件，請呼叫 [**put \_ APDU**](iscardcmd-put-apdu.md)。</span><span class="sxs-lookup"><span data-stu-id="8a510-125">To copy the APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object, call [**put\_Apdu**](iscardcmd-put-apdu.md).</span></span>

<span data-ttu-id="8a510-126">若要判斷 APDU 的長度，請呼叫 [**get \_ ApduLength**](iscardcmd-get-apdulength.md)。</span><span class="sxs-lookup"><span data-stu-id="8a510-126">To determine the length of the APDU, call [**get\_ApduLength**](iscardcmd-get-apdulength.md).</span></span>

<span data-ttu-id="8a510-127">如需 [**ISCardCmd**](iscardcmd.md) 介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="8a510-127">For a list of all the methods provided by the [**ISCardCmd**](iscardcmd.md) interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="8a510-128">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8a510-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8a510-129">如需智慧卡錯誤碼的詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="8a510-129">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8a510-130">範例</span><span class="sxs-lookup"><span data-stu-id="8a510-130">Examples</span></span>

<span data-ttu-id="8a510-131">下列範例示範如何 (APDU) 取得原始的 [*應用程式協定資料單位*](../secgloss/a-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="8a510-131">The following example shows how to retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="8a510-132">此範例假設 pISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面的有效指標，而且 PIByteApdu 是 [**IByteBuffer**](ibytebuffer.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="8a510-132">The example assumes that pISCardCmd is a valid pointer to the [**ISCardCmd**](iscardcmd.md) interface, and that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="8a510-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a510-133">Requirements</span></span>



| <span data-ttu-id="8a510-134">需求</span><span class="sxs-lookup"><span data-stu-id="8a510-134">Requirement</span></span> | <span data-ttu-id="8a510-135">值</span><span class="sxs-lookup"><span data-stu-id="8a510-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a510-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a510-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8a510-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a510-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8a510-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a510-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8a510-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a510-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8a510-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8a510-140">End of client support</span></span><br/>    | <span data-ttu-id="8a510-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8a510-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8a510-142">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="8a510-142">End of server support</span></span><br/>    | <span data-ttu-id="8a510-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a510-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8a510-144">標頭</span><span class="sxs-lookup"><span data-stu-id="8a510-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a510-145"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a510-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a510-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8a510-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a510-147"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a510-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a510-148">DLL</span><span class="sxs-lookup"><span data-stu-id="8a510-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a510-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a510-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a510-150">IID</span><span class="sxs-lookup"><span data-stu-id="8a510-150">IID</span></span><br/>                      | <span data-ttu-id="8a510-151">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8a510-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="8a510-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a510-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a510-153">**取得 \_ ApduLength**</span><span class="sxs-lookup"><span data-stu-id="8a510-153">**get\_ApduLength**</span></span>](iscardcmd-get-apdulength.md)
</dt> <dt>

[<span data-ttu-id="8a510-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="8a510-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="8a510-155">**put \_ Apdu**</span><span class="sxs-lookup"><span data-stu-id="8a510-155">**put\_Apdu**</span></span>](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
