---
description: 指定來源讀取器是否關閉媒體來源。
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: 'MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321663"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a><span data-ttu-id="9874a-103">MF \_ 來源 \_ 讀取 \_ 器 \_ \_ 在 \_ SHUTDOWN 屬性中斷 MEDIASOURCE</span><span class="sxs-lookup"><span data-stu-id="9874a-103">MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute</span></span>

<span data-ttu-id="9874a-104">指定 [來源讀取器](source-reader.md) 是否關閉媒體來源。</span><span class="sxs-lookup"><span data-stu-id="9874a-104">Specifies whether the [Source Reader](source-reader.md) shuts down the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="9874a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9874a-105">Data type</span></span>

<span data-ttu-id="9874a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9874a-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9874a-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="9874a-107">Get/set</span></span>

<span data-ttu-id="9874a-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="9874a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9874a-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="9874a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="9874a-110">備註</span><span class="sxs-lookup"><span data-stu-id="9874a-110">Remarks</span></span>

<span data-ttu-id="9874a-111">只有當應用程式透過呼叫 [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) 或呼叫 [**IMFReadWriteClassFactory：： CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)，從現有的媒體來源物件建立來源讀取器時，才會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="9874a-111">This attribute applies only when the application creates the source reader from an existing media source object, either by calling [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) or by calling [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span></span>

<span data-ttu-id="9874a-112">根據預設，當應用程式釋放來源讀取器時，來源讀取器會藉由呼叫媒體來源上的 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 來關閉媒體來源。</span><span class="sxs-lookup"><span data-stu-id="9874a-112">By default, when the application releases the source reader, the source reader shuts down the media source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span> <span data-ttu-id="9874a-113">屆時，應用程式將無法再使用媒體來源。</span><span class="sxs-lookup"><span data-stu-id="9874a-113">At that point, the application can no longer use the media source.</span></span>

<span data-ttu-id="9874a-114">但是，如果 MF \_ 來源 \_ 讀取器 \_ \_ 在 SHUTDOWN 上中斷連線 MEDIASOURCE \_ \_ 屬性為 **TRUE**，則來源讀取器不會關閉媒體來源。</span><span class="sxs-lookup"><span data-stu-id="9874a-114">However, if the MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is **TRUE**, the source reader does not shut down the media source.</span></span> <span data-ttu-id="9874a-115">這表示應用程式在釋放來源讀取器之後，仍然可以使用媒體來源。</span><span class="sxs-lookup"><span data-stu-id="9874a-115">That means the application can still use the media source after the application releases the source reader.</span></span> <span data-ttu-id="9874a-116">這也表示應用程式會負責呼叫媒體來源上的 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 。</span><span class="sxs-lookup"><span data-stu-id="9874a-116">It also means the application is responsible for calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>

<span data-ttu-id="9874a-117">如果應用程式從 URL 或位元組資料流程建立來源讀取器，來源讀取器一律會關閉媒體來源。</span><span class="sxs-lookup"><span data-stu-id="9874a-117">If the application creates the source reader from a URL or from a byte stream, the source reader always shuts down the media source.</span></span> <span data-ttu-id="9874a-118">\_ \_ \_ \_ \_ \_ 在此情況下，會忽略 MEDIASOURCE ON SHUTDOWN 屬性的 MF 來源讀取器中斷連線。</span><span class="sxs-lookup"><span data-stu-id="9874a-118">The MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is ignored in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="9874a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9874a-119">Requirements</span></span>



| <span data-ttu-id="9874a-120">需求</span><span class="sxs-lookup"><span data-stu-id="9874a-120">Requirement</span></span> | <span data-ttu-id="9874a-121">值</span><span class="sxs-lookup"><span data-stu-id="9874a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9874a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9874a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9874a-123">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9874a-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="9874a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9874a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9874a-125">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9874a-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9874a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9874a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9874a-127"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="9874a-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9874a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9874a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9874a-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9874a-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9874a-130">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="9874a-130">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="9874a-131">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="9874a-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




