---
description: ConfigureCardNameSearch 方法會指定要在智慧卡搜尋中使用的卡片名稱。
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'ISCardLocate：： ConfigureCardNameSearch 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193278"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a><span data-ttu-id="071b1-103">ISCardLocate：： ConfigureCardNameSearch 方法</span><span class="sxs-lookup"><span data-stu-id="071b1-103">ISCardLocate::ConfigureCardNameSearch method</span></span>

<span data-ttu-id="071b1-104">\[**ConfigureCardNameSearch** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="071b1-104">\[The **ConfigureCardNameSearch** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="071b1-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="071b1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="071b1-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="071b1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="071b1-107">**ConfigureCardNameSearch** 方法會指定要在 [*智慧卡*](../secgloss/s-gly.md)搜尋中使用的卡片名稱。</span><span class="sxs-lookup"><span data-stu-id="071b1-107">The **ConfigureCardNameSearch** method specifies the card names to be used in the search for the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="071b1-108">語法</span><span class="sxs-lookup"><span data-stu-id="071b1-108">Syntax</span></span>


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="071b1-109">參數</span><span class="sxs-lookup"><span data-stu-id="071b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="071b1-110">*pCardNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="071b1-110">*pCardNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="071b1-111">以 BSTR 形式的卡片名稱之 Automation 安全陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="071b1-111">A pointer to an Automation safe array of card names in BSTR form.</span></span>

</dd> <dt>

<span data-ttu-id="071b1-112">*pGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="071b1-112">*pGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="071b1-113">以 BSTR 形式的「卡片/讀者」群組名稱的自動化安全陣列指標，可新增至搜尋。</span><span class="sxs-lookup"><span data-stu-id="071b1-113">A pointer to an Automation safe array of names of card/reader groups in BSTR form to add to the search.</span></span>

</dd> <dt>

<span data-ttu-id="071b1-114">*bstrTitle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="071b1-114">*bstrTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="071b1-115">搜尋通用控制項的對話方塊標題。</span><span class="sxs-lookup"><span data-stu-id="071b1-115">Dialog box title for the search common control.</span></span>

</dd> <dt>

<span data-ttu-id="071b1-116">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="071b1-116">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="071b1-117">指定何時顯示 [*使用者介面*](../secgloss/u-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="071b1-117">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed.</span></span>



| <span data-ttu-id="071b1-118">值</span><span class="sxs-lookup"><span data-stu-id="071b1-118">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="071b1-119">意義</span><span class="sxs-lookup"><span data-stu-id="071b1-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="071b1-120"><dt>**SC \_ DLG \_ 基本 \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="071b1-120"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="071b1-121">只有在呼叫的應用程式所搜尋的卡片找不到且無法在讀取器中使用時，才會顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="071b1-121">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="071b1-122">如此一來，就可以透過內部對話方塊機制或使用) 的使用者回呼函式，以及傳回給呼叫的應用程式，來找出卡片、連接 (。</span><span class="sxs-lookup"><span data-stu-id="071b1-122">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="071b1-123"><dt>**SC \_ D \_ 沒有 \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="071b1-123"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="071b1-124">不論搜尋結果為何，都不會顯示任何 UI。</span><span class="sxs-lookup"><span data-stu-id="071b1-124">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="071b1-125"><dt>**SC \_ DLG \_ FORCE \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="071b1-125"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="071b1-126">不論搜尋結果為何，都會顯示 UI。</span><span class="sxs-lookup"><span data-stu-id="071b1-126">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="071b1-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="071b1-127">Return value</span></span>

<span data-ttu-id="071b1-128">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="071b1-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="071b1-129">傳回碼</span><span class="sxs-lookup"><span data-stu-id="071b1-129">Return code</span></span>                                                                                   | <span data-ttu-id="071b1-130">Description</span><span class="sxs-lookup"><span data-stu-id="071b1-130">Description</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="071b1-131"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="071b1-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="071b1-132">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="071b1-132">Operation completed successfully.</span></span><br/>                          |
| <dl> <span data-ttu-id="071b1-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="071b1-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="071b1-134">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="071b1-134">Invalid parameter.</span></span><br/>                                         |
| <dl> <span data-ttu-id="071b1-135"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="071b1-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="071b1-136">在 *pCardNames* 或 *pGroupNames* 中傳遞了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="071b1-136">A bad pointer was passed in *pCardNames* or *pGroupNames*.</span></span><br/> |
| <dl> <span data-ttu-id="071b1-137"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="071b1-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="071b1-138">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="071b1-138">Out of memory.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="071b1-139">備註</span><span class="sxs-lookup"><span data-stu-id="071b1-139">Remarks</span></span>

<span data-ttu-id="071b1-140">若要找出 [*智慧卡*](../secgloss/s-gly.md)，請呼叫 [**FindCard**](iscardlocate-findcard.md)。</span><span class="sxs-lookup"><span data-stu-id="071b1-140">To locate the [*smart card*](../secgloss/s-gly.md), call [**FindCard**](iscardlocate-findcard.md).</span></span>

<span data-ttu-id="071b1-141">如需此介面所提供的所有方法清單，請參閱 [**ISCardLocate**](iscardlocate.md)。</span><span class="sxs-lookup"><span data-stu-id="071b1-141">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="071b1-142">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="071b1-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="071b1-143">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="071b1-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="071b1-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="071b1-144">Requirements</span></span>



| <span data-ttu-id="071b1-145">需求</span><span class="sxs-lookup"><span data-stu-id="071b1-145">Requirement</span></span> | <span data-ttu-id="071b1-146">值</span><span class="sxs-lookup"><span data-stu-id="071b1-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="071b1-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="071b1-147">Minimum supported client</span></span><br/> | <span data-ttu-id="071b1-148">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="071b1-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="071b1-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="071b1-149">Minimum supported server</span></span><br/> | <span data-ttu-id="071b1-150">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="071b1-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="071b1-151">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="071b1-151">End of client support</span></span><br/>    | <span data-ttu-id="071b1-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="071b1-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="071b1-153">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="071b1-153">End of server support</span></span><br/>    | <span data-ttu-id="071b1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="071b1-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="071b1-155">標頭</span><span class="sxs-lookup"><span data-stu-id="071b1-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="071b1-156"><dt>Scardmgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="071b1-156"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="071b1-157">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="071b1-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="071b1-158"><dt>Scardmgr .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="071b1-158"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="071b1-159">DLL</span><span class="sxs-lookup"><span data-stu-id="071b1-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="071b1-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="071b1-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="071b1-161">IID</span><span class="sxs-lookup"><span data-stu-id="071b1-161">IID</span></span><br/>                      | <span data-ttu-id="071b1-162">IID \_ ISCardLocate 定義為1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="071b1-162">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="071b1-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="071b1-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="071b1-164">**FindCard**</span><span class="sxs-lookup"><span data-stu-id="071b1-164">**FindCard**</span></span>](iscardlocate-findcard.md)
</dt> <dt>

[<span data-ttu-id="071b1-165">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="071b1-165">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
