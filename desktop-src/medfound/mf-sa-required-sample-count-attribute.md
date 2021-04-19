---
description: 指出增強型影片轉譯器 (EVR) 媒體接收器需要進行去交錯的未壓縮緩衝區數目。
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: 'MF_SA_REQUIRED_SAMPLE_COUNT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976965"
---
# <a name="mf_sa_required_sample_count-attribute"></a><span data-ttu-id="7dc60-103">MF \_ SA \_ 必要 \_ 範例 \_ 計數屬性</span><span class="sxs-lookup"><span data-stu-id="7dc60-103">MF\_SA\_REQUIRED\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="7dc60-104">指出增強型影片轉譯器 (EVR) 媒體接收器需要進行去交錯的未壓縮緩衝區數目。</span><span class="sxs-lookup"><span data-stu-id="7dc60-104">Indicates the number of uncompressed buffers that the enhanced video renderer (EVR) media sink requires for deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="7dc60-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7dc60-105">Data type</span></span>

<span data-ttu-id="7dc60-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7dc60-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc60-107">備註</span><span class="sxs-lookup"><span data-stu-id="7dc60-107">Remarks</span></span>

<span data-ttu-id="7dc60-108">這是資料流程層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="7dc60-108">This is a stream-level attribute.</span></span> <span data-ttu-id="7dc60-109">若要從 EVR 取得屬性，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="7dc60-109">To get the attribute from the EVR, do the following:</span></span>

1.  <span data-ttu-id="7dc60-110">呼叫 [**IMFMediaSink：： GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) 以取得資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="7dc60-110">Call [**IMFMediaSink::GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) to get the stream sink.</span></span>
2.  <span data-ttu-id="7dc60-111">查詢 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="7dc60-111">Query the stream sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>
3.  <span data-ttu-id="7dc60-112">呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="7dc60-112">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7dc60-113">就內部而言，混音器會提供此屬性給 EVR。</span><span class="sxs-lookup"><span data-stu-id="7dc60-113">Internally, the mixer provides this attribute to the EVR.</span></span> <span data-ttu-id="7dc60-114">若要從混音器取得屬性，請呼叫 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)。</span><span class="sxs-lookup"><span data-stu-id="7dc60-114">To get the attribute from the mixer, call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span></span>

<span data-ttu-id="7dc60-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="7dc60-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc60-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dc60-116">Requirements</span></span>



| <span data-ttu-id="7dc60-117">需求</span><span class="sxs-lookup"><span data-stu-id="7dc60-117">Requirement</span></span> | <span data-ttu-id="7dc60-118">值</span><span class="sxs-lookup"><span data-stu-id="7dc60-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc60-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7dc60-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc60-120">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dc60-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="7dc60-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7dc60-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc60-122">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7dc60-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="7dc60-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7dc60-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc60-124"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc60-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dc60-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dc60-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc60-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7dc60-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7dc60-127">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7dc60-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7dc60-128">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7dc60-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7dc60-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="7dc60-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




