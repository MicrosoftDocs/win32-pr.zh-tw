---
description: 當 IMFSequencerSource：： UpdateTopology 方法以非同步方式完成時，由 sequencer 來源引發。
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: 'MESequencerSourceTopologyUpdated 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981483"
---
# <a name="mesequencersourcetopologyupdated-event"></a><span data-ttu-id="1ff87-103">MESequencerSourceTopologyUpdated 事件</span><span class="sxs-lookup"><span data-stu-id="1ff87-103">MESequencerSourceTopologyUpdated event</span></span>

<span data-ttu-id="1ff87-104">當 [**IMFSequencerSource：： UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) 方法以非同步方式完成時，由 sequencer 來源引發。</span><span class="sxs-lookup"><span data-stu-id="1ff87-104">Raised by the sequencer source when the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="1ff87-105">事件值</span><span class="sxs-lookup"><span data-stu-id="1ff87-105">Event values</span></span>

<span data-ttu-id="1ff87-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="1ff87-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1ff87-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1ff87-107">VARTYPE</span></span>            | <span data-ttu-id="1ff87-108">Description</span><span class="sxs-lookup"><span data-stu-id="1ff87-108">Description</span></span>                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff87-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="1ff87-109">VT\_UI4</span></span><br/> | <span data-ttu-id="1ff87-110">正在更新之拓撲的 Sequencer 元素識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ff87-110">Sequencer element identifier of the topology that is being updated.</span></span> <span data-ttu-id="1ff87-111">應用程式會在 [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology)方法的 *dwId* 參數中指定此值。</span><span class="sxs-lookup"><span data-stu-id="1ff87-111">The application specifies this value in the *dwId* parameter of the [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1ff87-112">備註</span><span class="sxs-lookup"><span data-stu-id="1ff87-112">Remarks</span></span>

<span data-ttu-id="1ff87-113">此事件表示 sequencer 來源已更新拓撲，但並不表示拓撲已準備好可供播放。</span><span class="sxs-lookup"><span data-stu-id="1ff87-113">This event signals that the sequencer source has updated the topology, but does not mean that the topology is ready for playback.</span></span> <span data-ttu-id="1ff87-114">應用程式應該等候 [MESessionTopologyStatus](mesessiontopologystatus.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="1ff87-114">The application should wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff87-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ff87-115">Requirements</span></span>



| <span data-ttu-id="1ff87-116">需求</span><span class="sxs-lookup"><span data-stu-id="1ff87-116">Requirement</span></span> | <span data-ttu-id="1ff87-117">值</span><span class="sxs-lookup"><span data-stu-id="1ff87-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff87-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ff87-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1ff87-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ff87-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1ff87-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ff87-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1ff87-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ff87-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1ff87-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1ff87-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ff87-123"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="1ff87-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff87-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ff87-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff87-125">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="1ff87-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="1ff87-126">Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="1ff87-126">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




