---
description: 讓來源讀取器或接收寫入器使用硬體媒體基礎轉換 (MFTs) 。
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: 'MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319979"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a><span data-ttu-id="b2623-103">MF \_ READWRITE \_ 啟用 \_ 硬體 \_ 轉換屬性</span><span class="sxs-lookup"><span data-stu-id="b2623-103">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="b2623-104">讓來源讀取器或接收寫入器使用硬體媒體基礎轉換 (MFTs) 。</span><span class="sxs-lookup"><span data-stu-id="b2623-104">Enables the source reader or sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>

## <a name="data-type"></a><span data-ttu-id="b2623-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b2623-105">Data type</span></span>

<span data-ttu-id="b2623-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b2623-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b2623-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="b2623-107">Get/set</span></span>

<span data-ttu-id="b2623-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="b2623-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b2623-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="b2623-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2623-110">備註</span><span class="sxs-lookup"><span data-stu-id="b2623-110">Remarks</span></span>

<span data-ttu-id="b2623-111">根據預設，來源讀取器和接收寫入器不會使用硬體解碼器或編碼器。</span><span class="sxs-lookup"><span data-stu-id="b2623-111">By default, the source reader and sink writer do not use hardware decoders or encoders.</span></span> <span data-ttu-id="b2623-112">若要啟用硬體 MFTs，請在建立來源讀取器或接收寫入器時，將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="b2623-112">To enable the use of hardware MFTs, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="b2623-113">使用這個屬性搭配下列函數：</span><span class="sxs-lookup"><span data-stu-id="b2623-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="b2623-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="b2623-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="b2623-115">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="b2623-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="b2623-116">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="b2623-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="b2623-117">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="b2623-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="b2623-118">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="b2623-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="b2623-119">預設行為有一個例外狀況。</span><span class="sxs-lookup"><span data-stu-id="b2623-119">There is one exception to the default behavior.</span></span> <span data-ttu-id="b2623-120">來源讀取器和接收寫入器會自動使用在呼叫端進程的本機註冊的 MFTs。</span><span class="sxs-lookup"><span data-stu-id="b2623-120">The source reader and sink writer automatically use MFTs that are registered locally in the caller's process.</span></span> <span data-ttu-id="b2623-121">若要在本機註冊 MFT，請呼叫 [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) 或 [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)。</span><span class="sxs-lookup"><span data-stu-id="b2623-121">To register an MFT locally, call [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span></span> <span data-ttu-id="b2623-122">即使未設定 [ **MF \_ READWRITE \_ 啟用 \_ 硬體 \_ 轉換** ] 屬性，仍會使用在本機註冊的硬體 MFTs。</span><span class="sxs-lookup"><span data-stu-id="b2623-122">Hardware MFTs that are registered locally are used even if the **MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS** attribute is not set.</span></span>

<span data-ttu-id="b2623-123">此屬性不會影響使用 DirectX Video 加速 (DXVA) 的硬體加速影片解碼。</span><span class="sxs-lookup"><span data-stu-id="b2623-123">This attribute does not affect hardware-accelerated video decoding that uses DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="b2623-124">若要在來源讀取器中啟用 DXVA 解碼，請設定 [ [MF 來源讀取器] 「 \_ \_ \_ D3D \_ 管理員](mf-source-reader-d3d-manager.md) 」屬性。</span><span class="sxs-lookup"><span data-stu-id="b2623-124">To enable DXVA decoding in the source reader, set the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="b2623-125">如果此屬性為 **TRUE**，請勿將 [ [MF \_ READWRITE 停 \_ 用 \_ 轉換器](mf-readwrite-disable-converters.md) ] 屬性設定為 [否]。</span><span class="sxs-lookup"><span data-stu-id="b2623-125">If this attribute is **TRUE**, do not set the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2623-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2623-126">Requirements</span></span>



| <span data-ttu-id="b2623-127">需求</span><span class="sxs-lookup"><span data-stu-id="b2623-127">Requirement</span></span> | <span data-ttu-id="b2623-128">值</span><span class="sxs-lookup"><span data-stu-id="b2623-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2623-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2623-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b2623-130">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2623-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b2623-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2623-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b2623-132">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2623-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b2623-133">標頭</span><span class="sxs-lookup"><span data-stu-id="b2623-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2623-134"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2623-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2623-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2623-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2623-136">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b2623-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2623-137">接收寫入器屬性</span><span class="sxs-lookup"><span data-stu-id="b2623-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2623-138">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="b2623-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




