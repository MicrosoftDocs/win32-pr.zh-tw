---
description: 指定3D 影片框架如何儲存在媒體範例中。
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: 'MFSampleExtension_3DVideo_SampleFormat 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115012"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a><span data-ttu-id="7c4a8-103">MFSampleExtension \_ 3DVideo \_ SampleFormat 屬性</span><span class="sxs-lookup"><span data-stu-id="7c4a8-103">MFSampleExtension\_3DVideo\_SampleFormat attribute</span></span>

<span data-ttu-id="7c4a8-104">指定3D 影片框架如何儲存在媒體範例中。</span><span class="sxs-lookup"><span data-stu-id="7c4a8-104">Specifies how a 3D video frame is stored in a media sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="7c4a8-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7c4a8-105">Data type</span></span>

<span data-ttu-id="7c4a8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7c4a8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7c4a8-107">備註</span><span class="sxs-lookup"><span data-stu-id="7c4a8-107">Remarks</span></span>

<span data-ttu-id="7c4a8-108">這個屬性的值是 [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="7c4a8-108">The value of this attribute is a member of the [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) enumeration.</span></span>

<span data-ttu-id="7c4a8-109">產生3D 影片框架的元件應該在包含3D 框架的每個媒體範例上，將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="7c4a8-109">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span> <span data-ttu-id="7c4a8-110">如果 [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) 屬性為 **FALSE** 或未設定，則會忽略屬性。</span><span class="sxs-lookup"><span data-stu-id="7c4a8-110">The attribute is ignored if the [MFSampleExtension\_3DVideo](mfsampleextension-3dvideo.md) attribute is **FALSE** or not set.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4a8-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c4a8-111">Requirements</span></span>



| <span data-ttu-id="7c4a8-112">需求</span><span class="sxs-lookup"><span data-stu-id="7c4a8-112">Requirement</span></span> | <span data-ttu-id="7c4a8-113">值</span><span class="sxs-lookup"><span data-stu-id="7c4a8-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4a8-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7c4a8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7c4a8-115">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c4a8-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="7c4a8-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7c4a8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7c4a8-117">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7c4a8-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="7c4a8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7c4a8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c4a8-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c4a8-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c4a8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c4a8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4a8-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7c4a8-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7c4a8-122">MFSampleExtension \_ 3DVideo</span><span class="sxs-lookup"><span data-stu-id="7c4a8-122">MFSampleExtension\_3DVideo</span></span>](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




