---
description: 在 Microsoft 媒體基礎管線中啟用低延遲處理。
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: 'MF_LOW_LATENCY 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693884"
---
# <a name="mf_low_latency-attribute"></a><span data-ttu-id="5c545-103">MF \_ 低 \_ 延遲屬性</span><span class="sxs-lookup"><span data-stu-id="5c545-103">MF\_LOW\_LATENCY attribute</span></span>

<span data-ttu-id="5c545-104">在 Microsoft 媒體基礎管線中啟用低延遲處理。</span><span class="sxs-lookup"><span data-stu-id="5c545-104">Enables low-latency processing in the Microsoft Media Foundation pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="5c545-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5c545-105">Data type</span></span>

<span data-ttu-id="5c545-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="5c545-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5c545-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="5c545-107">Get/set</span></span>

<span data-ttu-id="5c545-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="5c545-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5c545-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="5c545-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c545-110">備註</span><span class="sxs-lookup"><span data-stu-id="5c545-110">Remarks</span></span>

<span data-ttu-id="5c545-111">低延遲是定義為產生媒體資料時的最小可能延遲， (或在轉譯時接收) 。</span><span class="sxs-lookup"><span data-stu-id="5c545-111">Low latency is defined as the smallest possible delay from when the media data is generated (or received) to when it is rendered.</span></span> <span data-ttu-id="5c545-112">即時通訊案例需要低延遲。</span><span class="sxs-lookup"><span data-stu-id="5c545-112">Low latency is desirable for real-time communication scenarios.</span></span> <span data-ttu-id="5c545-113">針對其他案例，例如本機播放或轉碼，您通常不應該啟用低延遲模式，因為它可能會影響品質。</span><span class="sxs-lookup"><span data-stu-id="5c545-113">For other scenarios, such as local playback or transcoding, you typically should not enable low-latency mode, because it can affect quality.</span></span>

> [!Note]  
> <span data-ttu-id="5c545-114">這個屬性的 GUID 值與針對 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)介面定義的 [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)屬性相同。</span><span class="sxs-lookup"><span data-stu-id="5c545-114">The GUID value of this attribute is identical to the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) property defined for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>

 

<span data-ttu-id="5c545-115">在管線元件上設定此屬性，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5c545-115">Set this attribute on pipeline components as follows:</span></span>

-   <span data-ttu-id="5c545-116">媒體來源：使用 [**IMFMediaSourceEx：： GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) 方法。</span><span class="sxs-lookup"><span data-stu-id="5c545-116">Media source: Use the [**IMFMediaSourceEx::GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) method.</span></span>
-   <span data-ttu-id="5c545-117">媒體基礎轉換 (MFT) ：使用 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法。</span><span class="sxs-lookup"><span data-stu-id="5c545-117">Media Foundation transform (MFT): Use the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="5c545-118">針對編碼器，編碼器可能會透過 [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) 介面支援低延遲。</span><span class="sxs-lookup"><span data-stu-id="5c545-118">For encoders, the encoder might support low latency through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
-   <span data-ttu-id="5c545-119">媒體接收器：查詢 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="5c545-119">Media sink: Query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="5c545-120">應用程式通常不會直接在管線元件上設定此屬性，而是在下列其中一個物件上設定屬性：</span><span class="sxs-lookup"><span data-stu-id="5c545-120">Applications typically do not set this attribute directly on the pipeline components, but instead set the attribute on one of the following objects:</span></span>

-   <span data-ttu-id="5c545-121">[媒體會話](media-session.md)：使用 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)或 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguation* 參數，否則請在拓撲上設定屬性。</span><span class="sxs-lookup"><span data-stu-id="5c545-121">[Media Session](media-session.md): Use the *pConfiguation* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function, or else set the attribute on the topology.</span></span>
-   <span data-ttu-id="5c545-122">[來源讀取器](source-reader.md)：當您建立來源讀取器時，使用設定屬性設定屬性。</span><span class="sxs-lookup"><span data-stu-id="5c545-122">[Source Reader](source-reader.md): Set the attribute with the configuration properties when you create the Source Reader.</span></span> <span data-ttu-id="5c545-123">如需詳細資訊，請參閱 [來源讀取器屬性](source-reader-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="5c545-123">For more information, see [Source Reader Attributes](source-reader-attributes.md).</span></span>
-   <span data-ttu-id="5c545-124">[接收寫入器](sink-writer.md)：當您建立接收寫入器時，使用設定屬性設定屬性。</span><span class="sxs-lookup"><span data-stu-id="5c545-124">[Sink Writer](sink-writer.md): Set the attribute with the configuration properties when you create the Sink Writer.</span></span> <span data-ttu-id="5c545-125">如需詳細資訊，請參閱 [接收寫入器屬性](sink-writer-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="5c545-125">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c545-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c545-126">Requirements</span></span>



| <span data-ttu-id="5c545-127">需求</span><span class="sxs-lookup"><span data-stu-id="5c545-127">Requirement</span></span> | <span data-ttu-id="5c545-128">值</span><span class="sxs-lookup"><span data-stu-id="5c545-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c545-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c545-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5c545-130">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c545-130">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="5c545-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c545-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5c545-132">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c545-132">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5c545-133">標頭</span><span class="sxs-lookup"><span data-stu-id="5c545-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c545-134"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c545-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c545-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c545-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c545-136">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5c545-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5c545-137">接收寫入器屬性</span><span class="sxs-lookup"><span data-stu-id="5c545-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="5c545-138">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="5c545-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> <dt>

[<span data-ttu-id="5c545-139">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="5c545-139">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
