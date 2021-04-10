---
title: 'MM_ACM_FORMATCHOOSE 訊息 (Msacm.imaadpcm .h) '
description: MM 的 \_ \_ FORMATCHOOSE 訊息會在將專案新增至三個下拉式清單方塊的其中一個之前，通知 acmFormatChoose 對話攔截函式。
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- MM_ACM_FORMATCHOOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686639"
---
# <a name="mm_acm_formatchoose-message"></a><span data-ttu-id="9b893-104">MM \_ 的 \_ FORMATCHOOSE 訊息</span><span class="sxs-lookup"><span data-stu-id="9b893-104">MM\_ACM\_FORMATCHOOSE message</span></span>

<span data-ttu-id="9b893-105">**MM 的 \_ \_ FORMATCHOOSE** 訊息會在將專案新增至三個下拉式清單方塊的其中一個之前，通知 [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose)對話攔截函式。</span><span class="sxs-lookup"><span data-stu-id="9b893-105">The **MM\_ACM\_FORMATCHOOSE** message notifies an [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) dialog hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="9b893-106">此訊息可讓應用程式進一步自訂透過使用者介面所提供的選項。</span><span class="sxs-lookup"><span data-stu-id="9b893-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a><span data-ttu-id="9b893-107">參數</span><span class="sxs-lookup"><span data-stu-id="9b893-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b893-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span><span class="sxs-lookup"><span data-stu-id="9b893-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="9b893-109">要初始化的下拉式清單方塊，以及驗證或加入作業。</span><span class="sxs-lookup"><span data-stu-id="9b893-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="9b893-110">需求</span><span class="sxs-lookup"><span data-stu-id="9b893-110">Requirement</span></span> | <span data-ttu-id="9b893-111">值</span><span class="sxs-lookup"><span data-stu-id="9b893-111">Value</span></span> |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b893-112">FORMATCHOOSE \_ 自訂 \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="9b893-112">FORMATCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="9b893-113">*LParam* 參數是要加入至 [自訂名稱] 下拉式清單方塊之 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9b893-113">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="9b893-114">\_新增 FORMATCHOOSE 格式 \_</span><span class="sxs-lookup"><span data-stu-id="9b893-114">FORMATCHOOSE\_FORMAT\_ADD</span></span>       | <span data-ttu-id="9b893-115">*LParam* 參數是緩衝區的指標，會接受要加入至 [格式] 下拉式清單方塊中的 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)結構。</span><span class="sxs-lookup"><span data-stu-id="9b893-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span> <span data-ttu-id="9b893-116">應用程式必須複製要加入這個緩衝區的格式結構。</span><span class="sxs-lookup"><span data-stu-id="9b893-116">The application must copy the format structure to be added into this buffer.</span></span> |
| <span data-ttu-id="9b893-117">FORMATCHOOSE \_ 格式 \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="9b893-117">FORMATCHOOSE\_FORMAT\_VERIFY</span></span>    | <span data-ttu-id="9b893-118">*LParam* 參數是要加入至 [格式] 下拉式清單方塊之 [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9b893-118">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="9b893-119">FORMATCHOOSE \_ FORMATTAG \_ 新增</span><span class="sxs-lookup"><span data-stu-id="9b893-119">FORMATCHOOSE\_FORMATTAG\_ADD</span></span>    | <span data-ttu-id="9b893-120">*LParam* 參數是變數的指標，該變數會接受將波形音訊格式標記新增至 [格式標記] 下拉式清單方塊。</span><span class="sxs-lookup"><span data-stu-id="9b893-120">The *lParam* parameter is a pointer to a variable that will accept a waveform-audio format tag to be added to the Format Tag drop-down list box.</span></span>                                                                                             |
| <span data-ttu-id="9b893-121">FORMATCHOOSE \_ FORMATTAG \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="9b893-121">FORMATCHOOSE\_FORMATTAG\_VERIFY</span></span> | <span data-ttu-id="9b893-122">*LParam* 參數是要在 [格式標記] 下拉式清單方塊中列出的波形音訊格式標記。</span><span class="sxs-lookup"><span data-stu-id="9b893-122">The *lParam* parameter is a waveform-audio format tag to be listed in the Format Tag drop-down list box.</span></span>                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="9b893-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span><span class="sxs-lookup"><span data-stu-id="9b893-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="9b893-124">**WParam** 參數中所指定清單方塊所定義的值。</span><span class="sxs-lookup"><span data-stu-id="9b893-124">Value defined by the listbox specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b893-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b893-125">Return Value</span></span>

<span data-ttu-id="9b893-126">如果應用程式處理此訊息，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9b893-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b893-127">備註</span><span class="sxs-lookup"><span data-stu-id="9b893-127">Remarks</span></span>

<span data-ttu-id="9b893-128">如果應用程式處理 FILTERCHOOSE \_ 格式的 \_ 新增作業， *lParam* 中提供的記憶體緩衝區大小將會從 [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) 函式決定。</span><span class="sxs-lookup"><span data-stu-id="9b893-128">If the application processes the FILTERCHOOSE\_FORMAT\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="9b893-129">如果您的應用程式正在處理驗證作業，它可以藉由呼叫 **SetWindowLong** 函數，並將 *NINDEX* 設定為 DWL \_ MSGRESULT，並將 *lNewLong* 設定為 **FALSE** (轉換為 **LONG** 資料類型) ，防止對話方塊列出此選取專案。</span><span class="sxs-lookup"><span data-stu-id="9b893-129">If your application is processing a verify operation, it can prevent the dialog box from listing this selection by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="9b893-130">若要允許對話方塊列出此選項，請呼叫此函式，並將 *lNewLong* 設為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9b893-130">To allow the dialog box to list this selection, call this function with *lNewLong* set to **TRUE**.</span></span>

<span data-ttu-id="9b893-131">如果您的應用程式正在處理新增作業，它可能會藉由呼叫 **SetWindowLong** 函數，並將 *NINDEX* 設定為 DWL \_ MSGRESULT，並將 *lNewLong* 設定為 **FALSE** (轉換為 **LONG** 資料類型) ，來指出不再需要額外的新增作業。</span><span class="sxs-lookup"><span data-stu-id="9b893-131">If your application is processing an add operation, it can indicate that no more additions are required by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="9b893-132">若要指出需要更多新增專案，請呼叫此函式，並將 *lNewLong* 設為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9b893-132">To indicate more additions are required, call this function with *lNewLong* set to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b893-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b893-133">Requirements</span></span>



| <span data-ttu-id="9b893-134">需求</span><span class="sxs-lookup"><span data-stu-id="9b893-134">Requirement</span></span> | <span data-ttu-id="9b893-135">值</span><span class="sxs-lookup"><span data-stu-id="9b893-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b893-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b893-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9b893-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b893-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9b893-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b893-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9b893-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b893-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9b893-140">標頭</span><span class="sxs-lookup"><span data-stu-id="9b893-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b893-141"><dt>Msacm.imaadpcm。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b893-141"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b893-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b893-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b893-143">音訊壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="9b893-143">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="9b893-144">音訊壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="9b893-144">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

