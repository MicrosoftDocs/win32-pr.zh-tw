---
description: UpdateRecord 方法會建立應用程式協定資料單位 (APDU) 命令，此命令會使用 APDU 命令中指定的位來更新特定記錄。
ms.assetid: 66039afd-5d73-41b3-b87b-b5d598c6f3db
title: 'ISCardISO7816：： UpdateRecord 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bf810594e623d58944f58d3b7671664b3be175f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192956"
---
# <a name="iscardiso7816updaterecord-method"></a><span data-ttu-id="ee809-103">ISCardISO7816：： UpdateRecord 方法</span><span class="sxs-lookup"><span data-stu-id="ee809-103">ISCardISO7816::UpdateRecord method</span></span>

<span data-ttu-id="ee809-104">\[**UpdateRecord** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ee809-104">\[The **UpdateRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ee809-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="ee809-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ee809-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ee809-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ee809-107">**UpdateRecord** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會使用 APDU 命令中指定的位來更新特定記錄。</span><span class="sxs-lookup"><span data-stu-id="ee809-107">The **UpdateRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates a specific record with the bits given in the APDU command.</span></span>

> [!Note]  
> <span data-ttu-id="ee809-108">使用目前的記錄定址時，此命令會在已成功更新的記錄上設定記錄指標。</span><span class="sxs-lookup"><span data-stu-id="ee809-108">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ee809-109">語法</span><span class="sxs-lookup"><span data-stu-id="ee809-109">Syntax</span></span>


```C++
HRESULT UpdateRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="ee809-110">參數</span><span class="sxs-lookup"><span data-stu-id="ee809-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee809-111">*byRecordId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee809-111">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee809-112">P1 值：</span><span class="sxs-lookup"><span data-stu-id="ee809-112">P1 value:</span></span>

<span data-ttu-id="ee809-113">P1 = 00 指定目前的記錄</span><span class="sxs-lookup"><span data-stu-id="ee809-113">P1 = 00 designates the current record</span></span>

<span data-ttu-id="ee809-114">P1！ = ' 00 ' 是指定記錄的數目</span><span class="sxs-lookup"><span data-stu-id="ee809-114">P1 != '00' is the number of the specified record</span></span>

</dd> <dt>

<span data-ttu-id="ee809-115">*byRefCtrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee809-115">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee809-116">參考控制項 P2 的編碼：</span><span class="sxs-lookup"><span data-stu-id="ee809-116">Coding of the reference control P2:</span></span>



| <span data-ttu-id="ee809-117">值</span><span class="sxs-lookup"><span data-stu-id="ee809-117">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="ee809-118">意義</span><span class="sxs-lookup"><span data-stu-id="ee809-118">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="ee809-119"><dt>**目前的 EF**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-119"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="ee809-120">位位置： 00000---</span><span class="sxs-lookup"><span data-stu-id="ee809-120">Bit position: 00000---</span></span><br/> <span data-ttu-id="ee809-121">目前選取的 EF。</span><span class="sxs-lookup"><span data-stu-id="ee809-121">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="ee809-122"><dt>**簡短 EF 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-122"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="ee809-123">位位置： xxxxx---</span><span class="sxs-lookup"><span data-stu-id="ee809-123">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="ee809-124">簡短 EF 識別碼。</span><span class="sxs-lookup"><span data-stu-id="ee809-124">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="ee809-125"><dt>**第一筆記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-125"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="ee809-126">位位置：-----000</span><span class="sxs-lookup"><span data-stu-id="ee809-126">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="ee809-127"><dt>**最後一筆記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-127"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="ee809-128">位位置：-----001</span><span class="sxs-lookup"><span data-stu-id="ee809-128">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="ee809-129"><dt>**下一筆記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-129"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="ee809-130">位位置：-----010</span><span class="sxs-lookup"><span data-stu-id="ee809-130">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="ee809-131"><dt>**上一筆記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-131"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="ee809-132">位位置：-----011</span><span class="sxs-lookup"><span data-stu-id="ee809-132">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="ee809-133"><dt>**\#P1 中的記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-133"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="ee809-134">位位置：-----100</span><span class="sxs-lookup"><span data-stu-id="ee809-134">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="ee809-135">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee809-135">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee809-136">要更新之記錄的指標。</span><span class="sxs-lookup"><span data-stu-id="ee809-136">Pointer to the record to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="ee809-137">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ee809-137">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee809-138">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ee809-138">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="ee809-139">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="ee809-139">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="ee809-140">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並透過 *ppCmd* 指標傳回。</span><span class="sxs-lookup"><span data-stu-id="ee809-140">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee809-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee809-141">Return value</span></span>

<span data-ttu-id="ee809-142">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="ee809-142">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ee809-143">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ee809-143">Return code</span></span>                                                                                   | <span data-ttu-id="ee809-144">Description</span><span class="sxs-lookup"><span data-stu-id="ee809-144">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ee809-145"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-145"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ee809-146">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="ee809-146">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="ee809-147"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-147"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ee809-148">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="ee809-148">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="ee809-149"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-149"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ee809-150">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="ee809-150">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="ee809-151"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-151"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ee809-152">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="ee809-152">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="ee809-153">備註</span><span class="sxs-lookup"><span data-stu-id="ee809-153">Remarks</span></span>

<span data-ttu-id="ee809-154">只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所處理之基本檔案的安全性屬性時，才能執行封裝的命令。</span><span class="sxs-lookup"><span data-stu-id="ee809-154">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="ee809-155">當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="ee809-155">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="ee809-156">如果在發出此命令時，目前選取了另一個基本檔案，則可能會處理此命令，而不需要識別目前選取的檔案。</span><span class="sxs-lookup"><span data-stu-id="ee809-156">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="ee809-157">如果建立的命令套用至線性固定或迴圈結構化的基本檔案，則如果記錄長度與現有記錄的長度不同，則會中止。</span><span class="sxs-lookup"><span data-stu-id="ee809-157">If the constructed command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="ee809-158">如果命令套用至線性變數結構化的基本檔案，則當記錄長度與現有記錄的長度不同時，可能會執行此命令。</span><span class="sxs-lookup"><span data-stu-id="ee809-158">If the command applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="ee809-159">命令的 "previous" 選項 (P2 = xxxxx011) ，套用至迴圈檔案，其行為與 [**AppendRecord**](iscardiso7816-appendrecord.md)所建立的命令相同。</span><span class="sxs-lookup"><span data-stu-id="ee809-159">The "previous" option of the command (P2=xxxxx011), applied to a cyclic file, has the same behavior as a command constructed by [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="ee809-160">無法讀取沒有記錄結構的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="ee809-160">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="ee809-161">如果套用至不含記錄結構的基本檔案，則會中止已建立的命令。</span><span class="sxs-lookup"><span data-stu-id="ee809-161">The constructed command aborts if applied to an elementary file without record structure.</span></span>

<span data-ttu-id="ee809-162">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="ee809-162">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="ee809-163">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ee809-163">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ee809-164">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="ee809-164">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee809-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee809-165">Requirements</span></span>



| <span data-ttu-id="ee809-166">需求</span><span class="sxs-lookup"><span data-stu-id="ee809-166">Requirement</span></span> | <span data-ttu-id="ee809-167">值</span><span class="sxs-lookup"><span data-stu-id="ee809-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee809-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee809-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ee809-169">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee809-169">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ee809-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee809-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ee809-171">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee809-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee809-172">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ee809-172">End of client support</span></span><br/>    | <span data-ttu-id="ee809-173">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ee809-173">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ee809-174">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ee809-174">End of server support</span></span><br/>    | <span data-ttu-id="ee809-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee809-175">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ee809-176">標頭</span><span class="sxs-lookup"><span data-stu-id="ee809-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee809-177"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-177"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee809-178">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ee809-178">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee809-179"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-179"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ee809-180">DLL</span><span class="sxs-lookup"><span data-stu-id="ee809-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee809-181"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee809-181"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ee809-182">IID</span><span class="sxs-lookup"><span data-stu-id="ee809-182">IID</span></span><br/>                      | <span data-ttu-id="ee809-183">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ee809-183">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ee809-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee809-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee809-185">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="ee809-185">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="ee809-186">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="ee809-186">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="ee809-187">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="ee809-187">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="ee809-188">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="ee809-188">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
