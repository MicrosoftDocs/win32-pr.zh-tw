---
description: 針對描述 (TS) 的 MPEG-2 傳輸串流的媒體類型，指定傳輸封包是否包含內容封包標頭。
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: 'MF_MT_MPEG2_CONTENT_PACKET 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850456"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a><span data-ttu-id="738bf-103">MF \_ MT \_ MPEG2 \_ 內容封 \_ 包屬性</span><span class="sxs-lookup"><span data-stu-id="738bf-103">MF\_MT\_MPEG2\_CONTENT\_PACKET attribute</span></span>

<span data-ttu-id="738bf-104">針對描述 (TS) 的 MPEG-2 傳輸串流的媒體類型，指定傳輸封包是否包含內容封包標頭。</span><span class="sxs-lookup"><span data-stu-id="738bf-104">For a media type that describes an MPEG-2 transport stream (TS), specifies whether the transport packets contain Content Packet headers.</span></span>

## <a name="data-type"></a><span data-ttu-id="738bf-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="738bf-105">Data type</span></span>

<span data-ttu-id="738bf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="738bf-106">**UINT32**</span></span>



| <span data-ttu-id="738bf-107">值</span><span class="sxs-lookup"><span data-stu-id="738bf-107">Value</span></span>                                                                                                | <span data-ttu-id="738bf-108">意義</span><span class="sxs-lookup"><span data-stu-id="738bf-108">Meaning</span></span>                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="738bf-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="738bf-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="738bf-110">未新增任何內容封包標頭。</span><span class="sxs-lookup"><span data-stu-id="738bf-110">No Content Packet headers are added.</span></span><br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <span data-ttu-id="738bf-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="738bf-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="738bf-112">在 200-1000 毫秒的間隔內，會將14位元組的內容封包標頭新增至傳輸封包的開頭，如同無線電產業和企業的關聯所定義 (ARIB) 標準。</span><span class="sxs-lookup"><span data-stu-id="738bf-112">At 200–1000 millisecond intervals, a 14-byte Content Packet header is added to the beginning of the transport packet, as defined by the Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="738bf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="738bf-113">Requirements</span></span>



| <span data-ttu-id="738bf-114">需求</span><span class="sxs-lookup"><span data-stu-id="738bf-114">Requirement</span></span> | <span data-ttu-id="738bf-115">值</span><span class="sxs-lookup"><span data-stu-id="738bf-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="738bf-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="738bf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="738bf-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="738bf-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="738bf-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="738bf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="738bf-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="738bf-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="738bf-120">標頭</span><span class="sxs-lookup"><span data-stu-id="738bf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="738bf-121"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="738bf-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="738bf-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="738bf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738bf-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="738bf-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




