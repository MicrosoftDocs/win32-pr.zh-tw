---
description: 表示 DVD 功能表按鈕的數目已變更，或按鈕選取範圍已變更。
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: 'EC_DVD_BUTTON_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995999"
---
# <a name="ec_dvd_button_change"></a><span data-ttu-id="06fdb-103">EC \_ DVD \_ 按鈕 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="06fdb-103">EC\_DVD\_BUTTON\_CHANGE</span></span>

<span data-ttu-id="06fdb-104">表示 DVD 功能表按鈕的數目已變更，或按鈕選取範圍已變更。</span><span class="sxs-lookup"><span data-stu-id="06fdb-104">Signals that the number of DVD menu buttons has changed, or that the button selection has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="06fdb-105">參數</span><span class="sxs-lookup"><span data-stu-id="06fdb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06fdb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="06fdb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="06fdb-107">**DWORD** 值，表示可用按鈕的數目。</span><span class="sxs-lookup"><span data-stu-id="06fdb-107">**DWORD** value indicating the number of available buttons.</span></span>

</dd> <dt>

<span data-ttu-id="06fdb-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="06fdb-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="06fdb-109">**DWORD** 值，指出目前選取的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="06fdb-109">**DWORD** value indicating the currently selected button number.</span></span> <span data-ttu-id="06fdb-110">選取的按鈕數位零表示未選取任何按鈕。</span><span class="sxs-lookup"><span data-stu-id="06fdb-110">Selected button number zero implies that no button is selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06fdb-111">備註</span><span class="sxs-lookup"><span data-stu-id="06fdb-111">Remarks</span></span>

<span data-ttu-id="06fdb-112">按鈕編號的範圍為1到36。</span><span class="sxs-lookup"><span data-stu-id="06fdb-112">Button numbers range from 1 to 36.</span></span>

<span data-ttu-id="06fdb-113">目前選取的按鈕可以使用在光碟上撰寫的流覽命令，以及透過使用 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 介面的應用程式控制，自動變更。</span><span class="sxs-lookup"><span data-stu-id="06fdb-113">The currently selected button can change automatically with a navigation command authored on the disc as well as through application control by using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="06fdb-114">此事件可以通知任何可用的按鈕編號。</span><span class="sxs-lookup"><span data-stu-id="06fdb-114">This event can signal any of the available button numbers.</span></span> <span data-ttu-id="06fdb-115">這些數位不一定會對應到用於 [**IDvdControl2：： SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) 的按鈕編號，因為該方法只能啟用按鈕的子集。</span><span class="sxs-lookup"><span data-stu-id="06fdb-115">These numbers do not always correspond to button numbers used for [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) because that method can activate only a subset of buttons.</span></span>

<span data-ttu-id="06fdb-116">此事件會在所有網域中引發。</span><span class="sxs-lookup"><span data-stu-id="06fdb-116">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="06fdb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="06fdb-117">Requirements</span></span>



| <span data-ttu-id="06fdb-118">需求</span><span class="sxs-lookup"><span data-stu-id="06fdb-118">Requirement</span></span> | <span data-ttu-id="06fdb-119">值</span><span class="sxs-lookup"><span data-stu-id="06fdb-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06fdb-120">標頭</span><span class="sxs-lookup"><span data-stu-id="06fdb-120">Header</span></span><br/> | <dl> <span data-ttu-id="06fdb-121"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="06fdb-121"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06fdb-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06fdb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06fdb-123">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="06fdb-123">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="06fdb-124">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="06fdb-124">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="06fdb-125">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="06fdb-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




