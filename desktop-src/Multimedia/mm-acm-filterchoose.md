---
title: 'MM_ACM_FILTERCHOOSE 訊息 (Msacm.imaadpcm .h) '
description: MM 的 \_ \_ FILTERCHOOSE 訊息會在將專案新增至三個下拉式清單方塊的其中一個之前，通知 acmFilterChoose 對話方塊攔截函式。
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- MM_ACM_FILTERCHOOSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093987"
---
# <a name="mm_acm_filterchoose-message"></a><span data-ttu-id="6c986-104">MM \_ 的 \_ FILTERCHOOSE 訊息</span><span class="sxs-lookup"><span data-stu-id="6c986-104">MM\_ACM\_FILTERCHOOSE message</span></span>

<span data-ttu-id="6c986-105">**MM 的 \_ \_ FILTERCHOOSE** 訊息會在將專案新增至三個下拉式清單方塊的其中一個之前，通知 [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose)對話方塊攔截函式。</span><span class="sxs-lookup"><span data-stu-id="6c986-105">The **MM\_ACM\_FILTERCHOOSE** message notifies an [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) dialog box hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="6c986-106">此訊息可讓應用程式進一步自訂透過使用者介面所提供的選項。</span><span class="sxs-lookup"><span data-stu-id="6c986-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a><span data-ttu-id="6c986-107">參數</span><span class="sxs-lookup"><span data-stu-id="6c986-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c986-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span><span class="sxs-lookup"><span data-stu-id="6c986-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="6c986-109">要初始化的下拉式清單方塊，以及驗證或加入作業。</span><span class="sxs-lookup"><span data-stu-id="6c986-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="6c986-110">需求</span><span class="sxs-lookup"><span data-stu-id="6c986-110">Requirement</span></span> | <span data-ttu-id="6c986-111">值</span><span class="sxs-lookup"><span data-stu-id="6c986-111">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c986-112">FILTERCHOOSE \_ 自訂 \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="6c986-112">FILTERCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="6c986-113">*LParam* 參數是要加入至 [自訂名稱] 下拉式清單方塊之 [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6c986-113">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="6c986-114">FILTERCHOOSE \_ 篩選準則 \_ 新增</span><span class="sxs-lookup"><span data-stu-id="6c986-114">FILTERCHOOSE\_FILTER\_ADD</span></span>       | <span data-ttu-id="6c986-115">*LParam* 參數是緩衝區的指標，會接受要加入至 [篩選] 下拉式清單方塊中的 [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter)結構。</span><span class="sxs-lookup"><span data-stu-id="6c986-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span> <span data-ttu-id="6c986-116">應用程式必須複製要加入至此緩衝區的篩選結構。</span><span class="sxs-lookup"><span data-stu-id="6c986-116">The application must copy the filter structure to be added into this buffer.</span></span> |
| <span data-ttu-id="6c986-117">FILTERCHOOSE \_ 篩選準則 \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="6c986-117">FILTERCHOOSE\_FILTER\_VERIFY</span></span>    | <span data-ttu-id="6c986-118">*LParam* 參數是要加入至 [篩選] 下拉式清單方塊之 [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6c986-118">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="6c986-119">FILTERCHOOSE \_ FILTERTAG \_ 新增</span><span class="sxs-lookup"><span data-stu-id="6c986-119">FILTERCHOOSE\_FILTERTAG\_ADD</span></span>    | <span data-ttu-id="6c986-120">*LParam* 參數是 **DWORD** 的指標，會接受要加入 [篩選標記] 下拉式清單方塊中的波形音訊篩選標記。</span><span class="sxs-lookup"><span data-stu-id="6c986-120">The *lParam* parameter is a pointer to a **DWORD** that will accept a waveform-audio filter tag to be added to the Filter Tag drop-down list box.</span></span>                                                                                        |
| <span data-ttu-id="6c986-121">FILTERCHOOSE \_ FILTERTAG \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="6c986-121">FILTERCHOOSE\_FILTERTAG\_VERIFY</span></span> | <span data-ttu-id="6c986-122">*LParam* 參數是要列在 [篩選標記] 下拉式清單方塊中的波形音訊篩選標記。</span><span class="sxs-lookup"><span data-stu-id="6c986-122">The *lParam* parameter is a waveform-audio filter tag to be listed in the Filter Tag drop-down list box.</span></span>                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="6c986-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span><span class="sxs-lookup"><span data-stu-id="6c986-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="6c986-124">**WParam** 參數中指定的清單方塊所定義的值。</span><span class="sxs-lookup"><span data-stu-id="6c986-124">Value defined by the list box specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c986-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c986-125">Return Value</span></span>

<span data-ttu-id="6c986-126">如果應用程式處理此訊息，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6c986-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c986-127">備註</span><span class="sxs-lookup"><span data-stu-id="6c986-127">Remarks</span></span>

<span data-ttu-id="6c986-128">如果應用程式處理 FILTERCHOOSE \_ 篩選 \_ 新增作業，則 *lParam* 中提供的記憶體緩衝區大小將會從 [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) 函式決定。</span><span class="sxs-lookup"><span data-stu-id="6c986-128">If the application processes the FILTERCHOOSE\_FILTER\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="6c986-129">如果應用程式處理驗證作業，應用程式必須在傳回值之前加上 **SetWindowLong** (HWND，DWL \_ MSGRESULT， (LONG) **FALSE**) 以防止對話方塊列出此選取專案或 **SetWindowLong** (hwnd、DWL \_ MSGRESULT、 (LONG) **TRUE**) ，讓對話方塊可以列出此選取專案。</span><span class="sxs-lookup"><span data-stu-id="6c986-129">If the application processes a verify operation, the application must precede the return value with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG) **FALSE**) to prevent the dialog box from listing this selection or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) to allow the dialog box to list this selection.</span></span> <span data-ttu-id="6c986-130">如果處理新增作業，應用程式必須在 **SetWindowLong** (HWND，DWL \_ MSGRESULT， (LONG) **FALSE**) 以表示不需要再新增，或使用 **SetWindowLong** (hwnd，DWL \_ MSGRESULT， (long) **TRUE**) 如果需要更多新增專案。</span><span class="sxs-lookup"><span data-stu-id="6c986-130">If processing an add operation, the application must precede the return with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**FALSE**) to indicate that no more additions are required or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) if more additions are required.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c986-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c986-131">Requirements</span></span>



| <span data-ttu-id="6c986-132">需求</span><span class="sxs-lookup"><span data-stu-id="6c986-132">Requirement</span></span> | <span data-ttu-id="6c986-133">值</span><span class="sxs-lookup"><span data-stu-id="6c986-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c986-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c986-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6c986-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c986-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6c986-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c986-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6c986-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c986-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6c986-138">標頭</span><span class="sxs-lookup"><span data-stu-id="6c986-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c986-139"><dt>Msacm.imaadpcm。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c986-139"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c986-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c986-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c986-141">音訊壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="6c986-141">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="6c986-142">音訊壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="6c986-142">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

 





