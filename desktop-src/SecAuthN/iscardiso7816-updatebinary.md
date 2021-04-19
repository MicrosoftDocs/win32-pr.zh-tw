---
description: UpdateBinary 方法會將應用程式協定資料單位 (APDU) 命令，以使用 APDU 命令中指定的位來更新基本檔案中的位。
ms.assetid: 14ac6ad9-efcf-48ea-8712-19caeee47521
title: 'ISCardISO7816：： UpdateBinary 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d9651189cab228eaa5dacc9c2f5963201bbc65c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980339"
---
# <a name="iscardiso7816updatebinary-method"></a><span data-ttu-id="6a665-103">ISCardISO7816：： UpdateBinary 方法</span><span class="sxs-lookup"><span data-stu-id="6a665-103">ISCardISO7816::UpdateBinary method</span></span>

<span data-ttu-id="6a665-104">\[**UpdateBinary** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6a665-104">\[The **UpdateBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6a665-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6a665-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6a665-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6a665-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6a665-107">**UpdateBinary** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，以使用 APDU 命令中指定的位來更新基本檔案中的位。</span><span class="sxs-lookup"><span data-stu-id="6a665-107">The **UpdateBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates the bits present in an elementary file with the bits given in the APDU command.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a665-108">語法</span><span class="sxs-lookup"><span data-stu-id="6a665-108">Syntax</span></span>


```C++
HRESULT UpdateBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="6a665-109">參數</span><span class="sxs-lookup"><span data-stu-id="6a665-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a665-110">*byP1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a665-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a665-111">寫入的位移 (從二進位檔開頭將) 位置更新為二進位檔。</span><span class="sxs-lookup"><span data-stu-id="6a665-111">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="6a665-112">如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是簡短的 EF 識別碼，P2 則是從檔案開頭開始更新資料單位的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="6a665-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="6a665-113">如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭開始更新資料單位中第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="6a665-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="6a665-114">*byP2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a665-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a665-115">寫入的位移 (從二進位檔開頭將) 位置更新為二進位檔。</span><span class="sxs-lookup"><span data-stu-id="6a665-115">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="6a665-116">如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是簡短的 EF 識別碼，P2 則是從檔案開頭開始更新資料單位的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="6a665-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="6a665-117">如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭開始更新資料單位中第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="6a665-117">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="6a665-118">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a665-118">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a665-119">要更新之資料單位的字串指標。</span><span class="sxs-lookup"><span data-stu-id="6a665-119">Pointer to the string of data units to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="6a665-120">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6a665-120">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a665-121">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6a665-121">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="6a665-122">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="6a665-122">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="6a665-123">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並使用 *ppCmd* 指標來傳回。</span><span class="sxs-lookup"><span data-stu-id="6a665-123">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a665-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a665-124">Return value</span></span>

<span data-ttu-id="6a665-125">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="6a665-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6a665-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6a665-126">Return code</span></span>                                                                                   | <span data-ttu-id="6a665-127">Description</span><span class="sxs-lookup"><span data-stu-id="6a665-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6a665-128"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6a665-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6a665-129">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="6a665-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6a665-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6a665-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6a665-131">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="6a665-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6a665-132"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="6a665-132"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6a665-133">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="6a665-133">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6a665-134"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6a665-134"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6a665-135">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="6a665-135">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6a665-136">備註</span><span class="sxs-lookup"><span data-stu-id="6a665-136">Remarks</span></span>

<span data-ttu-id="6a665-137">只有當智慧卡的安全性狀態符合所處理之基本檔案的安全性屬性時，才能執行封裝的命令。</span><span class="sxs-lookup"><span data-stu-id="6a665-137">The encapsulated command can only be performed if the security status of the smart card satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="6a665-138">當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="6a665-138">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="6a665-139">無法清除沒有透明結構的基本檔。</span><span class="sxs-lookup"><span data-stu-id="6a665-139">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="6a665-140">如果套用至不含透明結構的基本檔案，封裝的命令會中止。</span><span class="sxs-lookup"><span data-stu-id="6a665-140">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="6a665-141">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="6a665-141">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="6a665-142">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6a665-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6a665-143">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6a665-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a665-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a665-144">Requirements</span></span>



| <span data-ttu-id="6a665-145">需求</span><span class="sxs-lookup"><span data-stu-id="6a665-145">Requirement</span></span> | <span data-ttu-id="6a665-146">值</span><span class="sxs-lookup"><span data-stu-id="6a665-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a665-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a665-147">Minimum supported client</span></span><br/> | <span data-ttu-id="6a665-148">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a665-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6a665-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a665-149">Minimum supported server</span></span><br/> | <span data-ttu-id="6a665-150">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a665-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a665-151">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6a665-151">End of client support</span></span><br/>    | <span data-ttu-id="6a665-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6a665-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6a665-153">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6a665-153">End of server support</span></span><br/>    | <span data-ttu-id="6a665-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6a665-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6a665-155">標頭</span><span class="sxs-lookup"><span data-stu-id="6a665-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a665-156"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a665-156"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a665-157">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="6a665-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a665-158"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6a665-158"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6a665-159">DLL</span><span class="sxs-lookup"><span data-stu-id="6a665-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a665-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a665-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6a665-161">IID</span><span class="sxs-lookup"><span data-stu-id="6a665-161">IID</span></span><br/>                      | <span data-ttu-id="6a665-162">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6a665-162">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6a665-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a665-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a665-164">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="6a665-164">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="6a665-165">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="6a665-165">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="6a665-166">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="6a665-166">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="6a665-167">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="6a665-167">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
