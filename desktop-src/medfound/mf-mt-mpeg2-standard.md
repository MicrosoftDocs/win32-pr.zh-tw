---
description: 如需描述 MPEG-2 程式串流 (PS) 或傳輸串流 (TS) 的媒體類型，請指定用來多工資料流程的標準。
ms.assetid: 3D4C1A81-A9BA-427F-93DB-F522A0616EAB
title: 'MF_MT_MPEG2_STANDARD 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0650a68975f449ea938b41872005e11d79922393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106995830"
---
# <a name="mf_mt_mpeg2_standard-attribute"></a><span data-ttu-id="5da15-103">MF \_ MT \_ MPEG2 \_ 標準屬性</span><span class="sxs-lookup"><span data-stu-id="5da15-103">MF\_MT\_MPEG2\_STANDARD attribute</span></span>

<span data-ttu-id="5da15-104">如需描述 MPEG-2 程式串流 (PS) 或傳輸串流 (TS) 的媒體類型，請指定用來多工資料流程的標準。</span><span class="sxs-lookup"><span data-stu-id="5da15-104">For a media type that describes an MPEG-2 program stream (PS) or transport stream (TS), specifies the standard that is used to multiplex the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="5da15-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5da15-105">Data type</span></span>

<span data-ttu-id="5da15-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5da15-106">**UINT32**</span></span>



| <span data-ttu-id="5da15-107">值</span><span class="sxs-lookup"><span data-stu-id="5da15-107">Value</span></span>                                                                                                | <span data-ttu-id="5da15-108">意義</span><span class="sxs-lookup"><span data-stu-id="5da15-108">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="5da15-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="5da15-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="5da15-110">標準 MPEG-2 PS 或 TS。</span><span class="sxs-lookup"><span data-stu-id="5da15-110">Standard MPEG-2 PS or TS.</span></span><br/>                                       |
| <span id="1"></span><dl> <span data-ttu-id="5da15-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="5da15-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="5da15-112">先進的電視系統委員會 (ATSC) 標準。</span><span class="sxs-lookup"><span data-stu-id="5da15-112">Advanced Television Systems Committee (ATSC) standard.</span></span><br/>          |
| <span id="2"></span><dl> <span data-ttu-id="5da15-113"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="5da15-113"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="5da15-114">數位視訊廣播 (DVB-T) 標準。</span><span class="sxs-lookup"><span data-stu-id="5da15-114">Digital Video Broadcasting (DVB) standard.</span></span><br/>                      |
| <span id="3"></span><dl> <span data-ttu-id="5da15-115"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="5da15-115"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="5da15-116">無線電產業和企業的關聯 (ARIB) 標準。</span><span class="sxs-lookup"><span data-stu-id="5da15-116">Association of Radio Industries and Businesses (ARIB) standard.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5da15-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5da15-117">Requirements</span></span>



| <span data-ttu-id="5da15-118">需求</span><span class="sxs-lookup"><span data-stu-id="5da15-118">Requirement</span></span> | <span data-ttu-id="5da15-119">值</span><span class="sxs-lookup"><span data-stu-id="5da15-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5da15-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5da15-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5da15-121">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5da15-121">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="5da15-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5da15-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5da15-123">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5da15-123">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5da15-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5da15-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5da15-125"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="5da15-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5da15-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5da15-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da15-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5da15-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




