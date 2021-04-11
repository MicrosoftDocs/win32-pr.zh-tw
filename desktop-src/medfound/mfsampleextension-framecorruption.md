---
description: 指定影片框架是否已損毀。
ms.assetid: 0218F6F6-6832-445C-B733-6A99E4EA2A3B
title: 'MFSampleExtension_FrameCorruption 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d3618e5d847833b539cdfa7f6f99ae784e96c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115001"
---
# <a name="mfsampleextension_framecorruption-attribute"></a><span data-ttu-id="6f9cf-103">MFSampleExtension \_ FrameCorruption 屬性</span><span class="sxs-lookup"><span data-stu-id="6f9cf-103">MFSampleExtension\_FrameCorruption attribute</span></span>

<span data-ttu-id="6f9cf-104">指定影片框架是否已損毀。</span><span class="sxs-lookup"><span data-stu-id="6f9cf-104">Specifies whether a video frame is corrupted.</span></span>

## <a name="data-type"></a><span data-ttu-id="6f9cf-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6f9cf-105">Data type</span></span>

<span data-ttu-id="6f9cf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6f9cf-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6f9cf-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="6f9cf-107">Get/set</span></span>

<span data-ttu-id="6f9cf-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="6f9cf-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6f9cf-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="6f9cf-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6f9cf-110">適用於</span><span class="sxs-lookup"><span data-stu-id="6f9cf-110">Applies to</span></span>

[<span data-ttu-id="6f9cf-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="6f9cf-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="6f9cf-112">備註</span><span class="sxs-lookup"><span data-stu-id="6f9cf-112">Remarks</span></span>

<span data-ttu-id="6f9cf-113">影片解碼器可以在其輸出範例上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="6f9cf-113">A video decoder can set this attribute on its output samples.</span></span> <span data-ttu-id="6f9cf-114">如果值為1，則此解碼器偵測到框架中的資料損毀。</span><span class="sxs-lookup"><span data-stu-id="6f9cf-114">If the value is 1, the decoder detected data corruption in the frame.</span></span> <span data-ttu-id="6f9cf-115">如果值為0，則不會有資料損毀，或未偵測到任何資料。</span><span class="sxs-lookup"><span data-stu-id="6f9cf-115">If the value is 0, there is no data corruption, or none was detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f9cf-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f9cf-116">Requirements</span></span>



| <span data-ttu-id="6f9cf-117">需求</span><span class="sxs-lookup"><span data-stu-id="6f9cf-117">Requirement</span></span> | <span data-ttu-id="6f9cf-118">值</span><span class="sxs-lookup"><span data-stu-id="6f9cf-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f9cf-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f9cf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6f9cf-120">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f9cf-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6f9cf-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f9cf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6f9cf-122">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f9cf-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6f9cf-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6f9cf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f9cf-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6f9cf-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f9cf-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f9cf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f9cf-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="6f9cf-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6f9cf-127">範例屬性</span><span class="sxs-lookup"><span data-stu-id="6f9cf-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="6f9cf-128">媒體範例</span><span class="sxs-lookup"><span data-stu-id="6f9cf-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




