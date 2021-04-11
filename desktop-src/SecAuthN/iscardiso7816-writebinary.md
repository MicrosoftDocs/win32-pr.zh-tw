---
description: WriteBinary 方法會建立應用程式協定資料單位 (APDU) 命令，以將二進位值寫入基本檔案。
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'ISCardISO7816：： WriteBinary 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 330e817bc501c451026589087991fb43c0b5ac57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936609"
---
# <a name="iscardiso7816writebinary-method"></a><span data-ttu-id="f207c-103">ISCardISO7816：： WriteBinary 方法</span><span class="sxs-lookup"><span data-stu-id="f207c-103">ISCardISO7816::WriteBinary method</span></span>

<span data-ttu-id="f207c-104">\[**WriteBinary** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f207c-104">\[The **WriteBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f207c-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="f207c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f207c-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f207c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f207c-107">**WriteBinary** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，以將二進位值寫入基本檔案。</span><span class="sxs-lookup"><span data-stu-id="f207c-107">The **WriteBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that writes binary values into an elementary file.</span></span>

<span data-ttu-id="f207c-108">視檔案屬性而定，此命令會執行下列其中一項作業：</span><span class="sxs-lookup"><span data-stu-id="f207c-108">Depending upon the file attributes, the command performs one of the following operations:</span></span>

-   <span data-ttu-id="f207c-109">包含在命令 APDU 中的位的邏輯 OR 已存在於命令 APDU (邏輯清除的檔案位狀態為 0) 。</span><span class="sxs-lookup"><span data-stu-id="f207c-109">The logical OR of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 0).</span></span>
-   <span data-ttu-id="f207c-110">包含在命令 APDU 中的位的邏輯 AND 都已存在於命令 APDU (邏輯清除的檔案位狀態為 1) 。</span><span class="sxs-lookup"><span data-stu-id="f207c-110">The logical AND of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 1).</span></span>
-   <span data-ttu-id="f207c-111">在命令 APDU 中指定之位的卡片中進行一次性寫入。</span><span class="sxs-lookup"><span data-stu-id="f207c-111">The one-time write in the card of the bits given in the command APDU.</span></span>

<span data-ttu-id="f207c-112">如果資料編碼位元組中未提供任何指示，則會套用邏輯 OR 行為。</span><span class="sxs-lookup"><span data-stu-id="f207c-112">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="f207c-113">語法</span><span class="sxs-lookup"><span data-stu-id="f207c-113">Syntax</span></span>


```C++
HRESULT WriteBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="f207c-114">參數</span><span class="sxs-lookup"><span data-stu-id="f207c-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f207c-115">*byP1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f207c-115">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f207c-116">從二進位檔案開頭的寫入位置位移 (EF) 。</span><span class="sxs-lookup"><span data-stu-id="f207c-116">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="f207c-117">如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是簡短的 EF 識別碼，P2 是從檔案開頭以資料單位寫入的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="f207c-117">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="f207c-118">如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭以資料單位寫入之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="f207c-118">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="f207c-119">*byP2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f207c-119">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f207c-120">從二進位檔案開頭的寫入位置位移 (EF) 。</span><span class="sxs-lookup"><span data-stu-id="f207c-120">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="f207c-121">如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是簡短的 EF 識別碼，P2 是從檔案開頭以資料單位寫入的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="f207c-121">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="f207c-122">如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭以資料單位寫入之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="f207c-122">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="f207c-123">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f207c-123">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f207c-124">要寫入之資料單位的字串指標。</span><span class="sxs-lookup"><span data-stu-id="f207c-124">Pointer to the string of data units to be written.</span></span>

</dd> <dt>

<span data-ttu-id="f207c-125">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f207c-125">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f207c-126">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f207c-126">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="f207c-127">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="f207c-127">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="f207c-128">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並透過 *ppCmd* 指標傳回。</span><span class="sxs-lookup"><span data-stu-id="f207c-128">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f207c-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="f207c-129">Return value</span></span>

<span data-ttu-id="f207c-130">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="f207c-130">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f207c-131">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f207c-131">Return code</span></span>                                                                                   | <span data-ttu-id="f207c-132">Description</span><span class="sxs-lookup"><span data-stu-id="f207c-132">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f207c-133"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f207c-133"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f207c-134">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="f207c-134">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f207c-135"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f207c-135"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f207c-136">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="f207c-136">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="f207c-137"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f207c-137"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f207c-138">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="f207c-138">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="f207c-139"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f207c-139"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f207c-140">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="f207c-140">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f207c-141">備註</span><span class="sxs-lookup"><span data-stu-id="f207c-141">Remarks</span></span>

<span data-ttu-id="f207c-142">只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所處理之基本檔案的安全性屬性時，才能執行封裝的命令。</span><span class="sxs-lookup"><span data-stu-id="f207c-142">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="f207c-143">當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="f207c-143">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="f207c-144">當寫入二進位運算已套用至一次性寫入 EF 的資料單位時，如果任何附加至此資料單位的) 與邏輯清除的狀態不同，則會在資料單位或邏輯清除狀態指標的內容 (時，中止任何參考此資料單位的寫入作業。</span><span class="sxs-lookup"><span data-stu-id="f207c-144">When a write binary operation has been applied to a data unit of a one-time write EF, any further write operation referring to this data unit will be aborted if the content of the data unit or the logical erased state indicator (if any) attached to this data unit is different from the logical erased state.</span></span>

<span data-ttu-id="f207c-145">無法寫入不含透明結構的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="f207c-145">Elementary files without a transparent structure cannot be written to.</span></span> <span data-ttu-id="f207c-146">如果套用至不含透明結構的基本檔案，封裝的命令會中止。</span><span class="sxs-lookup"><span data-stu-id="f207c-146">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="f207c-147">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="f207c-147">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="f207c-148">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f207c-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f207c-149">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="f207c-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f207c-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="f207c-150">Requirements</span></span>



| <span data-ttu-id="f207c-151">需求</span><span class="sxs-lookup"><span data-stu-id="f207c-151">Requirement</span></span> | <span data-ttu-id="f207c-152">值</span><span class="sxs-lookup"><span data-stu-id="f207c-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f207c-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f207c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f207c-154">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f207c-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f207c-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f207c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f207c-156">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f207c-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f207c-157">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f207c-157">End of client support</span></span><br/>    | <span data-ttu-id="f207c-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f207c-158">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f207c-159">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f207c-159">End of server support</span></span><br/>    | <span data-ttu-id="f207c-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f207c-160">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f207c-161">標頭</span><span class="sxs-lookup"><span data-stu-id="f207c-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="f207c-162"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f207c-162"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f207c-163">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f207c-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="f207c-164"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f207c-164"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f207c-165">DLL</span><span class="sxs-lookup"><span data-stu-id="f207c-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f207c-166"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f207c-166"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f207c-167">IID</span><span class="sxs-lookup"><span data-stu-id="f207c-167">IID</span></span><br/>                      | <span data-ttu-id="f207c-168">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f207c-168">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="f207c-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f207c-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f207c-170">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="f207c-170">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="f207c-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="f207c-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="f207c-172">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="f207c-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="f207c-173">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="f207c-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
