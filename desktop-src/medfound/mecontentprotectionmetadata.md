---
description: 媒體資料流程會使用此事件將保護系統專屬的中繼資料傳送給該解碼器。
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: 'MEContentProtectionMetadata 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848321"
---
# <a name="mecontentprotectionmetadata-event"></a><span data-ttu-id="c6d4c-103">MEContentProtectionMetadata 事件</span><span class="sxs-lookup"><span data-stu-id="c6d4c-103">MEContentProtectionMetadata event</span></span>

<span data-ttu-id="c6d4c-104">媒體資料流程會使用此事件將保護系統專屬的中繼資料傳送給該解碼器。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-104">Media Stream uses this event to send protection system specific metadata to the decoder.</span></span>

## <a name="event-values"></a><span data-ttu-id="c6d4c-105">事件值</span><span class="sxs-lookup"><span data-stu-id="c6d4c-105">Event values</span></span>

<span data-ttu-id="c6d4c-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c6d4c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c6d4c-107">VARTYPE</span></span>              | <span data-ttu-id="c6d4c-108">Description</span><span class="sxs-lookup"><span data-stu-id="c6d4c-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c6d4c-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="c6d4c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c6d4c-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="c6d4c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c6d4c-111">Attributes</span></span>

<span data-ttu-id="c6d4c-112">此事件會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="c6d4c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="c6d4c-113">Attribute</span></span>                                                                                              | <span data-ttu-id="c6d4c-114">描述</span><span class="sxs-lookup"><span data-stu-id="c6d4c-114">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6d4c-115">MF \_ 事件 \_ 串流 \_ 中繼資料 \_ >KEYDATA</span><span class="sxs-lookup"><span data-stu-id="c6d4c-115">MF\_EVENT\_STREAM\_METADATA\_KEYDATA</span></span>](mf-event-stream-metadata-keydata.md)<br/>                | <span data-ttu-id="c6d4c-116">這是選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-116">This is an optional attribute.</span></span> <span data-ttu-id="c6d4c-117">保護系統特定資料。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-117">Protection system specific data.</span></span><br/> <br/>              |
| [<span data-ttu-id="c6d4c-118">MF \_ 事件 \_ 串流 \_ 中繼資料 \_ 內容 \_ KEYIDS</span><span class="sxs-lookup"><span data-stu-id="c6d4c-118">MF\_EVENT\_STREAM\_METADATA\_CONTENT\_KEYIDS</span></span>](mf-event-stream-metadata-content-keyids.md)<br/> | <span data-ttu-id="c6d4c-119">與事件相關聯的內容金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-119">Content key IDs which the event is associated with.</span></span><br/> <br/>                          |
| [<span data-ttu-id="c6d4c-120">MF \_ 事件 \_ 串流 \_ 中繼資料 \_ SYSTEMID</span><span class="sxs-lookup"><span data-stu-id="c6d4c-120">MF\_EVENT\_STREAM\_METADATA\_SYSTEMID</span></span>](mf-event-stream-metadata-systemid.md)<br/>              | <span data-ttu-id="c6d4c-121">這是選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-121">This is an optional attribute.</span></span> <span data-ttu-id="c6d4c-122">主要資料的目標系統識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-122">System ID for which the key data is intended.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c6d4c-123">備註</span><span class="sxs-lookup"><span data-stu-id="c6d4c-123">Remarks</span></span>

<span data-ttu-id="c6d4c-124">例如，會使用此事件來傳達金鑰旋轉事件。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-124">This event is used, for example, for communicating key rotation event.</span></span> <span data-ttu-id="c6d4c-125">在此情況下，應儘早傳送，以在使用新的金鑰識別碼開始傳遞的範例之前，先將它準備好給解碼器。</span><span class="sxs-lookup"><span data-stu-id="c6d4c-125">In this case it should be sent as early as possible to give the decoder time to prepare itself before samples encrypted with the new key ID start arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d4c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6d4c-126">Requirements</span></span>



| <span data-ttu-id="c6d4c-127">需求</span><span class="sxs-lookup"><span data-stu-id="c6d4c-127">Requirement</span></span> | <span data-ttu-id="c6d4c-128">值</span><span class="sxs-lookup"><span data-stu-id="c6d4c-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d4c-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6d4c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d4c-130">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6d4c-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c6d4c-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6d4c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d4c-132">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6d4c-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="c6d4c-133">標頭</span><span class="sxs-lookup"><span data-stu-id="c6d4c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6d4c-134"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="c6d4c-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d4c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6d4c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d4c-136">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="c6d4c-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




