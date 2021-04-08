---
description: AttachByReader 方法會在指定的讀取器中開啟智慧卡。
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: 'ISCard：： AttachByReader 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945036"
---
# <a name="iscardattachbyreader-method"></a><span data-ttu-id="14319-103">ISCard：： AttachByReader 方法</span><span class="sxs-lookup"><span data-stu-id="14319-103">ISCard::AttachByReader method</span></span>

<span data-ttu-id="14319-104">\[**AttachByReader** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="14319-104">\[The **AttachByReader** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="14319-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="14319-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="14319-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="14319-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="14319-107">**AttachByReader** 方法會在指定的 [*讀取器*](../secgloss/r-gly.md)中開啟 [*智慧卡*](../secgloss/s-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="14319-107">The **AttachByReader** method opens the [*smart card*](../secgloss/s-gly.md) in the named [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="14319-108">語法</span><span class="sxs-lookup"><span data-stu-id="14319-108">Syntax</span></span>


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="14319-109">參數</span><span class="sxs-lookup"><span data-stu-id="14319-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14319-110">*bstrReaderName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14319-110">*bstrReaderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14319-111">包含智慧卡讀卡機名稱的 **BSTR** 。</span><span class="sxs-lookup"><span data-stu-id="14319-111">A **BSTR** that contains the name of the smart card reader.</span></span>

</dd> <dt>

<span data-ttu-id="14319-112">*ShareMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14319-112">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14319-113">要在其中索取智慧卡存取權的模式。</span><span class="sxs-lookup"><span data-stu-id="14319-113">Mode in which to claim access to the smart card.</span></span>



| <span data-ttu-id="14319-114">值</span><span class="sxs-lookup"><span data-stu-id="14319-114">Value</span></span>                                                                                                                                            | <span data-ttu-id="14319-115">意義</span><span class="sxs-lookup"><span data-stu-id="14319-115">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="14319-116"><dt>**獨家**</dt></span><span class="sxs-lookup"><span data-stu-id="14319-116"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="14319-117">沒有其他人使用此智慧卡連線。</span><span class="sxs-lookup"><span data-stu-id="14319-117">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="14319-118"><dt>**共用**</dt></span><span class="sxs-lookup"><span data-stu-id="14319-118"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="14319-119">其他應用程式可以使用此連接。</span><span class="sxs-lookup"><span data-stu-id="14319-119">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="14319-120">*PrefProtocol* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14319-120">*PrefProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14319-121">慣用的通訊協定值。</span><span class="sxs-lookup"><span data-stu-id="14319-121">Preferred protocol value.</span></span>

<dl><span id="T0"></span><span id="t0"></span><dt>

<span data-ttu-id="14319-122">**T0**</span><span class="sxs-lookup"><span data-stu-id="14319-122">**T0**</span></span>
</dt><span id="T1"></span><span id="t1"></span><dt>

<span data-ttu-id="14319-123">**T1**</span><span class="sxs-lookup"><span data-stu-id="14319-123">**T1**</span></span>
</dt><span id="RAW"></span><span id="raw"></span><dt>

<span data-ttu-id="14319-124">**RAW**</span><span class="sxs-lookup"><span data-stu-id="14319-124">**RAW**</span></span>
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

<span data-ttu-id="14319-125">**T0 \| T1**</span><span class="sxs-lookup"><span data-stu-id="14319-125">**T0\|T1**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14319-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="14319-126">Return value</span></span>

<span data-ttu-id="14319-127">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="14319-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="14319-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="14319-128">Return code</span></span>                                                                                  | <span data-ttu-id="14319-129">Description</span><span class="sxs-lookup"><span data-stu-id="14319-129">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14319-130"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="14319-130"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="14319-131">在名為讀取器的智慧卡上開啟，已順利完成。</span><span class="sxs-lookup"><span data-stu-id="14319-131">Open on the smart card in the named reader has been completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="14319-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="14319-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="14319-133">傳遞至函式的一或多個參數發生問題。</span><span class="sxs-lookup"><span data-stu-id="14319-133">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14319-134">備註</span><span class="sxs-lookup"><span data-stu-id="14319-134">Remarks</span></span>

<span data-ttu-id="14319-135">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="14319-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="14319-136">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="14319-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="14319-137">當您完成使用讀取器時，請呼叫 [**ISCard：:D etach**](iscard-detach.md) 方法來釋放附件。</span><span class="sxs-lookup"><span data-stu-id="14319-137">When you have finished using the reader, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="14319-138">範例</span><span class="sxs-lookup"><span data-stu-id="14319-138">Examples</span></span>

<span data-ttu-id="14319-139">下列範例顯示如何在指定的智慧卡讀卡機中附加至智慧卡。</span><span class="sxs-lookup"><span data-stu-id="14319-139">The following example shows attaching to a smart card in a specified smart card reader.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a><span data-ttu-id="14319-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="14319-140">Requirements</span></span>



| <span data-ttu-id="14319-141">需求</span><span class="sxs-lookup"><span data-stu-id="14319-141">Requirement</span></span> | <span data-ttu-id="14319-142">值</span><span class="sxs-lookup"><span data-stu-id="14319-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14319-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14319-143">Minimum supported client</span></span><br/> | <span data-ttu-id="14319-144">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14319-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="14319-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14319-145">Minimum supported server</span></span><br/> | <span data-ttu-id="14319-146">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14319-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14319-147">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="14319-147">End of client support</span></span><br/>    | <span data-ttu-id="14319-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="14319-148">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="14319-149">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="14319-149">End of server support</span></span><br/>    | <span data-ttu-id="14319-150">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14319-150">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="14319-151">標頭</span><span class="sxs-lookup"><span data-stu-id="14319-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="14319-152"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="14319-152"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="14319-153">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="14319-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="14319-154"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="14319-154"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="14319-155">DLL</span><span class="sxs-lookup"><span data-stu-id="14319-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14319-156"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14319-156"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="14319-157">IID</span><span class="sxs-lookup"><span data-stu-id="14319-157">IID</span></span><br/>                      | <span data-ttu-id="14319-158">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="14319-158">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="14319-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14319-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14319-160">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="14319-160">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="14319-161">**中斷連結**</span><span class="sxs-lookup"><span data-stu-id="14319-161">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="14319-162">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="14319-162">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="14319-163">**附加**</span><span class="sxs-lookup"><span data-stu-id="14319-163">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
