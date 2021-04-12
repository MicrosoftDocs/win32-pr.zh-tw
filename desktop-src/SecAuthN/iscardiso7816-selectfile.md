---
description: SelectFile 方法會建立應用程式協定資料單位 (APDU) 命令，此命令會在邏輯通道內設定目前的基本檔。 後續命令可能會透過邏輯通道隱含地參考目前的檔案。
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'ISCardISO7816：： SelectFile 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192955"
---
# <a name="iscardiso7816selectfile-method"></a><span data-ttu-id="2af08-104">ISCardISO7816：： SelectFile 方法</span><span class="sxs-lookup"><span data-stu-id="2af08-104">ISCardISO7816::SelectFile method</span></span>

<span data-ttu-id="2af08-105">\[**SelectFile** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2af08-105">\[The **SelectFile** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2af08-106">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="2af08-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2af08-107">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="2af08-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2af08-108">**SelectFile** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會在邏輯通道內設定目前的基本檔。</span><span class="sxs-lookup"><span data-stu-id="2af08-108">The **SelectFile** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sets a current elementary file within a logical channel.</span></span> <span data-ttu-id="2af08-109">後續命令可能會透過邏輯通道隱含地參考目前的檔案。</span><span class="sxs-lookup"><span data-stu-id="2af08-109">Subsequent commands may implicitly refer to the current file through the logical channel.</span></span>

<span data-ttu-id="2af08-110">在卡片檔案中選取 (DF) 的目錄（可能是檔案的根目錄 (MF) ）使其成為目前的 DF。</span><span class="sxs-lookup"><span data-stu-id="2af08-110">Selecting a directory (DF) within the card filestore — which may be the root (MF) of the filestore — makes it the current DF.</span></span> <span data-ttu-id="2af08-111">在這類選取專案之後，就可以透過該邏輯通道來參考隱含目前的基本檔。</span><span class="sxs-lookup"><span data-stu-id="2af08-111">After such a selection, an implicit current elementary file may be referred to through that logical channel.</span></span>

<span data-ttu-id="2af08-112">選取基本檔案會將選取的檔案及其父系設定為目前的檔案。</span><span class="sxs-lookup"><span data-stu-id="2af08-112">Selecting an elementary file sets the selected file and its parent as current files.</span></span>

<span data-ttu-id="2af08-113">在重設的答案之後，除非在歷程記錄的位元組或初始資料字串中指定不同，否則會透過基本邏輯通道隱含地選取 MF。</span><span class="sxs-lookup"><span data-stu-id="2af08-113">After the answer to reset, the MF is implicitly selected through the basic logical channel, unless specified differently in the historical bytes or in the initial data string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2af08-114">語法</span><span class="sxs-lookup"><span data-stu-id="2af08-114">Syntax</span></span>


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="2af08-115">參數</span><span class="sxs-lookup"><span data-stu-id="2af08-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2af08-116">*byP1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2af08-116">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2af08-117">選取控制項。</span><span class="sxs-lookup"><span data-stu-id="2af08-117">Selection control.</span></span>



| <span data-ttu-id="2af08-118">P1 (word) 中的上層位元組： 8 7 6 5 4 3 2 1</span><span class="sxs-lookup"><span data-stu-id="2af08-118">P1 (upper byte in word): 8 7 6 5 4 3 2 1</span></span>                                                                                                                                                            | <span data-ttu-id="2af08-119">意義</span><span class="sxs-lookup"><span data-stu-id="2af08-119">Meaning</span></span>                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <span data-ttu-id="2af08-120"><dt>**000000xx**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="2af08-120"><dt>**000000xx**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="2af08-121">選取檔案識別碼</span><span class="sxs-lookup"><span data-stu-id="2af08-121">Select File ID</span></span><br/>          |
| <span id="00000000"></span><dl> <span data-ttu-id="2af08-122"><dt>**00000000**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="2af08-122"><dt>**00000000**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="2af08-123">EF、DF 或 MF</span><span class="sxs-lookup"><span data-stu-id="2af08-123">EF, DF, or MF</span></span><br/>           |
| <span id="00000001"></span><dl> <span data-ttu-id="2af08-124"><dt>**00000001**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="2af08-124"><dt>**00000001**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="2af08-125">子 DF</span><span class="sxs-lookup"><span data-stu-id="2af08-125">Child DF</span></span><br/>                |
| <span id="00000010"></span><dl> <span data-ttu-id="2af08-126"><dt>**00000010**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="2af08-126"><dt>**00000010**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="2af08-127">DF 下的 EF</span><span class="sxs-lookup"><span data-stu-id="2af08-127">EF under DF</span></span><br/>             |
| <span id="00000011"></span><dl> <span data-ttu-id="2af08-128"><dt>**00000011**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="2af08-128"><dt>**00000011**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="2af08-129">目前 DF 的父 DF</span><span class="sxs-lookup"><span data-stu-id="2af08-129">Parent DF of current DF</span></span><br/> |



 

<span data-ttu-id="2af08-130">當 P1 = 00 時，卡片知道檔案識別碼的特定編碼方式，或如果要選取的檔案是 MF、DF 或 EF，則知道命令的執行內容。</span><span class="sxs-lookup"><span data-stu-id="2af08-130">When P1=00, the card knows either because of a specific coding of the file ID or because of the context of execution of the command if the file to select is the MF, a DF, or an EF.</span></span>

<span data-ttu-id="2af08-131">當 P1-P2 = 0000 時，如果已提供檔案識別碼，則在下列環境中應該是唯一的：</span><span class="sxs-lookup"><span data-stu-id="2af08-131">When P1-P2=0000, if a file ID is provided, then it shall be unique in the following environments:</span></span>

-   <span data-ttu-id="2af08-132">目前 DF 的直屬子系</span><span class="sxs-lookup"><span data-stu-id="2af08-132">Immediate children of the current DF</span></span>
-   <span data-ttu-id="2af08-133">父 DF</span><span class="sxs-lookup"><span data-stu-id="2af08-133">Parent DF</span></span>
-   <span data-ttu-id="2af08-134">父 DF 的直屬子系</span><span class="sxs-lookup"><span data-stu-id="2af08-134">Immediate children of the parent DF</span></span>

<span data-ttu-id="2af08-135">如果 P1-P2 = 0000，且資料欄位為空白或等於3F00，則選取 MF。</span><span class="sxs-lookup"><span data-stu-id="2af08-135">If P1-P2=0000 and if the data field is empty or equal to 3F00, then select the MF.</span></span>

<span data-ttu-id="2af08-136">當 P1 = 04 時，資料欄位是 DF 名稱，可能會以正確的截斷。</span><span class="sxs-lookup"><span data-stu-id="2af08-136">When P1=04, the data field is a DF name, possibly right truncated.</span></span>

<span data-ttu-id="2af08-137">在支援的情況下，後續具有相同資料欄位的這類命令，就應該選取名稱與資料欄位相符的 DFs (也就是從命令資料欄位) 開始。</span><span class="sxs-lookup"><span data-stu-id="2af08-137">When supported, successive such commands with the same data field shall select DFs whose names match with the data field (that is, start with the command data field).</span></span> <span data-ttu-id="2af08-138">如果卡片接受具有空白資料欄位的命令，則可以連續選取所有或 DFs 子集。</span><span class="sxs-lookup"><span data-stu-id="2af08-138">If the card accepts the command with an empty data field, then all or a subset of the DFs can be successively selected.</span></span>

</dd> <dt>

<span data-ttu-id="2af08-139">*byP2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2af08-139">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2af08-140">選取控制項。</span><span class="sxs-lookup"><span data-stu-id="2af08-140">Selection control.</span></span>

</dd> <dt>

<span data-ttu-id="2af08-141">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2af08-141">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2af08-142">需要作業的資料;否則 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="2af08-142">Data for operation if needed; else, **NULL**.</span></span> <span data-ttu-id="2af08-143">傳入此參數的資料類型包括：</span><span class="sxs-lookup"><span data-stu-id="2af08-143">Types of data that are passed in this parameter include:</span></span>

-   <span data-ttu-id="2af08-144">檔案識別碼</span><span class="sxs-lookup"><span data-stu-id="2af08-144">file ID</span></span>
-   <span data-ttu-id="2af08-145">來自 MF 的路徑</span><span class="sxs-lookup"><span data-stu-id="2af08-145">path from the MF</span></span>
-   <span data-ttu-id="2af08-146">來自目前 DF 的路徑</span><span class="sxs-lookup"><span data-stu-id="2af08-146">path from the current DF</span></span>
-   <span data-ttu-id="2af08-147">DF 名稱</span><span class="sxs-lookup"><span data-stu-id="2af08-147">DF name</span></span>

</dd> <dt>

<span data-ttu-id="2af08-148">*lBytesToRead* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2af08-148">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2af08-149">空白 (，也就是 0) 或回應中預期的最大資料長度。</span><span class="sxs-lookup"><span data-stu-id="2af08-149">Empty (that is, 0) or maximum length of data expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="2af08-150">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2af08-150">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2af08-151">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2af08-151">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="2af08-152">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="2af08-152">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="2af08-153">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並透過 *ppCmd* 指標傳回。</span><span class="sxs-lookup"><span data-stu-id="2af08-153">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2af08-154">傳回值</span><span class="sxs-lookup"><span data-stu-id="2af08-154">Return value</span></span>

<span data-ttu-id="2af08-155">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="2af08-155">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2af08-156">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2af08-156">Return code</span></span>                                                                                   | <span data-ttu-id="2af08-157">Description</span><span class="sxs-lookup"><span data-stu-id="2af08-157">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2af08-158"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2af08-158"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2af08-159">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="2af08-159">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="2af08-160"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2af08-160"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2af08-161">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="2af08-161">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="2af08-162"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="2af08-162"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2af08-163">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="2af08-163">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="2af08-164"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2af08-164"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2af08-165">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="2af08-165">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2af08-166">備註</span><span class="sxs-lookup"><span data-stu-id="2af08-166">Remarks</span></span>

<span data-ttu-id="2af08-167">除非另有指定，否則封裝命令的正確執行會根據下列規則來修改安全性狀態：</span><span class="sxs-lookup"><span data-stu-id="2af08-167">Unless otherwise specified, the correct execution of the encapsulated command modifies the security status according to the following rules:</span></span>

-   <span data-ttu-id="2af08-168">當目前的基本檔案變更，或沒有目前的基本檔案時，會遺失先前目前基本檔案的特定安全性狀態。</span><span class="sxs-lookup"><span data-stu-id="2af08-168">When the current elementary file is changed, or when there is no current elementary file, the security status specific to a former current elementary file is lost.</span></span>
-   <span data-ttu-id="2af08-169">當目前的「可寫入的目錄」 (DF) 為的子系或與先前目前的 DF 相同時，就會遺失之前的目前 DF 的特定安全性狀態。</span><span class="sxs-lookup"><span data-stu-id="2af08-169">When the current filestore directory (DF) is descendant of, or identical to the former current DF, the security status specific to the former current DF is lost.</span></span> <span data-ttu-id="2af08-170">先前和新的目前 DF 的所有通用祖系通用的安全性狀態會維持不變。</span><span class="sxs-lookup"><span data-stu-id="2af08-170">The security status common to all common ancestors of the previous and new current DF is maintained.</span></span>

<span data-ttu-id="2af08-171">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="2af08-171">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="2af08-172">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2af08-172">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2af08-173">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="2af08-173">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2af08-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="2af08-174">Requirements</span></span>



| <span data-ttu-id="2af08-175">需求</span><span class="sxs-lookup"><span data-stu-id="2af08-175">Requirement</span></span> | <span data-ttu-id="2af08-176">值</span><span class="sxs-lookup"><span data-stu-id="2af08-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2af08-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2af08-177">Minimum supported client</span></span><br/> | <span data-ttu-id="2af08-178">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2af08-178">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2af08-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2af08-179">Minimum supported server</span></span><br/> | <span data-ttu-id="2af08-180">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2af08-180">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2af08-181">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2af08-181">End of client support</span></span><br/>    | <span data-ttu-id="2af08-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2af08-182">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2af08-183">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2af08-183">End of server support</span></span><br/>    | <span data-ttu-id="2af08-184">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2af08-184">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2af08-185">標頭</span><span class="sxs-lookup"><span data-stu-id="2af08-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="2af08-186"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2af08-186"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2af08-187">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2af08-187">Type library</span></span><br/>             | <dl> <span data-ttu-id="2af08-188"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2af08-188"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2af08-189">DLL</span><span class="sxs-lookup"><span data-stu-id="2af08-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2af08-190"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2af08-190"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2af08-191">IID</span><span class="sxs-lookup"><span data-stu-id="2af08-191">IID</span></span><br/>                      | <span data-ttu-id="2af08-192">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2af08-192">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2af08-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2af08-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2af08-194">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="2af08-194">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
