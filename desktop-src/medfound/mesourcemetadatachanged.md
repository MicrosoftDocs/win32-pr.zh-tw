---
description: 當媒體來源更新其中繼資料時引發。
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: 'MESourceMetadataChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943548"
---
# <a name="mesourcemetadatachanged-event"></a><span data-ttu-id="17143-103">MESourceMetadataChanged 事件</span><span class="sxs-lookup"><span data-stu-id="17143-103">MESourceMetadataChanged event</span></span>

<span data-ttu-id="17143-104">當媒體來源更新其中繼資料時引發。</span><span class="sxs-lookup"><span data-stu-id="17143-104">Raised by a media source when it updates its metadata.</span></span>

## <a name="event-values"></a><span data-ttu-id="17143-105">事件值</span><span class="sxs-lookup"><span data-stu-id="17143-105">Event values</span></span>

<span data-ttu-id="17143-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="17143-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="17143-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="17143-107">VARTYPE</span></span>              | <span data-ttu-id="17143-108">Description</span><span class="sxs-lookup"><span data-stu-id="17143-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="17143-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="17143-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="17143-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="17143-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="17143-111">備註</span><span class="sxs-lookup"><span data-stu-id="17143-111">Remarks</span></span>

<span data-ttu-id="17143-112">如果媒體來源是在第一次建立來源時無法提供所有中繼資料，則應該在中繼資料可供使用之後引發此事件。</span><span class="sxs-lookup"><span data-stu-id="17143-112">If the media source cannot provide all of the metadata when the source is first created, it should raise this event after the metadata is available.</span></span>

<span data-ttu-id="17143-113">媒體來源應該建立新的簡報描述項，並將 (PD) 的表示描述項的所有屬性複製到事件物件。</span><span class="sxs-lookup"><span data-stu-id="17143-113">The media source should create a new presentation descriptor and copy all of the attributes from the presentation descriptor (PD) to the event object.</span></span> <span data-ttu-id="17143-114">應用程式可以使用事件物件來列舉新的 PD 屬性。</span><span class="sxs-lookup"><span data-stu-id="17143-114">The application can use the event object to enumerate the new PD attributes.</span></span> <span data-ttu-id="17143-115">尤其是，在完全下載檔案之前， [mf \_ pd \_ DURATION](mf-pd-duration-attribute.md) 和 [MF \_ pd 檔案 \_ \_ \_ 大小總計](mf-pd-total-file-size-attribute.md) 的值可能是未知的。</span><span class="sxs-lookup"><span data-stu-id="17143-115">In particular, the values for [MF\_PD\_DURATION](mf-pd-duration-attribute.md) and [MF\_PD\_TOTAL\_FILE\_SIZE](mf-pd-total-file-size-attribute.md) might be unknown until the file is completely downloaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="17143-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="17143-116">Requirements</span></span>



| <span data-ttu-id="17143-117">需求</span><span class="sxs-lookup"><span data-stu-id="17143-117">Requirement</span></span> | <span data-ttu-id="17143-118">值</span><span class="sxs-lookup"><span data-stu-id="17143-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17143-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17143-119">Minimum supported client</span></span><br/> | <span data-ttu-id="17143-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17143-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="17143-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17143-121">Minimum supported server</span></span><br/> | <span data-ttu-id="17143-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17143-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="17143-123">標頭</span><span class="sxs-lookup"><span data-stu-id="17143-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="17143-124"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="17143-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17143-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17143-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17143-126">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="17143-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="17143-127">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="17143-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




