---
description: 從增強型影片轉譯器 (EVR) 篩選要求新的輸入範例。
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: 'EC_SAMPLE_NEEDED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da73d02604e128fdf94edb8f84d1526cfcdb586e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992371"
---
# <a name="ec_sample_needed"></a><span data-ttu-id="62879-103">\_需要 EC 範例 \_</span><span class="sxs-lookup"><span data-stu-id="62879-103">EC\_SAMPLE\_NEEDED</span></span>

<span data-ttu-id="62879-104">從 [**增強型影片**](enhanced-video-renderer-filter.md) 轉譯器 (EVR) 篩選要求新的輸入範例。</span><span class="sxs-lookup"><span data-stu-id="62879-104">Requests a new input sample from the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="62879-105">參數</span><span class="sxs-lookup"><span data-stu-id="62879-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62879-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="62879-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="62879-107">需要新輸入之輸入資料流程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="62879-107">Identifier of the input stream that needs new input.</span></span>

</dd> <dt>

<span data-ttu-id="62879-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="62879-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="62879-109">零個。</span><span class="sxs-lookup"><span data-stu-id="62879-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="62879-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="62879-110">Default Action</span></span>

<span data-ttu-id="62879-111">無。</span><span class="sxs-lookup"><span data-stu-id="62879-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="62879-112">備註</span><span class="sxs-lookup"><span data-stu-id="62879-112">Remarks</span></span>

<span data-ttu-id="62879-113">EVR 篩選器的混音器會在需要新的輸入範例時傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="62879-113">The mixer for the EVR filter sends this message when it needs a new input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="62879-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="62879-114">Requirements</span></span>



| <span data-ttu-id="62879-115">需求</span><span class="sxs-lookup"><span data-stu-id="62879-115">Requirement</span></span> | <span data-ttu-id="62879-116">值</span><span class="sxs-lookup"><span data-stu-id="62879-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62879-117">標頭</span><span class="sxs-lookup"><span data-stu-id="62879-117">Header</span></span><br/> | <dl> <span data-ttu-id="62879-118"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="62879-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62879-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62879-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62879-120">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="62879-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> </dl>

 

 




