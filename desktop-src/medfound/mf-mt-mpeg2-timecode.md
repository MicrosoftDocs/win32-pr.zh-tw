---
description: 針對描述 (TS) 的 MPEG-2 傳輸串流的媒體類型，指定傳輸封包包含4位元組的時間代碼。
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: 'MF_MT_MPEG2_TIMECODE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193627"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a><span data-ttu-id="d42ef-103">MF \_ MT \_ MPEG2 時間 \_ 碼屬性</span><span class="sxs-lookup"><span data-stu-id="d42ef-103">MF\_MT\_MPEG2\_TIMECODE attribute</span></span>

<span data-ttu-id="d42ef-104">針對描述 (TS) 的 MPEG-2 傳輸串流的媒體類型，指定傳輸封包包含4位元組的時間代碼。</span><span class="sxs-lookup"><span data-stu-id="d42ef-104">For a media type that describes an MPEG-2 transport stream (TS), specifies the transport packets contain a 4-byte time code.</span></span>

## <a name="data-type"></a><span data-ttu-id="d42ef-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d42ef-105">Data type</span></span>

<span data-ttu-id="d42ef-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d42ef-106">**UINT32**</span></span>



| <span data-ttu-id="d42ef-107">值</span><span class="sxs-lookup"><span data-stu-id="d42ef-107">Value</span></span>                                                                                                | <span data-ttu-id="d42ef-108">意義</span><span class="sxs-lookup"><span data-stu-id="d42ef-108">Meaning</span></span>                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="d42ef-109"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="d42ef-109"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="d42ef-110">未新增任何時間碼。</span><span class="sxs-lookup"><span data-stu-id="d42ef-110">No time code is added.</span></span><br/>                                                                                                              |
| <span id="1"></span><dl> <span data-ttu-id="d42ef-111"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d42ef-111"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d42ef-112">每個傳輸封包的開頭會加上4個位元組的時間代碼。</span><span class="sxs-lookup"><span data-stu-id="d42ef-112">A 4-byte time code is added at the start of each transport packet.</span></span> <span data-ttu-id="d42ef-113">某些數位電視標準需要此時間代碼。</span><span class="sxs-lookup"><span data-stu-id="d42ef-113">This time code is required by some digital television standards.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d42ef-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d42ef-114">Requirements</span></span>



| <span data-ttu-id="d42ef-115">需求</span><span class="sxs-lookup"><span data-stu-id="d42ef-115">Requirement</span></span> | <span data-ttu-id="d42ef-116">值</span><span class="sxs-lookup"><span data-stu-id="d42ef-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d42ef-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d42ef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d42ef-118">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d42ef-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d42ef-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d42ef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d42ef-120">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d42ef-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d42ef-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d42ef-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d42ef-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d42ef-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d42ef-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d42ef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d42ef-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d42ef-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




