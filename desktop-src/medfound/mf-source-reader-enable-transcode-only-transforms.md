---
description: 可讓來源讀取器使用媒體基礎轉換， (MFTs) 已針對轉碼進行優化。
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: 'MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511321"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a><span data-ttu-id="b5464-103">MF \_ 來源 \_ 讀取器 \_ 啟用 \_ 轉碼 \_ 僅限 \_ 轉換屬性</span><span class="sxs-lookup"><span data-stu-id="b5464-103">MF\_SOURCE\_READER\_ENABLE\_TRANSCODE\_ONLY\_TRANSFORMS attribute</span></span>

<span data-ttu-id="b5464-104">可讓 [來源讀取器](source-reader.md) 使用媒體基礎轉換， (MFTs) 已針對轉碼進行優化。</span><span class="sxs-lookup"><span data-stu-id="b5464-104">Enables the [Source Reader](source-reader.md) to use Media Foundation transforms (MFTs) that are optimized for transcoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="b5464-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b5464-105">Data type</span></span>

<span data-ttu-id="b5464-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b5464-106">**UINT32**</span></span>

<span data-ttu-id="b5464-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="b5464-107">Treat as Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5464-108">備註</span><span class="sxs-lookup"><span data-stu-id="b5464-108">Remarks</span></span>

<span data-ttu-id="b5464-109">某些 MFTs （特別是在不同的解碼器）會針對轉碼進行優化，而不是播放。</span><span class="sxs-lookup"><span data-stu-id="b5464-109">Some MFTs, particularly decoders, are optimized for transcoding rather than playback.</span></span> <span data-ttu-id="b5464-110">根據預設，來源讀取器不會載入這類轉換。</span><span class="sxs-lookup"><span data-stu-id="b5464-110">By default, the Source Reader will not load such transforms.</span></span> <span data-ttu-id="b5464-111">如果您想要在來源讀取器中使用轉碼 MFTs，請將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b5464-111">Set this attribute to **TRUE** if you want to use transcoding MFTs with the Source Reader.</span></span>

<span data-ttu-id="b5464-112">應用程式可能會設定這個屬性，如果它不會即時處理轉碼或類似案例) 的資料 (。</span><span class="sxs-lookup"><span data-stu-id="b5464-112">An application might set this attribute if it does not process the data in real time (for transcoding or similar scenarios).</span></span> <span data-ttu-id="b5464-113">否則，若為即時播放，請使用預設行為。</span><span class="sxs-lookup"><span data-stu-id="b5464-113">Otherwise, for real-time playback, use the default behavior.</span></span>

<span data-ttu-id="b5464-114">就內部而言，此屬性會讓來源讀取器在呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)時，**只包含 MFT \_ 列舉 \_ 旗標 \_ 轉碼 \_** 旗標。</span><span class="sxs-lookup"><span data-stu-id="b5464-114">Internally, this attribute causes the Source Reader to include the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when it calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5464-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5464-115">Requirements</span></span>



| <span data-ttu-id="b5464-116">需求</span><span class="sxs-lookup"><span data-stu-id="b5464-116">Requirement</span></span> | <span data-ttu-id="b5464-117">值</span><span class="sxs-lookup"><span data-stu-id="b5464-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5464-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5464-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b5464-119">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5464-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b5464-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5464-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b5464-121">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5464-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b5464-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b5464-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5464-123"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="b5464-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5464-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5464-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5464-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b5464-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b5464-126">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="b5464-126">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




