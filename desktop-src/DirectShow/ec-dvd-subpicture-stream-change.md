---
description: 表示主要標題的目前子圖片串流號碼已變更。
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: 'EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c30ef0b27185b5300ac5cec877ed4e4b38685c12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994646"
---
# <a name="ec_dvd_subpicture_stream_change"></a><span data-ttu-id="de512-103">EC \_ DVD \_ 子圖片 \_ 串流 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="de512-103">EC\_DVD\_SUBPICTURE\_STREAM\_CHANGE</span></span>

<span data-ttu-id="de512-104">表示主要標題的目前子圖片串流號碼已變更。</span><span class="sxs-lookup"><span data-stu-id="de512-104">Signals that the current subpicture stream number changed for the main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="de512-105">參數</span><span class="sxs-lookup"><span data-stu-id="de512-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de512-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="de512-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="de512-107">**DWORD** 值，指出新的使用者子圖片串流號碼。</span><span class="sxs-lookup"><span data-stu-id="de512-107">**DWORD** value indicating the new user subpicture stream number.</span></span> <span data-ttu-id="de512-108">子圖片資料流程數位的範圍是從0到31。</span><span class="sxs-lookup"><span data-stu-id="de512-108">Subpicture stream numbers range from 0 to 31.</span></span> <span data-ttu-id="de512-109">Stream 0xFFFFFFFF 表示未選取任何資料流程。</span><span class="sxs-lookup"><span data-stu-id="de512-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="de512-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="de512-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="de512-111">指出子圖片開啟/關閉狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="de512-111">Boolean value that indicates the subpicture's on/off state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de512-112">備註</span><span class="sxs-lookup"><span data-stu-id="de512-112">Remarks</span></span>

<span data-ttu-id="de512-113">子圖片可使用在光碟上撰寫的流覽命令，以及透過使用 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)的應用程式控制，自動變更。</span><span class="sxs-lookup"><span data-stu-id="de512-113">The subpicture can change automatically with a navigation command authored on disc as well as through application control using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span></span>

<span data-ttu-id="de512-114">此事件會在所有網域中引發。</span><span class="sxs-lookup"><span data-stu-id="de512-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="de512-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="de512-115">Requirements</span></span>



| <span data-ttu-id="de512-116">需求</span><span class="sxs-lookup"><span data-stu-id="de512-116">Requirement</span></span> | <span data-ttu-id="de512-117">值</span><span class="sxs-lookup"><span data-stu-id="de512-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de512-118">標頭</span><span class="sxs-lookup"><span data-stu-id="de512-118">Header</span></span><br/> | <dl> <span data-ttu-id="de512-119"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="de512-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de512-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de512-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de512-121">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="de512-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="de512-122">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="de512-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="de512-123">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="de512-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




