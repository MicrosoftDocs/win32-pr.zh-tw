---
description: 由受信任的輸出引發，以傳送有關強制執行輸出原則的狀態資訊。
ms.assetid: 4906f6c3-1570-421f-aef1-914bd338bb1f
title: 'MEPolicyReport 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0053fb551a69b820beeb4237211cb9af446f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977821"
---
# <a name="mepolicyreport-event"></a><span data-ttu-id="9c915-103">MEPolicyReport 事件</span><span class="sxs-lookup"><span data-stu-id="9c915-103">MEPolicyReport event</span></span>

<span data-ttu-id="9c915-104">由受信任的輸出引發，以傳送有關強制執行輸出原則的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9c915-104">Raised by a trusted output to send status information about the enforcement of the output policy.</span></span>

## <a name="event-values"></a><span data-ttu-id="9c915-105">事件值</span><span class="sxs-lookup"><span data-stu-id="9c915-105">Event values</span></span>

<span data-ttu-id="9c915-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="9c915-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9c915-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9c915-107">VARTYPE</span></span>              | <span data-ttu-id="9c915-108">Description</span><span class="sxs-lookup"><span data-stu-id="9c915-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="9c915-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="9c915-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="9c915-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="9c915-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9c915-111">備註</span><span class="sxs-lookup"><span data-stu-id="9c915-111">Remarks</span></span>

<span data-ttu-id="9c915-112">此事件的屬性和狀態碼取決於受信任的輸出所強制執行的特定內容保護系統。</span><span class="sxs-lookup"><span data-stu-id="9c915-112">Attributes and status codes for this event depend on the specific content protection system enforced by the trusted output.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c915-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c915-113">Requirements</span></span>



| <span data-ttu-id="9c915-114">需求</span><span class="sxs-lookup"><span data-stu-id="9c915-114">Requirement</span></span> | <span data-ttu-id="9c915-115">值</span><span class="sxs-lookup"><span data-stu-id="9c915-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c915-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c915-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9c915-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c915-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9c915-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c915-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9c915-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c915-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c915-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9c915-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c915-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="9c915-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c915-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c915-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c915-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="9c915-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




