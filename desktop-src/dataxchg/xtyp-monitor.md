---
title: 'XTYP_MONITOR 交易 (Ddeml .h) '
description: 當系統中發生 DDE 事件時，動態資料交換 (DDE) 偵錯工具的 DDE 回呼函式 DdeCallback 接收 XTYP \_ 監視器交易。
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- XTYP_MONITOR 交易資料交換
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384434"
---
# <a name="xtyp_monitor-transaction"></a><span data-ttu-id="fe947-104">XTYP \_ 監視交易</span><span class="sxs-lookup"><span data-stu-id="fe947-104">XTYP\_MONITOR transaction</span></span>

<span data-ttu-id="fe947-105">當系統中發生 DDE 事件時，動態資料交換 (DDE) 偵錯工具的 DDE 回呼函式 [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)接收 **XTYP \_ 監視器** 交易。</span><span class="sxs-lookup"><span data-stu-id="fe947-105">A Dynamic Data Exchange (DDE) debugger's DDE callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_MONITOR** transaction whenever a DDE event occurs in the system.</span></span> <span data-ttu-id="fe947-106">若要接收此交易，應用程式必須在呼叫 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)函式時指定 **APPCLASS \_ 監視器** 值。</span><span class="sxs-lookup"><span data-stu-id="fe947-106">To receive this transaction, an application must specify the **APPCLASS\_MONITOR** value when it calls the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="fe947-107">參數</span><span class="sxs-lookup"><span data-stu-id="fe947-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe947-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="fe947-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="fe947-109">交易類型。</span><span class="sxs-lookup"><span data-stu-id="fe947-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="fe947-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="fe947-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="fe947-111">未使用。</span><span class="sxs-lookup"><span data-stu-id="fe947-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="fe947-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="fe947-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="fe947-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="fe947-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="fe947-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="fe947-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="fe947-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="fe947-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="fe947-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="fe947-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="fe947-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="fe947-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="fe947-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="fe947-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="fe947-119">DDE 物件的控制碼，其中包含有關 DDE 事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="fe947-119">A handle to a DDE object that contains information about the DDE event.</span></span> <span data-ttu-id="fe947-120">應用程式應該使用 [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) 函式來取得物件的指標。</span><span class="sxs-lookup"><span data-stu-id="fe947-120">The application should use the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function to obtain a pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="fe947-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="fe947-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="fe947-122">未使用。</span><span class="sxs-lookup"><span data-stu-id="fe947-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="fe947-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="fe947-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="fe947-124">DDE 事件。</span><span class="sxs-lookup"><span data-stu-id="fe947-124">The DDE event.</span></span> <span data-ttu-id="fe947-125">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fe947-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="fe947-126">值</span><span class="sxs-lookup"><span data-stu-id="fe947-126">Value</span></span>                                                                                                                                                                                                                      | <span data-ttu-id="fe947-127">意義</span><span class="sxs-lookup"><span data-stu-id="fe947-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <span data-ttu-id="fe947-128"><dt>**MF \_回呼**</dt> <dt>0x08000000</dt></span><span class="sxs-lookup"><span data-stu-id="fe947-128"><dt>**MF\_CALLBACKS**</dt> <dt>0x08000000</dt></span></span> </dl> | <span data-ttu-id="fe947-129">系統會將交易傳送至 DDE 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="fe947-129">The system sent a transaction to a DDE callback function.</span></span> <span data-ttu-id="fe947-130">DDE 物件包含 [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) 結構，可提供交易的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fe947-130">The DDE object contains a [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) structure that provides information about the transaction.</span></span><br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <span data-ttu-id="fe947-131"><dt>**MF \_約定**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="fe947-131"><dt>**MF\_CONV**</dt> <dt>0x40000000</dt></span></span> </dl>                | <span data-ttu-id="fe947-132">已建立或終止 DDE 交談。</span><span class="sxs-lookup"><span data-stu-id="fe947-132">A DDE conversation was established or terminated.</span></span> <span data-ttu-id="fe947-133">DDE 物件包含提供交談相關資訊的 [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) 結構。</span><span class="sxs-lookup"><span data-stu-id="fe947-133">The DDE object contains a [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) structure that provides information about the conversation.</span></span><br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <span data-ttu-id="fe947-134"><dt>**MF \_錯誤**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="fe947-134"><dt>**MF\_ERRORS**</dt> <dt>0x10000000</dt></span></span> </dl>          | <span data-ttu-id="fe947-135">發生 DDE 錯誤。</span><span class="sxs-lookup"><span data-stu-id="fe947-135">A DDE error occurred.</span></span> <span data-ttu-id="fe947-136">DDE 物件包含 [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) 結構，提供錯誤的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fe947-136">The DDE object contains a [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) structure that provides information about the error.</span></span><br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <span data-ttu-id="fe947-137"><dt>**MF \_HSZ \_ INFO**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="fe947-137"><dt>**MF\_HSZ\_INFO**</dt> <dt>0x01000000</dt></span></span> </dl>   | <span data-ttu-id="fe947-138">DDE 應用程式建立、釋放或遞增字串控制碼的使用計數，或字串控制碼因為呼叫 [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) 函式而釋出。</span><span class="sxs-lookup"><span data-stu-id="fe947-138">A DDE application created, freed, or incremented the usage count of a string handle, or a string handle was freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> <span data-ttu-id="fe947-139">DDE 物件包含 [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) 結構，提供字串控制碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fe947-139">The DDE object contains a [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure that provides information about the string handle.</span></span><br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <span data-ttu-id="fe947-140"><dt>**MF \_連結**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="fe947-140"><dt>**MF\_LINKS**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="fe947-141">DDE 應用程式已啟動或停止「建議」迴圈。</span><span class="sxs-lookup"><span data-stu-id="fe947-141">A DDE application started or stopped an advise loop.</span></span> <span data-ttu-id="fe947-142">DDE 物件包含 [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) 結構，提供建議迴圈的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fe947-142">The DDE object contains a [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) structure that provides information about the advise loop.</span></span><br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <span data-ttu-id="fe947-143"><dt>**MF \_POSTMSGS**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="fe947-143"><dt>**MF\_POSTMSGS**</dt> <dt>0x04000000</dt></span></span> </dl>    | <span data-ttu-id="fe947-144">已張貼 DDE 訊息的系統或應用程式。</span><span class="sxs-lookup"><span data-stu-id="fe947-144">The system or an application posted a DDE message.</span></span> <span data-ttu-id="fe947-145">DDE 物件包含提供訊息相關資訊的 [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) 結構。</span><span class="sxs-lookup"><span data-stu-id="fe947-145">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <span data-ttu-id="fe947-146"><dt>**MF \_SENDMSGS**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="fe947-146"><dt>**MF\_SENDMSGS**</dt> <dt>0x02000000</dt></span></span> </dl>    | <span data-ttu-id="fe947-147">系統或應用程式傳送了 DDE 訊息。</span><span class="sxs-lookup"><span data-stu-id="fe947-147">The system or an application sent a DDE message.</span></span> <span data-ttu-id="fe947-148">DDE 物件包含提供訊息相關資訊的 [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) 結構。</span><span class="sxs-lookup"><span data-stu-id="fe947-148">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe947-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe947-149">Return value</span></span>

<span data-ttu-id="fe947-150">如果回呼函式處理此交易，它應該會傳回0。</span><span class="sxs-lookup"><span data-stu-id="fe947-150">If the callback function processes this transaction, it should return 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe947-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe947-151">Requirements</span></span>



| <span data-ttu-id="fe947-152">需求</span><span class="sxs-lookup"><span data-stu-id="fe947-152">Requirement</span></span> | <span data-ttu-id="fe947-153">值</span><span class="sxs-lookup"><span data-stu-id="fe947-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe947-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe947-154">Minimum supported client</span></span><br/> | <span data-ttu-id="fe947-155">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe947-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fe947-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe947-156">Minimum supported server</span></span><br/> | <span data-ttu-id="fe947-157">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe947-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="fe947-158">標頭</span><span class="sxs-lookup"><span data-stu-id="fe947-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe947-159"><dt>Ddeml (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="fe947-159"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe947-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe947-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe947-161">**參考**</span><span class="sxs-lookup"><span data-stu-id="fe947-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fe947-162">**DdeAccessData**</span><span class="sxs-lookup"><span data-stu-id="fe947-162">**DdeAccessData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[<span data-ttu-id="fe947-163">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="fe947-163">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="fe947-164">**DdeUninitialize**</span><span class="sxs-lookup"><span data-stu-id="fe947-164">**DdeUninitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[<span data-ttu-id="fe947-165">**MONCBSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="fe947-165">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[<span data-ttu-id="fe947-166">**MONCONVSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="fe947-166">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[<span data-ttu-id="fe947-167">**MONERRSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="fe947-167">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[<span data-ttu-id="fe947-168">**MONHSZSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="fe947-168">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[<span data-ttu-id="fe947-169">**MONLINKSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="fe947-169">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[<span data-ttu-id="fe947-170">**MONMSGSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="fe947-170">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

<span data-ttu-id="fe947-171">**概念**</span><span class="sxs-lookup"><span data-stu-id="fe947-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fe947-172">動態資料交換管理程式庫</span><span class="sxs-lookup"><span data-stu-id="fe947-172">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

