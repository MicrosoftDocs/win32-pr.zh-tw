---
description: ListCardInterfaces 方法會抓取指定智慧卡支援的所有介面 (Guid) 識別碼。
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'ISCardDatabase：： ListCardInterfaces 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d52324edd4a502388ac6064de07a6ab58a68074d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191150"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a><span data-ttu-id="d0d0d-103">ISCardDatabase：： ListCardInterfaces 方法</span><span class="sxs-lookup"><span data-stu-id="d0d0d-103">ISCardDatabase::ListCardInterfaces method</span></span>

<span data-ttu-id="d0d0d-104">\[**ListCardInterfaces** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-104">\[The **ListCardInterfaces** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d0d0d-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d0d0d-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d0d0d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d0d0d-107">**ListCardInterfaces** 方法會抓取指定 [*智慧卡*](../secgloss/s-gly.md)支援的所有介面 (guid) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-107">The **ListCardInterfaces** method retrieves the identifiers (GUIDs) of all the interfaces supported for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d0d-108">語法</span><span class="sxs-lookup"><span data-stu-id="d0d0d-108">Syntax</span></span>


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a><span data-ttu-id="d0d0d-109">參數</span><span class="sxs-lookup"><span data-stu-id="d0d0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0d0d-110">*bstrCardName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0d0d-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d0d-111">智慧卡的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="d0d0d-112">*ppInterfaceGuids* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d0d0d-112">*ppInterfaceGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0d0d-113">如果成功，則為介面 Guid 的指標;如果作業失敗，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-113">Pointer to the interface GUIDs if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0d0d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0d0d-114">Return value</span></span>

<span data-ttu-id="d0d0d-115">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d0d0d-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d0d0d-116">Return code</span></span>                                                                                   | <span data-ttu-id="d0d0d-117">Description</span><span class="sxs-lookup"><span data-stu-id="d0d0d-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="d0d0d-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d0d0d-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d0d0d-119">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="d0d0d-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d0d0d-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d0d0d-121">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="d0d0d-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d0d0d-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d0d0d-123">在 *ppInterfaceGuids* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-123">A bad pointer was passed in *ppInterfaceGuids*.</span></span><br/> |
| <dl> <span data-ttu-id="d0d0d-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d0d0d-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d0d0d-125">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="d0d0d-126">備註</span><span class="sxs-lookup"><span data-stu-id="d0d0d-126">Remarks</span></span>

<span data-ttu-id="d0d0d-127">若要取出智慧卡的 [*主要服務提供者*](../secgloss/p-gly.md) ，請呼叫 [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-127">To retrieve the [*primary service provider*](../secgloss/p-gly.md) of the smart card, call [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).</span></span>

<span data-ttu-id="d0d0d-128">若要取出所有已知的 [*智慧卡*](../secgloss/s-gly.md)、 [*讀取器*](../secgloss/r-gly.md)和 [*讀取器群組*](../secgloss/r-gly.md) ，請分別呼叫 [**ListCards**](iscarddatabase-listcards.md)、 [**ListReaders**](iscarddatabase-listreaders.md)和 [**ListReaderGroups**](iscarddatabase-listreadergroups.md) 。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md), and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="d0d0d-129">如需此介面所提供的所有方法清單，請參閱 [**ISCardDatabase**](iscarddatabase.md)。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="d0d0d-130">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d0d0d-131">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d0d0d-132">範例</span><span class="sxs-lookup"><span data-stu-id="d0d0d-132">Examples</span></span>

<span data-ttu-id="d0d0d-133">下列範例將示範如何取得所指定智慧卡所支援之介面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0d0d-133">The following example shows retrieving the identifiers of the interfaces supported for the specified smart card.</span></span>


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
}
```



## <a name="requirements"></a><span data-ttu-id="d0d0d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0d0d-134">Requirements</span></span>



| <span data-ttu-id="d0d0d-135">需求</span><span class="sxs-lookup"><span data-stu-id="d0d0d-135">Requirement</span></span> | <span data-ttu-id="d0d0d-136">值</span><span class="sxs-lookup"><span data-stu-id="d0d0d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0d0d-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0d0d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d0d0d-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0d0d-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d0d0d-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0d0d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d0d0d-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0d0d-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0d0d-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d0d0d-141">End of client support</span></span><br/>    | <span data-ttu-id="d0d0d-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0d0d-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d0d0d-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d0d0d-143">End of server support</span></span><br/>    | <span data-ttu-id="d0d0d-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0d0d-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d0d0d-145">標頭</span><span class="sxs-lookup"><span data-stu-id="d0d0d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0d0d-146"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0d0d-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0d0d-147">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d0d0d-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0d0d-148"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d0d0d-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d0d0d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d0d0d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0d0d-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0d0d-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0d0d-151">IID</span><span class="sxs-lookup"><span data-stu-id="d0d0d-151">IID</span></span><br/>                      | <span data-ttu-id="d0d0d-152">IID \_ ISCardDatabase 定義為1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d0d0d-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d0d0d-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0d0d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0d0d-154">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="d0d0d-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="d0d0d-155">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="d0d0d-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="d0d0d-156">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="d0d0d-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="d0d0d-157">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="d0d0d-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="d0d0d-158">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="d0d0d-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
