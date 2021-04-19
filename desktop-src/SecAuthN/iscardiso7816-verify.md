---
description: 建立應用程式協定資料單位 (APDU) 命令，此命令會使用卡片中儲存的參考資料，從介面裝置所傳送的驗證資料) 中起始比較 ( (例如，密碼) 。
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'ISCardISO7816：： Verify 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980338"
---
# <a name="iscardiso7816verify-method"></a><span data-ttu-id="bc4c0-103">ISCardISO7816：： Verify 方法</span><span class="sxs-lookup"><span data-stu-id="bc4c0-103">ISCardISO7816::Verify method</span></span>

<span data-ttu-id="bc4c0-104">\[[ **驗證** ] 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bc4c0-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bc4c0-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="bc4c0-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bc4c0-107">**Verify** 方法會 (APDU 來建立 [*應用程式協定資料單位*](../secgloss/a-gly.md)) 命令，以在從介面裝置傳送的驗證資料) 中，使用儲存在卡片中的參考資料來啟動 (的驗證資料 (例如，密碼) 。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-107">The **Verify** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the comparison (in the card) of the verification data sent from the interface device with the reference data stored in the card (for example, password).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc4c0-108">語法</span><span class="sxs-lookup"><span data-stu-id="bc4c0-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="bc4c0-109">參數</span><span class="sxs-lookup"><span data-stu-id="bc4c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc4c0-110">*byRefCtrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc4c0-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc4c0-111">參考資料的數量詞。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-111">A quantifier of the reference data.</span></span> <span data-ttu-id="bc4c0-112">參考控制項 P2 的編碼如下。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-112">Coding of the reference control P2 follows.</span></span>

<span data-ttu-id="bc4c0-113">當主體是空的時，您可以使用此命令來取得進一步允許的重試次數 (SW1-SW2 = 63CX) 或檢查是否不需要驗證 (SW1-SW2 = 9000) 。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-113">When the body is empty, the command may be used either to retrieve the number 'X' of further allowed retries (SW1-SW2=63CX) or to check whether the verification is not required (SW1-SW2=9000).</span></span>



| <span data-ttu-id="bc4c0-114">值</span><span class="sxs-lookup"><span data-stu-id="bc4c0-114">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="bc4c0-115">意義</span><span class="sxs-lookup"><span data-stu-id="bc4c0-115">Meaning</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="bc4c0-116"><dt>**沒有資訊**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-116"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="bc4c0-117">位位置：00000000</span><span class="sxs-lookup"><span data-stu-id="bc4c0-117">Bit position: 00000000</span></span><br/> <span data-ttu-id="bc4c0-118">P2 = 00 是保留的，表示在這些卡片中不會使用任何特定的辨識符號，而驗證命令會明確地參考秘密資料。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-118">P2=00 is reserved to indicate that no particular qualifier is used in those cards where the verify command references the secret data unambiguously.</span></span><br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="bc4c0-119"><dt>**全域參考**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-119"><dt>**Global Ref**</dt></span></span> </dl>         | <span data-ttu-id="bc4c0-120">位位置： 0-------</span><span class="sxs-lookup"><span data-stu-id="bc4c0-120">Bit position: 0-------</span></span><br/> <span data-ttu-id="bc4c0-121">全域 Ref 的範例就是密碼。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-121">An example of Global Ref would be a password.</span></span><br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="bc4c0-122"><dt>**特定參考**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-122"><dt>**Specific Ref**</dt></span></span> </dl> | <span data-ttu-id="bc4c0-123">位位置： 1-------</span><span class="sxs-lookup"><span data-stu-id="bc4c0-123">Bit position: 1-------</span></span><br/> <span data-ttu-id="bc4c0-124">特定 Ref 的範例是 DF 特定密碼。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-124">An example of Specific Ref is DF specific password.</span></span><br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="bc4c0-125"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-125"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="bc4c0-126">位位置：-xx-----</span><span class="sxs-lookup"><span data-stu-id="bc4c0-126">Bit position: -xx-----</span></span><br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <span data-ttu-id="bc4c0-127"><dt>**參考資料 \#**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-127"><dt>**Ref Data \#**</dt></span></span> </dl>        | <span data-ttu-id="bc4c0-128">位位置：---xxxxx</span><span class="sxs-lookup"><span data-stu-id="bc4c0-128">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="bc4c0-129">例如，參考資料編號可能是密碼號碼或簡短的 EF 識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-129">The reference data number may be, for example, a password number or a short EF identifier.</span></span><br/>                                                           |



 

</dd> <dt>

<span data-ttu-id="bc4c0-130">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc4c0-130">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc4c0-131">驗證資料的指標。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-131">A pointer to the verification data.</span></span> <span data-ttu-id="bc4c0-132">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-132">This parameter can be **NULL**.</span></span> <span data-ttu-id="bc4c0-133">預設值是 **NULL**。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-133">The default value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc4c0-134">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bc4c0-134">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc4c0-135">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-135">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="bc4c0-136">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-136">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="bc4c0-137">如果 *ppCmd* 設定為 **Null**，就會使用 *ppCmd* 指標在內部建立和傳回 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md)物件。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-137">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc4c0-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc4c0-138">Return value</span></span>

<span data-ttu-id="bc4c0-139">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="bc4c0-140">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bc4c0-140">Return code</span></span>                                                                                   | <span data-ttu-id="bc4c0-141">Description</span><span class="sxs-lookup"><span data-stu-id="bc4c0-141">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="bc4c0-142"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bc4c0-143">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-143">The operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="bc4c0-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bc4c0-145">使用了不正確參數。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-145">A parameter that is not valid was used.</span></span><br/> |
| <dl> <span data-ttu-id="bc4c0-146"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bc4c0-147">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-147">A bad pointer was passed in.</span></span><br/>            |
| <dl> <span data-ttu-id="bc4c0-148"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bc4c0-149">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-149">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="bc4c0-150">備註</span><span class="sxs-lookup"><span data-stu-id="bc4c0-150">Remarks</span></span>

<span data-ttu-id="bc4c0-151">可能會因為比較結果而修改安全性狀態。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-151">The security status may be modified as a result of a comparison.</span></span> <span data-ttu-id="bc4c0-152">失敗的比較可能會記錄在卡片 (例如，以限制使用參考資料) 的進一步嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-152">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="bc4c0-153">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-153">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="bc4c0-154">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-154">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bc4c0-155">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="bc4c0-155">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc4c0-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc4c0-156">Requirements</span></span>



| <span data-ttu-id="bc4c0-157">需求</span><span class="sxs-lookup"><span data-stu-id="bc4c0-157">Requirement</span></span> | <span data-ttu-id="bc4c0-158">值</span><span class="sxs-lookup"><span data-stu-id="bc4c0-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc4c0-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc4c0-159">Minimum supported client</span></span><br/> | <span data-ttu-id="bc4c0-160">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc4c0-160">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bc4c0-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc4c0-161">Minimum supported server</span></span><br/> | <span data-ttu-id="bc4c0-162">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc4c0-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bc4c0-163">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="bc4c0-163">End of client support</span></span><br/>    | <span data-ttu-id="bc4c0-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bc4c0-164">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bc4c0-165">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="bc4c0-165">End of server support</span></span><br/>    | <span data-ttu-id="bc4c0-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bc4c0-166">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bc4c0-167">標頭</span><span class="sxs-lookup"><span data-stu-id="bc4c0-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc4c0-168"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-168"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc4c0-169">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bc4c0-169">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc4c0-170"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-170"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bc4c0-171">DLL</span><span class="sxs-lookup"><span data-stu-id="bc4c0-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc4c0-172"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc4c0-172"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc4c0-173">IID</span><span class="sxs-lookup"><span data-stu-id="bc4c0-173">IID</span></span><br/>                      | <span data-ttu-id="bc4c0-174">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bc4c0-174">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="bc4c0-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc4c0-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc4c0-176">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="bc4c0-176">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
