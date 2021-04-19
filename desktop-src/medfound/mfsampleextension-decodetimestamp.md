---
description: 包含範例 (DTS) 的解碼時間戳記。
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: 'MFSampleExtension_DecodeTimestamp 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996634"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a><span data-ttu-id="d79a4-103">MFSampleExtension \_ DecodeTimestamp 屬性</span><span class="sxs-lookup"><span data-stu-id="d79a4-103">MFSampleExtension\_DecodeTimestamp attribute</span></span>

<span data-ttu-id="d79a4-104">包含範例 (DTS) 的解碼時間戳記。</span><span class="sxs-lookup"><span data-stu-id="d79a4-104">Contains the decode time stamp (DTS) for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="d79a4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d79a4-105">Data type</span></span>

<span data-ttu-id="d79a4-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d79a4-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="d79a4-107">備註</span><span class="sxs-lookup"><span data-stu-id="d79a4-107">Remarks</span></span>

<span data-ttu-id="d79a4-108">屬性（attribute）的值為 100-毫微秒單位的 DTS。</span><span class="sxs-lookup"><span data-stu-id="d79a4-108">The value of the attribute is the DTS in 100-nanosecond units.</span></span> <span data-ttu-id="d79a4-109">DTS 是以一些編碼標準（包括 MPEG）來定義。</span><span class="sxs-lookup"><span data-stu-id="d79a4-109">The DTS is defined in some encoding standards, including MPEG.</span></span> <span data-ttu-id="d79a4-110">DTS 會指定編碼圖片應該解碼的時機。</span><span class="sxs-lookup"><span data-stu-id="d79a4-110">The DTS specifies when the encoded picture should be decoded.</span></span> <span data-ttu-id="d79a4-111">如果編碼的影片包含 B 個框架，則 DTS 可能與展示時間不同，因為 B 圖片在位流中的時態順序不會出現。</span><span class="sxs-lookup"><span data-stu-id="d79a4-111">If the encoded video contains B frames, the DTS can differ from the presentation time, because B pictures appear out of temporal order in the bitstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="d79a4-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d79a4-112">Requirements</span></span>



| <span data-ttu-id="d79a4-113">需求</span><span class="sxs-lookup"><span data-stu-id="d79a4-113">Requirement</span></span> | <span data-ttu-id="d79a4-114">值</span><span class="sxs-lookup"><span data-stu-id="d79a4-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d79a4-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d79a4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d79a4-116">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d79a4-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d79a4-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d79a4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d79a4-118">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d79a4-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d79a4-119">標頭</span><span class="sxs-lookup"><span data-stu-id="d79a4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d79a4-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d79a4-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d79a4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d79a4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d79a4-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d79a4-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d79a4-123">範例屬性</span><span class="sxs-lookup"><span data-stu-id="d79a4-123">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




