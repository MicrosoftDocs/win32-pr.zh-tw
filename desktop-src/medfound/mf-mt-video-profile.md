---
description: 指定輸出媒體類型上影片編碼的設定檔。 這是 MF \_ MT \_ MPEG2 \_ 配置檔案屬性的別名。
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: 'MF_MT_VIDEO_PROFILE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971601"
---
# <a name="mf_mt_video_profile-attribute"></a><span data-ttu-id="4893f-104">MF \_ MT \_ 影片 \_ 配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="4893f-104">MF\_MT\_VIDEO\_PROFILE attribute</span></span>

<span data-ttu-id="4893f-105">指定輸出媒體類型上影片編碼的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4893f-105">Specifies the profile of video encoding on the output media type.</span></span> <span data-ttu-id="4893f-106">這是 [MF \_ MT \_ MPEG2 \_ 設定檔](mf-mt-mpeg2-profile-attribute.md) 屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="4893f-106">This is an alias of [MF\_MT\_MPEG2\_PROFILE](mf-mt-mpeg2-profile-attribute.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="4893f-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="4893f-107">Data type</span></span>

<span data-ttu-id="4893f-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4893f-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4893f-109">備註</span><span class="sxs-lookup"><span data-stu-id="4893f-109">Remarks</span></span>

<span data-ttu-id="4893f-110">**H.264 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="4893f-110">**H.264 encoders:**</span></span>

<span data-ttu-id="4893f-111">已超出支援的設定檔，以包含 [**eAVEncH264VProfile \_ ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) 和 **eAVEncH264VProfile \_ ConstrainedHigh**。</span><span class="sxs-lookup"><span data-stu-id="4893f-111">Supported profiles are exceeded to include [**eAVEncH264VProfile\_ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) and **eAVEncH264VProfile\_ConstrainedHigh**.</span></span>

<span data-ttu-id="4893f-112">編碼器應同時支援此屬性的 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 和 [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) 。</span><span class="sxs-lookup"><span data-stu-id="4893f-112">Encoders shall support both [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) and [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) for this attribute.</span></span>

<span data-ttu-id="4893f-113">這是靜態的，因此必須先設定影片編碼器，才能開始串流。</span><span class="sxs-lookup"><span data-stu-id="4893f-113">This is static, so video encoders must be configured before the streaming starts.</span></span> <span data-ttu-id="4893f-114">如果應用程式設定編碼器不支援的設定檔，則編碼器應該拒絕媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4893f-114">If the application sets a profile which the encoder does not support, the encoder shall reject the media type.</span></span>

<span data-ttu-id="4893f-115">建議的預設值： [**eAVEncH264VProfile \_ 主要**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4893f-115">Recommended default: [**eAVEncH264VProfile\_Main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="4893f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4893f-116">Requirements</span></span>



| <span data-ttu-id="4893f-117">需求</span><span class="sxs-lookup"><span data-stu-id="4893f-117">Requirement</span></span> | <span data-ttu-id="4893f-118">值</span><span class="sxs-lookup"><span data-stu-id="4893f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4893f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4893f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4893f-120">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4893f-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4893f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4893f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4893f-122">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4893f-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4893f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4893f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4893f-124"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="4893f-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4893f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4893f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4893f-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4893f-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
