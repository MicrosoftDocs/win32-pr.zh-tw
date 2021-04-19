---
description: 指定 h.264 影片資料流程的速率控制模式。
ms.assetid: EA8EFEFA-9292-4D7B-BF5D-DE5239BB1D2C
title: 'MF_MT_H264_RATE_CONTROL_MODES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3fc19070cd3b45aa25a1307a216f611dce1fd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971019"
---
# <a name="mf_mt_h264_rate_control_modes-attribute"></a><span data-ttu-id="0daa6-103">MF \_ MT \_ H264 \_ 速率 \_ 控制 \_ 模式屬性</span><span class="sxs-lookup"><span data-stu-id="0daa6-103">MF\_MT\_H264\_RATE\_CONTROL\_MODES attribute</span></span>

<span data-ttu-id="0daa6-104">指定 h.264 影片資料流程的速率控制模式。</span><span class="sxs-lookup"><span data-stu-id="0daa6-104">Specifies the rate-control mode for an H.264 video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="0daa6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="0daa6-105">Data type</span></span>

<span data-ttu-id="0daa6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0daa6-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0daa6-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="0daa6-107">Get/set</span></span>

<span data-ttu-id="0daa6-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="0daa6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0daa6-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="0daa6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="0daa6-110">適用於</span><span class="sxs-lookup"><span data-stu-id="0daa6-110">Applies to</span></span>

[<span data-ttu-id="0daa6-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0daa6-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="0daa6-112">備註</span><span class="sxs-lookup"><span data-stu-id="0daa6-112">Remarks</span></span>

<span data-ttu-id="0daa6-113">此屬性適用于透過 USB 傳輸之 h.264 資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0daa6-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="0daa6-114">值會對應至 UVC 1.2 h.264 探查/commit 控制項中的 **bmRateControlModes** 欄位。</span><span class="sxs-lookup"><span data-stu-id="0daa6-114">The value corresponds to the **bmRateControlModes** field in the UVC 1.2 H.264 probe/commit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0daa6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0daa6-115">Requirements</span></span>



| <span data-ttu-id="0daa6-116">需求</span><span class="sxs-lookup"><span data-stu-id="0daa6-116">Requirement</span></span> | <span data-ttu-id="0daa6-117">值</span><span class="sxs-lookup"><span data-stu-id="0daa6-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0daa6-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0daa6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0daa6-119">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0daa6-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0daa6-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0daa6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0daa6-121">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0daa6-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0daa6-122">標頭</span><span class="sxs-lookup"><span data-stu-id="0daa6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0daa6-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="0daa6-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0daa6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0daa6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0daa6-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="0daa6-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0daa6-126">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="0daa6-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




