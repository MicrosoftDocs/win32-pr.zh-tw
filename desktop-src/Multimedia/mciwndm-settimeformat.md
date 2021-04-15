---
title: 'MCIWNDM_SETTIMEFORMAT 訊息 (Vfw .h) '
description: MCIWNDM \_ SETTIMEFORMAT 訊息會設定 MCI 裝置的時間格式。 您可以使用 MCIWndSetTimeFormat 宏明確地傳送此訊息。
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508332"
---
# <a name="mciwndm_settimeformat-message"></a><span data-ttu-id="1957c-105">MCIWNDM \_ SETTIMEFORMAT 訊息</span><span class="sxs-lookup"><span data-stu-id="1957c-105">MCIWNDM\_SETTIMEFORMAT message</span></span>

<span data-ttu-id="1957c-106">**MCIWNDM \_ SETTIMEFORMAT** 訊息會設定 MCI 裝置的時間格式。</span><span class="sxs-lookup"><span data-stu-id="1957c-106">The **MCIWNDM\_SETTIMEFORMAT** message sets the time format of an MCI device.</span></span> <span data-ttu-id="1957c-107">您可以使用 [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="1957c-107">You can send this message explicitly or by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span>


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="1957c-108">參數</span><span class="sxs-lookup"><span data-stu-id="1957c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1957c-109"><span id="lp"></span><span id="LP"></span>*Lp*</span><span class="sxs-lookup"><span data-stu-id="1957c-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="1957c-110">緩衝區的指標，其中包含表示時間格式的以 null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="1957c-110">Pointer to a buffer containing the null-terminated string indicating the time format.</span></span> <span data-ttu-id="1957c-111">指定「框架」以將時間格式設定為框架，或指定 "ms" 以將時間格式設定為毫秒。</span><span class="sxs-lookup"><span data-stu-id="1957c-111">Specify "frames" to set the time format to frames, or "ms" to set the time format to milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1957c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1957c-112">Return Value</span></span>

<span data-ttu-id="1957c-113">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="1957c-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1957c-114">備註</span><span class="sxs-lookup"><span data-stu-id="1957c-114">Remarks</span></span>

<span data-ttu-id="1957c-115">只要 MCI 裝置支援這些格式，應用程式就可以指定框架或毫秒以外的時間格式。</span><span class="sxs-lookup"><span data-stu-id="1957c-115">An application can specify time formats other than frames or milliseconds as long as the formats are supported by the MCI device.</span></span> <span data-ttu-id="1957c-116">Noncontinuous 格式（例如追蹤和 SMPTE）可能會導致追蹤的行為不穩定。</span><span class="sxs-lookup"><span data-stu-id="1957c-116">Noncontinuous formats, such as tracks and SMPTE, can cause the trackbar to behave erratically.</span></span> <span data-ttu-id="1957c-117">針對這些時間格式，您可能會想要使用 [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) 宏和指定 MCIWNDF NOPLAYBAR 視窗樣式來關閉工具列 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1957c-117">For these time formats, you might want to turn off the toolbar by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro and specifying the MCIWNDF\_NOPLAYBAR window style.</span></span>

<span data-ttu-id="1957c-118">如果您想要將時間格式設定為框架或毫秒，您也可以使用 [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) 或 [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) 宏。</span><span class="sxs-lookup"><span data-stu-id="1957c-118">If you want to set the time format to frames or milliseconds, you can also use the [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) or [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) macro.</span></span> <span data-ttu-id="1957c-119">如需時間格式的清單，請參閱 [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) 宏。</span><span class="sxs-lookup"><span data-stu-id="1957c-119">For a list of time formats, see the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="1957c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1957c-120">Requirements</span></span>



| <span data-ttu-id="1957c-121">需求</span><span class="sxs-lookup"><span data-stu-id="1957c-121">Requirement</span></span> | <span data-ttu-id="1957c-122">值</span><span class="sxs-lookup"><span data-stu-id="1957c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1957c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1957c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1957c-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1957c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1957c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1957c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1957c-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1957c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1957c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="1957c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1957c-128"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="1957c-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1957c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1957c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1957c-130">**MCIWndChangeStyles**</span><span class="sxs-lookup"><span data-stu-id="1957c-130">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[<span data-ttu-id="1957c-131">**MCIWndGetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="1957c-131">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[<span data-ttu-id="1957c-132">**MCIWndSetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="1957c-132">**MCIWndSetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[<span data-ttu-id="1957c-133">**MCIWndUseFrames**</span><span class="sxs-lookup"><span data-stu-id="1957c-133">**MCIWndUseFrames**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[<span data-ttu-id="1957c-134">**MCIWndUseTime**</span><span class="sxs-lookup"><span data-stu-id="1957c-134">**MCIWndUseTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





