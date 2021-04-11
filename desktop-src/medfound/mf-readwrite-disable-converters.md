---
description: 啟用或停用來源讀取器或接收寫入器的格式轉換。
ms.assetid: 282b70c3-c81c-47dd-bfa2-7e77138ccb91
title: 'MF_READWRITE_DISABLE_CONVERTERS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8532c45ca3aeb272fa6b6ef422e0d82e40bd3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194982"
---
# <a name="mf_readwrite_disable_converters-attribute"></a><span data-ttu-id="7f3af-103">MF \_ READWRITE \_ 停用 \_ 轉換器屬性</span><span class="sxs-lookup"><span data-stu-id="7f3af-103">MF\_READWRITE\_DISABLE\_CONVERTERS attribute</span></span>

<span data-ttu-id="7f3af-104">啟用或停用來源讀取器或接收寫入器的格式轉換。</span><span class="sxs-lookup"><span data-stu-id="7f3af-104">Enables or disables format conversions by the source reader or sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f3af-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7f3af-105">Data type</span></span>

<span data-ttu-id="7f3af-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7f3af-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7f3af-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="7f3af-107">Get/set</span></span>

<span data-ttu-id="7f3af-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="7f3af-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7f3af-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="7f3af-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f3af-110">備註</span><span class="sxs-lookup"><span data-stu-id="7f3af-110">Remarks</span></span>

<span data-ttu-id="7f3af-111">根據預設，來源讀取器和接收寫入器可以針對未壓縮的音訊和影片串流執行某些格式轉換。</span><span class="sxs-lookup"><span data-stu-id="7f3af-111">By default, the source reader and sink writer can perform some format conversions on uncompressed audio and video streams.</span></span> <span data-ttu-id="7f3af-112">若要停用此行為，請在建立來源讀取器或接收寫入器時，將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="7f3af-112">To disable this behavior, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="7f3af-113">使用這個屬性搭配下列函數：</span><span class="sxs-lookup"><span data-stu-id="7f3af-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="7f3af-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="7f3af-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="7f3af-115">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="7f3af-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="7f3af-116">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="7f3af-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="7f3af-117">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="7f3af-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="7f3af-118">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="7f3af-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="7f3af-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f3af-119">Requirements</span></span>



| <span data-ttu-id="7f3af-120">需求</span><span class="sxs-lookup"><span data-stu-id="7f3af-120">Requirement</span></span> | <span data-ttu-id="7f3af-121">值</span><span class="sxs-lookup"><span data-stu-id="7f3af-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f3af-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f3af-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7f3af-123">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f3af-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7f3af-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f3af-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7f3af-125">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f3af-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7f3af-126">標頭</span><span class="sxs-lookup"><span data-stu-id="7f3af-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f3af-127"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f3af-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f3af-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f3af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f3af-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7f3af-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f3af-130">接收寫入器屬性</span><span class="sxs-lookup"><span data-stu-id="7f3af-130">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f3af-131">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="7f3af-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




