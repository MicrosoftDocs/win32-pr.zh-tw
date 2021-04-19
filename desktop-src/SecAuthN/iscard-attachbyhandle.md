---
description: 將 ISCard 物件附加至開啟和設定的智慧卡控點。
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: 'ISCard：： AttachByHandle 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990409"
---
# <a name="iscardattachbyhandle-method"></a><span data-ttu-id="6ea13-103">ISCard：： AttachByHandle 方法</span><span class="sxs-lookup"><span data-stu-id="6ea13-103">ISCard::AttachByHandle method</span></span>

<span data-ttu-id="6ea13-104">\[**AttachByHandle** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6ea13-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ea13-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6ea13-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6ea13-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6ea13-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6ea13-107">**AttachByHandle** 方法會將 [**ISCard**](iscard.md)物件附加至開啟和設定的 [*智慧卡*](../secgloss/s-gly.md)控制碼。</span><span class="sxs-lookup"><span data-stu-id="6ea13-107">The **AttachByHandle** method attaches the [**ISCard**](iscard.md) object to an open and configured [*smart card*](../secgloss/s-gly.md) handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea13-108">語法</span><span class="sxs-lookup"><span data-stu-id="6ea13-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a><span data-ttu-id="6ea13-109">參數</span><span class="sxs-lookup"><span data-stu-id="6ea13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ea13-110">*hCard* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ea13-110">*hCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ea13-111">智慧卡的開啟連接控制碼。</span><span class="sxs-lookup"><span data-stu-id="6ea13-111">A handle to an open connection to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ea13-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ea13-112">Return value</span></span>

<span data-ttu-id="6ea13-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="6ea13-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6ea13-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6ea13-114">Return code</span></span>                                                                                  | <span data-ttu-id="6ea13-115">Description</span><span class="sxs-lookup"><span data-stu-id="6ea13-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="6ea13-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6ea13-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6ea13-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="6ea13-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="6ea13-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6ea13-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6ea13-119">*HCard* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="6ea13-119">The *hCard* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6ea13-120">備註</span><span class="sxs-lookup"><span data-stu-id="6ea13-120">Remarks</span></span>

<span data-ttu-id="6ea13-121">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6ea13-121">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6ea13-122">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6ea13-122">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="6ea13-123">當您完成使用控制碼時，請呼叫 [**ISCard：:D etach**](iscard-detach.md) 方法來釋放附件。</span><span class="sxs-lookup"><span data-stu-id="6ea13-123">When you have finished using the handle, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="6ea13-124">範例</span><span class="sxs-lookup"><span data-stu-id="6ea13-124">Examples</span></span>

<span data-ttu-id="6ea13-125">下列範例顯示如何附加至智慧卡控制碼。</span><span class="sxs-lookup"><span data-stu-id="6ea13-125">The following example shows attaching to a smart card handle.</span></span>


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
```



## <a name="requirements"></a><span data-ttu-id="6ea13-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ea13-126">Requirements</span></span>



| <span data-ttu-id="6ea13-127">需求</span><span class="sxs-lookup"><span data-stu-id="6ea13-127">Requirement</span></span> | <span data-ttu-id="6ea13-128">值</span><span class="sxs-lookup"><span data-stu-id="6ea13-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea13-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ea13-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6ea13-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ea13-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6ea13-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ea13-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6ea13-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ea13-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ea13-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6ea13-133">End of client support</span></span><br/>    | <span data-ttu-id="6ea13-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ea13-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6ea13-135">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6ea13-135">End of server support</span></span><br/>    | <span data-ttu-id="6ea13-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ea13-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6ea13-137">標頭</span><span class="sxs-lookup"><span data-stu-id="6ea13-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ea13-138"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ea13-138"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ea13-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6ea13-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ea13-140"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6ea13-140"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6ea13-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6ea13-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ea13-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ea13-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ea13-143">IID</span><span class="sxs-lookup"><span data-stu-id="6ea13-143">IID</span></span><br/>                      | <span data-ttu-id="6ea13-144">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6ea13-144">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6ea13-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ea13-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ea13-146">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="6ea13-146">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="6ea13-147">**中斷連結**</span><span class="sxs-lookup"><span data-stu-id="6ea13-147">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="6ea13-148">**取得 \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="6ea13-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="6ea13-149">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="6ea13-149">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="6ea13-150">**附加**</span><span class="sxs-lookup"><span data-stu-id="6ea13-150">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
