---
description: 媒體類型的主要類型 GUID。
ms.assetid: b88b5fcf-8025-4638-930d-9fc5cf0ec8a3
title: 'MF_MT_MAJOR_TYPE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c4cc02df4f89e261605c91b71ac1c80ba38b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972873"
---
# <a name="mf_mt_major_type-attribute"></a><span data-ttu-id="23404-103">MF \_ MT \_ 主要 \_ 類型屬性</span><span class="sxs-lookup"><span data-stu-id="23404-103">MF\_MT\_MAJOR\_TYPE attribute</span></span>

<span data-ttu-id="23404-104">媒體類型的主要類型 GUID。</span><span class="sxs-lookup"><span data-stu-id="23404-104">Major type GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="23404-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="23404-105">Data type</span></span>

<span data-ttu-id="23404-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="23404-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="23404-107">備註</span><span class="sxs-lookup"><span data-stu-id="23404-107">Remarks</span></span>

<span data-ttu-id="23404-108">主要類型會定義媒體資料的整體分類。</span><span class="sxs-lookup"><span data-stu-id="23404-108">The major type defines the overall category of the media data.</span></span> <span data-ttu-id="23404-109">主要類型包括影片、音訊、腳本等等。</span><span class="sxs-lookup"><span data-stu-id="23404-109">Major types include video, audio, script, and so forth.</span></span> <span data-ttu-id="23404-110">如需可能值的清單，請參閱 [主要媒體類型](media-type-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="23404-110">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="23404-111">取得此屬性的替代方式是呼叫 [**IMFMediaType：： GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)。</span><span class="sxs-lookup"><span data-stu-id="23404-111">An alternate way to retrieve this attribute is to call [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype).</span></span>

<span data-ttu-id="23404-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="23404-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="23404-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="23404-113">Requirements</span></span>



| <span data-ttu-id="23404-114">需求</span><span class="sxs-lookup"><span data-stu-id="23404-114">Requirement</span></span> | <span data-ttu-id="23404-115">值</span><span class="sxs-lookup"><span data-stu-id="23404-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23404-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23404-116">Minimum supported client</span></span><br/> | <span data-ttu-id="23404-117">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23404-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="23404-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23404-118">Minimum supported server</span></span><br/> | <span data-ttu-id="23404-119">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23404-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="23404-120">標頭</span><span class="sxs-lookup"><span data-stu-id="23404-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="23404-121"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="23404-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23404-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23404-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23404-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="23404-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="23404-124">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="23404-124">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="23404-125">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="23404-125">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="23404-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="23404-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="23404-127">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="23404-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




