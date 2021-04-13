---
description: 建立應用程式協定資料單位 (APDU) 命令，有條件地更新安全性狀態，並在智慧卡不信任時驗證電腦的身分識別。
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'ISCardISO7816：： ExternalAuthenticate 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386170"
---
# <a name="iscardiso7816externalauthenticate-method"></a><span data-ttu-id="b4069-103">ISCardISO7816：： ExternalAuthenticate 方法</span><span class="sxs-lookup"><span data-stu-id="b4069-103">ISCardISO7816::ExternalAuthenticate method</span></span>

<span data-ttu-id="b4069-104">\[**ExternalAuthenticate** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="b4069-104">\[The **ExternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b4069-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="b4069-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b4069-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="b4069-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b4069-107">**ExternalAuthenticate** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，有條件地更新安全性狀態，並在 [*智慧卡*](../secgloss/s-gly.md)不信任時驗證電腦的身分識別。</span><span class="sxs-lookup"><span data-stu-id="b4069-107">The **ExternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that conditionally updates security status, verifying the identity of the computer when the [*smart card*](../secgloss/s-gly.md) does not trust it.</span></span>

<span data-ttu-id="b4069-108">此命令會 (依據卡片先前發出的挑戰，使用 (yes 或 no) 計算的結果，例如，INS 會 \_ 取得 \_ 挑戰命令) 、金鑰 (可能秘密) 儲存在卡片中，以及由介面裝置傳輸的驗證資料。</span><span class="sxs-lookup"><span data-stu-id="b4069-108">The command uses the result (yes or no) of the computation by the card (based on a challenge previously issued by the card, for example, by the INS\_GET\_CHALLENGE command), a key (possibly secret) stored in the card, and authentication data transmitted by the interface device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4069-109">語法</span><span class="sxs-lookup"><span data-stu-id="b4069-109">Syntax</span></span>


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="b4069-110">參數</span><span class="sxs-lookup"><span data-stu-id="b4069-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4069-111">*byAlgorithmRef* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4069-111">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4069-112">卡片中的演算法參考。</span><span class="sxs-lookup"><span data-stu-id="b4069-112">The reference of the algorithm in the card.</span></span>

<span data-ttu-id="b4069-113">如果此值為零，則表示未提供任何資訊。</span><span class="sxs-lookup"><span data-stu-id="b4069-113">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="b4069-114">在發出命令或在資料欄位中提供演算法的參考時，可以知道演算法的參考。</span><span class="sxs-lookup"><span data-stu-id="b4069-114">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="b4069-115">*bySecretRef* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4069-115">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4069-116">秘密的參考。</span><span class="sxs-lookup"><span data-stu-id="b4069-116">The reference of the secret.</span></span>



| <span data-ttu-id="b4069-117">值</span><span class="sxs-lookup"><span data-stu-id="b4069-117">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="b4069-118">意義</span><span class="sxs-lookup"><span data-stu-id="b4069-118">Meaning</span></span>                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="b4069-119"><dt>**沒有資訊**</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-119"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="b4069-120">位位置：00000000</span><span class="sxs-lookup"><span data-stu-id="b4069-120">Bit position: 00000000</span></span><br/> <span data-ttu-id="b4069-121">未提供任何資訊。</span><span class="sxs-lookup"><span data-stu-id="b4069-121">No information is given.</span></span> <span data-ttu-id="b4069-122">在發出命令或在 [資料] 欄位中提供秘密的參考時，就會知道秘密的參考。</span><span class="sxs-lookup"><span data-stu-id="b4069-122">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="b4069-123"><dt>**全域參考**</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-123"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="b4069-124">位位置： 0-------</span><span class="sxs-lookup"><span data-stu-id="b4069-124">Bit position: 0-------</span></span><br/> <span data-ttu-id="b4069-125">全域參考資料 () 的 MF 特定金鑰。</span><span class="sxs-lookup"><span data-stu-id="b4069-125">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="b4069-126"><dt>**特定參考**</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-126"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="b4069-127">位位置： 1-------</span><span class="sxs-lookup"><span data-stu-id="b4069-127">Bit position: 1-------</span></span><br/> <span data-ttu-id="b4069-128">特定的參考資料 () 的 DF 特定索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b4069-128">Specific reference data (a DF specific key).</span></span><br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="b4069-129"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-129"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="b4069-130">位位置：-xx-----</span><span class="sxs-lookup"><span data-stu-id="b4069-130">Bit position: -xx-----</span></span><br/> <span data-ttu-id="b4069-131">00 (其他值為 RFU) 。</span><span class="sxs-lookup"><span data-stu-id="b4069-131">00 (other values are RFU).</span></span><br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="b4069-132"><dt>**秘密**</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-132"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="b4069-133">位位置：---xxxxx</span><span class="sxs-lookup"><span data-stu-id="b4069-133">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="b4069-134">秘密的數目。</span><span class="sxs-lookup"><span data-stu-id="b4069-134">Number of the secret.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="b4069-135">*pChallenge* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4069-135">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4069-136">驗證相關資料的指標。</span><span class="sxs-lookup"><span data-stu-id="b4069-136">A pointer to the authentication-related data.</span></span> <span data-ttu-id="b4069-137">這個參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4069-137">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b4069-138">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b4069-138">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4069-139">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b4069-139">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="b4069-140">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="b4069-140">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="b4069-141">如果 *ppCmd* 設定為 **Null**，就會使用 *ppCmd* 指標在內部建立和傳回 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md)物件。</span><span class="sxs-lookup"><span data-stu-id="b4069-141">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4069-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4069-142">Return value</span></span>

<span data-ttu-id="b4069-143">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="b4069-143">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b4069-144">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b4069-144">Return code</span></span>                                                                                   | <span data-ttu-id="b4069-145">Description</span><span class="sxs-lookup"><span data-stu-id="b4069-145">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="b4069-146"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-146"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b4069-147">作業已成功完成。</span><span class="sxs-lookup"><span data-stu-id="b4069-147">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="b4069-148"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-148"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b4069-149">傳遞的參數無效。</span><span class="sxs-lookup"><span data-stu-id="b4069-149">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="b4069-150"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-150"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b4069-151">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="b4069-151">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="b4069-152"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-152"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b4069-153">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="b4069-153">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="b4069-154">備註</span><span class="sxs-lookup"><span data-stu-id="b4069-154">Remarks</span></span>

<span data-ttu-id="b4069-155">為了讓封裝的命令成功，從卡片取得的最後一項挑戰必須是有效的。</span><span class="sxs-lookup"><span data-stu-id="b4069-155">For the encapsulated command to be successful, the last challenge obtained from the card must be valid.</span></span>

<span data-ttu-id="b4069-156">失敗的比較可能會記錄在卡片 (例如，以限制使用參考資料) 的進一步嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="b4069-156">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="b4069-157">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="b4069-157">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="b4069-158">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b4069-158">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b4069-159">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="b4069-159">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4069-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4069-160">Requirements</span></span>



| <span data-ttu-id="b4069-161">需求</span><span class="sxs-lookup"><span data-stu-id="b4069-161">Requirement</span></span> | <span data-ttu-id="b4069-162">值</span><span class="sxs-lookup"><span data-stu-id="b4069-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4069-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4069-163">Minimum supported client</span></span><br/> | <span data-ttu-id="b4069-164">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4069-164">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b4069-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4069-165">Minimum supported server</span></span><br/> | <span data-ttu-id="b4069-166">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4069-166">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b4069-167">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b4069-167">End of client support</span></span><br/>    | <span data-ttu-id="b4069-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4069-168">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b4069-169">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="b4069-169">End of server support</span></span><br/>    | <span data-ttu-id="b4069-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4069-170">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b4069-171">標頭</span><span class="sxs-lookup"><span data-stu-id="b4069-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4069-172"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-172"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4069-173">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b4069-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4069-174"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-174"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b4069-175">DLL</span><span class="sxs-lookup"><span data-stu-id="b4069-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4069-176"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4069-176"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b4069-177">IID</span><span class="sxs-lookup"><span data-stu-id="b4069-177">IID</span></span><br/>                      | <span data-ttu-id="b4069-178">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b4069-178">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="b4069-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4069-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4069-180">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="b4069-180">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="b4069-181">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="b4069-181">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
