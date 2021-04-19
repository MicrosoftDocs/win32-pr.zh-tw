---
description: FindCard 方法會搜尋智慧卡，並對其開啟有效的連接。
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'ISCardLocate：： FindCard 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf3cf05ff6e6040d5cac2bde161fa2eea07d5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975074"
---
# <a name="iscardlocatefindcard-method"></a><span data-ttu-id="dc35d-103">ISCardLocate：： FindCard 方法</span><span class="sxs-lookup"><span data-stu-id="dc35d-103">ISCardLocate::FindCard method</span></span>

<span data-ttu-id="dc35d-104">\[**FindCard** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="dc35d-104">\[The **FindCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dc35d-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="dc35d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dc35d-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="dc35d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dc35d-107">**FindCard** 方法會搜尋 [*智慧卡*](../secgloss/s-gly.md)，並對其開啟有效的連接。</span><span class="sxs-lookup"><span data-stu-id="dc35d-107">The **FindCard** method searches for the [*smart card*](../secgloss/s-gly.md) and opens a valid connection to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc35d-108">語法</span><span class="sxs-lookup"><span data-stu-id="dc35d-108">Syntax</span></span>


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a><span data-ttu-id="dc35d-109">參數</span><span class="sxs-lookup"><span data-stu-id="dc35d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc35d-110">*ShareMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc35d-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc35d-111">當開啟連接時，要在其中共用或不共用智慧卡的模式。</span><span class="sxs-lookup"><span data-stu-id="dc35d-111">Mode in which to share or not share the smart card when a connection is opened to it.</span></span>



| <span data-ttu-id="dc35d-112">值</span><span class="sxs-lookup"><span data-stu-id="dc35d-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="dc35d-113">意義</span><span class="sxs-lookup"><span data-stu-id="dc35d-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="dc35d-114"><dt>**獨家**</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="dc35d-115">沒有其他人使用此智慧卡連線。</span><span class="sxs-lookup"><span data-stu-id="dc35d-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="dc35d-116"><dt>**共用**</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="dc35d-117">其他應用程式可以使用此連接。</span><span class="sxs-lookup"><span data-stu-id="dc35d-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="dc35d-118">*通訊協定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc35d-118">*Protocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc35d-119">連接到卡片時要使用的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="dc35d-119">Protocol to use when connecting to the card.</span></span>

<span data-ttu-id="dc35d-120">T0</span><span class="sxs-lookup"><span data-stu-id="dc35d-120">T0</span></span>

<span data-ttu-id="dc35d-121">T1</span><span class="sxs-lookup"><span data-stu-id="dc35d-121">T1</span></span>

<span data-ttu-id="dc35d-122">RAW</span><span class="sxs-lookup"><span data-stu-id="dc35d-122">RAW</span></span>

<span data-ttu-id="dc35d-123">T0 \| T1</span><span class="sxs-lookup"><span data-stu-id="dc35d-123">T0\|T1</span></span>

</dd> <dt>

<span data-ttu-id="dc35d-124">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc35d-124">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc35d-125">指定何時顯示 [*使用者介面*](../secgloss/u-gly.md) ：</span><span class="sxs-lookup"><span data-stu-id="dc35d-125">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed:</span></span>



| <span data-ttu-id="dc35d-126">值</span><span class="sxs-lookup"><span data-stu-id="dc35d-126">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="dc35d-127">意義</span><span class="sxs-lookup"><span data-stu-id="dc35d-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="dc35d-128"><dt>**SC \_ DLG \_ 基本 \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-128"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="dc35d-129">只有在呼叫的應用程式所搜尋的卡片找不到且無法在讀取器中使用時，才會顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="dc35d-129">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="dc35d-130">如此一來，就可以透過內部對話方塊機制或使用) 的使用者回呼函式，以及傳回給呼叫的應用程式，來找出卡片、連接 (。</span><span class="sxs-lookup"><span data-stu-id="dc35d-130">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="dc35d-131"><dt>**SC \_ D \_ 沒有 \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-131"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="dc35d-132">不論搜尋結果為何，都不會顯示任何 UI。</span><span class="sxs-lookup"><span data-stu-id="dc35d-132">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="dc35d-133"><dt>**SC \_ DLG \_ FORCE \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-133"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="dc35d-134">不論搜尋結果為何，都會顯示 UI。</span><span class="sxs-lookup"><span data-stu-id="dc35d-134">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="dc35d-135">*ppCardInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dc35d-135">*ppCardInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc35d-136">指向資料結構指標的指標，該結構包含或傳回已開啟 [*智慧卡*](../secgloss/s-gly.md)的相關資訊（如果成功）。</span><span class="sxs-lookup"><span data-stu-id="dc35d-136">Pointer to a pointer to a data structure that contains or returns information about the opened [*smart card*](../secgloss/s-gly.md), if successful.</span></span> <span data-ttu-id="dc35d-137">如果作業失敗，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="dc35d-137">Will be **NULL** if operation has failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc35d-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc35d-138">Return value</span></span>

<span data-ttu-id="dc35d-139">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="dc35d-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="dc35d-140">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dc35d-140">Return code</span></span>                                                                                   | <span data-ttu-id="dc35d-141">Description</span><span class="sxs-lookup"><span data-stu-id="dc35d-141">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="dc35d-142"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dc35d-143">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="dc35d-143">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="dc35d-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dc35d-145">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="dc35d-145">Invalid parameter.</span></span><br/>                        |
| <dl> <span data-ttu-id="dc35d-146"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dc35d-147">在 *ppCardInfo* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="dc35d-147">A bad pointer was passed in *ppCardInfo*.</span></span><br/> |
| <dl> <span data-ttu-id="dc35d-148"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dc35d-149">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="dc35d-149">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="dc35d-150">備註</span><span class="sxs-lookup"><span data-stu-id="dc35d-150">Remarks</span></span>

<span data-ttu-id="dc35d-151">若要設定搜尋的搜尋條件，請呼叫 [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) 來指定智慧卡的卡片名稱。</span><span class="sxs-lookup"><span data-stu-id="dc35d-151">To set the search criteria of the search, call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to specify a smart card's card names.</span></span>

<span data-ttu-id="dc35d-152">如需此介面所提供的所有方法清單，請參閱 [**ISCardLocate**](iscardlocate.md)。</span><span class="sxs-lookup"><span data-stu-id="dc35d-152">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="dc35d-153">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dc35d-153">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="dc35d-154">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="dc35d-154">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc35d-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc35d-155">Requirements</span></span>



| <span data-ttu-id="dc35d-156">需求</span><span class="sxs-lookup"><span data-stu-id="dc35d-156">Requirement</span></span> | <span data-ttu-id="dc35d-157">值</span><span class="sxs-lookup"><span data-stu-id="dc35d-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc35d-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc35d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="dc35d-159">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc35d-159">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dc35d-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc35d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="dc35d-161">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc35d-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc35d-162">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="dc35d-162">End of client support</span></span><br/>    | <span data-ttu-id="dc35d-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc35d-163">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dc35d-164">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="dc35d-164">End of server support</span></span><br/>    | <span data-ttu-id="dc35d-165">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc35d-165">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dc35d-166">標頭</span><span class="sxs-lookup"><span data-stu-id="dc35d-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc35d-167"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-167"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc35d-168">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="dc35d-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc35d-169"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-169"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc35d-170">DLL</span><span class="sxs-lookup"><span data-stu-id="dc35d-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc35d-171"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc35d-171"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dc35d-172">IID</span><span class="sxs-lookup"><span data-stu-id="dc35d-172">IID</span></span><br/>                      | <span data-ttu-id="dc35d-173">IID \_ ISCardLocate 定義為1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="dc35d-173">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="dc35d-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc35d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc35d-175">**ConfigureCardNameSearch**</span><span class="sxs-lookup"><span data-stu-id="dc35d-175">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[<span data-ttu-id="dc35d-176">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="dc35d-176">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
