---
description: 若為3D 影片格式，請指定哪個 view 是基底視圖。
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: 'MF_MT_VIDEO_3D_LEFT_IS_BASE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985042"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a><span data-ttu-id="bcf97-103">MF \_ MT \_ VIDEO \_ 3d \_ 左邊 \_ 是 \_ 基底屬性</span><span class="sxs-lookup"><span data-stu-id="bcf97-103">MF\_MT\_VIDEO\_3D\_LEFT\_IS\_BASE attribute</span></span>

<span data-ttu-id="bcf97-104">若為3D 影片格式，請指定哪個 view 是基底視圖。</span><span class="sxs-lookup"><span data-stu-id="bcf97-104">For a 3D video format, specifies which view is the base view.</span></span>

## <a name="data-type"></a><span data-ttu-id="bcf97-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="bcf97-105">Data type</span></span>

<span data-ttu-id="bcf97-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="bcf97-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf97-107">備註</span><span class="sxs-lookup"><span data-stu-id="bcf97-107">Remarks</span></span>

<span data-ttu-id="bcf97-108">根據預設，3D 影片順序中的左視圖是基底視圖。</span><span class="sxs-lookup"><span data-stu-id="bcf97-108">By default, the left view in a 3D video sequence is the base view.</span></span> <span data-ttu-id="bcf97-109">如果右視圖是基底視圖，請將此屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bcf97-109">If the right view is the base view, set this attribute to **FALSE**.</span></span>

<span data-ttu-id="bcf97-110">若要將 stereoscopic video 轉換成2D，請保留基底視圖，並捨棄另一個視圖。</span><span class="sxs-lookup"><span data-stu-id="bcf97-110">To convert stereoscopic video to 2D, keep the base view and discard the other view.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf97-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcf97-111">Requirements</span></span>



| <span data-ttu-id="bcf97-112">需求</span><span class="sxs-lookup"><span data-stu-id="bcf97-112">Requirement</span></span> | <span data-ttu-id="bcf97-113">值</span><span class="sxs-lookup"><span data-stu-id="bcf97-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf97-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcf97-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf97-115">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcf97-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="bcf97-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcf97-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf97-117">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcf97-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="bcf97-118">標頭</span><span class="sxs-lookup"><span data-stu-id="bcf97-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcf97-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf97-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf97-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcf97-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf97-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="bcf97-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




