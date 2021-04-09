---
description: 使用的方法會將應用程式協定資料單位 (APDU) 命令，以根據所選取的檔案類型，抓取單一基本資料物件或 (包含在結構化) 資料物件中的一組資料物件。
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: 'ISCardISO7816：： Scardssp 方法 (.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 93dca04daa50e068a68dc62cf11a580eb8e3b1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694039"
---
# <a name="iscardiso7816getdata-method"></a><span data-ttu-id="dee21-103">ISCardISO7816：：：：的方法</span><span class="sxs-lookup"><span data-stu-id="dee21-103">ISCardISO7816::GetData method</span></span>

<span data-ttu-id="dee21-104">\[您可以在 [需求] 區段中指定的作業系統中使用 [ **操作方法]** 。</span><span class="sxs-lookup"><span data-stu-id="dee21-104">\[The **GetData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dee21-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="dee21-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dee21-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="dee21-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dee21-107">使用 **的** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，以根據所選取的檔案類型，抓取單一基本資料物件或 (包含在結構化) 資料物件中的一組資料物件。</span><span class="sxs-lookup"><span data-stu-id="dee21-107">The **GetData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that retrieves either a single primitive data object or a set of data objects (contained in a constructed data object), depending on the type of file selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee21-108">語法</span><span class="sxs-lookup"><span data-stu-id="dee21-108">Syntax</span></span>


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="dee21-109">參數</span><span class="sxs-lookup"><span data-stu-id="dee21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dee21-110">*byP1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dee21-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee21-111">參數。</span><span class="sxs-lookup"><span data-stu-id="dee21-111">Parameters.</span></span>



| <span data-ttu-id="dee21-112">值</span><span class="sxs-lookup"><span data-stu-id="dee21-112">Value</span></span>                                                                                  | <span data-ttu-id="dee21-113">意義</span><span class="sxs-lookup"><span data-stu-id="dee21-113">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="dee21-114"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-114"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="dee21-115">RFU</span><span class="sxs-lookup"><span data-stu-id="dee21-115">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="dee21-116"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-116"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="dee21-117">BER-TLV 標記 (1 位元組) 在 P2 中</span><span class="sxs-lookup"><span data-stu-id="dee21-117">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="dee21-118"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-118"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="dee21-119">應用程式資料 (專屬編碼) </span><span class="sxs-lookup"><span data-stu-id="dee21-119">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="dee21-120"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-120"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="dee21-121">P2 中的簡單 TLV 標記</span><span class="sxs-lookup"><span data-stu-id="dee21-121">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="dee21-122"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-122"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="dee21-123">RFU</span><span class="sxs-lookup"><span data-stu-id="dee21-123">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="dee21-124"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-124"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="dee21-125">BER-TLV 標記 (2 個位元組) 在 P1-P2 中</span><span class="sxs-lookup"><span data-stu-id="dee21-125">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="dee21-126">*byP2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dee21-126">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee21-127">參數。</span><span class="sxs-lookup"><span data-stu-id="dee21-127">Parameters.</span></span>



| <span data-ttu-id="dee21-128">值</span><span class="sxs-lookup"><span data-stu-id="dee21-128">Value</span></span>                                                                                  | <span data-ttu-id="dee21-129">意義</span><span class="sxs-lookup"><span data-stu-id="dee21-129">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="dee21-130"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-130"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="dee21-131">RFU</span><span class="sxs-lookup"><span data-stu-id="dee21-131">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="dee21-132"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-132"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="dee21-133">BER-TLV 標記 (1 位元組) 在 P2 中</span><span class="sxs-lookup"><span data-stu-id="dee21-133">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="dee21-134"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-134"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="dee21-135">應用程式資料 (專屬編碼) </span><span class="sxs-lookup"><span data-stu-id="dee21-135">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="dee21-136"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-136"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="dee21-137">P2 中的簡單 TLV 標記</span><span class="sxs-lookup"><span data-stu-id="dee21-137">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="dee21-138"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-138"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="dee21-139">RFU</span><span class="sxs-lookup"><span data-stu-id="dee21-139">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="dee21-140"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-140"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="dee21-141">BER-TLV 標記 (2 個位元組) 在 P1-P2 中</span><span class="sxs-lookup"><span data-stu-id="dee21-141">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="dee21-142">*lBytesToGet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dee21-142">*lBytesToGet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee21-143">回應中預期的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="dee21-143">Number of bytes expected in the response.</span></span>

</dd> <dt>

<span data-ttu-id="dee21-144">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="dee21-144">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dee21-145">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="dee21-145">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="dee21-146">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="dee21-146">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="dee21-147">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並使用 *ppCmd* 指標來傳回。</span><span class="sxs-lookup"><span data-stu-id="dee21-147">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dee21-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="dee21-148">Return value</span></span>

<span data-ttu-id="dee21-149">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="dee21-149">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="dee21-150">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dee21-150">Return code</span></span>                                                                                   | <span data-ttu-id="dee21-151">Description</span><span class="sxs-lookup"><span data-stu-id="dee21-151">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dee21-152"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-152"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dee21-153">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="dee21-153">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="dee21-154"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-154"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dee21-155">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="dee21-155">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="dee21-156"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-156"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dee21-157">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="dee21-157">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="dee21-158"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-158"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dee21-159">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="dee21-159">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="dee21-160">備註</span><span class="sxs-lookup"><span data-stu-id="dee21-160">Remarks</span></span>

<span data-ttu-id="dee21-161">只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所讀取之基本檔案的安全性屬性時，才能執行封裝的命令。</span><span class="sxs-lookup"><span data-stu-id="dee21-161">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span> <span data-ttu-id="dee21-162">安全性條件取決於卡片的原則，並可透過 [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)、 [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)、 [**ISCardAuth**](iscardauth.md)等操作。</span><span class="sxs-lookup"><span data-stu-id="dee21-162">Security conditions are dependent on the policy of the card, and may be manipulated through [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md), and so on.</span></span>

<span data-ttu-id="dee21-163">若要選取檔案，請呼叫 [**SelectFile**](iscardiso7816-selectfile.md)。</span><span class="sxs-lookup"><span data-stu-id="dee21-163">To select a file, call [**SelectFile**](iscardiso7816-selectfile.md).</span></span>

<span data-ttu-id="dee21-164">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="dee21-164">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="dee21-165">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dee21-165">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="dee21-166">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="dee21-166">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dee21-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="dee21-167">Requirements</span></span>



| <span data-ttu-id="dee21-168">需求</span><span class="sxs-lookup"><span data-stu-id="dee21-168">Requirement</span></span> | <span data-ttu-id="dee21-169">值</span><span class="sxs-lookup"><span data-stu-id="dee21-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dee21-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dee21-170">Minimum supported client</span></span><br/> | <span data-ttu-id="dee21-171">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dee21-171">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dee21-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dee21-172">Minimum supported server</span></span><br/> | <span data-ttu-id="dee21-173">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dee21-173">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dee21-174">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="dee21-174">End of client support</span></span><br/>    | <span data-ttu-id="dee21-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dee21-175">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dee21-176">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="dee21-176">End of server support</span></span><br/>    | <span data-ttu-id="dee21-177">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dee21-177">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dee21-178">標頭</span><span class="sxs-lookup"><span data-stu-id="dee21-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="dee21-179"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-179"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dee21-180">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="dee21-180">Type library</span></span><br/>             | <dl> <span data-ttu-id="dee21-181"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-181"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dee21-182">DLL</span><span class="sxs-lookup"><span data-stu-id="dee21-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dee21-183"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dee21-183"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dee21-184">IID</span><span class="sxs-lookup"><span data-stu-id="dee21-184">IID</span></span><br/>                      | <span data-ttu-id="dee21-185">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="dee21-185">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="dee21-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dee21-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee21-187">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="dee21-187">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="dee21-188">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="dee21-188">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="dee21-189">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="dee21-189">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="dee21-190">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="dee21-190">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="dee21-191">**PutData**</span><span class="sxs-lookup"><span data-stu-id="dee21-191">**PutData**</span></span>](iscardiso7816-putdata.md)
</dt> <dt>

[<span data-ttu-id="dee21-192">**SelectFile**</span><span class="sxs-lookup"><span data-stu-id="dee21-192">**SelectFile**</span></span>](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
