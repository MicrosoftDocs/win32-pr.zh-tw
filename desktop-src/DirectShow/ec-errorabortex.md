---
description: EC_ERRORABORTEX-因為發生錯誤，所以已中止作業。
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: 'EC_ERRORABORTEX (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3bf1e1f24f9d5b07312f542c1ce4ea671f601d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094606"
---
# <a name="ec_errorabortex"></a><span data-ttu-id="e1ff6-103">EC \_ ERRORABORTEX</span><span class="sxs-lookup"><span data-stu-id="e1ff6-103">EC\_ERRORABORTEX</span></span>

<span data-ttu-id="e1ff6-104">作業已中止，因為發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="e1ff6-104">An operation was aborted because of an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1ff6-105">參數</span><span class="sxs-lookup"><span data-stu-id="e1ff6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1ff6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e1ff6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e1ff6-107">**(HRESULT)** 失敗的作業程式碼失敗。</span><span class="sxs-lookup"><span data-stu-id="e1ff6-107">**(HRESULT)** Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="e1ff6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e1ff6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e1ff6-109">**(BSTR)** 包含其他錯誤資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="e1ff6-109">**(BSTR)** String that contains additional error information.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="e1ff6-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="e1ff6-110">Default Action</span></span>

<span data-ttu-id="e1ff6-111">無。</span><span class="sxs-lookup"><span data-stu-id="e1ff6-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1ff6-112">備註</span><span class="sxs-lookup"><span data-stu-id="e1ff6-112">Remarks</span></span>

<span data-ttu-id="e1ff6-113">舊版 [Windows Media 來源](windows-media-source-filter.md) 篩選傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="e1ff6-113">The legacy [Windows Media Source](windows-media-source-filter.md) filter sends this event.</span></span> <span data-ttu-id="e1ff6-114">新的篩選器不應傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="e1ff6-114">New filters should not send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ff6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1ff6-115">Requirements</span></span>



| <span data-ttu-id="e1ff6-116">需求</span><span class="sxs-lookup"><span data-stu-id="e1ff6-116">Requirement</span></span> | <span data-ttu-id="e1ff6-117">值</span><span class="sxs-lookup"><span data-stu-id="e1ff6-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ff6-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e1ff6-118">Header</span></span><br/> | <dl> <span data-ttu-id="e1ff6-119"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1ff6-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1ff6-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1ff6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ff6-121">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="e1ff6-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e1ff6-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="e1ff6-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




