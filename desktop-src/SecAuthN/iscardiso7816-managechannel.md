---
description: ManageChannel 方法會在開啟和關閉邏輯通道 (APDU) 命令中，建立應用程式協定資料單位。
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'ISCardISO7816：： ManageChannel 方法 (Scardssp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026554"
---
# <a name="iscardiso7816managechannel-method"></a><span data-ttu-id="47948-103">ISCardISO7816：： ManageChannel 方法</span><span class="sxs-lookup"><span data-stu-id="47948-103">ISCardISO7816::ManageChannel method</span></span>

<span data-ttu-id="47948-104">\[**ManageChannel** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="47948-104">\[The **ManageChannel** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="47948-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="47948-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="47948-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="47948-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="47948-107">**ManageChannel** 方法會在開啟和關閉邏輯通道 (APDU) 命令中，建立 [*應用程式協定資料單位*](../secgloss/a-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="47948-107">The **ManageChannel** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that opens and closes logical channels.</span></span>

<span data-ttu-id="47948-108">Open 函式會開啟基礎以外的新邏輯通道。</span><span class="sxs-lookup"><span data-stu-id="47948-108">The open function opens a new logical channel other than the basic one.</span></span> <span data-ttu-id="47948-109">系統會提供卡片的選項，以指派邏輯頻道號碼，或提供給卡片的邏輯通道編號。</span><span class="sxs-lookup"><span data-stu-id="47948-109">Options are provided for the card to assign a logical channel number, or for the logical channel number to be supplied to the card.</span></span>

<span data-ttu-id="47948-110">Close 函式會明確地關閉非基本的邏輯通道。</span><span class="sxs-lookup"><span data-stu-id="47948-110">The close function explicitly closes a logical channel other than the basic one.</span></span> <span data-ttu-id="47948-111">成功關閉之後，邏輯通道應該可供重複使用。</span><span class="sxs-lookup"><span data-stu-id="47948-111">After the successful closing, the logical channel shall be available for re-use.</span></span>

## <a name="syntax"></a><span data-ttu-id="47948-112">語法</span><span class="sxs-lookup"><span data-stu-id="47948-112">Syntax</span></span>


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="47948-113">參數</span><span class="sxs-lookup"><span data-stu-id="47948-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47948-114">*byChannelState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47948-114">*byChannelState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47948-115">P1 的 Bit b8 可用來指出 open 函式或 close 函數;如果 b8 為0，則管理通道應該會開啟邏輯通道，如果 b8 是1，則管理通道應該會關閉邏輯通道：</span><span class="sxs-lookup"><span data-stu-id="47948-115">Bit b8 of P1 is used to indicate the open function or the close function; if b8 is 0, then MANAGE CHANNEL shall open a logical channel and if b8 is 1, then MANAGE CHANNEL shall close a logical channel:</span></span>

<span data-ttu-id="47948-116">P1 = 要開啟的 ' 00 '</span><span class="sxs-lookup"><span data-stu-id="47948-116">P1 = '00' to open</span></span>

<span data-ttu-id="47948-117">P1 = ' 80 ' 表示關閉</span><span class="sxs-lookup"><span data-stu-id="47948-117">P1 = '80' to close</span></span>

<span data-ttu-id="47948-118">其他值為 RFU</span><span class="sxs-lookup"><span data-stu-id="47948-118">Other values are RFU</span></span>

</dd> <dt>

<span data-ttu-id="47948-119">*byChannel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47948-119">*byChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47948-120">針對開啟的函式 (P1 = ' 00 ' ) ，P2 的位 b1 和 b2 會用來以類別位元組中的相同方式來撰寫邏輯通道編號的程式碼，而 P2 的其他位則是 RFU。</span><span class="sxs-lookup"><span data-stu-id="47948-120">For the open function (P1 = '00'), the bits b1 and b2 of P2 are used to code the logical channel number in the same manner as in the class byte, the other bits of P2 are RFU.</span></span>

<span data-ttu-id="47948-121">當 P2 的 b1 和 b2 是 **Null** 時，卡片會指派將會在資料欄位的位 b1 和 b2 中傳回的邏輯通道編號。</span><span class="sxs-lookup"><span data-stu-id="47948-121">When b1 and b2 of P2 are **NULL**, then the card will assign a logical channel number that will be returned in bits b1 and b2 of the data field.</span></span>

<span data-ttu-id="47948-122">當 P2 的 b1 和/或 b2 不是 **Null** 時，它們會以非基本的邏輯通道編號進行編碼;然後，卡片會開啟外部指派的邏輯頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="47948-122">When b1 and/or b2 of P2 are not **NULL**, they code a logical channel number other than the basic one; then the card will open the externally assigned logical channel number.</span></span>

</dd> <dt>

<span data-ttu-id="47948-123">*ppCmd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="47948-123">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="47948-124">在輸入時， [**ISCardCmd**](iscardcmd.md) 介面物件的指標或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="47948-124">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="47948-125">傳回時，它會填入由這項作業所建立的 APDU 命令。</span><span class="sxs-lookup"><span data-stu-id="47948-125">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="47948-126">如果 *ppCmd* 設定為 **Null**，就會在內部建立 [*智慧卡*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) 物件，並使用 *ppCmd* 指標來傳回。</span><span class="sxs-lookup"><span data-stu-id="47948-126">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47948-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="47948-127">Return value</span></span>

<span data-ttu-id="47948-128">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="47948-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="47948-129">傳回碼</span><span class="sxs-lookup"><span data-stu-id="47948-129">Return code</span></span>                                                                                   | <span data-ttu-id="47948-130">Description</span><span class="sxs-lookup"><span data-stu-id="47948-130">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="47948-131"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="47948-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="47948-132">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="47948-132">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="47948-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="47948-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="47948-134">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="47948-134">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="47948-135"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="47948-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="47948-136">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="47948-136">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="47948-137"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="47948-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="47948-138">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="47948-138">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="47948-139">備註</span><span class="sxs-lookup"><span data-stu-id="47948-139">Remarks</span></span>

<span data-ttu-id="47948-140">當開啟的函式從基本邏輯通道成功執行時，應該會以隱含方式選取此 MF 作為目前的 DF，而新邏輯通道的安全性狀態應與 ATR 後的基本邏輯通道相同。</span><span class="sxs-lookup"><span data-stu-id="47948-140">When the open function is successfully performed from the basic logical channel, the MF shall be implicitly selected as the current DF and the security status of the new logical channel should be the same as the basic logical channel after ATR.</span></span> <span data-ttu-id="47948-141">新邏輯通道的安全性狀態應與任何其他邏輯通道的安全性狀態分開。</span><span class="sxs-lookup"><span data-stu-id="47948-141">The security status of the new logical channel should be separate from that of any other logical channel.</span></span>

<span data-ttu-id="47948-142">當開啟的函式從邏輯通道（不是基本通道）成功執行時，系統會選取發出命令之邏輯通道的目前 DF 作為目前的 DF。</span><span class="sxs-lookup"><span data-stu-id="47948-142">When the open function is successfully performed from a logical channel, which is not the basic one, the current DF of the logical channel that issued the command will be selected as the current DF.</span></span> <span data-ttu-id="47948-143">此外，新邏輯通道的安全性狀態應與執行 open 函式之邏輯通道的安全性狀態相同。</span><span class="sxs-lookup"><span data-stu-id="47948-143">In addition, the security status for the new logical channel should be the same as the security status of the logical channel from which the open function was performed.</span></span>

<span data-ttu-id="47948-144">成功關閉函式之後，與此邏輯通道相關的安全性狀態將會遺失。</span><span class="sxs-lookup"><span data-stu-id="47948-144">After a successful close function, the security status related to this logical channel is lost.</span></span>

<span data-ttu-id="47948-145">如需此介面所提供的所有方法清單，請參閱 [**ISCardISO7816**](iscardiso7816.md)。</span><span class="sxs-lookup"><span data-stu-id="47948-145">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="47948-146">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="47948-146">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="47948-147">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="47948-147">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47948-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="47948-148">Requirements</span></span>



| <span data-ttu-id="47948-149">需求</span><span class="sxs-lookup"><span data-stu-id="47948-149">Requirement</span></span> | <span data-ttu-id="47948-150">值</span><span class="sxs-lookup"><span data-stu-id="47948-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47948-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47948-151">Minimum supported client</span></span><br/> | <span data-ttu-id="47948-152">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47948-152">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="47948-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47948-153">Minimum supported server</span></span><br/> | <span data-ttu-id="47948-154">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47948-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47948-155">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="47948-155">End of client support</span></span><br/>    | <span data-ttu-id="47948-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="47948-156">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="47948-157">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="47948-157">End of server support</span></span><br/>    | <span data-ttu-id="47948-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="47948-158">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="47948-159">標頭</span><span class="sxs-lookup"><span data-stu-id="47948-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="47948-160"><dt>Scardssp。h</dt></span><span class="sxs-lookup"><span data-stu-id="47948-160"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="47948-161">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="47948-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="47948-162"><dt>Scardsrv .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="47948-162"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="47948-163">DLL</span><span class="sxs-lookup"><span data-stu-id="47948-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47948-164"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47948-164"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="47948-165">IID</span><span class="sxs-lookup"><span data-stu-id="47948-165">IID</span></span><br/>                      | <span data-ttu-id="47948-166">IID \_ ISCardISO7816 定義為53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="47948-166">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="47948-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47948-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47948-168">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="47948-168">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
