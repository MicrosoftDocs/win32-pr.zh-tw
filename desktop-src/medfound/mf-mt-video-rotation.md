---
description: 以逆時針方向指定影片框架的旋轉。
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: 'MF_MT_VIDEO_ROTATION 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852820"
---
# <a name="mf_mt_video_rotation-attribute"></a><span data-ttu-id="94187-103">MF \_ MT \_ 影片 \_ 旋轉屬性</span><span class="sxs-lookup"><span data-stu-id="94187-103">MF\_MT\_VIDEO\_ROTATION attribute</span></span>

<span data-ttu-id="94187-104">以逆時針方向指定影片框架的旋轉。</span><span class="sxs-lookup"><span data-stu-id="94187-104">Specifies the rotation of a video frame in the counter-clockwise direction.</span></span>

## <a name="data-type"></a><span data-ttu-id="94187-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="94187-105">Data type</span></span>

<span data-ttu-id="94187-106">**MFVideoRotationFormat** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="94187-106">**MFVideoRotationFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="94187-107">備註</span><span class="sxs-lookup"><span data-stu-id="94187-107">Remarks</span></span>

<span data-ttu-id="94187-108">掌上型裝置的影片（例如行動電話）通常會以90、180或270度旋轉。</span><span class="sxs-lookup"><span data-stu-id="94187-108">Video from a handheld device, such as a mobile phone, is often rotated by 90, 180, or 270 degrees.</span></span> <span data-ttu-id="94187-109">如果相機將方向以中繼資料的形式儲存在影片檔案中，則在播放時可以調整影像。</span><span class="sxs-lookup"><span data-stu-id="94187-109">If the camera stores the orientation as metadata in the video file, the image can be adjusted at the time of playback.</span></span>

<span data-ttu-id="94187-110">如果此屬性設定為 **MFVideoRotationFormat \_ 90**，則表示內容已以逆時針方向旋轉90度。</span><span class="sxs-lookup"><span data-stu-id="94187-110">If this attribute set to **MFVideoRotationFormat\_90**, it means that the content has been rotated 90 degrees in the counter-clockwise direction.</span></span> <span data-ttu-id="94187-111">如果內容在順時針方向旋轉90度，則屬性值會是 **MFVideoRotationFormat \_ 270**。</span><span class="sxs-lookup"><span data-stu-id="94187-111">If the content was rotated 90 degrees in the clockwise direction, the attribute value would be **MFVideoRotationFormat\_270**.</span></span>

<span data-ttu-id="94187-112">此屬性支援的值會在 [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat)中列舉。</span><span class="sxs-lookup"><span data-stu-id="94187-112">The supported values for this attribute are enumerated in [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span></span>

<span data-ttu-id="94187-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="94187-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="94187-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="94187-114">Requirements</span></span>



| <span data-ttu-id="94187-115">需求</span><span class="sxs-lookup"><span data-stu-id="94187-115">Requirement</span></span> | <span data-ttu-id="94187-116">值</span><span class="sxs-lookup"><span data-stu-id="94187-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94187-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94187-117">Minimum supported client</span></span><br/> | <span data-ttu-id="94187-118">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94187-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="94187-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94187-119">Minimum supported server</span></span><br/> | <span data-ttu-id="94187-120">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94187-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="94187-121">標頭</span><span class="sxs-lookup"><span data-stu-id="94187-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="94187-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="94187-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94187-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94187-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94187-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="94187-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="94187-125">媒體類型</span><span class="sxs-lookup"><span data-stu-id="94187-125">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




