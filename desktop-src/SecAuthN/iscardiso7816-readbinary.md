---
description: ReadBinary 方法會建立應用程式協定資料單位 (APDU) 命令取得回應訊息，以提供透明結構化基本檔案內容的一部分。
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'ISCardISO7816：： ReadBinary 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851731"
---
# <a name="iscardiso7816readbinary-method"></a><span data-ttu-id="97ed2-103">ISCardISO7816：： ReadBinary 方法</span><span class="sxs-lookup"><span data-stu-id="97ed2-103">ISCardISO7816::ReadBinary method</span></span>

<span data-ttu-id="97ed2-104">\[**ReadBinary** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="97ed2-104">\[The **ReadBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="97ed2-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="97ed2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="97ed2-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="97ed2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="97ed2-107">**ReadBinary** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令取得回應訊息，以提供透明結構化基本檔案內容的一部分。</span><span class="sxs-lookup"><span data-stu-id="97ed2-107">The **ReadBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that acquires a response message that gives that part of the contents of a transparent-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="97ed2-108">語法</span><span class="sxs-lookup"><span data-stu-id="97ed2-108">Syntax</span></span>


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="97ed2-109">參數</span><span class="sxs-lookup"><span data-stu-id="97ed2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97ed2-110">*byP1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97ed2-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97ed2-111">P1-P2 欄位，從檔開頭開始讀取的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="97ed2-111">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="97ed2-112">如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是簡短的 EF 識別碼，P2 是從檔案開頭開始讀取之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="97ed2-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="97ed2-113">如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭讀入資料單位的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="97ed2-113">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="97ed2-114">*byP2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97ed2-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97ed2-115">P1-P2 欄位，從檔開頭開始讀取的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="97ed2-115">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="97ed2-116">如果 P1 中的 b8 = 1，則 P1 和 b6 的 P1 會設定為零 (RFU 位) ，則為 P1 到 P1 的 b1 是簡短的 EF 識別碼，P2 是從檔案開頭開始讀取之第一個位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="97ed2-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="97ed2-117">如果 P1 中的 b8 = 0，則 P1 \| \| P2 是從檔案開頭讀入資料單位的第一個位元組位移。</span><span class="sxs-lookup"><span data-stu-id="97ed2-117">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="97ed2-118">*lBytesToRead* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97ed2-118">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97ed2-119">要從透明 EF 讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="97ed2-119">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="97ed2-120">如果 Le 欄位只包含零，則在256的限制（長度為）或延長長度的65536以內，則必須讀取檔案結尾為止的所有位元組。</span><span class="sxs-lookup"><span data-stu-id="97ed2-120">If the Le field contains only zeros, then within the limit of 256 for short length or 65536 for extended length, all the bytes until the end of the file should be read.</span></span>

</dd> <dt>

<span data-ttu-id="97ed2-121">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="97ed2-121">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97ed2-122">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="97ed2-122">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="97ed2-123">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="97ed2-123">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="97ed2-124">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並使用 *ppCmd* 指標來傳回。</span><span class="sxs-lookup"><span data-stu-id="97ed2-124">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97ed2-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="97ed2-125">Return value</span></span>

<span data-ttu-id="97ed2-126">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="97ed2-126">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="97ed2-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="97ed2-127">Return code</span></span>                                                                                   | <span data-ttu-id="97ed2-128">Description</span><span class="sxs-lookup"><span data-stu-id="97ed2-128">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="97ed2-129"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="97ed2-129"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="97ed2-130">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="97ed2-130">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="97ed2-131"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="97ed2-131"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="97ed2-132">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="97ed2-132">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="97ed2-133"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="97ed2-133"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="97ed2-134">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="97ed2-134">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="97ed2-135"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="97ed2-135"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="97ed2-136">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="97ed2-136">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="97ed2-137">備註</span><span class="sxs-lookup"><span data-stu-id="97ed2-137">Remarks</span></span>

<span data-ttu-id="97ed2-138">只有當 [*智慧卡*](../secgloss/s-gly.md) 的安全性狀態符合所處理之基本檔案的安全性屬性時，才能執行封裝的命令。</span><span class="sxs-lookup"><span data-stu-id="97ed2-138">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="97ed2-139">當命令包含有效的簡短基本識別碼時，它會將檔案設定為目前的基本檔案。</span><span class="sxs-lookup"><span data-stu-id="97ed2-139">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="97ed2-140">無法清除沒有透明結構的基本檔。</span><span class="sxs-lookup"><span data-stu-id="97ed2-140">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="97ed2-141">如果套用至不含透明結構的基本檔案，封裝的命令會中止。</span><span class="sxs-lookup"><span data-stu-id="97ed2-141">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="97ed2-142">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="97ed2-142">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="97ed2-143">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="97ed2-143">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="97ed2-144">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="97ed2-144">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97ed2-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="97ed2-145">Requirements</span></span>



| <span data-ttu-id="97ed2-146">需求</span><span class="sxs-lookup"><span data-stu-id="97ed2-146">Requirement</span></span> | <span data-ttu-id="97ed2-147">值</span><span class="sxs-lookup"><span data-stu-id="97ed2-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97ed2-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97ed2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="97ed2-149">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97ed2-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="97ed2-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97ed2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="97ed2-151">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97ed2-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97ed2-152">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="97ed2-152">End of client support</span></span><br/>    | <span data-ttu-id="97ed2-153">Windows XP</span><span class="sxs-lookup"><span data-stu-id="97ed2-153">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="97ed2-154">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="97ed2-154">End of server support</span></span><br/>    | <span data-ttu-id="97ed2-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="97ed2-155">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="97ed2-156">標頭</span><span class="sxs-lookup"><span data-stu-id="97ed2-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="97ed2-157"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="97ed2-157"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="97ed2-158">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="97ed2-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="97ed2-159"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="97ed2-159"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="97ed2-160">DLL</span><span class="sxs-lookup"><span data-stu-id="97ed2-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97ed2-161"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97ed2-161"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="97ed2-162">IID</span><span class="sxs-lookup"><span data-stu-id="97ed2-162">IID</span></span><br/>                      | <span data-ttu-id="97ed2-163">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="97ed2-163">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="97ed2-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97ed2-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ed2-165">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="97ed2-165">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="97ed2-166">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="97ed2-166">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="97ed2-167">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="97ed2-167">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="97ed2-168">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="97ed2-168">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
