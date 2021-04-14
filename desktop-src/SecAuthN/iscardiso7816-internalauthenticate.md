---
description: 建立應用程式協定資料單位 (APDU) 命令，此命令會使用從介面裝置送出的挑戰資料和相關的秘密 (（例如，儲存在卡片中的金鑰) ）來起始卡片的驗證資料計算。
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'ISCardISO7816：： InternalAuthenticate 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1e30dbb06373907c5cea07e45d4f7a390b773349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026555"
---
# <a name="iscardiso7816internalauthenticate-method"></a><span data-ttu-id="58588-103">ISCardISO7816：： InternalAuthenticate 方法</span><span class="sxs-lookup"><span data-stu-id="58588-103">ISCardISO7816::InternalAuthenticate method</span></span>

<span data-ttu-id="58588-104">\[**InternalAuthenticate** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="58588-104">\[The **InternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="58588-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="58588-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="58588-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="58588-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="58588-107">**InternalAuthenticate** 方法會建立 [*應用程式協定資料單位*](../secgloss/a-gly.md) (APDU) 命令，此命令會使用從介面裝置送出的挑戰資料和相關的秘密 (（例如，儲存在卡片中的金鑰) ）來起始卡片的驗證資料計算。</span><span class="sxs-lookup"><span data-stu-id="58588-107">The **InternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the computation of the authentication data by the card using the challenge data sent from the interface device and a relevant secret (for example, a key) stored in the card.</span></span>

<span data-ttu-id="58588-108">當相關的秘密附加至 MF 時，命令可能會用來驗證整個卡片。</span><span class="sxs-lookup"><span data-stu-id="58588-108">When the relevant secret is attached to the MF, the command may be used to authenticate the card as a whole.</span></span>

<span data-ttu-id="58588-109">當相關的秘密附加至另一個 DF 時，命令可用來驗證該 DF。</span><span class="sxs-lookup"><span data-stu-id="58588-109">When the relevant secret is attached to another DF, the command may be used to authenticate that DF.</span></span>

## <a name="syntax"></a><span data-ttu-id="58588-110">語法</span><span class="sxs-lookup"><span data-stu-id="58588-110">Syntax</span></span>


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="58588-111">參數</span><span class="sxs-lookup"><span data-stu-id="58588-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58588-112">*byAlgorithmRef* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58588-112">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58588-113">卡片中的演算法參考。</span><span class="sxs-lookup"><span data-stu-id="58588-113">Reference of the algorithm in the card.</span></span>

<span data-ttu-id="58588-114">如果此值為零，則表示未提供任何資訊。</span><span class="sxs-lookup"><span data-stu-id="58588-114">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="58588-115">在發出命令或在資料欄位中提供演算法的參考時，可以知道演算法的參考。</span><span class="sxs-lookup"><span data-stu-id="58588-115">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="58588-116">*bySecretRef* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58588-116">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58588-117">秘密的參考。</span><span class="sxs-lookup"><span data-stu-id="58588-117">Reference of the secret.</span></span>



| <span data-ttu-id="58588-118">值</span><span class="sxs-lookup"><span data-stu-id="58588-118">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="58588-119">意義</span><span class="sxs-lookup"><span data-stu-id="58588-119">Meaning</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="58588-120"><dt>**沒有資訊**</dt></span><span class="sxs-lookup"><span data-stu-id="58588-120"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="58588-121">位位置：00000000</span><span class="sxs-lookup"><span data-stu-id="58588-121">Bit position: 00000000</span></span> <br/> <span data-ttu-id="58588-122">未提供任何資訊。</span><span class="sxs-lookup"><span data-stu-id="58588-122">No information is given.</span></span> <span data-ttu-id="58588-123">在發出命令或在 [資料] 欄位中提供秘密的參考時，就會知道秘密的參考。</span><span class="sxs-lookup"><span data-stu-id="58588-123">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="58588-124"><dt>**全域參考**</dt></span><span class="sxs-lookup"><span data-stu-id="58588-124"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="58588-125">位位置： 0-------</span><span class="sxs-lookup"><span data-stu-id="58588-125">Bit position: 0-------</span></span> <br/> <span data-ttu-id="58588-126">全域參考資料 () 的 MF 特定金鑰。</span><span class="sxs-lookup"><span data-stu-id="58588-126">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="58588-127"><dt>**特定參考**</dt></span><span class="sxs-lookup"><span data-stu-id="58588-127"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="58588-128">位位置： 1-------</span><span class="sxs-lookup"><span data-stu-id="58588-128">Bit position: 1-------</span></span><br/> <span data-ttu-id="58588-129">特定的參考資料 () 的 DF 特定索引鍵。</span><span class="sxs-lookup"><span data-stu-id="58588-129">Specific reference data (a DF specific key).</span></span><br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="58588-130"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="58588-130"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="58588-131">位位置：-xx-----</span><span class="sxs-lookup"><span data-stu-id="58588-131">Bit position: -xx-----</span></span><br/> <span data-ttu-id="58588-132">00 (其他值為 RFU) 。</span><span class="sxs-lookup"><span data-stu-id="58588-132">00 (other values are RFU).</span></span><br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="58588-133"><dt>**秘密**</dt></span><span class="sxs-lookup"><span data-stu-id="58588-133"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="58588-134">位位置：---xxxxx</span><span class="sxs-lookup"><span data-stu-id="58588-134">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="58588-135">秘密的數目。</span><span class="sxs-lookup"><span data-stu-id="58588-135">Number of the secret.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="58588-136">*pChallenge* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58588-136">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58588-137">驗證相關資料的指標 (例如，挑戰) 。</span><span class="sxs-lookup"><span data-stu-id="58588-137">Pointer to the authentication-related data (for example, challenge).</span></span>

</dd> <dt>

<span data-ttu-id="58588-138">*lReplyBytes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="58588-138">*lReplyBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58588-139">回應中預期的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="58588-139">Maximum number of bytes expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="58588-140">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="58588-140">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="58588-141">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="58588-141">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="58588-142">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="58588-142">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="58588-143">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並使用 *ppCmd* 指標來傳回。</span><span class="sxs-lookup"><span data-stu-id="58588-143">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58588-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="58588-144">Return value</span></span>

<span data-ttu-id="58588-145">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="58588-145">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="58588-146">傳回碼</span><span class="sxs-lookup"><span data-stu-id="58588-146">Return code</span></span>                                                                                   | <span data-ttu-id="58588-147">Description</span><span class="sxs-lookup"><span data-stu-id="58588-147">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="58588-148"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="58588-148"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="58588-149">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="58588-149">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="58588-150"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="58588-150"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="58588-151">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="58588-151">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="58588-152"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="58588-152"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="58588-153">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="58588-153">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="58588-154"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="58588-154"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="58588-155">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="58588-155">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="58588-156">備註</span><span class="sxs-lookup"><span data-stu-id="58588-156">Remarks</span></span>

<span data-ttu-id="58588-157">成功執行命令可能會受到先前命令的成功完成 (例如，確認或選取檔案) 或選取 (例如) 相關的秘密。</span><span class="sxs-lookup"><span data-stu-id="58588-157">The successful execution of the command may be subject to successful completion of prior commands (for example, VERIFY or SELECT FILE) or selections (for example, the relevant secret).</span></span>

<span data-ttu-id="58588-158">如果在發出命令時目前已選取金鑰和演算法，則命令可以隱含地使用金鑰和演算法。</span><span class="sxs-lookup"><span data-stu-id="58588-158">If a key and an algorithm are currently selected when issuing the command, then the command may implicitly use the key and the algorithm.</span></span>

<span data-ttu-id="58588-159">發出命令的次數可能會記錄在卡片中，以限制使用相關密碼或演算法的進一步嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="58588-159">The number of times the command is issued may be recorded in the card to limit the number of further attempts of using the relevant secret or the algorithm.</span></span>

<span data-ttu-id="58588-160">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="58588-160">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="58588-161">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="58588-161">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="58588-162">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="58588-162">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58588-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="58588-163">Requirements</span></span>



| <span data-ttu-id="58588-164">需求</span><span class="sxs-lookup"><span data-stu-id="58588-164">Requirement</span></span> | <span data-ttu-id="58588-165">值</span><span class="sxs-lookup"><span data-stu-id="58588-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58588-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58588-166">Minimum supported client</span></span><br/> | <span data-ttu-id="58588-167">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58588-167">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="58588-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58588-168">Minimum supported server</span></span><br/> | <span data-ttu-id="58588-169">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58588-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58588-170">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="58588-170">End of client support</span></span><br/>    | <span data-ttu-id="58588-171">Windows XP</span><span class="sxs-lookup"><span data-stu-id="58588-171">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="58588-172">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="58588-172">End of server support</span></span><br/>    | <span data-ttu-id="58588-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="58588-173">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="58588-174">標頭</span><span class="sxs-lookup"><span data-stu-id="58588-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="58588-175"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="58588-175"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="58588-176">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="58588-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="58588-177"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="58588-177"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="58588-178">DLL</span><span class="sxs-lookup"><span data-stu-id="58588-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58588-179"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58588-179"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="58588-180">IID</span><span class="sxs-lookup"><span data-stu-id="58588-180">IID</span></span><br/>                      | <span data-ttu-id="58588-181">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="58588-181">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="58588-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58588-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58588-183">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="58588-183">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="58588-184">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="58588-184">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
