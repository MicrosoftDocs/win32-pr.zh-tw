---
description: 從應用程式協定資料單位抓取資料欄位 (APDU) ，將其放在位元組緩衝區物件中。
ms.assetid: fbffeeeb-56e5-4484-b294-8b6f59c919eb
title: 'ISCardCmd：： get_Data 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb6a8c28316bd4fd08160063606d3e15054fd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514141"
---
# <a name="iscardcmdget_data-method"></a><span data-ttu-id="72773-103">ISCardCmd：： get \_ Data 方法</span><span class="sxs-lookup"><span data-stu-id="72773-103">ISCardCmd::get\_Data method</span></span>

<span data-ttu-id="72773-104">\[**取得 \_ 資料** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="72773-104">\[The **get\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="72773-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="72773-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="72773-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="72773-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="72773-107">**Get \_ Data** 方法會從 [*應用程式協定資料單位*](../secgloss/a-gly.md)中抓取資料欄位， (APDU) ，將它放在位元組緩衝區物件中。</span><span class="sxs-lookup"><span data-stu-id="72773-107">The **get\_Data** method retrieves the data field from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU), placing it in a byte buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="72773-108">語法</span><span class="sxs-lookup"><span data-stu-id="72773-108">Syntax</span></span>


```C++
HRESULT get_Data(
  [out] LPBYTEBUFFER *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="72773-109">參數</span><span class="sxs-lookup"><span data-stu-id="72773-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72773-110">*ppData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="72773-110">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72773-111">位元組緩衝區物件的指標 (會在傳回時保存 APDU 資料欄位的 **IStream**) 。</span><span class="sxs-lookup"><span data-stu-id="72773-111">Pointer to the byte buffer object (**IStream**) that holds the APDU data field on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72773-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="72773-112">Return value</span></span>

<span data-ttu-id="72773-113">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="72773-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="72773-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="72773-114">Return code</span></span>                                                                                   | <span data-ttu-id="72773-115">Description</span><span class="sxs-lookup"><span data-stu-id="72773-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="72773-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="72773-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="72773-117">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="72773-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="72773-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="72773-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="72773-119">*PpData* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="72773-119">The *ppData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="72773-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="72773-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="72773-121">在 *ppData* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="72773-121">A bad pointer was passed in *ppData*.</span></span><br/> |
| <dl> <span data-ttu-id="72773-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="72773-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="72773-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="72773-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="72773-124">備註</span><span class="sxs-lookup"><span data-stu-id="72773-124">Remarks</span></span>

<span data-ttu-id="72773-125">若要設定 APDU 的資料欄位，請呼叫 [**put \_ 資料**](iscardcmd-put-data.md)。</span><span class="sxs-lookup"><span data-stu-id="72773-125">To set the data field of the APDU, call [**put\_Data**](iscardcmd-put-data.md).</span></span>

<span data-ttu-id="72773-126">如需此介面所提供的所有方法清單，請參閱 [**ISCardCmd**](iscardcmd.md)。</span><span class="sxs-lookup"><span data-stu-id="72773-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="72773-127">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="72773-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="72773-128">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="72773-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="72773-129">範例</span><span class="sxs-lookup"><span data-stu-id="72773-129">Examples</span></span>

<span data-ttu-id="72773-130">下列範例示範如何取出 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 的資料欄位。</span><span class="sxs-lookup"><span data-stu-id="72773-130">The following example shows how to retrieve the data field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="72773-131">此範例假設 pIByteData 是 [**IByteBuffer**](ibytebuffer.md) 介面實例的有效指標，而且該 PISCardCmd 是 [**ISCardCmd**](iscardcmd.md) 介面實例的有效指標。</span><span class="sxs-lookup"><span data-stu-id="72773-131">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Retrieve the data.
hr = pISCardCmd->get_Data(&pIByteData);
if (FAILED(hr)) 
{
    printf("Failed get_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="72773-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="72773-132">Requirements</span></span>



| <span data-ttu-id="72773-133">需求</span><span class="sxs-lookup"><span data-stu-id="72773-133">Requirement</span></span> | <span data-ttu-id="72773-134">值</span><span class="sxs-lookup"><span data-stu-id="72773-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72773-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72773-135">Minimum supported client</span></span><br/> | <span data-ttu-id="72773-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72773-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72773-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72773-137">Minimum supported server</span></span><br/> | <span data-ttu-id="72773-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72773-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72773-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="72773-139">End of client support</span></span><br/>    | <span data-ttu-id="72773-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="72773-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="72773-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="72773-141">End of server support</span></span><br/>    | <span data-ttu-id="72773-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72773-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="72773-143">標頭</span><span class="sxs-lookup"><span data-stu-id="72773-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="72773-144"><dt>Scarddat。h</dt></span><span class="sxs-lookup"><span data-stu-id="72773-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="72773-145">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="72773-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="72773-146"><dt>Scarddat .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72773-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72773-147">DLL</span><span class="sxs-lookup"><span data-stu-id="72773-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72773-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72773-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="72773-149">IID</span><span class="sxs-lookup"><span data-stu-id="72773-149">IID</span></span><br/>                      | <span data-ttu-id="72773-150">IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="72773-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="72773-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72773-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72773-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="72773-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="72773-153">**放置 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="72773-153">**put\_Data**</span></span>](iscardcmd-put-data.md)
</dt> </dl>

 

 
