---
description: 當 IMFOutputTrustAuthority：： SetPolicy 方法以非同步方式完成時，由輸出信任授權單位引發 (OTA) 。
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: 'MEPolicySet 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238af6cbd740e62825ae0b661769c1cf1bf880ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986825"
---
# <a name="mepolicyset-event"></a><span data-ttu-id="48396-103">MEPolicySet 事件</span><span class="sxs-lookup"><span data-stu-id="48396-103">MEPolicySet event</span></span>

<span data-ttu-id="48396-104">當 [**IMFOutputTrustAuthority：： SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) 方法以非同步方式完成時，由輸出信任授權單位引發 (OTA) 。</span><span class="sxs-lookup"><span data-stu-id="48396-104">Raised by an output trust authority (OTA) when the [**IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="48396-105">事件值</span><span class="sxs-lookup"><span data-stu-id="48396-105">Event values</span></span>

<span data-ttu-id="48396-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="48396-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="48396-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="48396-107">VARTYPE</span></span>              | <span data-ttu-id="48396-108">Description</span><span class="sxs-lookup"><span data-stu-id="48396-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="48396-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="48396-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="48396-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="48396-110">No event data.</span></span><br/> <br/> |
| <span data-ttu-id="48396-111">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="48396-111">VT\_UI4</span></span><br/> | <span data-ttu-id="48396-112">可以透過[MF_POLICY_ID](mf-policy-id.md)屬性在[IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)上設定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="48396-112">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) through the [MF_POLICY_ID](mf-policy-id.md) attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="48396-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="48396-113">Requirements</span></span>



| <span data-ttu-id="48396-114">需求</span><span class="sxs-lookup"><span data-stu-id="48396-114">Requirement</span></span> | <span data-ttu-id="48396-115">值</span><span class="sxs-lookup"><span data-stu-id="48396-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48396-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48396-116">Minimum supported client</span></span><br/> | <span data-ttu-id="48396-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48396-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="48396-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48396-118">Minimum supported server</span></span><br/> | <span data-ttu-id="48396-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48396-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48396-120">標頭</span><span class="sxs-lookup"><span data-stu-id="48396-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="48396-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="48396-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48396-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48396-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48396-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="48396-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




