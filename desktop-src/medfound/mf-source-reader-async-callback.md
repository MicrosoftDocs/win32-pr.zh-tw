---
description: 包含來源讀取器的應用程式回呼介面指標。
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: 'MF_SOURCE_READER_ASYNC_CALLBACK 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193620"
---
# <a name="mf_source_reader_async_callback-attribute"></a><span data-ttu-id="c21b4-103">MF \_ 來源 \_ 讀取器 \_ 非同步 \_ 回呼屬性</span><span class="sxs-lookup"><span data-stu-id="c21b4-103">MF\_SOURCE\_READER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="c21b4-104">包含應用程式的 [來源讀取器](source-reader.md)回呼介面指標。</span><span class="sxs-lookup"><span data-stu-id="c21b4-104">Contains a pointer to the application's callback interface for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="c21b4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c21b4-105">Data type</span></span>

<span data-ttu-id="c21b4-106">**IMFSourceReaderCallback \** _ 儲存為 _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="c21b4-106">**IMFSourceReaderCallback\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="c21b4-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="c21b4-107">Get/set</span></span>

<span data-ttu-id="c21b4-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="c21b4-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="c21b4-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="c21b4-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="c21b4-110">備註</span><span class="sxs-lookup"><span data-stu-id="c21b4-110">Remarks</span></span>

<span data-ttu-id="c21b4-111">這個屬性的值是應用程式 [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c21b4-111">The value of this attribute is a pointer to the application's [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) interface.</span></span>

<span data-ttu-id="c21b4-112">使用這個屬性搭配下列函數：</span><span class="sxs-lookup"><span data-stu-id="c21b4-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="c21b4-113">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="c21b4-113">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="c21b4-114">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="c21b4-114">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="c21b4-115">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="c21b4-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a><span data-ttu-id="c21b4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c21b4-116">Requirements</span></span>



| <span data-ttu-id="c21b4-117">需求</span><span class="sxs-lookup"><span data-stu-id="c21b4-117">Requirement</span></span> | <span data-ttu-id="c21b4-118">值</span><span class="sxs-lookup"><span data-stu-id="c21b4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21b4-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c21b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c21b4-120">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c21b4-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c21b4-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c21b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c21b4-122">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c21b4-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c21b4-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c21b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c21b4-124"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="c21b4-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c21b4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c21b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c21b4-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c21b4-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c21b4-127">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="c21b4-127">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="c21b4-128">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="c21b4-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




