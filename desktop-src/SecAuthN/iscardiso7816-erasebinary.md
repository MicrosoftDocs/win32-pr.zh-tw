---
description: 建立應用程式協定資料單位 (APDU) 命令，該命令會依序將基本檔案的一部分內容設定為其邏輯清除狀態（從指定的位移開始）。
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: 'ISCardISO7816：： EraseBinary 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a9bad21bbb35b7ac16209ac0075267ef7300fe21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994511"
---
# <a name="iscardiso7816erasebinary-method"></a><span data-ttu-id="03043-103">ISCardISO7816：： EraseBinary 方法</span><span class="sxs-lookup"><span data-stu-id="03043-103">ISCardISO7816::EraseBinary method</span></span>

<span data-ttu-id="03043-104">\[**EraseBinary** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="03043-104">\[The **EraseBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="03043-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="03043-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="03043-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="03043-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="03043-107">**EraseBinary** 方法會將 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，順序將基本檔案的一部分內容設定為其邏輯清除狀態（從指定的位移開始）。</span><span class="sxs-lookup"><span data-stu-id="03043-107">The **EraseBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sequentially sets part of the content of an elementary file to its logical erased state, starting from a given offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="03043-108">語法</span><span class="sxs-lookup"><span data-stu-id="03043-108">Syntax</span></span>


```C++
HRESULT EraseBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="03043-109">參數</span><span class="sxs-lookup"><span data-stu-id="03043-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03043-110">*byP1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03043-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03043-111">RFU 位置。</span><span class="sxs-lookup"><span data-stu-id="03043-111">RFU position.</span></span>

<span data-ttu-id="03043-112">如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是一個簡短的 EF 識別碼，P2 則是從檔案開頭開始，資料單位)  (清除的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="03043-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="03043-113">如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭)  (資料單位中清除之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="03043-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="03043-114">如果資料欄位存在，則會將第一個資料單位的位移編碼為不會被清除。</span><span class="sxs-lookup"><span data-stu-id="03043-114">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="03043-115">此位移應高於 P1-P2 中編碼的位移。</span><span class="sxs-lookup"><span data-stu-id="03043-115">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="03043-116">當資料欄位為空白時，此命令會清除到檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="03043-116">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="03043-117">*byP2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03043-117">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03043-118">RFU 位置。</span><span class="sxs-lookup"><span data-stu-id="03043-118">RFU position.</span></span>

<span data-ttu-id="03043-119">如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是一個簡短的 EF 識別碼，P2 則是從檔案開頭開始，資料單位)  (清除的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="03043-119">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="03043-120">如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭)  (資料單位中清除之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="03043-120">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="03043-121">如果資料欄位存在，則會將第一個資料單位的位移編碼為不會被清除。</span><span class="sxs-lookup"><span data-stu-id="03043-121">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="03043-122">此位移應高於 P1-P2 中編碼的位移。</span><span class="sxs-lookup"><span data-stu-id="03043-122">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="03043-123">當資料欄位為空白時，此命令會清除到檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="03043-123">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="03043-124">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="03043-124">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03043-125">指定清除範圍之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="03043-125">A pointer to the data that specifies the erase range.</span></span> <span data-ttu-id="03043-126">這個參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="03043-126">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="03043-127">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="03043-127">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="03043-128">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="03043-128">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="03043-129">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="03043-129">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="03043-130">如果 *ppCmd* 設定為 **Null**，就會使用 *ppCmd* 指標在內部建立和傳回 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md)物件。</span><span class="sxs-lookup"><span data-stu-id="03043-130">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03043-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="03043-131">Return value</span></span>

<span data-ttu-id="03043-132">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="03043-132">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="03043-133">傳回碼</span><span class="sxs-lookup"><span data-stu-id="03043-133">Return code</span></span>                                                                                   | <span data-ttu-id="03043-134">Description</span><span class="sxs-lookup"><span data-stu-id="03043-134">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="03043-135"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="03043-135"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="03043-136">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="03043-136">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="03043-137"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="03043-137"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="03043-138">傳遞的參數無效。</span><span class="sxs-lookup"><span data-stu-id="03043-138">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="03043-139"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="03043-139"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="03043-140">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="03043-140">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="03043-141"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="03043-141"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="03043-142">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="03043-142">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="03043-143">備註</span><span class="sxs-lookup"><span data-stu-id="03043-143">Remarks</span></span>

<span data-ttu-id="03043-144">只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所處理之基本檔案的安全性屬性時，才能執行封裝的命令。</span><span class="sxs-lookup"><span data-stu-id="03043-144">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="03043-145">當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="03043-145">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="03043-146">無法清除沒有透明結構的基本檔。</span><span class="sxs-lookup"><span data-stu-id="03043-146">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="03043-147">如果套用至不含透明結構的基本檔案，封裝的命令會中止。</span><span class="sxs-lookup"><span data-stu-id="03043-147">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="03043-148">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="03043-148">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="03043-149">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="03043-149">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="03043-150">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="03043-150">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03043-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="03043-151">Requirements</span></span>



| <span data-ttu-id="03043-152">需求</span><span class="sxs-lookup"><span data-stu-id="03043-152">Requirement</span></span> | <span data-ttu-id="03043-153">值</span><span class="sxs-lookup"><span data-stu-id="03043-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03043-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03043-154">Minimum supported client</span></span><br/> | <span data-ttu-id="03043-155">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03043-155">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="03043-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03043-156">Minimum supported server</span></span><br/> | <span data-ttu-id="03043-157">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03043-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03043-158">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="03043-158">End of client support</span></span><br/>    | <span data-ttu-id="03043-159">Windows XP</span><span class="sxs-lookup"><span data-stu-id="03043-159">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="03043-160">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="03043-160">End of server support</span></span><br/>    | <span data-ttu-id="03043-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03043-161">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="03043-162">標頭</span><span class="sxs-lookup"><span data-stu-id="03043-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="03043-163"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="03043-163"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="03043-164">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="03043-164">Type library</span></span><br/>             | <dl> <span data-ttu-id="03043-165"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="03043-165"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="03043-166">DLL</span><span class="sxs-lookup"><span data-stu-id="03043-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03043-167"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03043-167"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="03043-168">IID</span><span class="sxs-lookup"><span data-stu-id="03043-168">IID</span></span><br/>                      | <span data-ttu-id="03043-169">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="03043-169">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="03043-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03043-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03043-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="03043-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="03043-172">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="03043-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="03043-173">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="03043-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="03043-174">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="03043-174">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
