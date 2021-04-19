---
description: ListReaders 方法會抓取智慧卡資料庫中註冊之智慧卡讀取器的名稱。
ms.assetid: e1ca85a1-9206-4c09-ba0f-10b60e472dfb
title: 'ISCardDatabase：： ListReaders 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaders
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dcd78066a95c69b75d5089ba1683e5c937cb7414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991732"
---
# <a name="iscarddatabaselistreaders-method"></a><span data-ttu-id="8d872-103">ISCardDatabase：： ListReaders 方法</span><span class="sxs-lookup"><span data-stu-id="8d872-103">ISCardDatabase::ListReaders method</span></span>

<span data-ttu-id="8d872-104">\[**ListReaders** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8d872-104">\[The **ListReaders** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8d872-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="8d872-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8d872-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="8d872-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8d872-107">**ListReaders** 方法會抓取 [*智慧卡資料庫*](../secgloss/s-gly.md)中註冊之智慧卡 [*讀取器*](../secgloss/r-gly.md)的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d872-107">The **ListReaders** method retrieves the names of the smart card [*readers*](../secgloss/r-gly.md) registered in the [*smart card database*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d872-108">語法</span><span class="sxs-lookup"><span data-stu-id="8d872-108">Syntax</span></span>


```C++
HRESULT ListReaders(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaders
);
```



## <a name="parameters"></a><span data-ttu-id="8d872-109">參數</span><span class="sxs-lookup"><span data-stu-id="8d872-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d872-110">*localeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8d872-110">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d872-111">語言當地語系化識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d872-111">Language localization ID.</span></span>

</dd> <dt>

<span data-ttu-id="8d872-112">*ppReaders* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8d872-112">*ppReaders* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d872-113">如果成功，則為 Bstr 的 SAFEARRAY 的指標，其中包含智慧卡讀取器的名稱;如果作業失敗，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="8d872-113">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart card readers if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d872-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d872-114">Return value</span></span>

<span data-ttu-id="8d872-115">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="8d872-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8d872-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8d872-116">Return code</span></span>                                                                                   | <span data-ttu-id="8d872-117">Description</span><span class="sxs-lookup"><span data-stu-id="8d872-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="8d872-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8d872-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8d872-119">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="8d872-119">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="8d872-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8d872-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8d872-121">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="8d872-121">Invalid parameter.</span></span><br/>                       |
| <dl> <span data-ttu-id="8d872-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="8d872-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8d872-123">在 *ppReaders* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="8d872-123">A bad pointer was passed in *ppReaders*.</span></span><br/> |
| <dl> <span data-ttu-id="8d872-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8d872-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8d872-125">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="8d872-125">Out of memory.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="8d872-126">備註</span><span class="sxs-lookup"><span data-stu-id="8d872-126">Remarks</span></span>

<span data-ttu-id="8d872-127">若要取出所有已知的 [*智慧卡*](../secgloss/s-gly.md) 或 [*讀取器群組*](../secgloss/r-gly.md)，請分別呼叫 [**ListCards**](iscarddatabase-listcards.md) 或 [**ListReaderGroups**](iscarddatabase-listreadergroups.md) 。</span><span class="sxs-lookup"><span data-stu-id="8d872-127">To retrieve all known [*smart cards*](../secgloss/s-gly.md) or [*reader groups*](../secgloss/r-gly.md), call [**ListCards**](iscarddatabase-listcards.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="8d872-128">分別取得 [*主要服務提供者*](../secgloss/p-gly.md) 或特定卡片 [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) 或 [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) 的介面。</span><span class="sxs-lookup"><span data-stu-id="8d872-128">To retrieve the [*primary service provider*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="8d872-129">如需此介面所提供的所有方法清單，請參閱 [**ISCardDatabase**](iscarddatabase.md)。</span><span class="sxs-lookup"><span data-stu-id="8d872-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="8d872-130">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8d872-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8d872-131">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="8d872-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8d872-132">範例</span><span class="sxs-lookup"><span data-stu-id="8d872-132">Examples</span></span>

<span data-ttu-id="8d872-133">下列範例顯示如何抓取智慧卡資料庫中註冊的智慧卡讀取器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d872-133">The following example shows retrieving the names of the smart card readers registered in the smart card database.</span></span>


```C++
LPSAFEARRAY pReaders = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaders(0x0409,  // English (US)
                               &pReaders);
if (FAILED(hr))
{
   printf("Failed ListReaders\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a><span data-ttu-id="8d872-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d872-134">Requirements</span></span>



| <span data-ttu-id="8d872-135">需求</span><span class="sxs-lookup"><span data-stu-id="8d872-135">Requirement</span></span> | <span data-ttu-id="8d872-136">值</span><span class="sxs-lookup"><span data-stu-id="8d872-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d872-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d872-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8d872-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d872-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8d872-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d872-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8d872-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d872-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8d872-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8d872-141">End of client support</span></span><br/>    | <span data-ttu-id="8d872-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8d872-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8d872-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="8d872-143">End of server support</span></span><br/>    | <span data-ttu-id="8d872-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8d872-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8d872-145">標頭</span><span class="sxs-lookup"><span data-stu-id="8d872-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d872-146"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d872-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d872-147">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8d872-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d872-148"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8d872-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8d872-149">DLL</span><span class="sxs-lookup"><span data-stu-id="8d872-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d872-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d872-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8d872-151">IID</span><span class="sxs-lookup"><span data-stu-id="8d872-151">IID</span></span><br/>                      | <span data-ttu-id="8d872-152">IID \_ ISCardDatabase 定義為1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8d872-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8d872-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d872-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d872-154">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="8d872-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="8d872-155">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="8d872-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="8d872-156">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="8d872-156">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="8d872-157">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="8d872-157">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="8d872-158">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="8d872-158">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> </dl>

 

 
