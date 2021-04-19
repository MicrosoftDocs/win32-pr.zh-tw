---
description: 抓取智慧卡的 ATR 字串。
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: 'ISCard：： get_Atr 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979326"
---
# <a name="iscardget_atr-method"></a><span data-ttu-id="1cba5-103">ISCard：： get \_ Atr 方法</span><span class="sxs-lookup"><span data-stu-id="1cba5-103">ISCard::get\_Atr method</span></span>

<span data-ttu-id="1cba5-104">\[**Get \_ Atr** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1cba5-104">\[The **get\_Atr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1cba5-105">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="1cba5-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1cba5-106">**Get \_ Atr** 方法會抓取 [*智慧卡*](../secgloss/s-gly.md)的 [*Atr 字串*](../secgloss/a-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="1cba5-106">The **get\_Atr** method retrieves an [*ATR string*](../secgloss/a-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cba5-107">語法</span><span class="sxs-lookup"><span data-stu-id="1cba5-107">Syntax</span></span>


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a><span data-ttu-id="1cba5-108">參數</span><span class="sxs-lookup"><span data-stu-id="1cba5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cba5-109">*ppAtr* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1cba5-109">*ppAtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cba5-110">以 [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) 形式的位元組緩衝區指標，會在傳回時包含 ATR 字串。</span><span class="sxs-lookup"><span data-stu-id="1cba5-110">Pointer to a byte buffer in the form of an [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) that will contain the ATR string on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cba5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1cba5-111">Return value</span></span>

<span data-ttu-id="1cba5-112">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="1cba5-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1cba5-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1cba5-113">Return code</span></span>                                                                                   | <span data-ttu-id="1cba5-114">Description</span><span class="sxs-lookup"><span data-stu-id="1cba5-114">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="1cba5-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1cba5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1cba5-116">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="1cba5-116">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="1cba5-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1cba5-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1cba5-118">*PpAtr* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="1cba5-118">The *ppAtr* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="1cba5-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="1cba5-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1cba5-120">在 *ppAtr* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="1cba5-120">A bad pointer was passed in *ppAtr*.</span></span><br/>          |
| <dl> <span data-ttu-id="1cba5-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1cba5-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1cba5-122">無法取得滿足要求的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1cba5-122">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1cba5-123">備註</span><span class="sxs-lookup"><span data-stu-id="1cba5-123">Remarks</span></span>

<span data-ttu-id="1cba5-124">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1cba5-124">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1cba5-125">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="1cba5-125">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1cba5-126">範例</span><span class="sxs-lookup"><span data-stu-id="1cba5-126">Examples</span></span>

<span data-ttu-id="1cba5-127">下列範例顯示從智慧卡取出 ATR 字串。</span><span class="sxs-lookup"><span data-stu-id="1cba5-127">The following example shows retrieving the ATR string from the smart card.</span></span>


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="1cba5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="1cba5-128">Requirements</span></span>



| <span data-ttu-id="1cba5-129">需求</span><span class="sxs-lookup"><span data-stu-id="1cba5-129">Requirement</span></span> | <span data-ttu-id="1cba5-130">值</span><span class="sxs-lookup"><span data-stu-id="1cba5-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cba5-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1cba5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1cba5-132">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cba5-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1cba5-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1cba5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1cba5-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1cba5-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1cba5-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1cba5-135">End of client support</span></span><br/>    | <span data-ttu-id="1cba5-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1cba5-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1cba5-137">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1cba5-137">End of server support</span></span><br/>    | <span data-ttu-id="1cba5-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1cba5-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1cba5-139">標頭</span><span class="sxs-lookup"><span data-stu-id="1cba5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cba5-140"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="1cba5-140"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="1cba5-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1cba5-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="1cba5-142"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1cba5-142"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1cba5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="1cba5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cba5-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cba5-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1cba5-145">IID</span><span class="sxs-lookup"><span data-stu-id="1cba5-145">IID</span></span><br/>                      | <span data-ttu-id="1cba5-146">IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1cba5-146">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="1cba5-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1cba5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cba5-148">**取得 \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="1cba5-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="1cba5-149">**取得 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="1cba5-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="1cba5-150">**取得 \_ 通訊協定**</span><span class="sxs-lookup"><span data-stu-id="1cba5-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="1cba5-151">**取得 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="1cba5-151">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="1cba5-152">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="1cba5-152">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="1cba5-153">**IByteBuffer：： Read**</span><span class="sxs-lookup"><span data-stu-id="1cba5-153">**IByteBuffer::Read**</span></span>](ibytebuffer-read.md)
</dt> </dl>

 

 
