---
description: 指定在第一個簡報之後排入的簡報開始時間。
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: 'MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978819"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a><span data-ttu-id="f6f4e-103">\_ \_ \_ \_ \_ PRESENTATION \_ SWITCH 屬性的 MF 拓撲開始時間</span><span class="sxs-lookup"><span data-stu-id="f6f4e-103">MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute</span></span>

<span data-ttu-id="f6f4e-104">指定在第一個簡報之後排入的簡報開始時間。</span><span class="sxs-lookup"><span data-stu-id="f6f4e-104">Specifies the start time for presentations that are queued after the first presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="f6f4e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f6f4e-105">Data type</span></span>

<span data-ttu-id="f6f4e-106">**INT64** 儲存為 **UINT64**</span><span class="sxs-lookup"><span data-stu-id="f6f4e-106">**INT64** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="f6f4e-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="f6f4e-107">Get/set</span></span>

<span data-ttu-id="f6f4e-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。</span><span class="sxs-lookup"><span data-stu-id="f6f4e-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="f6f4e-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。</span><span class="sxs-lookup"><span data-stu-id="f6f4e-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f6f4e-110">套用至</span><span class="sxs-lookup"><span data-stu-id="f6f4e-110">Applies To</span></span>

[<span data-ttu-id="f6f4e-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="f6f4e-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="f6f4e-112">備註</span><span class="sxs-lookup"><span data-stu-id="f6f4e-112">Remarks</span></span>

<span data-ttu-id="f6f4e-113">當應用程式將媒體會話上的第一個簡報排入佇列時，應用程式會在 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)方法的 *pvarStartPosition* 參數中指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="f6f4e-113">When the application queues the first presentation on the Media Session, the application specifies the start time in the *pvarStartPosition* parameter of the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method.</span></span> <span data-ttu-id="f6f4e-114">不過，在任何後續的簡報中，開始時間是由 \_ \_ 拓撲上的 [ \_ \_ \_ PRESENTATION SWITCH] \_ 屬性的 [MF 拓撲開始時間] 所指定。</span><span class="sxs-lookup"><span data-stu-id="f6f4e-114">For any subsequent presentations, however, the start time is given by the MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute on the topology.</span></span> <span data-ttu-id="f6f4e-115">開始時間是以 100-毫微秒單位（相對於簡報開頭）來指定。</span><span class="sxs-lookup"><span data-stu-id="f6f4e-115">The start time is specified in 100-nanosecond units, relative to the beginning of the presentation.</span></span> <span data-ttu-id="f6f4e-116">例如，如果值為50000000，播放會在簡報中開始5秒。</span><span class="sxs-lookup"><span data-stu-id="f6f4e-116">For example, if the value is 50000000, playback starts 5 seconds into the presentation.</span></span> <span data-ttu-id="f6f4e-117">如果未設定此屬性，則預設開始時間為零。</span><span class="sxs-lookup"><span data-stu-id="f6f4e-117">If this attribute is not set, the default start time is zero.</span></span>

<span data-ttu-id="f6f4e-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="f6f4e-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f4e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6f4e-119">Requirements</span></span>



| <span data-ttu-id="f6f4e-120">需求</span><span class="sxs-lookup"><span data-stu-id="f6f4e-120">Requirement</span></span> | <span data-ttu-id="f6f4e-121">值</span><span class="sxs-lookup"><span data-stu-id="f6f4e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f4e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6f4e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f4e-123">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6f4e-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f6f4e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6f4e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f4e-125">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6f4e-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f6f4e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f6f4e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6f4e-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f4e-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6f4e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6f4e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f4e-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f6f4e-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6f4e-130">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="f6f4e-130">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




