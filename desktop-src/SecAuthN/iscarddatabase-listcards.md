---
description: ListCards 方法會將符合指定介面識別碼的所有智慧卡名稱， (Guid) 、指定的 ATR 字串或兩者。
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'ISCardDatabase：： ListCards 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e8a5bf56aa27a044d29e2e0153698bfefe69e1d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690519"
---
# <a name="iscarddatabaselistcards-method"></a><span data-ttu-id="1bad8-103">ISCardDatabase：： ListCards 方法</span><span class="sxs-lookup"><span data-stu-id="1bad8-103">ISCardDatabase::ListCards method</span></span>

<span data-ttu-id="1bad8-104">\[**ListCards** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1bad8-104">\[The **ListCards** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1bad8-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="1bad8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1bad8-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="1bad8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1bad8-107">**ListCards** 方法會將符合指定介面識別碼的所有智慧卡名稱， (guid) 、指定的 [*ATR 字串*](../secgloss/a-gly.md)或兩者。</span><span class="sxs-lookup"><span data-stu-id="1bad8-107">The **ListCards** method retrieves all of the smart card names that match the specified interface identifiers (GUIDs), the specified [*ATR string*](../secgloss/a-gly.md), or both.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bad8-108">語法</span><span class="sxs-lookup"><span data-stu-id="1bad8-108">Syntax</span></span>


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a><span data-ttu-id="1bad8-109">參數</span><span class="sxs-lookup"><span data-stu-id="1bad8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bad8-110">*pAtr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bad8-110">*pAtr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bad8-111">[*智慧卡*](../secgloss/s-gly.md)ATR 字串的指標。</span><span class="sxs-lookup"><span data-stu-id="1bad8-111">Pointer to a [*smart card*](../secgloss/s-gly.md) ATR string.</span></span> <span data-ttu-id="1bad8-112">ATR 字串必須封裝成 [**IByteBuffer**](ibytebuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="1bad8-112">The ATR string must be packaged into an [**IByteBuffer**](ibytebuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bad8-113">*pInterfaceGuids* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bad8-113">*pInterfaceGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bad8-114">COM 介面識別碼之 SAFEARRAY 的指標， (Guid) BSTR 格式。</span><span class="sxs-lookup"><span data-stu-id="1bad8-114">Pointer to a SAFEARRAY of COM interface identifiers (GUIDs) in BSTR format.</span></span>

</dd> <dt>

<span data-ttu-id="1bad8-115">*localeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bad8-115">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bad8-116">語言當地語系化識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bad8-116">Language localization identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1bad8-117">*ppCardNames* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1bad8-117">*ppCardNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bad8-118">Bstr 之 SAFEARRAY 的指標，其中包含符合搜尋參數的智慧卡名稱（如果成功的話）;如果作業失敗，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="1bad8-118">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart cards that satisfied the search parameters if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bad8-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="1bad8-119">Return value</span></span>

<span data-ttu-id="1bad8-120">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="1bad8-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1bad8-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1bad8-121">Return code</span></span>                                                                                   | <span data-ttu-id="1bad8-122">Description</span><span class="sxs-lookup"><span data-stu-id="1bad8-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1bad8-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1bad8-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1bad8-124">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="1bad8-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1bad8-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1bad8-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1bad8-126">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="1bad8-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1bad8-127"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="1bad8-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1bad8-128">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="1bad8-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="1bad8-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1bad8-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1bad8-130">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="1bad8-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1bad8-131">備註</span><span class="sxs-lookup"><span data-stu-id="1bad8-131">Remarks</span></span>

<span data-ttu-id="1bad8-132">若要取出所有已知的 [*讀取*](../secgloss/r-gly.md) 器或 [*讀取器*](../secgloss/r-gly.md)，請分別呼叫 [**ListReaders**](iscarddatabase-listreaders.md) 或 [**ListReaderGroups**](iscarddatabase-listreadergroups.md) 。</span><span class="sxs-lookup"><span data-stu-id="1bad8-132">To retrieve all known [*readers*](../secgloss/r-gly.md) or [*reader*](../secgloss/r-gly.md), call [**ListReaders**](iscarddatabase-listreaders.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="1bad8-133">分別取出特定卡片 [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)或 [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)的 [*主要服務*](../secgloss/p-gly.md)或介面。</span><span class="sxs-lookup"><span data-stu-id="1bad8-133">To retrieve the [*primary service*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="1bad8-134">如需此介面所提供的所有方法清單，請參閱 [**ISCardDatabase**](iscarddatabase.md)。</span><span class="sxs-lookup"><span data-stu-id="1bad8-134">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="1bad8-135">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1bad8-135">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1bad8-136">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="1bad8-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1bad8-137">範例</span><span class="sxs-lookup"><span data-stu-id="1bad8-137">Examples</span></span>

<span data-ttu-id="1bad8-138">下列範例顯示如何抓取符合指定 ATR 字串的智慧卡名稱。</span><span class="sxs-lookup"><span data-stu-id="1bad8-138">The following example shows retrieving the smart card names that match the specified ATR string.</span></span>


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="1bad8-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bad8-139">Requirements</span></span>



| <span data-ttu-id="1bad8-140">需求</span><span class="sxs-lookup"><span data-stu-id="1bad8-140">Requirement</span></span> | <span data-ttu-id="1bad8-141">值</span><span class="sxs-lookup"><span data-stu-id="1bad8-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bad8-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bad8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1bad8-143">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bad8-143">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1bad8-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bad8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1bad8-145">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bad8-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1bad8-146">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1bad8-146">End of client support</span></span><br/>    | <span data-ttu-id="1bad8-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1bad8-147">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1bad8-148">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1bad8-148">End of server support</span></span><br/>    | <span data-ttu-id="1bad8-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1bad8-149">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1bad8-150">標頭</span><span class="sxs-lookup"><span data-stu-id="1bad8-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bad8-151"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="1bad8-151"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="1bad8-152">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1bad8-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="1bad8-153"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1bad8-153"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1bad8-154">DLL</span><span class="sxs-lookup"><span data-stu-id="1bad8-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bad8-155"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bad8-155"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1bad8-156">IID</span><span class="sxs-lookup"><span data-stu-id="1bad8-156">IID</span></span><br/>                      | <span data-ttu-id="1bad8-157">IID \_ ISCardDatabase 定義為1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1bad8-157">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1bad8-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bad8-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bad8-159">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="1bad8-159">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="1bad8-160">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="1bad8-160">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="1bad8-161">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="1bad8-161">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="1bad8-162">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="1bad8-162">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="1bad8-163">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="1bad8-163">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
