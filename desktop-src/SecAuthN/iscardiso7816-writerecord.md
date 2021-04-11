---
description: 建立會起始其中一個所列出作業的 APDU 命令。
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: 'ISCardISO7816：： WriteRecord 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 30bfdb9ff8779633d81da89bbf7ac8e69a617d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112176"
---
# <a name="iscardiso7816writerecord-method"></a><span data-ttu-id="801ca-103">ISCardISO7816：： WriteRecord 方法</span><span class="sxs-lookup"><span data-stu-id="801ca-103">ISCardISO7816::WriteRecord method</span></span>

<span data-ttu-id="801ca-104">\[**WriteRecord** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="801ca-104">\[The **WriteRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="801ca-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="801ca-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="801ca-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="801ca-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="801ca-107">**WriteRecord** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會起始下列其中一項作業：</span><span class="sxs-lookup"><span data-stu-id="801ca-107">The **WriteRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates one of the following operations:</span></span>

-   <span data-ttu-id="801ca-108">記錄的寫入一次。</span><span class="sxs-lookup"><span data-stu-id="801ca-108">The write once of a record.</span></span>
-   <span data-ttu-id="801ca-109">卡片中已有記錄資料位元組的邏輯 **OR** ，內含命令 APDU 中提供的記錄資料位元組。</span><span class="sxs-lookup"><span data-stu-id="801ca-109">The logical **OR** of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>
-   <span data-ttu-id="801ca-110">卡片中已有記錄資料位元組的邏輯 AND，其中包含命令 APDU 中提供的記錄資料位元組。</span><span class="sxs-lookup"><span data-stu-id="801ca-110">The logical AND of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>

<span data-ttu-id="801ca-111">如果資料編碼位元組中未提供任何指示，則會套用邏輯 OR 行為。</span><span class="sxs-lookup"><span data-stu-id="801ca-111">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

> [!Note]  
> <span data-ttu-id="801ca-112">使用目前的記錄定址時，此命令會在已成功更新的記錄上設定記錄指標。</span><span class="sxs-lookup"><span data-stu-id="801ca-112">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="801ca-113">語法</span><span class="sxs-lookup"><span data-stu-id="801ca-113">Syntax</span></span>


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="801ca-114">參數</span><span class="sxs-lookup"><span data-stu-id="801ca-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="801ca-115">*byRecordId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="801ca-115">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801ca-116">記錄識別。</span><span class="sxs-lookup"><span data-stu-id="801ca-116">Record identification.</span></span> <span data-ttu-id="801ca-117">這是 P1 值：</span><span class="sxs-lookup"><span data-stu-id="801ca-117">This is the P1 value:</span></span>

<span data-ttu-id="801ca-118">P1 = ' 00 ' 會指定目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="801ca-118">P1 = '00' designates the current record.</span></span>

<span data-ttu-id="801ca-119">P1！ = ' 00 ' 是指定之記錄的編號。</span><span class="sxs-lookup"><span data-stu-id="801ca-119">P1 != '00' is the number of the specified record.</span></span>

</dd> <dt>

<span data-ttu-id="801ca-120">*byRefCtrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="801ca-120">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801ca-121">參考控制項 P2 的編碼。</span><span class="sxs-lookup"><span data-stu-id="801ca-121">Coding of the reference control P2.</span></span>



| <span data-ttu-id="801ca-122">值</span><span class="sxs-lookup"><span data-stu-id="801ca-122">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="801ca-123">意義</span><span class="sxs-lookup"><span data-stu-id="801ca-123">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="801ca-124"><dt>**目前的 EF**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-124"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="801ca-125">位位置： 00000---</span><span class="sxs-lookup"><span data-stu-id="801ca-125">Bit position: 00000---</span></span><br/> <span data-ttu-id="801ca-126">目前選取的 EF。</span><span class="sxs-lookup"><span data-stu-id="801ca-126">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="801ca-127"><dt>**簡短 EF 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-127"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="801ca-128">位位置： xxxxx---</span><span class="sxs-lookup"><span data-stu-id="801ca-128">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="801ca-129">簡短 EF 識別碼。</span><span class="sxs-lookup"><span data-stu-id="801ca-129">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="801ca-130"><dt>**第一筆記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-130"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="801ca-131">位位置：-----000</span><span class="sxs-lookup"><span data-stu-id="801ca-131">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="801ca-132"><dt>**最後一筆記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-132"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="801ca-133">位位置：-----001</span><span class="sxs-lookup"><span data-stu-id="801ca-133">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="801ca-134"><dt>**下一筆記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-134"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="801ca-135">位位置：-----010</span><span class="sxs-lookup"><span data-stu-id="801ca-135">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="801ca-136"><dt>**上一筆記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-136"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="801ca-137">位位置：-----011</span><span class="sxs-lookup"><span data-stu-id="801ca-137">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="801ca-138"><dt>**\#P1 中的記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-138"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="801ca-139">位位置：-----100</span><span class="sxs-lookup"><span data-stu-id="801ca-139">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="801ca-140">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="801ca-140">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801ca-141">要寫入之記錄的指標。</span><span class="sxs-lookup"><span data-stu-id="801ca-141">Pointer to the record to be written.</span></span>

</dd> <dt>

<span data-ttu-id="801ca-142">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="801ca-142">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="801ca-143">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="801ca-143">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="801ca-144">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="801ca-144">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="801ca-145">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並透過 *ppCmd* 指標傳回。</span><span class="sxs-lookup"><span data-stu-id="801ca-145">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="801ca-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="801ca-146">Return value</span></span>

<span data-ttu-id="801ca-147">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="801ca-147">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="801ca-148">傳回碼</span><span class="sxs-lookup"><span data-stu-id="801ca-148">Return code</span></span>                                                                                   | <span data-ttu-id="801ca-149">Description</span><span class="sxs-lookup"><span data-stu-id="801ca-149">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="801ca-150"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-150"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="801ca-151">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="801ca-151">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="801ca-152"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-152"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="801ca-153">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="801ca-153">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="801ca-154"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-154"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="801ca-155">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="801ca-155">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="801ca-156"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-156"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="801ca-157">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="801ca-157">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="801ca-158">備註</span><span class="sxs-lookup"><span data-stu-id="801ca-158">Remarks</span></span>

<span data-ttu-id="801ca-159">只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所處理之基本檔案的安全性屬性時，才能執行封裝的命令。</span><span class="sxs-lookup"><span data-stu-id="801ca-159">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="801ca-160">當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="801ca-160">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="801ca-161">如果在發出此命令時，目前選取了另一個基本檔案，則可能會處理此命令，而不需要識別目前選取的檔案。</span><span class="sxs-lookup"><span data-stu-id="801ca-161">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="801ca-162">如果封裝的命令套用至線性固定或迴圈結構化的基本檔案，則如果記錄長度與現有記錄的長度不同，則會中止。</span><span class="sxs-lookup"><span data-stu-id="801ca-162">If the encapsulated command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span> <span data-ttu-id="801ca-163">如果它套用至線性變數結構化的基本檔案，則可能會在記錄長度與現有記錄的長度不同時執行。</span><span class="sxs-lookup"><span data-stu-id="801ca-163">If it applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="801ca-164">如果 P2 = xxxxx011 且基本檔案是迴圈檔案，則此命令的行為會與使用 [**AppendRecord**](iscardiso7816-appendrecord.md)所建立的命令相同。</span><span class="sxs-lookup"><span data-stu-id="801ca-164">If P2=xxxxx011 and the elementary file is cyclic file, this command has the same behavior a command constructed using [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="801ca-165">無法寫入沒有記錄結構的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="801ca-165">Elementary files without a record structure cannot be written to.</span></span> <span data-ttu-id="801ca-166">如果套用至不含記錄結構的基本檔，則會中止已建立的命令。</span><span class="sxs-lookup"><span data-stu-id="801ca-166">The constructed command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="801ca-167">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="801ca-167">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="801ca-168">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="801ca-168">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="801ca-169">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="801ca-169">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="801ca-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="801ca-170">Requirements</span></span>



| <span data-ttu-id="801ca-171">需求</span><span class="sxs-lookup"><span data-stu-id="801ca-171">Requirement</span></span> | <span data-ttu-id="801ca-172">值</span><span class="sxs-lookup"><span data-stu-id="801ca-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="801ca-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="801ca-173">Minimum supported client</span></span><br/> | <span data-ttu-id="801ca-174">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="801ca-174">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="801ca-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="801ca-175">Minimum supported server</span></span><br/> | <span data-ttu-id="801ca-176">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="801ca-176">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="801ca-177">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="801ca-177">End of client support</span></span><br/>    | <span data-ttu-id="801ca-178">Windows XP</span><span class="sxs-lookup"><span data-stu-id="801ca-178">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="801ca-179">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="801ca-179">End of server support</span></span><br/>    | <span data-ttu-id="801ca-180">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="801ca-180">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="801ca-181">標頭</span><span class="sxs-lookup"><span data-stu-id="801ca-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="801ca-182"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-182"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="801ca-183">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="801ca-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="801ca-184"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-184"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="801ca-185">DLL</span><span class="sxs-lookup"><span data-stu-id="801ca-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="801ca-186"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="801ca-186"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="801ca-187">IID</span><span class="sxs-lookup"><span data-stu-id="801ca-187">IID</span></span><br/>                      | <span data-ttu-id="801ca-188">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="801ca-188">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="801ca-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="801ca-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="801ca-190">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="801ca-190">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="801ca-191">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="801ca-191">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="801ca-192">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="801ca-192">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="801ca-193">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="801ca-193">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
