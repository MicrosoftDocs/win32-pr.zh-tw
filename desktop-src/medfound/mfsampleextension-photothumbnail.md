---
description: 包含 IMFSample 的相片縮圖。
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: 'MFSampleExtension_PhotoThumbnail 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115000"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a><span data-ttu-id="f77df-103">MFSampleExtension \_ PhotoThumbnail 屬性</span><span class="sxs-lookup"><span data-stu-id="f77df-103">MFSampleExtension\_PhotoThumbnail attribute</span></span>

<span data-ttu-id="f77df-104">包含 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)的相片縮圖。</span><span class="sxs-lookup"><span data-stu-id="f77df-104">Contains the photo thumbnail of a [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span>

## <a name="data-type"></a><span data-ttu-id="f77df-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f77df-105">Data type</span></span>

<span data-ttu-id="f77df-106">以 **IMFMediaBuffer** 儲存的 **IUnknown**</span><span class="sxs-lookup"><span data-stu-id="f77df-106">**IUnknown** stored as **IMFMediaBuffer**</span></span>

<span data-ttu-id="f77df-107">縮圖會使用 **KSPROPERTYSETID \_ ExtendedCameraControl** 來設定。</span><span class="sxs-lookup"><span data-stu-id="f77df-107">The thumbnail is configured using the **KSPROPERTYSETID\_ExtendedCameraControl**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f77df-108">備註</span><span class="sxs-lookup"><span data-stu-id="f77df-108">Remarks</span></span>

<span data-ttu-id="f77df-109">這個屬性是在 MFT0 所提供的 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)上設定的，而且是與相片縮圖相關聯之 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="f77df-109">This attribute is set on the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) provided by the MFT0 and is the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associated with the photo thumbnail.</span></span>

<span data-ttu-id="f77df-110">相片縮圖的格式可以是 JPEG (主要類型影像) 、NV12 或 ARGB32。</span><span class="sxs-lookup"><span data-stu-id="f77df-110">The format of the photo thumbnail can be JPEG (major type image), NV12 or ARGB32.</span></span>

<span data-ttu-id="f77df-111">縮圖需要 [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) 來描述媒體類型。</span><span class="sxs-lookup"><span data-stu-id="f77df-111">The [MFSampleExtension\_PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) is required for thumbnails to describe the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f77df-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f77df-112">Requirements</span></span>



| <span data-ttu-id="f77df-113">需求</span><span class="sxs-lookup"><span data-stu-id="f77df-113">Requirement</span></span> | <span data-ttu-id="f77df-114">值</span><span class="sxs-lookup"><span data-stu-id="f77df-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f77df-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f77df-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f77df-116">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f77df-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="f77df-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f77df-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f77df-118">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f77df-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f77df-119">標頭</span><span class="sxs-lookup"><span data-stu-id="f77df-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f77df-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f77df-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f77df-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f77df-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f77df-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f77df-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f77df-123">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="f77df-123">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
