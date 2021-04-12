---
title: 'ICM_ABOUT 訊息 (Vfw .h) '
description: '\_關於訊息的 ICM 會通知視訊壓縮驅動程式顯示其 [關於] 對話方塊，或查詢 video 壓縮驅動程式來判斷它是否有 [關於] 對話方塊。 您可以使用 ICAbout 宏明確地傳送此訊息。'
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- ICM_ABOUT message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024567"
---
# <a name="icm_about-message"></a><span data-ttu-id="2938f-105">\_關於訊息的 ICM</span><span class="sxs-lookup"><span data-stu-id="2938f-105">ICM\_ABOUT message</span></span>

<span data-ttu-id="2938f-106">**\_ 關於** 訊息的 ICM 會通知視訊壓縮驅動程式顯示其 [關於] 對話方塊，或查詢 video 壓縮驅動程式來判斷它是否有 [關於] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2938f-106">The **ICM\_ABOUT** message notifies a video compression driver to display its About dialog box or queries a video compression driver to determine if it has an About dialog box.</span></span> <span data-ttu-id="2938f-107">您可以使用 [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2938f-107">You can send this message explicitly or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro.</span></span>


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="2938f-108">參數</span><span class="sxs-lookup"><span data-stu-id="2938f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2938f-109"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span><span class="sxs-lookup"><span data-stu-id="2938f-109"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="2938f-110">顯示之對話方塊的父視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="2938f-110">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="2938f-111">您也可以在這個參數中指定-1，以判斷驅動程式是否有 [關於] 對話方塊，如同在 [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) 宏中一樣。</span><span class="sxs-lookup"><span data-stu-id="2938f-111">You can also determine if a driver has an About dialog box by specifying -1 in this parameter, as in the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro.</span></span> <span data-ttu-id="2938f-112">如果驅動程式 \_ 有 [關於] 對話方塊或 ICERR 不支援，則會傳回 ICERR OK \_ 。</span><span class="sxs-lookup"><span data-stu-id="2938f-112">The driver returns ICERR\_OK if it has an About dialog box or ICERR\_UNSUPPORTED otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2938f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2938f-113">Return Value</span></span>

<span data-ttu-id="2938f-114">\_如果驅動程式支援此訊息或 ICERR 不支援，則會傳回 ICERR OK \_ 。</span><span class="sxs-lookup"><span data-stu-id="2938f-114">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2938f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2938f-115">Requirements</span></span>



| <span data-ttu-id="2938f-116">需求</span><span class="sxs-lookup"><span data-stu-id="2938f-116">Requirement</span></span> | <span data-ttu-id="2938f-117">值</span><span class="sxs-lookup"><span data-stu-id="2938f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2938f-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2938f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2938f-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2938f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2938f-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2938f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2938f-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2938f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2938f-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2938f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2938f-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="2938f-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2938f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2938f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2938f-125">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="2938f-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2938f-126">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="2938f-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





