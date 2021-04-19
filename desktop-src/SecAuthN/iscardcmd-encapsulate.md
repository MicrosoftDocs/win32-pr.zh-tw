---
description: 封裝方法會將指定的命令應用程式協定資料單位封裝 (APDU) 至另一個命令 APDU，以傳輸至智慧卡。
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: 'ISCardCmd：：封裝方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cd671a11edd9977695eeaf858e38f962b3dd0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985020"
---
# <a name="iscardcmdencapsulate-method"></a><span data-ttu-id="107db-103">ISCardCmd：：封裝方法</span><span class="sxs-lookup"><span data-stu-id="107db-103">ISCardCmd::Encapsulate method</span></span>

<span data-ttu-id="107db-104">\[**封裝** 方法可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="107db-104">\[The **Encapsulate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="107db-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="107db-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="107db-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="107db-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="107db-107">**封裝** 方法會將指定的命令 [*應用程式協定資料單位*](../secgloss/a-gly.md)封裝 (APDU) 至另一個命令 APDU，以傳輸至 [*智慧卡*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="107db-107">The **Encapsulate** method encapsulates the given command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) into another command APDU for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="107db-108">語法</span><span class="sxs-lookup"><span data-stu-id="107db-108">Syntax</span></span>


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a><span data-ttu-id="107db-109">參數</span><span class="sxs-lookup"><span data-stu-id="107db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="107db-110">*pApdu* \[在\]</span><span class="sxs-lookup"><span data-stu-id="107db-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="107db-111">要封裝的 APDU 指標。</span><span class="sxs-lookup"><span data-stu-id="107db-111">Pointer to the APDU to be encapsulated.</span></span>

</dd> <dt>

<span data-ttu-id="107db-112">*ApduType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="107db-112">*ApduType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="107db-113">[*T = 0*](../secgloss/t-gly.md)傳輸的 ISO 7816-4 案例。</span><span class="sxs-lookup"><span data-stu-id="107db-113">ISO 7816-4 case for [*T=0*](../secgloss/t-gly.md) transmissions.</span></span>

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

<span data-ttu-id="107db-114">**ISO \_ 案例 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="107db-114">**ISO\_CASE\_1**</span></span>
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

<span data-ttu-id="107db-115">**ISO \_ 案例 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="107db-115">**ISO\_CASE\_2**</span></span>
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

<span data-ttu-id="107db-116">**ISO \_ 案例 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="107db-116">**ISO\_CASE\_3**</span></span>
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

<span data-ttu-id="107db-117">**ISO \_ 案例 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="107db-117">**ISO\_CASE\_4**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="107db-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="107db-118">Return value</span></span>

<span data-ttu-id="107db-119">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="107db-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="107db-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="107db-120">Return code</span></span>                                                                                   | <span data-ttu-id="107db-121">Description</span><span class="sxs-lookup"><span data-stu-id="107db-121">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="107db-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="107db-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="107db-123">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="107db-123">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="107db-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="107db-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="107db-125">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="107db-125">Invalid parameter.</span></span><br/>                   |
| <dl> <span data-ttu-id="107db-126"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="107db-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="107db-127">在 *pApdu* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="107db-127">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="107db-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="107db-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="107db-129">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="107db-129">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="107db-130">備註</span><span class="sxs-lookup"><span data-stu-id="107db-130">Remarks</span></span>

<span data-ttu-id="107db-131">若要建立命令 APDU，請呼叫 [**BuildCmd**](iscardcmd-buildcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="107db-131">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="107db-132">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="107db-132">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="107db-133">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="107db-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="107db-134">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="107db-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="107db-135">範例</span><span class="sxs-lookup"><span data-stu-id="107db-135">Examples</span></span>

<span data-ttu-id="107db-136">下列範例顯示如何封裝命令 APDU。</span><span class="sxs-lookup"><span data-stu-id="107db-136">The following example shows how to encapsulate a command APDU.</span></span> <span data-ttu-id="107db-137">此範例假設 pIByteApdu 是 [**IByteBuffer**](ibytebuffer.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="107db-137">The example assumes that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="107db-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="107db-138">Requirements</span></span>



| <span data-ttu-id="107db-139">需求</span><span class="sxs-lookup"><span data-stu-id="107db-139">Requirement</span></span> | <span data-ttu-id="107db-140">值</span><span class="sxs-lookup"><span data-stu-id="107db-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="107db-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="107db-141">Minimum supported client</span></span><br/> | <span data-ttu-id="107db-142">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="107db-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="107db-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="107db-143">Minimum supported server</span></span><br/> | <span data-ttu-id="107db-144">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="107db-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="107db-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="107db-145">End of client support</span></span><br/>    | <span data-ttu-id="107db-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="107db-146">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="107db-147">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="107db-147">End of server support</span></span><br/>    | <span data-ttu-id="107db-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="107db-148">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="107db-149">標頭</span><span class="sxs-lookup"><span data-stu-id="107db-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="107db-150"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="107db-150"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="107db-151">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="107db-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="107db-152"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="107db-152"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="107db-153">DLL</span><span class="sxs-lookup"><span data-stu-id="107db-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="107db-154"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="107db-154"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="107db-155">IID</span><span class="sxs-lookup"><span data-stu-id="107db-155">IID</span></span><br/>                      | <span data-ttu-id="107db-156">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="107db-156">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="107db-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="107db-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="107db-158">**BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="107db-158">**BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="107db-159">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="107db-159">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
