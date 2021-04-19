---
description: 包含描述 MFSampleExtension PhotoThumbnail 屬性中所包含之影像格式類型的 IMFMediaType \_ 。
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: 'MFSampleExtension_PhotoThumbnailMediaType 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106975598"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a><span data-ttu-id="02cde-103">MFSampleExtension \_ PhotoThumbnailMediaType 屬性</span><span class="sxs-lookup"><span data-stu-id="02cde-103">MFSampleExtension\_PhotoThumbnailMediaType attribute</span></span>

<span data-ttu-id="02cde-104">包含描述 [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)屬性中所包含之影像格式類型的 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 。</span><span class="sxs-lookup"><span data-stu-id="02cde-104">Contains the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) which describes the image format type contained in the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="02cde-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="02cde-105">Data type</span></span>

<span data-ttu-id="02cde-106">以 **IMFMediaType** 儲存的 **IUnknown**</span><span class="sxs-lookup"><span data-stu-id="02cde-106">**IUnknown** stored as **IMFMediaType**</span></span>

## <a name="remarks"></a><span data-ttu-id="02cde-107">備註</span><span class="sxs-lookup"><span data-stu-id="02cde-107">Remarks</span></span>

<span data-ttu-id="02cde-108">如果照片範例中有 [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md) 屬性，則需要 MFSampleExtension PhotoThumbnailMediaType， \_ 而且必須包含最小的 [mf \_ mt \_ 主要 \_ 類型](mf-mt-major-type-attribute.md)、 [mf \_ mt \_ 子類型](mf-mt-subtype-attribute.md) 和 [mf \_ mt \_ 框架 \_ 大小](mf-mt-frame-size-attribute.md) ，以描述縮圖。</span><span class="sxs-lookup"><span data-stu-id="02cde-108">If the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute is present on the photo sample, the MFSampleExtension\_PhotoThumbnailMediaType is required and must contain, at a minimum, [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md), [MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md) and [MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md) which describe the thumbnail.</span></span>

## <a name="requirements"></a><span data-ttu-id="02cde-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="02cde-109">Requirements</span></span>



| <span data-ttu-id="02cde-110">需求</span><span class="sxs-lookup"><span data-stu-id="02cde-110">Requirement</span></span> | <span data-ttu-id="02cde-111">值</span><span class="sxs-lookup"><span data-stu-id="02cde-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02cde-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02cde-112">Minimum supported client</span></span><br/> | <span data-ttu-id="02cde-113">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02cde-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="02cde-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02cde-114">Minimum supported server</span></span><br/> | <span data-ttu-id="02cde-115">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02cde-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="02cde-116">標頭</span><span class="sxs-lookup"><span data-stu-id="02cde-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="02cde-117"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="02cde-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02cde-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02cde-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02cde-119">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="02cde-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="02cde-120">MFSampleExtension \_ PhotoThumbnail</span><span class="sxs-lookup"><span data-stu-id="02cde-120">MFSampleExtension\_PhotoThumbnail</span></span>](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




