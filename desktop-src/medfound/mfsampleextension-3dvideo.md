---
description: 指定媒體範例是否包含3D 影片框架。
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: 'MFSampleExtension_3DVideo 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976791"
---
# <a name="mfsampleextension_3dvideo-attribute"></a><span data-ttu-id="a7f5a-103">MFSampleExtension \_ 3DVideo 屬性</span><span class="sxs-lookup"><span data-stu-id="a7f5a-103">MFSampleExtension\_3DVideo attribute</span></span>

<span data-ttu-id="a7f5a-104">指定媒體範例是否包含3D 影片框架。</span><span class="sxs-lookup"><span data-stu-id="a7f5a-104">Specifies whether a media sample contains a 3D video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="a7f5a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a7f5a-105">Data type</span></span>

<span data-ttu-id="a7f5a-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="a7f5a-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a7f5a-107">備註</span><span class="sxs-lookup"><span data-stu-id="a7f5a-107">Remarks</span></span>

<span data-ttu-id="a7f5a-108">如果此屬性為 **TRUE**，則媒體範例包含具有兩個或更多 stereoscopic views 的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="a7f5a-108">If this attribute is **TRUE**, the media sample contains a video frame that has two or more stereoscopic views.</span></span> <span data-ttu-id="a7f5a-109">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a7f5a-109">The default value is **FALSE**.</span></span>

<span data-ttu-id="a7f5a-110">產生3D 影片框架的元件應該在包含3D 框架的每個媒體範例上，將此屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="a7f5a-110">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f5a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7f5a-111">Requirements</span></span>



| <span data-ttu-id="a7f5a-112">需求</span><span class="sxs-lookup"><span data-stu-id="a7f5a-112">Requirement</span></span> | <span data-ttu-id="a7f5a-113">值</span><span class="sxs-lookup"><span data-stu-id="a7f5a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f5a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7f5a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f5a-115">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7f5a-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a7f5a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7f5a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f5a-117">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7f5a-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a7f5a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a7f5a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7f5a-119"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a7f5a-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7f5a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7f5a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f5a-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a7f5a-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a7f5a-122">MFSampleExtension \_ 3DVideo \_ SampleFormat</span><span class="sxs-lookup"><span data-stu-id="a7f5a-122">MFSampleExtension\_3DVideo\_SampleFormat</span></span>](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




