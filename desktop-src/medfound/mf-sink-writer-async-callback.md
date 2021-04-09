---
description: 包含接收寫入器的應用程式回呼介面指標。
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: 'MF_SINK_WRITER_ASYNC_CALLBACK 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695020"
---
# <a name="mf_sink_writer_async_callback-attribute"></a><span data-ttu-id="bd933-103">MF \_ 接收 \_ 寫入器 \_ 非同步 \_ 回呼屬性</span><span class="sxs-lookup"><span data-stu-id="bd933-103">MF\_SINK\_WRITER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="bd933-104">包含接收器寫入器的應用程式回呼介面指標。</span><span class="sxs-lookup"><span data-stu-id="bd933-104">Contains a pointer to the application's callback interface for the sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="bd933-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="bd933-105">Data type</span></span>

<span data-ttu-id="bd933-106">**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) IMFSinkWriterCallback \** _ 儲存為 _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="bd933-106">**[**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="bd933-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="bd933-107">Get/set</span></span>

<span data-ttu-id="bd933-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。</span><span class="sxs-lookup"><span data-stu-id="bd933-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="bd933-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。</span><span class="sxs-lookup"><span data-stu-id="bd933-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd933-110">備註</span><span class="sxs-lookup"><span data-stu-id="bd933-110">Remarks</span></span>

<span data-ttu-id="bd933-111">這個屬性的值是應用程式 [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="bd933-111">The value of this attribute is a pointer to the application's [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) interface.</span></span>

<span data-ttu-id="bd933-112">使用這個屬性搭配下列函數：</span><span class="sxs-lookup"><span data-stu-id="bd933-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="bd933-113">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="bd933-113">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="bd933-114">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="bd933-114">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="bd933-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd933-115">Requirements</span></span>



| <span data-ttu-id="bd933-116">需求</span><span class="sxs-lookup"><span data-stu-id="bd933-116">Requirement</span></span> | <span data-ttu-id="bd933-117">值</span><span class="sxs-lookup"><span data-stu-id="bd933-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd933-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd933-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd933-119">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd933-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="bd933-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd933-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd933-121">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd933-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bd933-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bd933-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd933-123"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd933-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd933-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd933-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd933-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="bd933-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bd933-126">接收寫入器屬性</span><span class="sxs-lookup"><span data-stu-id="bd933-126">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




