---
description: 指定最新框架步驟的時間戳記。
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: 'EC_SCRUB_TIME (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985571"
---
# <a name="ec_scrub_time"></a><span data-ttu-id="e925c-103">EC \_ 清理 \_ 時間</span><span class="sxs-lookup"><span data-stu-id="e925c-103">EC\_SCRUB\_TIME</span></span>

<span data-ttu-id="e925c-104">指定最新框架步驟的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="e925c-104">Specifies the time stamp for the most recent frame step.</span></span>

## <a name="parameters"></a><span data-ttu-id="e925c-105">參數</span><span class="sxs-lookup"><span data-stu-id="e925c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e925c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e925c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e925c-107">時間戳記的 (**DWORD**) 較低的32位。</span><span class="sxs-lookup"><span data-stu-id="e925c-107">(**DWORD**) Lower 32 bits of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="e925c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e925c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e925c-109">時間戳記的 (**DWORD**) 最高32位。</span><span class="sxs-lookup"><span data-stu-id="e925c-109">(**DWORD**) Upper 32 bits of the time stamp.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="e925c-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="e925c-110">Default Action</span></span>

<span data-ttu-id="e925c-111">無。</span><span class="sxs-lookup"><span data-stu-id="e925c-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="e925c-112">備註</span><span class="sxs-lookup"><span data-stu-id="e925c-112">Remarks</span></span>

<span data-ttu-id="e925c-113">[**增強型影片**](enhanced-video-renderer-filter.md)轉譯器的簡報者 (EVR) 篩選器會在完成框架步驟時，將此訊息傳送至 EVR。</span><span class="sxs-lookup"><span data-stu-id="e925c-113">The presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter sends this message to the EVR when it completes a frame step.</span></span>

## <a name="requirements"></a><span data-ttu-id="e925c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e925c-114">Requirements</span></span>



| <span data-ttu-id="e925c-115">需求</span><span class="sxs-lookup"><span data-stu-id="e925c-115">Requirement</span></span> | <span data-ttu-id="e925c-116">值</span><span class="sxs-lookup"><span data-stu-id="e925c-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e925c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e925c-117">Header</span></span><br/> | <dl> <span data-ttu-id="e925c-118"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e925c-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e925c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e925c-120">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="e925c-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




