---
description: ReadRecord 方法會建立應用程式協定資料單位 (APDU) 命令，以讀取指定記錄的內容或基本檔案的一筆記錄的開頭部分。
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'ISCardISO7816：： ReadRecord 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026712"
---
# <a name="iscardiso7816readrecord-method"></a><span data-ttu-id="a61f0-103">ISCardISO7816：： ReadRecord 方法</span><span class="sxs-lookup"><span data-stu-id="a61f0-103">ISCardISO7816::ReadRecord method</span></span>

<span data-ttu-id="a61f0-104">\[**ReadRecord** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a61f0-104">\[The **ReadRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a61f0-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="a61f0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a61f0-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="a61f0-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a61f0-107">**ReadRecord** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，以讀取指定記錄的內容或基本檔案的一筆記錄的開頭部分。</span><span class="sxs-lookup"><span data-stu-id="a61f0-107">The **ReadRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that reads either the contents of the specified records or the beginning part of one record of an elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a61f0-108">語法</span><span class="sxs-lookup"><span data-stu-id="a61f0-108">Syntax</span></span>


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a61f0-109">參數</span><span class="sxs-lookup"><span data-stu-id="a61f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a61f0-110">*byRecordId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a61f0-110">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a61f0-111">要讀取之第一筆記錄的記錄號碼或識別碼 (00 表示目前的記錄) 。</span><span class="sxs-lookup"><span data-stu-id="a61f0-111">Record number or ID of the first record to be read (00 indicates the current record).</span></span>

</dd> <dt>

<span data-ttu-id="a61f0-112">*byRefCtrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a61f0-112">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a61f0-113">參考控制項的編碼。</span><span class="sxs-lookup"><span data-stu-id="a61f0-113">Coding of the reference control.</span></span>



| <span data-ttu-id="a61f0-114">值</span><span class="sxs-lookup"><span data-stu-id="a61f0-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="a61f0-115">意義</span><span class="sxs-lookup"><span data-stu-id="a61f0-115">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="a61f0-116"><dt>**目前的 EF**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-116"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="a61f0-117">位位置： 00000---</span><span class="sxs-lookup"><span data-stu-id="a61f0-117">Bit position: 00000---</span></span><br/> <span data-ttu-id="a61f0-118">目前選取的 EF。</span><span class="sxs-lookup"><span data-stu-id="a61f0-118">Currently selected EF.</span></span><br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="a61f0-119"><dt>**簡短 EF 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-119"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="a61f0-120">位位置： xxxxx---</span><span class="sxs-lookup"><span data-stu-id="a61f0-120">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="a61f0-121">簡短 EF 識別碼。</span><span class="sxs-lookup"><span data-stu-id="a61f0-121">Short EF identifier.</span></span><br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="a61f0-122"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-122"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="a61f0-123">位位置： 11111---</span><span class="sxs-lookup"><span data-stu-id="a61f0-123">Bit position: 11111---</span></span><br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <span data-ttu-id="a61f0-124"><dt>**記錄 \#**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-124"><dt>**Record \#**</dt></span></span> </dl>            | <span data-ttu-id="a61f0-125">位位置：-----1xx</span><span class="sxs-lookup"><span data-stu-id="a61f0-125">Bit position: -----1xx</span></span><br/> <span data-ttu-id="a61f0-126">P1 中記錄號碼的使用量。</span><span class="sxs-lookup"><span data-stu-id="a61f0-126">Usage of record number in P1.</span></span><br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <span data-ttu-id="a61f0-127"><dt>**讀取記錄**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-127"><dt>**Read Record**</dt></span></span> </dl> | <span data-ttu-id="a61f0-128">位位置：-----100</span><span class="sxs-lookup"><span data-stu-id="a61f0-128">Bit position: -----100</span></span><br/> <span data-ttu-id="a61f0-129">讀取記錄 P1。</span><span class="sxs-lookup"><span data-stu-id="a61f0-129">Read record P1.</span></span><br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <span data-ttu-id="a61f0-130"><dt>**最高到最後**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-130"><dt>**Up to Last**</dt></span></span> </dl>     | <span data-ttu-id="a61f0-131">位位置：-----101</span><span class="sxs-lookup"><span data-stu-id="a61f0-131">Bit position: -----101</span></span><br/> <span data-ttu-id="a61f0-132">從 P1 讀取所有記錄到最後一個。</span><span class="sxs-lookup"><span data-stu-id="a61f0-132">Read all records from P1 up to the last.</span></span> <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <span data-ttu-id="a61f0-133"><dt>**最多 P1**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-133"><dt>**Up to P1**</dt></span></span> </dl>             | <span data-ttu-id="a61f0-134">位位置：-----110</span><span class="sxs-lookup"><span data-stu-id="a61f0-134">Bit position: -----110</span></span><br/> <span data-ttu-id="a61f0-135">讀取從最多到 P1 的所有記錄。</span><span class="sxs-lookup"><span data-stu-id="a61f0-135">Read all records from the last up to P1.</span></span> <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="a61f0-136"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-136"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="a61f0-137">位位置：-----111</span><span class="sxs-lookup"><span data-stu-id="a61f0-137">Bit position: -----111</span></span><br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <span data-ttu-id="a61f0-138"><dt>**記錄識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-138"><dt>**Record ID**</dt></span></span> </dl>         | <span data-ttu-id="a61f0-139">位位置：-----0xx</span><span class="sxs-lookup"><span data-stu-id="a61f0-139">Bit position: -----0xx</span></span><br/> <span data-ttu-id="a61f0-140">P1 中記錄號碼的使用量。</span><span class="sxs-lookup"><span data-stu-id="a61f0-140">Usage of record number in P1.</span></span><br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <span data-ttu-id="a61f0-141"><dt>**第一次發生**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-141"><dt>**First Occur**</dt></span></span> </dl> | <span data-ttu-id="a61f0-142">位位置：-----000</span><span class="sxs-lookup"><span data-stu-id="a61f0-142">Bit position: -----000</span></span><br/> <span data-ttu-id="a61f0-143">讀取首次發生。</span><span class="sxs-lookup"><span data-stu-id="a61f0-143">Read first occurrence.</span></span> <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <span data-ttu-id="a61f0-144"><dt>**上次發生時間**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-144"><dt>**Last Occur**</dt></span></span> </dl>     | <span data-ttu-id="a61f0-145">位位置：-----001</span><span class="sxs-lookup"><span data-stu-id="a61f0-145">Bit position: -----001</span></span><br/> <span data-ttu-id="a61f0-146">讀取最後一個出現的專案。</span><span class="sxs-lookup"><span data-stu-id="a61f0-146">Read last occurrence.</span></span> <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <span data-ttu-id="a61f0-147"><dt>**下次發生**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-147"><dt>**Next Occur**</dt></span></span> </dl>     | <span data-ttu-id="a61f0-148">位位置：-----010</span><span class="sxs-lookup"><span data-stu-id="a61f0-148">Bit position: -----010</span></span><br/> <span data-ttu-id="a61f0-149">讀取下一個出現的專案。</span><span class="sxs-lookup"><span data-stu-id="a61f0-149">Read next occurrence.</span></span> <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <span data-ttu-id="a61f0-150"><dt>**上一個**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-150"><dt>**Previous**</dt></span></span> </dl>             | <span data-ttu-id="a61f0-151">位位置：-----011</span><span class="sxs-lookup"><span data-stu-id="a61f0-151">Bit position: -----011</span></span><br/> <span data-ttu-id="a61f0-152">讀取先前的出現專案。</span><span class="sxs-lookup"><span data-stu-id="a61f0-152">Read previous occurrence.</span></span> <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="a61f0-153"><dt>**秘密**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-153"><dt>**Secret**</dt></span></span> </dl>                     | <span data-ttu-id="a61f0-154">位位置：---xxxxx</span><span class="sxs-lookup"><span data-stu-id="a61f0-154">Bit position: ---xxxxx</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="a61f0-155">*lBytesToRead* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a61f0-155">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a61f0-156">要從透明 EF 讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="a61f0-156">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="a61f0-157">如果 Le 欄位只包含零，則根據 P2 的 b3b2b1，以及在256的長度下限或65536（延長長度），此命令應完全讀取單一要求的記錄或要求的記錄順序。</span><span class="sxs-lookup"><span data-stu-id="a61f0-157">If the Le field contains only zeros, then depending on b3b2b1 of P2 and within the limit of 256 for short length or 65536 for extended length, the command should read completely either the single requested record or the requested sequence of records.</span></span>

</dd> <dt>

<span data-ttu-id="a61f0-158">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a61f0-158">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a61f0-159">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a61f0-159">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="a61f0-160">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="a61f0-160">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="a61f0-161">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並透過 *ppCmd* 指標傳回。</span><span class="sxs-lookup"><span data-stu-id="a61f0-161">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a61f0-162">傳回值</span><span class="sxs-lookup"><span data-stu-id="a61f0-162">Return value</span></span>

<span data-ttu-id="a61f0-163">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="a61f0-163">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a61f0-164">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a61f0-164">Return code</span></span>                                                                                   | <span data-ttu-id="a61f0-165">Description</span><span class="sxs-lookup"><span data-stu-id="a61f0-165">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a61f0-166"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-166"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a61f0-167">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="a61f0-167">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a61f0-168"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-168"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a61f0-169">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="a61f0-169">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="a61f0-170"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-170"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a61f0-171">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="a61f0-171">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="a61f0-172"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-172"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a61f0-173">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="a61f0-173">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a61f0-174">備註</span><span class="sxs-lookup"><span data-stu-id="a61f0-174">Remarks</span></span>

<span data-ttu-id="a61f0-175">只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所讀取之基本檔案的安全性屬性時，才能執行封裝的命令。</span><span class="sxs-lookup"><span data-stu-id="a61f0-175">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span>

<span data-ttu-id="a61f0-176">如果在發出此命令時，目前選取了另一個基本檔案，則可能會在未識別目前選取的檔案的情況下進行處理。</span><span class="sxs-lookup"><span data-stu-id="a61f0-176">If another elementary file is currently selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="a61f0-177">當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="a61f0-177">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="a61f0-178">無法讀取沒有記錄結構的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="a61f0-178">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="a61f0-179">如果套用至不含記錄結構的基本檔案，封裝的命令會中止。</span><span class="sxs-lookup"><span data-stu-id="a61f0-179">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="a61f0-180">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="a61f0-180">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="a61f0-181">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a61f0-181">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a61f0-182">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="a61f0-182">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a61f0-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="a61f0-183">Requirements</span></span>



| <span data-ttu-id="a61f0-184">需求</span><span class="sxs-lookup"><span data-stu-id="a61f0-184">Requirement</span></span> | <span data-ttu-id="a61f0-185">值</span><span class="sxs-lookup"><span data-stu-id="a61f0-185">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a61f0-186">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a61f0-186">Minimum supported client</span></span><br/> | <span data-ttu-id="a61f0-187">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a61f0-187">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a61f0-188">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a61f0-188">Minimum supported server</span></span><br/> | <span data-ttu-id="a61f0-189">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a61f0-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a61f0-190">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a61f0-190">End of client support</span></span><br/>    | <span data-ttu-id="a61f0-191">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a61f0-191">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a61f0-192">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a61f0-192">End of server support</span></span><br/>    | <span data-ttu-id="a61f0-193">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a61f0-193">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a61f0-194">標頭</span><span class="sxs-lookup"><span data-stu-id="a61f0-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="a61f0-195"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-195"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a61f0-196">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a61f0-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="a61f0-197"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-197"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a61f0-198">DLL</span><span class="sxs-lookup"><span data-stu-id="a61f0-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a61f0-199"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a61f0-199"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a61f0-200">IID</span><span class="sxs-lookup"><span data-stu-id="a61f0-200">IID</span></span><br/>                      | <span data-ttu-id="a61f0-201">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a61f0-201">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a61f0-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a61f0-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a61f0-203">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="a61f0-203">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="a61f0-204">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="a61f0-204">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="a61f0-205">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="a61f0-205">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="a61f0-206">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="a61f0-206">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
