---
description: AppendRecord 方法會將應用程式協定資料單位 (APDU) 命令，將記錄附加至線性結構化基礎檔案的結尾 (EF) 或在迴圈結構化的基本檔案中寫入記錄號碼1。
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: 'ISCardISO7816：： AppendRecord 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28d1b6762e0a350bb87b673f21fa063ae2478e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191852"
---
# <a name="iscardiso7816appendrecord-method"></a><span data-ttu-id="c1d76-103">ISCardISO7816：： AppendRecord 方法</span><span class="sxs-lookup"><span data-stu-id="c1d76-103">ISCardISO7816::AppendRecord method</span></span>

<span data-ttu-id="c1d76-104">\[**AppendRecord** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c1d76-104">\[The **AppendRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c1d76-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="c1d76-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c1d76-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c1d76-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c1d76-107">**AppendRecord** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，將記錄附加至線性結構化基礎檔案的結尾 (EF) 或在迴圈結構化的基本檔案中寫入記錄號碼1。</span><span class="sxs-lookup"><span data-stu-id="c1d76-107">The **AppendRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that either appends a record to the end of a linear-structured elementary file (EF) or writes record number 1 in a cyclic-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d76-108">語法</span><span class="sxs-lookup"><span data-stu-id="c1d76-108">Syntax</span></span>


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="c1d76-109">參數</span><span class="sxs-lookup"><span data-stu-id="c1d76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d76-110">*byRefCtrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1d76-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d76-111">識別要附加的基本檔。</span><span class="sxs-lookup"><span data-stu-id="c1d76-111">Identifies the elementary file to be appended.</span></span>



| <span data-ttu-id="c1d76-112">值</span><span class="sxs-lookup"><span data-stu-id="c1d76-112">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="c1d76-113">意義</span><span class="sxs-lookup"><span data-stu-id="c1d76-113">Meaning</span></span>                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="c1d76-114"><dt>**目前的 EF**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-114"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="c1d76-115">位位置：00000000</span><span class="sxs-lookup"><span data-stu-id="c1d76-115">Bit position: 00000000</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="c1d76-116"><dt>**簡短 EF 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-116"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="c1d76-117">位位置： xxxxx000</span><span class="sxs-lookup"><span data-stu-id="c1d76-117">Bit position: xxxxx000</span></span><br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="c1d76-118"><dt>**保留**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-118"><dt>**Reserved**</dt></span></span> </dl>             | <span data-ttu-id="c1d76-119">位位置： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="c1d76-119">Bit position: xxxxxxxx</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c1d76-120">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1d76-120">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d76-121">要附加至檔案的資料指標。</span><span class="sxs-lookup"><span data-stu-id="c1d76-121">A pointer to the data to be appended to the file.</span></span>



| <span data-ttu-id="c1d76-122">值</span><span class="sxs-lookup"><span data-stu-id="c1d76-122">Value</span></span>                                                                                                                                                | <span data-ttu-id="c1d76-123">意義</span><span class="sxs-lookup"><span data-stu-id="c1d76-123">Meaning</span></span>                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <span data-ttu-id="c1d76-124"><dt>**Tn**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-124"><dt>**Tn**</dt></span></span> </dl>     | <span data-ttu-id="c1d76-125">1 個位元組</span><span class="sxs-lookup"><span data-stu-id="c1d76-125">1 byte</span></span><br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <span data-ttu-id="c1d76-126"><dt>**Ln**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-126"><dt>**Ln** </dt></span></span> </dl> | <span data-ttu-id="c1d76-127">1或3個位元組</span><span class="sxs-lookup"><span data-stu-id="c1d76-127">1 or 3 bytes</span></span><br/> |
| <span id="data"></span><span id="DATA"></span><dl> <span data-ttu-id="c1d76-128"><dt>**資料**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-128"><dt>**data**</dt></span></span> </dl>                    | <span data-ttu-id="c1d76-129">Ln 位元組</span><span class="sxs-lookup"><span data-stu-id="c1d76-129">Ln bytes</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="c1d76-130">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c1d76-130">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d76-131">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c1d76-131">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="c1d76-132">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="c1d76-132">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="c1d76-133">如果 *ppCmd* 設定為 **Null**，就會使用 *ppCmd* 指標在內部建立和傳回 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md)物件。</span><span class="sxs-lookup"><span data-stu-id="c1d76-133">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1d76-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1d76-134">Return value</span></span>

<span data-ttu-id="c1d76-135">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="c1d76-135">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c1d76-136">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c1d76-136">Return code</span></span>                                                                                   | <span data-ttu-id="c1d76-137">Description</span><span class="sxs-lookup"><span data-stu-id="c1d76-137">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c1d76-138"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-138"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c1d76-139">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="c1d76-139">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="c1d76-140"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-140"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c1d76-141">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="c1d76-141">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="c1d76-142"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-142"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c1d76-143">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="c1d76-143">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="c1d76-144"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c1d76-145">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="c1d76-145">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c1d76-146">備註</span><span class="sxs-lookup"><span data-stu-id="c1d76-146">Remarks</span></span>

<span data-ttu-id="c1d76-147">只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合讀取之基本檔案的安全性屬性時，才能執行封裝的命令。</span><span class="sxs-lookup"><span data-stu-id="c1d76-147">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file read.</span></span>

<span data-ttu-id="c1d76-148">如果在發出此命令時選取了另一個基本檔案，則可能會在未識別目前選取的檔案的情況下進行處理。</span><span class="sxs-lookup"><span data-stu-id="c1d76-148">If another elementary file is selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="c1d76-149">無法讀取沒有記錄結構的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="c1d76-149">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="c1d76-150">如果套用至不含記錄結構的基本檔案，封裝的命令會中止。</span><span class="sxs-lookup"><span data-stu-id="c1d76-150">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="c1d76-151">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="c1d76-151">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="c1d76-152">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1d76-152">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c1d76-153">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="c1d76-153">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d76-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1d76-154">Requirements</span></span>



| <span data-ttu-id="c1d76-155">需求</span><span class="sxs-lookup"><span data-stu-id="c1d76-155">Requirement</span></span> | <span data-ttu-id="c1d76-156">值</span><span class="sxs-lookup"><span data-stu-id="c1d76-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d76-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1d76-157">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d76-158">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1d76-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c1d76-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1d76-159">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d76-160">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1d76-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1d76-161">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c1d76-161">End of client support</span></span><br/>    | <span data-ttu-id="c1d76-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c1d76-162">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c1d76-163">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c1d76-163">End of server support</span></span><br/>    | <span data-ttu-id="c1d76-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1d76-164">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c1d76-165">標頭</span><span class="sxs-lookup"><span data-stu-id="c1d76-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1d76-166"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-166"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1d76-167">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c1d76-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1d76-168"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-168"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1d76-169">DLL</span><span class="sxs-lookup"><span data-stu-id="c1d76-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1d76-170"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1d76-170"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1d76-171">IID</span><span class="sxs-lookup"><span data-stu-id="c1d76-171">IID</span></span><br/>                      | <span data-ttu-id="c1d76-172">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="c1d76-172">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c1d76-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1d76-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d76-174">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="c1d76-174">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="c1d76-175">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="c1d76-175">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="c1d76-176">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="c1d76-176">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="c1d76-177">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="c1d76-177">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
